# Movie Review and Event Similarity Analysis
## Overview
This repository contains the code and dataset used in the master's thesis: "Audience Engagement Through Movie Events: A Semantic Similarity Approach". The research analyzes how different types of events in films engage audiences by comparing IMDb user reviews to annotated event descriptions.

## Repository Contents
### 1. `Scrape.ipynb`
This Jupyter notebook contains the code for scraping IMDb user reviews for the selected movies. It uses the Selenium library to automate web browsing and collect user reviews from IMDb. The reviews are saved into a dataset for further cleaning and analysis. Can be found [here]([`Scrape.ipynb`](https://github.com/arisef77/Movie-Review-Event-Similarity/blob/main/Scrape.ipynb))

### 2. `Analysis events with reviews.ipynb`
This Jupyter notebook includes the process of cleaning and analyzing the scraped reviews and calculating the semantic similarity between user reviews and the event descriptions using the SpaCy library. The notebook explains how to split both reviews and events into sentences, calculate similarity scores, and filter pairs with significant semantic similarity. Can be found [here](https://github.com/arisef77/Movie-Review-Event-Similarity/blob/main/Analysis%20events%20with%20reviews.ipynb)

### 3. Datasets
The following CSV files are provided in the repository:

- ***IMDb Reviews*** (filename: [`imdb_reviews.csv`](https://github.com/arisef77/Movie-Review-Event-Similarity/blob/main/imdb_reviews.csv)): This dataset contains the raw user reviews scraped from IMDb for the selected movies. It includes the following columns:

    -  `Movie`: The movie title.
    -  `Review`: The user-written review for the movie.
<br>    

- ***IMDb Reviews Cleaned*** (filename: [`imdb_reviews_cleaned.csv`](https://github.com/arisef77/Movie-Review-Event-Similarity/blob/main/imdb_reviews.csv)): This dataset contains the cleaned user reviews after removing duplicates and irrelevant content. It is used in the semantic similarity analysis with event descriptions. The cleaning process ensures only unique and complete reviews are included.

- ***Event Types*** (filename: [`dataset_event_types.csv`](https://github.com/arisef77/Movie-Review-Event-Similarity/blob/main/dataset_event_types.csv)): This dataset includes the annotated events for the selected movies, categorized into four event types: Non-event, Process, Stative Event, and Change of State. Each event is linked to a specific movie and is used to compare with the IMDb user reviews. The columns in this file are:

    -  `Movie`: The movie title.
    -  `Event`: A description of the event.
    -  `Event Type`: The type of event (e.g., Process, Change of State).
These datasets are used in the analysis to match user reviews with annotated events and calculate semantic similarity.

## Prerequisites
Ensure you have the following installed:

- Python 3.x
- Jupyter Notebook
- SpaCy
- Pandas
- Selenium (for web scraping)
- Chrome WebDriver (or any other browser driver required for Selenium)

## License

The code in this project is licensed under the MIT License - see the [LICENSE](https://github.com/arisef77/Movie-Review-Event-Similarity/blob/main/LICENCE.md) file for details.
The user reviews scraped from IMDb are subject to IMDb's [Conditions of Use](https://www.imdb.com/conditions).
