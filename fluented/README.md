#kubernetes-podlogging-fluented-elasticsearch-kibana

###kubernetes-pod日志收集-分析系统

##部署步骤

1 安装部署elasticsearch

$ kubectl create -f {path}/es-statefulset.yaml

2 创建es-service

$ kubectl create -f {path}/es-service.yaml

3 部署fluented的ConfigMap

$ kubectl create -f {path}/fluentd-es-configmap.yaml

4 部署Fluented

$ kubectl create -f {path}/fluentd-es-ds.yaml

5 部署kibana

$ kubectl create -f {path}/kibana-deployment.yaml

6 部署kibana代理服务