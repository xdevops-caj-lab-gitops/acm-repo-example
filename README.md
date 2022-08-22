# A Mono-repository for ACM repo examples

## 前提条件

已经在Hub Cluster上安装好ACM，并用ACM纳管以下集群：
- `ocp1`

Lab Env:
- OpenShift 4.10.24
- OpenShift ACM Operator 2.5.1

## Create ACM applications

Run below commands on Hub Cluster.

Create namespaces:
```bash
oc apply -f acm/01_namespaces
```

Create channels:
```bash
oc apply -f acm/02_channels
```

Create applications:
```bash
# parksmap
oc apply -f acm/03_apps/parksmap

# spring-petclinic
oc apply -f acm/03_apps/spring-petclinic
```

## Clean Up

Clean up previous created resources after testing.
```bash
oc delete project parksmap
oc delete project spring-petclinic
```

## References

- [ACM Product Document](https://access.redhat.com/documentation/en-us/red_hat_advanced_cluster_management_for_kubernetes/2.5)
- [Open Cluster Management](https://open-cluster-management.io/)