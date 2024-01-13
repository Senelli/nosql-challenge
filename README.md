# nosql-challenge

## Part 1: Database and Jupyter Notebook Set Up
- Used the NoSQL_setup_starter.ipynb for this section of the challenge
- Imported the data provided in the establishments.json file from the Terminal. Named the database uk_food and the collection establishments. Used the statement below.
    - mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json
- Imported the librarie: PyMongo and Pretty Print (pprint).
- Created an instance of the Mongo Client.
- Confirmed that the database was created properly and the data was loaded properly:
    - Listed the databases that are existing in MongoDB. Confirmed that uk_food is listed.
    - Listed the collection(s) in the database to ensure that establishments is there.
    - Found and displayed one document in the establishments collection using find_one and displayed with pprint.
    - Assigned the establishments collection to a variable to prepare the collection for use.

## Part 2: Update the Database
- Used NoSQL_setup_starter.ipynb for this section of the challenge.
- Added a new record to the database
- Found the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields.
- Updated the new restaurant with the BusinessTypeID for "Restaurant/Cafe/Canteen".
- Checked how many documents contain the Dover Local Authority
- Removed any establishments within the Dover Local Authority from the database and checked the number of documents to ensure they were deleted.
- Some of the number values are stored as strings, when they should be stored as numbers.
    - converted the fields latitude and longitude to type decimal
    - converted the field RatingValue to type integer

## Part 3: Exploratory Analysis
- Usde NoSQL_analysis_starter.ipynb for this section of the challenge.
- Answered the following questions:
    - Which establishments have a hygiene score equal to 20?
    - Which establishments in London have a RatingValue greater than or equal to 4?
    - What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
    - How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.
- For each question:
    - Used the count_documents to display the number of documents contained in the result
    - Displayed the first document in the results using pprint
    - Converted the result to a Pandas DataFrame
    - Printed the number of rows in the DataFrame
    - Displayed the first 10 rows of the DataFrame