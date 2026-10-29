In order to run flask-postgres app on kubernetes:

1. Start the kubernetes cluster (minikube, for instance, with 3 nodes)

`minikube start --nodes=3 --profile first`

2. Apply desired state to kubernetes cluster, by applying manifest files:

`kubectl apply -f . `

3. Create a route to load balancer service, in order to access it from host machine:

`minikube tunnel -p first`

    Open on http://localhost:5007/

3. To delete all resources, associated with this configuration, run:

`kubectl delete -f . `