# Microsoft Az-400 (Adrián Arenilla Seco)

## Lab 16: Deploying a multi-container application to Azure Kubernetes Services
In this lab, you will use Azure DevOps to deploy a containerized ASP.NET Core web application MyHealthClinic (MHC) to an AKS cluster.

### [Go to lab instructions -->](AZ400_M16_Deploying_multi-container_application_to_Azure_Kubernetes_Services.md)


Select the checkbox below the Kubernetes extension to install the extension into the project.
![](Evidences/Image1.png)


Project created successfully.
![](Evidences/Image2.png)


Run the code to identify the latest version of Kubernetes available in the Azure region and run the code to create a resource group that will host the AKS deployment.
![](Evidences/Image3.png)


Run the code to create an AKS cluster using the latest version available.
![](Evidences/Image4.png)


Run the code to create the logical server to host the Azure SQL database.
![](Evidences/Image5.png)


Run the code to allow access from Azure to the newly provisioned logical server (sql server firewall-rule), run the code to create the Azure SQL database (sql db create) and run the code to create the Azure Container registry.
![](Evidences/Image6.png)


Run the code to grant the AKS-generated managed identity to access to the newly created ACR.
![](Evidences/Image7.png)


Run the code to display the name of logical server hosting the Azure SQL and run the code to display the name of the login server of the Azure Container registry.
![](Evidences/Image8.png)


Set up the options of pipeline.
![](Evidences/Image9.png)


Set up the options of pipeline.
![](Evidences/Image10.png)


Change the values of variables into pipeline. 
![](Evidences/Image11.png)


Set up the options of release pipeline.
![](Evidences/Image12.png)


Set up the options of release pipeline.
![](Evidences/Image13.png)


Set up the options of release pipeline.
![](Evidences/Image14.png)


Set up the options of release pipeline.
![](Evidences/Image15.png)


Set up the options of release pipeline.
![](Evidences/Image16.png)


Set up the options of release pipeline.
![](Evidences/Image17.png)


Set up the options of release pipeline.
![](Evidences/Image18.png)


Change the values of variables into release pipeline. 
![](Evidences/Image19.png)


Run pipeline.
![](Evidences/Image20.png)


Monitor its progress and verify that it completes successfully.
![](Evidences/Image21.png)


Verify that the AKS is created and running correctly.
![](Evidences/Image22.png)


Verify that the Kubernetes services are operational and go to the IP.
![](Evidences/Image23.png)


Verify that the page opens correctly on the IP address.
![](Evidences/Image24.png)


On the Azure Container registry blade, in the Services section, click Repositories and verify that the list of repositories includes the myhealth.web entry.
![](Evidences/Image25.png)


Monitor its progress and verify that it completes successfully.
![](Evidences/Image26.png)


Run the code to gain access to the AKS cluster.
![](Evidences/Image27.png)


Run the code to list the pods running in AKS that were deployed by using the release pipeline (kubectl get pods) and run the code to list the load balancer service that provides an external IP address via which you can access the containerized application (kubectl get service).
![](Evidences/Image28.png)


List the resource groups created in the lab for this module by running the following command:
```
az group list --query "[?starts_with(name,'az400m16l01a-RG')].name" --output tsv
```

Delete the resource groups that you created in the lab for this module by executing the following command:
```
az group list --query "[?starts_with(name,'az400m16l01a-RG')].[name]" --output tsv | xargs -L1 bash -c 'az group delete --name $0 --no-wait --yes'
```
![](Evidences/Image29.png)


### [<-- Back to readme](../README.md)

