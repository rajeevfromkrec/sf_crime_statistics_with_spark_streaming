
### Intro
In this project, you will be provided with a real-world dataset, extracted from Kaggle, on San Francisco crime incidents, and you will provide statistical analyses of the data using Apache Spark Structured Streaming. You will apply skills and knowledge to create a Kafka server to produce data, and ingest data through Spark Structured Streaming.

### How to use the application
In order to run the application , you will need to run following

#### Zookeeper:
/usr/bin/zookeeper-server-start config/zookeeper.properties

#### Kafka server:
/usr/bin/kafka-server-start config/server.properties

#### Insert data into topic:
python kafka_server.py

#### Kafka consumer console to see data in console:
kafka-console-consumer --topic "topic-name" --from-beginning --bootstrap-server localhost:9092

#### Kafka consumer program:
python consumer_server.py

#### Run Spark job:
spark-submit --packages org.apache.spark:spark-sql-kafka-0-10_2.11:2.3.4 --master local[*] data_stream.py

### screenshot of kafka console consumer output
![kafka_consumer_console](https://github.com/rajeevfromkrec/sf_crime_statistics_with_spark_streaming/blob/main/kafka_consumer_console.PNG?raw=true)
  
Progress
Progress

Streaming UI Output
Streaming UI Output

### Questions
### 1. How did changing values on the SparkSession property parameters affect the throughput and latency of the data?
You can view the values numInputRows, inputRowsPerSecond, and processedRowsPerSecond. Changing the values of the below key / value pairs showed a difference in how much data was being processed.

### 2. What were the 2-3 most efficient SparkSession property key/value pairs? Through testing multiple variations on values, how can you tell these were the most optimal?
maxRatePerPartition
spark.default.parallelism
You can tell there was an optimal gain / loss by going off the above values in the first question.
