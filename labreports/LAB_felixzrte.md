# Lab Report: Continuous Integration
___
**Course:** CIS 411, Spring 2021  
**Instructor(s):** [Trevor Bunch](https://github.com/trevordbunch)  
**Name:** Felix Zarate  
**GitHub Handle:** @felixzrte 
**Repository:** cis411_lab_CI 
___

# Step 1: Fork this repository
- The URL of my forked repository: https://github.com/felixzrte/cis411_lab1_CI
- The accompanying diagram of what my fork precisely and conceptually represents...
![Fork Diagram](../assets/Fork_Diagram.pdf)

# Step 2: Clone your forked repository from the command line  
- My local file directory is: /Users/felixzarate/Documents/GitHub/cis411_lab1_CI
- The command to navigate to the directory when I open up the command line is:
cd /Users/felixzarate/Documents/GitHub/cis411_lab1_CI

# Step 3: Run the application locally
- My GraphQL response from adding myself as an account on the test project
``` json
{
  "data": {
    "mutateAccount": {
      "id": "362c952d-f066-4c61-b90c-5b7223faf7bb",
      "name": "Felix Zarate",
      "email": "fz1151@messiah.edu"
    }
  }
}
```

# Step 4: Creating a feature branch
- The output of my git commit log
```
8065951 (HEAD -> labreport, origin/labreport) your commit and reference @trevorbunch in the message
7490dcb (upstream/main, origin/main, origin/HEAD, main) Add Links to Node in Instructions
```
- The accompanying diagram of what my feature branch precisely and conceptually represents...
![Fork Diagram](../assets/Branch_Diagram.pdf)


# Step 5: Setup a Continuous Integration configuration
- What is the .circleci/config.yml doing?  
This file is what will be read when CircleCI is ran. This file contains code that serves the purpose, "to orchestrate your build, tests, security scans, approval steps, and deployment." (https://circleci.com/docs/2.0/config-intro/)

- What do the various sections on the config file do?  
  Within the config file, there are multiple levels. The top-level is the jobs keyword and within jobs, you have the build keyword. In this file, build is the only job. Step contains all the run commands which will run the code in the order that the run statement are put in.

- When a CI build is successful, what does that philosophically and practically/precisely indicate about the build?  
   If the build is successful then that tells the team that the build can be pushed or deployed.

- If you were to take the next step and ready this project for Continuous Delivery, what additional changes might you make in this configuration (conceptual, not code)?  
Integrate the continuous delivery process into an agile framework. Agile teams would focus on specific features that need to be refined.   

# Step 6: Merging the feature branch
* The output of my git commit log
```

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
