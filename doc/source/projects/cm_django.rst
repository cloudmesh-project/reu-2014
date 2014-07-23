Cloudmesh Django
======================================================================

Team
----------------------------------------------------------------------

.. image:: ../images/image.jpg
   :height: 100


* Jeff Ridgeway, jdridgeway4@gmail.com
* Gregor von Laszewski, laszewski@gimail.com

Problem
----------------------------------------------------------------------

The cloud computing system Cloudmesh currently uses flask as a backend.
Even though flask is easier to use than django, django has become very favored
in the cloud computing community as of recently.  The purpose of this project is
to develop a prototype django server that will have sets of functions that will 
make Cloudmesh as applicable using django than to use flask.  The documentation
on django is varied and comprehensive and in achieving the purpose of the project, 
simple gudies and examples will be conducted for future use by the cloudmesh team
to shift or clone the flask framework to django.  These examples will incorporate
how to develop concrete views and models using the database known as mongodb to
reflect from the database.  This framework will also include attaching a
bootstrap theme to the django server and list of virtual machines on various 
clouds that currently use Cloudmesh databases.

**Keywords:** Cloudmesh, django, bootstrap theme, flask, views, models

Plan of Action:

* Week 1: Learn basic tools: python, git , django
* Week 2: Set up various simple django web servers includining the
  simple server and one that uses the bootstrap theme. Evaluate if we
  can interact with mongo or mongo engine. assess at the end of the
  week changes to the project based on what we find out
* Week 3: Develop views and models and templates that display some
  data, while the initial test could use sqllite, we want out views
  and models to interact with mongo db. Save and document each case in
  its own directory
* Week4: put some real data into the database, such as the reservation
  data from Natiele or the user data from Ifeanyi and create views for
  them. Create a view that displays the ploticus image that Gregor
  creats from the reservation information. Develop views for projects
  and roles.
* Week 5: inspect a real cloudmesh db and create views for some of teh
  data. Examples are profile, images, flavors, inventory.
* Week 6-7: complete the implementation and documentation
* Week 8: complete the 2 page paper and complete the documentation for
  the cloudmesh team, make sure that the code is documented.

Tip:

* pylint, autopep8
* read documentation, identify useful documentation, create useful
  links
* interact with Ifeanyi that works on a similar project

Mitigation strategy:

* in case it turns out that django is not the right tool, we will use
  flask and change our deliverables slightly.






Design
----------------------------------------------------------------------
Python programming
Django Configuration files
Bootstrap Templates

Implementation
----------------------------------------------------------------------
Development through Django server

Links
----------------------------------------------------------------------
* Django: https://www.djangoproject.com
* Python Idioms: http://python.net/~goodger/projects/pycon/2007/idiomatic/handout.html
* Git: http://git-scm.com/docs/gittutorial
* Hitchhiker's Guide to Python: http://docs.python-guide.org/en/latest/
* Software Carpentry: http://ivory.idyll.org/articles/advanced-swc/
* The Django Book, Chapter 4: Templates: http://www.djangobook.com/en/2.0/chapter04.html


Progress & Plans
------------------------------------------------------------------------


:Progress: 
  * [done, Week 1] learned python language and syntax, 
  * [done, Week 1] installed django & python on a ubuntu machine
  * [done, Week 1] learned git
  * [done, Week 1] learned virtualenv
  * [done, Week 1] learned pip
  * [in progress, Week1] read a portion of django documentation
  * [done, Week 2] the simple django server is checked into github
  * [done, Week 2] the bootstrap based simple server is in github
  * [done, Week 2] Successfully learned how to create a model and view in github
  * [done, Week 2] documentation of how to get a django-bootstrapped theme server up and running
  * [done, Week 3] install models, views, and templates
  * [done, Week 3] documentation of models, views, and templates
  * [done, Week 4] Successful connection to mongodb
  * [done, Week 4] Creation of demos of models, views, and templates
  * [done, Week 4] Successful creation of tables in django bootstrap theme
  * [done, Week 5] Create a MongoDb connection with Django
  * [done, Week 5] Documented MongoDb connection with Django
  * [done, Week 5] 


  * [done, Week 2] documentation of how to get a django-bootstrapped theme server up and running 
  * [done, Week 3] installation of models, views, and templates
  * [done, Week 3] documentation of models, vies, and templates
  * [done, Week 4] Successful connection to mongodb
  * [done, Week 4] Creation of demos of models, views, and templates
  * [done, Week 4] Successful creation of tables in django bootstrap theme
  
  
:Problems: 
  * [Week 2] cloud not get the mongo base django to work, existing
    tutorials were buggy according to gregor, possible too difficult
    task. Reasignment of next task, instead of using mongo for
    authentication we just use it for visualization of an existing
    dataset via django.  users are managed through sql we will in wee
    3 use the reservation database and than test how to develop views
    and templates. we start with reading up on views and templates.
  * [Week 3] had a difficult time understanding examples and documentation
    about django and how to create successful models, views, and templates
    to be seen as django and had a hard time install mongodb as a backend 
  * [Week 4] Making the demos was hard at first.  Creating the tables was also
    about django and how to create successful models, views, and templates 
    to be seen with django and had a hard time installing mongodb as a backend.
  * [Week 4] Working the demos was hard at first.  Creating the tables was also
    difficult as well. 

:Plan: 
  * [Week2] read more django documentation and implement django server 
  * [Week2] develop a django sever with mongodb as backend
  * [Week 4] 1 page paper
  * [Week 7] 2 page paper
  * [Week 8] poster

 


