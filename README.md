simple Kubernetes Demo to show
- deployinging nginx
- exposing to service
- routing traffic via ingress

Prerequites
- minikube
- kubectl
- 

```bash
minikube start
minikube addons enable ingress
kubectl apply -f k8s/
MINI_IP=$(minikube ip)
echo "$MINI_IP hello.local" | sudo tee -a /etc/hosts
curl -I http://hello.local/
