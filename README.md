Demo app of a simple flask application that I am trying to deploy in a kubernetes cluster.

I am using my powdermaps.com domain to play around, the kubernetes cluster is from DigitalOcean.

### Flask app
github repo: https://github.com/mrasap/flask

The front end is a simple flask app. It creates a simple sqlite database with a counter. The flask app has two paths:    
- `/` shows the counter
- `/increase` increases the counter

### Kubernetes manifests
github repo: https://github.com/mrasap/flask-kubernetes/


### Helm templating
github repo: https://github.com/mrasap/flask-kubernetes-helm/
