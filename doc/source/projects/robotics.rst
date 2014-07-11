IoTCloud2
======================================================================

Team
----------------------------------------------------------------------
Leif Christiansen grindvald@gmail.com

Supun Kamburugamuva supun06@gmail.com

Abstract
----------------------------------------------------------------------

Kinect sensors provide a cheap and effective tool for 3 dimensional imaging. Currently, many open source project are being developed utilizing the Kinect sensor in a variety of areas. One such area is robotics. 
The Kinect sensor may be used to create an accurate 3 dimensional model of an environment allowing a robot to navigate effectively. 
Supun Kamburugamuva has worked previously with a Kinect based robot and software suite, the Turtlebot and accompanying open-source software produced by Robot Operating Systems (ROS). 
Supun's previous work, IoTCloud, focused on performing all necessary computations pertaining to object avoidance on the cloud. 
But the ROS software requires considerable overhead, lessening the efficiency with which these calculations may be made. 
Our new project will utilize the OpenKinect Java library to perform more efficient retrieval and transmission of depth data from the Kinect. 
Faster processing will allow for the operation of numerous robots simultaneously with real-time parallel computing deployed on the cloud.


Implementation
----------------------------------------------------------------------

* `Robot Operating System (ROS) <http://www.ros.org/>`_
* `OpenKinect driver <http://openkinect.org/wiki/Main_Page>`_

Links
----------------------------------------------------------------------

* https://github.com/iotcloud/reu
* https://github.com/supunkamburugamuva/iotcloud2
* https://github.com/supunkamburugamuva/sensorstream
* https://github.com/supunkamburugamuva/iotrobots


Week 1
----------------------------------------------------------------------

What Has Been Done This Week
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* learned github and corresponding commands
* familiarized myself with the Kinect sensor, both in terms of hardware and scientific applications (links included below)
* discussed with Supun Kamburugamuva at length to discern the goal and scope of his project
* examined documentation of software and libraries pertinent to the project

  * OpenKinect 
  * Processing
  * ROS (Robot Operating System)
  * OpenNI
  * SimpleOpenNI
   
* installed OpenKinect and the corresponding Java wrapper

  * explored the capabilities of said wrapper to interact with the Kinect
   
* installed and built the OpenNI library
* found potential alternative libraries to SimpleOpenNI

  * Daniel Shifman's Kinect library
  * PCL (Point Cloud Library)

* installed ROS

  * installed Rviz (3D graphics visualization software) ROS package
  * installed freenect_stack ROS package (freenect based Kinect driver)
   
* worked through a number of ROS tutorials to learn about ROS fundamentals such as Nodes, Topics, how to manage subcriptions and publications, and ROS filesystem commands among others

What Has Not Been Achieved This Week?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* installing and building the SimpleOpenNI2 library
* recording the depth image information from the Kinect 
* successfully visualizing Kinect data in Rviz
* installing and building OpenNI2, the newest version of OpenNI

What is Planed For Next Week?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* continuing to learn about the ROS software
* build a library that will be used to write code for the Kinect (whether it be SimpleOpenNI2 or otherwise) 
* record depth image data from the Kinect.

Links
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
* Articles

  * www.cs.washington.edu/robotics/postscripts/3d-mapping-iser-10-final.pdf
  * http://scholar.google.com/scholar_url?hl=en&q=http://www.mdpi.com/1424-8220/12/2/1437/pdf&sa=X&scisig=AAGBfm0cShgyJ38PAqssax-iG5vzh88IIg&oi=scholarr
  * http://research.microsoft.com/pubs/155378/ismar2011.pdf
  * http://www.cs.washington.edu/robotics/postscripts/icra11-scene-differencing.pdf

* http://www.processing.org/
* http://shiffman.net/p5/kinect/reference/org/openkinect/processing/Kinect.html
* http://code.google.com/p/simple-openni/

Week 2
----------------------------------------------------------------------

