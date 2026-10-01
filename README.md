# 🚀 Monolithic Azure Infrastructure

![Terraform](https://img.shields.io/badge/Terraform-Infrastructure%20as%20Code-7B42BC?logo=terraform)
![Microsoft Azure](https://img.shields.io/badge/Microsoft%20Azure-Cloud-0078D4?logo=microsoftazure)
![GitHub](https://img.shields.io/badge/GitHub-Version%20Control-181717?logo=github)

> A modular and reusable Infrastructure as Code (IaC) project for provisioning and managing Microsoft Azure infrastructure using Terraform.

---

## 📌 Overview

**Monolithic Azure Infrastructure** is a Terraform-based Infrastructure as Code project designed to automate the provisioning and management of Azure cloud resources.

The project follows a **modular Terraform architecture**, where commonly used Azure infrastructure components are organized into reusable modules.

Instead of manually creating resources through the Azure Portal, infrastructure can be defined as code, reviewed, version-controlled, and deployed consistently.

### 🎯 Project Objectives

- Automate Azure infrastructure provisioning using Terraform
- Create reusable Terraform modules
- Reduce infrastructure configuration duplication
- Maintain a structured and maintainable codebase
- Support environment-based infrastructure configuration
- Follow Infrastructure as Code best practices
- Manage infrastructure changes through Git and GitHub

---

## 🛠️ Technology Stack

| Technology | Purpose |
|------------|---------|
| **Microsoft Azure** | Cloud infrastructure platform |
| **Terraform** | Infrastructure as Code |
| **AzureRM Provider** | Terraform provider for Azure |
| **Git** | Version control |
| **GitHub** | Source code management |

---

## 📂 Repository Structure

```text
monolithic-azure-infra/
│
├── environments/
│
├── modules/
│   ├── azurerm_application_gateway/
│   ├── azurerm_bastion/
│   ├── azurerm_key_vault/
│   ├── azurerm_load_balancer/
│   ├── azurerm_public_ip/
│   ├── azurerm_resource_group/
│   ├── azurerm_subnet/
│   ├── azurerm_virtual_machine/
│   └── azurerm_virtual_network/
│
├── .gitignore
└── README.md
```

---

## 🧩 Terraform Modules

The project contains reusable Terraform modules for commonly required Azure infrastructure components.

| Module | Description |
|--------|-------------|
| `azurerm_resource_group` | Creates and manages Azure Resource Groups |
| `azurerm_virtual_network` | Creates and manages Azure Virtual Networks |
| `azurerm_subnet` | Creates Azure Subnets |
| `azurerm_public_ip` | Provisions Azure Public IP addresses |
| `azurerm_virtual_machine` | Provisions Azure Virtual Machines |
| `azurerm_load_balancer` | Configures Azure Load Balancer |
| `azurerm_application_gateway` | Configures Azure Application Gateway |
| `azurerm_bastion` | Provides secure access to Azure Virtual Machines |
| `azurerm_key_vault` | Creates and manages Azure Key Vault |

---

## 🌐 Azure Infrastructure Components

### Networking

- Azure Virtual Network
- Azure Subnet
- Azure Public IP
- Azure Load Balancer
- Azure Application Gateway
- Azure Bastion

### Compute

- Azure Virtual Machine

### Security

- Azure Key Vault

### Resource Management

- Azure Resource Groups

---

## ♻️ Why Terraform Modules?

Terraform modules make infrastructure code reusable, maintainable, and easier to scale.

Instead of writing the same infrastructure configuration repeatedly, reusable modules can be consumed by different environments.

### Benefits

- ♻️ Reusability
- 📦 Better code organization
- 🔧 Easier maintenance
- 📈 Improved scalability
- 🚫 Reduced code duplication
- 🔄 Consistent infrastructure deployment

---

## 🌍 Environment-Based Configuration

The repository separates environment-specific configuration from reusable Terraform modules.

This allows the same Terraform modules to be reused across different environments while maintaining environment-specific configuration.

```text
environments/
      │
      └── Environment Configuration
                  │
                  ▼
             Terraform Modules
                  │
        ┌─────────┼─────────┐
        ▼         ▼         ▼
      Network   Compute   Security
```

---

## 🚀 Getting Started

### Prerequisites

Before deploying the infrastructure, make sure the following are installed:

- Terraform
- Azure CLI
- Git
- An active Azure subscription

---

## 🔐 Authenticate with Azure

Login to Azure using Azure CLI:

```bash
az login
```

Verify the active Azure subscription:

```bash
az account show
```

If you have multiple subscriptions, select the required subscription:

```bash
az account set --subscription "<SUBSCRIPTION_ID>"
```

---

## 📥 Clone the Repository

```bash
git clone https://github.com/shivamsona99/monolithic-azure-infra.git
```

Navigate to the repository:

```bash
cd monolithic-azure-infra
```

---

## ⚙️ Terraform Workflow

The standard Terraform workflow used for infrastructure deployment is:

```text
Terraform Code
      │
      ▼
terraform init
      │
      ▼
terraform validate
      │
      ▼
terraform plan
      │
      ▼
terraform apply
      │
      ▼
Azure Infrastructure
```

### 1️⃣ Initialize Terraform

```bash
terraform init
```

Initializes the Terraform working directory and downloads the required providers.

### 2️⃣ Validate Configuration

```bash
terraform validate
```

Validates the Terraform configuration and checks for configuration errors.

### 3️⃣ Create Execution Plan

```bash
terraform plan
```

Displays the changes Terraform intends to make before modifying the Azure infrastructure.

### 4️⃣ Deploy Infrastructure

```bash
terraform apply
```

Creates or updates the Azure infrastructure according to the Terraform configuration.

### 5️⃣ Destroy Infrastructure

```bash
terraform destroy
```

Removes the Azure resources managed by the Terraform configuration.

> ⚠️ **Warning:** Use `terraform destroy` carefully because it can permanently delete Azure resources.

---

## 🔒 Security Best Practices

- Never commit passwords or secrets to GitHub.
- Never commit private keys.
- Avoid hard-coding sensitive credentials.
- Use appropriate Azure authentication mechanisms.
- Keep sensitive `.tfvars` files out of source control.
- Review `terraform plan` before applying changes.
- Protect Terraform state when using remote state management.
- Use `.gitignore` to prevent sensitive or generated files from being committed.

---

## 🔄 Infrastructure Lifecycle

```text
Write Terraform Code
        │
        ▼
Create / Update Modules
        │
        ▼
Terraform Init
        │
        ▼
Terraform Validate
        │
        ▼
Terraform Plan
        │
        ▼
Review Changes
        │
        ▼
Terraform Apply
        │
        ▼
Azure Infrastructure
```

---

## 📈 Scalability

The modular structure allows the project to grow as additional Azure services are required.

New Terraform modules can be added without changing the overall project architecture.

For example:

```text
modules/
│
├── azurerm_virtual_network/
├── azurerm_subnet/
├── azurerm_virtual_machine/
├── azurerm_application_gateway/
├── azurerm_load_balancer/
├── azurerm_bastion/
├── azurerm_key_vault/
│
└── future-modules/
    ├── azurerm_storage_account/
    ├── azurerm_container_registry/
    └── azurerm_aks/
```

---

## 🎯 Key Learning Outcomes

This project demonstrates practical understanding of:

- Infrastructure as Code
- Terraform
- Microsoft Azure
- Terraform Modules
- Azure Networking
- Azure Compute
- Azure Security Services
- Environment-based infrastructure organization
- Git and GitHub
- Infrastructure lifecycle management
- Reusable infrastructure design

---

## 🔮 Future Enhancements

Possible future improvements include:

- Azure Storage Account backend for Terraform state
- Remote state management
- State locking
- Azure DevOps CI/CD pipeline
- Automated Terraform validation
- Automated Terraform plan
- Approval-based Terraform deployment
- Additional Azure services
- Security and compliance automation
- Infrastructure monitoring

---

## 👨‍💻 Author

### Shivam Kumar

**DevOps | Microsoft Azure | Terraform | Azure DevOps**

🔗 **GitHub:**  
https://github.com/shivamsona99

🔗 **LinkedIn:**  
https://linkedin.com/in/shivam-kumar-singh-devops99

---

## 📄 License

This project is created for **learning, practice, and demonstration purposes**.
