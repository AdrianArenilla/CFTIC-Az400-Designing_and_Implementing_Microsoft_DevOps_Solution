# Microsoft Az-400 (Adrián Arenilla Seco)

## Lab 14B: Automating infrastructure deployments in the Cloud with Terraform and Azure Pipelines
In this lab, you will learn how to incorporate Terraform into Azure Pipelines for implementing Infrastructure as Code.

### [Go to lab instructions -->](AZ400_M14_Automating_infrastructure_deployments_in_the_Cloud_with_Terraform.md)


Select the checkbox below the Replace Tokens and Terraform labels to install extensions.
![](Evidences/Image1.png)


Project created successfully.
![](Evidences/Image2.png)


Switch from the master branch to the terraform branch.
![](Evidences/Image3.png)


Run pipeline.
![](Evidences/Image4.png)


Monitor its progress and verify that it completes successfully.
![](Evidences/Image5.png)


On the Artifacts pane, verify that it contains the PartsUnlimitedwebsite.zip file, then expand its Terraform subfolder, and verify that it includes the webapp.tf file.
![](Evidences/Image6.png)


Update all tasks, save and create release.
![](Evidences/Image7.png)


Select the version to the _Terraform-CI.
![](Evidences/Image8.png)


Monitor its progress and verify that it completes successfully.
![](Evidences/Image9.png)


After deploying the tubing once, deploy again.
![](Evidences/Image10.png)


Verify within the azure portal that the app service has been created correctly.
![](Evidences/Image11.png)


Displaying the newly deployed web application.
![](Evidences/Image12.png)


List the resource groups created in the lab for this module by running the following command:
```
az group list --query '[?contains(`["terraformrg", "PULTerraform"]`, name)].name' --output tsv
```

Delete the resource groups that you created in the lab for this module by executing the following command:
```
az group list --query '[?contains(`["terraformrg", "PULTerraform"]`, name)].name' --output tsv | xargs -L1 bash -c 'az group delete --name $0 --no-wait --yes'
```
![](Evidences/Image13.png)


### [<-- Back to readme](../README.md)

