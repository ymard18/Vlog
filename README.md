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
![image](https://user-images.githubusercontent.com/75766691/104581761-f8dab580-5699-11eb-9a42-267e53e0c6f8.png)

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

Step 8: Edit hdfs-site.xml and edit the property mentioned below inside configuration tag:
hdfs-site.xml contains configuration settings of HDFS daemons (i.e. NameNode, DataNode, Secondary NameNode). It also includes the replication factor and block size of HDFS.

Step 9: Edit the mapred-site.xml file and edit the property mentioned below inside configuration tag:
mapred-site.xml contains configuration settings of MapReduce application like number of JVM that can run in parallel, the size of the mapper and the reducer process,  CPU cores available for a process, etc.

In some cases, mapred-site.xml file is not available. So, we have to create the mapred-site.xml file using mapred-site.xml template.

Command: cp mapred-site.xml.template mapred-site.xml

Command: vi mapred-site.xml.

Step 10: Edit yarn-site.xml and edit the property mentioned below inside configuration tag:
yarn-site.xml contains configuration settings of ResourceManager and NodeManager like application memory management size, the operation needed on program & algorithm, etc.

Command: vi yarn-site.xml

Step 11: Edit hadoop-env.sh and add the Java Path as mentioned below:
hadoop-env.sh contains the environment variables that are used in the script to run Hadoop like Java home path, etc.

Command: vi hadoop–env.sh

Step 12: Go to Hadoop home directory and format the NameNode.
Command: cd

Command: cd hadoop-2.7.3

Command: bin/hadoop namenode -format

Step 13: Once the NameNode is formatted, go to hadoop-2.7.3/sbin directory and start all the daemons.
Command: cd hadoop-2.7.3/sbin

![image](https://user-images.githubusercontent.com/75766691/104582541-f9278080-569a-11eb-888e-717d02ec2d02.png)

Hadoop is an open-source software framework for storing data and running applications on clusters of commodity hardware. It provides massive storage for any kind of data, enormous processing power and the ability to handle virtually limitless concurrent tasks or jobs.

1. Scalable
Hadoop is a highly scalable storage platform, because it can store and distribute very large data sets across hundreds of inexpensive servers that operate in parallel. Unlike traditional relational database systems (RDBMS) that can't scale to process large amounts of data, Hadoop enables businesses to run applications on thousands of nodes involving thousands of terabytes of data.

2. Cost effective
Hadoop also offers a cost effective storage solution for businesses' exploding data sets. The problem with traditional relational database management systems is that it is extremely cost prohibitive to scale to such a degree in order to process such massive volumes of data. In an effort to reduce costs, many companies in the past would have had to down-sample data and classify it based on certain assumptions as to which data was the most valuable. The raw data would be deleted, as it would be too cost-prohibitive to keep. While this approach may have worked in the short term, this meant that when business priorities changed, the complete raw data set was not available, as it was too expensive to store. Hadoop, on the other hand, is designed as a scale-out architecture that can affordably store all of a company's data for later use. The cost savings are staggering: instead of costing thousands to tens of thousands of pounds per terabyte, Hadoop offers computing and storage capabilities for hundreds of pounds per terabyte.

3. Flexible
Hadoop enables businesses to easily access new data sources and tap into different types of data (both structured and unstructured) to generate value from that data. This means businesses can use Hadoop to derive valuable business insights from data sources such as social media, email conversations or clickstream data. In addition, Hadoop can be used for a wide variety of purposes, such as log processing, recommendation systems, data warehousing, market campaign analysis and fraud detection.
