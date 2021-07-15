# Microsoft Az-400 (Adrián Arenilla Seco)

## Lab 05: Configuring Agent Pools and Understanding Pipeline Styles
In this lab, you will step through the process of converting a classic pipeline into a YAML-based one and running it first by using a Microsoft-hosted agent and then performing the equivalent task by using a self-hosted agent.

### [Go to lab instructions -->](AZ400_M05_Configuring_Agent_Pools_and_Understanding_Pipeline_Styles.md)


Project created successfully.
![](Evidences/Image1.png)


Create new pipeline.
![](Evidences/Image2.png)


New pipeline created.
![](Evidences/Image3.png)


Go to Edit option into PartsUnlimitedE2E.yml
![](Evidences/Image4.png)


Uncheck the "Enable continuous integration" box.
![](Evidences/Image5.png)


Inside PartsUnlimitedE2E.yml go to options to export to .yml
![](Evidences/Image6.png)


Go to PartsUnlimitedE2E.yml options to edit.
![](Evidences/Image7.png)


Replace the old code.
![](Evidences/Image8.png)


Paste the new code.
![](Evidences/Image9.png)


Check that the job is completed correctly.
![](Evidences/Image10.png)


Go to Azure DevOps organization to enter Personal access tokens option.
![](Evidences/Image11.png)


Create a new personal access token.
![](Evidences/Image12.png)


Add agent pool.
![](Evidences/Image13.png)


Add agent pool.
![](Evidences/Image14.png)


Into agent poll create a new agent.
![](Evidences/Image15.png)


Open PowerShell Administrator into the folder and execute the script "config.cmd".
![](Evidences/Image16.png)


Verify that the new agent is online.
![](Evidences/Image17.png)


Edit the code so that it displays like the image.
![](Evidences/Image18.png)


Edit the .yml file and modify Nuget settings.
![](Evidences/Image19.png)


Verify that the file has been modified correctly.
![](Evidences/Image20.png)


Check that the job is completed correctly.
![](Evidences/Image21.png)


Pipeline correctly executed.
![](Evidences/Image22.png)


### [<-- Back to readme](../README.md)

