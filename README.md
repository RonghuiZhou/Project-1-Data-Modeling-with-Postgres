## Project 1: Data Modeling with Postgres
Udacity Data Engineer     
Here's a [guide](https://www.markdownguide.org/basic-syntax/) on Markdown Syntax.

### Introduction
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to. Currently, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app. 

### Project Description
In this project, we created a Postgres database with tables designed to optimize queries on song play analysis. We also created a star database schema and write an ETL pipeline that transfers data from files in two local directories into these tables in Postgres using Python and SQL.

### Database schema design and ETL pipeline
We implemented the Star Schema for this project, with one fact table (songplays) and four dimension tables (songs, artists, users and time).

### Files
In addition to the data files, the project workspace includes six files:

* 1. test.ipynb displays the first few rows of each table to let you check your database. 
* 2. create_tables.py drops and creates your tables. You run this file to reset your tables before each time you run your ETL scripts.
* 3. etl.ipynb reads and processes a single file from song_data and log_data and loads the data into your tables. This notebook contains detailed instructions on the ETL process for each of the tables.
* 4. etl.py reads and processes files from song_data and log_data and loads them into your tables. You can fill this out based on your work in the ETL notebook.
* 5. sql_queries.py contains all your sql queries, and is imported into the last three files above.
* 6. README.md provides discussion on your project.


### Song Dataset
The first dataset is a subset of real data from the [Million Song Dataset](http://millionsongdataset.com/). Each file is in JSON format and contains metadata about a song and the artist of that song. The files are partitioned by the first three letters of each song's track ID.  

And below is an example of what a single song file, TRAABJL12903CDCF1A.json, looks like.

    {"num_songs": 1, "artist_id": "ARJIE2Y1187B994AB7", "artist_latitude": null, "artist_longitude": null, "artist_location": "", "artist_name": "Line Renaud", "song_id": "SOUPIRU12A6D4FA1E1", "title": "Der Kleine Dompfaff", "duration": 152.92036, "year": 0}

### Log Dataset
The second dataset consists of log files in JSON format generated by this [event simulator](https://github.com/Interana/eventsim) based on the songs in the dataset above. These simulate activity logs from a music streaming app based on specified configurations.


