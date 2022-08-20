# A Mono-repository for ACM repo examples

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
oc apply -f acm/02_apps/parksmap

# spring-petclinic
oc apply -f acm/02_apps/petclinic
```