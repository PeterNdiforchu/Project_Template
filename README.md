# Project_Template

# Spotify Data Analytics

<img width="1296" alt="Screenshot 2024-02-23 at 4 26 27 AM" src="https://github.com/PeterNdiforchu/Project_Template/assets/76578061/2f763b8b-2f79-4fb0-a490-d6cd4ae5572c">

## Project Description
At the core of this project is the process of extracting data from Spotify on user listening history, performing data transformations, and loading the data to a database for user song play analytics. The program uses Spotipy, a lightweight Python library for the Spotify Web API. The primary objectives of this project are to:
- Build a data pipeline for Spotify music streams for the year 2022.
- Analyze music streams to create Spotify Wrapped-style insights and compare them with the official 2022 Wrapped.
- Analyze the top 5 moods of 2022 based on music streams and use the data to predict 2023 mood.
- Develop proficiency in data pipeline building and machine learning with Python.

## Data Extraction
Data is extracted from Spotify using the Spotify Web API's endpoint to get the 50 most recently played tracks. The result is a Python dictionary, which is then used to create multiple dataframes after some data cleanup.

## Technologies Used
- Programming Languages: Python, SQL
- Libraries: Pandas
- Tools: Airflow, AWS

## Data Preprocessing
Python and Pandas are used to transform the extracted data. Transformations include removing duplicate albums and artists and creating a unique identifier column (UNIX_Time_Stamp) to ensure data integrity. Data is structured using both dictionaries and lists, with detailed steps in the `spotify_etl.py` Jupyter notebook.

## Data Loading
Data is loaded into a local Postgres database. The database schema is created using SQL Data Definition Language (DDL). Three main tables are defined for the ETL process. Data is loaded into a temporary table using the Pandas `.to_sql` method before inserting it into the final database. This ensures that tracks are unique.
<img width="1296" alt="Screenshot 2024-02-23 at 4 26 27 AM" src="https://github.com/PeterNdiforchu/Project_Template/assets/157251680/51cd3a8f-95f9-4044-80ed-4cceb39db46a">

## Analysis and Insights
Machine learning is applied to perform a sensitivity analysis and identify moods based on song plays at different points in time. Top 5 moods identified were inspirational, happy, exuberant, energetic and contentment.

## How to Use the Project
- Follow instructions to install Postgres on your local machine.
- Use SQL queries to create the schema for the Spotify database.
- Find SQL queries for creating the necessary tables in the project.
- Use Python scripts to extract, transform, and load data.
- Detailed instructions and code can be found in the project files.

## Project Structure
- `spotify_etl.py`: Jupyter notebook with data extraction and transformation steps.
- `sql_queries.sql`: SQL queries for database schema and table creation.
- `README.md`: You're here!

## Contributing
If you're interested in collaborating on this project, please feel free to reach out and discuss potential contributions.

## License
This project is open source under the [TBD] license. You can use and modify the code as needed.

## Contact Information
You can reach out to [Your Contact Information] for questions, collaboration, or more information about this project.

