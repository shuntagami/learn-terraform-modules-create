# Learn Terraform Modules Create

Learn what Terraform modules are and how to create one.

This repo is a companion repo to the [Build a Module tutorial](https://developer.hashicorp.com/terraform/tutorials/modules/module-create).

# Setup

```
terraform init
terraform apply
aws s3 cp modules/aws-s3-static-website-bucket/www/ s3://$(terraform output -raw website_bucket_name)/ --recursive
open https://shuntagami-static-website.s3.ap-northeast-1.amazonaws.com/index.html
```

# Cleanup up the website and infrastructure

```
aws s3 rm s3://$(terraform output -raw website_bucket_name)/ --recursive
terraform destroy
```
