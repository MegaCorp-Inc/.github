# GCP Infrastructure Deployment with Terraform

Welcome to the Terraform configuration repository for deploying infrastructure on Google Cloud Platform (GCP). This README provides a detailed overview of the activated services, current configurations, and guidelines for managing the infrastructure using Terraform.

<img src="https://raw.githubusercontent.com/MegaCorp-Inc/.github/main/cc.jpg" />

## Services Activated on GCP

Our Terraform configuration enables the following services on GCP:

- **Compute Engine API**
- **VPC (Virtual Private Cloud)**
- **Firewall**
- **Service Networking API**
- **Cloud Build API**
- **Cloud Functions API**
- **Cloud Logging API**
- **Eventarc API**
- **Cloud Pub/Sub API**
- **Cloud Run Admin API**

## Current Configuration

Here is an overview of our current infrastructure configuration:

- **Region**: `us-east1`
- **Zone**: `us-east1-b`
- **IP CIDR Range for Web Application**: `69.4.20.0/24` -> `10.1.0.0/24`
- **IP CIDR Range for Database**: `4.20.69.0/24` -> `10.2.0.0/24`
- **Firewall Rules**: Allow traffic to port `6969`
- **Compute Instance Custom Image**: `webapp-centos-stream-8-a4-v1-20240227204431`

## Managing Infrastructure with Terraform

To manage the infrastructure, follow these steps:

1. **Initialize Terraform**
   - Execute `terraform init` to initialize the Terraform modules and prepare the working directory.

2. **Validate Configuration**
   - Run `terraform validate` to check the syntax and consistency of the configuration files.

3. **Plan Infrastructure Changes**
   - Use `terraform plan` to preview the changes that Terraform will apply to the infrastructure based on the current configuration.

4. **Apply Changes**
   - Execute `terraform apply` to implement the changes defined in the configuration files. This command will create or update the resources on GCP.

## Key Takeaways and Improvements

- **IP Range Selection**: Proper selection of IP ranges is essential for maintaining connectivity with GCP's internal services.
- **Network Segmentation**: Adjusted subnet configurations to avoid conflicts and improve network segmentation.
- **Enhanced Connectivity**: Implemented VPC peering and Serverless VPC connectors to facilitate better service connectivity.
- **Infrastructure Image Path**: Ensured consistency by updating the image path for building new infrastructure.
- **Cloud SQL Security**: Enhanced the security of Cloud SQL instances by configuring them with private IP addresses.
- **Connectivity Solutions**: Utilized Private Service Access (PSA) and VPC peering for secure and private intra-VPC connections.
- **Private Service Connect (PSC)**: Configured PSC for secure private connectivity within the VPC network.
- **Firewall Tagging**: Improved network security by applying firewall rules based on tags.

By following these best practices and continuous learning, we aim to maintain a secure and efficient infrastructure on Google Cloud Platform.

<img src="https://private-user-images.githubusercontent.com/144539453/326956327-a649c482-bdd1-4f13-8414-f9c0205e0c4a.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjIwMjUyMDMsIm5iZiI6MTcyMjAyNDkwMywicGF0aCI6Ii8xNDQ1Mzk0NTMvMzI2OTU2MzI3LWE2NDljNDgyLWJkZDEtNGYxMy04NDE0LWY5YzAyMDVlMGM0YS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzI2JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcyNlQyMDE1MDNaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT02NTJlNTE5MGE3ZGQyMTJiNDk2ZjI1NDgwNGEyMmQwOWU2OGY5Y2IyNDFiMzQyM2IyZTM3NTkxOGM2YjdhY2M0JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.p2J1SIKUJUPUC9b83H1ONjUOhPKOeM6RvwZemmzebbg" />

---

We hope this README provides a clear and comprehensive guide for managing GCP infrastructure with Terraform. For further assistance or inquiries, please refer to the documentation or contact our team. Happy deploying!
