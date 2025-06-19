# workshopinstall

1. Install the OpenShift GitOps Operator

```
oc apply -f https://raw.githubusercontent.com/mostmark/workshopinstall/refs/heads/main/add-openshift-gitops.yaml

```

2. Wait untill installed and ready, then add cluster role to user

```
oc adm policy add-cluster-role-to-user cluster-admin -z openshift-gitops-argocd-application-controller -n openshift-gitops

```

3. Install the workshop infra components

```
oc apply -f https://raw.githubusercontent.com/bmeklund/workshop-install/refs/heads/main/argocd/workshop-infra.yaml

```
