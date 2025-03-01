```
apt install apache2-utils
```


```
sudo htpasswd -c /etc/nginx/.htpasswd username
```

```
location / {
    auth_basic "Restricted Access";
    auth_basic_user_file /etc/nginx/.htpasswd;
    # ... rest of your location config
}
```