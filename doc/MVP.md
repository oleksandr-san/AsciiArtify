# MVP

1. Login to Argo CD UI
2. Create new application
    2.1 Source type: Git
    2.2 Repository URL: https://github.com/den-vasyliev/go-demo-app
    2.3 Path: helm
    2.4 Target revision: HEAD
    2.5 Destination: default, namespace - demo
3. Launch application sync
4. Check application status