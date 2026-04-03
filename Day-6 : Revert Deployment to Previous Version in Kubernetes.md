# Day-6 Revert Deployment to Previous Version in Kubernetes

## 📌 Scenario
Earlier today, the Nautilus DevOps team deployed a new release for an application. A customer has reported a bug in this release, so the team needs to revert to the previous stable version.

## 🎯 Objective
Rollback the Kubernetes deployment `nginx-deployment` to its previous revision.

---

## 🛠 Prerequisites
- Access to the jump host
- `kubectl` configured to communicate with the Kubernetes cluster

---

## 🔄 Rollback Deployment

Run the following command to revert to the previous version:

```bash
kubectl rollout undo deployment/nginx-deployment
```
## Screenshots

<img width="1040" height="466" alt="image" src="https://github.com/user-attachments/assets/458d9d1e-23c5-4dd6-9350-4d6795e696bc" />
<img width="1038" height="483" alt="image" src="https://github.com/user-attachments/assets/a35c8908-1494-43fe-8efe-a48802a8dff5" />



