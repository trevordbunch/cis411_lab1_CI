# Lab Report: Continuous Integration
___
**Course:** CIS 411, Spring 2021  
**Instructor(s):** [Trevor Bunch](https://github.com/trevordbunch)  
**Name:** Adam Hungerford 
**GitHub Handle:** [Adam Hungerford](https://github.com/adamhungerford)  
**Repository:** https://github.com/adamhungerford/cis411_lab1_CI
___

# Step 1: Fork this repository
- The URL of my forked repository: https://github.com/adamhungerford/cis411_lab1_CI
[!Git Fork Diagram](../assets/gitForkDiagram.png)

# Step 2: Clone your forked repository from the command line  
The cloned repository is located at C:\users\adhun\cis411_lab1_CI.
To navigate to the directory, type `cd cis411_lab1_CI`.

# Step 3: Run the application locally
- My GraphQL response from adding myself as an account on the test project
``` json
{
  "data": {
    "mutateAccount": {
      "id": "fe566914-a55f-40b7-b9e9-1e3346c7c6c6",
      "name": "Adam Hungerford",
      "email": "adhungerford02@gmail.com"
    }
  }
}
```

# Step 4: Creating a feature branch
- The output of my git commit log
```
14f8d7b (HEAD -> labreport, origin/labreport) Created and began work on the lab report. Hi @trevordbunch!
7490dcb (upstream/main, origin/main, origin/HEAD, main) Add Links to Node in Instructions
ecaaa53 Update branch terminology
c552213 Merge pull request #3 from hallienicholas/main
78ede9f Corrected error
1fe415c Merge pull request #1 from trevordbunch/labreport
13e571f Update Lab readme, instructions and templates
eafe253 Adjust submitting instructions
47e83cd Add images to LabReport
ec18770 Add Images
dbf826a Answer Step 4
a9c1de6 Complete Step 1, 2 and 3 of LAB_TREVORDBUNCH
1ead543 remove LAB.md
8c38613 Initial commit of labreport with @tangollama
dabceca Merge pull request #24 from tangollama/circleci
a4096db Create README.md
2f01bf4 Update LAB_INSTRUCTIONS.md
347bd50 Update LAB_INSTRUCTIONS.md
7aaa9f3 Update LAB_INSTRUCTIONS.md
37393ae Bug fixed
1949d2a Update LAB_INSTRUCTIONS.md
d36ad90 Update LAB.md
59ef18a Update LAB_INSTRUCTIONS.md
37be3c8 Update LAB_INSTRUCTIONS.md
97da547 Update LAB.md
0bd6244 updated Step 0 title
4562cd8 added npm and node install repreq
255051e adding template
13a09b7 Adding the LAB.md and correcting some instructions.
d2ddea5 Version 0.0.1 of the lab isntructions
ab312fc more progress
62fb0a5 more progress
fe1937b more in the lab instructions
3e807fb first section
9ae6b83 remove LAB.md
e429c1a lab instructions
ce1fcea circleci default config
80bbdbb circleci default config
968099e remove test db
7362cd1 working
44ce6ae Initial commit
```
- The accompanying diagram of what my feature branch precisely and conceptually represents...
[!Branches diagram](../assets/branchesDiagram)

# Step 5: Setup a Continuous Integration configuration
- What is the .circleci/config.yml doing?  

It seems as though .circleci/config.yml automizes certain parts of the integration process (checking out branches), as well as testing them before merging. 

- What do the various sections on the config file do?  
`version` seems to be meta information, or maybe just a command telling CircleCI to use a specific version of itself. The main part of the config is `jobs`, which probably indicates a list of things to do before integration. `build` includes all of the steps during the build process. `docker` probably has something to do with Docker. `working_directory` gives CircleCI a place to work inside. `steps` is an outline of the instructions to follow for the build process. `restore-cache` seems to be a failsafe in case the integration is unsuccessful. `run` installs yarn, which will be used to test later. `save_cache` probably makes a test copy of the project to run tests on in the next `run`.

- When a CI build is successful, what does that philosophically and practically/precisely indicate about the build?  

The new parts of the build do not conflict with the rest of the build in ways that would cannibalize the build (i.e., functional errors instead of syntax conflicts). 

- If you were to take the next step and ready this project for Continuous Delivery, what additional changes might you make in this configuration (conceptual, not code)?  

I would like to add logic to handle sending things to different branches, where different actions would be triggered. (For example, changes to the main branch would automatically deploy, while changes to the labreport branch would still trigger testing.)
   

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
![CircleCI Success](../assets/circleci_success.png)

# Step 7: Submitting a Pull Request
_Remember to reference at least one other student in the PR content via their GitHub handle._



# Step 8: [EXTRA CREDIT] Augment the core project
PR reference in the report to one of the following:
1. Add one or more unit tests to the core assignment project. 
2. Configure the CircleCI config.yml to automatically build a Docker image of the project.
3. Configure an automatic deployment of the successful CircleCI build to an Amazon EC2 instance.
