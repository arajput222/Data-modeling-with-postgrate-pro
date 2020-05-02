# Data-modeling-with-postgrate-pro
This is Data Modeling with postgrate project.

Sparkify is a music streaming app.This Udacity Data Engineering nanodegree project creates a postgres database sparkifydb for a music app, Sparkify.The analytics team is particularly interested in understanding what songs users are listening to.Currently, their data resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app. However, this cannot provid an easy way to query the data.

# Python scripts

  * reate_tables.py: Clean previous schema and creates tables.
  * sql_queries.py: All queries used in the ETL pipeline.
  * etl.py: Read JSON logs and JSON metadata and load the data into generated tables.
  
# Schema design and ETL pipeline

The star schema has 1 fact table (songplays), and 4 dimension tables (users, songs, artists, time). DROP, CREATE, INSERT, and SELECT queries are defined in sql_queries.py. create_tables.py uses functions 

   SELECT COUNT(hour) FROM time;, hour of the day music most often listened to.

   SELECT COUNT(hour) FROM time;base, drop_tables, and create_tables to create the database sparkifydb and the required tables.

Extract, transform, load processes in etl.py populate the songs and artists tables with data derived from the JSON song files, data/song_data. Processed data derived from the JSON log files, data/log_data, is used to populate time and users tables. A SELECT query collects song and artist id from the songs and artists tables and combines this with log file derived data to populate the songplays fact table.

# Song play example queries

Day of the week music most frequently listened to.

  SELECT COUNT(weekday) FROM time;

Or, hour of the day music most often listened to.

   SELECT COUNT(hour) FROM time;
   
Or, Simple queries might include number of users with each membership level.

    SELECT COUNT(level) FROM users;
    
    
