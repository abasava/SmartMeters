Sources to get data
===================
SMARTMeters project Team 3

----Avinash Basavaraj------
----Emma Hamilton----------
----Lila Ghemri------------


1. Create the account on the git hub 
2. Fork the existing project templete with in the git hub
3.login into the ubuntu machine using "ssh -i .ssh/bootcamp.pem ubuntu@team3.from-tx.com" for mac machine
4.Install the git in the ubuntu machine using "sudo apt-get install git"
5.Clone the Github project to the ubuntu local using "git clone git@github.com:abasava/SmartMeters.git"
6.Download and install the CDH(Cloudera Manager) refer the chapter 1 for more details.
7.Download the data , clean and save in the linux file system  "scp -i ~/.ssh/bootcamp.pem SDGE.csv ubuntu@team3.from-tx.com:/home/ubuntu"
8.Copy the file into the HDFS cluster using " hdfs dfs -put SDGE.csv team3/data/SDGE.csv" after creating the folders in HDFS.
9.Started the HIVE to create the table " create table sdgedata (timestart string,timeend string,usage float) 
    > row format delimited
    > fields terminated by ',';"
10. Load the CSV data to HIVE table " load data inpath 'team3/data/SDGE.csv' into table sdgedata;" 
11. Run the queries in the HIVE command for example "select * from sdgedata;"



Thanks 
Team3




