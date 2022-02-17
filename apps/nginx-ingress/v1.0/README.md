ingress-nginx-3.29.0

helm upgrade --install nginx-ingress ingress-nginx/ingress-nginx --namespace kube-system
--set controller.service.loadBalancerIP=10.0.0.22
--set defaultBackend.enabled=false