Cloudmesh Resource Reservation
======================================================================

Team
----------------------------------------------------------------------

* Natiele Bohn, nattibohn@gmail.com
* Gregor von Laszewski, laszewski@gmail.com
* Oliver Lewis, oliverlewis7@gmail.com

Github webpage
----------------------------------------------------------------------

Code: https://www.github.com/cloudmesh/reservation
Contributors: https://www.github.com/cloudmesh/reservation/graphs/contributors

Problem
----------------------------------------------------------------------

Cloudmesh Resource Reservation is being developed to
create and manage reservations inside Cloudmesh.
Cloudmesh is a project that includes the ability to conduct
bare metal provisioning. It is important that this is supported
in a multiuser environment. We will be developing for this a
time based reservation system in which users will have
access to resources based on time slices. This project will
develop such a reservation system as a commandline tool and
also as a GUI (if time permits while leveraging the work
done by von Laszewski for this project). As a result we will
have a simple commandline tool that allows the administrator
or user to choose a reservation or query the system to find a
suitable reservation. Limits will be put in place so that users
do not reserve too many resources and block the systems
while not allowing others to use it. The system will have an
abstract plugin that allows the integration of a real bare metal
provisioning. However, for this project, we will simulate it
and focus only on the management of the reservation itself
and not how they are used or how machines are leveraged for
the actual bare metal provisioning. Convenient tables and
views are developed as part of the GUI development which is
doable as the GUI framework is already included in the
project developed by von Laszewski.

Plan of Action 
----------------------------------------------------------------------

The follow information is a temporary plan of actions that
can bring more details about the daily lab activities proposed
by von Laszewski:

* Week 1: Learn the basics: python, git, mongo, get familiar with the old reservation code developed by Oliver Lewis who is a grad student here at Indiana University

* Week 2: Develop a mongo database to generate random reservations and display them in an image via Ploticus 
 
* Week 3: Complete the database design while using Mongoengine and create commandline tools using Docopts to interact with the database (rewrite Olivers code)

* Week 4: Improve the flask interface that von Laszewski developed and create better views, work with Fugang on this in case help is needed.

* Week 5: Develop a mechanism that restricts access in various ways through policies. For example: a user is time limited on all or some machines, the user has not access to all machines, the user has restrictions based on project memberships

* Week 6: Write commandline tools to manage policies, write GUI forms and use forms to manage policies in mongo. Use Mongoengine for all of this
 
* Week 7: Continue development and code cleanup

* Week 8: Complete the 2 page paper that you worked on until now, complete the documentation, code and transition ownership to Gregor von Laszewski and Fugang. Discuss the possibility of this code can be introduced into the production code of Cloudmesh.

Week I
----------------------------------------------------------------------

The follow information are some of the tasks already done on
the first week of work:

* Install Ubuntu
* Learn commands on Linux shell
* Learn Python and its syntax
* Create account on GitHub
* Read the old code of Reservation
* Learn commands like git clone, git pull, git commit and git push to bring the code of reservation to my workstation and after make changes in the code push it back to GitHub to allows another users to see the changes in the code and work in parallel

Week II
----------------------------------------------------------------------
The follow information are some of the tasks already done on
the second week of work:

* Learn about how Mongodb works on the background of Mongoengine
* Created a database to integrate and generate random reservations on Cloudmesh
* Test the code on generate.py on reservations 
* Develop new functions inside model.py on reservations. The functions developed were responsible for find different information inside the random reservations that were created.

Week III
----------------------------------------------------------------------
The follow information are some of the tasks already done on
the second week of work:

* Create functions add, update and delete to model.py
* Create commandlines using DOCOPTS
* Start to look how the flask works to update the flask already developed by Gregor von Laszewski
* Added function list on flask interface

Week IV
----------------------------------------------------------------------
The follow information are some of the tasks already done on
the second week of work:

* Added functions on flask interface
* Improve the flask to a better view
* Created a form to add reservations using the flask interface
* Still working to create a better function update on model.py (this function should update a reservation that is already created.)

Week V
----------------------------------------------------------------------
The follow information are some of the tasks already done on
the second week of work:

* Continued to work on the flask functions / Bootstrap
* Create forms
* Separate example code to production code

Week VI
----------------------------------------------------------------------
The follow information are some of the tasks already done on
the second week of work:

* Better form views
* Usage of Restful instead of Flask

Week VII
----------------------------------------------------------------------
The follow information are some of the tasks already done on
the second week of work:

* Focused on a paper requested by von Laszewiski and the poster requested by REU Program.
* Oral presentation of the project in Indianapolis, IUPUI campus.

Links
----------------------------------------------------------------------

Some documentation that I read can be found at these webpages:

* http://www.mongoengine.org/
* https://www.python.org/
* http://www.flask.pocoo.org/docs/tutorial/
* http://www.docopt.org/
* http://www.w3.org/TR/html-aapi/
* http://www.blog.miguelgrinberg.com/post/designing-a-restful-api-with-python-and-flask
* http://www.flask-restful.readthedocs.org/en/latest/quickstart.html#full-example

