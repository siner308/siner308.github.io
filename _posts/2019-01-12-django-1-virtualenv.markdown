---
title:  "Start Django (1)"
subtitle: "with virtualenv"
author: "Siner"
avatar: "img/authors/siner.jpeg"
image: "img/django-words.png"
categories:
- django
date:   2019-01-06 21:57:00
---
There is two requirements to start Django.

- **virtualenv** (virtual environment) for executing Django
- **Django** installed in virtualenv

install these two things and start the Django project.


## 1) Install pip
  check this link : [https://pip.pypa.io/en/stable/installing/](https://pip.pypa.io/en/stable/installing/)
  
  ```python
  curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
  python get-pip.py
  ```

## 2) Install virtualenv
  ```python
  pip install virtualenv
  ```

## 3) Create virtualenv
  ```python
  virtualenv -p python3 venv_for_django
  ```

## 4) Activate virtualenv
  ```python
  source venv_for_django/bin/activate
  ```

## 5) Check python version
  ```python
  python --version
  ```

For **Django2.0**, **python3** must be installed in virtualenv
So, we input **-p python3** option when we create virtualenv.

(If you didn't input this option, maybe python2 will be default, **Django1.1(deprecated) will be installed.**)

![image](https://user-images.githubusercontent.com/34048253/50682089-0d1e5d80-1051-11e9-947a-d7b222ee2912.png)


## 6) Install Django
  ```python
  pip install django
  ```

![image](https://user-images.githubusercontent.com/34048253/50682114-27f0d200-1051-11e9-99ce-89e17965b271.png)



## 7) Create Django project
Very simple to create Django project
Just command one line in virtualenv installed Django following below.

  ```python
  django-admin startproject myproject
  ```

![image](https://user-images.githubusercontent.com/34048253/50682121-2fb07680-1051-11e9-8eb6-aa221b4c5d35.png)



## 8) Start Django project
Just execute **python manage.py runserver** located in myproject with **ip**, **port** option

  ```python
  python manage.py runserver 0.0.0.0:8000
  ```

![image](https://user-images.githubusercontent.com/34048253/50682135-3808b180-1051-11e9-9929-48e4cc492774.png)

![image](https://user-images.githubusercontent.com/34048253/50682139-3dfe9280-1051-11e9-9a1f-fb3c55fd8283.png)

When we trying to connect **hostip:8000**, we will get something yellow screen with ALLOWED_HOSTS error.
So we add our host IP to ALLOWED_HOSTS list.

ALLOWED_HOSTS option will be exist in **myproject/settings.py**


So go there, and edit.

![image](https://user-images.githubusercontent.com/34048253/50682146-448d0a00-1051-11e9-945a-8be58e023651.png)

![image](https://user-images.githubusercontent.com/34048253/50682155-4a82eb00-1051-11e9-91dd-2cf0ac9cc2c5.png)


After editing, runserver again, we can get result below. 

![image](https://user-images.githubusercontent.com/34048253/50681554-4524a100-104f-11e9-9cf9-07d10b780561.png)
