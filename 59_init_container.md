# Init containers in kubernetes
```
kubectl get pods
```
```
vi /tmp/init.yaml
```
```
apiVersion: apps/v1
kind: Deployment
metadata:
  name: ic-deploy-xfusion
  labels:
    app: ic-xfusion
spec:
  replicas: 1
  selector:
    matchLabels:
      app: ic-xfusion
  template:
    metadata:
      labels:
        app: ic-xfusion
    spec:
      volumes:
        - name: ic-volume-xfusion
          emptyDir: {}
      initContainers:
        - name: ic-msg-xfusion
          image: debian:latest
          command:
            [
              "/bin/bash",
              "-c",
              "echo Init Done - Welcome to xFusionCorp Industries > /ic/blog",
            ]
          volumeMounts:
            - name: ic-volume-xfusion
              mountPath: /ic

      containers:
        - name: ic-main-xfusion
          image: debian:latest
          command:
            [
              "/bin/bash",
              "-c",
              "while true; do cat /ic/blog; sleep 5; done",
            ]
          volumeMounts:
            - name: ic-volume-xfusion
              mountPath: /ic
```
```
cat /tmp/init.yaml

kubectl create -f /tmp/init.yaml

kubectl get deploy

kubectl get pods
```
*Wait for pods to get running*
```
kubectl logs -f ic-deploy-xfusion-5f8dbfd6f6-fz7zr

kubectl exec ic-deploy-xfusion-5f8dbfd6f6-fz7zr -- cat /ic/blog
```

