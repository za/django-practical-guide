*************************
LESSON 01 - Build a Page
*************************
This is definitely the first thing everyone learning web development would like to do.
How to display something when user type URL like 'www.mywebsite.com' in their browser
address bar. We'll learn how to do it in this chapter using Django.

Start Django Project
====================
Assuming :doc:`Django properly installed </contents/prework>`, we can run the
following command::

    django-admin startproject myshop .

Above command will create a new directory called `myshop` in your current directory. It should
look like below when you run command `tree .` in your current directory::

    .
    ├── manage.py
    └── myshop
        ├── __init__.py
        ├── settings.py
        ├── urls.py
        └── wsgi.py

    1 directory, 5 files

This is an initial structure for our Django project. We can try to run it using command::

    python manage.py runserver

You should see an output like below::

    Performing system checks...

    System check identified no issues (0 silenced).

    You have unapplied migrations; your app may not work properly until they are applied.
    Run 'python manage.py migrate' to apply them.

    December 24, 2014 - 01:52:42
    Django version 1.7.1, using settings 'myshop.settings'
    Starting development server at http://127.0.0.1:8000/
    Quit the server with CONTROL-C.

This mean your new Django project now ready to serve a request from browser or any HTTP client
and will return a response.

.. todo::
   Should we put the error when `python manage.py migrate` not run or just include the command
   above before running `manage.py runserver` ?
