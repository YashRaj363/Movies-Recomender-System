A scalable Content-Based Movie Recommender System built using Machine Learning and deployed with Streamlit.

The system recommends the Top 5 similar movies based on textual metadata using cosine similarity.

🚀 Live Demo

🔗 https://movies-recomender-system.streamlit.app/

Try selecting a movie and get instant recommendations with posters.

📌 Problem Statement

Users often struggle to find movies similar to ones they already like.
This project builds a recommendation engine that suggests movies based on similarity of features like genres, cast, crew, and keywords.

🧠 How It Works
1️⃣ Feature Engineering

Combined genres, keywords, cast, and crew

Created a unified text representation (tags)

2️⃣ Text Vectorization

Used CountVectorizer

Converted text into high-dimensional sparse vectors

3️⃣ Similarity Computation

Applied cosine_similarity

Computed similarity dynamically

Stored vectors in compressed sparse .npz format for optimization

4️⃣ Recommendation Pipeline

User selects a movie

System finds similarity scores

Sorts and returns top 5 similar movies

Fetches posters using TMDB API

🏗️ Architecture

User Input
→ Feature Vector
→ Cosine Similarity
→ Ranking
→ Top 5 Movies
→ Poster Fetch via API

🛠️ Tech Stack

Python

Pandas

Scikit-learn

SciPy

Streamlit

TMDB API

⚡ Performance Optimization

Avoided storing full similarity matrix (O(n²) space complexity)

Used sparse matrix storage (vectors.npz)

Reduced storage from 176MB → 295KB

Implemented caching for faster performance

📂 Project Structure
movie_recommendation/
│
├── app.py
├── movies.pkl
├── vectors.npz
├── requirements.txt
└── README.md
🧪 Run Locally

Clone the repository:

git clone https://github.com/YashRaj363/Movies-Recomender-System.git
cd Movies-Recomender-System

Install dependencies:

pip install -r requirements.txt

Run the app:

streamlit run app.py
🎯 Key ML Concepts Used

Content-Based Filtering

Cosine Similarity

Text Vectorization

Sparse Matrix Optimization

Feature Engineering

Ranking Algorithm

👨‍💻 Author

Yash Raj
Machine Learning Enthusiast
