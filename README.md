readme.md
SF Crime Statistics with Spark Streaming
Intro
In this project, you will be provided with a real-world dataset, extracted from Kaggle, on San Francisco crime incidents, and you will provide statistical analyses of the data using Apache Spark Structured Streaming. You will draw on the skills and knowledge you've learned in this course to create a Kafka server to produce data, and ingest data through Spark Structured Streaming.


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
