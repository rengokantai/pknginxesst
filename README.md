#### pknginxesst

- cp4
to use auth_basic and auth_basic_user_file

create password file by using htpasswd:
```
htpasswd -b -d -c /etc/nginx/auth.d/auth.pwd username pass  # create new file and add user
htpasswd -b -d -c /etc/nginx/auth.d/auth.pwd username pass  # add user or set new password
htpasswd -D /etc/nginx/auth.d/auth.pwd username #  Delete user
```
Default encrypt method is crypt,not so strong.
Install ssha:
```
apt-get install slapd
```
To encrypt a string:
```
slappasswd -s pass
```