What Has Been Done This Week
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* succesfully visualized Kinect data using Rviz (camera, depth, and IR)

  * installed openni_camera and openni_launcher packages (another Kinect driver)
  * installed kinect_aux package (nodes facilitating the use of the Kinects tilt motor and LED status light)
  * determined the correct message subcriptions and fixed frame in order to display the Kinect data
  * determined that segmentation faults of Rviz are endemic to ros-hydro, seg.faults occur intermittently on startup and adding images

* learned basic Python using Lynda tutorials
* learned about additional ROS nodes

  * image_view
  * rqt_graph

* researched the format of depth data transmissions from the Kinect

  * found three algorithms for converting the 11-bit disparity data into distance data 

* reinstalled SimpleOpenNI dependencies in the hopes of installing the older version of the library

  * NiTE
  * OpenNI
  * Eigen3
  * Swig
  * Boost
  
* edited Supun's KinectTest.java to display depth data using JFrame 

  * studied the libfreenect example using OpenGL, a much faster graphics visualizer
  * points are colored red, yellow, or blue depending on the distance from the sensor

* found two compression techniques shown to be useful in handling Kinect depth data, LZ4 and RLECodec

  * found a Java library implementing LZ4 compression that has been shown to be useful with Kinect depth data  

* wrote a program that recieves Kinect depth data, compresses the data using LZ4, prints the uncompressed and compressed data to two text files, decompresses the data, and displays the colored distance data in a JFrame

What Has Not Been Achieved This Week?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* installing and building SimpleOpenNI2 library or SimpleOpenNI, this library will not be used for the project
* successful compression of depth data

  * the LZ4 library is invoked correctly (it seems) but the text files show no decrease in size

* programming a smoother display for depth data, the JFrame lags considerably

* programming a smooth gradient of colored distance data as opposed to color thresholds

What is Planed For Next Week?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* implementation of an efficient compression algorithm along with useful data filters
* programming a client to send depth information to the IoTCloud2 server
* implementation of depth disparity to distance algorithms of higher accuracy
* improving the program displaying colored depth data

Links
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
http://thebytekitchen.com/2014/03/24/data-compression-for-the-kinect/
https://github.com/jpountz/lz4-java

Week 3
----------------------------------------------------------------------

What Has Been Done This Week
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* implemented two Java compression libraries

  * Snappy, a Run Length Encoder by Google
  * Jzlib, a Java implementation of Zlib; Jzlib offers greater compression and will be used
  
* improved my depth display program to color depth points with a smooth gradient ranging through several colors

 .. image:: ../images/ScrnShot.png

* implemented a more accurate depth calculation algorithm as a table look-up
* wrote a program that performs basic object detection using the kinect

  * ObjDetect.java
  
* completed several RabbitMQ tutorials
* wrote programs using RabbitMQ that send kinect data over computer networks 
  
  * SendFrame.java
  * RecvFrame.java

What Has Not Been Achieved This Week?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* compression per frame of less than 100 kB
* an optimized program for the transmission of kinect depth data
  * current program has a delay of ~1 second
* implementation of useful filters on depth data (e.x. DiscreteMedianFilter from TheByteKitchen)

What is Planed For Next Week?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* collaborate with Supun to integrate my code into the IoTCloud project proper
* write program to perform real time processing on depth data on the cloud
* hook up the kinect to robots and test my programs
* optimize depth transmission 

Links
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
* http://www.jcraft.com/jzlib/
* http://www.rabbitmq.com/

Week 4
----------------------------------------------------------------------

What Has Been Done This Week
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* had meetings with Supun to evaluate our current project and determine how best to move forward
* fixed my computer, it was unusable for a day and a half
* wrote code that Supun used in a bolt that detects whether there are any object in front of the turtlebot past a certian threshold
* wrote a rough draft of a project abstract
* resolved bug in RecvFrame.java program that was crashing the program
* found code that allows the Kinect distance information to be converted into a point cloud
* wrote a Bash script that allows the user to configure and run SendFrame.java and RecvFrame.java simultaneously
* wrote new versions of SendFrame.java and RecvFrame.java implementing a new compression algorithm on top of JZlib (algorithm taken from paper below)

  * increased compression time from ~19 ms to ~10 ms
  * increased compression ration from ~5:1 to ~10:1
  * achieved a compression of 50 kb per frame

