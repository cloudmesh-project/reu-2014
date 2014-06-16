IoTCloud2
======================================================================

Team
----------------------------------------------------------------------
Leif Christiansen grindvald@gmail.com

Supun Kamburugamuva supun06@gmail.com

Problem
----------------------------------------------------------------------

Perform real time parallel computing on Kinect sensor data recieved from
large numbers of simulated turtlebots so that they may avoid objects.
The goal of the project is to improve upon the efficiency of Supun
Kamburugamuva's previous implementation so that a larger number of 
robots may be operated simultaneously.

Design
----------------------------------------------------------------------


Implementation
----------------------------------------------------------------------


Links
----------------------------------------------------------------------

* https://github.com/supunkamburugamuva/iotcloud2
* https://github.com/iotcloud/reu
* http://openkinect.org/wiki/Main_Page
* http://code.google.com/p/simple-openni/
* https://github.com/iotcloud/reu
* https://github.com/supunkamburugamuva/iotcloud2
* https://github.com/supunkamburugamuva/sensorstream
* http://www.processing.org/
* http://www.ros.org/
* http://shiffman.net/p5/kinect/reference/org/openkinect/processing/Kinect.html


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

Links to Articles
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
* www.cs.washington.edu/robotics/postscripts/3d-mapping-iser-10-final.pdf
* http://scholar.google.com/scholar_url?hl=en&q=http://www.mdpi.com/1424-8220/12/2/1437/pdf&sa=X&scisig=AAGBfm0cShgyJ38PAqssax-iG5vzh88IIg&oi=scholarr
* http://research.microsoft.com/pubs/155378/ismar2011.pdf
* http://www.cs.washington.edu/robotics/postscripts/icra11-scene-differencing.pdf

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
