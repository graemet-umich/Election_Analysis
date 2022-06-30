# Election Analysis
The Colorado Board of Elections requires an election audit for a U.S. Congressional Precinct election.

## Overview of Election Audit
An election audit is required by the Colorado Board of Elections to certify an election. There was an initial request for a limited audit of a Colorado U.S. Congressional Precinct election, but requirements changed, and a more detailed audit was needed.

### Election Results Received
The election results from three different voting methods (mail-in ballots, punch cards, and direct recording electronic counting machines) were combined and provided here in a tabulated CSV file. A single vote is represented by a record (row) consisting of a Ballot ID, the County in which the vote was cast, and the candidate chosen. 

### A Better Way: From Excel to Python
Previous election audits were performed using Excel, which requires cumbersome manual steps. The automated election audit provided here is performed using Python, which is faster, less prone to human error, and more flexible. If this automated election audit proves to be successful, it can be used to certify other Congressional, Senatorial, State, and Local elections.

## Election Audit Results
The election audit has specific formatting guidelines. The correctly formatted audit is provided here:

```
Election Results
-------------------------
Total Votes: 369,711
-------------------------

County Votes:
Jefferson: 10.5% (38,855)
Denver: 82.8% (306,055)
Arapahoe: 6.7% (24,801)

-------------------------
Largest County Turnout: Denver
-------------------------
Charles Casper Stockham: 23.0% (85,213)
Diana DeGette: 73.8% (272,892)
Raymon Anthony Doane: 3.1% (11,606)
-------------------------
Winner: Diana DeGette
Winning Vote Count: 272,892
Winning Percentage: 73.8%
-------------------------
```

### Initial Election Audit Requirements and Results
- **Votes Cast:** There were 369,711 votes cast.
- **Total Votes and Percentage of Total Votes for Each Candidate:** There were only three candidates on the ballot. Charles Casper Stockham received 85,213 votes, which was 23.0% of the total votes. Diana DeGette received 272,892 votes, which was 73.8% of the total votes. Raymon Anthony Doane received 11,606 votes, which was 3.1% of the total votes.
- **Winner of the Election:** Candidate Diana DeGette won the election in a landslide with 272,892 votes, which was 73.8% of the vote total.

### Additional Election Audit Requirements and Results
- **Total Votes and Percentage of Total Votes for Each County in the Precinct:** This Precinct has only three counties. There were 38,855 Jefferson County voters, which was 10.5% of the total vote. There were 306,055 Denver County voters, which was 82.8% of the total vote. There were 24,801 Arapahoe County voters, which was 6.7% of the total vote.
- **County with the Highest Turnout:** Denver County had the highest voter turnout of any county by far with 306,055 votes cast.


## Election Audit Summary
Using Python, this automated election audit was completed faster and with less human error than previous audits using Excel. However, the real power of this new Python programmatic approach is its flexibility in easily being able to handle other U.S. Congressional, U.S. Senatorial, and even State and Local elections. Here are examples of how the Python script can be changed to accomodate different elections.

### Change the Election Audit Title to Accomodate Different Election Years and Different Election Types
Colorado is divided into 7 U.S. Congressional Districts (and set to gain an additional district at the 2022 mid-terms). Currently the election audit is generic:

```
    # Print the final vote count
    election_results = (
        f"\nElection Results\n"
        ...
```

The title can be made more specific by adding the election year and the election type.

```
    election_year = 2022
    election_type = "Fifth District U.S. Congressional"
    ...
    # Print the final vote count
    election_results = (
        f"\n{election_year} Colorado {election_type} Election Results\n"
        ...
```

What about a U.S. Senatorial election?

```
    election_type = "U.S. Senatorial"
```

Or a State Senatorial election?

```
    election_type = "State Senatorial"
```

The rest of the script stays the same. The election audit still provides the same county and candidate summary statistics.