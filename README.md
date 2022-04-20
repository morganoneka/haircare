# Haircare Product Analysis
What brands are best for which hair types?

## TL;DR
For now, I only have conclusive evidence for variations based on subreddit.

Brands preferred by wavies: Trader Joe's
Brands preverred by coilies: Cantu


## How to run
1. `GetPostLists.ipynb` uses PushShift to gather list of links to posts for our subreddits.
2. `GetPostComments.ipynb` uses the Reddit API wrapper PRAW to retrieve comments from each post in our list.
3. `DataCleaning.ipynb` teases out information about hair statistics and product information.
4. `DataExploration.ipynb` visualizes trends in the data and does some basic statistical analysis.

## Terminology
Hair that is not straight is considered textured. There are three types of textured hair: wavy, curly, and coily (also known as type 2, 3, and 4).

