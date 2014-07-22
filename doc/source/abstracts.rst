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
       
       Mississippi Valley State University
       
       .. image:: images/mvsu_ifeanyi.png
          :height: 100
          
     - **Cloudmesh Project and Account Management Framework**:

       Cloudmesh is a project that allows the management of virtual 	   
       machines in a federated fashion. It can be run in two modes. 	   
       One is a standalone mode where the users run cloudmesh on the 	    
       local machines. The second mode is a hosted mode where multiple 	      
       users share a web server through which the virtual machines are 	      
       managed. One of the important tasks, on this project, is to 	  
       integrate users into cloudmesh. Hence, as we work closely with 	     
       FutureGrid, we need to make sure that users are imported into 	    
       cloudmesh. This is currently achieved via an integration to the 	      
       FutureGrid LDAP server. Nevertheless, it is assumed that the 	   
       users and projects are already in that server, as the 	    	   
       FutureGrid portal provides such an interface. However, it is 	   
       based on an older version of drupal and it is desirable to    	    
       re-implement the user and project management functionality in  	     
       cloudmesh.
       
       This project will explore how we can design a data model in 	  
       mongoengine to represent users and projects, and, also, 	 	
       identify how we can leverage either django or flask to manage 	    
       such projects. To address the later, we will first evaluate if 	     
       we can get a django web application started and identify how to 	      
       use it. If this turns out to be too difficult, we will fall 	  
       back to flask. As part of the management, we need to implement 	     
       a queue in which users are queued for approval, and a project 	    
       queue whereby projects are queued and approved by a committee. 	     
       A simple backend system written in python will support this 	  
       task and provide an abstraction that is outside of the web 	 
       interface.

       **Keywords:** Cloudmesh; FutureGrid; Django; Mongoengine; Mongodb
   * - 

       .. image:: images/photo_natiele.png
          :height: 100

     - Natiele Bohn

       Mentor: Gregor von Laszewski
       
       Dillard University / UNISINOS
       
       .. image:: images/dillard.png
          :height: 100
          
       .. image:: images/unisinos.png
          :height: 100
          
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

       .. image:: images/rsz_1rsz_photo_jeff1.png
          :height: 100

     - Jefferson Ridgeway

       Mentor: Gregor von Laszewski
       
       University: Elizabeth City State University 
       
       .. image:: images/elizabeth_city_logo.png
          :height: 100
     
     - **Cloudmesh Project and Account Management Framework: Django**

       The cloud computing system Cloudmesh currently uses flask
       as a backend. Even though flask is easier to use than django, 
       django has become favored  web framework to use 
       in the cloud computing community as of recently.    
       The purpose of this project is to develop a
       prototype django server that will have sets of functions that
       will make Cloudmesh as applicable using django than to use flask. 
       The documentation on django is varied and comprehensive and in 
       achieving the purpose of the project, simple guides and examples will
       be conducted for future use by the cloudmesh team to shift or clone
       the flask framework to django. These examples will incorporate
       how to develop concerte views and models using the database 
       known as mongodb to reflect the data from the database. This framework will also include 
       attaching the bootstrap theme to the django server and list of 
       virtual machines on various clouds that currently use Cloudmesh databases.

       **Keywords:** Cloudmesh, django, bootstrap theme, flask, views, models
       
   * - 
       .. image:: images/photo.JPG
          :height: 100

     - Leif Christiansen

       Mentor: Supun Kamburugamuva
       
       Lewis & Clark College
       
       .. image:: images/LC.jpg
          :height: 100
       
     - **IoTCloud2**

       Kinect sensors provide a cheap and effective tool for 3 dimensional
       imaging. Currently, many open source project are being developed 
       utilizing the Kinect sensor in a variety of areas. One such area is
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
       
       Indiana University
       
       .. image:: images/iu.jpeg
          :height: 100

       Mentors: Saliya Ekanayake, Yang Ruan, Geoffrey Fox
     - **BioInformatics: Genomic Sequence Analysis Automation**

       An organisms genetic code determines everything about that organism: it determines what species the organism will become, how big it will grow, whether or not it will have gills or will be able to convert light into energy. The genetic code of many organisms is quite similar, but of course there are differences which allow for every unique individual. If the similarity between genetic sequences could be mapped, deriving and understanding the relationships between organisms could be done efficiently and effectively. Our team is trying to do exactly that: map the similarity between genomic sequences. Using complex algorithms within computer programs, the team has been able to define "distances" between genomic sequences, and these distances can be scaled and used to create a plot. There is, of course, some work to be done. These processes developed by the lab are heuristic and only understood and accessable by a few. Also they aren't automated. However, by setting up a server to run a Python based portal designed to accept user input via the web and run these algorithms on computer clusters, these issues could be dealt with. Being able to efficiently map the differences in genomic sequences will vastly improve people's understanding of where the organisms of today arose. This may also have vast implications in the realms of geneology and medecine as a result of the improved understanding of the relationships between various organisms.
       
       **Keywords:** Bioinformatics, Clusters, Distance-Matrix, Genomics, Map-Reduce, Phylogenic Tree, Twister
 
   * -
  
       .. image:: images/photo_tori.png
          :height: 100

     - Tori Wilbon

       Mentor: Saliya Ekanayake
       
       University: Elizabeth City State University
       
       .. image:: images/elizabeth_city_logo.png
          :height: 100
          
     - **Evaluating the Performance of MPI JAVA in FutureGrid and BigRed2**

       Message Passage Interface (MPI) has been the common choice among developers when developing tightly coupled parallel High Performance Computing (HPC) applications and the majority of such applications are based on either C, C++ or Fortran. The recent advancement in processing big data, however, has brought attention towards Java. Effort has also been put on Java's support for HPC with flavors of MPI such as OpenMPI Java and FastMPJ. We evaluate these against native C based MPI on a set of micro-benchmarks from the standard Ohio MicroBenchmark suite from Ohio State University. The results show a promising future with Java and MPI for HPC applications
       **Keywords:** MPI Java, Linux, Pairwise Cluster, FutureGRID, BIG RED2

   * -
   
       .. image:: images/photo_nigel.png
          :height: 100

     - Nigel Pugh

       Mentor: Saliya Ekanayake
       
       University: Elizabeth City State University
       
       .. image:: images/elizabeth_city_logo.png
          :height: 100
          
       
     - **Evaluating the Performance of MPI JAVA in FutureGrid and BigRed2**

       Message Passage Interface (MPI) has been the common choice among developers when developing tightly coupled parallel High Performance Computing (HPC) applications. The goal of our research is to understand performance characteristics of parallel programs written in Java versions of MPI. Two such MPI libraries exist, i.e. OpenMPI and FastMPJ. We will evaluate the performance of two deterministically annealed clustering programs. These algorithms are of O(N^2) complexity and part of the study will be to understand configuration options that optimally runs them. In addition to measuring the performance we also focus on developing a set of sample applications, which will benefit the MPI Java community.

       **Keywords:** MPI Java, Linux, Pairwise Cluster, FutureGRID, BIG RED2



   * -
   
       .. image:: images/taty_fixed.png
          :height: 100

     - Tatyana Matthews

       Mentor: Scott McCaulay
       
       University: Elizabeth City State University
       
       .. image:: images/elizabeth_city_logo.png
          :height: 100
       
     - **Apache Big Data Stack**

       As the amount of data generated around the world continues to accelerate by the second, the more the
       term Big Data finds its way into scientific conversation. Because of this tremendous surge, it has become
       imperative that such mass data use “computing power and space” for it to be processed, analyzed, and
       serve other purposes [1]. Hence, in order to meet head-on the enormous challenges rendered by Big Data, open
       source software from the Apache Foundation is evaluated as a “Big Data Stack” to support scientific computing.
       The approach to handling the complications surrounding Big Data involve installing and testing as many open-source
       software packages from the Apache Big Data Stack as possible on FutureGrid machines and later making those
       packages accessible utilizing Chef. The packages will be built into projects and from that point Chef will
       be used to transform the infrastructure of each project’s code, making it agile and accessible through a network
       of servers [2]. Essentially, this research will demonstrate how the Apache Big Data Stack can be used and applied
       to solve complex problems regarding Big Data.


       **Keywords:** Apache Big Data Stack, Chef, FutureGrid, Big Data

   * -
   
       .. image:: images/kjs.png
          :height: 100

     - Khaliq Satchell

       Mentor: Dr. Geoffrey Fox, Yang Ruan
       
       University: Elizabeth City State University
       
       .. image:: images/elizabeth_city_logo.png
          :height: 100
       
     - **The Use Of Parallelization Support To Speed Up PlotViz3**

        In biology there is a scientific field that develops methods and software tools for organizing and 
        analyzing biological data. That field is bioinformatics and it combines computer science with other 
        fields in order to study biological data and processes which in turn can provide meaningful information 
        on genomic sequences. Currently, there is a software called PlotViz3, a three-dimensional data point 
        browser, which can be helpful for scientists in the field of bioinformatics. PlotViz3 can be used to 
        interactively discover intrinsic structures efficiently of which are high-dimensional and contain large 
        volumes of data. This means that scientists will be able to find the correlations between the DNA
        sequence clusters that they have data for more effectively than their previous methods such as phylogenetic 
        trees. This software should be accessible to every scientist working in bioinformatics but has yet to be 
        put out there for them because the process is not easily done. Once it is basic enough for simple execution 
        then scientist will have a new and more efficient tool for analyzing organism's genomic sequences. The
        purpose of this project is to add parallelization support to the code for multithreading PlotViz3. The code 
        in the software uses the C++ programming language which is what I shall be using to make improvements. In 
        the end, adding this support will speed up the virtualization process in the software and make it less time 
        consuming when looking for results quickly and efficiently.


       **Keywords:** Bioinformatics, Genomic Sequences, PlotViz3, Phylogenetic Trees, Multithreading, Parallelization, C++


