

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

  - [What is Django](#what-is-django)
  - [Setting up development environment](#setting-up-development-environment)
  - [Creating Django boilerplate environment](#creating-django-boilerplate-environment)
  - [Django Views](#django-views)
  - [Create `url.py` file inside the app folder](#create-urlpy-file-inside-the-app-folder)
  - [Django Templates](#django-templates)
- [Django Rest Framework](#django-rest-framework)
  - [Installation](#installation)

<!-- /code_chunk_output -->

<hr>

https://open.spotify.com/track/2JhU9tkEJqUsjjr37cIpdG?si=fc6e345c6f764967# Django
## What is Django
- free open source framework for building web applications with python
    - less time & less code compared to other frameworks
- Features out of the box: 
    - admin panel
    - object-relational mapper
    - user authentication
    - caching

## Setting up development environment
- make sure python & python3 are up to date and pipenv is installed

## Creating Django boilerplate environment
- `pipenv install django`
    - this creates a virtualenv, the path will be stated under "Virtualenv location:"
- `pipenv shell` 
    - python interpreter 
    - make sure that you enter the virtual environment in the python interpreter if you are using vscode integrated terminal
    - [command shift P] is the command, type in "<b>python: select interpreter</b>", make sure the enter the correct path
    - <b>to find the correct path</b>: `pipenv --venv` 
        - copy that path and paste it into the interpreter panel 
- `django-admin`
    - this shows you all the commands you can use with 'django-admin'
- `django-admin startproject <project name> .`
    - initializes project files
    - the period "." signifies that django should use the current directory as its main directory, instead of creating another, redundant, directory
- `python manage.py startapp <app name>`
    - initializes app files
    - make sure to include the app name inside of the INSTALLED_APPS list in the settings.py file

## Django Views
- view functions are functions that take a request and return a response, a request handler / action
- essentially functions that are called when, mapped to a url, the url is called

## Create `url.py` file inside the app folder
- create a `urlpatterns` list to establish your paths
    - these paths will contain the url endpoint, and the view that will be called when that endpoint is accessed
- if you are creating a lot of urls that may start with the same endpoint, i.e "store/shop", "store/cart", "store/sale"
    - you can go into the `urls.py` inside the <b>project</b> folder, and import "include" from django.urls
    - then you can add a path inside the urlpatterns list that would look like this: 
        - `path('store/', include('store.urls'))`
    - this makes it so that inside the app, you don't have to include "store" in your url paths, you can just use "cart/", "shop/", etc. 
    - the `include('store.urls')` will direct all endpoints that start with "store/" to point to "store.urls"

## Django Templates
- create a templates folder inside the app folder
- inside this template you can create html 

# Django Rest Framework
- used for building out APIs
## Installation 
- `pip install djangorestframework`
- add <b>rest_framework</b> to INSTALLED_APPS
## Serializing Data
- this allows us to return any model object in a JSON response to access from an api call
- `serializers.py` inside app
