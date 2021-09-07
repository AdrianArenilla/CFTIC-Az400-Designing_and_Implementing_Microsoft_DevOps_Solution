# Microsoft Az-400 (Adrián Arenilla Seco)

## Lab 10A: Controlling Deployments using Release Gates
In this lab, you will learn about configuring Azure deployment gates.

### [Go to lab instructions -->](AZ400_M10_Controlling_Deployments_using_Release_Gates.md)


Project created successfully.
![](Evidences/Image1.png)


Run the following command to create a resource group.
```
RESOURCEGROUPNAME="az400m10l01-RG"
az group create -n $RESOURCEGROUPNAME -l "<westeurope>""
```
![](Evidences/Image2.png)


To create an App service plan.
```
SERVICEPLANNAME="az400m01l01-sp1"
az appservice plan create -g $RESOURCEGROUPNAME -n $SERVICEPLANNAME --sku S1
```
![](Evidences/Image3.png)


Create web apps with unique app names.
```
SUFFIX=$RANDOM$RANDOM
az webapp create -g $RESOURCEGROUPNAME -p $SERVICEPLANNAME -n PU$SUFFIX-Canary
```
![](Evidences/Image4.png)


Create web apps with unique app names.
```
az webapp create -g $RESOURCEGROUPNAME -p $SERVICEPLANNAME -n PU$SUFFIX-Prod
```
![](Evidences/Image5.png)


Navigate to the resource group az400m10l01-RG and review the resources you created.
![](Evidences/Image6.png)


On the Application Insights blade, click Turn on Application Insights, accept the default settings, and click Apply to create and connect Application Insights resource to your Canary web app.
![](Evidences/Image7.png)


Create alert rule blade, in the Condition section.
![](Evidences/Image8.png)


Create alert rule blade, in the Condition section.
![](Evidences/Image9.png)


On the Pipeline tab, in the Artifacts rectangle, click the Continuous deployment trigger button.
![](Evidences/Image10.png)


Update the data of the Canary environment pipeline.
![](Evidences/Image11.png)


Update the data of the Production environment pipeline.
![](Evidences/Image12.png)


Run pipeline.
![](Evidences/Image13.png)


Verify that the pipeline has been done correctly (CI).
![](Evidences/Image14.png)


Track the progress of the release and verify that the deployment to both web apps completed successfully.
![](Evidences/Image15.png)


Verify that the web page loads successfully (Canary environment).
![](Evidences/Image16.png)


Verify that the web page loads successfully (Production environment).
![](Evidences/Image17.png)


Configure pre-deployment gates.
![](Evidences/Image18.png)


Select the project name and set the Read permission to Allow.
![](Evidences/Image19.png)


Configure post-deployment gates.
![](Evidences/Image20.png)


If the result is Fail, wait for the next evaluation. 

This indicates that there are active work items. These work items need to be closed in order to proceed further. Next sampling time will be after 5 minutes.
![](Evidences/Image21.png)


We close the pending task and wait for the time for the next evaluation.
![](Evidences/Image22.png)


Once the evaluation is successful, you will see the request for pre-deployment approval.
![](Evidences/Image23.png)


Track the progress of the release and verify that the deployment to both web apps completed successfully.
![](Evidences/Image24.png)


Validate that failed requests were detected by Application Insights by navigating to the Application Insights blade of the Canary web app page.
![](Evidences/Image25.png)


List the resource groups created in the lab for this module by running the following command:
```
az group list --query "[?starts_with(name,'az400m10l01-RG')].name" --output tsv
```

Delete the resource groups that you created in the lab for this module by executing the following command:
```
az group list --query "[?starts_with(name,'az400m10l01-RG')].[name]" --output tsv | xargs -L1 bash -c 'az group delete --name $0 --no-wait --yes'
```
![](Evidences/Image26.png)


### [<-- Back to readme](../README.md)
