# Microsoft Az-400 (Adrián Arenilla Seco)

## Lab 11A: Configuring Pipelines as Code with YAML
In this lab, you will learn how to configure pipelines using YAML.

### [Go to lab instructions -->](AZ400_M11_Configuring_Pipelines_as_Code_with_YAML.md)


Project created successfully.
![](Evidences/Image1.png)


Create Web App + SQL resource.
![](Evidences/Image2.png)


Create Web App + SQL resource.
![](Evidences/Image3.png)


Delete PartsUnlimited pipeline.
![](Evidences/Image4.png)


Delete the azure-pipelines.yml file.
![](Evidences/Image5.png)


Create a new pipeline and update the azure-pipelines.yml file created.
![](Evidences/Image6.png)


Monitor its progress and verify that it completes successfully.
![](Evidences/Image7.png)


Review test statistics.
![](Evidences/Image8.png)


Add continuous delivery to the YAML definition.
![](Evidences/Image9.png)


Azure app service deploy added to azure-pipelines.yml file.
![](Evidences/Image10.png)


The pipeline will look similar to this example.
![](Evidences/Image11.png)


Allow access to the pipeline to access the requested resource.
![](Evidences/Image12.png)


Click on Permit the access.
![](Evidences/Image13.png)


Once the task completes, your app will be deployed to an Azure web app.
![](Evidences/Image14.png)


Edit the connection string in the Azure portal of the App Service.
![](Evidences/Image15.png)


Review the deployed site.
![](Evidences/Image16.png)


List the resource groups created in the lab for this module by running the following command:
```
az group list --query "[?starts_with(name,'az400m11l01-RG')].name" --output tsv
```

Delete the resource groups that you created in the lab for this module by executing the following command:
```
az group list --query "[?starts_with(name,'az400m11l01-RG')].[name]" --output tsv | xargs -L1 bash -c 'az group delete --name $0 --no-wait --yes'
```
![](Evidences/Image17.png)


### [<-- Back to readme](../README.md)

