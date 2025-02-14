```
npm install pm2 -g
```

```
pm2 start npm --name "nextjs-app" -- start
pm2 startup
pm2 save
pm2 status
pm2 logs 'app-name'
```

```
nano start_django.sh
source /path/to/venv/bin/activate
python /path/to/your-django-app/manage.py runserver


chmod +x start_django.sh
pm2 start /path/to/start_django.sh --name "my-django-app"
```