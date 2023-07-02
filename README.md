# NoSQL Challenge
This repository contains the code and data for analyzing food hygiene ratings data collected by the UK Food Standards Agency. The analysis is conducted to assist the food magazine, Eat Safe, Love, in providing valuable insights to their journalists and food critics for selecting establishments to focus on in their future articles. The analysis is divided into three parts: Database and Jupyter Notebook Setup, Update the Database, and Exploratory Analysis.

## Part 1: Database and Jupyter Notebook Set Up
In this section, we set up the MongoDB database and Jupyter Notebook environment for the analysis.

### Requirements
Python 3.x      
MongoDB installed and running      
Jupyter Notebook

### Instructions
Clone the repository to your local machine.      
Navigate to the repository folder and open the NoSQL_setup_starter.ipynb Jupyter Notebook.      
Import Data and Set Up MongoDB      
Import the data provided in the establishments.json file into a MongoDB database named uk_food and a collection named establishments. Record the commands used for this operation in a markdown cell in the notebook.       
Import the required libraries: PyMongo and pprint.       
Create an instance of the Mongo Client to connect to the database.       
Confirm the successful import of data by listing the databases in MongoDB and checking that uk_food is listed. Also, verify that the establishments collection is present and display one document from the collection using find_one and pprint.       
Assign the establishments collection to a variable to prepare it for use in the analysis.

## Part 2: Update the Database
In this section, we perform requested modifications to the establishments collection before conducting any queries or analysis for the magazine.

### Instructions
Open the NoSQL_setup_starter.ipynb Jupyter Notebook if not already open.       
Update Database      
Locate the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields.      
Update the information for the exciting new halal restaurant in Greenwich, adding the found BusinessTypeID to the restaurant's document.      
Check how many documents contain the Dover Local Authority and remove all establishments within the Dover Local Authority from the database. Verify the successful deletion of these documents.        
Correct the data types for certain fields:       
Use update_many to convert latitude and longitude to decimal numbers.         
Use update_many to convert RatingValue to integer numbers.


## Part 3: Exploratory Analysis
In this section, we perform exploratory analysis on the food hygiene ratings data to answer specific questions posed by Eat Safe, Love magazine.

### Instructions
Open the NoSQL_analysis_starter.ipynb Jupyter Notebook.      
Exploratory Analysis      
Answer the following questions using appropriate queries and analysis:       

a. Which establishments have a hygiene score equal to 20?        
b. Which establishments in London have a RatingValue greater than or equal to 4? (Use $regex for the search)        
c. What are the top 5 establishments with a RatingValue of '5', sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"? (Search within 0.01 degree on either side of the latitude and longitude)             
d. How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest and print out the top ten local authority areas.

