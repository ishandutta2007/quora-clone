# Quora clone
Quora clone written in Django.

![alt tag](http://i.imgur.com/vj4TQFg.jpg)

### Installation
```
# clone repo
git clone https://github.com/econti/quora-clone.git
# go into repo
cd quora-clone
# make a virtual environment
virtualenv env
# start the env
. env/bin/activate
# install the requirements
pip install -r requirements.txt
```
Now set up your db. Install postgres and make sure you are running it.
```
psql
create database quora;
```

Now set up the environment variables.
```
# make .env file in root of directory with following variables
DEBUG=True
SECRET_KEY='mys3cr3tk3y'
DATABASE_URL='postgres://<your_pg_username>:p4ssw0rd@localhost:5432/quora'
```

Now run the database migrations
```
python manage.py migrate
```
Now run the server
```
python manage.py runserver
```
Head to `http://127.0.0.1:8000/`

### Fb Auth & Authenticating users
There are two ways to create users. One via fb authentication and the other via the app's authentication.

For the app's native authentication vist `localhost:8000/hidden_login`. To set up fb auth simply create a new fb app and modify the following variables in `settings.py`.
```
SOCIAL_AUTH_FACEBOOK_KEY = ''
SOCIAL_AUTH_FACEBOOK_SECRET =''
```
### Admin Site

Create superuser for admin site
```
python manage.py createsuperuser
```

Head to `http://127.0.0.1:8000/admin`

### Support:

If you want the good work to continue please support us on

* [PAYPAL](https://www.paypal.me/ishandutta2007)
* [BITCOIN ADDRESS: 3LZazKXG18Hxa3LLNAeKYZNtLzCxpv1LyD](https://www.coinbase.com/join/5a8e4a045b02c403bc3a9c0c)
