How to install Chef Enterprise and set up a Workstation in Ubuntu 12.04.3
---------------------------------------------------------------------------------
*The following developed documentation is comprised with the guide
of official documentation along with personal encounters with Ubuntu Desktop 12.04.3.*

*Source: https://www.youtube.com/watch?v=r3mN2M9n51Y*

**Install Chef**

1.	Travel to http://www.opscode.com 
2.	Click "Get Chef" button in upper right-hand corner of page and choose the "Hosted Chef" option 
3.	While looking at the sign-up page, don’t sign up just yet!
  *	On the right hand side, click the link that says "Start with the Chef-client and server installation"
  *	Choose Ubuntu for OS, your specified version, and the "x86_64" architecture
  *	When prompted choose the Chef version "11.6.2-1"
4.	In looking at the "Quick Install Instructions" after opening the terminal:
  *	Login to sudo using the command ``$ su`` and insert your password
  *	Copy & paste the command given in "Quick Install Instructions" (you may have to type the prompt)
  *	Click Enter and the installation process should begin
  *	Process will be complete when terminal reads ``Thank you for installing Chef!``
  
*You have just installed Chef, the Ruby language, knife (command line tool for admin), chef-client (Client application),
ohai (system profiler), and many more*

**Create a User**

1.	Travel to http://opscode.com 
2.	Click the link that says "Get Chef", you will be signing up for the free trial of Enterprise Chef

  *	When signing up for an account, make sure your Chef Organization name is "globally unique"
  *	Fill out the form and agree to the terms and services agreements
  *	Click Get Started
  *	Go to Create Organization and create a "globally unique" name/short name
  *	Once finished, click link that says "Create Organization" 
3.	On the next screen, download the starter kit –**SAVE** the file, this should automatically save as a .zip file, if not make those adjustments

  *	Move the folder that reads "chef-starter.zip" somewhere that is convenient 
  *	To check the contents of that folder, open the file and you should see the chef-repo directory
  
**Using knife –the command line tool for the chef data index**

*If you have no text editor, I recommend using Sublime Text 2 or Notepad++, which can be downloaded
and found via searching the web. There is a link on the Apache Big Data Stack page*

1.	Inside the terminal type the command ``$ chef-repo``
2.	Type ``$ dir`` 
  * A list of files in the chef-repo folder should display
3.	Type ``$ dir .chef``
  *	This should display three files in the .chef directory
    * ``knife.rb``, ``organization name-validator.pem``, and ``user.pem``
4.	Open your text editor, go to File, Open a folder, open the "chef-repo" folder
  *	Once clicking the "chef-repo" folder a sidebar menu will display itself on the side of your text editor
      *	Under "chef" drop-down, click the "knife.rb" and a file should be displayed in your text editor. 
      knife.rb will be used to configure your local work station
*The following step will verify that knife is working correctly and that configuration is accurate*

5.	Type the command ``$ knife –version`` (this will show you that chef is installed and the specific version)
  *	Type the command ``$ knife client list`` (this will ensure that your configuration is accurate and is connected to the chef server) – should return ``nameoforganization-validator``

**Source Code Repository** (this will track changes over time)

1.	Type the command ``$ git init`` and then ``$ git status`` (this will create an empty Git repository in chef-repo)

2.	Type the command ``$ git add  .`` to add all files to the repository

3.	``$ git status``

4.	``$ git commit –m "the starter kit from Chef"`` (this adds all the files and commits them to the source code repository)

5.	Run ``$ git status``  to ensure a clean repository 

**Confirming Organization for Enterprise Chef**

*If not already logged in to Enterprise Chef* 

1. From the opscode homepage (link above), click the Get Chef link, and login to Enterprise Chef

2.	Browse to "Administration" tab to see the organization listed

**Setting Up a Node using the knife bootstrap command**

1.	First ensure that you are in the chef-repo directory

2.	Type the command ``$ knife bootstrap –help`` (will show options/ways to use chef bootstrap)

3.	In order to bootstrap the target instance, type the following command ``$ knife bootstrap HOSTNAME –sudo –x USERNAME –P PASSWORD –N "target1"``

*Username, password, hostname, and node name will depend on the node you choose and its particular properties*

4.	Click Enter (wait time will vary) 
  *	If problems are encountered, check for correct hostname, username, password, and node name. Also, check to verify if a port number is needed based on the node selected. *If necessary check out the Chef Fundamentals Webinar link for setting up a node, which can be found on the Apache Big Data Stack page*
  *	You will know that the connection is complete when the following is exhibited ``Chef Client finished, 0/0 resources updated …``
  
5.	Login to Hosted Enterprise Chef

6.	After viewing the Nodes tab, if node is not visible already, refresh the web page and your node should be displayed under "Node Name"
  *	Clicking on the node will display further details
    *	Take a look at the "Details", "Attributes", and "Permissions" tabs

