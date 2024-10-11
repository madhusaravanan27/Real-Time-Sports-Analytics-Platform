Real Time Sports Analytic Platform

Project Overview:

The Real Time Sports Analytic Platform is a distributed data pipeline designed to process a live lacrosse game stream, update player and team statistics, and generate live box scores for web developers. The project integrates various technologies, including PySpark, MongoDB, Microsoft SQL Server (MSSQL), and Minio (S3-compatible storage), to simulate a real-world sports analytics system. The project is part of a technical assessment for a data engineering role, adapted for an academic course.

Technologies Used:

PySpark: For distributed data processing and transformations
MongoDB: NoSQL database for storing real-time box scores
Microsoft SQL Server (MSSQL): For team and player reference data
Minio: S3-compatible object storage for live game stream data
Apache Drill: Distributed SQL query engine for querying databases
Jupyter Lab: Used for developing and running PySpark code

Key Accomplishments:

1. Real-Time Data Stream Processing:
Developed a pipeline that ingests a live game stream from an S3 bucket (Minio) containing shot events and goals during a lacrosse game.
Processed the game stream using PySpark to track player shots, goals, and team scores as the game progresses.

3. Box Score Generation:
Generated a live box score in real-time, transforming game events into a JSON format suitable for web display.
The box score is updated periodically during the game and stored in MongoDB for quick access by web developers.
Each box score includes the current player and team statistics, such as shots taken, goals scored, and winning/losing status.  

4. Player and Team Statistics Update:
   
After the game is completed, the pipeline updates the team win/loss records and player statistics in a new set of tables (players2 and teams2) in MSSQL to reflect the final game results.
Implemented the logic to calculate cumulative shots and goals for each player and team using PySpark, ensuring the database reflects the game outcome.

5. Database Integration and Querying:
   
Utilized Apache Drill to query the distributed datasets, integrating MSSQL, MongoDB, and Minio to retrieve and update data as required by the application.
Wrote SQL queries in Apache Drill to extract and display team and player data, as well as the live game stream for analytics and reporting.

6. End-to-End Data Pipeline:
   
Combined the various components into a cohesive PySpark script that automates the entire process: ingesting the game stream, updating statistics, generating live box scores, and updating final stats when the game is over.
Ensured the pipeline runs multiple times during the game, allowing web developers to access up-to-date statistics as the game progresses.
