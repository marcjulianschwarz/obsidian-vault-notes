# Nginx Gunicorn Flask 

```shell
sudo apt update 
sudo apt upgrade

sudo apt install nginx
sudo nginx
```

```shell
sudo adduser test
```

Remove user 

```bash
sudo deluser --remove-home ubuntu
```

## Create Flask app 

Create the flask app with the test user. 

```shell
wget "https://repo.anaconda.com/miniconda/Miniconda3-py310_23.3.1-0-Linux-x86_64.sh"
bash Miniconda3-latest-Linux-x86_64.sh
```

or use [Python Virtual Environments: A Primer – Real Python](https://realpython.com/python-virtual-environments-a-primer/)


```shell
conda create -n "test" python=3.10 pip
```

```shell
pip install flask gunicorn
```

Create a wsgi.py file 

```python
# first is filename, second is app name in file
from app import app

if __name__ == "__main__":
        app.run()
```
## Create Flask Service 

```shell
nano /etc/systemd/system/flaskapp.service
```

Add to the file:
```shell
[Unit]
Description=Guincorn serving flask app 
# only start service when there is a network connection 
After=network.target    

[Service]
User=<user>
Group=www-data
WorkingDirectory=/home/<user>/<cwd>
Environment="PATH=/home/<user>/miniconda3/envs/<env>/bin"
# start gunicorn server with 3 workers that handle icoming requests 
# bind to unix socket (inter process communitcation)
# wsgi:app (module:app-instance)
ExecStart=/home/<user>/miniconda3/envs/<env>/bin/gunicorn --workers 3 --bind unix:<service>.sock -m 007 wsgi:app

[Install]
WantedBy=multi-user.target
```

Enable (service will start after system start) and start the service for the current session.
```shell
sudo systemctl enable flaskapp.service
sudo systemctl start flaskapp.service
```

When changing flask app restart service.
```shell
sudo systemctl restart flaskapp.service
```

## Nginx Config 

Comment out default config in 
```shell
nano /etc/nginx/sites-available/default
```

Add new server config in 
```
nano /etc/nginx/sites-available/app.conf
```

Content 
```shell
server {
        listen 80;
        server_name test.marc-julian.de;

		# all requests on /api will be forwarded to the flaskapp unix socket where gunicorn will see them and forward to flask
        location /api {
                include proxy_params;
                proxy_pass http://unix:/home/test/flaskapp/flaskapp.sock;
        }

		# all other requests on root will be served by the /data/www directory 
        location / {
                root /data/www;
        }

		# all /images requests will be served by the /images directory
        location /images {      
                root /images;   
        }
}
```

This file is automatically included in the nginx.conf file. Only need to sym-link it to the sites-enabled directory.

```shell
sudo ln -s /etc/nginx/sites-available/app.conf /etc/nginx/sites-enabled/app.conf
```

## Node 


[GitHub - nvm-sh/nvm: Node Version Manager - POSIX-compliant bash script to manage multiple active node.js versions](https://github.com/nvm-sh/nvm)
use newest script 

```
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
```


```
nvm install node
exit
```

## Memory 

```
free -M
```

