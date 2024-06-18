### Movie Recommendation System Report

**** Introduction:

This report discusses the implementation of a movie recommendation system using collaborative filtering techniques. The system is based on user ratings of movies to 
suggest similar movies that a user might like.

**** Data Sources:

1. **Recommend.csv**: This dataset contains user ratings for various movies.
2. **Movie_Id_Titles.csv**: This dataset provides the titles corresponding to movie IDs used in the ratings dataset.

**** Steps and Analysis:

1. **Data Loading and Exploration:**
   - Loaded the `Recommend.csv` dataset containing columns: `user_id`, `item_id` (movie ID), `rating`, and `timestamp`.
   - Loaded the `Movie_Id_Titles.csv` dataset to get the movie titles based on `item_id`.
   - Merged these datasets on `item_id` to form a unified dataset `data` with movie titles included.

2. **Data Exploration:**
   - Explored basic statistics and characteristics of the dataset:
     - Checked dimensions using `df.shape`.
     - Examined number of unique users and movies using `df.nunique()`.

3. **Data Analysis:**
   - Calculated average ratings and number of ratings per movie:
     - Grouped by movie title and computed mean rating and count of ratings.
     - Created a DataFrame `rating` to store this information.

4. **Visualization:**
   - Visualized distribution of number of ratings using a histogram.
   - Visualized distribution of average ratings using a histogram.

5. **Recommendation Calculation:**
   - Constructed a pivot table `moviemat` where rows represent `user_id`, columns represent movie titles, and values represent ratings.
   - Calculated correlations between target movies (e.g., "Star Wars (1977)", "Liar Liar (1997)") and all other movies based on user ratings.

6. **Recommendation Results:**
   - Identified movies highly correlated with the target movies based on user ratings.
   - Filtered and sorted results based on movies with a significant number of ratings (e.g., >400 ratings).

**** Example Recommendations:

- **For "Star Wars (1977)":**
  - Identified movies highly correlated such as "Return of the Jedi (1983)", "Empire Strikes Back, The (1980)".
- **For "Liar Liar (1997)":**
  - Identified movies highly correlated such as "Batman Forever (1995)", "Mask, The (1994)".
- **For "Contact (1997)":**
  - Identified movies highly correlated such as "Starship Troopers (1997)", "Event Horizon (1997)".

**** Conclusion:

This movie recommendation system leverages collaborative filtering to provide personalized movie suggestions based on user ratings. By calculating correlations between 
movies, it identifies similar movies that users might enjoy. Further enhancements could include integrating more sophisticated algorithms, handling larger datasets, and 
incorporating user feedback for real-time recommendations.

This system demonstrates the power of data-driven approaches in enhancing user experience and engagement in movie recommendation platforms.

