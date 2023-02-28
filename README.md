# Movie Recommendation System

![Python](https://img.shields.io/badge/Python-3.8-blueviolet)
![API](https://img.shields.io/badge/API-TMDB-fcba03)

A content-based recommender system that recommends movies similar to the movie the user likes and analyses the sentiments of the reviews given by the user.

## Overview

The movies are recommended based on the content of the movie you entered or selected. The main parameters that are considered for the recommendations are the genre, director, and top 3 casts. The details of the movies, such as title, genre, runtime, rating, poster, casts, etc., are fetched from [TMDB](https://www.themoviedb.org/documentation/api). The reviews of each individual movie given by the users are "web-scraped" from the IMDB website with the help of `beautifulsoup4`, and the reviews are subjected to sentiment analysis, where the model predicts whether the review is positive or negative.

## How to get the API key?

Create an account in https://www.themoviedb.org/. Once you successfully created an account, click on the `API` link from the left hand sidebar in your account settings and fill all the details to apply for an API key. If you are asked for the website URL, just give "NA" if you don't have one. You will see the API key in your `API` sidebar once your request has been approved.

## Similarity Score : 

   **How does it decide which item is most similar to the item user likes(or selects in our case)?** Here comes the similarity scores.
   
   It is a numerical value ranges between zero to one which helps to determine how much two items are similar to each other on a scale of zero to one. This similarity score is obtained measuring the similarity between the text details of both of the items. So, similarity score is the measure of similarity between given text details of two items. This can be done by cosine-similarity.
   
## How Cosine Similarity works?
  Cosine similarity is a metric used to measure how similar the documents are irrespective of their size. Mathematically, it measures the cosine of the angle between two vectors projected in a multi-dimensional space. The cosine similarity is advantageous because even if the two similar documents are far apart by the Euclidean distance (due to the size of the document), chances are they may still be oriented closer together. The smaller the angle, higher the cosine similarity.
  
  ![image](https://user-images.githubusercontent.com/36665975/70401457-a7530680-1a55-11ea-9158-97d4e8515ca4.png)

### Sources of the datasets 

[IMDB 5000 Movie Dataset](https://www.kaggle.com/carolzhangdc/imdb-5000-movie-dataset)

