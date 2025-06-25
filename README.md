# workshopinstall

1. Install the OpenShift GitOps Operator

```
oc apply -f https://raw.githubusercontent.com/bmeklund/workshop-install/refs/heads/main/add-openshift-gitops.yaml

```

2. Install the workshop infra components

```
oc apply -f https://raw.githubusercontent.com/bmeklund/workshop-install/refs/heads/main/argocd/workshop-infra.yaml

```
