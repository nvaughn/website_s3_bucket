# Terraform - Module Demo

This is a simple Terraform module to S3 bucket for a static site

## What will this do?

This configuration will provision a world readable S3 bucket in your AWS account. 

## What are the prerequisites?

AWS account
Terraform

Quickstart
----------

Call this module from your Terraform root config.  Create a new module resource referencing this github project as source.

module "website_s3_bucket" {
  source = "git@github.com:nvaughn/website_s3_bucket

  bucket_name = "cbt-demo-04-11-2022"

  tags = {
    Terraform   = "true"
    Environment = "dev"
  }
}

