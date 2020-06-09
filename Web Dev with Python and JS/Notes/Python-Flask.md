Python is an interpreted language and can be used to build dynamic websites and web apps.

Data types:
-int
-float
-str
-bool
-none

Modules are separate .py files of code, often written by others, used in a new file without rewriting all the old code again. 

A class in Python is used to define a new, custom data type. 


Flask: A microframework writen in Python which allows us to start a simple web server.

'HTTP (Hypertext Transfer Protocol) is the system the internet uses to interact and communicate between computers and servers. When a URL is entered into a browser, an HTTP request is sent to a server, which interprets the request and sends appropriate HTTP response, which, if all goes as expected, contains the requested information to be displayed by the web browser.'

Flask code is usually found in app.py
Uses routes - parts of the URL that show which page is being requested. 

export FLASK_APP=application.py: ensures that application.py will be used as the web server.

Flask can return separate HTML files - which themselves should be stored in a 
'templates' directory.

Varibles are defined in the app.py file and can be passed as arguments within the HTML files.
Another language, Jinja2, helps render these templates. 

    headline = "Hello, world!"
    return render_template("index.html", headline=headline)
    
    --> In index.html : <h1>{{ headline }} </h1>
    
Session: How Flask keeps track of user data. 



