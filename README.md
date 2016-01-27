



# rmr2

This package enable writing R programs for the Hadoop Mapreduce system, that is parallel distributed programs for the most popular big data platform.


## Requirements

 - A Hadoop custer running any recent Hadoop distribution (CDH3 and higher, Apache Hadoop 2.2.0 and higher, HDP2 and higher) 
 - R installed on each node of the cluster (3.0 or higher)

## Installation

`rmr2` itself needs to be installed on each node with the following expression: 


```r
install.packages("rmr2", repos = c("http://archive.rzilla.org", unlist(options("repos"))))
```

## Configuration

`rmr2` needs two env variables to be set (only on the master node): `HADOOP_CMD` and `HADOOP_STREAMING`. `HADOOP_CMD` should contain the main `hadoop` command whereas `HADOOP_JAR` should be set to the streaming jar, named something like `hadoop-streaming*.jar`, where the exact naming depends on version and distribution. Optionally, `HDFS_CMD` can be set to help `rmr` locate the `hdfs` command executable, which at this time only spares a few warnings, but may be mandatory in the future. 

## Version

The current version is 3.3.1 .


