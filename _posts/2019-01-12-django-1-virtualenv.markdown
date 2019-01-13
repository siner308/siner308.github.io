---
layout: post
title:  "Start Django (1)"
subtitle: "with virtualenv"
author: "Siner"
header-img: "img/django/django-virtualenv.jpg"
catalog: true
tags:
    - django
    - virtualenv
    - python
    - webserver
date:   2019-01-12
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
![image](https://user-images.githubusercontent.com/34048253/51082217-18a31000-1746-11e9-94b3-2cdfb6039ca4.png)


## 2) Install virtualenv
  ```python
  pip install virtualenv
  ```
![image](https://user-images.githubusercontent.com/34048253/51082225-3a9c9280-1746-11e9-9bc4-91a05049b0de.png)

## 3) Create virtualenv
  ```python
  virtualenv -p python3 venv_for_django
  ```
![image](https://user-images.githubusercontent.com/34048253/51082232-4be59f00-1746-11e9-8eac-5f11b63184f6.png)

## 4) Activate virtualenv
  ```python
  source venv_for_django/bin/activate
  ```
![image](https://user-images.githubusercontent.com/34048253/51082234-59028e00-1746-11e9-8200-7bce0f604007.png)

## 5) Check python version
  ```python
  python --version
  ```

For **Django2.0**, **python3** must be installed in virtualenv
So, we input **-p python3** option when we create virtualenv.

(If you didn't input this option, maybe python2 will be default, **Django1.1(deprecated) will be installed.**)


![image](https://user-images.githubusercontent.com/34048253/51082240-89e2c300-1746-11e9-9444-018887dd64b2.png)

## 6) Install Django
  ```python
  pip install django
  ```

![image](https://user-images.githubusercontent.com/34048253/51082246-9c5cfc80-1746-11e9-856e-11fbf902c6a8.png)



## 7) Create Django project
Very simple to create Django project
Just command one line in virtualenv installed Django following below.

  ```python
  django-admin startproject myproject
  ```
![image](https://user-images.githubusercontent.com/34048253/51082256-d0382200-1746-11e9-86bc-5dd2ca6659bc.png)


## 8) Start Django project
Just execute **python manage.py runserver** located in myproject with **ip**, **port** option

  ```python
  python manage.py runserver 0.0.0.0:8000
  ```
![image](https://user-images.githubusercontent.com/34048253/51082269-01b0ed80-1747-11e9-84fe-e045bdb44691.png)

## 9) ALLOWED_HOSTS
![image](https://user-images.githubusercontent.com/34048253/51082279-5d7b7680-1747-11e9-9674-6e49b2eb9612.png)

When we trying to connect **hostip:8000**, we will get something yellow screen with ALLOWED_HOSTS error.
So we add our host IP to ALLOWED_HOSTS list.

ALLOWED_HOSTS option will be exist in **myproject/settings.py**


So go there, and edit.
![image](https://user-images.githubusercontent.com/34048253/51082397-76852700-1749-11e9-9d75-9a4853fee34d.png)
![image](https://user-images.githubusercontent.com/34048253/51082295-be0ab380-1747-11e9-87cb-fca9b5e81e32.png)


## 10) Result
After editing, runserver again, we can get result below. 
![image](https://user-images.githubusercontent.com/34048253/51082317-0f1aa780-1748-11e9-91b7-2a6c99a98b4b.png)

