#RecommendationRecipes

This project is a recipe recommendation system that combines collaborative filtering with content-based filtering. The goal is to recommend recipes to users based on their previous interactions (ratings) and additional constraints like available ingredients and maximum cooking time. 

Get the data from https://www.kaggle.com/datasets/shuyangli94/food-com-recipes-and-user-interactions

1. Data Loading
•	Recipes Data (recipes_df): This dataset contains recipe information, including recipe IDs, names, ingredients, cooking time, and tags.
•	User Ratings Data (user_ratings_cleaned): This dataset contains user interactions (ratings) with specific recipes. Each row indicates a user, a recipe, and the corresponding rating given by the user.

2. Collaborative Filtering
Collaborative filtering is used to recommend recipes based on the preferences of similar users.
•	Data Preparation
•	Matrix Creation
•	Nearest Neighbors Model

3. Content-Based Filtering
This approach filters recipes based on user-defined constraints like available ingredients and cooking time.
•	Ingredient Filtering 
•	Time Filtering 

4. Combining Collaborative and Content-Based Filtering/Final Recommendation Function()
The final recommendation system combines both collaborative and content-based filtering.
•	It first filters the recipes by available ingredients and cooking time.
•	Recommends recipes to a user by finding similar users (based on KNN) and suggesting the recipes that the similar users have rated positively. It returns a list of recommended recipe IDs.
•	Finally, it returns a list of recipes that meet both the collaborative filtering and content-based filtering criteria.

5. Example Output
The system prints the number of recipes filtered by ingredients, the number of recipes filtered by cooking time, and the recommended recipe IDs for a specific user. The final output contains the recipes that meet all the specified criteria.

6. Visualization
Add visualizations to provide into cooking time distributions. That visualizations help users understand their cooking time and the recipe dataset better.

Key Concepts
•	Collaborative Filtering: Recommending recipes by finding similar users based on their ratings and suggesting recipes that those similar users liked.
•	Content-Based Filtering: Filtering recipes based on user-specified criteria like available ingredients and cooking time.
•	Hybrid Approach: This project combines collaborative filtering and content-based filtering to provide personalized recommendations that also meet the user's specific constraints.
