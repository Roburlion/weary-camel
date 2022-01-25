# Weary Camel Interactive
The goal of this app is to get it on Heroku as quickly as possible, that way it can be used as an agile start for other project (like the library and polls tutorials)
> ### This site is published on heroku at https://weary-camel.herokuapp.com/
### push an existing repository from the command line
```bash
echo "# weary-camel-interactive" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/Roburlion/weary-camel-interactive.git
git push -u origin main
```
### create a new repository on the command line
```bash
git remote add origin https://github.com/Roburlion/weary-camel-interactive.git
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
git remote add origin https://github.com/Roburlion/weary-camel-interactive.git
git push -u origin master
```

