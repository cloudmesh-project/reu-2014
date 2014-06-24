Cloudmesh Project and Account Management Framework
======================================================================

Team
----------------------------------------------------------------------

.. image:: ../images/photo_ifeanyi.png
   :height: 200

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

Cloudmesh is a project that allows the management of virtual machines 
in a federated fashion. It can be run in two modes. One is a standalone 
mode where the users run cloudmesh on the local machines. The second 
mode is a hosted mode where multiple users share a web server through 
which the virtual machines are managed. One of the important tasks, 
on this project, is to integrate users into cloudmesh. Hence, as we 
work closely with FutureGrid, we need to make sure that users are 
imported into cloudmesh. This is currently achieved via an integration 
to the FutureGrid LDAP server. Nevertheless, it is assumed that the 
users and projects are already in that server, as the FutureGrid portal 
provides such an interface. However, it is based on an older version of 
drupal and it is desirable to re-implement the user and project 
management functionality in cloudmesh.

This project will explore how we can design a data model in mongoengine 
to represent users and projects, and, also, identify how we can leverage 
either django or flask to manage such projects. To address the later, 
we will first evaluate if we can get a django web application started 
and identify how to use it. If this turns out to be too difficult, we 
will fall back to flask. As part of the management, we need to implement 
a queue in which users are queued for approval, and a project queue whereby 
projects are queued and approved by a committee. A simple backend system 
written in python will support this task and provide an abstraction that 
is outside of the web interface.

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



Progree	Problems Plans:
----------------------------------------------------------------------

:Progress:
  * [done, Week 1] Installed ubuntu, mongodb, mongoengine, pip and virtualenv to the machine.
  * [done, Week 1] learned how to use github and its commands
  * [done, Week 1] learned python
  * [done, Week 1] created a "Users" database independent from but similar to that of futuregrid portal.
  * [done, Week 1] created test, management and form python files to help complete the above task.
  * [in progress, Week 1] acquiring more knowledge on how to access the database using mongoengine.
  * [done, Week 2] learned and documented how to pull request
  * [done, Week 2] created a random user generator on test.py
  * [done, Week 2] created a delete function on test.py
  * [done, Week 2] updated the cm_account.py file
  * [done, Week 2] created the user_dict.py file that contains dict for the users attributes
  * [done, Week 2] wrote a program that reads from the reservation database
  * [in progress, Week 2] started studying how to use docopt to create commands
  * [done, Week 3] uderstood a good deal of how to write docopt based commands
  * [done, Week 3] created sample programs that uses docopt based commands.
  * [done, Week 3] modified test.py to generate both random and specific number of users
  * [done, Week 3] modified test.py to delete either all or specific users.
  * [done, Week 3] modified test.py to find all or specific users
  * [done, Week 3] used docopt based command to perform all functions in test.py
  * [done, Week 3] updated the management.py to use the json table format
  * [done, Week 3] updated the user_dict.py with lists with cities, institution and phone numbers
  * [in progress, Week 3] trying the best way to refine and add more functions to test.py

:Problems:
  * [Week 1] took a while to install the different softwares need for this project. This 
    is as many errors were made and some documentations found online were not up to date. Finally,
    I dould not understand most of the documentations found till after studying it for a while.
  * [Week 2] could not figure out how to use django with mongodb.
  * [Week 3] had to create different test and management python files in order to get the 
    most efficient functions. Hence, the code continues to be refined
    if better ways come up.

:Plans:
  * [Week 4] create another a web UI for projects to be linked to the users
  * [Week 5] implement an approval mechnism for users and projects.
  * [Week 6] evaluate what is missing and continue the implementation tasks
  * [Week 8] complete the 2 page paper, cleanup the program, make sure the
    user documentation and code documentation are done.
