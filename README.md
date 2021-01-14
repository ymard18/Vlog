# Vlog
Install Hadoop

Step 1: Click here to download the Java 8 Package. Save this file in your home directory.

Step 2: Extract the Java Tar File.
Command: tar -xvf jdk-8u101-linux-i586.tar.gz

Step 3: Download the Hadoop 2.7.3 Package.
Command: wget https://archive.apache.org/dist/hadoop/core/hadoop-2.7.3/hadoop-2.7.3.tar.gz

Step 4: Extract the Hadoop tar File.
Command: tar -xvf hadoop-2.7.3.tar.gz
Step 5: Add the Hadoop and Java paths in the bash file (.bashrc).
Open. bashrc file. Now, add Hadoop and Java Path as shown below.

Command:  vi .bashrc
Then, save the bash file and close it.

For applying all these changes to the current Terminal, execute the source command.

Command: source .bashrc
To make sure that Java and Hadoop have been properly installed on your system and can be accessed through the Terminal, execute the java -version and hadoop version commands.


Step 6: Edit the Hadoop Configuration files.
Command: cd hadoop-2.7.3/etc/hadoop/
Step 7: Open core-site.xml and edit the property mentioned below inside configuration tag:
core-site.xml informs Hadoop daemon where NameNode runs in the cluster. It contains configuration settings of Hadoop core such as I/O settings that are common to HDFS & MapReduce.

Command: vi core-site.xml

