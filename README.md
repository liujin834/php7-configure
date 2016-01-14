# configure script

## don't forget change '--prefix' ,'--with-fpm-user' ,'--with-fpm-group' in the script!

recommend `--prefix` is `/opt/server/nginx` and `/opt/server/php`

# etc config files
```shell
├── init.d
│   └── nginx
├── nginx
│   ├── conf.d
│   │   └── black_list.conf
│   ├── fastcgi_params
│   ├── mime.types
│   ├── nginx.conf
│   ├── proxy_params
│   └── sites-enabled
│       └── example.conf
└── php
    ├── php-fpm.conf
    ├── php-fpm.d
    │   └── www.conf
    └── php.ini
```

you can move nginx and php config file to `/opt/server/etc`

# install nginx service on ubuntu

```shell
sudo chmod u=rwx,g=rx,o=x /etc/init.d/nginx
sudo update-rc.d nginx enable  2 3 4 5  //ubuntu 16.04
sudo update-rc.d nginx start 20 2 3 4 5 . stop 20 0 1 6 //ubuntu 15.04 and lower
```
