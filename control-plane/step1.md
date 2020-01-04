Zuerst werden wir den Status der Control Plane Elemente überprüfen und schauen wo wir diese in Kubernetes finden.

Wenn wir `kubectl get all`{{execute HOST1}} auf dem Master Node ausführen sehen wir nur einen service laufen und finden nicht die vorhin beschriebenen Master Komponenten. Das liegt darin, dass die Control Plane Komponenten in einem eigenen Namespace laufen `kube-system`.

Daher probieren wir den Command noch einmal mit folgender Änderung `kubectl get all -n kube-system`{{execute HOST1}}.

Zur besseren Übersicht betrachten wir nur die Podsm`kubectl get pods -n kube-system`{{execute HOST1}}