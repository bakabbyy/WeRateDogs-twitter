# Analyzing WeRateDogs Tweets

---

## Introduction

The Twitter account [WeRateDogs]( https://twitter.com/dog_rates ) took the world by storm with the popular meme "they're good dogs Brent" back in 2016. Today with over 8 million followers worldwide, the account is known for the adorable dogs they feature as well as they're unique rating system of how good of boys and girls they are. I mean, how could you not love it with faces like these:

<img src="C:\Users\Main User\Documents\WeRateDogs-twitter-project\dog-rates-social.jpg" style="zoom:50%;" />

So they may not be the greatest at math, but people don't seem to mind. Honestly I don't either, I mean they're such good dogs. But after tweeting over 10K photos of the most adorable floofers, I wonder if these ratings have some legs after all. And being that we live in a world of measurement  and tracking, I'm curious if there are any connections that can be found between the dogs featured and the response by the Twitter audience. Heck it'd be cool if there were data collected from a neural network that I could somehow use, I mean that's such a hot buzz word right now. I know what you're thinking, "Alex, but that's two words." Well you're right, that is two words. And I just so happen to have that data and will be analyzing that so let's do it.

## The Goodest Dogs

So let's dive right in. After cleaning the data, I was able to derive the tweet and image prediction information for a little over 2,000 tweets. That's a lot of dogs and a lot of ratings. Let's look at how those ratings fell.

![](C:\Users\Main User\Documents\WeRateDogs-twitter-project\distro_ratings.png)

That is a lot of good boys and girls! But let's not go too overboard, this histogram actual shows us that the ratings weren't too drastically high for all dogs. The average dog rating across all tweets was about 12.3. Here's how that shook out by classifcation.

![](C:\Users\Main User\Documents\WeRateDogs-twitter-project\dog_stage_rating.png)

Looks like those little puppers need just a bit more training, as they have the lowest average rating according to WeRateDogs. Maybe once they're potty trained and level up to a puppo they'll jump up to having the highest average rating of all of the dog stages.

## What's in a Name

Through cleaning the dataset, a lot of the names were removed due to incorrect parsing of the tweet texts as well as null values. Of the populated dog names, here are the top 15 most common.

![](C:\Users\Main User\Documents\WeRateDogs-twitter-project\popular_dog_names.png)

I've definitely heard some of these names before for dogs. Except Koda, never heard that one. I'm stealing it. And I may steal the dog too, as this Koda has the highest retweet count of the name (6,822 retweets) and was correctly predicted as a Samoyed at a 96% confidence level.

<img src="C:\Users\Main User\Documents\WeRateDogs-twitter-project\koda.jpg" style="zoom: 33%;" />

## You're my Favorite

These dogs are definitely exceptional with these high ratings, especially my new dog Koda. I wonder how the internet feels about these dogs? I'm glad you asked.

<img src="C:\Users\Main User\Documents\WeRateDogs-twitter-project\avg_eng.png"  />

It looks like the WeRateDogs Twitter account did really take off after 2016. So much so that the average favorite count per tweet grew 357% from July 2016 to July 2017, averaging almost 30,000 favorites per tweet in July 2017. It looks like the world agrees, these are very good dogs.

## Hm, Accurate

You didn't think I forgot about the neural network stuff did you? Well I didn't, here we go.

The top three image predictions were selected based on each tweet image. To find the breed that was most accurately predicted based on it's photo, I separated each trial into it's own DataFrame, cleaned the breed names, and renamed the columns to a consistent naming convention to concatenate them together. Here is the result of the tweet image predictions.

![](C:\Users\Main User\Documents\WeRateDogs-twitter-project\avg_conf.png)

The Bernese mountain dog came out on top as being accurately predicted with the highest average confidence level of ~77%. These dogs are accurately predicted almost almost 30% more times than the second most accurate, the pembroke. Here's a bernese mountain dog named Venti that has the second highest favorite count of the breed at almost 27,000.

<img src="C:\Users\Main User\Documents\WeRateDogs-twitter-project\bernese.jpg" style="zoom:33%;" />

Good boy.