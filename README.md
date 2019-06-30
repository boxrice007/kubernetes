# Kubernetes
## use kubeadm create kubernetes
### kubeadm init --kubernetes-version=1.15.0 \

### --apiserver-advertise-address=192.168.137.161 \

### --image-repository registry.aliyuncs.com/google_containers \

### --service-cidr=10.1.0.0/16 --pod-network-cidr=10.244.0.0/16

note:
apiverver: local address

image-repository: aliyun repository

service-cidr: cluster ip

pod-netwokr-cidr: pod ip
