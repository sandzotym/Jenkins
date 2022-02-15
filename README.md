# Jenkins

- CI - Build, Test, Code Coverage, Docker Image
- CD - Deploy, Push Docker Images to DockerHub

Install Jenkins & see it running default at localhost:8080

**Create Job for Build on Commit & Dockerize**
- Create New Job
- Name the Project
- Freestyle Project
- Github Project (URL)
- SCM (.git URL from Clone & Download Button)
- Schedule (* * * * *) for Build on Commit
- Build - invoke top level Maven targets, Goals - install
- Apply & Save

**How to Add Docker Plugin to Jenkins**
Jenkins - Manage Jenkins - Manage Plugins - Available (Cloudbees, Docker Plugin & docker-build-step)
then Jenkins Home - <Project> - Configure - Build (Add Build Step i.e. build/Docker Build & Publish - provide repoName as <DockerID>/<imageName> & registry Credentials as configured below for DockerHub)

**How to Add DockerHub Credentials to Jenkins**

Go to Credentials → Global → Add credentials, and fill out the form with your username and password. Fill in ID and Descriptions. Note that if you set the ID, you will need this specific ID to refer this credential from your scripts. Here we are just using dockerhub_id.

![image](https://user-images.githubusercontent.com/93154062/153647993-345ce6bb-521c-4e54-9378-7c599ce822ff.png)

**How to Configure Maven to Jenkins**

Go to Global Jenkins Configuration at http://localhost:8080/configureTools/

![image](https://user-images.githubusercontent.com/93154062/153914332-db0aee8d-e584-40b8-80fd-7993a507dfdd.png)

Then go to your Project. Inside settings/configure -> build. Select Maven which you have created as above.

![image](https://user-images.githubusercontent.com/93154062/153914407-053c137e-6e9e-425f-871a-a006b6addfe4.png)

**How to provide Compiler to Jenkins**

Go to Global Jenkins Configuration at http://localhost:8080/configureTools/
- Click "JDK installations" under JDK
- Uncheck Install Automatically
- Provide path to the JDK under JAVA_HOME field.

![image](https://user-images.githubusercontent.com/93154062/153915362-3ea5be68-a64a-4802-bd67-8beb0b62812c.png)
