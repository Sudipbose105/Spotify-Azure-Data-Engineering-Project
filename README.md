# Spotify-Azure-Data-Engineering-Project

This is an end-to-end data engineering project using Azure cloud stack.

Here I have used Medalian arthitecture to process the data in three layers - Bronze->Silver->Gold

Azure Data Factory is used to ingest the data from source to destination. Incremental data loading and backfilling of data features are implemented in the ADF pipeline.

Azure SQL DB is used as a source and ADLS Gen2 is used as destination in the ADF pipeline.

I have also implemented Azure logic apps and used it in the pipeline for sending mail alerts in case of pipeline failure.

Here is the pipeline design as below:

<img width="1292" height="465" alt="image" src="https://github.com/user-attachments/assets/b871349e-8564-4046-ac8b-881b1b363122" />

<img width="1293" height="558" alt="image" src="https://github.com/user-attachments/assets/31489560-1d90-4af5-ae9f-4fd10c807916" />

<img width="1330" height="439" alt="image" src="https://github.com/user-attachments/assets/2d7b3f37-ae2d-4415-8e1a-6cad5f5d6574" />

<img width="1334" height="491" alt="image" src="https://github.com/user-attachments/assets/7a275fee-18a5-4af0-91be-9a71f8c5e226" />

<img width="1902" height="723" alt="image" src="https://github.com/user-attachments/assets/181fa682-cda1-4641-ba05-23ff498246bc" />


Used databricks autoloader to incrementally load and process the new files from bronze to silver layer.

Created metadata driven notebook to generate SQL query dynamically based on user inputs. Used JINJA templating engine to achieve the same.

Finally, created a DLT lakeflow pipeline to load the data from silver to gold layer. Implemented slowly changing dimension type 2 feature in the DLT pipeline using auto_cdc_flow.

Here is the DLT pipeline design as below:

<img width="1571" height="647" alt="image" src="https://github.com/user-attachments/assets/a6cd315c-10a9-4e6a-bdee-bac900f04020" />

Used databricks assest bundles to deploy the code to different environments smoothly.













