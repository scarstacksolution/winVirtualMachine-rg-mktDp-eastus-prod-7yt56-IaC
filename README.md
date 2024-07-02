# winVirtualMachine-rg-mktDp-eastus-prod-7yt56-IaC


Steps:

- Use the Uplaod File fetaure to upload a working ARM Template JSON File
- Create a Resource group in your Azure portal using the following name for the Resource group: rg-mktDp-eastus-prod-7yt56
- Create a Service Principal for GitHub
	1.	Run the below script in aBash session using Azure CloudShell. Be sure to replace the script below with your Subscription ID and Resource Group where you want your IaC ARM Template Cloud resource to be deployed:
       az ad sp create-for-rbac --name "winVM1ServicePrincipal" --role contributor --scopes /subscriptions/your-subscription-id/resourceGroups/your-resource-group-name --json-auth
	2.	Copy the output and paste in the main GitHub repository to be used as a value under Settings -> Security -> Actions -> New repository secret with name field as AZURE_CREDENTIALS
- Navigate to the "Actions" Tab of the Repository and click "set up a workflow yourself" to create a YAML File.
- Update the name of the YAML File as: winVM1-IaC-ARM
- Upload the below content into the YAML File main field area:
- 
Xxxxxxx

- Observe the following areas/lines the file above pasted:
        1.	Line 22: WindowsVM_ARMTemplate.json is the name of your ARM Template file
        2.      Line 26: Microsoft.Compute/virtualMachines defined the type of cloud resource you are deploying and can be gotten from the actual ARM Template file
        3.	Line 28: winVM1jsonARMDeploy
  



