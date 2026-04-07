# Day-7 : Deploy ReplicaSet in Kubernetes Cluster

## 📌 Objective
Deploy a ReplicaSet in a Kubernetes cluster using the `httpd:latest` image.

---

## 🧾 Requirements

- **ReplicaSet Name:** `httpd-replicaset`
- **Image:** `httpd:latest`
- **Replicas:** `4`
- **Container Name:** `httpd-container`
- **Labels:**
  - `app: httpd_app`
  - `type: front-end`

---

## 📄 ReplicaSet YAML

```yaml
apiVersion: apps/v1
kind: ReplicaSet
metadata:
  name: httpd-replicaset
  labels:
    app: httpd_app
    type: front-end
spec:
  replicas: 4
  selector:
    matchLabels:
      app: httpd_app
  template:
    metadata:
      labels:
        app: httpd_app
        type: front-end
    spec:
      containers:
      - name: httpd-container
        image: httpd:latest
```

### 🚀 Deployment Steps

1. Create the YAML file
```
vi httpd-replicaset.yaml
```
Paste the YAML content and save the file.

2. Apply the configuration
```
kubectl apply -f httpd-replicaset.yaml
```
3. Verify the ReplicaSet
```
kubectl get rs
```
4. Verify the Pods
```
kubectl get pods -l app=httpd_app
```
## 🔍 Expected Outcome
- A ReplicaSet named httpd-replicaset is created.
- 4 pods are running using the httpd:latest image.
- Pods are labeled correctly and managed by the ReplicaSet.

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/6ad577bd-15af-46b6-9a19-f81aeb679df8" />


