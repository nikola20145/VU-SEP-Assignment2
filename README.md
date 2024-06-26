# VU-SEP-Assignment2

# Report for Assignment 2

Programming language used: Java

## Workflow 1: Testing (`testing.yml`)

I used Maven to compile and run the tests on each commit made to any repository branch.
Link to an execution of testing workflow, which demonstrates the process of using Maven to compile and run the tests on each commit made to any repository branch: https://github.com/YBushi/VU-SEP-Assignment2/actions/runs/9635440427

<Provide the link to one log (from the "Actions" tab on GitHub) of an execution of this workflow>

## Workflow 2: Static analysis (`static_analysis_1.yml`)

<Inform which tool is used to perform code quality check with static analysis.>

<Provide the link to one log (from the "Actions" tab on GitHub) of an execution of this workflow>

## Workflow 3: Static analysis (`static_analysis_2.yml`)

<Inform which tool is used to perform code quality check with static analysis.>

Since we are using Maven to build and compile the code, I implemented a workflow that runs the maven checkstyle function (default) as the 2nd static code analysis which runs on Pull Requests. Here is a link to one log from the actions:
## Workflow 4: Release (`release.yml`)

<Provide the link to one log (from the "Actions" tab on GitHub) of an execution of this workflow>

## Statement of individual contributions
Tomas: I have created a Maven pom.xml file that was set up to compile and run tests that were provided. I have set up the structure of this repository by creating new folders into which I put the files that were provided. I have created testing-workflow branch, where I have implemented testing workflow. Finally, I have reviewed the implementation of the workflows of my team members.

<Write what each group member did. Use the following table for that and add additional text under it if you see fit.>

| Member | Created workflows | Reviewed workflows | Merged pull requests' number |
| --- | --- | --- | --- |
| Member A | | | |
| Member B | | | |
| Member C | | | |
| Member D | | | |

