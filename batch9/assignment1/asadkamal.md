Q1) Agile vs DevOps?
ans: Agile 
In agile method the whole process is divided into different iteration/sprint. i.e., a software having 6 features so the process should be divided into 3 sprint each having 2 features. 
The advantage of agile is to receive feedback after short sprint and make change in next sprint to save time.
In agile you must wait to complete the sprint and then release the feature.
 DevOps 
In DevOps method the whole process is also divided into different iteration/sprint, but the developer should not wait for weeks to complete the iteration, because when the code is ready then why wait for weeks. So, in DevOps the code will release immediately. 
The purpose of this is to capable team so that they can release the feature immediately and not dependent on other.

Q2) Define CI, Continuous Delivery & Continuous Deployment?
Continuous integration 
Continuous integration (CI) is the practice of automating the integration of code changes from multiple developers into a main/central repository, where builds and tests then run. Automated tools are used to assert the new code’s correctness before integration. 
Key goal is to identify failure faster and address bugs quicker.
It benefits developer most, less merge conflict. 
Continuous Delivery
it is a stage where the feature is deployed automatically in staging area for a while to test and checks that new feature will not break nothing. Can use other than main branch strategy.
Code changes are automatically built, tested, and release for production. 
Continuous Deployment
When the change is approved by CI/continuous delivery, the feature or build artifact are deployed to production environment manually and get feedback from the user. 
It can use master branch strategy (if the code merge in master so automatically deployed in production). 

Q3) What are the benefits of Cloud Computing?
•	On demand computing resource 
•	Resource scaling up and down is very easy and cheap
•	Quick and easy to meet demand 
•	Pay for what and how much is used 
•	State of art infrastructure is readily available 
•	99.99% or more uptime

Q4) Difference b/w Git & GitHub? 
Git is a version control system that lets you manage and keep track of your source code history and GitHub is an online database that allows you to keep track of and share your Git version control projects outside of your local computer/server unlike GIT

Q5) Stages of Git? 
There are 3 stages in local
•	Working directory
•	Staging area 
•	Local area/repo
And 1 stage in remote 
•	Remote repository

Q6) 3 methods of git reset
•	git reset –mixed: that will uncommit and move to previous commit 
•	 git reset --soft: it will uncommit, but file will be in staging 
•	 git reset --hard: it will uncommit, remove from stage, remove from local repo
