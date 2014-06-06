Week 1
======================================================================

What Has Been Done This Week
----------------------------------------------------------------------

This week was spent on several tasks. Firstly, familiarizing myself with the Kinect sensor. This involved examining the hardware and current scientific applications involving the Kinect. In order to accomplish this task I utilized a variety of web sources detailing its construction and functioning. I also read several articles, links are included below, documenting research projects involving the Kinect. In doing so I gained a better understanding of the functioning of the Kinect's depth camera,  ie the measurements performed and data recorded, and its possible use in a research setting. 
Secondly, I met frequently with Supun in order to fully grasp the goal and scope of his project. This also involved further reading on software that would be used. As of now, for the project we will utilize the Kinect driver provided from OpenKinect, the graphics software Processing, the java library SimpleOpenNI and ROS. I spent time scanning the documentation on these softwares and then began my third task, installing them.
I successfully installed the OpenKinect drivers but ran into problems installing the Java wrapper. Supun informed me that I needed to build the .so files and not just download them. This required me to download a number of dependencies. I also ran into a compiling error because the version of java used to compile was not the same as the one used to run. This problem was solved and I was eventually able to successfully compile and run the sample code provided by OpenKinect. I also wrote some of my own code exploring the OpenKinect library, moving the sensor up and down as well as changing the LED settings.
After this I moved on to installing and building the SimpleOpenNI library. This required I download a number of dependencies and install OpenNI and NiTE. I spent a long time working through numerous errors that occurred in this process only to discover that OpenNI is out of date and there is a new version OpenNI2. OpenNI has been successfully built but I have not been able to install OpenNI2. Furthermore, the company that developed and distributed NiTE, PrimeSense, was recently bought by Apple and the open source code has been eradicated. I tried to remove all references to NiTE in the Cmake file of SimpleOpenNI but even after doing so could not successfully build the .so file.
I found a couple of other libraries that might be useful, one by Daniel Shifman and the other by PCL. I will discuss these with Supun. 
After explaining my difficulties with SimpleOpenNI2 to Supun he suggested that I devote my time to some other task and he would see if he could solve the problem. So I installed ROS along with two ROS software packages, Rviz for 3D visualization and the ROS freenect Kinect driver. I again ran into errors and have been unable to load the Kinect camera data into Rviz. I also spent some time working through ROS tutorials to familiarize myself with the software.

What Has Not Been Achieved This Week?
----------------------------------------------------------------------

*	This week I was unable to install and build the SimpleOpenNI2 library and thus was unable to accomplish my task of recording the depth image information from the sensor.
* I could not successfully connect the Kinect to Rviz.

What is Planed For Next Week?
----------------------------------------------------------------------
Next week I plan on continuing to learn about the ROS software, build a library that will be used to write code for the Kinect (whether it be SimpleOpenNI2 or otherwise) and record depth image data from the Kinect.
