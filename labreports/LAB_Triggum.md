# Lab Report: Continuous Integration
___
**Course:** CIS 411, Spring 2021  
**Instructor(s):** [Trevor Bunch](https://github.com/trevordbunch)  
**Name:** Bryan Chang 
**GitHub Handle:** Triggum  
**Repository:** [Your Forked Repository](https://github.com/Triggum/cis411_lab1_CI.git)  
___

# Step 1: Fork this repository
- The URL of my forked repository: https://github.com/Triggum/cis411_lab1_CI.git
- [The accompanying diagram of what my fork precisely and conceptually represent](https://docs.google.com/drawings/d/e/2PACX-1vR-NP9_xXGGhqzy1veUhCRUP3w1VXFGa-hMJA-4SSULd83UmaGaSHCUMq0sDxD2vr9nHaKTc4lcH-c9/pub?w=960&h=720)

# Step 2: Clone your forked repository from the command line  
- My local file directory is...
  - C:\Users\Bryan Chang\Documents\Github\cis411_lab1_CI
- The command to navigate to the directory when I open up the command line is...
  - cd Documents\Github\cis411_lab1_CI

# Step 3: Run the application locally
- My GraphQL response from adding myself as an account on the test project
``` json
{
  "data": {
    "mutateAccount": {
      "id": "32398b0b-c3ec-4511-a572-792023b36ded",
      "name": "Bryan Chang",
      "email": "Bryanc2h4@gmail.com"
    }
  }
}
```

# Step 4: Creating a feature branch
- The output of my git commit log
```
PS C:\Users\Bryan Chang\Documents\GitHub\cis411_lab1_CI\labreports> git log --oneline 
9c6f49d (HEAD -> labreport, origin/labreport) added lab report templated from @trevordbunch
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

```
- [The accompanying diagram of what my feature branch precisely and conceptually represents](https://docs.google.com/drawings/d/e/2PACX-1vSUkPoO5ZGwY0wc-ZYJahopNk6Ab5Z7e7qoROeKz2bHLf4yDwXcWEPiPDi4ipkT6vgBgYk1r4DtQ2rM/pub?w=960&h=720)

# Step 5: Setup a Continuous Integration configuration
- What is the .circleci/config.yml doing?  
  It is a tool to setup a build and to execute a shell command @CircleCI_Documentation

- What do the various sections on the config file do?  
  - Citation: @CircleCI_Documentation_ConfigurationInformation
  - The first line indicates the version
  - Lines 2 to 3 are the job level where there is a collection of children
  - Line 6 to 7 contains run directives that are executed in the order that they were declared
  - Line 8 provides organizational information 
  - Line 9 to 11 is where a list of shell commands can be initiated
   
- When a CI build is successful, what does that philosophically and practically/precisely indicate about the build?  
  - It means that a part to the whole project has been made and progress has been made. It also precisely indicates how much the project is finished.
   

- If you were to take the next step and ready this project for Continuous Delivery, what additional changes might you make in this configuration (conceptual, not code)?  
  - Testing the code and approving the tests. (Source: @https://www.atlassian.com/continuous-delivery/continuous-deployment/how-to-get-to-continuous-deployment)
   

# Step 6: Merging the feature branch
* The output of my git commit log
```
PS C:\Users\Bryan Chang\Documents\GitHub\cis411_lab1_CI\labreports> git merge labreport 
Updating 7490dcb..9c6f49d
Fast-forward
 labreports/LAB_Triggum.md | 79 +++++++++++++++++++++++++++++++++++++++++++++++
 1 file changed, 79 insertions(+)
 create mode 100644 labreports/LAB_Triggum.md
PS C:\Users\Bryan Chang\Documents\GitHub\cis411_lab1_CI\labreports> git log --oneline   
9c6f49d (HEAD -> main, origin/labreport, labreport) added lab report templated from @trevordbunch
7490dcb (upstream/main, origin/main, origin/HEAD) Add Links to Node in Instructions     
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
(END)
```

* A screenshot of the _Jobs_ list in CircleCI
![CircleCI Success](../assets/)

# Step 7: Submitting a Pull Request
_Remember to reference at least one other student in the PR content via their GitHub handle._



# Step 8: [EXTRA CREDIT] Augment the core project
PR reference in the report to one of the following:
1. Add one or more unit tests to the core assignment project. 
2. Configure the CircleCI config.yml to automatically build a Docker image of the project.
3. Configure an automatic deployment of the successful CircleCI build to an Amazon EC2 instance.
