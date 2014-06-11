Cloudmesh Project and Account Management Framework
======================================================================

Team
----------------------------------------------------------------------

* Ifeanyi Rowland Onyenweaku,    rowlandifeanyi17@gmail.com
* Gregor von Laszewski, laszewski@gmail.com

Links
----------------------------------------------------------------------

* Issues: https://github.com/cloudmesh/management/issues
* Code: https://github.com/cloudmesh/management
* Contributors:
  https://github.com/cloudmesh/management/graphs/contributors

Problem
----------------------------------------------------------------------

TODO: please conduct spell and grammer checking

Cloudmesh is a project that allows the management of virtual machines
in a federated fasion. It can be run in two modes. One is a standalone
mode whare the users runs cloudmesh on the local machines. Another
mode is a hosted mode where multiple users share a web server through
which the virtual machines are managed. One of the important tasks is
to integrate users into cloudmesh. As we work closely with FutureGrid
we need to make sure that users are imported into cloudmesh. This is
currently achieved with an integration to the FutureGrid LDAP
server. However it assumes that users and projects are already in that
server. The FuturGrid portal provides such an interface. However it is
based on an older version of drupal and it is desirable to reimplement
the user and project management functionality in cloudmesh. This
project will explore (a) how we can design a data model in mongoengine to
represent users and projects, (b) identify how we can leverage either
django or flask to manage such projects. To address (b) we will first
evaluate if we can get a django web application started and identify
how to use it. If this turns out to be to difficult, we will fall back
to flask. 

As part of the management we need to implement a queue in which users
are queued for approval, a project queue in which projects are queued
and approved by a comittee. A simple backend system written in python
will support this task provide an abstraction that is outside of the
web interface.

Plan of action:

* Week 1: learn tools such as python, git, set up the computer, learn
  mongo
* Week 2: Evaluate if django is a viable technology for the project
* Week 3: Develop the data abstractions and create simple programs to
  interact with the database
* Week 4: Develop a simple Web UI witha  form to add users, projects,
  and roles so that we can upload that data into the database
* Wekk 5: Implement an approval mechnism for users and projects. IN
  case of projects we need a role comittee member that allows to vote
  on a project.
* Week 6 and 7: Evaluate what is missing and continue the
  implementation tasks
* Week 8: complete the 2 page paper that has been written continiously
  over the previous weeks, cleanup the program, make sure the
  user documentation and code documentation are done.

Tip:
----------------------------------------------------------------------
* use pylint
* use autopep8
* use sphinx for documentation, Gregor will help on getting your
  modules into sphinx.
* discuss your project with another student 


Design
----------------------------------------------------------------------

Create a database that will be used to manage the futuregrid portal.

Implementation
----------------------------------------------------------------------



Week 1:
----------------------------------------------------------------------

Progress:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* installed softwares needed:

  * ubuntu
  * mongoDb
  * mongoengine
  * aptana

* Learnt how to use github and its' commands
* Learnt python
* Leant and stil learning how to access/create/use a database 
  (mongoDB). 

  * Created a database to develop a data structure for users based on
    what is on the Futuregrid portal.
		 
  * Started writing python codes that will help achieve.
    this task:

    * Management.py:
    * test.py
    * form.py: Dictionary for sections in portal
		
* Learnt and still learning how to use mongoengine to manage
  my database

Next week Plans:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
* Create a random user generator function.
* Update the program to be able to print a table of the users.
* Figure how to use doc_opt to perform different actions.
* Create a dump of all the address in a dictionary form.
* Create functions that will help analize different info.
* Read on flask, esp wtf forms
* Create a gui account for user account 
