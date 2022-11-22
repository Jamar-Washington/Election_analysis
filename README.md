# Election_analysis

## Project Overview
In the PyPoll project, we are helping Tom, who works at the Colorado Board of Elections, with getting the results of a congressional seat in the state of Colorado. His manager wants to use Python to automate the process by taking the data from an CSV file. He has asked us to help find the total number of votes, the number of votes each candidate recieved, the percentage of votes each candidate recieved, and which candidate won the election by popular vote.

### Tools used in the project
**Python**

## Election-Audit
### Results

* Total number of votes
To get the total number of votes, the rows were calculated in the CSV file. To exclude the first row that did not have a vote, a line of code was used as a way to exclude it from the votes.

* Number of votes each candidate recieved
To find out the number of votes each candidate recieved, first the candidate was found by finding their name in each row. If the candidate was not already added into list of candidates running, they were added to list and got a vote added to their. If they were already added, the list was bypassed and the candidate received another vote.

* Percentage of votes each candidate recieved
Once we found the number of votes each candidate recieved, that number was divided by the total number of votes to calculate the percentage.

* Candidate who won the popular
After every candidate was added to list with their respected amount of vote, a block of code was written to if candidate had a higher vote count then the last candidate on the list. If they did not, the list would go to the next candidate. However, if the count was higher, then the candidate would be the candidate that the code would look to see if candidates further down the list had a higher voter count. In order to start the list, a "blank" candidate was initialized with no name and no votes. 

* County Turnout
The county turnout was the same as the results mentioned above. The only change was that instead of candidates, the counties votes are used. The county votes were extracted by using a different part of the CSV file.

The results were all printed out in a text file as shown below.
![results](https://user-images.githubusercontent.com/109183214/187247585-4a4ee761-5e28-4255-88e5-6e35154b7da0.png)

### Summary
The best part about this code is that it can be used to determine senatorial and local elections as well. If we were to change it a senatorial election, the whole state of Colorado would be used so the largest county turnout would be removed. If this was a local election, we could modify the code to look at the zip code instead of a county.
