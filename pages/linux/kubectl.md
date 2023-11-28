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

- Delete pod
`kubectl delete pod {{pod_name}}`

- List of containers inside pod
`kubectl get pod {{pod_name}} -o jsonpath="{.spec['initContainers','containers'][*].name}"`
