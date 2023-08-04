<div style="background-color: #f9f9f9; border-left: 6px solid #3f51b5; padding: 0.5em;">
  🎮 <strong>The Legend of Zelda: Tears of the Kingdom</strong>: <em>was played heavily between completing Terraform labs.</em>
</div>

## Table of Contents

- [Install AWS CLI](#install)
- [Configure AWS CLI](#Configure-AWS-CLI)
- [View Commands](#View-Commands)
- [Validate](#validate)
- [Plan](#plan)
- [Apply](#apply)
- [Destroy](#destroy)
- [Terraform with AWS](#Terraform-with-AWS)
- [Resources](#resources)

## Install

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
## Configure AWS CLI

```bash
#initialize dir for TF
terraform init
```

## View Commands

```bash
#view AWS CLI version
aws --version
```bash
#view TF providers
terraform providers
```


## Resources

- [Terraform Official Documentation](https://www.terraform.io/docs/index.html)
- [Getting Started Guide](https://www.terraform.io/intro/index.html)
- [Terraform Registry (Modules & Providers)](https://registry.terraform.io/)
- [Community Forums and Support](https://discuss.hashicorp.com/c/terraform-core/27)

---
