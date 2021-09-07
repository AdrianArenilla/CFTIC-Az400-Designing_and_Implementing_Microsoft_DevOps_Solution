# Microsoft Az-400 (Adrián Arenilla Seco)

## Lab 09: Package Management with Azure Artifacts
In this lab, you will learn how to use Azure Artifacts, NuGet, npm, and Maven in Azure DevOps.

### [Go to lab instructions -->](AZ400_M09_Package_Management_with_Azure_Artifacts.md)


Project created successfully.
![](Evidences/Image1.png)


Clone the project in Visual Studio.
![](Evidences/Image2.png)


Verify that the repository has been cloned correctly within Visual Studio.
![](Evidences/Image3.png)


Create new feed.
![](Evidences/Image4.png)


On the Connect to feed pane, in the NuGet section, select Visual Studio and, on the Visual Studio pane, copy the Source url.
![](Evidences/Image5.png)


Connect Visual Studio to the newly created feed.
![](Evidences/Image6.png)


Create a new project (Class Library (.NET Framework) template).
![](Evidences/Image7.png)


Configure the new project.
![](Evidences/Image8.png)


Delete Class1.cs
![](Evidences/Image9.png)


Verify that the Target framework is set to .NET Framework 4.5.1.
![](Evidences/Image10.png)


Build the project.
![](Evidences/Image11.png)


We'll use NuGet.exe to generate a NuGet package directly from the built project.
![](Evidences/Image12.png)


Move the nuget.exe file to the same folder containing the .csproj file.
![](Evidences/Image13.png)


From the Administrator: Windows PowerShell window, run the following to create a .nupkg file from the project. 
```
./nuget.exe pack ./PartsUnlimited.Shared.csproj
```
![](Evidences/Image14.png)


Verify that the name is PartsUnlimited.Shared.1.0.0.nupkg.
![](Evidences/Image15.png)


From the Administrator: Windows PowerShell window, run the following to create a .nupkg file from the project. 
```
./nuget.exe push -source "PartsUnlimitedShared" -ApiKey AzDO PartsUnlimited.Shared.1.0.0.nupkg
```
![](Evidences/Image16.png)


The PartsUnlimitedShared feed should include the newly published NuGet package. 
![](Evidences/Image17.png)


Importing a NuGet package.
![](Evidences/Image18.png)


If everything is correct, the package installs correctly.
![](Evidences/Image19.png)


Build the project and verify that the build completed successfully.
![](Evidences/Image20.png)


Add new Class template type element.
![](Evidences/Image21.png)


In the code of the TaxService.cs class, replace the existing definition of the class with the following code and save the file.
```
namespace PartsUnlimited.Shared
{
    public class TaxService
    {
        static public decimal CalculateTax(decimal taxable, string postalCode)
        {
            return taxable * (decimal).1;
        }
    }
}
```
![](Evidences/Image22.png)


In the AssemblyInfo.cs file, change the `[assembly: AssemblyVersion("1.0.0.0")]` to `[assembly: AssemblyVersion("1.1.0.0")]` and save the file.
![](Evidences/Image23.png)


Build the project.
![](Evidences/Image24.png)


From the Administrator: Windows PowerShell window and run the following command to repackage the NuGet package. 
```
./nuget.exe pack PartsUnlimited.Shared.csproj
```
![](Evidences/Image25.png)


Verify that there are now 2 files with different version names.
![](Evidences/Image26.png)


From the Administrator: Windows PowerShell window, run the following command to publish the updated package. 
```
./nuget.exe push -source "PartsUnlimitedShared" -ApiKey AzDO PartsUnlimited.Shared.1.1.0.nupkg
```
![](Evidences/Image27.png)


On the PartsUnlimitedShared 1.0.0 artifact pane, click the Versions tab and verify that it includes versions 1.0.0 and 1.1.0.
![](Evidences/Image28.png)


Update a NuGet package to install the new version.
![](Evidences/Image29.png)


If everything is correct, the package installs correctly.
![](Evidences/Image30.png)


Build and run the site. Verify that it works as expected.
![](Evidences/Image31.png)


### [<-- Back to readme](../README.md)

