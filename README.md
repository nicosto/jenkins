# 

## install

```bash
$ kubectl create ns jenkins-operator
$ kubectl create ns jenkins
```

```bash
$ kubectl -n jenkins-operator apply -f operator/service_account.yaml
$ kubectl -n jenkins-operator apply -f operator/role_binding.yaml
$ kubectl -n jenkins-operator apply -f operator/role.yaml
```

```bash
$ kubectl -n jenkins apply -f controller/role.yaml
$ kubectl -n jenkins apply -f controller/role_binding_jenkins.yaml
```

```bash
$ kubectl -n jenkins -n jenkins-operator apply -f operator/operator.yaml
```

