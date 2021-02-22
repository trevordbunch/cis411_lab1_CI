# Lab Report: Continuous Integration
___
**Course:** CIS 411, Spring 2021  
**Instructor(s):** [Trevor Bunch](https://github.com/trevordbunch)  
**Name:** Isaac Parada  
**GitHub Handle:** isaacparada  
**Repository:** Your Forked Repository  
___

# Step 1: Fork this repository
- The URL of my forked repository: https://github.com/isaacparada/cis411_lab1_CI
- The accompanying diagram of what my fork precisely and conceptually represents...

![Fork Diagram](/labreports/Screen1.png)

# Step 2: Clone your forked repository from the command line  
- My local file directory is... (Finder on Mac) Isaac > Documents > GitHub > cis411_lab1_CI
- The command to navigate to the directory when I open up the command line is... cd Documents/GitHub/cis411_lab1_CI

# Step 3: Run the application locally
- My GraphQL response from adding myself as an account on the test project
``` json
{
  "data": {
    "mutateAccount": {
      "id": "637e2569-f7d5-40a4-ba95-9e063db07d87",
      "name": "Isaac Parada",
      "email": "ip1164@messiah.edu"
    }
  }
}
```

# Step 4: Creating a feature branch
- The output of my git commit log
```
ea76725 (HEAD -> labreport) Screenshot of commit log
65e12e3 (origin/labreport) update of .readme file
7e13f81 Upload of Fork diagram
4f00eda Create Screen2.png
a0f13b1 Create Screen3.png
f5dfcaf Update config.yml
cb5be44 Create LAB_isaacparada.md
```
- The accompanying diagram of what my feature branch precisely and conceptually represents...

![Feature Diagram](/labreports/Screen6.png)

# Step 5: Setup a Continuous Integration configuration
- What is the .circleci/config.yml doing?  

It is testing the code against criteria that has been written. 

- What do the various sections on the config file do?  

They allow you to add workflows and jobs (which are the tests I believe). From what I gather (might be completely wrong) is it adds the new code to a container and if all the tests are passed it integrates the contents of that container into the main project's containers.

- When a CI build is successful, what does that philosophically and practically/precisely indicate about the build?  

That the changes have been integrated into the final build. And that the changes were compatible with the set criteria the team decided to follow. 
   

- If you were to take the next step and ready this project for Continuous Delivery, what additional changes might you make in this configuration (conceptual, not code)?  

Have some ability to add new code into the source of the live application. 
   

# Step 6: Merging the feature branch
* The output of my git commit log
```
Trevors-MBP:cis411_lab0 trevorbunch$ git log --oneline
dbf826a (HEAD -> labreport, origin/labreport) Answer Step 4
a9c1de6 Complete Step 1, 2 and 3 of LAB_TREVORDBUNCH
1ead543 remove LAB.md
8c38613 Initial commit of labreport with @tangollama
dabceca (upstream/main, origin/main, origin/HEAD, main) Merge pull request #24 from tangollama/circleci
a4096db Create README.md
...
44ce6ae Initial commit
(END)
```

* A screenshot of the _Jobs_ list in CircleCI
![CircleCI](/labreports/Screen2.png)

# Step 7: Submitting a Pull Request
_Remember to reference at least one other student in the PR content via their GitHub handle._



# Step 8: [EXTRA CREDIT] Augment the core project
PR reference in the report to one of the following:
1. Add one or more unit tests to the core assignment project. 
2. Configure the CircleCI config.yml to automatically build a Docker image of the project.
3. Configure an automatic deployment of the successful CircleCI build to an Amazon EC2 instance.