# Play the ground

Images are available on quay:

 - [torch-matmul](https://quay.io/repository/fridex/torch-matmul)
 - [tensorflow-matmul](https://quay.io/repository/fridex/tensorflow-matmul)

To build them, clone the repo and run:

```
 cd torch-matmul/
 podman build . -t quay.io/fridex/torch-matmul
```

```
 cd torch-matmul/
 podman build . -t quay.io/fridex/tensorflow-matmul
```

## To run in OpenShift

```
oc process -f job-template.yaml -p IMAGE="quay.io/fridex/torch-matmul:latest" -p CPU=1 -p MEMORY=1Gi | oc apply -f -
```

```
oc process -f job-template.yaml -p IMAGE="quay.io/fridex/tensorflow-matmul:latest" -p CPU=1 -p MEMORY=1Gi | oc apply -f -
```
