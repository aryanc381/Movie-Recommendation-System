# Movie Recommendation System 
![Python](https://img.shields.io/badge/Python-3.12.4-blueviolet)
![API](https://img.shields.io/badge/API-TMDB-fcba03)



In this project, I have made a content-based movie recommendation system that recommends movies to the user based on the movies that they currently like via search toggle bar.

## Types of Recommendation System 
1. **Content-based** - Based on the user tags, here tags are interests for example : genre, country, etc.
2. **Collaborative** - Based on the similarity of the user, content is suggested from one user to another user. For example, I am liking stephen curry's basketball match and you also follow stephen curry, then that video will also be shown (recommended) to you.
3. **Hybrid** - Content based + Collaborative (for example : I like to see basketball clips, that will be shown to me only + my friend and I watch piano videos, he liked a hindi piano cover then that will also be shown to me).

Mostly huge MNCs use ```hybrid``` recommendation systems but I have seen startups using ```content-based``` and ```collaborative``` systems as they are cheap OR easy to make.
(In this project, I'll be making a content-based recommendation system as it makes sense - similar content is most likely to be watched by the consumer)

## Project Architecture
The project is divided mainly into 3 parts -
1. ```Frontend``` - The frontend is made using Streamlit API to make the frontend of the webapp that consists of the heading and the search bar.
2. ```Backend``` - The backend of the webapp is running on a heroku server (You can use Apache to use your local machine as the server or streamlit subscription to deploy the webapp).
3. ```ML System``` - I used python and ML tools from scikitlearn which I will talk about in depth shortly in the later part of this document.

## Dataset
Find the entire dataset here (9MB) : [TMDB 5000 Movie MetaData](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)

## Importance of a recommender system
Let me explain you the importance of a recommender system in the real world.
I want you to think that you own a shoe retail store in Koregaon park, India. There's a lot of competition in Koregaon park for shoe vendors as there are a lot of them and a lot of them are well reputed. You want your store to be a one stop destination. Imagine I come to your store and my shoe size is UK12 and I ask you for basketball shoes. You show me 5 pairs of shoes and you see that I like the red precision 6 shoes very much but I already have them is what I say. What would you do as the owner of that shop. You would show me more types of ```UK12``` shoes that are ```red``` in colour, becuse I showed interest in red shoes. This is what a recommender system does on big websites like amazon, netflix, etc because customer acquisition is very important. Also these recommender systems are very important to the company because the attention span of consumers is reducing when it comes to online shopping, so showing the most right product at the right time is very important for sales. Well in the example above, red and UK12 are the tags. The ML Algorithm uses these tags to identify similar products and create a confidence rate. The product with the highest confidence rate is shown. 
In this project, the tags are movie director, actor, movie name, genre, type, etc that help the ML Algorithm to understand the similarities between the movies.

## The project
### ML Algorithm 
1. **Data Extraction** - I used pandas library for data extraction and seaborn to visualise it where I realised majority of the movies are english.
2. **Feature Selection** - genre, id, keywords, title, overview, cast, crew.
3. **Data Preprocessing** - The entire data was preprocessed into title and tags where tags = overview + genres + keywords + cast + crew.
4. **Vectorization** - Conversion of texts into words (text-vectorization)
