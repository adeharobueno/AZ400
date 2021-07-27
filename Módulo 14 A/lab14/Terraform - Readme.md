Run terraform in cloud shell of azure

```
terraform
```

Create a `terraform-createrg.tf` file

```javascript
provider "azurerm" {
features {}
}
resource "azurerm_resource_group" "rg" {
        name = "testResourceGroup"
        location = "westus"
}
```

Initializing terraform with previous file 

```
terraform init
```

Appliying terraform previues file

```
terraform apply
```

`yes` when prompt a value of action and review the generated file:

```
cat terraform.tfstate
```

