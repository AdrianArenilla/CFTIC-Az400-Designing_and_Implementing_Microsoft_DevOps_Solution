# Microsoft Az-400 (Adrián Arenilla Seco)

## Lab 11B: Setting Up and Running Functional Tests
In this lab, you will learn how to execute Selenium test cases on a C# web application, as part of the Azure DevOps Release pipeline.

### [Go to lab instructions -->](AZ400_M11_Setting_Up_and_Running_Functional_Tests.md)


Project created successfully.
![](Evidences/Image1.png)


Create Azure resources from custom deployment.
![](Evidences/Image2.png)


Review all resources created with the template.
![](Evidences/Image3.png)


Connection to RDP.
![](Evidences/Image4.png)


Configure a self-hosted Azure DevOps agent.
![](Evidences/Image5.png)


Edit a release pipeline.
![](Evidences/Image6.png)


Set up the options of release pipeline Selenium.
![](Evidences/Image7.png)


Set up the options of release pipeline Selenium.
![](Evidences/Image8.png)


Set up the options of release pipeline Selenium.
![](Evidences/Image9.png)


Run pipeline.
![](Evidences/Image10.png)


Monitor its progress and verify that it completes successfully.
![](Evidences/Image11.png)


Review the deployed site.
![](Evidences/Image12.png)


Monitor its progress and verify that it completes successfully.
![](Evidences/Image13.png)


Review test statistics.
![](Evidences/Image14.png)


List the resource groups created in the lab for this module by running the following command:
```
az group list --query "[?starts_with(name,'az400m11l02-RG')].name" --output tsv
```

Delete the resource groups that you created in the lab for this module by executing the following command:
```
az group list --query "[?starts_with(name,'az400m11l02-RG')].[name]" --output tsv | xargs -L1 bash -c 'az group delete --name $0 --no-wait --yes'
```
![](Evidences/Image15.png)


### [<-- Back to readme](../README.md)

