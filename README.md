# k8-admin
```
step1: Creating a IAM role.
```
```
step2: creating a policy for the role. ( describe cluster)
```
```
step3: create role , rolebinding 
```
* note: Role and rolebinding is for namespace resouce level access. eg: pods,services,deployments etc.

```
step4: intergarting IAM with eks using aws-auth configmap from kube-system namespace.
make some configuration code changes in it .
adding mapUser:|
       - groups:
         - # role name
        userarn: 
        username: 
```



