# PSModuleFixer - PUBLIC REPOSITORY
# Do not commit any private info in this repository!

## Background:

When updating powershell modules, often old versions of the modules are left behind.
There are two scripts in this repo to help manage this:

* psmodulestatusreport.ps1
* psmodulefixer.ps1

## What they do:

### psmodulestatusreport.ps1 
psmodulestatusreport.ps1 is a read only script that will tell you any module that has multiple versions installed, showing the found version of the module, along with the highest _installed_ version you have (there may be newer versions online)

### psmodulefixer.ps1
psmodulefixer.ps1 is a destructive script in that it will look at all your modules and delete all but the most current installed version of each module. In my experience, this has taken quite a while to run, sometimes an hour or more.

## Other information:
This came about when updating azureRM commandlets.

You can update your AzureRM commandlets to the latest published version with this command:

```
Update-Module -Name AzureRM -Force
```


Info on these can be fonud here:
https://docs.microsoft.com/en-us/powershell/azure/install-azurerm-ps?view=azurermps-6.6.0


