BioInformatics: Genomic Sequence Analysis Automation
======================================================================

Team
----------------------------------------------------------------------
Lorander S. Saggu
lsaggu@indiana.edu

Mentors: Saliya Ekanayake, Yang Ruan

Abstract
----------------------------------------------------------------------
An organisms genetic code determines everything about that organism: it determines what species the organism will become, how big it will grow, whether or not it will have gills or will be able to convert light into energy. The genetic code of many organisms is quite similar, but of course there are differences which allow for every unique individual. If the similarity between genetic sequences could be mapped, deriving and understanding the relationships between organisms could be done efficiently and effectively. Our team is trying to do exactly that: map the similarity between genomic sequences. Using complex algorithms within computer programs, the team has been able to define "distances" between genomic sequences, and these distances can be scaled and used to create a plot. There is, of course, some work to be done. These processes developed by the lab are heuristic and only understood and accessable by a few. Also they aren't automated. However, by setting up a server to run a Python based portal designed to accept user input via the web and run these algorithms on computer clusters, these issues could be dealt with. Being able to efficiently map the differences in genomic sequences will vastly improve people's understanding of where the organisms of today arose. This may also have vast implications in the realms of geneology and medecine as a result of the improved understanding of the relationships between various organisms.

Problem
----------------------------------------------------------------------

Currently, methods for processing,
analyzing, and mapping genomic sequence data have been developed. The team has
received new data which needs to be processed and analyzed.

However, these processes and methods are incredibly heuristic and
prone to error. The methods in place are constantly subject to
tweaking and fine tuning. Also, the tools and processes in place are
currently understood only by a few, making it difficult for other groups or scientists to be able to access and use them.


Design
----------------------------------------------------------------------

Essentially, I will work to analyze and process the new data and
develop a 3D relational-mapping of the data so that I may develop an understanding of the tools and of the process.

Then, pimarily, I will seek to develop a system which would allow users
to communicate their data to tools which would more efficiently
process the data on computer clusters and produce useful output for
the users. This system will interface with existing frameworks (Cloudmesh, FutureGrid).

Implementation
----------------------------------------------------------------------
I will seek to create a portal in Python that will interface with the Cloudmesh front-end framework. The front end will accept user information via the web, while the back end will take the information and run the sequence analysis software before returning the results. A central server will host this program which will remotely access computer clusters as necessary.

Visualization Tools:	PlotViz

Keywords
----------------------------------------------------------------------
Bioinformatics, Clusters, Distance-Matrix, Genomics, Map-Reduce, Phylogenic Tree, Twister
	

Links
----------------------------------------------------------------------
ClusterLink: https://github.com/lsaggu/clusterLink

Week 1: 6/6/2014
----------------------------------------------------------------------

Done This Week:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Determined what project I will be working on: Studying and processing genomics data, specifically fungi genome sequences, and trying to create an accurate visualization of the relationship between the different sequences.

- Studied up on using PlotViz, a visualization tool
- Studied Map-Reduce, MPI (Message Passing Interface), phylogenetic trees, multi-dimensional scaling, and clustering. 
- Spent time studying the past results and documents produced by Dr. Fox and his team on genomics analysis.

- Worked with Saliya Ekenayake to set up and deploy the Pairwise Clustering tool on the “R2” genomic data.

- Began setting up accounts in order to work with Yang Ruan in processing new genomic “D1” data through the Twister pipeline.

- Spoke with Saliya about a potential shift in the scope of my project	towards developing a system that would allow users to enter data through the internet and submit that data appropriately to the computer clusters that would process it.

- Began moving forward with the "Twister" pipeline after establishing a FutureGrid account.

Uncompleted This Week:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Run the Smith-Waterman algorithm on the new “D1” data in order to create a genomic distance matrix.

- Need to finish applying for and creating accounts for computer cluster access in order to run the algorithm mentioned above.

- Solidify end goals of project in terms of what IU-SROC program expects.

Next Week:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Complete account creation/general setup if any remains.  
- Begin processing genomic data through Twister Pipeline. I need to document the process! Or at least maintain notes of the steps involved.

- Update goals and next steps for project. Determine what I will actually be doing.

Week 2: 6/9 - 6/13
----------------------------------------------------------------------

Done This Week:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Completed setting up the environment to run Twister in FutureGrid

- Ran a sample data set through the Smith-Waterman, PWC, and MDS algorithms in FutureGrid in order to obtain a visualization viewed with PlotViz.

- Began working on the portal framework which will ultimately be able to access clusters remotely and submit scripts that will run the algorithms.

- Set up Twister environment in Quarry and requested nodes to work with.

- Updated project goals: Develop a back-end system in Python that will connect to and submit jobs to a computer cluster and integrate with Cloudmesh

- Set up Linux machine to work on with Saliya


Uncompleted This Week:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Connecting to FutureGrid using jsch in Java portal
- Completing PBS script to run on cluster.

- Downloading appropriate Python libraries for ssh connection and PBS scripting.


Next Week:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Gain a better understanding of the arguments/commands necessary to run the Twister-Pipeline.

- Continue developing the portal framework now in Python: be able to connect to cluster and submit a job.

- Generate the PBS script to be sent by Python program.

- Use allocated nodes in Quarry to run Twister-Pipeline on larger data set.

Week 3 6/16 - 6/20
----------------------------------------------------------------------
Done This Week:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
- Began designing clusterLink.py: uses sh library to connect to grid via command line and submit a PBS script to be run on the cluster

- Began working on a test PBS script to be submitted to cluster.

- Successfully sent testPBS script to run on cluster using python program: clusterLink.py

- Completed file modification functions in Bash script (twisterScript)
- Completed simple script to run Twister.

- Developed python function to dynamically create Twister script which will run SWG and PWC algorithms on given data
	


Uncompleted This Week
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Getting TwisterScript to successfully submit a TWISTER job on FutureGrid
- Still have some development left to do on python program and script.

Next Week
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Need to meet with Yang and go over script and over Quarry Jobs!
- Successfully run script REMOTELY on FutureGrid.
- RUN MDS on QUARRY on 56k + 1k data

Week 4 6/23 - 6/27
----------------------------------------------------------------------
Done This Week:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
- Developed clusterLink.py program
- Managed to successfully run a script on FutureGrid computer cluster
- Completed get_status and transfer methods for clusterLink.py which print the status of a job and transfer files to the remote host respectively.
- Discussed next steps regarding integration of clusterLink.py with Cloudmesh with mentors

Uncompleted This week
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
- I left early this week for a leadership development program
- Need to install Cloudmesh and CMD3
- Read up on the documentation necessary for integration with Cloudmesh!

Next Week
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
- Install Cloudmesh and CMD3 in order to integrate clusterLink.py into the Cloudmesh framework
- Develop dynamic script generation with Saliya and Yang



