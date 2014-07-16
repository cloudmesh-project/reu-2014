PlotViz: A Bioinformatic Visualization Tool
======================================================================

Team
----------------------------------------------------------------------
- Khaliq Satchell

  ksatchel@indiana.edu


- Geoffrey Fox (Mentor)

  gcfexchange@gmail.com


- Yang Ruan (Mentor)

  yangruan@indiana.edu


- Saliya Ekanayake (Mentor)

  esaliya@gmail.com

Problem
----------------------------------------------------------------------

I will be working to develop visualization support for multithreading PlotViz3 in order to speed up its processes.


How to Build the Libraries in Windows 7 Ultimate SP1 64 Bit
----------------------------------------------------------------------

1.  Download and install Microsoft Visual Studio 2010, CMAKE, and NSIS.
2.  Download and extract pviz3 and pviz3dev files to the root directory.
3.  Add a new folder in pviz3dev called "workspace".
4.  Open the Control Panel, go to System Security and click on System.
5.  In System, click on Advanced System Settings.
6.  In the Advanced tab click on Environment Variables.
7.  Click New located under User Variables for (Username).
8.  Add "PVIZ3DEV_HOME" for variable name and "C:\pviz3dev" for variable value and click OK.
9.  Add "PVIZ3_SRC" for variable name and "C:\pviz3" for variable value and click OK.
10. Add "PVIZ3DEV_WORKSPACE" for variable name and "C:\pviz3dev\workspace" for variable value and click OK.
11. Click OK to exit out of Environment Variables and exit out of Advanced System Settings.
12. Logout of computer and log back in to set changes.
13. Open Visual Studio x64 Win64 Command Prompt (2010) by opening the start menu and going to All Programs.
14. In All Programs, click on Microsoft Visual Studio 2010.
15. In Microsoft Visual Studio 2010, click on Visual Studio Tools and then click on Visual Studio x64 Win64 Command Prompt (2010).
16. In the command prompt, type "cd %PVIZ3_SRC%\build" and press enter.
17. Type in "%PVIZ3_SRC%\config.bat".
18. After the operation is complete, type "nmake" and press enter.
19. A solution file called PVIZ3(PVIZ3.sln) will be created for Visual Studio 2010 in this location: C:\pviz3\build-vs.
20. Open the solution file and build PACKAGE and INSTALL.
21. After they both succeed you are free to change the code.

Implementation
----------------------------------------------------------------------

PlotViz3

Microsoft Visual Studio 2010
	

Links
----------------------------------------------------------------------

http://salsahpc.indiana.edu/pviz3/#developers

- Where you can learn how to build the libraries for PlotViz3

http://salsahpc.indiana.edu/pviz3/#downloads

- Where you can download PlotViz3

Progress Report
----------------------------------------------------------------------

Progress:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- [done, Week 1] Chose a research project
- [done, Week 1] Learned about the functions of PlotViz3
- [done, Week 1] Read previous research papers
- [done, Week 1] Downloaded PlotViz3
- [in progress, Week 4] Learning how to implement a C++ parallel version of matrix multiplication
- [in progress, Week 4] Built the libraries for PlotViz3

Problems:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- [Week 1] Couldn't access salsadev svn repository
- [Week 2] Constantly getting errors while trying to build libraries for PlotViz3
- [Week 3] My computer's hard disk drive is failing so I was unable to complete any work

Plans:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- [Week 2] Finish building libraries for PlotViz3
- [Week 2] Learn how to use PlotViz3
- [Week 3] Finish building libraries for PlotViz3
- [Week 4] Have laptop fixed so that I may once again try to build the libraries for PlotViz3
