# Terraform Commands and Resources

This document includes a collection of essential Terraform commands and resources for managing and provisioning infrastructure.

## Table of Contents

- [Initialization](#initialization)
- [Planning](#planning)
- [Applying Changes](#applying-changes)
- [State Management](#state-management)
- [Modules](#modules)
- [Resources](#resources)

## Initialization

### Initialize a Terraform Working Directory
```bash
terraform init
```

## Planning

### Generate and Show an Execution Plan
```bash
terraform plan
```

## Applying Changes

### Build or Change Infrastructure
```bash
terraform apply
```

### Destroy Terraform-Managed Infrastructure
```bash
terraform destroy
```

## State Management

### List Resources in the State
```bash
terraform state list
```

### Show Resource Properties
```bash
terraform state show [address]
```

## Modules

### Using Modules

You can use modules to create reusable components. Here's an example of how to include a module:

```hcl
module "example" {
  source = "./module_folder"
  some_variable = "value"
}
```

## Resources

- [Terraform Official Documentation](https://www.terraform.io/docs/index.html)
- [Getting Started Guide](https://www.terraform.io/intro/index.html)
- [Terraform Registry (Modules & Providers)](https://registry.terraform.io/)
- [Community Forums and Support](https://discuss.hashicorp.com/c/terraform-core/27)

---
