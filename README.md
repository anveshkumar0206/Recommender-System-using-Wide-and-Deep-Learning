# Anie Recommender-System-using-Wide-and-Deep-Learning

This project implements a Wide & Deep Learning-based recommendation system for anime content, inspired by the architecture presented in the research paper: Wide & Deep Learning for Recommender Systems. The system combines the benefits of memorization (wide models) and generalization (deep models) to generate more accurate anime recommendations for users.

Dataset
The dataset is sourced from Kaggle: https://www.kaggle.com/datasets/dbdmobile/myanimelist-dataset 
MyAnimeList Dataset (2023)

Files used:
anime-dataset-2023.csv: Metadata about anime such as genre, studio, type, and episodes.
users-details-2023.csv: User demographics and activity-related information.
users-score-2023.csv: Ratings users gave to different anime (used as ground truth).

Model Architecture
The model follows the Wide & Deep architecture:
Wide Component: Handles sparse features like user-anime interaction pairs and cross-product transformations.
Deep Component: Learns dense embeddings for user and anime features such as genres, type, source, studio, and user statistics. 

This component includes:
Embedding layers for categorical features.
Dense hidden layers with ReLU activations.
Dropout for regularization.
The final output is a predicted score representing the user's affinity for a particular anime.

Features Used
User Features: total watched, total plan-to-watch, mean score given, etc.
Anime Features: genre, source, type, mean rating, number of episodes, studio.
Crossed Features: user_id x anime_id pair (for the wide component).

Evaluation
Data Split: 80% training, 20% testing.
Metric: Mean Squared Error (MSE) for prediction accuracy.
Goal: Predict the rating a user would give to an unseen anime.


Results
Wide & Deep model outperformed both standalone wide and deep baselines in our experiments.
Captures both explicit interactions and learned latent preferences.

Installation
Clone the repository:
bash
Copy
Edit
git clone https://github.com/anveshkumar0206/Recommender-System-using-Wide-and-Deep-Learning.git
cd Recommender-System-using-Wide-and-Deep-Learning
Install dependencies:
pip install -r requirements.txt
Run the notebook or script to train the model.
