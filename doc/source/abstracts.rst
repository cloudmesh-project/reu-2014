Project Abstracts
======================================================================


.. list-table:: The FutureGrid REU Project List
   :widths: 20 20 50
   :header-rows: 1

   * - Image
     - Contact
     - Project
   * - 

       .. image:: images/photo_ifeanyi.png
          :height: 100

     - Ifeanyi ...
     - Cloudmesh is a project that allows the management of virtual
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

