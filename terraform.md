# 🔬 Terraform

{% hint style="info" %}
Install terraform autocomplete - \`**`` terraform -install-autocomplete` ``**
{% endhint %}

### format, validate & Init

* `terraform fmt` - Format code as per HCL standard
* `terraform validate` - validate code syntax
* `terraform validate -backend=false` - Validate code, skip [backend](https://www.terraform.io/cli/commands/validate) validation

### terraform state

* `terraform state list` - List resource in the state file
* `terraform state show [resource]` - Show properties of a resource
* `terraform show` - Show everything in state file
* `terraform state list` - List resource
