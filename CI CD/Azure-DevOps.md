Azure Boards are like To-do list

Story - a specific way of defining the tasks

Azure Boards has 5 components:

Work Items
Boards
Backlogs
Sprints
Dashboards

Boards work processes:
Basic
Agile
Scrum
Capability Maturity Model Integration (CMMI)

Basic Workflow:

To-Do
Doing
Done

Work Items tab or commanly called Blade (blade is more often associated with the Azure management website)

Sprint: a short, time-boxed period when a team completes a planned amount of work.

Can plan sprints using Azure DevOps Boards.

Build: WHAT gets BUILD (The What)
Release: The WHERE 

Pipeline --> Phases --> Tasks ==> Agents Agents

Jobs carried out in tasks stage is by AGENTS (Microsoft Managed Agents)

Agents can be grouped into one or more --> Agent Pool


YAML is commonly called "Configuration as a Code"


Azure DevOps Services:
    - Boards : track work
    - Pipelines : Build & Deploy
    - Repos : Cloud-based Source Control
    - Test Plans : Used to Test Apps
##Integration & Extensions:
    - Slack
    - Trello
    - Campfire
    - GitHub
## Azure Boards Components
    - Work Items
    - Boards
    - Backlogs
    - Sprint
    - Dashboards
Board Work Process:
Basic: simplest model that uses Taks, Epics to track work
Agile:  planning methods, including scrum, and track development and test activities separately.
Scrum: team practices Scrum
CMMI:  Capability Maturity Model Integration
More formal project methods that require a framework for process improvement and an auditable records of decisions.

Work Flow:   simply Kanban Board ==> To Do   | Doing   | DONE

Sprint: is a short, time-boxed period when a scrum team works to complete a set amount of work
E.g.: 2 week sprint
Tasks:
    1. Create Application server
    2. Create Database server
##Queries: useful to identify certain data around the work items. Helpful for planner or project manager.
    - Bulk Update, assign or reassign
    - Email list of work items
    - Reporting Feature

##Azure Repos: 

Azure Repos are similar to GitHub Repos - a place to store the code base.
    - Centralized place to store code base where multiple people can collaborate and work on a single code base.
    - Support features like creating pull request, merging pull requests, creating branch managing files etc.

What is version control system?
    - To manage code at a centralized place and track all changes done or team has done.
    - Collaboration
    - Storing versions (properly) saving a version of your project after making changes
    - Restoring previous versions
    - Understanding what happened.
    - Backup!!
Types of version control:
    1. Git = Distributed
    2. TFVC (Team Foundation Version Control) = centralized
 

Git Terminology:
    - Branches: copy of master or some other branch
    - Commit: snapshot of project's currently staged changes
    - Pull Request: way to tell and merge changes of one branch to other.

##Azure Pipelines:

CI/CD:
    - Continuous Integration
    - Continuous Delivery/Deployment
    - Pipelines - CI/CD happens

Azure Pipelines:
    - Execution of continuous integration takes place
    - Builds or Run Job/task when code is submitted
    - Build Agent - helps to build the code
    - Outputs a build artifact (.zip file, .jar file, .exe)

Can be classified into Build vs Release pipeline:

Build:
Code --> Steps --> Artifact
Release:
Test --> Staging --> Production