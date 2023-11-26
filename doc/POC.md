# POC

## [Argo CD](https://youtu.be/wnxkhadK5AY)

1. Start cluster
```
k3d cluster create argocd-poc
```

2. Install Argo CD¶

```sh
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

3. Get admin password
```sh
kubectl get secret -n argocd argocd-initial-admin-secret -o jsonpath={.data.password} | base64 --decode
```

4. Enter Argo CD UI
```sh
kubectl port-forward svc/argocd-server -n argocd 8080:443
```

![Demo](ArgoCD-POC.gif)