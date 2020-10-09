# k8s Toolbox
This is a toolbox for various testing and troubleshooting on Kubernetes.   
I use it on kubernetes to verify networking et.al.

# Run In Kubernetes
kubectl run -ti --rm toolbox-$RANDOM --image=ludwigprager/k8s-toolbox:1

# Run In Docker
docker run -ti \
  --name toolbox \
  ludwigprager/k8s-toolbox:1 \
  /bin/bash

or

docker exec -ti toolbox /bin/sh

# Build The Image Yourself
source set-env.sh
docker build -t $K8S_TOOLBOX_IMAGE .
