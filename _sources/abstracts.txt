Project Abstracts
======================================================================


.. list-table:: The FutureGrid REU Project List
   :widths: 10 30 50
   :header-rows: 1

   * - Image
     - Contact
     - Project
   * - 

       .. image:: images/photo_ifeanyi.png
          :height: 100

     - Ifeanyi Rowland Onyenweaku

       Mentor: Gregor von Laszewski
     - **Cloudmesh Project and Account Management Framework**:

       Cloudmesh is a project that allows the management of virtual
       machines in a federated fasion. It can be run in two modes. One
       is a standalone mode whare the users runs cloudmesh on the
       local machines. Another mode is a hosted mode where multiple
       users share a web server through which the virtual machines are
       managed. One of the important tasks is to integrate users into
       cloudmesh. As we work closely with FutureGrid we need to make
       sure that users are imported into cloudmesh. This is currently
       achieved with an integration to the FutureGrid LDAP
       server. However it assumes that users and projects are already
       in that server. The FuturGrid portal provides such an
       interface. However it is based on an older version of drupal
       and it is desirable to reimplement the user and project
       management functionality in cloudmesh. This project will
       explore (a) how we can design a data model in mongoengine to
       represent users and projects, (b) identify how we can leverage
       either django or flask to manage such projects. To address (b)
       we will first evaluate if we can get a django web application
       started and identify how to use it. If this turns out to be to
       difficult, we will fall back to flask.

       As part of the management we need to implement a queue in which
       users are queued for approval, a project queue in which
       projects are queued and approved by a comittee. A simple
       backend system written in python will support this task provide
       an abstraction that is outside of the web interface.

       **Keywords:** Cloudmesh; FutureGrid; Django; Mongoengine; Mongodb
   * - 

       .. image:: images/photo_ifeanyi.png
          :height: 100

     - Natalie Bohn

       Mentor: Gregor von Laszewski
     - **Cloudmesh Resource Reservation**

       Cloudmesh Resource Reservation is being developed to create and
       manage reservations inside Cloudmesh. Cloudmesh is a project
       that includes the ability to conduct bare metal
       provisioning. It is important that this is supported in a
       multiuser environment. We will be developing for this a time
       based reservation system in which users will have access to
       resources based on time slices. This project will develop such
       a reservation system as a commandline tool and also as a GUI
       (if time permits while leveraging the work done by von
       Laszewski for this project). As a result we will have a simple
       commandline tool that allows the administrator or user to
       choose a reservation or query the system to find a suitable
       reservation. Limits will be put in place so that users do not
       reserve too many resources and block the systems while not
       allowing others to use it. The system will have an abstract
       plugin that allows the integration of a real bare metal
       provisioning. However, for this project, we will simulate it
       and focus only on the management of the reservation itself and
       not how they are used or how machines are leveraged for the
       actual bare metal provisioning. Convenient tables and views are
       developed as part of the GUI development which is doable as the
       GUI framework is already included in the project developed by
       von Laszewski.  

       **Keywords:** Python, docopt, Mongodb, mongoengine, Cloudmesh
   * - 

       .. image:: images/photo_ifeanyi.png
          :height: 100

     - Jefferson Ridgeway

       Mentor: Gregor von Laszewski
     - **Django For Cloudmesh**

       The cloud computing system Cloudmesh currently uses flask,
       however because of the low usage of the web
       framework. Installation of django, a similar framework has
       proven to be more productive, efficient, and easier to use and
       apply than flask. The purpose of this project is to develop a
       prototype django server that will have sets of functions that
       will make Cloudmesh easier for user to interact with. This
       includes attaching bootstrap theme to the django server and
       list of virtual machines on various clouds that currently use
       Cloudmesh databases.  

       **Keywords:** Cloudmesh, django, bootstrap theme, flask
