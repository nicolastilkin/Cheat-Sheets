# ☸️ Kubernetes Cheat Sheet

## 📦 kubectl Basics

| Action               | Command                                                   |
| -------------------- | --------------------------------------------------------- |
| Show cluster info    | `kubectl cluster-info`                                    |
| List all nodes       | `kubectl get nodes`                                       |
| List all namespaces  | `kubectl get namespaces`                                  |
| Switch namespace     | `kubectl config set-context --current --namespace=<name>` |
| View current context | `kubectl config current-context`                          |

---

## 🐳 Pods

| Action                      | Command                                    |
| --------------------------- | ------------------------------------------ |
| List all pods               | `kubectl get pods`                         |
| List pods in all namespaces | `kubectl get pods --all-namespaces`        |
| Describe a pod              | `kubectl describe pod <pod-name>`          |
| Delete a pod                | `kubectl delete pod <pod-name>`            |
| Exec into a pod             | `kubectl exec -it <pod-name> -- /bin/bash` |
| Logs from a pod             | `kubectl logs <pod-name>`                  |

---

## 📦 Deployments

| Action            | Command                                                      |
| ----------------- | ------------------------------------------------------------ |
| List deployments  | `kubectl get deployments`                                    |
| Create deployment | `kubectl create deployment <name> --image=<image>`           |
| Scale deployment  | `kubectl scale deployment <name> --replicas=<count>`         |
| Update image      | `kubectl set image deployment/<name> <container>=<new-image>` |
| Delete deployment | `kubectl delete deployment <name>`                           |

---

## 🌐 Services

| Action                       | Command                                                      |
| ---------------------------- | ------------------------------------------------------------ |
| List services                | `kubectl get services`                                       |
| Expose deployment as service | `kubectl expose deployment <name> --type=LoadBalancer --port=<port>` |
| Describe service             | `kubectl describe service <name>`                            |
| Delete service               | `kubectl delete service <name>`                              |

---

## ⚙️ ConfigMaps & Secrets

| Action           | Command                                                      |
| ---------------- | ------------------------------------------------------------ |
| Create configmap | `kubectl create configmap <name> --from-literal=key=value`   |
| Create from file | `kubectl create configmap <name> --from-file=<file>`         |
| View configmaps  | `kubectl get configmaps`                                     |
| Create secret    | `kubectl create secret generic <name> --from-literal=key=value` |
| View secrets     | `kubectl get secrets`                                        |

---

## 📁 Apply / Manage Resources

| Action                | Command                                         |
| --------------------- | ----------------------------------------------- |
| Apply config file     | `kubectl apply -f <file>.yaml`                  |
| Delete from file      | `kubectl delete -f <file>.yaml`                 |
| Dry run (test)        | `kubectl apply -f <file>.yaml --dry-run=client` |
| View resource in YAML | `kubectl get <resource> <name> -o yaml`         |

---

## 📂 Namespaces

| Action                 | Command                                         |
| ---------------------- | ----------------------------------------------- |
| Create namespace       | `kubectl create namespace <name>`               |
| Delete namespace       | `kubectl delete namespace <name>`               |
| View current namespace | `kubectl config view --minify | grep namespace` |

---

## 📌 Useful Tips

| Task                     | Command                             |
| ------------------------ | ----------------------------------- |
| View all resource types  | `kubectl api-resources`             |
| Explain a resource       | `kubectl explain <resource>`        |
| Autocomplete for kubectl | `source <(kubectl completion bash)` |

---