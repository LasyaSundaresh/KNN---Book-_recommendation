# KNN---Book-_recommendation



📚 Book Recommender System
Overview

This project implements a Book Recommender System using item-based collaborative filtering with K-Nearest Neighbors (KNN).
It recommends books based on user ratings and calculates similarity scores.

The system is tested to ensure accurate recommendations and is ready for notebook demos and GitHub showcase.

Features

Recommends books similar to a given book using cosine similarity.

Displays book titles and similarity scores.

Filters out users and books with very few ratings to improve recommendation quality.

Works with large datasets using sparse matrices for efficiency.

Unit-tested for correctness.

Dataset

The project uses two CSV files:

Books.csv

Columns: ISBN, Book-Title, Book-Author, Year-Of-Publication, Publisher

Contains book details.

Ratings.csv

Columns: User-ID, ISBN, Book-Rating

Contains ratings from users for books.

⚠️ Ensure both CSV files are in the same folder as the notebook/script.

Technology Stack

Python 3

Pandas – data manipulation

NumPy – numerical operations

scikit-learn – KNN model for collaborative filtering

Jupyter Notebook – interactive demonstration

How It Works

Data Preprocessing

Remove users with <200 ratings and books with <100 ratings.

Merge ratings with book information.

Create a pivot table: Book-Title x User-ID matrix.

KNN Model

Fit NearestNeighbors with cosine distance on the pivot matrix.

Calculate similarity as 1 - cosine_distance.

Recommendations

Input a book title.

Return top N similar books with similarity scores.
