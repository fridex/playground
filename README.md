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
