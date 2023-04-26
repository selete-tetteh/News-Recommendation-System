# News-Recommendation-System
This is a Python-based news recommendation system that utilizes natural language processing techniques such as TF-IDF vectorization and KMeans clustering to group news articles based on their text similarity. By analyzing the content of the articles, the system is able to recommend similar news articles to users.

# Installation
To run the code, you will need to have Python 3.x installed on your system along with the following libraries:

pandas
scikit-learn
scipy
matplotlib
nltk

# Usage
Clone the repository to your local machine.
Navigate to the directory containing the code.
Run the following command to execute the code:
python news_recommendation_system.py
The system will recommend similar articles for a given article ID.

# How it works
The system follows the following steps:

Loads news data from a CSV file containing columns such as 'date', 'title', 'text', and 'link'.
Performs text preprocessing on the 'text' column of the news data, including making all text lowercase, removing stopwords, removing punctuation marks, and removing HTML tags.
Drops duplicate rows from the news data based on the cleaned text.
Adds an 'id' column to the news data for identification.
Preprocesses the data by applying TF-IDF vectorization using TfidfVectorizer from scikit-learn, which converts text data into numerical representations.
Performs KMeans clustering on the TF-IDF matrix to group similar articles into clusters.
Defines a function to recommend similar articles for a given article ID by calculating cosine similarity between the TF-IDF vectors of the articles.
The recommended similar articles are printed with their titles, links, and similarity scores based on cosine similarity.
