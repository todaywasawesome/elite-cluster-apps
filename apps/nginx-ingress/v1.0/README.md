ingress-nginx-3.29.0

helm template nginx-ingress ingress-nginx --namespace kube-system \
--set controller.service.loadBalancerIP=10.0.0.22 \
--set defaultBackend.enabled=false \
--repo https://kubernetes.github.io/ingress-nginx


helm upgrade nginx-ingress ingress-nginx --namespace kube-system \
--set controller.service.loadBalancerIP=10.0.0.24 \
--set defaultBackend.enabled=false \
--repo https://kubernetes.github.io/ingress-nginx \
--dry-run
