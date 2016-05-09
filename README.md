E63_Lambda_Architecture-Sample code for E63_LA_Project. 

1. Compile the code and run the package  for each layer . 

             mvn clean package
		
1.common module used in both layer - ErrorCount		
2. Batch Layer - file BatchErrorCount.scala 
3. Speed Layer  - file StreamErrorCount.scala
4. Serving  layer  -Query  using impala 

Usage : 

To send/recv  data to the streaming example, use: nc -lk , 

nc -lk 9999     # to listen to port 9999 on local host 

send file to host port  nc localhost 9999 < textData.txt   


•	Real-time processing using spark stream : Open Terminal window and run the code.
 
    Code read the stream  at T sec, using spark  RDD method, and write to HDFS.
  Code read the stream  at T(10) sec, using spark  RDD method, and write to HDFS.

java -cp SparkStreamingLambda-1.0-SNAPSHOT.jar  sparklambda.streaming.StreamingErrorCount localhost 9999


Batch Processing Using Spark SQL : Open the terminal window  and run the code 
 To query Historical data set .


java -cp SparkStreamingLambda-1.0-SNAPSHOT.jar sparklambda.etl.BatchErrorCount


Done 