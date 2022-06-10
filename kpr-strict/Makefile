deploy:
	kind create cluster --config cluster.yaml
	./render-values.sh
	helm -n kube-system install cilium cilium/cilium -f values.yaml

destroy:
	kind delete clusters example-kpr-base
	rm -f values.yaml
