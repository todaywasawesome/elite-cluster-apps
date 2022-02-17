metallb-2.3.5

helm install metallb stable/metallb --namespace kube-system
--set configInline.address-pools[0].name=default
--set configInline.address-pools[0].protocol=layer2
--set configInline.address-pools[0].addresses[0]=10.0.0.20-10.0.0.60