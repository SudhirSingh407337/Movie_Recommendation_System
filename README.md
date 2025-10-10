# Movie Recommendation System

## Overview
This project implements a movie recommendation system using collaborative filtering techniques. It provides personalized movie recommendations based on user preferences and ratings. The system is built using Python and leverages libraries such as pandas, NumPy, scikit-learn, and matplotlib for data processing, machine learning, and visualization.

## Features
- **Collaborative Filtering Models**:
  - User-based Collaborative Filtering
  - Matrix Factorization using Singular Value Decomposition (SVD)
- **Evaluation Metrics**:
  - Mean Squared Error (MSE)
  - Root Mean Squared Error (RMSE)
  - Mean Absolute Error (MAE)
- **Interactive Recommendations**:
  - Generate personalized movie recommendations for any user.
  - Display user-specific ratings and top recommendations.
- **Data Visualization**:
  - Distribution of ratings
  - Ratings per user
  - Model performance comparison (RMSE and MAE)

## Dataset
The system uses the following datasets:
- `movies.csv`: Contains movie information (e.g., movie ID, title, genres).
- `ratings.csv`: Contains user ratings for movies (e.g., user ID, movie ID, rating, timestamp).

## Installation
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd Movie-Recommendation-System
   ```
2. Install the required Python libraries:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
1. Open the Jupyter Notebook:
   ```bash
   jupyter notebook movie_recommendation_system.ipynb
   ```
2. Run the cells sequentially to:
   - Load and preprocess the data.
   - Train the recommendation models.
   - Evaluate model performance.
   - Generate and display recommendations.

## How It Works
1. **Data Preprocessing**:
   - Filters users and movies with sufficient ratings to reduce sparsity.
   - Creates a user-movie rating matrix for collaborative filtering.
2. **Model Training**:
   - User-based CF computes user similarity using cosine similarity.
   - SVD decomposes the rating matrix into latent factors for users and movies.
3. **Evaluation**:
   - Models are evaluated on a test set using MSE, RMSE, and MAE.
   - Results are visualized to compare model performance.
4. **Interactive Recommendations**:
   - Users can input their user ID and select a model to get personalized recommendations.

## Example Output
### Model Performance Comparison:
| Model           | MSE   | RMSE  | MAE   |
|-----------------|-------|-------|-------|
| User-based CF   | 6.537 | 2.557 | 2.330 |
| SVD             | 2.783 | 1.668 | 1.358 |

### Top Recommendations for User 3 using SVD:
1. **Movie Title 1**
   - Movie ID: 123 | Predicted Rating: 4.75
   - Genres: Action|Adventure
2. **Movie Title 2**
   - Movie ID: 456 | Predicted Rating: 4.60
   - Genres: Comedy|Drama

## Dependencies
- Python 3.7+
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn

## Future Enhancements
- Add genre-based filtering for hybrid recommendations.
- Implement item-based collaborative filtering.
- Optimize hyperparameters for better model performance.
- Integrate a web interface for easier user interaction.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgments
- [MovieLens Dataset](https://grouplens.org/datasets/movielens/) for providing the data.
- Python community for the amazing libraries used in this project.
