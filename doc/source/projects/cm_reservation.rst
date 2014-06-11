Cloudmesh Resource Reservation
======================================================================

Team
----------------------------------------------------------------------

* Natiele Bohn, nattibohn@gmail.com
* Gregor von Laszewski, laszewski@gmail.com
* Oliver Lewis


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

