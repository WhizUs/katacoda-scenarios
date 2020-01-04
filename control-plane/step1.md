Zuerst werden wir den Status der Control Plane Elemente überprüfen und schauen wo wir diese in Kubernetes finden.

Wenn wir `kubectl get all`{{execute HOST1}} auf dem Master Node ausführen sehen wir nur einen service laufen und finden nicht die vorhin beschriebenen Master Komponenten. Das liegt darin, dass die Control Plane Komponenten in einem eigenen Namespace laufen `kube-system`.

Daher probieren wir den Command noch einmal mit folgender Änderung `kubectl get all -n kube-system`{{execute HOST1}}. Nun ist schon deutlich mehr zu sehen.

Zur besseren Übersicht betrachten wir nun einmal nur die Pods `kubectl get pods -n kube-system`{{execute HOST1}}. Der Output sollte nun ähnlich dem Folgenden aussehen:

```sh
etcd-master                      1/1     Running   0          9m33s
kube-apiserver-master            1/1     Running   0          9m34s
kube-controller-manager-master   1/1     Running   0          9m29s
kube-proxy-7nhlz                 1/1     Running   0          10m
kube-proxy-kjcpf                 1/1     Running   0          10m
kube-scheduler-master            1/1     Running   0          9m44s
```

Hier sehen wir schon deutlich die Master Komponenten. Unter anderem der apiserver den wir uns im nächsten Step genauer ansehen.