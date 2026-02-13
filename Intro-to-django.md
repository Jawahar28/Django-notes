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
* 7. To see the list of Django Commmands : python -m manage.py --help
* 8. Type python -m 'manage.py --help <subcommand>' for help on a specific subcommand.
* 9. To create a user : python manage.py createsuperuser

# Apps :
# Exploring the Django project :

* settings.py - This is the way we customize your django application.

    * Allowed Hosts means it will grant access to those urls only which we mention in the list.
        Ex: localhost:3000, localhost:8000 etc.

    * If Debug is False, It will show empty page even though we allowed the hosts.

    * Installed Apps: Django Architecture works in the thought-process of applications.

    * We will be working on Databases.

    * Auth Password validations: Providing different password validations to work.

    * Middleware : The request that I would be getting are, have these applications but after I get the request , I want to process that request.
    
* urls.py : List of urls available for the project. We will be a providing for which url we are redirecting the url.

* At first, if we run the admin site and enter the credentials, it shows us that the table doesn't exist. This is because "Django" will not know on the structure as it leads to error. So to propagant this we need to migrate the tables and run the server , now we will see " Enter the correct credentials" . Now we need to create a "User" and and make the project run successfully.


# Views : It would populate the response for the URL.

* Writing a view : 
    1. First import : from django.http import HttpResponse / whatever module you would like to print

    2. define function_name(request):
            // code

            return response("")

* Writing a view in URLpatterns in urls.py is very important to see what we have written.

* In the URLPatterns : path("whatever the url name you want to redirect/endpoint", function_name)

* What we can have vs what we can't have  in Views :

    1. For a single request, we can have only one view.
    2. We don't need to have separate files for separate views.
        For better approach : 
            a. Create a Folder/Python Package name Views.
            b. Within this folder add views.py files.
            c. Create a __init__.py file to import the views and make it a module.
            d. Then import the views in the init file.

