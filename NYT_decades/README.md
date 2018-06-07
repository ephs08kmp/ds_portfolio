
# New York Times over the Decades

The world has changed over the past decades. Has what we read about in the media changed? This project will utilize data from the [New York Times (NYT) archives API](https://developer.nytimes.com/archive_api.json).  From these archives, the NYT provides the lead paragraph from the article, along with other information about the article.  Using these lead paragraphs, I used the natural language processing techniques of Term Frequency Inverse Document Frequency Vectorization to turn paragraphs into vectors by determining the frequent and infrequent words and how frequently the words were used. I also used spaCy to determine the number of various parts of speech that were used in the paragraphs.  Using the best 5% of the features, I used various clustering methods to group the sentences based on similarity.  Finally, I used these features to predict the decade from which a sentence of a New York Times article was written.  

This modeling be useful for authors to determine the patterns of writing over time, especially the changes, or lack thereof, in topics and ways to help people better understand the world. 

You can see the natural language processing, clustering, and modeling in the `New_York_Times_Decades.ipynb` notebook above.  

### Installation
Get an API key by registering with the [New York Times API](https://developer.nytimes.com/signup).

Clone this repo to your computer.

Get into the folder using cd NYT_decades.

### Usage
Run all cells in the `New_York_Times_Decades.ipynb` file using a jupyter notebook.

### Extending this
If you want to extend this work, here are a few places to start:

- Change search parameters in GET requests.
- Switch to categorizing article by author.
- Use a different NYT API search for article trends by different traits.
