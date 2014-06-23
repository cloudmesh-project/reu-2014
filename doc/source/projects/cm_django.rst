Cloudmesh Django
======================================================================

Team
----------------------------------------------------------------------

.. image:: ../images/rsz_1rsz_photo_jeff1.png
   :height:: 100


* Jeff Ridgeway, jdridgeway4@gmail.com
* Gregor von Laszewski, laszewski@gimail.com

Problem
----------------------------------------------------------------------

Cloudmesh contains a webserver that uses flask as a backend. Although
flask is very powerful and easy to use, django is more comonly used in
the cloud community. This also includes Openstack Horizon that uses
flask. This project will explore how to use django instead of flask
for the development of cloudmesh. As such we need an easy install and
usage documentation that will be developed as part of this
project. The django documentation is quite extensive and the main task
will include the development of simple guides and examples that can be
reused by the cloudmesh team to transition or clone the flask
framework to django. The examples will develop concrete views and
models utilizing mongodb to visualize contents form the
database. Simple guides will be developed that tell others ow to do
this.

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
Algorithms in Python

Implementation
----------------------------------------------------------------------
Work through Django server

Links
----------------------------------------------------------------------

* Django: https://www.djangoproject.com
* Python Idioms: http://python.net/~goodger/projects/pycon/2007/idiomatic/handout.html
* Git: http://git-scm.com/docs/gittutorial
* Hitchhiker's Guide to Python: http://docs.python-guide.org/en/latest/
* Software Carpentry: http://ivory.idyll.org/articles/advanced-swc/


Progress & Plans
------------------------------------------------------------------------


:Progress: 
  * [done, Week 1] learned python language and syntax, 
  * [done, Week 1] installed django & python on a ubuntu machine
  * [done, Week 1] learned git
  * [done, Week 1] learned virtualenv
  * [done, Week 1] learned pip
  * [in progress, Week1] read a portion of django documentation
  * [done, Week 2] the simple django server is checke into github
  * [done, Week 2] the bootstrap based simple server is in github
  * [done, Week 2] Successfully learned how to create a model and view in github
  * [done, Week 2] documentation of how to get a django-bootstrapped theme server up and running 
  * [done, Week 3] installation of models, views, and templates
  * [done, Week 3] documentation of models, vies, and templates

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
    to be seen with django and had a hard time installing mongodb as a backend.

:Plan: 
  * [Week2] read more django documentation and implement django server 
  * [Week2] develop a django sever with mongodb as backend
  * [Week 4] 1 page paper
  * [Week 7] 2 page paper
  * [Week 8] poster

 


