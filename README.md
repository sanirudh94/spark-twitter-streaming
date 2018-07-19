# spark-twitter-streaming
This project is about revealing trends and patterns across demographics from live Twitter data stream. Also filter through spam messages to get relevant trending information.

# Motivation 
* Subscribe to live twitter stream
* Transform twitter stream to 
  * Extract most relevant fields from huge Tweet Blob
  * Detect possible Spam Messages
* Index the data to make them searchable
* Create analytical and interavtive dashboards to reveal trends

# Built With
  * Apache Spark
  * Elasticsearch
  * Kibana
  * twitter4j Api
  * sbt-An interactive build tool
  
# Overall Workflow

* Connect to the Twitter streaming API  using OAuth to continuosly ingest new tweets
*  Created a SparkStreamingContext[Dstreams] with batch interval of 10 seconds
* Extracted important fields and produced JSON with processed fields for each incoming tweet
* Passed each tweet through a spam detector and flag spam messages
* Converted JSON into Map and send it to an Elasticsearch Cluster with relevant mappings
* Analyical results from data in Elasticsearch are visualized with Kibana dashboards

![alt text](https://wlbhiro.files.wordpress.com/2015/01/realtime_batch_architecture.png)

# Results 
<p align="center">
  <img src="/Users/deepikasharma/Downloads/image1.png" width="350" title="hover text"/>
  
</p>
