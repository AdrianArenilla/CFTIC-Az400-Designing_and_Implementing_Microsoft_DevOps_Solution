# Microsoft Az-400 (Adrián Arenilla Seco)

## Lab 07: Integrating Azure Key Vault with Azure DevOps
In this lab, you will learn how you can integrate Azure Key Vault with an Azure DevOps pipeline.

### [Go to lab instructions -->](AZ400_M07_Integrating_Azure_Key_Vault_with_Azure_DevOps.md)


Project created successfully.
![](Evidences/Image1.png)


Run the following command to create a service principal:
```
az ad sp create-for-rbac --name <service-principal-name>
```

Run the following commands to retrieve the values of the Azure subscription ID and subscription name attributes: 
```
az account show --query id --output tsv
az account show --query name --output tsv
```
![](Evidences/Image2.png)


Key vault created.
![](Evidences/Image3.png)


Create a new policy on key vault.
![](Evidences/Image4.png)


Run pipeline SmartHotel-CouponManagement-CI.
![](Evidences/Image5.png)


Edit SmartHotel-CouponManagement-CD.
![](Evidences/Image6.png)


Create a new connection service.
![](Evidences/Image7.png)


Complete and verify the required lab fields.
![](Evidences/Image8.png)


Verify that Azure Key Vault is correct.
![](Evidences/Image9.png)


Verify that Azure Deployment is correct.
![](Evidences/Image10.png)


Verify that Azure App Service Deploy is correct and save.
![](Evidences/Image11.png)


Create new release.
![](Evidences/Image12.png)


If everything is correct, click on Create.
![](Evidences/Image13.png)


Make sure your pipeline runs successfully and has finished.
![](Evidences/Image14.png)


Make sure your pipeline runs successfully and has finished.
![](Evidences/Image15.png)


Verify the resources within the resource group.
![](Evidences/Image16.png)


Login to the website.
![](Evidences/Image17.png)


Test any coupon to verify operation.
![](Evidences/Image18.png)


See the results.
![](Evidences/Image19.png)



List the resource groups created in the lab for this module by running the following command:
```
az group list --query "[?starts_with(name,'az400m07l01-RG')].name" --output tsv
```

Delete the resource groups that you created in the lab for this module by executing the following command:
```
az group list --query "[?starts_with(name,'az400m07l01-RG')].[name]" --output tsv | xargs -L1 bash -c 'az group delete --name $0 --no-wait --yes'
```
![](Evidences/Image20.png)


### [<-- Back to readme](../README.md)

