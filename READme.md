

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [What is Django](#what-is-django)
- [Setting up development environment](#setting-up-development-environment)
- [Creating django boilerplate environment](#creating-django-boilerplate-environment)

<!-- /code_chunk_output -->

<hr>

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

## Creating django boilerplate environment
- `pipenv install django`
    - this creates a virtualenv, the path will be stated under "Virtualenv location:"
- `pipenv shell` 
    - python interpreter 
    - make sure that you enter the virtual environment in the python interpreter if you are using vscode integrated terminal
    - [command shift P] is the command, type in "python: select interpreter", make sure the enter the correct path
    - <b>to find the correct path</b>: `pipenv --venv` 
        - copy that path and paste it into the interpreter panel 
- `django-admin`
    - this shows you all the commands you can use with 'django-admin'
- `django-admin startproject <project name .>`
    - initializes project files
    - the period "." signifies that django should use the current directory as its main directory, instead of creating another, redundant, directory