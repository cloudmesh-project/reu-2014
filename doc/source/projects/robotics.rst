IoTCloud2
======================================================================

Team
----------------------------------------------------------------------
Leif Christiansen grindvald@gmail.com

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
