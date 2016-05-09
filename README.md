# E63_Lambda_Architecture-
Sample code for E63_LA_Project. 
4.	 Compile the code and run the package  for each layer .
# E63_Lambda_Architecture- Sample code for E63_LA_Project. 

             mvn clean package
Compile the code and run the package.

Batch Layer ,   Speed Layer and     Serving  Components .
        mvn clean package
		
common module used in both layer - ErrorCount		
Batch Layer - file BatchErrorCount.scala 
Speed Layer  - file StreamErrorCount.scala
Serving  layer  -Query  using impala 

Usage : 

•	Real-time processing using spark stream : Open Terminal window and run the code.
 
    Code read the stream  at T sec, using spark  RDD method, and write to HDFS.
  Code read the stream  at T(10) sec, using spark  RDD method, and write to HDFS.

java -cp SparkStreamingLambda-1.0-SNAPSHOT.jar  sparklambda.streaming.StreamingErrorCount localhost

To send/recv  data to the streaming example, use: nc -lk , 

nc -lk 9999     # to listen to port 9999 on local host 

# send file to host port  nc localhost 9999 < textData.txt   

Batch Processing Using Spark SQL : Open the terminal window  and run the code 
 To query Historical data set .

Java -cp SparkStreamingLambda-1.0-SNAPSHOT.jar sparklambda.streaming.StreamingErrorCount localhost 9999

java -cp SparkStreamingLambda-1.0-SNAPSHOT.jar sparklambda.etl.BatchErrorCount


Done 