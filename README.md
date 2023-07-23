# Module-12-NoSQL-Challenge
Setup:

By using the import command `mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json`, I was able to properly import the establishments.json file into the uk_food database using MongoDB. From here, the correct dependencies were imported, a mongo instance created, and the correct database name and collection were assigned. Now, I was able to insert a new document into the collection and update its BusinessTypeID using the .update_one() and .find() methods, as well as delete all those documents with the field LocalAuthorityName, update fields latitude and longitude values to decimal type using .updateMany(), and update field RatingValue to integer type (again using .updateMany()).

Analysis:

For the analysis part, I was able to find all those establishments with a hygiene score of 20 and convert the results into a pandas DataFrame. Using the $regex operator, I was also able to filter results to those establishments with a RatingValue greater than or equal to 4 (using the $gte operator) in London and convert them into a DataFrame. I was also able to filter establishments down to 0.01 degree of the latitude and longitude of the document I inserted in the setup notebook (Penang Flavours), sort them by hygiene score, and then converted the results to a DataFrame. Then, by using a pipeline with match, group, and sort parameters, I was able to query the number of establishments in each LocalAuthorityName with a hygiene score of 0 and place the results into a DataFrame.

My fellow student, Ethan, graciously helped me with my latitude and longitude query!