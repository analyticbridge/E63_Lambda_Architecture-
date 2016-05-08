# E63_Lambda_Architecture-
Sample code for E63_LA_Project. 
4.	 Compile the code and run the package  for each layer .

             mvn clean package

Batch Layer ,   Speed Layer and     Serving  Components .

Usage : 

•	Real-time processing using spark stream : Open Terminal window and run the code.
 
    Code read the stream  at T sec, using spark  RDD method, and write to HDFS.

java -cp SparkStreamingLambda-1.0-SNAPSHOT.jar  sparklambda.streaming.StreamingErrorCount localhost

To send/recv  data to the streaming example, use: nc -lk , 

nc -lk 9999     # to listen to port 9999 on local host 
# send file to host port  nc localhost 9999 < textData.txt   

Batch Processing Using Spark SQL : Open the terminal window  and run the code 
 To query Historical data set .

java -cp SparkStreamingLambda-1.0-SNAPSHOT.jar sparklambda.etl.BatchErrorCount

Done 