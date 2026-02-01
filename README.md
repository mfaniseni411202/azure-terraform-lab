# Azure Terraform Deployment Project

## Overview
This project demonstrates Infrastructure as Code (IaC) using Terraform to deploy an Azure Resource Group. The deployment was executed via Azure Cloud Shell, showcasing cloud-native development workflows.

## Project ArchitectureTerraform
 
Code → Azure Provider → Resource Group Deployment

## Technologies Used
- **Infrastructure as Code:** Terraform v1.6+
- **Cloud Platform:** Microsoft Azure
- **Environment:** Azure Cloud Shell (Bash)
- **Documentation:** Markdown

## Deployment Steps
1. **Authentication:** Azure Cloud Shell implicit authentication
2. **Initialization:** `terraform init` - Download Azure provider plugins
3. **Planning:** `terraform plan` - Preview infrastructure changes
4. **Execution:** `terraform apply` - Deploy Azure Resource Group
5. **Verification:** Azure Portal validation
6. **Cleanup:** `terraform destroy` - Remove resources

## Code Structure
```hcl
resource "azurerm_resource_group" "banele_rg" {
  name     = "rg-banele-terraform-lab"
  location = "South Africa North"
  
  tags = {
    Environment = "Lab"
    Owner       = "Banele"
    Project     = "Cloud-Engineering"
  }
}
Key Learnings
Terraform's declarative syntax for cloud infrastructure

Azure Cloud Shell as a zero-install development environment

Importance of terraform plan before applying changes

Cloud cost management through immediate resource cleanup

Infrastructure lifecycle management principles

Screenshots
Step	Description	File
1	Terraform Initialization	screenshots/01-init-success.png
2	Terraform Plan Output	screenshots/02-plan-output.png
3	Terraform Apply Success	screenshots/03-apply-success.png
4	Azure Portal Verification	screenshots/04-portal-verify.png
5	Resource Cleanup	screenshots/05-destroy-complete.png
Future Enhancements
Add Azure Virtual Machine deployment

Implement Terraform variables for flexibility

Create remote state storage (Azure Blob)

Add network security groups

Implement CI/CD pipeline with GitHub Actions

Author
Banele Ndlanzi
GitHub Profile | LinkedIn ProfileLicense
This project is for educational purposes as part of cloud engineering skill development.
