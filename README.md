# Movies-ETL

##Amazing Prime would like to refactor the code to create a function that performs the ETL process to put three data files together and upload into PostgreSQL database

###Result

-movies table displays 6051 rows 
[movies_table](https://github.com/Yunaka1269/Movies-ETL/blob/main/Resources/movies_query.PNG)

-ratings table displays 26,024,289 rows 
[ratings_table](https://github.com/Yunaka1269/Movies-ETL/blob/main/Resources/ratings_query.PNG)

####Resources

-Data Source

	-movies_metadata.csv
	
	-ratings.csv
	
	-wikipedia-movies.json


-Software

	-postgresql 12.4.1
	
	-pgAdmin version 4.24

	-Jupyter Notebook 6.1.4
  
###Summary

Upon iterate through and filtering the data, I removed one row that's ['video'] == 'True' and this creates a dicrepancy of one row between my movies table counts and Module8 Challenge screenshot. Remember that ratings table needs to be dropped from Postgre before running the refactored code because the code importing the data won't start if table already exists. Also, if 'append' for 'if_exists' parameter is changed to 'replace', the code keeps overriding every 1,000,000 rows and it will show only 24,289 rows instead of 26,024,289 rows. Otherwise, the refactored code can be used for every newly added title.
