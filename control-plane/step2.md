Nun werden wir uns die `kube-apiserver-master` Komponente genauer anschauen.

Natürlich kann es immer vorkommen, dass man sich eine Komponente genauer ansehen und dabei die Logs überprüfen möchte.

Die kann man sehr einfach mit dem Command `kubectl logs kube-apiserver-master`{{execute HOST1}}. Du siehst die Meldung

```sh
Error from server (NotFound): pods "kube-apiserver-master" not found
```

Probier es nochmal und spezifiziere dabei den Namespace kube-system `kubectl logs kube-apiserver-master -n kube-system`{{execute HOST1}}. Nun siehst du die logs von `kube-apiserver-master`.

Gehe weiter zum nächsten Schritt und probiere es selbst.