# Jenkins

**How to Add DockerHub Credentials to Jenkins**

Go to Credentials → Global → Add credentials, and fill out the form with your username and password. Fill in ID and Descriptions. Note that if you set the ID, you will need this specific ID to refer this credential from your scripts. Here we are just using dockerhub_id.

![image](https://user-images.githubusercontent.com/93154062/153647993-345ce6bb-521c-4e54-9378-7c599ce822ff.png)

**How to Configure Maven to Jenkins**

Go to Global Jenkins Configuration at http://localhost:8080/configureTools/

![image](https://user-images.githubusercontent.com/93154062/153914332-db0aee8d-e584-40b8-80fd-7993a507dfdd.png)

Then go to your Project. Inside settings/configure -> build. Select Maven which you have created as above.

![image](https://user-images.githubusercontent.com/93154062/153914407-053c137e-6e9e-425f-871a-a006b6addfe4.png)
