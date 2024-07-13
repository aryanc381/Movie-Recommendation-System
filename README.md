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

## Projet Work-Flow
The project is divided mainly into 3 parts -
1. ```Frontend``` - The frontend is made using Streamlit API to make the frontend of the webapp that consists of the heading and the search bar.
2. ```Backend``` - The backend of the webapp is running on a heroku server (You can use Apache to use your local machine as the server or streamlit subscription to deploy the webapp).
3. ```ML System``` - I used python and ML tools from scikitlearn which I will talk about in depth later.

## Dataset
Find the entire dataset here (9MB) : [TMDB 5000 Movie MetaData](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)

