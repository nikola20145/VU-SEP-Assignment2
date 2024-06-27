# VU-SEP-Assignment2

# Report for Assignment 2

Programming language used: Java

## Workflow 1: Testing (`testing.yml`)

I used Maven to compile and run the tests on each commit made to any repository branch.
Link to an execution of testing workflow, which demonstrates the process of using Maven to compile and run the tests on each commit made to any repository branch: https://github.com/YBushi/VU-SEP-Assignment2/actions/runs/9635440427

## Workflow 2: Static analysis (`static_analysis_1.yml`)

The build process (compilation, testing, packaging) is efficiently managed by Maven. Code quality and consistency are maintained through PMD’s static analysis checks during the build process which is compatible with Maven. This helps in catching issues early in the development cycle, potentially saving time and resources by avoiding more complex problems later on. That is what my workflow consited of, I only involved the basic ruleset for PMD. The workflow was executed each time a commit was made on the repository : https://github.com/YBushi/VU-SEP-Assignment2/actions/runs/9643777085


## Workflow 3: Static analysis (`static_analysis_2.yml`)

<Inform which tool is used to perform code quality check with static analysis.>

Since we are using Maven to build and compile the code, I implemented a workflow that runs the maven checkstyle function (default) as the 2nd static code analysis which runs on Pull Requests made to any branch. Here is a link to one log from the actions: https://github.com/YBushi/VU-SEP-Assignment2/actions/runs/9686187402. The code style errors can be seen at the end of the output. (It is really long).

## Workflow 4: Release (`release.yml`)

[Release action log](https://github.com/YBushi/VU-SEP-Assignment2/actions/runs/9686615701)

Here is the latest log from release, its the result from our teammate testing it.

## Statement of individual contributions
Tomas: I have created a Maven pom.xml file that was set up to compile and run tests that were provided. I have set up the structure of this repository by creating new folders into which I put the files that were provided. I have created testing-workflow branch, where I have implemented testing workflow. Finally, I have reviewed the implementation of the workflows of my team members.

Nikola: I did plenty of stuff regarding the assignment which involved updating the template for the README.md, raising some important issues like posting the URL of our repo, adding the SEP team and the TA that is going to grade us. Additionally I did solid amount of work with regards to my workflow, I didn't do much research on which static analysis tool to pick. I knew we used Maven build tool and I saw some static analysis tools from Lecture 7 slides, immmediately I chose PMD which was compatible with our java project which is built with Maven. I chose it because I am somewhat familiar with it. Since the project we were given was pretty simple I used only the basic ruleset for PMD. The process of creating the workflow was solid with some trial and error and some searching on the net and use of the slides I managed to finish it, along the way consistently updated my teammates regarding the process with commits and issues. After that I of course made a pull requests and raised an issue for my teammates to review it and merge it at the end if everything is fine. Besides this throughout the whole process I made sure everyone was on the right track with their tasks and offered help if needed. Constructed a big message where I talked about the structure of commits, pull requests, issues etc... So that we will be all consistent and make the best use out of the GitHub services.

Jayran: I did research on the different Java Static Code Analysis Tools. I selected one that I found the easiest for me to understand and use which ended up being Checkstyle. I did research on the different checkstyles implementations, and later understood that I should implement it through maven since that is what we are using to build and compile the code. The builtin checkstyle mvn command uses there own checkstyle rule to assess the code. I implemented this through trial and error, creating issues when there is something that's not working and making a commit that refernces or fixes the issue to keep my teammates updated. I then made my pull request and reviewed and approved on my teamates workflows via the issues and pull requests. 

Luis: After doing some research on how to have an automatic release, I stumbled a simple issue that I had flown over: I forgot to give write permissions to the actions@github.com. After finding the fix, everthing was in order, releases have a tag that goes as follows: v"X", where X is the release number. From my understanding of code archive, a .zip and .tar file is availble for download for each release, with of course, the code corresponding to that release. In order to test it however, I had to change the "on push" to the release-workflow branch. When tests were done, I renamed it to main. After finishing my workflow, I asked my teammates to test it, and also how to test theirs, which lead me to make succesful tests which were ready to be merged in main.


<Write what each group member did. Use the following table for that and add additional text under it if you see fit.>


| Member | Created workflows | Reviewed workflows | Merged pull requests' number |
| --- | --- | --- | --- |
| Tomas | 1 | 3 | 7 |
| Jayran | 1 | 3 | 26 |
| Luis | 1 | 3 | 20 |
| Nikola | 1 | 3 | 14 |

