# kubectl

> How to use kuber command line client

- List of namespaces
`kubectl get namespace`

- Create namespace
`kubectl create namespace {{name}}`

- List of deployments
`kubectl get deployment`

- List of pods
`kubectl get pod`

- List of replicasets
`kubectl get replicaset`

- How to forward port from pod
`kubectl port-forward {{pod_name}} {{port}}`

- Set default namespace for context
`kubectl config set-context {{my-context}} --namespace={{mystuff}}`

- Use context
`kubectl config use-context {{my-context}}`
