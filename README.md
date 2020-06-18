# WordPress

### !ACHTUNG!
WordPress работает без proxy_pass в Nginx.
UPD: Чтобы исправить эту проблему нужно убрать Apache.

##### Installation
1. Клонировать репозиторий на хост.
2. Запустить script.sh для установки docker и docker-compose.
3. Перезайти в систему.
4. Запустить ```docker-compose up -d``` 
5. В браузере перейти на IP адресс хоста и настроить WordPress.

####### Issues
```
Connection Information
To perform the requested action, WordPress needs to access your web server.
Please enter your FTP credentials to proceed. 
If you do not remember your credentials, you should contact your web host.
```
Fix:
```
chown -Rf www-data.www-data /var/www/html/
```
