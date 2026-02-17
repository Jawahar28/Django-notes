# ORM , MODELS, ADMIN PANEL, Headless CMS:

# ORM : Object Relation Mapping 

* We had tables in RDBMS, within the table we have some features like columns , entries, relations, entity.

* Database is a collection of Tables , Table will have info about entity(user, order, payment) also known as object.

* Similar to RDBMS , in backend we have objects that are mapped to the entities in SQL with help of ORM.

# How we connect them with ORM?

* With the help of classes and properties, we can map the object to the entity.

* A class structure should represent entity.

# Creating MOdels:

* In the app, we have models.py file (or) we can create a models.py file in the project itself.

* In the models.py, first we should import the database

* Class structure :

    class class-name(models.Model):
        //
        entities:
        name, username, email,age,etc.

        //



* If we don't mention id the model class it doesn't effect the outcome since in the settings.py we have primary key set to default.

* We can change the database engine and name, in the settings.py

    1. change engine to 'SQL TOOL'.
    2. Create a Database in the tool : CREATE DATABASE "db_name".
    3. Change name to the created db_name.
    4. Add user to it. (Who is using/ where do we create tables)
    5. Add password (Your SQL Tool password for learning).
       - This password should not be mention during deployment/ for complex projects.
    6. Add Host to it. (whether local host or web domain host)
    7. Add Port(e.g. 3006, 5000, 8000, 3306)


* Whatever we write in the models, we should make migrations make updates/ changes/ create in the database which is connected in the backend.

    - To create migrations : python manage.py makemigrations(These will not appear in the database)

    - To commit migrations : python manage.py migrate(These will show the data in the database)

* We can see all the migrations, in the migrations folders.


# DJANGO - ADMIN : It populates the info of the user.

* 1. To add our own data,first we need to migrate our tables.

* 2. In our admin.py, first import our models from foldername.models import model_name.

* 3. Then register the model with admin.site.register(model_name).

* 4. We can add data in the Admin Panel, which reflects in the database automatically.

* 5. It usually behaves as CRUD(CREATE, READ, UPDATE, DELETE).

* 6. We can also provide entites like feilds = ["entitites"] and by providing @admin.register(model) instead of site.register.

* 7. We can also provide what to display like list_display = ["Entities to display instead of displaying all fields"], search_fields = ['Entitites used to search']

* 8. Fieldsets : It sets the fields like, product info as one block, stock info as another block and we can use classes : collapse to collapse or show.

* 9. We can use choices options to make choices for the entities.

* 10. We can use Foriegn Key to make connections between the models.

# HEADLESS CMS :

* CMS : Content Management System.

* It provides API's to the backend, so that the project will work without FrontEnd Part.



