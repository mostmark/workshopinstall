# workshopinstall

1. Install the OpenShift GitOps Operator

```
oc apply -f https://raw.githubusercontent.com/mostmark/workshopinstall/refs/heads/main/add-openshift-gitops.yaml

```

2. Add cluster role to user

```
oc adm policy add-cluster-role-to-user cluster-admin -z openshift-gitops-argocd-application-controller -n openshift-gitops

```

3. Get the Argo password

```
argoPass=$(oc get secret/openshift-gitops-cluster -n openshift-gitops -o jsonpath='{.data.admin\.password}' | base64 -d)
echo $argoPass

```

4. Install the Gitea Operator

```
oc apply -f https://raw.githubusercontent.com/mostmark/workshopinstall/refs/heads/main/gitea.yaml

```

5. Install the workshop infra components

```
oc apply -f https://raw.githubusercontent.com/mostmark/workshopinstall/refs/heads/main/workshop-infra.yaml

```
