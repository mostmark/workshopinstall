# workshopinstall

1. Install the OpenShift GitOps Operator

```
oc apply -f https://raw.githubusercontent.com/mostmark/workshopinstall/refs/heads/main/add-openshift-gitops.yaml

```

2. Install the Gitea Operator

```
oc apply -f https://raw.githubusercontent.com/mostmark/workshopinstall/refs/heads/main/gitea.yaml

```

3. Install the workshop infra components

```
oc apply -f https://raw.githubusercontent.com/mostmark/workshopinstall/refs/heads/main/workshop-infra.yaml

```
