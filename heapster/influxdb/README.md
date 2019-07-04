#Here are the problems encountered

###heapster-7bb7cf984f-9956v               0/1     Pending   0

[root@Master01 ~]# kubectl describe pod heapster-7bb7cf984f-9956v 

Events:
  Type     Reason            Age                 From               Message
  ----     ------            ----                ----               -------
  Warning  FailedScheduling  11s (x6 over 4m2s)  default-scheduler  0/1 nodes are available: 1 node(s) had taints that the pod didn't tolerate.

Slove:

kubectl taint nodes --all node-role.kubernetes.io/master-

### kubectl logs heaspter 

E0704 07:09:05.012867       1 manager.go:101] Error in scraping containers from kubelet:192.168.137.41:10250: failed to get all container stats from Kubelet URL "https://192.168.137.41:10250/stats/container/": request failed - "403 Forbidden", response: "Forbidden (user=system:serviceaccount:kube-system:heapster, verb=create, resource=nodes, subresource=stats)"

Slove

kubectl edit clusterrole system:heapster

rules:

- apiGroups:

  - ""

  resources:

  - events

  - namespaces

  - nodes

  - pods

  - nodes/stats

  verbs:

  - get

  - list

  - watch

  - create

- apiGroups:

  - extensions

  resources:

  - deployments

  verbs:

  - get

  - list

  - watch


