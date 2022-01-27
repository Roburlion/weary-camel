# Weary Camel
This site was created using a personnel set of instructions

This site is up at https://weary-camel.herokuapp.com/

This app is a non working project stub without any apps.

The goal of this app is to get it on Heroku as quickly as possible, that way it can be used as an agile start for other project (like the library and polls tutorials)
> ### This site is published on heroku at https://weary-camel.herokuapp.com/
### push an existing repository from the command line
```bash
echo "# weary-camel-interactive" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/Roburlion/weary-camel.git
git push -u origin main
```
### create a new repository on the command line
```bash
git remote add origin https://github.com/Roburlion/weary-camel.git
git branch -M main
git push -u origin main
```

#### version 1

Now I have just the project base and nothing else.  This is as basic as it can get.  I want to see if I can get this up on heroku right now.

* Do I want to do CLI or Pipeline?

| CLI PRO             | CLI CON | PL PRO                                          | PL CON |
| ------------------- | ------- | ----------------------------------------------- | ------ |
| I've done it before |         | This is how I want to do my apps in the future. |        |

## Create Slug

Here, the bare minimum was setup.

I decided to go with "base" as my project name as it is will sit high in the file tree.  I will call my app, camel.

```bash
django-admin startproject base
cd base
git init && git add . && git commit -m "init"
```

> Logon to github and create and empty repo named weary-camel-interactive

```bash
git remote add origin https://github.com/Roburlion/weary-camel.git
git push -u origin master
```

```bash
manage.py runserver
```

Verified with Django success page.

## Setup venv

```bash
python -m venv env
env\Scripts\activeate
pip install --upgrade pip
pip install django
pip list
```

Create **requirements.txt** with:

```bash
django
gunicorn
django-heroku
requests
whitenoise
```

Create **runtime.txt** with:

```bash
python-3.10.2
```

Create **Procfile** with:

```
web: gunicorn base.wsgi
```

Create **.gitignore** with:

```
env
```

Push changes

```bash
git init && git add . && git commit -m "env and files created"
git push origin master
```

#### Configure static assets

See Heroku's [Django and Static Assets](https://devcenter.heroku.com/articles/django-assets "https://devcenter.heroku.com/articles/django-assets") for more info.

In **settings.py** replace **BASE_DIR** with

```
BASE_DIR = os.path.dirname(os.path.dirname(os.path.abspath(__file__)))
```

and add

```
import os

# Static files (CSS, JavaScript, Images)
# https://docs.djangoproject.com/en/1.9/howto/static-files/
STATIC_ROOT = os.path.join(BASE_DIR, 'staticfiles')
STATIC_URL = '/static/'

# Extra places for collectstatic to find static files.
STATICFILES_DIRS = (
    os.path.join(BASE_DIR, 'static'),
)
```



created base/static/nothing

created /staticfiles/nothing

Still not working

```bash
heroku config:set --app=weary-camel DISABLE_COLLECTSTATIC=1
```



## Setup heroku via pipeline

create blank app named **weary-camel**.

weary-camel > Deploy > Deployment method > **GitHub**

Click **search** and locate the **weary-camel-interactive** repo.

Select **Enable Automatic Deploys**

Select **Deploy Branch**

Failed to run.



## Everything else

