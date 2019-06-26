Ingress架构图

![image](https://github.com/boxrice007/kubernetes/blob/master/ingress/img/20181004153431230.png)

这个安装ingress的具体步骤

1 创建ingress-nginx namespace

kubectl create -f namespace.yaml

2 创建configmap

kubectl create -f configmap.yaml

3 创建default-backend

kubectl create -f default-backend.yaml

4 创建rbac

kubectl create -f rbac.yaml

5 创建nginx-ingress-controller

kubectl create -f with-rbac.yaml

6 创建TCP、UDP

kubectl create -f tcp-services-configmap.yaml

kubectl create -f udp-services-configmap.yaml

7 创建ingress-controller的service

kubectl create -f service-nodeport.yaml

8 创建ingress

kubectl create -f ingress-default-backend.yaml

测试

![image](https://github.com/boxrice007/kubernetes/blob/master/ingress/img/ingress.png)
