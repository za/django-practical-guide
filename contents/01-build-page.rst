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

Try to access the page using browser. Type into the browser's address bar - *http://localhost:8000/*.
You should see something like below:-

.. image:: /images/01-runserver-initial.png

Mapping URL to function
=======================
So how actually the page being generated ? How Django know to generate the page when user type
the URL such as *http://localhost:8000/* above ?

Django allow us to define a mapping between the url such as:-

    * http://localhost:8000/
    * http://localhost:8000/page/hello/
    * http://www.myshop.com/products/flash-card/
    * ...

To a certain a function that will be executed to return the output (response) to user. So url like
*http://localhost:8000/* can be mapped to function named `index()` and Django will call that function
whenever user request the url through their browser or any HTTP client.

.. note:: Browser like Google Chrome, Mozilla Firefox or Microsoft Internet Explorer are just one of HTTP
          client that can be used to access HTTP resources using URL. There are also command line clients
          like CURL or Wget that also can be used similar to browsers.

The process of mapping URL path to function (or any kind of handlers) also called **routing**. In Django,
this is done through `urlpatterns` configuration. Open file named `myshop/urls.py`
[:download:`download </src/myshop/urls.py>`] and you should see
the following code::

    from django.conf.urls import patterns, include, url
    from django.contrib import admin

    urlpatterns = patterns('',
        # Examples:
        # url(r'^$', 'myshop.views.home', name='home'),
        # url(r'^blog/', include('blog.urls')),

        url(r'^admin/', include(admin.site.urls)),
    )
