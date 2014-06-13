Cloudmesh Resource Reservation
======================================================================

Team
----------------------------------------------------------------------

* Natiele Bohn, nattibohn@gmail.com
* Gregor von Laszewski, laszewski@gmail.com
* Oliver Lewis (Grad student)


Problem
----------------------------------------------------------------------

Cloudmesh is a project that includes the ability to conduct bare metal
provisioning. It is important that this is supported in a multiuser
environment. We will be developing for this a time based reservation
system in which users will have access to resources based on time
slices. This project will develop such a reservation system as a
commandline tool and also as a GUI (if time permits while leveraging
the work done by von Laszewski for this project). As a result we will
have a simple commandline tool that allows the administrator or user
to chose a reservation or query the system to find a suitable
reservation. Limits will be put in place so that users do not reserve
too many resources and block the sytems while not allowing others to
use it. The system will have an abstract plugin that allows the
integration of a real bare metal provisioner. Howevre for this
project, we will simulate it and focus only on the management of the
reservation itself and not how they are used or how machines are
leveraged for the actual bare metal provisioning. Convemient tables
and views are developed as part of the GUI development which is doable
as the GUI framework is already included in the project developed by
von Laszewski. 

Plan of Action:

* Week 1: Learn the basics: python, git, mongo, get familair with the
  ol reservation code developed by oliver
* Week 2: develop a mongo db to generate random reservations and
  dispaly them in an image via ploticus
* Week 3: complete the database design while using mongoengine and
  create commandline tools useing docopts to interact withe the
  database (reqrite Olivers code)
* Week 4: Improve the flask interface von Laszewski developed and
  create better views, work with Fugang on this in case help is
  needed.
* Week 5: develop a mechnism that restricts access in various ways
  through policies. For example use is time limited on all or some
  machines, she has not access to all machines, she has restrictions
  based on project memberships
* Week 6: write command line tools to manage policies, write gui forms
  and use forms to manage policies in mongo. USe mongoengine for all
  of thsi
* Week 7: continue development and code cleanup
* Week 8: complete the 2 page paper that you worked on till now,
  complete the documentation, code and transition ownereship to Gregor
  and Fugang. Discuss the possibility if this code can be introduced
  into the production code of cloudmesh.






First week
----------------------------------------------------------------------

The challenges of the first week of the program was to learn Python in
just some days and learn Linux commands to know how to use Ubuntu.
Besides to learn Python and Linux commands I had to read and
understand docopt and have a basic knowledge about mongodb/
mongoengine.



Design
----------------------------------------------------------------------


Implementation
----------------------------------------------------------------------

First week
----------------------------------------------------------------------

This project I am working has being implemented in Python and using
mongoengine as database management.  It's function is to see what
resources are avaliable to be used on cloud and make a reservation of
this resource.  It has to validate if the time requested its avaliable
and return if the reservation is possible or not. And if not, it has
to say what is the next time this particular resource will be
avaliable for the solicited amout of time.


Links
----------------------------------------------------------------------

Some documentation that I read can be found at:

* http://www.pythonforbeginners.com/
* http://docs.mongoengine.org/
* http://docopt.org/

