# winVirtualMachine-rg-mktDp-eastus-prod-7yt56-IaC


Steps:

- Use the Uplaod File fetaure to upload a working ARM Template JSON File
- Create a Service Principal for GitHub
	1.	Run the below script in aBash session using Azure CloudShell. Be sure to replace the script below with your Subscription ID and Resource Group where you want your IaC ARM Template Cloud resource to be deployed:
       az ad sp create-for-rbac --name "winVM1ServicePrincipal" --role contributor --scopes /subscriptions/<subscription-id>/resourceGroups/<group-name> --json-auth
	2.	Copy the output and paste in the main GitHub repository to be used as a value under Settings -> Security -> Actions -> New repository secret with name field as AZURE_CREDENTIALS
