# API, REST API, DJANGO+REST, SERIALIZERS

# API: Application Programming Interface

* It's like Exposed functions.

* Web API: Exposed functions over web.
           We use HTTP protocol for web requests.

* HEADERS : GET AND POST.


* Component of GET request : address / queries

* We can't send the payload(body) in the GET request.

* Eg: Just URL/ http of the page.(Instagram)

* If we wan't to use Instagram, we do 'GET request' for the home page without creadentials/ home page details(doesn't need payload to generate)

* Component of POST request : payloads

* Here payloads plays a major role in the POST request.

* Eg: In the Instagram Home Page, we see the login/signup , these require body to generate. So we do "POST request" to use the website/url.

* Having URLs like : createuser/, deleteuser/, fetchuserinfo/ use some methods to create, update, delete, read posts.
                     

* Same like CRUD, In API we have GET(Read), POST(Create), PUT(Update), DELETE(delete).

* Body: Body is being used to make a request from browser, some other client like(Android App), It contains all the parts of the request/ webpage.

# What is JSON?

* A JSON data looks like a dictionary(Key- Value Pair) in Python.

* You accessed:

        http://127.0.0.1:8000/users/POST/

        But in your urls.py, you only defined:

        say_hello/<name>
        admin/
        users/

* There is no URL pattern for users/POST/, so Django throws a 404.

        🔍 What’s Actually Happening

        In Django:

        GET, POST, PUT, etc. are HTTP methods

        They are NOT part of the URL

        You don’t write them in the browser URL

        So this:

        users/POST/

        means you're treating POST like a URL path parameter.

* Correct Way to Handle POST in Django

        You should:

        Keep URL as /users/

        Handle POST inside the view

        Example
        🔹 urls.py
        from django.urls import path
        from . import views

        urlpatterns = [
            path('users/', views.users_view),
        ]
        🔹 views.py
        from django.http import HttpResponse

        def users_view(request):
            if request.method == "GET":
                return HttpResponse("This is GET request")

            elif request.method == "POST":
                return HttpResponse("This is POST request")
*  How to Send a POST Request

        You CANNOT send POST by typing URL in browser.

        Instead use:

        Postman

        curl

        HTML form

        JavaScript fetch

        Django test client

    * Example using curl:
        curl -X POST http://127.0.0.1:8000/users/
        🎯 Why Django Shows That List

        Django tried matching:

        say_hello/<name>
        admin/
        users/

        But you gave:

        users/POST/

        No match → 404.

* Important Concept (Interview Tip)

        URL = Resource
        HTTP Method = Action

        Example:

        GET    /users/      → get users
        POST   /users/      → create user
        PUT    /users/1/    → update user
        DELETE /users/1/    → delete user

        Same URL, different methods.