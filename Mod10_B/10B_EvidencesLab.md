# Microsoft Az-400 (Adrián Arenilla Seco)

## Lab 10B: Creating a Release Dashboard
In this lab, you will learn how to create a release dashboard and use the REST API to retrieve release data from Azure DevOps.

### [Go to lab instructions -->](AZ400_M10_Creating_a_Release_Dashboard.md)


Create an Azure DevOps Starter resource.
![](Evidences/Image1.png)


Create an Azure DevOps Starter resource.
![](Evidences/Image2.png)


Create an Azure DevOps Starter resource.
![](Evidences/Image3.png)


Create an Azure DevOps Starter resource.
![](Evidences/Image4.png)


On the DevOps Starter blade, track the progress of CI/CD pipeline until it completes successfully.
![](Evidences/Image5.png)


Edit the file Index.cshtml and Commit the changes.
![](Evidences/Image6.png)


Make sure your pipeline runs successfully and has finished.
![](Evidences/Image7.png)


Make sure your pipeline runs successfully and has finished.
![](Evidences/Image8.png)


Edit the file Index.cshtml and Commit the changes.
![](Evidences/Image9.png)


Now, the pipeline will fail. The failure will be caused by the built-in assembly test, which considers the change associated with the new version to be invalid.
![](Evidences/Image10.png)


Create an Azure DevOps release dashboard.
![](Evidences/Image11.png)


Generate an Azure DevOps personal access token.
![](Evidences/Image12.png)


Query release information via REST API by using Postman.
![](Evidences/Image13.png)


Query release information via REST API by using Postman.
![](Evidences/Image14.png)


Query release information via REST API by using Postman.
![](Evidences/Image15.png)


On the DevOps Starter blade, track the progress of CI/CD.
![](Evidences/Image16.png)


List the resource groups created in the lab for this module by running the following command:
```
az group list --query "[?starts_with(name,'az400m10l02-rg')].name" --output tsv
```

Delete the resource groups that you created in the lab for this module by executing the following command:
```
az group list --query "[?starts_with(name,'az400m10l02-rg')].[name]" --output tsv | xargs -L1 bash -c 'az group delete --name $0 --no-wait --yes'
```
![](Evidences/Image17.png)


### [<-- Back to readme](../README.md)

