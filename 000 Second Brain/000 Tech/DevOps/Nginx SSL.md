This is the official instruction

```
sudo apt update
sudo apt install snapd
sudo snap install --classic certbot
sudo ln -s /snap/bin/certbot /usr/bin/certbot
```

This is an old way of installing it 
```
apt-get update
sudo apt-get install certbot
apt-get install python3-certbot-nginx
```

```
sudo certbot --nginx -d example.com -d www.example.com
```

> [!WARNING]
> Make sure that firewall allows access on port 443.

