Demo app of a simple flask application that I am trying to deploy in a kubernetes cluster.

I am using my powdermaps.com domain to play around, the kubernetes cluster is from DigitalOcean.

### Flask app
github repo: https://github.com/mrasap/flask

The front end is a simple flask app. It creates a simple sqlite database with a counter. The flask app has two paths:    
- `/` shows the counter
- `/increase` increases the counter

### Kubectl CLI 101
Guide used: https://www.digitalocean.com/docs/kubernetes/how-to/connect-with-kubectl/   
Documentation: https://kubernetes.io/docs/   

Download the kubeconfig.yaml file from digital ocean. This yaml file is used to gain access to the kubernetes cluster. Kubectl will look for a config file in ~/.kube and automatically use it to access the cluster. `kubectl version` will also give you the version running on the kubernetes cluster if your config file is setup correctly in ~/.kube. Otherwise, you can also give this config file as a parameter for your kubectl commands using the `--kubeconfig="path/to/kubeconfig.yaml"` flag.   

`kubectl --kubeconfig="flask-kubeconfig.yaml" get nodes` will show you a list of all the nodes using the flask-kubeconfig.yaml file.   

Alternatively, you can also create contexts to store multiple cluster config files: https://kubernetes.io/docs/tasks/access-application-cluster/configure-access-multiple-clusters/


### Helm templating
github repo: https://github.com/mrasap/flask-kubernetes-helm/


### Roadmap of features
[X] Flask demo web app   
[X] Git version control   
[X] Containerized the web app with docker   
[X] Multistage docker container with alpine as base to minimize the size   
[X] non-root user running in the container
[X] Dockerhub repo automatic builds   
[X] Orchestrate the app with kubernetes   
[ ] Templated the deployment with helm   
[ ] Automated the complete deployment with a bash script   
[ ] Ingress load balancer with nginx-ingress   
[ ] TLS support with cert-manager   
[ ] Upgrade cert-manager to latest build   
[ ] Kubernetes StateFulSet   
[ ] Kubernetes namespaces   
[ ] Kubernetes rbac   
[ ] Postgresql for persistent data   
[ ] Redis for caching   
[ ] ELK stack for logging   
[ ] Prometheus for monitoring?   
[ ] Unittests   
[ ] Jenkins CI pipeline   
[ ] Deployment with Spinnaker   

