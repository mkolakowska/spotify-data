# spotify-data

### Introduction
In this project, we will build an ETL (Extract, Transform, Load) pipeline using the Spotify API on AWS. The pipeline will retrieve data from from the Spotify API, transform it to a desire format, and load it into an AWS data store.

### Architecture
![Architecture Diagram](https://github.com/mkolakowska/spotify-data/blob/main/spotify_architecture.png)

### About Dataset/API
This API contains information about music artist, albums and songs - [Spotify API](https://developer.spotify.com/documentation/web-api)

### Services Used
1. **S3 (Simple Storage Service)**
2. **Lambda**
3. **CloudWatch**
4. **Glue Crawler**
5. **AWS Glue (Data Catalog)**
6. **Athena**

### Install Packages
```
pip install pandas
pip install numpy
pip install spotipy
```

### Project Execution Flow
Extract Data from API -> Lambda Trigger (every 1 hour) -> Run Extract Code -> Store Raw Data -> Trigger Transform Function -> Transform Data and Load It -> Query Using Athena
