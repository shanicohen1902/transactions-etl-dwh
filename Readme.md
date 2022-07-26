## Features
This is a basic ETL pipeline for populating transactions data into a data warehouse, implemented in Jupyter Notebook.
1. transactions-etl.ipynb:
    Using this simple pipeline, the data warehouse is populated from the transaction file. Contains stages for extraction, transfer, and loading
1. transactions-task-tables: simple queries to view the tables 
1. transactions-task-reports: a data warehouse usage example

 __In the model folder, you will find a Star schema design with two different fact tables and dimensions for the data warehouse__

## Tech
- Python3 (pandas, Jupyter notebook)
- Postgres

## Requirenments
- Docker / Postgres installation
- Python3
- pip package manager

## Setup
1. Python dependencies
All python dependencies can be install from requirenments.txt
    ```sh
    pip install -r requirements.txt
    ```

1. Postgres install. 
Postgres can be used from a container. for example - 
    ```sh
    docker pull postgres
    docker run --name postgresql -e POSTGRES_USER=myusername -e POSTGRES_PASSWORD=mypassword -p 5432:5432 -v /data:/var/lib/postgresql/data -d postgres
    ```
1. From the project root, open jupyter notebook - 
    ```sh
    jupyter notebook
    ```

1. Update connection string url from - 

    ```
    connection = sqlalchemy.create_engine(f'postgresql+psycopg2://myusername@0.0.0.0:5432/postgres')
    ```

    to your connection string 
1. Start with transactions-etl.ipynb file that create the data

I think that's it!