What Has Not Been Achieved This Week?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* resolution of bug in SendFrame.java that causes the program to crash and requires a full reset of hardware
* a smooth color gradient in the new RecvFrame.java program
* sending frames at 500 kb/s (currently at 750 kb/s)

What is Planed For Next Week?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* continue to optimize depth transmission 
* add color gradient to the new RecvFrame.java program
* complete two turtlebot demo programs

  * the turtlebot will follow a person at a set distance
  * the turtlebot will recieve user input but refuse to drive past a certain closeness to detected objects

* demo turtlebot functionality for Dr.Fox

Links
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
* http://research.microsoft.com/pubs/153971/depthcode-final.pdf

Week 5
----------------------------------------------------------------------

What Has Been Done This Week
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* improved SendFrame_new.java

  * implemented a table look up for the inversion algorithm
  * fixed compression error by increasing buffer size
  * implemented prediction algorithm (did not improve compression time, will not be used)

* installed IoTCloud2 on my personal computer

  * configured ROS settings to allow for communication between ROS nodes on multiple computers
  * solved connectivity problem between my personal computer and the Turtlebot laptop; connected personal computer to ethernet since wireless did not work
  * installed maven 3
  * solved maven compiler plugin error, pom files needed to be updated to use a newer java version
  
* researched an RLE compression algorith using the Golomb-Rice coding technique
* deployed the Turtlebot sensor in IoTCloud2

  * installed storm-incubator
  * installed storm-broker-connenctors
  * updated the rosjava used with the turtlebot from electric to hydro
  * fixed errors in pom.xml dependencies and the same compiler version error as IoTCloud2
  * added new dependcies from the rosjava maven repository to pom.xml files (rosjava_core, rosjava_messages, rosjava_bootstrap)
  
* got the Turtlebot up and running on my personal computer

  * added rabbitmq.config file allowing the Turtlebot computer to access the rabbitmq server run on my personal computer
  * manually linked IoTCloud2 libraries to the Turtlebot project on my personal computer
  * removed a line of code calling for a command line argument in TurtleController.java
  
* worked on improving the follower code

  * implemented the SendFrame_new compression, SendFrame compression was used previously

What Has Not Been Achieved This Week?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* dynamic buffer allocation for compression

  * I was unable to use the JZlib methods designed for this end (ZOutputStream, ZInputStream) 

* full functionality of follow me with the new compression

What is Planed For Next Week?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* finish both turtlebot demo programs
* get turtlebot running with cloud processing on my personal computer
* begin writing a paper/making a poster 

Links
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* https://github.com/supunkamburugamuva/storm-broker-connectors
* https://github.com/apache/incubator-storm
* http://maven.apache.org/
* https://github.com/rosjava/rosjava_mvn_repo
* https://github.com/turtlebot

Week 6
----------------------------------------------------------------------

What Has Been Done This Week
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* continued to improve the follower code

  * fine tuned constants
  * planned possibly solutions to allow the turtlebot to find users that have stepped out of frame
  
* ran the turtlebot using storm on my personal computer

  * deployed the turtlebot sensor in IoTCloud2
  * deployed the storm topology
  * hardcoded my personal ip
  * corrected naming errors 
  * corrected typos in documentation
  
* began work on a write-up of my contributions to the project

  * rewrote a proper abstract
  * researched compression and message sending techniques employed
  
* modularized the compression and decompression as a seperate class, Compressor

What Has Not Been Achieved This Week?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* final improvements to the follower program
* measure latency and message rates of the system when using the cloud

What is Planed For Next Week?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* fine tune the follower program
* test the scalability of the system using simulated sensors
* finish writing a paper

Links
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* http://storm.incubator.apache.org/
