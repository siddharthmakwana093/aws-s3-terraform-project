# aws-s3-terraform-project

# AWS Static Website Hosting with Terraform and CloudFront

## Overview
This project provisions and deploys a static website on AWS S3 using Terraform and integrates AWS CloudFront to enable secure HTTPS access.

## Architecture
User → CloudFront (HTTPS) → S3 Static Website Hosting

## AWS Services Used
- Amazon S3
- Amazon CloudFront
- Terraform

## Features
- Infrastructure as Code (IaC)
- Static website hosting
- HTTPS delivery using CloudFront CDN
- Public access configuration using bucket policies

## Terraform Commands

terraform init
terraform plan
terraform apply
terraform destroy

## Issues Faced & Resolutions

### Issue
S3 static website endpoint was inaccessible on some mobile browsers because browsers automatically enforced HTTPS.

### Root Cause
Amazon S3 website endpoints support HTTP only.

### Resolution
Configured AWS CloudFront in front of the S3 website endpoint to provide HTTPS support and proper routing.

## Outcome
Successfully deployed a publicly accessible HTTPS-enabled static website using Terraform and AWS services.
