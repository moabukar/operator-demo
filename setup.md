# Operator Demo

## Setup

```bash
kubebuilder init --domain moabukar.co.uk --repo moabukar.co.uk/operator-demo

kubebuilder create api --group webapp --version v1 --kind OperatorDemo

make install

make run

kubectl apply -k config/samples

make docker-build docker-push IMG=docker.io/moabukar/operator-demo:latest

make deploy IMG=docker.io/moabukar/operator-demo:latest

# cleanup
make uninstall
make undeploy
```
