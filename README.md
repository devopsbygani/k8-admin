# k8-admin

## Step-by-step Guide

### Step 1: Creating an IAM Role
Create an IAM role from the AWS console.

---

### Step 2: Creating a Policy for the Role
Create a policy for the role that allows describing the EKS cluster. and attching the policy to user

---

### Step 3: Create Role and RoleBinding
Create a Kubernetes Role and RoleBinding.

> **Note:**  
> Role and RoleBinding are used for namespace-level resource access, e.g., for pods, services, deployments, etc.

---

### Step 4: Integrating IAM with EKS using `aws-auth` ConfigMap
Edit the `aws-auth` ConfigMap from the `kube-system` namespace to map the IAM user or role.

Make configuration code changes like this:

```yaml
mapUsers: |
  - groups:
      - <role-name>
    userarn: <enter value here>
    username: <enter value here>

* reference : https://github.com/keikoproj/aws-auth.git


