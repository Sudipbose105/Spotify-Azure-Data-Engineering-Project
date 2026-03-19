# Spotify-Azure-Data-Engineering-Project

This is an end-to-end data engineering project using Azure cloud stack.

Here I have used Medalian arthitecture to process the data in three layers - Bronze->Silver->Gold

Azure Data Factory is used to ingest the data from source to destination. Incremental data loading and backfilling of data features are implemented in the ADF pipeline.

Azure SQL DB is used as a source and ADLS Gen2 is used as destination in the ADF pipeline.

I have also implemented Azure logic apps and used it in the pipeline for sending mail alerts in case of pipeline failure.

Here is the pipeline design as below:

<img width="1292" height="465" alt="image" src="https://github.com/user-attachments/assets/b871349e-8564-4046-ac8b-881b1b363122" />

