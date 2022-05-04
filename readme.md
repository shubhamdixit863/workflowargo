# Argo WorkFlow POC

Running Microservice workflow in Argo

## Installation

Make sure you have kubernetes cluster running on your machine ,for local deployment you can use minikube or K3s

```bash
kubectl create ns argo
kubectl apply -n argo -f https://raw.githubusercontent.com/argoproj/argo-workflows/master/manifests/quick-start-postgres.yaml

```

## Usage
Port forwarding is required to view the argo workflow ui on your localhost ,visit http://localhost:2746
``` 
kubectl -n argo port-forward deployment/argo-server 2746:2746

```
Run the curl commands mentioned in the workflowapi.txt files to see it working


## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)