# E63_Lambda_Architecture-
Sample code for E63_LA_Project. 
4.	 Compile the code and run the package  for each layer .

             mvn clean package

Batch Layer ,   Speed Layer and     Serving  Components  .

Usage : 

•	Real-time processing using spark stream : Open Terminal window and run the code.
 
    Code read the stream  at T sec, using spark  RDD method, and write to HDFS.

java -cp SparkStreamingLambda-1.0-SNAPSHOT.jar:/usr/jars/spark-assembly-1.6.0-cdh5.7.0-hadoop2.6.0-cdh5.7.0.jar sparklambda.streaming.StreamingErrorCount localhost
To send data to the streaming example, use: nc -lk
	Batch Processing Using Spark SQL : Open the terminal window  and run the code 
         To query Historical data set .

java -cp SparkStreamingLambda-1.0-SNAPSHOT.jar:/lib/spark-assembly-1.0.2-hadoop2.2.0.jar sparklambda.etl.BatchErrorCount

Done 