# MVP

1. Login to Argo CD UI
2. Create new application
  - Source type: Git
  - Repository URL: https://github.com/den-vasyliev/go-demo-app
  - Path: helm
  - Target revision: HEAD
  - Destination: default, namespace - demo
3. Launch application sync
4. Check application endpoint
```sh
kubectl port-forward -n mvp svc/ambassador 8088:80

curl -F 'image=@/workspaces/AsciiArtify/demo/argo.png' localhost:8088/img/
```

![Demo](../img/ArgoCD-MVP.gif)