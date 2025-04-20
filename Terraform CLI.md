# 🌍 Terraform CLI

## 🛠️ Setup

| Action                  | Command                                                      |
| ----------------------- | ------------------------------------------------------------ |
| Install Terraform       | [Install Guide](https://developer.hashicorp.com/terraform/downloads) |
| Check version           | `terraform version`                                          |
| Show available commands | `terraform --help`                                           |

---

## 📁 Terraform Workflow

| Step                      | Command              | Description                                   |
| ------------------------- | -------------------- | --------------------------------------------- |
| **1. Initialize project** | `terraform init`     | Downloads providers, sets up `.terraform` dir |
| **2. Format code**        | `terraform fmt`      | Formats `.tf` files                           |
| **3. Validate syntax**    | `terraform validate` | Validates `.tf` code                          |
| **4. Plan changes**       | `terraform plan`     | Shows what will be created/changed            |
| **5. Apply changes**      | `terraform apply`    | Applies the planned infrastructure            |
| **6. Destroy resources**  | `terraform destroy`  | Tears down infrastructure                     |

---

## 📦 Modules & State

| Action                     | Command                                             |
| -------------------------- | --------------------------------------------------- |
| Use a module               | `module "example" { source = "./modules/example" }` |
| Show current state         | `terraform show`                                    |
| List resources in state    | `terraform state list`                              |
| Remove resource from state | `terraform state rm <resource>`                     |
| Import existing resource   | `terraform import <resource> <id>`                  |

---

## 📂 Files & Directory Structure

| File                  | Purpose                                  |
| --------------------- | ---------------------------------------- |
| `main.tf`             | Main configuration                       |
| `variables.tf`        | Input variables                          |
| `outputs.tf`          | Output values                            |
| `terraform.tfvars`    | Default values for variables             |
| `.terraform.lock.hcl` | Dependency lock file                     |
| `.terraform/`         | Working directory for providers, plugins |

---

## 🔧 Variables

```hcl
# Define variable
variable "region" {
  description = "AWS region"
  type        = string
  default     = "us-east-1"
}

# Use variable
provider "aws" {
  region = var.region
}