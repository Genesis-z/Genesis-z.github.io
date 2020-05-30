---
layout: post
title:  "Django - Create your first project"
author: sal
categories: [ python ]
image: assets/images/python-django.png
beforetoc: " A step by step process to create your first project with Django"
toc: true
---

<!-- wp:paragraph -->
<p>Django is&nbsp; a high-level web application frame work with loads of features in it. Actually there are endless web frameworks out there in world !! Then why Django ?&nbsp;&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Because,&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:list {"ordered":true} -->
<ol><li>Its written in python, which is one of easy, most readable and user friendly programming language&nbsp;</li><li>The next comes the scope of its features. You don’t have to depend on external libraries if you need to build a website. It means the syntax is seamless here.&nbsp;</li><li>Don’t need to worry that updating one library or framework will render others that you’ve installed useless.&nbsp;If you do find yourself needing to add extra features, there are a range of external libraries that you can use to enhance your site.&nbsp;</li><li>One great thing is about its<a href="https://www.djangoproject.com/"> in-depth documentation</a></li><li>There is also fantastic Django developers community,&nbsp;so if you get stuck there’s almost always a way forward by either checking the docs or&nbsp;<a rel="noreferrer noopener" href="https://stackoverflow.com/questions/tagged/django" target="_blank">asking the community</a>.</li></ol>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p><strong>Structure of Django:&nbsp;</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>A Django consist of single project which can have multiple apps in it. The concept of having multiple apps is that each can handle a self-contained function that the site needs to perform. For example, Instagram is an application which might need several functions in it to perform like user management, private messaging, image feed etc,.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Django apps are structured so that there is a&nbsp;separation&nbsp;of logic. It supports the Model-View-Controller Pattern, which is the architecture on most of the web frameworks.&nbsp;The basic principle is that in each application there are three separate files that handle the three main pieces of logic separately:&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li><strong>Model</strong>&nbsp;defines the data structure. This is usually a database and is the base layer to an application.&nbsp;</li><li><strong>View</strong>&nbsp;displays some or all of the data to the user with HTML and CSS.&nbsp;</li><li><strong>Controller</strong>&nbsp;handles how the database and the view interact.&nbsp;</li></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>This is the basic concept on how it works. Let's&nbsp;use this and try to create a simple web app,&nbsp;&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>First Django Project :&nbsp;</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Lets&nbsp;create a separate directory for our project and activate the virtual environment. If you are using development tools like&nbsp;pycharm, the&nbsp;venv&nbsp;is created by default when you are starting a new project.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Now install Django&nbsp;&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>Pip install django </code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>The latest&nbsp;django&nbsp;version will be installed. Now,&nbsp;Lets create our&nbsp;django&nbsp;project now,&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>Django-admin startproject navbar_demo, 

root@Prince-PC:~/Desktop/Python_practise/navbar_demo# tree 
. 
├── db.sqlite3 
├── manage.py 
├── navbar_demo 
│   ├── asgi.py 
│   ├── __init__.py 
│   ├── settings.py 
│   ├── urls.py 
│   └── wsgi.py </code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Here is what each file inside the project is about,&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li>manage.py: A command-line utility that lets you interact with this Django project in various ways. You can read all the details about manage.py in&nbsp;<a href="https://docs.djangoproject.com/en/3.0/ref/django-admin/" target="_blank" rel="noreferrer noopener">django-admin and manage.py</a>.&nbsp;</li><li>The inner&nbsp;navbar_demo/ directory is the actual Python package for your project. Its name is the Python package name you’ll need to use to import anything inside it (e.g.&nbsp;mysite.urls).&nbsp;</li><li>navbar_demo/__init__.py: An empty file that tells Python that this directory should be considered a Python package. If you’re a Python beginner, read&nbsp;<a href="https://docs.python.org/3/tutorial/modules.html#tut-packages" target="_blank" rel="noreferrer noopener">more about packages</a>&nbsp;in the official Python docs.&nbsp;</li><li>navbar_demo/ettings.py: Settings/configuration for this Django project.&nbsp;<a href="https://docs.djangoproject.com/en/3.0/topics/settings/" target="_blank" rel="noreferrer noopener">Django settings</a>&nbsp;will tell you all about how settings work.&nbsp;</li><li>navbar_demo/urls.py: The URL declarations for this Django project; a “table of contents” of your Django-powered site. You can read more about URLs in&nbsp;<a href="https://docs.djangoproject.com/en/3.0/topics/http/urls/" target="_blank" rel="noreferrer noopener">URL dispatcher</a>.&nbsp;</li><li>navbar_demo/asgi.py: An entry-point for ASGI-compatible web servers to serve your project. See&nbsp;<a href="https://docs.djangoproject.com/en/3.0/howto/deployment/asgi/" target="_blank" rel="noreferrer noopener">How to deploy with ASGI</a>&nbsp;for more details.&nbsp;</li><li>navbar_demo/wsgi.py: An entry-point for WSGI-compatible web servers to serve your project. See&nbsp;<a href="https://docs.djangoproject.com/en/3.0/howto/deployment/wsgi/" target="_blank" rel="noreferrer noopener">How to deploy with WSGI</a>&nbsp;for more details.&nbsp;</li></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>check your&nbsp;django&nbsp;project with the below command,&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>python manage.py runserver </code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Create Django app as below,&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>Python manage.py startapp pages 

