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

       Cloudmesh is a project that allows the management of virtual 	   machines in a federated fashion. It can be run in two modes. 	   One is a standalone mode where the users run cloudmesh on the 	    local machines. The second mode is a hosted mode where multiple 	      users share a web server through which the virtual machines are 	      managed. One of the important tasks, on this project, is to 	  integrate users into cloudmesh. Hence, as we work closely with 	     FutureGrid, we need to make sure that users are imported into 	    cloudmesh. This is currently achieved via an integration to the 	      FutureGrid LDAP server. Nevertheless, it is assumed that the 	   users and projects are already in that server, as the 	    	   FutureGrid portal provides such an interface. However, it is 	   based on an older version of drupal and it is desirable to    	    re-implement the user and project management functionality in  	     cloudmesh.
       This project will explore how we can design a data model in 	  mongoengine to represent users and projects, and, also, 	 	identify how we can leverage either django or flask to manage 	    such projects. To address the later, we will first evaluate if 	     we can get a django web application started and identify how to 	      use it. If this turns out to be too difficult, we will fall 	  back to flask. As part of the management, we need to implement 	     a queue in which users are queued for approval, and a project 	    queue whereby projects are queued and approved by a committee. 	     A simple backend system written in python will support this 	  task and provide an abstraction that is outside of the web 	 interface.

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

       .. image:: images/photo_jeff.png
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
       
   * - 
   
       .. image:: images/photo_leif.jpg
          :height: 100

     - Leif Christiansen

       Mentor: Supun Kamburugamuva
     - **IoTCloud2**

       Kinect sensors provide a cheap and effective tool for 3 dimensional
       imageing. Currently, many open source project are being developed 
       utilizing the Kinect sensor in a variety of areas. One such are is
       robotics. The Kinect sensor may be used to create an accurate 3
       dimensional model of an environment allowing a robot to navigate
       effectively. Supun Kamburugamuva has worked previously with a Kinect
       based robot and software suite, the Turtlebot and accompanying 
       open-source software produced by Robot Operating Systems (ROS). 
       Supun's previous work, IoTCloud, focused on performing all necessary
       computations pertaining to object avoidance on the cloud. But the 
       ROS software requires considerable overhead, lessening the efficiency
       with which these calculations may be made. Our new project will 
       utilize the OpenKinect Java library to perform more efficient 
       retrieval and transmission of depth data from the Kinect. Faster
       processing will allow for the operation of numerous robots 
       simultaneously with real-time parallel computing deployed on the 
       cloud.
       
       **Keywords:** depth camera, laser scanning, cloud computing, point cloud, real-time
	   
   * -
  
       .. image:: images/saggu.png
          :height: 100

     - Loran Saggu

       Mentor: Saliya Ekanayake, Yang Ruan, Geoffrey Fox
     - **BioInformatics: Genomic Sequence Analysis Automation**

	An organisms genetic code determines everything about that organism: it determines what species the organism will become, how big it will grow, whether or not it will have gills or will be able to convert light into energy. The genetic code of many organisms is quite similar, but of course there are differences which allow for every unique individual. If the similarity between genetic sequences could be mapped, deriving and understanding the relationships between organisms could be done efficiently and effectively. Dr. Geoffrey Fox and his lab are trying to do exactly that: map the similarity between genomic sequences. They seek to do this using complex algorithms within computer programs they have designed that essentially define "distances" between genomic sequences, and these distances can be scaled and used to create a plot. There is, of course, some work to be done. These processes developed by Dr. Fox and his lab are heuristic and only understood and accessable by a few. Also they aren't automated. However, by setting up a server to run a Java based portal designed to accept user input via the web and run these algorithms on computer clusters, these issues could be dealt with. Being able to efficiently map the differences in genomic sequences will vastly improve people's understanding of where the organisms of today arose. This may also have vast implications in the realms of geneology, and medecine as a result of the improved understanding of the relationships between various organisms.
       
       **Keywords:** Bioinformatics, Clusters, Distance-Matrix, Genomics, Map-Reduce, Phylogenic Tree, Twister
 
   * -
  
	.. image:: images/photo_tori.png
          :height: 100

     - Tori Wilbon

       Mentor: Saliya Ekanayake
     - **Evaluating the Performance of MPI JAVA in FutureGrid and BigRed2**

	Message Passing Interface (MPI) has become the de facto way of implementing High 
	Performance Computing (HPC) applications as it provides library routines to satisfy 
	virtually all communication patterns. The goal of our research is to understand 
	performance characteristics of parallel programs written in Java versions of MPI. 
	Two such MPI libraries exist, i.e. OpenMPI and FastMPJ. The team will be testing 
	performance of our applications based on both these frameworks. The algorithms that 
	the team will be measuring are a complex and O(N^2) complexities. The team needs to 
	make sure they run in an optimal fashion and give us the best results. The other aspect 
	to our project is to develop some sample MPI Java programs.

       **Keywords:** MPI Java, Linux, Pairwise Cluster, FutureGRID, BIG RED2

   * -
   
	.. image:: images/photo_nigel.png
          :height: 100

     - Nigel Pugh

       Mentor: Saliya Ekanayake
     - **Evaluating the Performance of MPI JAVA in FutureGrid and BigRed2**

       Message Passing Interface (MPI) has become the de facto way of implementing High Performance Computing (HPC) applications as it provides library routines to satisfy virtually all communication patterns. The goal of our research is to understand performance characteristics of parallel programs written in Java versions of MPI. Two such MPI libraries exist, i.e. OpenMPI and FastMPJ. The team will be testing performance of our applications based on both these frameworks. The algorithms that the team will be measuring are a complex and O(N^2) complexities. The team needs to make sure they run in an optimal fashion and give us the best results. The other aspect to our project is to develop some sample MPI Java programs.

       **Keywords:** MPI Java, Linux, Pairwise Cluster, FutureGRID, BIG RED2

   * -
	.. image:: images/tatyfinal.png
          :height: 100

     - Tatyana Matthews

       Mentor: Scott McCaulay
     - **Apache Big Data Stack**

       The Apache Big Data Stack is representative of a large spectrum of numerous open-source software programs provided through 
       Apache projects. The term Apache refers to the Apache Software Foundation (ASF), which provides support for open-source 
       software projects and attracts a large community of users. This mass group of users is what ultimately generates enormous 
       amounts 	of data ---Big Data. Accordingly, this enormous digital volume consists of data that cannot be captured and 
       organized by traditional tools, thus presenting an obstacle. It is vital to utilize computing power and storage in order 
       to organize such data; however, this presents economical concerns due to costly affects. The Apache Big Data Stack and the
       product Chef will be investigated and applied to resolve such an issue. Research will involve installing and testing as many
       open-source software packages as possible on FutureGrid machines and later making them accessible utilizing Chef. In order
       to accomplish this, software packages deriving from the Apache Big Data Stack spectrum will be installed on to a virtual machine
       to create application packages. These packages will be built into projects and Chef will be used to transform the infrastructure
       of the project’s code and bring it to life so that it can be made accessible through a network of servers. Finally, research will
       demonstrate how use of the Apache Big Data Stack and Chef can be applied to contribute to the evolution of innovation in the
       Big Data field.

       **Keywords:** Apache Big Data Stack, Chef, FutureGrid, Big Data

