# virt-dv-scale-density
Batched VM density test including DataVolume clones (using VolumeSnapshot per namespace)

# Introduction

The motivation for this test is very similar to kube-burner-ocp's [virt-clone](https://github.com/kube-burner/kube-burner-ocp?tab=readme-ov-file#virt-clone) test as well as this original [VM deployment writeup](https://developers.redhat.com/articles/2024/09/04/use-kube-burner-measure-red-hat-openshift-vm-and-storage-deployment-scale).

However this specific config was designed for a very high scale test with the ability to control "batching" timing by introducing a wait after each namespaced iteration.

# Running

Requires kube-burner-ocp tool: https://github.com/kube-burner/kube-burner-ocp/releases

Currently the config requires an ES server although it could be modified for "Local" indexing. See the kube-burner docs for more info: https://kube-burner.github.io/kube-burner/latest/

Example run cmd to reach 10K VMs / 10K PVCs:

```
ES_INDEXING=true ES_INDEX="ripsaw-kube-burner" ES_SERVER="https://yourESserver:443" ITERATIONS=20 OBJ_REPLICAS=500 kube-burner-ocp init  -c dvvmclone.yml
```
