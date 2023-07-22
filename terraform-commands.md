## Acknowledgments

**_The Legend of Zelda: Tears of the Kingdom_** was played heavily in between completing Terraform labs.

### Terraform Commands

```bash
#install TF
#Homebrew
brew tap hashicorp/tap
brew install hashicorp/tap/terraform

#Linux
yum-config-manager --add-repo https://rpm.releases.hashicorp.com/hashicorp/stable/rhel/7
yum install terraform
```
```bash
#update Terraform
#Homebrew
brew update
brew upgrade hashicorp/tap/terraform
```
```bash
#check TF version
terraform -version
```
```bash
#TF help
terraform -help
```
```bash
#initialize dir for TF
terraform init
```
```bash
#view TF state file / infrastructure status
terraform show
```
```bash
#list all of the items in Terraform’s managed state
terraform state list
```
```bash
#format TF files
terraform fmt
```
```bash
#validate TF files
terraform validate
```
```bash
#TF dry-run
terraform plan
```
```bash
#save a TF plan
terraform plan -out <plan-file-name>
```
```bash
#run TF w/confirmation
terraform apply
```
```bash
#run a saved TF plan
terraform apply <plan-file-name>
```
```bash
#run TF w/o confirming
terraform apply -auto-approve
```
```bash
#destroy w/confirmation
terraform destroy
```
```bash
#destroy resources created by TF w/o confirmation
terraform destroy -auto-approve
```
```bash
#plan a destroy
terraform plan -destroy
```
```bash
#save destroy plan
terraform plan -destroy -out <plan-file-name>
```
