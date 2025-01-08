Recipe Recommendation System

This project aims to build a recipe recommendation system based on user preferences, available ingredients, and specific constraints such as cooking time and difficulty level. The system uses collaborative filtering techniques to suggest personalized recipes, factoring in users' past ratings and other data. 

Download data from https://www.kaggle.com/datasets/shuyangli94/food-com-recipes-and-user-interactions

1. Data Preprocessing
The system starts by preprocessing two primary datasets:
user_ratings_data, and recipes_data
by:
User-Recipe Interaction Matrix
Handling Missing Values, and
Feature Engineering

2. 
- Fill missing values with 0 - indicating no interaction
- Convert the matrix to a sparse format to save memory
- Fit the NearestNeighbors model using the sparse matrix

3. Recommendation Algorithm
- Ensure the provided user_idx is valid in the sparse user-recipe matrix
- Use the trained KNN model to find the nearest neighbors of the user
- Exclude the first index
- Find the recipes that have interacted 
- Return recommended recipes

4. Visualization
Add visualizations to provide into cooking time distributions. That visualizations help users understand their cooking time and the recipe dataset better.


(Challenges Faced for Large Data Processing)
One of the major challenges was handling large datasets, especially when building the user-recipe interaction matrix. The initial dataset was huge, and this caused memory allocation errors (e.g., MemoryError). To address this:
- I converted large matrices into sparse matrix representations, significantly reducing memory usage.
- In some cases, we had to downsample the dataset by focusing on active users and frequently rated recipes to make the problem more tractable.

(Ideas for Improvement)
- Implementing advanced matrix factorization techniques (like SVD or ALS) to handle sparse data more effectively. This would reduce the reliance on manually filling in missing ratings.
- Encouraging users to rate more recipes by providing incentives or making the rating process simpler could help generate more comprehensive data.
