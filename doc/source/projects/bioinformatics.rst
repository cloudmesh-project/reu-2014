BioInformatics: Genomic Sequence Analysis Automation
======================================================================

Team
----------------------------------------------------------------------
Lorander S. Saggu
lsaggu@indiana.edu

Mentors: Saliya Ekanayake, Yang Ruan

Abstract
----------------------------------------------------------------------
An organisms genetic code determines everything about that organism: it determines what species the organism will become, how big it will grow, whether or not it will have gills or will be able to convert light into energy. The genetic code of many organisms is quite similar, but of course there are differences which allow for every unique individual. If the similarity between genetic sequences could be mapped, deriving and understanding the relationships between organisms could be done efficiently and effectively. Dr. Geoffrey Fox and his lab are trying to do exactly that: map the similarity between genomic sequences. They seek to do this using complex algorithms within computer programs they have designed that essentially define "distances" between genomic sequences, and these distances can be scaled and used to create a plot. There is, of course, some work to be done. These processes developed by Dr. Fox and his lab are heuristic and only understood and accessable by a few. Also they aren't automated. However, by setting up a server to run a Java based portal designed to accept user input via the web and run these algorithms on computer clusters, these issues could be dealt with. Being able to efficiently map the differences in genomic sequences will vastly improve people's understanding of where the organisms of today arose. This may also have vast implications in the realms of geneology, and medecine as a result of the improved understanding of the relationships between various organisms.

Problem
----------------------------------------------------------------------

Currently, Dr. Fox and his team have developed methods for processing,
analyzing, and mapping genomic sequence data. Dr. Fox's team has
received new data which needs to be processed and analyzed.

However, these processes and methods are incredibly heuristic and
prone to error. There methods in place are constantly subject to
tweaking and fine tuning. Also, the tools and processes in place are
currently understood only by a few making it difficult for other groups or scientists to be able to access and use them.


Design
----------------------------------------------------------------------

Essentially, I will work with Saliya Ekenayake, Yang Ruan, and
Dr. Geoffrey Fox in order to analyze and process the new data and
develop a 3D relational-mapping of the data so that I may develop an understanding of the tools and of the process.

Then, pimarily, I will seek to develop a system which would allow users
to communicate their data to tools which would more efficiently
process the data on computer clusters and produce useful output for
the users.

Implementation
----------------------------------------------------------------------
I will seek to create a portal with a front and back end will be designed in Java. The front end will accept user information via the web, while the back end will take the information and run the sequence analysis software before returning the results. A central server will host this program which will remotely access computer clusters as necessary.

Visualization Tools:	PlotViz

Keywords
----------------------------------------------------------------------
Bioinformatics, Clusters, Distance-Matrix, Genomics, Map-Reduce, Phylogenic Tree, Twister
	

Links
----------------------------------------------------------------------


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


Uncompleted This Week:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Connecting to FutureGrid using jsch in Java portal
- Completing PBS script to run on cluster.


Next Week:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Gain a better understanding of the arguments/commands necessary to run the Twister-Pipeline.

- Continue developing the portal framework: be able to connect to cluster and submit a job.

- Use allocated nodes in Quarry to run Twister-Pipeline on larger data set.


