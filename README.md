# Ford Go Bike Data Exploration
## by Michael Owusu Agyebeng


## Dataset

> As part of Udacity’s Data Science course, I had to wrangle and analyze WeRateDogs posts on twitter. This involved gathering data by downloading a csv file form [kaggle](https://www.kaggle.com/code/msytnadeem/weratedogs-tweet-data-wrangling), downloading a file from URL, and gathering data from the Twitter API. I was required to request for permission from twitter to grant me developer status and permission to gather data from their platform.

## Assessing the data
>After gathering the data, I found 12 issues which included ten (10) quality issues and two (2) tidiness issues. I cleaned then and merged them together to form one dataset which I stored and named “twitter_archive_master.csv”.
### Quality Issues
1. tweet_id must be a string not an integer
2. retweeted_status_id is not a float but a string
3. retweeted_status_user_id is not a float but a string
4. timestamp is a date not a string
5. in_reply_to_status_id is not a float but a string
6. in_reply_to_user_id is also not a float but a string
7. replies could also mean duplicates so we will have to drop them
8. retweets in df data hence there are duplicates so we have to drop retweeted_status_id, retweeted_status_user_id and retweeted_status_timestamp
9. dog names in the img_df data were in different cases
10. some dogs names are "a", "None", "the", etc
### Tidiness Issues
1. html tags in source column of df data
2. doggo, floofer, pupper and puppo columns need to be merged

> After which I cleaned them


## Summary of Findings

* Golden Reteiver was the most common breed oof dog found in the data with over 130 mentions 
* Oliver, Charlie, and Cooper were the most common dog names giving a tie of 10 counts each.
* MMost dog tweets were posted in December and may be because of the festive season and holidays hence most people spent time at home with their dogs. The month of August had the least number of posts.
* Monday recorded the most tweets with over 300 dog tweets signifying it is the day most of the tweets were posted.
*here is also a very strong positive relationship between retweet count and favorite count of the WeRateDogs data. This signifies an association between retweets and favorites. Hence the more retweets a post gets, the more favorites it gets.
* Almost all of our data was gotten from iPhone users with them giving a 98.1% of our data.
* When retweet and favorite count was put viewed over time, it was recognized that favorite counts were always more than retweets but as time went by, while retweet count increased approximately linear, favorite count seemed to grow approximately exponentially. Which indicates that as at November 2015 there were fewer engagements (a sum of less than 5000 favorites and retweets) on WeRateDogs posts, but it had popularity over time and racked up more than 30000 favorites alone in July 2017.
* Putting the average retweet and favorite count side by side, it is evident that favorite counts were averagely more than retweet counts and doublestage had the most favorites while pupper had the least favorite count
