# Haircare Product Analysis
What brands and products are best for which hair types?

Check out the recommender [here](https://morganoneka.github.io/haircare/products.html)!


## Reddit Data
Part 1 of this project was to look at brands based on Reddit comments. Textured-hair subreddits (r/wavyhair, r/curlyhair, and r/naturalhair) often share product suggestions. While product names are hard to standardize, brands are more straightforward to search for. The following scripts identify trends between common brands and different hair stats.
1. `Reddit Post Lists.ipynb` uses PushShift to gather list of links to posts for our subreddits.
2. `Reddit  Comments.ipynb` uses the Reddit API wrapper PRAW to retrieve comments from each post in our list.
3. `Reddit Data Cleaning.ipynb` teases out information about hair statistics and product information.
4. `Reddit Data Exploration.ipynb` visualizes trends in the data and does some basic statistical analysis.

## Amazon Data
Part 2 of this project was to look at specific products, and use user rankings to create a recommendation system. Right now, this system works by ranking each product based on different keywords. For each keyword, we look at the ratio of positive (4-5 stars) comments containing that keyword vs. the ratio of negative (1-2 stars) comments containing that keyword. Products are then recommended which have a high positive comment ratio for all the user's keywords. These keywords include common "hair stats" used in the textured hair community, like porosity and density, as well as other common hair needs, like frizz and volume.
1. `Amazon Product Scraping.ipynb` scrapes products from product pages identified in `productpages.xlsx`.
2. `Amazon Brand Exploration.ipynb` provides some basic visualizations for an individual brand — showing review distributions, comparing reviews across keywords, and word clouds for positive and negative reviews.
3. `Amazon Brand Comparison.ipynb` compares ratings across brands and keywords.
4. `Amazon Prediction.ipynb` prepares keyword scores, as described above, for the web-based visualization.

## Terminology
Hair that is not straight is considered textured. There are three types of textured hair: wavy, curly, and coily (also known as type 2, 3, and 4).

But hair also differs beyond just what we can see at first glance. *Density* refers to how many hairs are on a person's head; *thickness* is how thick each individual strand of hair is; and *porosity* is how "open" the hair shaft is, i.e. how easily it lets in water and products. These three "hair stats" influence how a person's hair responds to different haircare products.
