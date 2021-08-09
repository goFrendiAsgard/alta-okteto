# Getting started with Okteto (Kubernetes)

* Download kubectl from kubernetes's official website
* Create Okteto account (cloud.okteto.com)
* Go to setting, download kubernetes credential
* Set `KUBECONFIG` environment: 
    - Powershell (windows) user: `$Env:KUBECONFIG=("$HOME\Downloads\okteto-kube.config;$Env:KUBECONFIG;$HOME\.kube\config")`
* Check your current kubectl config: `kubectl config current-context`

# Example

* https://github.com/kubernetes/examples/tree/master/guestbook
* Apply: `kubectl apply -f manifest`
* See resources:
    - `kubectl get pods`
    - `kubectl get services`
    - `kubectl get ingress`
    - `kubectl get nodes`
* Port forwarding
    - `kubectl port-forward service/guestbook 8080:3000` (kubectl port-forward `<service>` `<local-port>:<remote-port>`)
    