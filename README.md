# Deliverable 3: Amazon Reviews

## Intro / Overview

The purpose of this module is to analyze Amazon reviews written by members of the Amazon Vine programme. This is a service that allows manufacturers and retailers to receive reviews of their products.

As part of this exercise, we were asked to choose from 50 datasets to extract, transform and load into a dataframe in order to complete our analysis. Throughout this analysis, we use:

- PySpark to extract the dataset, transform the data, connect to AWS RDS instance and load the transformed data into pgAdmin.
- Google Colaboratory to import PySpark libraries and connect to Postgres in order to create SQL tables and export the results.

Of the 50 datasets, I chose to analyze reviews that were made by users in the "Automotive" category.


## Results and Findings

The dataset had millions of records of reviews. In order to focus on reviews that would be considered more likely to be helpful, we needed to filter the dataset by:

- Count of Total Votes equal or greater than 20.
- Percent of Helpful Votes to Total Votes equal or greater than 50%.

<img width="885" alt="image" src="https://user-images.githubusercontent.com/104689265/188257868-641c4c6f-dc1c-4b54-ac78-dec12e20bdeb.png">


The results reduced the total number of reviews from severals millions to thousands. We observed the following:

1. How many Vine reviews and non-Vine reviews were there?

<img width="953" alt="image" src="https://user-images.githubusercontent.com/104689265/188257974-db41eb25-86f4-49ae-8c5f-6178531d4c56.png">


Vine members made up only 0.3% (82) of the reviews whereas the remaining 99.7% were Non-Vine members (24723).

2. How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

Vine members gave 33 out of 82 reviews a 5 star rating.
Non-Vine members gave 12,795 out of 24,723 reviews a 5 star rating.

3. What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

40.2% of the reviews for Vine members were rated 5 stars.
51.8% of the reviews for Non-Vine members were rated 5 stars.

## Summary and Conclusion

Based on the results, Vine members did show bias when rating their products considering that the number of 5-star ratings was about 10% more than Non-Vine members (40.2% vs. 51.8%). With this, we can assume that Vine customers are much more critical when submitting their reviews. However, in order to support this assumption further, we should include all of the data rather than filtering it to a percentage of helpful vs. total votes as we did for this analysis. Reviewing the data as is would give us more information and allow us to further support our assumption as shown below.

This may be different with other review categories such as, sports, video games, furnitures, etc.
