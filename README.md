# E63_Lambda_Architecture- Sample code for E63_LA_Project. 

Compile the code and run the package.

        mvn clean package
		
common module used in both layer - ErrorCount		
Batch Layer - file BatchErrorCount.scala 
Speed Layer  - file StreamErrorCount.scala
Serving  layer  -Query  using impala 

Usage : 

•	Real-time processing using spark stream : Open Terminal window and run the code.
 
  Code read the stream  at T(10) sec, using spark  RDD method, and write to HDFS.

java -cp SparkStreamingLambda-1.0-SNAPSHOT.jar  sparklambda.streaming.StreamingErrorCount localhost

To send/recv  data to the streaming example, use: nc -lk , 

nc -lk 9999     # to listen to port 9999 on local host 

# send file to host port  nc localhost 9999 < textData.txt   

Batch Processing Using Spark SQL : Open the terminal window  and run the code 

Java -cp SparkStreamingLambda-1.0-SNAPSHOT.jar sparklambda.streaming.StreamingErrorCount localhost 9999

java -cp SparkStreamingLambda-1.0-SNAPSHOT.jar sparklambda.etl.BatchErrorCount


Done 