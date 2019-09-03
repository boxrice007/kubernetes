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

### 0/1 nodes are available: 1 node(s) had taints that the pod didn't tolerate.

kubectl taint nodes --all node-role.kubernetes.io/master-

# Bash-completion

## yum install -y bash-completion

## source /usr/share/bash-completion/bash_completion

## source <(kubectl completion bash)

## echo "source <(kubectl completion bash)" >> ~/.bashrc
 
