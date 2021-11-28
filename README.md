# Election analysis

## Project Overview
A Colorado Board of Elections employee has given me the following tasks to complete the election audit of a recent local congressional election.

1. Calculate the total number of votes cast.
2. Get a complete list of candidates who received votes
3. Calculate the percentage of votes each candidate won
4. Determine the winner of the election based on popular vote

After the submission of the first information request. I have been requested to provide information related to the disclosure by county containing the following information>

5. List of the counties involved in the election with their respective turnout.
6. Percentage of turnout that each county have 
7. County with the highest turnout during the election

## Resources 
- Data Source: election_results.csv
- Software: Python 3.9.9, Visual Studio Code, 1.62.3

## Election-Audit Results:

A complete summary of the election is produced by the outcome of the code developed audit of the election. A screen shoot of the outcome of the code developed is attached below:

![outcome](/Resources/Election_summary.png)

## Election Audit Summary

Once the audit of this Election has been performed, there is an investment already done in developing a code that runs the Audit and produce a report automatically. It could be in the interest of the Election Commission on using this script for future elections. 

The most important two changes to be performed in the script are related to providing the user with the possibility of entering the name of the file to be analyzed and the name of the file where the output must be stored. 

This could be achieved by replacing the lines 8 to 11 in the script by the following:

    8   # Ask the user to input the file name to be audited
    9   source_of_info = str(input("Please load the file that you    want to analyze in the Resources folder and then enter the name of the file here including the extension: "))
    10  # Ask the user to input the file name where output will be stored
    11   output_of_info = str(input("Please set the name of the file that would be stored as result of the audit on the Analysis folder: "))
    12  # Add a variable to load a file from a path.
    13  file_to_load = os.path.join("Resources", source_of_info)
    14  # Add a variable to save the file to a path.
    15  file_to_save = os.path.join("analysis", output_of_info)

With the replacement the script would be ready to analyze any file with election outcome coded in the way election_results.cvs is presented.

Other functionalities that can be incorporated are related to allow the user to set up the headers of the cvs file to be used so different format of file could be analyzed. This functionality request more changes in the script but they start in the same way as the previous. Requires and input of the user that modifies the way the script runs.

It is also possible to incorporate the results per candidate on a per county. This will require a modification of the script adding a more detailed disclosure per county. 

Finally, this file could be used on a national level, It would need a per State analysis that would require some modifications on the script but running on the same rationale used to build up this one. 

The response time of the script is very fast, and the results are 100% accurate so I believe that the Election Commission should think seriously about expanding this script. 

A version with the first change is already included on the code called PyPoll_Challenge_Recoded.py as a proof of the potential of this script.
