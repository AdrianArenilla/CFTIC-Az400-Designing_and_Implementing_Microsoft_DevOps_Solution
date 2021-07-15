# Microsoft Az-400 (Adrián Arenilla Seco)

## Lab 02: Version Controlling with Git in Azure Repos
In this lab, you will learn how to establish a local Git repository, which can easily be synchronized with a centralized Git repository in Azure DevOps. In addition, you will learn about Git branching and merging support. You will use Visual Studio Code, but the same processes apply for using any Git-compatible client.

### [Go to lab instructions -->](AZ400_M02_Version_Controlling_with_Git_in_Azure_Repos.md)


Project created successfully.
![](Evidences/Image1.png)


Store the credentials in Git.
```
git config --global credential.helper wincred
```
See if we already have the credentials.
```
git config --list
```
![](Evidences/Image2.png)


Clone the repository in VSCode.
![](Evidences/Image3.png)


Successfully cloned repository.
![](Evidences/Image4.png)


Save work with commits.
![](Evidences/Image5.png)


Publish changes.
![](Evidences/Image6.png)


View sync status.
![](Evidences/Image7.png)


Verify commit in the Azure DevOps portal.
![](Evidences/Image8.png)


Second change made to the document.
![](Evidences/Image9.png)


Third change made to the document.
![](Evidences/Image10.png)


Commit only in one document.
![](Evidences/Image11.png)


Publish changes.
![](Evidences/Image12.png)


Compare changes to a local document.
![](Evidences/Image13.png)


Compare changes to a document hosted on the Azure DevOps portal.
![](Evidences/Image14.png)


"Dev" branch created and selected.
![](Evidences/Image15.png)


Publish changes.
![](Evidences/Image16.png)


Verify branch in the Azure DevOps portal.
![](Evidences/Image17.png)


Deleted "dev" branch.
![](Evidences/Image18.png)


Update the source branches in the local snapshot and it will remove the ones that are no longer there.
![](Evidences/Image19.png)


The branch "dev" doesn't exist.
![](Evidences/Image20.png)


### [<-- Back to readme](../README.md)

