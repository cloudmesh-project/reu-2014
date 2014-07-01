How to install Apache Maven 3.2.1 on Ubuntu 12.04.3
-------------------------------------------------------

*The following developed documentation is comprised with the guide
of official documentation along with personal encounters with Ubuntu Desktop 12.04.3*

*Source: http://maven.apache.org/download.cgi*


**First begin by confirming that Java is installed, Maven 3.2.1 requires JDK, not JRE**

If Java is **NOT** present, do the following:

1.	Search Java 6, click the link that reads "Java Archive Downloads-Java SE 6-Oracle"
2.	Proceed to the left tab for Java Se, click downloads tab
3.	Click image that reads "Java Platform (JDK) 8u5"
4.	Scroll until you reach Linux x86 (file size 152.5MB) jdk-8u5-linux-i586.tar.gz file
5.	Click file to download

Once Java is present go online to Maven site referenced above and proceed with the instructions under Unix-based
Operating Systems (Linux …+) Steps 1-7

**If following messages appear:**

``ERROR: JAVA_HOME is not defined correctly cannot execute /usr/java/jdk1.7.0_51/bin/java``
OR
``Warning: JAVA_HOME environment variable is not set``

1.	Record the location of ‘Java home:’ ---this will be utilized to set a Java home, record Maven home just in case as well
2.	``$ export JAVA_HOME='location recorded'``
3. Enter 

4. Maven will not work properly unless you set the $PATH, $M2, and $M2_HOME variables

``$ export PATH=$M2:$PATH`` (essentially step 5 found on the website)

5. Enter 
6. ``$ mvn –version`` **NOTICE:** ``mvn –version`` **NOT** ``mvn --version``

If Maven is correctly installed, your terminal will display something similar:

``Apache Maven 3.0.4
Maven home: /usr/share/maven
Java version: 1.6.0.31, vendor: Sun Microsystems Inc.
Java home: /usr/lib/jvm/java-6-openjdk-i386/jre
Default locale: en_us, platform encoding:UTF-8
OS name: "linux", version: "3.8.0-29-generic", arch "i386", family: "unix"``

**TO CHECK LOCATIONS:**

* Maven location: ``$ ls ls /usr/share/maven``

* Config files: ``$ ls -ls /etc/maven``
