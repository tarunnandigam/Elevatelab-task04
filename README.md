What I Learned: 

Infrastructure as Code (IaC): How Terraform automates the creation of infrastructure using configuration files.
Terraform Workflow:
terraform init → initializes provider
terraform plan → previews actions
terraform apply → executes changes
terraform destroy → tears down resources
Provider Concept: Understood how the Docker provider allows Terraform to communicate with Docker.
State Management: Learned how Terraform tracks resources in terraform.tfstate.
Running the same configuration multiple times doesn’t recreate existing resources — Terraform only applies necessary changes.
Debugging & Problem Solving: Got comfortable reading Terraform error messages and fixing configuration issues.

Issues Faced and How I Solved Them :
1)Error: Inconsistent dependency lock file - Terraform provider not initialized.
sol : Run terraform init to download the Docker provider and reinitialize.

2)Port 8080 already in use-Another process or container was using the same port.
sol : Changed the external port from 8080 to 8081 in main.tf and reapplied configuration.


## Steps I Followed

1. **Set Up Environment**
   - Installed Terraform using Snap:  
     
     ==>sudo snap install terraform
     
   - Verified installation with `terraform -v`.
   - Ensured Docker was installed and running using:
    
     ==> sudo systemctl start docker
     

2. **Created Project Directory**
   
   ==> mkdir terraform-docker-project
   


cd terraform-docker-project

