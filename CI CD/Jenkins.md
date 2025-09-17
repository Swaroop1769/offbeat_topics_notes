JENKINS:


--> one of the most popular DevOps tools.
--> Key DevOps CI/CD tool
--> automate builds and deployments
--> Open source with 1400 plugins



In real world, we use in industry Declarative Pipelines - we configure jenkins pipeline using Code.


Jenkins---becomes popular when it comes to AUTOMATION and CI/CD.

In devops we have developers who build apps.

Example: consider the JAVA application
consider CI (Continuous Integration):
dev --> code --> Build --> Test

dev(developer) -----> Code (commit using Github 
                    or BitBucket)------> Build(We could do that on local machine but it's inefficient. So where Jenkins comes - we take these steps into a pipeline and dev will commit their change, goes to code, and jenkins will automatically scan for new commits. When new commit is picked up, it will start a build.)-----> Test (as a part of CI we ask jenkins to create this step in a pipeline as well.Go ahead and test what we've build)

Key part of this is we're now automating this Process.
So if the test fails, developer commits the change so that the test stage passes.

Let's have a look at CD (Continuous Delivery):

DevOps engineers gets involved at CD stages:

CD ---> Build Docker Image --> push it upto a Repository ---> add it to Kubernetees file --->  and then Deploy it.

But with Jenkins we can AUTOMATE the entire process.

So if test passed, start the build, push and deploy.
Rather than doing manually we now have fast-track way of doing this.

The main advantage of Jenkins is we can configure the pipelines and have a completely automated process.

CI/CD is popular as it massively speeds up the development process.

We can also have Jenkins used for numerous ways:

as an automated platform to schedule cleanups.
we can have it for deploying releases.
we can have it for building standalone applications (so CI)


Reason for Docker:


we use Docker as a platform to install Jenkins. The 2 reasons are:

it gives us a standard platform regardless of what OS you're on!
it speeds up the installation process enormously.

After the installation of Jenkins using Docker Desktop, Docker Toolbox and running the following command you will be getting one password, save it somewhere on Notepad. 
docker run -p 8080:8080 -p 50000:50000 --restart=on-failure jenkins/jenkins:lts-jdk17

And then open your Browser and type - localhost:8080 and click Enter.
Now the Jenkins will ask us what plugins needs to be installed - choose Suggested one's and Click Enter. After that click on Sign in using Admin user.

Now you'll see the Jenkins installed.
To  Create New jobs:
Different options - 
Freestyle project is most common one to use. It's like a blank slate we can create whatever we want.
Pipeline is an other option. Where we have different phases Build, Test, Deploy
Multi Configuration Project: If we have a project and we need to run the same job,but will slightly different parameters
GitHub Organization: Multi-Branch Pipeline are incredibly powerful. Advantage of multi branch pipeline is if we have multiple branches - we can have one job that runs on every different branch.


Click on the Freestyle project for creating a sample job:
Now type an echo command for basic job and save it later on Build it.


To create a sample pipeline, this time choose the pipeline option and Give a name to your pipeline 
Build Triggers: The two most popular ones in Build Triggers are - Poll SCM and Build Periodically
Basically build triggers tells when to run a job and the reason why poll SCM and Build Periodically are popular are
With Build periodically you can set an interval of when to build it. For example if you are having a clean up job (operations Engineers looks at) let's say we start a deployment in morning and tear down at evening 7'o clock. So that' something like a periodically or maybe a clean up job-every hour we might have to clear something down.
Poll SCM: it will look at our Source code management,say it to be Github of Bitbucket. And if a developer makes a change