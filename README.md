# Writing my First Django App

## How to create Django App ?

 $ python -m django --version
 
    If Django is installed, you should see the version of your installation.
    If it isn’t, you’ll get an error telling “No module named django”
 
 From the command line, cd into a directory where you’d like to store your code, then run the following command:

 $ django-admin startproject mysite
  This will create a mysite directory in your current directory. If it didn’t work, see [here for the details](https://docs.djangoproject.com/en/1.11/faq/troubleshooting/#troubleshooting-django-admin)
  
  Let’s look at what startproject created:

    mysite/
        manage.py
        mysite/
            __init__.py
            settings.py
            urls.py
            wsgi.py
            
            ⋅⋅* The outer **mysite/** root directory is just a container for your project. Its name doesn’t matter to Django; you can rename it to anything you like.
            ⋅⋅* **manage.py**: A command-line utility that lets you interact with this Django project in various ways. You can read all the details about
            ⋅⋅* **The inner mysite/** directory is the actual Python package for your project. Its name is the Python package name you’ll need to use to import anything inside it (e.g. mysite.urls).
            ⋅⋅* **mysite/__init__.py**: An empty file that tells Python that this directory should be considered a Python package. If you’re a Python beginner, read more about packages in the official Python docs.
            ⋅⋅* **mysite/settings.py**: Settings/configuration for this Django project. Django settings will tell you all about how settings work.
            ⋅⋅* **mysite/urls.py**: The URL declarations for this Django project; a “table of contents” of your Django-powered site. You can read more about URLs in URL dispatcher.
            ⋅⋅* **mysite/wsgi.py**: An entry-point for WSGI-compatible web servers to serve your project. See How to deploy with WSGI for more details.
            
            
# The development server:
     Let’s verify your Django project works. Change into the outer mysite directory, if you haven’t already, and run the following commands:

    $ python manage.py runserver
    You’ll see the following output on the command line:

    Performing system checks...

    System check identified no issues (0 silenced).

    You have unapplied migrations; your app may not work properly until they are applied.
    Run 'python manage.py migrate' to apply them.

    November 01, 2017 - 15:50:53
    Django version 1.11, using settings 'mysite.settings'
    Starting development server at http://127.0.0.1:8000/
    Quit the server with CONTROL-C.
            
Everthing That I told above is taken from the [Django-Document Official website](https://docs.djangoproject.com/en/1.11/intro/tutorial01/)
