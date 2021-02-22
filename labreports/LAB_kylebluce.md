# Lab Report: Continuous Integration
___
**Course:** CIS 411, Spring 2021  
**Instructor(s):** [Trevor Bunch](https://github.com/trevordbunch)  
**Name:** Kyle Luce  
**GitHub Handle:** https://github.com/kylebluce  
**Repository:** https://github.com/kylebluce/cis411_lab1_CI  
___

# Step 1: Fork this repository
- The URL of my forked repository: https://github.com/kylebluce/cis411_lab1_CI

![ForkedRepoDiagram](/assets/cis411lab1drawing1.png)

# Step 2: Clone your forked repository from the command line  
- My local file directory is...

"C:\Users\Kyle Luce\Documents\GitHub\cis411_lab1_CI"    

- The command to navigate to the directory when I open up the command line is... 

"cd C:\Users\Kyle Luce\Documents\GitHub\cis411_lab1_CI"    

# Step 3: Run the application locally
- My GraphQL response from adding myself as an account on the test project
``` json
{
  "data": {
    "mutateAccount": {
      "id": "e16e7134-e09a-4067-a423-73e6c61f59f6",
      "name": "Kyle Luce",
      "email": "kylebluce@gmail.com"
    }
  }
}
```

# Step 4: Creating a feature branch
- The output of my git commit log
```
964e930 (HEAD -> labreport, origin/labreport) labreport @trevordbunch
```
![FeatureBranchDiagram](/assets/cis411lab1drawing2.png)

# Step 5: Setup a Continuous Integration configuration
- What is the .circleci/config.yml doing?  

According to the CircleCI website, config.yml is a powerful file that defines the entire pipeline for a project. That means that this file is reponsible for the connection between CircleCI and GitHub. This file represents all the changes made during the Continuous Integration process.

- What do the various sections on the config file do? 

The config file has the following sections: workflows, jobs, orbs, executors, and commands. Workflows represent multiple jobs or tasks to be done. The jobs go through a series of steps that run commands. Executors define build environments which are used to run jobs. Orbs are reusable snippets of code that can be used anywhere throughout the config.
   
- When a CI build is successful, what does that philosophically and practically/precisely indicate about the build?  

When a CI build is successful, that means that the build is running without errors and is connected to GitHub properly. It means that the process of continous integration is working with whatever you have setup in the config file and the rest of your project.

- If you were to take the next step and ready this project for Continuous Delivery, what additional changes might you make in this configuration (conceptual, not code)?  

I think the some of the most important aspects of continuous delivery is to be able to keep the project up to date. So. I would make sure that the project was being continuously updates. I think the other thing I would implement is additional security measures so that the project was safe from being tampered with. That would probably include additional access control and possibly encryption.
   

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
![CircleCI Jobs](/assets/cis411CIJobs.PNG)
