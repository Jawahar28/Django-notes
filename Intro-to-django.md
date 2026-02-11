# Django : It is a Framework used for building web applications using Python.

* Django is a combination of multiple small applications.

* Framework  vs Library:

    -> Library : I will create some utility for you, I wouldn't have preconseve notion about stuff , it's just more of utility stuff and now how you utilise it is totally dependent on you.

    -> Framework : I will have some structure, patterns created for you and what you do is fill in the places and then you are good to go.

                    These will have combination of API's request responses,
                    Auth, sessions, Database, Middlewares and many more.
    
* Some Example frameworks for Python Web Dev are: Flask, Django, FastAPI.

* Tools Needed : VSCode/Pycharm, 
                 Postman(Requests are coming from this)
                 Python3

* To see the commands for manage.py file : python -m manage --help
* To see all the django commands : python manage.py --help

# Django Commands :

* 1. To start project : django-admin startproject "project-name" .
* 2. To start new application : django-admin startapp "app-name"
* 3. To run the server : python manage.py runserver
* 4. To See the updates in the tables in db: python manage.py makemigrations
* 5. To update the changes : python manage.py migrate
* 6. To Quit the server : Ctrl + C


# Exploring the Django project :

* settings.py - This is the way we customize your django application.

    * Allowed Hosts means it will grant access to those urls only which we mention in the list.
        Ex: localhost:3000, localhost:8000 etc.

    * If Debug is False, It will show empty page even though we allowed the hosts.

    * Installed Apps: Django Architecture works in the thought-process of applications.

    * We will be working on Databases.

    * Auth Password validations: Providing different password validations to work.
 
