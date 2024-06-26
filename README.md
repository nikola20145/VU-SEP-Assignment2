# VU-SEP-Assignment2

# Report for Assignment 2

Programming language used: Java

## Workflow 1: Testing (`testing.yml`)

I used Maven to compile and run the tests on each commit made to any repository branch.
Link to an execution of testing workflow, which demonstrates the process of using Maven to compile and run the tests on each commit made to any repository branch: https://github.com/YBushi/VU-SEP-Assignment2/actions/runs/9635440427

## Workflow 2: Static analysis (`static_analysis_1.yml`)

<Inform which tool is used to perform code quality check with static analysis.>

<Provide the link to one log (from the "Actions" tab on GitHub) of an execution of this workflow>

## Workflow 3: Static analysis (`static_analysis_2.yml`)

<Inform which tool is used to perform code quality check with static analysis.>

Since we are using Maven to build and compile the code, I implemented a workflow that runs the maven checkstyle function (default) as the 2nd static code analysis which runs on Pull Requests made to any branch. Here is a link to one log from the actions: https://github.com/YBushi/VU-SEP-Assignment2/actions/runs/9686187402. 

## Workflow 4: Release (`release.yml`)

<Provide the link to one log (from the "Actions" tab on GitHub) of an execution of this workflow>

## Statement of individual contributions
Tomas: I have created a Maven pom.xml file that was set up to compile and run tests that were provided. I have set up the structure of this repository by creating new folders into which I put the files that were provided. I have created testing-workflow branch, where I have implemented testing workflow. Finally, I have reviewed the implementation of the workflows of my team members.

Jayran: I did research on the different Java Static Code Analysis Tools. I selected one that I found the easiest for me to understand and use which ended up being Checkstyle. I did research on the different checkstyles implementations, and later understood that I should implement it through maven since that is what we are using to build and compile the code. The builtin checkstyle mvn command uses there own checkstyle rule to assess the code. I implemented this through trial and error, creating issues when there is something that's not working and making a commit that refernces or fixes the issue to keep my teammates updated. I then made my pull request and reviewed and approved on my teamates workflows via the issues and pull requests. 

<Write what each group member did. Use the following table for that and add additional text under it if you see fit.>


| Member | Created workflows | Reviewed workflows | Merged pull requests' number |
| --- | --- | --- | --- |
| Tomas | 1 | 3 |  |
| Jayran | 1 | 3 | 26 |
| Luis | 1 | 3 | |
| Nikola | 1 | 3 | |

