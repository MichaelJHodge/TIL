Django: A web framework (much heavier weight than Flask) that has more out-of-the-box features 
which would become repetitive with Flask (which is a micro-framework).

To start a new project, run: django-admin startproject projectname

Django creates a number of files with a new project:

  - __init__.py : defines the directory projectname as a Python ‘package’, a collection of multiple Python files
  Django is built on the idea of packages. A web application can be made up of multiple packages, each serving a 
  slightly different purpose, and Django will help manage these.
  - manage.py : a Python script that can be used to perform useful operations on a web application
  - settings.py : basic settings, like time zone, other applications installed in the project, what sort 
  of database is used, etc.
  - urls.py : determines what URLs/routes can be accessed when using the web application
  - wsgi.py : a file that helps to deploy an application to a web server
  - project_name/ : the directory for the project that contains all of the above files by default

A Django project is made up of one or more Django apps, all serving a certain purpose.

To creat an app, inside the project directory, run: python manage.py startapp appname

views.py is analogous to application.py (this contains the code that determines what the user sees
at certain routes). 
- This app will first look like: from django.shortcuts import render

urls.py (which is needed to specify routes) could look like: 

          from django.urls import path

          from . import views

          urlpatterns = [
              path("", views.index),
          ]

There will also be multiple url.py files, as each app will have its own routes. These separate url.py
files help signify differences in functionality, organize code, and make apps reusable/portable 

To run an app in Django: python manage.py runserver

MIGRATIONS
- When building a web application, all the tables will rarely be defined will all the 
correct columns from the beginning. Usually, tables are built up as the application grows, 
and the database will be modified. It would be tedious to change both the Django model code 
and run the SQL commands to modify the database.
- Django uses "migration" to combat this. It auto detects changes to models.py and auto generates
the needed SQL code to make the correct changes. 

DJANGO SHELL
- Django provides a shell (like Python's interpreter) which allows for direct modification
of the DB. Running the shell: python manage.py shell
- Inside this shell, Python commands can be run. 

TEMPLATES
- Like Flask, in order to render an HTML template, the rendered template should be returned by 
the function which handles a route. For Django, that’s in flights/views.py.
- Similar to the templating system with Jinja
- Django passes info into a template via the context directory

        from .models import Flight

        def index(request)
            context = {
                 "flights": Flights.objects.all()
            }
            return render(request, "flights/index.html", context)
          
ADMIN - a built in Django app that allows us to more easily add or modify existing
data on a web page. One of the most POWERFUL aspects of Django. 

Model Relationships
- We can implement (unlike with Flask and SQL) an 'in-between-table' that has 2 columns,
one for one attribute (like passenger ID) and another (like flight ID).
- Django allows for this and even auto implements this in-between table. 

Cross-site Request Forgery is a potential security vulnerability in forms whereby someone 
could forge where the form is coming from. Django is built in to protect these type of attacks.

Static Files: Django uses special syntax, such us:

        {% load static %}

        <!DOCTYPE html>
        <html>
            <head>
                <title>{% block title %}{% endblock %}</title>
                <link rel="stylesheet" href="{% static 'flights/styles.css' %}"/>
            </head>
            <body>
                {% block body %}
                {% endblock %}
            </body>
        </html>




 
 
