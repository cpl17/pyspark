This project contains the following:

* A short script that utilizes __tweepy__ and __twitter dev api__ to locally serve tweets
* The tweets are filtered according to a provided keyword
* Concurrently, a spark app is hosted on the same port and ingests the tweets every 10 seconds
* Then, __mapreduce__ is performed on the RDDs to find the hashtag frequencies, which are stored in a temporary table
* The top 10 hashtags are queried using __SparkSQL__
* Finally, a dynamic barplot of the frequenices is created
