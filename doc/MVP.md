# MVP

1. Login to Argo CD UI
2. Create new application
  - Source type: Git
  - Repository URL: https://github.com/den-vasyliev/go-demo-app
  - Path: helm
  - Target revision: HEAD
  - Destination: default, namespace - demo
3. Launch application sync
4. Check application status