# ETL Data Modeling: *Sparkify* Streaming Music

This project builds an ETL (*extract transform load*) pipeline to perform big data operations for a fictitious streaming music app, Sparkify. 
This ETL pipeline uses a NoSQL keyspace in Apache Cassandra for OLAP (Online Analytical Processing).
For a similar project using a PostgreSQL relational database, please see [my other repository](https://github.com/markplotlib/modeling-postgresql).

This ETL pipeline employs a **star schema** for the NoSQL keyspace. 
This star schema has a log table of `songplays` as its **fact table** at the star center. 
Data stored in .csv files illustrate song play data from 30 event log files, spanning the month of November 2018. 
This data is artificially produced using [eventsim](https://github.com/Interana/eventsim).

The **dimension tables**, situated at the star's peripheries, are tables named for `users`, `songs`, `artists`, and `time` (timestamps). 
This real musical data comes from the [Million Song Dataset](http://millionsongdataset.com/).

# Execution Instructions

This is a stand-alone notebook file, *cassandra-etl-pipeline.ipynb*, containing all the code.

# Repository Files

This notebook file calls upon the data files in the directory `event_data`

## Data Preview

A sample of the data columns below shows info about songs, artists, and music listener accounts.
Apache Cassandra's structure supports analytical queries to drive business decisions about the *Sparkify* streaming music platform.

![image info](./images/image_event_datafile_new.png)
