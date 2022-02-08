# Movies-ETL

## Overview
The purpose of this analysis was to create an automated pipeline that takes in new data, performs appropriate transformations, and then loads data into existing tables.  This was accomplished by performing an Extract Transform Load (ETL).  This was done by creating a function that reads in three seperate files, extracting and transforming data, and creating a database.  Pandas was used to read in the json and csv files while pgAdmin and SQLalchemy were used for database management.  The final product was an automated pipline that takes in movie data, transforms it, and adds it to our existing database with the final results presented in ETL_create_database.ipynb.

# Results
Functions were created that would clean the data read in.  
![image](https://user-images.githubusercontent.com/88444529/153024061-93f443e7-8161-4b56-a412-6b89853aaa31.png)
An ETL function was then created that took in the three different files and transformation were performed including using regex to change the box office data, cleaning the release date data, and dropping columns that were not needed among other things.  The cleaned files were added to our database using SQLalchemy and were able to append additional information to the tables by adding the "if exists" to the code.  
![image](https://user-images.githubusercontent.com/88444529/153025286-38703ac0-93f4-4b65-8783-8bf0eada8ede.png)
The results of adding the files to tables in pgAdmin are preseneted in the following images.
![image](https://user-images.githubusercontent.com/88444529/153025479-f22e8667-71de-42ec-a515-62112882a816.png)
![image](https://user-images.githubusercontent.com/88444529/153025536-8a66265d-9c2c-4960-a687-1bdacb68c79b.png)

## Conclusion
A pipeline was created successfully that took in csv and json files and cleand them, added them to a database, and allowed the database to be updated with new information.  In the future code could be refactored to make things more clean.
