#### Project to install a simple flask app on kubernetes

The front end is a simple flask app. It creates a simple sqlite database with a counter. The flask app has two paths:    
- `/` shows the counter
- `/increase` increases the counter


Currently implemented:
- Docker multistage container
- Docker non-root user
- Kubernetes deployment


Will implement:   
- Helm
- HTTPS
- StateFull volumes
- Jenkins CI/CD?
- Spinnaker?