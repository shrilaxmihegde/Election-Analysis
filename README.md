# Overview of Election Audit Analysis 
A Colorado Board of Elections has requested to complete the election audit of a recent local congressional election. 
1. Total number of  votes cast.
2. Total number of  votes each candidate  received.
3. Calculate the  total number of votes casted in each county.
4. Winner of the election based on popular votes.
5. Calculate the percentage each candidate won.

##  Purpose:
We practiced many things in python election _project
1. Read and extract data from CSV file.
	```with open(file_to_load) as election_data:
    reader = csv.reader(election_data)
2. Perform mathematical operations using data types.
3. Declare the variables using different data types.
4. Create and use data structures like lists, tuples,and  dictionaries. 

```
		candidate_options = []
		candidate_votes = {}
		county_options = []
		county_votes  = {}
```

5. How to give a path from in python code.
```
	file_to_load = os.path.join( "Resources", "election_results.csv")
	file_to_save = os.path.join("analysis", "election_analysis.txt")
```	

6. write data to an output file and print the file.
```
	  txt_file.write(winning_candidate_summary)
```	  
	  
##  Election-Audit Result :
 
1. Total Votes Cast : 369,711

![Total Votes)](/Resources/Totalvotes.png)

2. The number of votes and  percentage of each county:

> - Jefferson : 10.5% (38,855)
> - Denver :  82.8% (306,055)
> - Arapahoe :6.7% (24,801)
	
> - Largest county turnout :Denver
	 
![county Summary)](/Resources/countysummary.png)

3. The number of votes and percentage of the total votes each candidate received:

> - Charles Casper Stockham : 23.0% (85,213)
> - Diana DeGette :  73.8% (272,892)
> - Raymon Anthony Doane : 3.1% (11,606)

4. Candidate won the election :

> - Winner ; Diana DeGette
> - Winning vote Count : 272, 892
> - winning Percentage :73.8%
    
    
![Candidate Summary)](/Resources/candidatesummary.png)


## Election -Audit summary :
This script is capable of providing the county wise summary and candidate wise sumary along with who is the winning candidate and how much percentage of the votes candidate received. This script can be generalized by accepting the input for second column in the csv file like City or State or any other segments where reporting needs to be done.
Based on the user input, summary heading  will reflect in the output file.

eg:  
```
to_be_sumarized = input ("Please enter the attribute to summarize (City or County or State) :")
		 election_results = (
        f"\nElection Results\n"
        f"-------------------------\n"
        f"Total Votes: {total_votes:,}\n"
        f"-------------------------\n\n"
        f"{to_be_sumarized} Votes:\n")
        
        f"Largest {to_be_sumarized} Turnout: {largest_county}\n"







