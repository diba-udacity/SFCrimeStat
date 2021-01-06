# SFCrimeStat
Project for Udacity Data Streaming Course

Screenshots for the different steps are in the respective folder.

Answers to the questions in Step 3:



## How did changing values on the SparkSession property parameters affect the throughput and latency of the data?

## What were the 2-3 most efficient SparkSession property key/value pairs? Through testing multiple variations on values, how can you tell these were the most optimal?

One can try to play with the following properties:
- spark.sql.shuffle.partitions
- ark.default.parallelism

I ended with the following
- When setting spark.sql.shuffle.partitions to 2 vs. 10, showed that the processedRowsPerSecond was better for 2.
- When setting spark.default.parallelism to 100 vs. 10,000, showed that the processedRowsPerSecond was better for 100.
