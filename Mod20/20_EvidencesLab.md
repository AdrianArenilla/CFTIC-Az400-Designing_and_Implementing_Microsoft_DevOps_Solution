# Microsoft Az-400 (Adrián Arenilla Seco)

## Lab 20: Managing technical debt with SonarCloud and Azure DevOps
In this lab, you will learn how to integrate Azure DevOps Services with SonarCloud.

### [Go to lab instructions -->](AZ400_M20_Managing_technical_debt_with_SonarQube_and_Azure_DevOps.md)


Create a new DevOps project.
![](Evidences/Image1.png)


Choose the name and the visibility and click on create.
![](Evidences/Image2.png)


Import a Git repository.
![](Evidences/Image3.png)


Verify that the import is successful.
![](Evidences/Image4.png)


Create a new personal access token (PAT).
![](Evidences/Image5.png)


Get the SonarCloud extension from the Visual Studio Marketplace.
![](Evidences/Image6.png)


Install within your DevOps organization.
![](Evidences/Image7.png)


Log in with Azure DevOps.
![](Evidences/Image8.png)


Choose import an organization from Azure.
![](Evidences/Image9.png)


Review the data an click on Create Organization.
![](Evidences/Image10.png)


Choose the DevOps project and click on Set Up.
![](Evidences/Image11.png)


Continue to install the extension and view all data from the project.
![](Evidences/Image12.png)


Create a new pipeline.
![](Evidences/Image13.png)


Create a new service connection.
![](Evidences/Image14.png)


Choose SonarCloud to connect to it.
![](Evidences/Image15.png)


Verify that the SonarCloud token is valid and choose a service connection name.
![](Evidences/Image16.png)


Modify the azure-pipelines.yml file and click on Save and run.
![](Evidences/Image17.png)


Monitor its progress and verify that it completes successfully. 
![](Evidences/Image18.png)


Create a new pipeline but now choose classic editor.
![](Evidences/Image19.png)


The source is Azure Repos Git and check the rest of the options and Continue.
![](Evidences/Image20.png)


Choose .NET Desktop with SonarCloud template and Apply.
![](Evidences/Image21.png)


Create a new service connection within the task Prepare analysis on SonarCloud verifying the SonarCloud token.
![](Evidences/Image22.png)


Set up the options of pipeline. 
![](Evidences/Image23.png)


Monitor its progress and verify that it completes successfully. 
![](Evidences/Image24.png)


To be able to see the Quality gate result, after running he first report we need to set New Code Definition. This way, subsequent pipeline runs will include Quality Gate results.
![](Evidences/Image25.png)


Choose Previous version.
![](Evidences/Image26.png)


Monitor its progress and verify that it completes successfully. 
![](Evidences/Image27.png)


Monitor its progress and verify that it completes successfully. 
![](Evidences/Image28.png)


Verify that the report now includes the Quality Gate result and click the number designating the count of Bugs.
![](Evidences/Image29.png)


Review the error details in line number 9 of Program.cs file, including the recommendation stating Change this condition so that it does not always evaluate to 'true'; some subsequent code is never executed.
![](Evidences/Image30.png)


Configure pull request integration in SonarCloud by assigning an Azure DevOps personal access token to your SonarCloud project.
![](Evidences/Image31.png)


Configure pull request integration in SonarCloud.
![](Evidences/Image32.png)


Configure pull request integration in SonarCloud.
![](Evidences/Image33.png)


On the **Program.cs** pane, add the following empty method to the code directly above the line `public static bool AlwaysReturnsTrue()` and Commit.
```
public void Unused(){}
```
![](Evidences/Image34.png)


Choose a new branch name and Commit.
![](Evidences/Image35.png)


Monitor its progress and verify that it completes successfully. 
![](Evidences/Image36.png)


Review the results of the SonarCloud checks and close the pane.
![](Evidences/Image37.png)


Block pull requests in response to failing Code Quality checks.
![](Evidences/Image38.png)


Click on complete to join the branches.
![](Evidences/Image39.png)


### [<-- Back to readme](../README.md)