├── pages 
│   ├── admin.py 
│   ├── apps.py 
│   ├── __init__.py 
│   ├── migrations 
│   ├── models.py 
│   ├── tests.py 
│   └── views.py </code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Here is what every file inside the app is all about,&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li><strong>__init__.py</strong>&nbsp;tells Python to treat the directory as a Python package.&nbsp;</li><li><strong>admin.py</strong>&nbsp;contains settings for the Django admin pages.&nbsp;</li><li><strong>apps.py</strong>&nbsp;contains settings for the application configuration.&nbsp;</li><li><strong>models.py</strong>&nbsp;contains a series of classes that Django’s ORM converts to database tables.&nbsp;</li><li><strong>tests.py</strong>&nbsp;contains test classes.&nbsp;</li><li><strong>views.py</strong>&nbsp;contains functions and classes that handle what data is displayed in the HTML templates.&nbsp;</li></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>After you created your Django app, we need to add the app name in the installed apps.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>INSTALLED_APPS = [ 
'pages', 
'django.contrib.admin', 
'django.contrib.auth', 
'django.contrib.contenttypes', 
'django.contrib.sessions', 
'django.contrib.messages', 
'django.contrib.staticfiles', 
] </code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Now&nbsp;it's&nbsp;time to create your views, the function that displays you what you see in the webpage&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>Pages/views.py  ## file name
--------------
 
def index(request): 
context = {"home_page": "active"} # new info here 
return render(request, 'pages/index.html', context) 
def about(request): 
context = {"about_page": "active"} # new info here 
return render(request, 'pages/about.html', context) 
def contact(request): 
context = {"contact_page": "active"} # new info here 
return render(request, 'pages/contact.html', context) </code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>By default, the Django will look for the HTML templates inside each app in the project. So we are creating the templates for this project as below,&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>├── pages 
│   ├── templates 
│   │   └── pages 
│   │       ├── about.html 
│   │       ├── contact.html 
│   │       ├── index.html 
│   │       └── layouts 
│   │           ├── base.html 
│   │           └── navbar.html </code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>We need to create the html file inside the templates directory as below, templates directory should be followed by the directory named same as the app and then the HTML files will be created inside it.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Each app that we are creating in Django project should be having its urls.py file and it should be linked to urls.py file of the project. Therefore here's one for our project&nbsp;&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>Pages/urls.py 
--------------

from django.urls import path 
from . import views 
 
urlpatterns = [ 
path('', views.index, name='index'), 
path('about/', views.about, name='about'), 
path('contact/', views.contact, name='contact'), 
] </code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Link the pages/urls.py file to navbar_demo/urls.py file&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>from django.contrib import admin 
from django.urls import path, include 
 
urlpatterns = [ 
path('admin/', admin.site.urls), 
path('', include('pages.urls')), 
] </code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Let's make our HTML page little attractive by adding bootstrap CDN to our code. We need to add the&nbsp;css&nbsp;files locally in the static directory. It should be created in your project directory where you will be having the manage.py file and dbsqlite3.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>. 
├── db.sqlite3 
├── manage.py 
├── navbar_demo 
│   ├── asgi.py 
│   ├── settings.py 
│   ├── urls.py 
│   └── wsgi.py 
├── pages 
├── static 
│   └── css 
│       └── bootstrap.min.css </code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>This is because Django will check for the static files in the root directory as defined in the settings.py&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code># Static files (CSS, JavaScript, Images) 
# https://docs.djangoproject.com/en/3.0/howto/static-files/ 
 
STATICFILES_DIRS = ( 
os.path.join(BASE_DIR, 'static'), 
) 
STATIC_ROOT = os.path.join(BASE_DIR, 'staticfiles') 
 
STATIC_URL = '/static/' </code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>**Note: STATICFILES_DIRS and STATIC_ROOT can be changed as per the requirement **&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>You can also check this by using the below like,&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>Python manage.py findstatus css/bootstrap.min.css 
Python manage.py collectstatic </code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Now you have created your first&nbsp;django&nbsp;project successfully. Also given the code in git for your reference.&nbsp;&nbsp;</p>
<!-- /wp:paragraph -->

Here is the [Github](https://github.com/Dimension8d/Django_bootstrap) Link for the source code.

![webpage_snap]({{ site.baseurl }}/assets/images/python-django-2.png)

Hope this would be helpful...
