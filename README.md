Create Azure Virtual Network with Site to Site Connection (Resource Manager)
============================================================================

            

This is a script cmdlet that can be used to automate the deployment of an Azure virtual machine network that needs to be connected to an on-premise system.


The cmdlet is based on the steps detailed in Cheryl's article: https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-create-site-to-site-rm-powershell


I basically took her steps and added:


  *  sensible defaults 
  *  some basic sanity checking 
  *  confirm/whatif support 
  *  A progress bar 
  *  Get-Help Support 

I developed this because I found myself going through these steps with the new Resource Manager often for new O365 customers who wanted their dirsync infroastructure hosted in Azure, so I decided to automate the process in the new Resource Manager model.


Requires Powershell v3 or later and Azure powershell module 0.9 or later. Tested on 0.9.8.






PowerShell
Edit|Remove
powershell
PS C:\Temp>AzureVirtualNetworkS2S.ps1 `
-ResourceGroup Default-Networking `
-location centralus `
-localGatewayIPAddress 1.1.1.1  `
-localAddressPrefix 10.0.0.0/8

PS C:\Temp>AzureVirtualNetworkS2S.ps1 ` 
-ResourceGroup Default-Networking ` 
-location centralus ` 
-localGatewayIPAddress 1.1.1.1  ` 
-localAddressPrefix 10.0.0.0/8







        
    
TechNet gallery is retiring! This script was migrated from TechNet script center to GitHub by Microsoft Azure Automation product group. All the Script Center fields like Rating, RatingCount and DownloadCount have been carried over to Github as-is for the migrated scripts only. Note : The Script Center fields will not be applicable for the new repositories created in Github & hence those fields will not show up for new Github repositories.
