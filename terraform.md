# Terraform

## What is Terraform?

Terraform is an open-source `Infrastructure as Code` software tool that enables you to safely and predictably create, change, and improve infrastructure.

It can be used to provision resources on the main hyperscalars such as `AWS` and `Microsoft Azure`.

## Key Commands for Running Terraform

These are the key commands that you run in the terminal in order to run your terraform code.

| Command        | Description                                        |
|----------------|----------------------------------------------------|
|`terraform init`| Initialise Directory, pull down providers|
|`terraform fmt` | Format code per HCL Canonical standard|
|`terraform validate`| Validates the code for errors|
|`terraform plan`| Creates a plan for your environment|
|`terraform apply`| Creates the environment with your chosen provider|
|`terraform destroy`| Deletes your environment|

You can see a full terraform cheat sheet [here](https://acloudguru.com/blog/engineering/the-ultimate-terraform-cheatsheet)

You can also find help on terraform commands by using one of the 3 following commands:

```bash
> terraform
> terraform -h
> terraform --help
```

## Terraform - Infrastructure as Code

Hashicorp provides a [registry](https://registry.terraform.io/namespaces/hashicorp) where you can search documentation for different resources you want to create for all different providers, such as AWS, and Azure.