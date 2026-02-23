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

* Body: Body is being used to make a request from browser, some other client like(Android App), 