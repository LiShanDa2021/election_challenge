# Analysis of CO's 1st Congressional District Election

## Project Overview

A Colorado Board of elections asked us to audit a recent local congressional election. Since hundreds of thousands of votes were cast, they needed to automate this process. I did so using the Python programming language. As part of the audit I created a Python program titled PyPoll_Challenge.py to do the following.

1. Calculate the total number of votes cast.
  + I did this with a `for` loop that went through the .csv file and increase a variable by 1 for each row.
2. Acquire a complete list of candidates who received votes.
  + I did this by creating an empty list of candidates and then creating a conditional within the `for` loop. Whenever the `for` loop encountered a candidate not yet contained within the list, it added that candidate to the list.
3. Calculate the total number of votes each candidate received.
  + I did this by creating a dictionary that mapped a candidate's name to a variable containing their vote tally.
4. Calculate the percentage of votes each candidate won.
  + I did this by using Python's ability to perform mathematical functions.
5. Determine the winner based on the popular vote.
  + I did this by creating a variable to store the highest vote total and then creating a conditional that compared a candidate's votes to said variable. If the candidate's vote total was higher than the variable storing the highest vote total, the candidate's name was stored in the winning candidate slot and their vote total replaced the variable.

## Resources

* Data Source: election_results.csv
* Software: Python 3.8.8

## Summary

The analysis of the election shows that:

* There were 369,711 votes cast in the election.

* The counties involved were:
  + Jefferson
  + Denver
  + Arapahoe

* The number of votes and percentages of the total vote by county were as follows.
  + Jefferson made up 10.5% of the vote with 38,855 votes.
  + Denver made up 82.8% of the vote with 306,055 votes.
  + Arapahoe made up 6.7% of the vote with 24,801 votes.

* Denver had the largest number of votes with 306,055 votes. 

* The candidates were:
  + Charles Casper Stockham
  + Diana DeGette
  + Raymon Anthony Doane

* The candidate results were:
  + Charles Casper Stockhame received 23.0% of the vote with 85,213 votes.
  + Diana DeGette received 73.8% of the vote with 272,892 votes.
  + Raymon Anthony Doane received 3.1% of the vote with 11,606 votes.

* The winner of the election was:
  + Diana DeGette with 73.8% of the vote and 272,892 votes.

Here is a screenshot of the resulting terminal output when PyPoll_Challenge.py is run.

![terminal results](https://github.com/LiShanDa2021/election_challenge/blob/main/terminal%20screenshot%20election%20analysis.png?raw=true)

And here is a screenshot of the resulting text file it prints.

![text results](https://github.com/LiShanDa2021/election_challenge/blob/main/text%20file%20screenshot%20election%20analysis.png?raw=true)

## Election Audit Summary

The use of PyPoll_Challenge.py in Colorado's first district congressional election was a resounding success. The program was able to parse hundreds of thousands of lines of data in less than a second and provide a useful breakdown of the election. Because of PyPoll's success, I propose we sell the program to other districts who want to automate their elections. In order to do so, however, I would need to make changes to the program. First of all, other districts may require even more data. They might want to see a breakdown of how many votes a candidate received in a given county. I may even need to break it down even further into developing a way to analyze results by precinct. Furthermore, presently, the program lacks a method to respond to ties. While the probability of a tie is miniscule in a given county and unlikely in a given precinct, it is almost certain that, accross thousands of precincts there will be a few ties. A few lines of code could enable the program to account for them. Finally, there needs to be a more secure way of storing the election data before it is analyzed. I was able to open the original .csv file and change one of the names to Mickey Mouse and then save the file again.


