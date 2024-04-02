# Executive Summary

On average, over a hundred anime seasons are produced each year and for anime enthusiasts and weebs, finding the series they would like is a difficult and time-consuming task. Out of the many anime seasons produced, only a few make it to the status of mainstream anime. The rest are overshadowed by the popularity of mainstream anime and often become known only to a few anime-watching communities. As more and more people pick up the hobby of watching anime, the more mainstream anime gains more fame and following. This results in these less-known yet brilliant anime series being lost and forgotten.

In this report, we want to create an anime recommender system that can generate personalized recommendations that users will like despite the large number and variety of anime series that exist. We created recommendation systems using (1) user-based collaborative filtering, (2) item-based collaborative filtering, (3) Slope One-based Collaborative Filtering, (4) Co-clustering-based Collaborative Filtering and three latent factor-based collaborative filtering methods namely (5a) SVD, (5b) NMF, and (5c) SVD++. Once the recommender systems are created, we evaluate each of them using several metrics, namely (1) error scores (RMSE, MSE), (2) coverage scores, (3) novelty scores, (4) personalization scores, (5) intra-list similarity score, and (6) runtime.

Our results suggest that each recommender system has its own set of advantages and disadvantages. SVD and SVD++ have the lowest prediction errors and highest intra-list similarity, but has the lowest coverage, personalization, and novelty. Moreover, SVD++ has a notably high runtime with more than five times the runtime of item based collaborative filtering which is the second highest in terms of runtime. Slope-one has the highest coverage, and high novelty and personalization. Co-clustering has the highest novelty and personalization, and the lowest runtime. NMF performs well in personalization, but is only mediocre in terms of coverage and novelty and has the highest prediction errors. User and item based collaborative filtering performed will in terms of novelty and personalization, with average prediction errors. Ultimately, the choice of a recommender system to be used depends on which evaluation metric the user deems to be important. To improve this report further, we can try out other algorithms like content-based collaborative filtering and batch recommender systems. We can also explore several other algorithms in the scikit-Surprise library to improve the performance of our recommender system.

# Problem Statement

As the library of Anime titles from different platforms grows, how do we create a recommender system that can suggest relatively unknown titles that are highly similar to the viewing history of a specific user and the recommendations being personalized to each viewer?

# Motivation

The history of Anime can be traced back to the birth of Japan’s film industry in the early 1900s and has emerged as one of Japan’s major cultural breakthroughs over the past century.[1] Known originally for in-depth and imaginative story-telling, Anime has evolved to where it is now by integrating animation technology advancements into the said art. This evolution led to an increase in the audience not only in Japan but even penetrated the global mainstream media. But even with the influence of different cultures, authors of anime title has stayed true to their beliefs and ensured that their visions and art style are the ones driving their products. And as the popularity of anime increased over time, there also has been an influx of authors who wanted the world to view their life's works resulting in a great number of titles being published. 

An increase in selection, however, is not always a positive thing. The high number of choices results in viewers spending hours, even days, scrolling through hundreds of anime never finding the content they like. To create a better streaming environment that boosts revenue and increases the time spent on the website, businesses need to provide tailor-fit suggestions based on a user’s needs. It can take a lot of time and effort to search for the right anime to watch. This is why a recommender system for anime titles is important as it will save users ample time by providing them with a personalized recommendation based on their needs. On the business side, a recommender system will help increase engagement, retention, and time spent on the platform, resulting in increased revenue and profitability. Businesses also want to keep the churn rate to a minimum to ensure longevity in the platform. With personalized recommendations, the platform will increase the likelihood of users staying and watching more anime, and at the same time attract more ad revenue and subscription revenue.
