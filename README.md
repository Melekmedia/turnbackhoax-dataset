## TURNBACKHOAX DATASET

***Here you can find the dataset from https://turnbackhoax.id***

***This dataset was obtained on 25th April 2021***

***This dataset contained News dataset in Bahasa Indonesia***

## Overview  
The dataset CSV files is comma separated file and have the following columns:

 - `label` - Unique identifider for each news
 - `Headline` - Title of the news article
 - `Body` - Content of the news article
 
## Scrapping Method    
 
Scripts are written in PHP.

Install all the libraries using composer and the following command
    
    composer install

 
There is two main function that has to be run

First one is 

    $script->copy_header_and_link();

This function run a request to https://turnbackhoax.id to get the header and the link of each news

We manually copy and paste them to excel file (can be seen in code/src/Scrapping Result (Heading and Link).xlsx)

After we got the link, we iterating them and send a request to get their content using this function


    $script->copy_content();

And again we manually copy them to excel

## UPDATE by Melekmedia (15/1/2022)

We regroup the article according to hoax category based on First Draft's version. Article without category, excluded. Check the dataset here >> https://docs.google.com/spreadsheets/d/1szynyjjtqnk-d2grE8uh35MRTOTBN6RHXmeI8FiB5Jo/edit?usp=sharing
