This is a Python ETL pipeline, that extracts user and songs activity data to create star schema using postgres.

## Datasets
1. song dataset - json data that contains artist and song information
2. log dataset - jsons data that contains user activity

## Star schema created by pipeline
### Fact table
  * songplays - records in log data associated with song plays

### Dimension tables
  * users - users associated with songs being played
  * songs - songs that are being played by users
  * aritsts - artist of the songs that are being played
  * time - time when songs are played
  

# Running the pipeline
> to run we need python3 and postgres

> you must create the star schema tables before running the pipeline

> to create the tables run:
 ```
 python3 create_tables.py
 ```
 >>> this will drop tables if they exist and create new emplty tables

> once star schema tables are created you can run the pipeline

> to run the pipeline run:
```
python3 etl.py
```
 >>> this will extract the data from the json files and insert it in the star schema.
 
  


  
