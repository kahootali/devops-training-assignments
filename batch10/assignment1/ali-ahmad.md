# - Agile vs DevOps:
Key Difference Between Agile and DevOps
DevOps is a practice of bringing development and operations teams together whereas Agile is an iterative approach that focuses on collaboration, customer feedback and small rapid releases.
DevOps focuses on constant testing and delivery while the Agile process focuses on constant changes.
DevOps requires relatively a large team while Agile requires a small team.
DevOps leverages both shifts left and right principles, on the other hand, Agile leverage shift-left principle.
The target area of Agile is Software development whereas the Target area of DevOps is to give end-to-end business solutions and fast delivery.
DevOps focuses more on operational and business readiness whereas Agile focuses on functional and non-function readiness.
# - Define CI, Continuous Delivery & Continuous Deployment:
Continuous integration:
Developers practicing continuous integration merge their changes back to the main branch as often as possible. The developer's changes are validated by creating a build and running automated tests against the build. By doing so, you avoid integration challenges that can happen when waiting for release day to merge changes into the release branch.

Continuous integration puts a great emphasis on testing automation to check that the application is not broken whenever new commits are integrated into the main branch.

Continuous delivery:
Continuous delivery is an extension of continuous integration since it automatically deploys all code changes to a testing and/or production environment after the build stage. 

This means that on top of automated testing, you have an automated release process and you can deploy your application any time by clicking a button.

In theory, with continuous delivery, you can decide to release daily, weekly, fortnightly, or whatever suits your business requirements. However, if you truly want to get the benefits of continuous delivery, you should deploy to production as early as possible to make sure that you release small batches that are easy to troubleshoot in case of a problem.
# - What are the benefits of Cloud Computing:
Benefits of cloud computing:
Cloud computing offers your business many benefits. It allows you to set up what is essentially a virtual office to give you the flexibility of connecting to your business anywhere, any time. With the growing number of web-enabled devices used in today's business environment (e.g. smartphones, tablets), access to your data is even easier.

There are many benefits to moving your business to the cloud:

Reduced IT costs:
Moving to cloud computing may reduce the cost of managing and maintaining your IT systems. Rather than purchasing expensive systems and equipment for your business, you can reduce your costs by using the resources of your cloud computing service provider. You may be able to reduce your operating costs because:

the cost of system upgrades, new hardware and software may be included in your contract
you no longer need to pay wages for expert staff
your energy consumption costs may be reduced
there are fewer time delays.
Scalability:
Your business can scale up or scale down your operation and storage needs quickly to suit your situation, allowing flexibility as your needs change. Rather than purchasing and installing expensive upgrades yourself, your cloud computer service provider can handle this for you. Using the cloud frees up your time so you can get on with running your business.

Business continuity:
Protecting your data and systems is an important part of business continuity planning. Whether you experience a natural disaster, power failure or other crisis, having your data stored in the cloud ensures it is backed up and protected in a secure and safe location. Being able to access your data again quickly allows you to conduct business as usual, minimising any downtime and loss of productivity.

Collaboration efficiency:
Collaboration in a cloud environment gives your business the ability to communicate and share more easily outside of the traditional methods. If you are working on a project across different locations, you could use cloud computing to give employees, contractors and third parties access to the same files. You could also choose a cloud computing model that makes it easy for you to share your records with your advisers (e.g. a quick and secure way to share accounting records with your accountant)
# - Difference b/w Git & Github:
Git: Git is a distributed version control system for tracking changes in source code during software development. It is designed for coordinating work among programmers, but it can be used to track changes in any set of files. Its goals include speed, data integrity, and support for distributed, non-linear workflows. 

GitHub: GitHub is a web-based Git repository hosting service, which offers all of the distributed revision control and source code management (SCM) functionality of Git as well as adding its own features. 
# - Stages of Git:
• Modified:
So, going back to our example, we saw that, those students have messed up their project. So, under Git we can create a repository, a repository is basically a kind of a directory that contains all the files related to your code. So, in the repository we can write code, and maintain it. Once, the code is written, anyone willing to make some modification can make those changes in their own remote repository. A remote repository is a local copy (one that you create on your local machine) of the original project that is being maintained via Git. So, basically you can make changes to your copy of the project without hampering the original code. This is called Modification, i.e. making some additions to the original project.

• Staged:
In the previous section we learnt about modification, now let’s look at the second stage in Git, i.e. staged. So, we saw that we can make changes to the project without hampering the original version, but how do we apply those changes to our remote repository? So, we use the commands in the Git command line — git add. So, this command tracks the new changes and pushes it to the staging area. So, staging area is place prior to the actual implementation of changes, i.e. this area contains all the added files that contain new code, which are ready to be joined to the remote repository. So, all the new files are first pushed to the staging area. This can also be understood with an analogy. We all must have participated in a race or some sort of athletic event. Before, the race begins, we hear three words, Get, Set…, Go! Now, we can think of ‘Set’ as the staging area. So, this is an indication that make yourself ready, as the race is about to start. Similarly, staging area is a place where all the new files are finally ready to be joined to the remote repository.

• Commit:
This is the final stage, as this stage finally applies the new changes to the remote repository. Looking at the previous analogy, this is your ‘Go’ position. So, a commit is a set of new files that are being added to a project as part of the modification. Each commit represents the changes made to project in the past, with the details about the time at which commit was made and the author of the code. So, finally when you make a commit, and it gets committed, then this simply means that you have successfully applied a certain modification to the code.
# - 3 methods of git reset?
The inner workings of git reset
I like to think of git reset as a command that reverses the process described above (introducing a change to the working dir, adding it to the index, and then commiting it to the repository).

Git reset has three operating modes — --soft, --mixed, or --hard. I see them as three stages:

Stage 1 — update HEAD — git reset --soft
Stage 2 — update index — git reset --mixed
Stage 3 — update working dir — git reset --hard