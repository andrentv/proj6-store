criar pasta
git init
criar env / source <nameenv>/bin/activate
pip install django
django-admin startproject <nome> .
cd <nome>
python manage.py startapp <nomeapp>
python manage.py runserver

Options:
Criar pasta settings / arq base.py e heroku.py
setups em arq manage.py / base.py / heroku.py / wsgi.py / asgi.py

Ações
criar arq
requirements.txt
runtime.txt
Procfile
Pastas no root: static /staticfiles

heroku login
heroku create or heroku git:remote -a vacc-proj5-heroku
heroku config:set ALLOWED_HOSTS=vacc-proj5-heroku.herokuapp.com
heroku config:set DJANGO_SETTINGS_MODULE=proj5.settings.heroku
heroku config:set SECRET_KEY=()()()
heroku config:set DEBUG_VALUE=False
heroku addons
heroku addons:create heroku-postgresql:hobby-dev
heroku config:set DISABLE_COLLECTSTATIC=1
heroku run python manage.py makemigrations
heroku run python manage.py migrate
heroku run python manage.py createsuperuser
heroku run bash

heroku config:set ALLOWED_HOSTS=<endsiteheroku> -a, --app <nomeappheroku>




settings = django rest framework and insert code
serializer / view / urls (atention name of folder and dbase)

pip install django-cors-headers
alterações settings.py install apps/ middlaware/ code at bottom

deploy heroku
pip install django-on-heroku
pip install gunicorn whitenoise
heroku CLI


heroku login / confirmar com senha
pip freeze > riquirements.txt
pip install -r requirements.txt --upgrade
heroku git:remote -a <vacc-ecommercebackend> #inclui git remote
#settings incluir import heroku/os / alterar Debub=False / incluir host heroku / Middleware / static root and Staticfiles Storage / django_heroku bottom
git push heroku main

#Postgres
Criar servidor com as credenciais Heroku

#transferir dados
heroku run python manage.py makemigrations
heroku run python manage.py migrate
python manage.py dumpdata --natural-primary --natural-foreign > dump.json
commit again
heroku run python manage.py loaddata dump.json



# postgresql
# sudo -i -u postgres // psql -U antv
# sudo systemctl restart postgresql
# sudo nano /etc/postgresql/12/main/pg_hba.conf
# psql | \q | \list | \du | \password
# CREATE DATABASE <name>; #criar
# drop database <name>; #deletar
# ALTER ROLE 'user' PASSWORD 'novasenha';
# GRANT ALL PRIVILEGES ON DATABASE <data> to <user>;