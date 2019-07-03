# k8s-monitoring

## Prerequisites
- Minikube
- Kubectl

## Bootstrap
` minikube start --cpus 2 --memory 5000 `

- I'm going to install the monitoring components into a "monitoring" namespace. While this is not necessary, it does show "best practices" in organizing applications by namespace rather than deploying everything into the default namespace.
`kubectl create -f monitoring-ns.yaml`
`kubectl create -f node_exporter_ds.yaml`
`kubectl create -f prometheus.yaml`
`kubectl create -f grafana.yaml`
