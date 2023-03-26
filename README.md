# Eat Safe, Love

The `NoSQL_setup.ipynb` sets up and updates the database. The `NoSQL_analysis.ipynb` queries relevant information for analyses and converts results into Pandas DataFrame. The data provided in the `establishments.json` file was imported using Terminal with `mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json`. 

### Set Up and Update Database
* Insert the new halal restaurant opened in Greenwich to the Database.

* Update the new restauarant with the correct BusineesTypeID.
    
* Drop all establishments that has Dover as their Local Authority from the database. 

* Convert latitude and longitude to decimal numbers.

    
### Exploratory Analysis
1. Which establishments have a hygiene score equal to 20?
   
   There are 41 documents with a hygiene score of 20
   
2. Which establishments in London have a RatingValue greater than or equal to 4?

   There are 34 documents with Authority London and RatingValue greater than or equal to 4

3. What are the top 5 establishments with a RatingValue rating value of '5', sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?

   The top 5 establishments with a RatingValue of '5' sorted by lowest hygiene score nearest to "Penang Flavours" are: "Volunteer", "Plumstead Manor Nursery", "Atlantic Fish Bar", "Iceland", and "Howe and Co Fish and Chips - Van 17". 
   
4. How many establishments in each Local Authority area have a hygiene score of 0?
   
   There are 55 rows in the DataFrame. This is the preview of the first 10 rows:
    | _id | count |
    |-----|-------|
    |Thanet|1130|
    |Greenwich|882|
    |Maidstone|713|
    |Newham|711|
    |Swale|686|
    |Chelmsford|680|
    |Medway|672|
    |Bexley|607|
    |Southend-On-Sea|586|
    |Tendring|542|
