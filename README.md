# Election_Analysis

# Overview of Audit
In this Audit we took the voting data and through our Python script we out put the total votes, votes by county (count and %), largest county turnout, votes by candidate (count and %), and the winning results.The purpose of this audit is to easily take voting data and show key data points in a clean format. We can see how each county voted along with how close the actual race was.
# Election Audit Results
    -Total Votes: 369,711
    -Jefferson: 10.5 % (38,855)
    -Denver: 82.8 % (306,055)
    -Arapahoe: 6.7 % (24,801)
    
    -Largest County Turnout: Denver
    
    -Charles Casper Stockham: 23.0% (85,213)
    -Diana DeGette: 73.8% (272,892)
    -Raymon Anthony Doane: 3.1% (11,606)
    
    -Winner: Diana DeGette
    -Winning Vote Count: 272,892
    -Winning Percentage: 73.8%
    
# Election Audit Summary
Given that the voting data comes in the same format, with very minimal changes we can run this for any election to output a file with a clean summary of the results. The code can also be modified to output different data, if you so chose. Below is the only part of the code we would need to change. Here is showing how we tell the script to find the election result data.

```
#Add a variable to load a file from a path.
file_to_load = os.path.join(".", "Resources", "election_results.csv")
```
Another adjustment we could make is the "Largest County Turnout". I personally don't think this tells us much and the highest number of votes is going to always be Denver based on its population. We can delete this out or we could adjust it to be more meaningful if we added the total number of registered voters or potential voters for each county we could return the largest turn out based on the % total voters who voted.
 ```
 if county_vote_count > winning_county_votes:
            winning_county = county
            winning_county_votes = county_vote_count
```
More potential data that could be added is the candidate breakdown for each county. This would make the file a bit busier with 9 more lines of data plus titles, but could provide useful insight.


