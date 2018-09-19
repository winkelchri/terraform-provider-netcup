# terraform-provider-netcup
A Terraform provider for the www.netcup.de SCP webservice

Fork of https://github.com/rincedd/terraform-provider-netcup

# Current state

Currently, netcup is only available as a data source.

## Example configuration

Don't forget to add the `secret.tf` to .gitignore!

``` secrets.tf
variable "netcup_username" {
  default = "username"
}

variable "netcup_password" {
  default = "supersecret!11"
}
```

``` example.tf
provider "netcup" {
    login_name = "${var.netcup_username}"
    password = "${var.netcup_password}"
}

data "netcup_vserver" "balu" {}
```
