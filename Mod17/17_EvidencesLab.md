# Microsoft Az-400 (Adrián Arenilla Seco)

## Lab 17: Monitoring Application Performance with Application Insights
In this lab, you'll learn about how you can add Application Insights to an existing web application, as well as how to monitor the application via the Azure portal.

### [Go to lab instructions -->](AZ400_M17_Monitoring_Application_Performance_with_Application_Insights.md)


Project created successfully.
![](Evidences/Image1.png)


Create a Web App + SQL resource.
![](Evidences/Image2.png)


Create a Web App + SQL resource.
![](Evidences/Image3.png)


Delete Dev and QA stages.
![](Evidences/Image4.png)


Set up the options of release pipeline. 
![](Evidences/Image5.png)


Change the Pre-deployment condition.
![](Evidences/Image6.png)


Change the name of the WebsiteName variable inside the pipeline.
![](Evidences/Image7.png)


Review the lines referencing the Application Insights key and for a SQL connection.
![](Evidences/Image9.png)


Create a new application setting.
![](Evidences/Image10.png)


Change the name of defaultConnection.
![](Evidences/Image11.png)


Monitor its progress and verify that it completes successfully. 
![](Evidences/Image12.png)


Monitor its progress and verify that it completes successfully. 
![](Evidences/Image13.png)


Verify that the Parts Unlimited web site loads as expected.
![](Evidences/Image14.png)


This will trigger a server error since that category does not exist.
![](Evidences/Image15.png)


Review the resulting Application Insights blade displaying charts presenting different characteristics of the collected data, including the traffic you generated and failed requests you triggered.
![](Evidences/Image16.png)


Application map graph.
![](Evidences/Image17.png)


Smart detection graph.
![](Evidences/Image18.png)


Live metrics graph.
![](Evidences/Image19.png)


Transaction search graph.
![](Evidences/Image20.png)


Transaction search graph grouped by results.
![](Evidences/Image21.png)


Transaction search graph filtered by exception.
![](Evidences/Image22.png)


End-to-end transaction details view timeline.
![](Evidences/Image23.png)


End-to-end transaction details view telemetry.
![](Evidences/Image24.png)


Create a new test within availability graph.
![](Evidences/Image25.png)


Failures graph.
![](Evidences/Image26.png)


Details of the failures graph.
![](Evidences/Image27.png)


Performance graph.
![](Evidences/Image28.png)


Metrics graph splited by operations name.
![](Evidences/Image29.png)


Users graph.
![](Evidences/Image30.png)


More details of users graph.
![](Evidences/Image31.png)


More details of events graph.
![](Evidences/Image32.png)


Select an event to view the user flow.
![](Evidences/Image33.png)


User flows graph.
![](Evidences/Image34.png)


Analysis of page views graph.
![](Evidences/Image35.png)


Add a condition on an alert rule.
![](Evidences/Image36.png)


Create action group on an alert rule.
![](Evidences/Image37.png)


Define the type of notification within the action group.
![](Evidences/Image38.png)


Create alert rule with all parameter configurated.
![](Evidences/Image39.png)


Alert delivered in the mail.
![](Evidences/Image40.png)


List the resource groups created in the lab for this module by running the following command:
```
az group list --query "[?starts_with(name,'az400m17l01')].name" --output tsv
```

Delete the resource groups that you created in the lab for this module by executing the following command:
```
az group list --query "[?starts_with(name,'az400m17l01')].[name]" --output tsv | xargs -L1 bash -c 'az group delete --name $0 --no-wait --yes'
```
![](Evidences/Image41.png)


### [<-- Back to readme](../README.md)

