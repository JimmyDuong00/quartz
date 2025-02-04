---
draft: true
tags:
  - azure
  - terraform
  - azuregoat
---
This project is the beginning of the #azuregoat series that will investigate, exploit, and remediate the OWASP Top 10 Web App vulnerabilities. This project will allow us to learn how to attack and defend Cloud infrastructure. 
## Deploying the project:
Login to Azure portal and open the CLI:

Create the 'azuregoat_app' resource group and select the location to create the group in:

```
az group create --name azuregoat_app --location westus
```

Open the Azure CLI and switch to Bash:

Clone the INE repo:
```
git clone https://github.com/ine-labs/AzureGoat
```

Navigate into the 'AzureGoat' folder:
```
cd AzureGoat
```

Initialize the config files:
```
terraform init
```

(Optional) List all resources that will be deployed:

```
terraform plan
```

Deploy resources:

```
terraform apply --auto-approve
```

In the CLI, you will see a link of the deployed site, copy and paste it into a web browser and check if everything is working:


We can now begin the labs.

## Destroying the project:
When we are done or we want to save on costs in Azure, we can quickly destroy the infrastructure until needed again.

In the Azure CLI:

```
terraform destroy --auto-approve
```

Make sure to double check in the console if everything has been completely destroyed before signing off! 
## Attacking:
[[Insecure Direct Object Reference]]
[[Server Side Request Forgery]]
[[Security Misconfiguration]]
[[WIP Using Azure Runbooks for Privilege Escalation]]

## Defending
[[Defending SKL Injection Attacks with Azure Web Application Firewall]]
[[Defending Storage Accounts]]
[[Defending Against Privilege Escalation using Azure Polices and Alerts]]
[[Adding security controls into Terraform]]

## Conclusion and Final Thoughts

