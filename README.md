# GitOps for OpenShift4 with Argo CD 


## Install GitOps Operator

~~~
oc apply -f https://github.com/mabehiro/ocp-gitops/main/gitops-cluster/gitops-operator.yaml -n openshift-operators
oc project openshift-gitops
oc adm policy add-cluster-role-to-user cluster-admin -z openshift-gitops-argocd-application-controller
~~~


## Apps of App

~~~
oc apply -f https://github.com/mabehiro/ocp-gitops/main/gitops-cluster/app-of-apps.yaml
~~~
