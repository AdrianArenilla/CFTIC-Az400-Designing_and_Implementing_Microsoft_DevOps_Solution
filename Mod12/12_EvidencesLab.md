# Microsoft Az-400 (Adrián Arenilla Seco)

## Lab 12: Feature Flag Management with LaunchDarkly and Azure DevOps
In this lab, you will learn how to optimize management of feature flags in Azure DevOps by leveraging LaunchDarkly.

### [Go to lab instructions -->](AZ400_M12_Feature_Flag_Management_with_LaunchDarkly_and_Azure_DevOps.md)


Select the checkbox below the LaunchDarkly Integration V2.
![](Evidences/Image1.png)


Project created successfully.
![](Evidences/Image2.png)


Create a feature flag in LaunchDarkly.
![](Evidences/Image3.png)


Create a feature flag in LaunchDarkly.
![](Evidences/Image4.png)


Set the Commit mention linking and Commit mention work item resolution settings to On.
![](Evidences/Image5.png)


Clone the repository into Visual Studio.
![](Evidences/Image6.png)


Change the branch to launch-darkly.
![](Evidences/Image7.png)


In the NuGet: PartsUnlimitedWebsite pane, note that LaunchDarkly.Client is already installed.
![](Evidences/Image8.png)


Verify that the application launches successfully in the local browser session.
![](Evidences/Image9.png)


Update the HomeController.cs file.
![](Evidences/Image10.png)


Update the AccountController.cs file.
![](Evidences/Image11.png)


Update the _Layout.cshtml file.
![](Evidences/Image12.png)


Update the SDK key of the HomeController.cs file.
![](Evidences/Image13.png)


Update the SDK key of the AccountController.cs file.
![](Evidences/Image14.png)


Update the HomeController.cs file.
![](Evidences/Image15.png)


Verify that the Member portal link no longer appears in the web browser displaying the Parts Unlimited website, since the MemberPortal flag is, at this point, turned off .
![](Evidences/Image16.png)


In the query results, note the work item ID and click the entry representing the work item.
![](Evidences/Image17.png)


WorkItem is integrated correctly with LaunchDarkly.
![](Evidences/Image18.png)


Create a new token in LaunchDarkly portal.
![](Evidences/Image19.png)


Create a new service connection.
![](Evidences/Image20.png)


Verify that the connection service has been created correctly.
![](Evidences/Image21.png)


Associate a feature flag with the work item.
![](Evidences/Image22.png)


Create a new release pipeline LaunchDarkly_CD.
![](Evidences/Image23.png)


Set up the options of release pipeline LaunchDarkly_CD.
![](Evidences/Image24.png)


Create a new personal access token (PAT).
![](Evidences/Image25.png)


Change the value of this variables.
![](Evidences/Image26.png)


Create a new release pipeline LaunchDarkly-CI..
![](Evidences/Image27.png)


Monitor its progress and verify that it completes successfully.
![](Evidences/Image28.png)


Monitor its progress and verify that it completes successfully.
![](Evidences/Image29.png)


Verify that the application launches successfully in the local browser session.
![](Evidences/Image30.png)


Delete the resource group.
![](Evidences/Image31.png)


### [<-- Back to readme](../README.md)

