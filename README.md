# Election_Analysis
## Project Overview
The purpose of this project was to complete an election audit on a recent congressional election provided by a Colorado Board of Elections employee.
The tasks were as follows:

1. Calculate the total number of votes
2. Get a complete list of candidates that received votes
3. Calculate the total number of votes each candidate received
4. Calculate the percentage of votes each candidate won
5. Determine the winner of the election based on popular vote

## Resources
- Data Source: election_results.csv
- Software: Python 3.9.5, VS Code version 1.57.1.
## Summary
The analysis of the election shows that:
- There were 369,711 votes cast in the election.
- The candidates were:
  - Charles Casper Stockham
  - Diana DeGette
  - Raymon Anthony Doane
- The candidate results were
  - Charles Casper Stockham received 23% of the vote with 85,213 number of votes.
  - Diana DeGette received 73.8% of the vote with 272,892 number of votes.
  - Raymon Anthony Doane received 3.1% of the vote with 11,606 number of votes.
- The winner of the election was:
  - Diana DeGette with 73.8% of the vote and 272,892 number of votes.
## Challenge Overview
The purpose of the challenge was to use the election_results.csv data to determine the following:

- The voter turnout for each county
- The percentage of votes from each county out of the total count
- The county with the highest turnout

Our goal was to use for loops and conditional statements with membership and logical operators to print these results to the command line and save them to the election_results.txt file.

### Results:

The final results are as follows:

<img src="https://user-images.githubusercontent.com/84201614/123560813-40498f80-d76a-11eb-842a-5dbef1ed32e0.png" width="400" height="500">

- The total number of votes in the election totals 369,711 votes. 
- To find the number of votes and percentage of votes for each county we can first define the county name as a variable and create the county votes dictionary. We can create a for loop to retrieve the county vote count, calculate the percentage of votes for the county, and print the results to the terminal with the following code:

      # 6a: Write a for loop to get the county from the county dictionary.
      for county_name in county_votes:

        # 6b: Retrieve the county vote count.
        votes_county = county_votes.get(county_name)
        
        # 6c: Calculate the percentage of votes for the county.
        votes_county_percentage = float(votes_county) / float(total_votes) * 100
        county_results =(f"{county_name}: {votes_county_percentage:.1f}% ({votes_county:,})\n")
        
         # 6d: Print the county results to the terminal.
        print(county_results)

- **County votes results**:
  - Jefferson: 10.5% (38,855)
  - Denver: 82.8% (306,055)
  - Arapahoe: 6.7% (24,801)
  
  The county with the largest number of votes was Denver. We can determine this by writing an if statement with the following code:

        Write an if statement to determine the winning county and get its vote count.
      
        if (votes_county > winning_county_count) and (votes_county_percentage > winning_county_percentage):
            winning_county_count = votes_county
            winning_county = county_name
            winning_county_percent = votes_county_percentage
            
        print(winning_county)

- **Candidate results:**
  - Charles Casper Stockham: 23.0% (85,213)
  - Diana DeGette: 73.8% (272,892)
  - Raymon Anthony Doane: 3.1% (11,606)
  
To determine the candidate results we can retrieve the vote count and percentage of each candidate with the following code:

        Retrieve vote count and percentage
        
        votes = candidate_votes.get(candidate_name)
        vote_percentage = float(votes) / float(total_votes) * 100
        candidate_results = (
            f"{candidate_name}: {vote_percentage:.1f}% ({votes:,})\n")

- **Winner:**
  - Diana DeGette
  - 272,892 votes
  - 73.8% of total votes

The winning candidate, vote count, and percentage can be determined using the following code:
    
      if (votes > winning_count) and (vote_percentage > winning_percentage):
            winning_count = votes
            winning_candidate = candidate_name
            winning_percentage = vote_percentage
            

## Challenge Summary
Overall, this script was efficient in determining a variety of results for the Colorado congressional election including the winning candidate, number of votes, percentage of votes for each candidate, votes by county, and more. While this script was successful for this election, it can also be used for any election with additional modifications to the script. For example, we could collect additional data such as the winning candidate based on applicant age groups or gender and create additional variables and dictionaries to loop through and print results. The possibilities are endless!
