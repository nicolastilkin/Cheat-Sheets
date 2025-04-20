# ☁️ Azure

## 🛠️ CLI Configuration

| Action                    | Command                                                     |
| ------------------------- | ----------------------------------------------------------- |
| Login to Azure            | `az login`                                                  |
| Set subscription          | `az account set --subscription "<subscription-name-or-id>"` |
| Show current subscription | `az account show`                                           |
| List subscriptions        | `az account list --output table`                            |
| Set default output format | `az configure --defaults output=table`                      |

---

## 📦 Resource Groups

| Action                | Command                                               |
| --------------------- | ----------------------------------------------------- |
| List resource groups  | `az group list`                                       |
| Create resource group | `az group create --name <name> --location <location>` |
| Delete resource group | `az group delete --name <name>`                       |

---

## 🖥️ Virtual Machines

| Action     | Command                                                      |
| ---------- | ------------------------------------------------------------ |
| List VMs   | `az vm list -d -o table`                                     |
| Create VM  | `az vm create --name <vm-name> --resource-group <rg> --image UbuntuLTS --admin-username azureuser --generate-ssh-keys` |
| Start VM   | `az vm start --name <vm-name> --resource-group <rg>`         |
| Stop VM    | `az vm stop --name <vm-name> --resource-group <rg>`          |
| Restart VM | `az vm restart --name <vm-name> --resource-group <rg>`       |
| Delete VM  | `az vm delete --name <vm-name> --resource-group <rg>`        |

---

## 💾 Storage

| Action                 | Command                                                      |
| ---------------------- | ------------------------------------------------------------ |
| List storage accounts  | `az storage account list`                                    |
| Create storage account | `az storage account create --name <name> --resource-group <rg> --location <location> --sku Standard_LRS` |
| List containers        | `az storage container list --account-name <name>`            |
| Upload blob            | `az storage blob upload --account-name <name> --container-name <container> --name <blob-name> --file <file-path>` |

---

## 🌐 Networking

| Action           | Command                                                      |
| ---------------- | ------------------------------------------------------------ |
| List VNets       | `az network vnet list`                                       |
| Create VNet      | `az network vnet create --name <vnet-name> --resource-group <rg> --subnet-name <subnet-name>` |
| List NSGs        | `az network nsg list`                                        |
| Open port in NSG | `az vm open-port --port <port> --resource-group <rg> --name <vm-name>` |

---

## 🔐 Identity & Access (IAM)

| Action      | Command                                                      |
| ----------- | ------------------------------------------------------------ |
| List users  | `az ad user list`                                            |
| Create user | `az ad user create --display-name <name> --user-principal-name <user@domain> --password <password>` |
| List roles  | `az role definition list`                                    |
| Assign role | `az role assignment create --assignee <user-or-app-id> --role <role-name> --scope <scope>` |

---

## 🧠 Azure Monitor & Logs

| Action                   | Command                                                      |
| ------------------------ | ------------------------------------------------------------ |
| List activity logs       | `az monitor activity-log list`                               |
| View metrics             | `az monitor metrics list --resource <resource-id>`           |
| View diagnostic settings | `az monitor diagnostic-settings list --resource <resource-id>` |

---

## 🧾 Billing & Cost

| Action                | Command                                                      |
| --------------------- | ------------------------------------------------------------ |
| Show current usage    | `az consumption usage list`                                  |
| Show cost by resource | `az consumption usage list --include-meter-details --query "[].{Resource:instanceName, Cost:pretaxCost}"` |

---

## 📋 Tags

| Action              | Command                                              |
| ------------------- | ---------------------------------------------------- |
| Add tag to resource | `az resource tag --tags env=prod --resource-id <id>` |
| List tags           | `az tag list`                                        |

---

## 🧰 Misc

| Action                   | Command                       |
| ------------------------ | ----------------------------- |
| List available locations | `az account list-locations`   |
| Check CLI version        | `az version`                  |
| Upgrade Azure CLI        | `az upgrade`                  |
| Show help for command    | `az <group> <command> --help` |

---

## ✅ Best Practices

- Use `--output table` or `--output json` for readable output.
- Use `az login --use-device-code` for WSL or headless login.
- Use `az group export` to back up ARM templates.
- Leverage tags for cost management and automation.

---