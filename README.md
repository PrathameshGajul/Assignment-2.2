Explain in detail:

a)HDFS
Ans:
1)Hadoop File System was developed using distributed file system design. It is run on commodity hardware.Unlike other distributed  systems,HDFS is highly faulttolerant and designed using low-cost hardware.
2)HDFS holds very large amount of data and provides easier access. To store such huge data, the files are stored across multiple machines. These files are stored in redundant fashion to rescue the system from possible data losses in case of failure.
3)HDFS also makes applications available to parallel processing.
4)Features of HDFS
  -It is suitable for the distributed storage and processing.
  -Hadoop provides a command interface to interact with HDFS.
  -The built-in servers of namenode and datanode help users to easily check the status of cluster.
  -Streaming access to file system data.
  -HDFS provides file permissions and authentication.
 5)Goals of HDFS
    -Fault detection and recovery : Since HDFS includes a large number of commodity hardware, failure of components is frequent. Therefore HDFS should have mechanisms for quick and automatic fault detection and recovery.

   -Huge datasets : HDFS should have hundreds of nodes per cluster to manage the applications having huge datasets.

   -Hardware at data : A requested task can be done efficiently, when the computation takes place near the data. Especially where huge datasets are involved, it reduces the network traffic and increases the throughput.
   
   
 b)Hadoop Cluster
 Ans:
 1)A Hadoop cluster is a special type of computational cluster designed specifically for storing and analyzing huge amounts of unstructured data in a distributed computing environment.
 2)Such clusters run Hadoop's open source distributed processing software on low-cost commodity computers.
 3)Typically one machine in the cluster is designated as the NameNode and another machine the as JobTracker; these are the masters. 
 4)The rest of the machines in the cluster act as both DataNode and TaskTracker; these are the slaves.
 5)Hadoop clusters are often referred to as "shared nothing" systems because the only thing that is shared between nodes is the network that connects them.
 6)Hadoop clusters are known for boosting the speed of data analysis applications.
 7)They also are highly scalable: If a cluster's processing power is overwhelmed by growing volumes of data, additional cluster nodes can be added to increase throughput.
 8)Hadoop clusters also are highly resistant to failure because each piece of data is copied onto other cluster nodes, which ensures that the data is not lost if one node fails.
9)Benefits of Hadoop Cluster
  -scalability
  -cost effective
  -suitable for analyzing big data


c)HDFS Blocks
Ans:
1)Hadoop distributed file system also stores the data in terms of blocks.
2)However the block size in HDFS is very large. The default size of HDFS block is 64MB. The files are split into 64MB blocks and then stored into the hadoop filesystem. The hadoop application is responsible for distributing the data blocks across multiple nodes. 
3)Advantages of HDFS Block
  -The blocks are of fixed size, so it is very easy to calculate the number of blocks that can be stored on a disk.
  -HDFS block concept simplifies the storage of the datanodes. The datanodes doesn’t need to concern about the blocks metadata data like file permissions etc. The namenode maintains the metadata of all the blocks.
  -If the size of the file is less than the HDFS block size, then the file does not occupy the complete block storage.
  -As the file is chunked into blocks, it is easy to store a file that is larger than the disk size as the data blocks are distributed and stored on multiple nodes in a hadoop cluster.
  -locks are easy to replicate between the datanodes and thus provide fault tolerance and high availability. Hadoop framework replicates each block across multiple nodes (default replication factor is 3). In case of any node failure or block corruption, the same block can be read from another node.
 
   
