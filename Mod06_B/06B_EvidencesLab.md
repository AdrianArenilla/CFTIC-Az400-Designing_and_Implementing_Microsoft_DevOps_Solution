# Microsoft Az-400 (Adrián Arenilla Seco)

## Lab 06B: Integrating External Source Control with Azure Pipelines
In this lab, you’ll see how easy it is to set up Azure Pipelines with your GitHub projects and how you can start seeing benefits immediately.

### [Go to lab instructions -->](AZ400_M06_Integrating_External_Source_Control_with_Azure_Pipelines.md)


Install Azure Pipelines on GitHub.
![](Evidences/Image1.png)


Complete the installation.
![](Evidences/Image2.png)


Install Azure Pipelines in all repositories.
![](Evidences/Image3.png)


Grant permissions.
![](Evidences/Image4.png)


Configure the Azure Pipelines project based on the fork of the GitHub repo.
![](Evidences/Image5.png)


ERROR!!
![](Evidences/Image6.png)


The project is now private and the job is completed correctly. 
![](Evidences/Image7.png)


Project public vs. project private errors.
![](Evidences/Image8.png)


Change visibility for errors.
![](Evidences/Image9.png)


GitHub project repo hosting the fork.
![](Evidences/Image10.png)


Modification of the file "azure-pipelines.yml".
![](Evidences/Image11.png)


Check that the job is completed correctly. 
![](Evidences/Image12.png)


Modification of the file "arithmeticController.js".
![](Evidences/Image13.png)


Error into the code.
![](Evidences/Image14.png)


Error into the job in Azure DevOps portal.
![](Evidences/Image15.png)


The error indicates that in the test the numbers are concatenated instead of being added.
![](Evidences/Image16.png)


Edit the file to solve the error.
![](Evidences/Image17.png)


Modification of the file "arithmeticController.js".
![](Evidences/Image18.png)


The new code is correct.
![](Evidences/Image19.png)


Check that the job is completed correctly. 
![](Evidences/Image20.png)


Add badge to the file "readme.md"
![](Evidences/Image21.png)


Badge added successfully.
![](Evidences/Image22.png)


[![Build Status](https://dev.azure.com/AdrianArenilla/06b-Integrating%20External%20Source%20Control%20with%20Azure%20Pipeline/_apis/build/status/AdrianArenilla.calculator?branchName=master)](https://dev.azure.com/AdrianArenilla/06b-Integrating%20External%20Source%20Control%20with%20Azure%20Pipeline/_build/latest?definitionId=12&branchName=master)

### [<-- Back to readme](../README.md)

