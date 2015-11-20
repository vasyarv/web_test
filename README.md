# Как сделать в python-social-auth нормального админа

`python3 manage.py createsuperuser`

Ставим sqlite3 и заходим в консоль

`attach "mydb.sqlite" as db1;`

`SELECT name FROM db1.sqlite_master WHERE type='table';`

Далее исполняем, но нужно подправить название модуля

`select * from vkmodule_userprofile;`  

Чтобы узнать название строчек:

`PRAGMA table_info('table_name');`

`update vkmodule_userprofile set is_superuser=1 where username="admin";`


