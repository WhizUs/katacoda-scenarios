Übungen zur Control Plane in Kubernetes.

Die Kubernetes Control Plane hat Master Komponenten

kube-apiserver 
etcd
kube-scheduler
kube-controller-manager
cloud-controller-manager (nur bei Cloud Provider existent)

und Node Komponenten

kubelet
kube-proxy
Container Runtime (Docker, containerd, cri-o, rktlet and any implementation of the Kubernetes CRI)

In diesem Tutorial lernst du wie du dir eine Übersicht über die Control Plane Komponenten deines Clusters machst und wie du diese im Fehlerfall analysierst.