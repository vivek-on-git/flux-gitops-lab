
--kind directory
flux bootstrap github \
  --owner=vivek-on-git \
  --repository=flux-gitops-lab \
  --branch=main \
  --path=clusters/kind \
  --personal
  
  
--- eks directory
flux bootstrap github \
  --owner=vivek-on-git \
  --repository=flux-gitops-lab \
  --branch=main \
  --path=clusters/eks \
  --personal


### Install Flux operator
helm install flux-operator \
  oci://ghcr.io/controlplaneio-fluxcd/charts/flux-operator \
  --namespace flux-system \
  --create-namespace
  
### Install Flux Instance
kubectl apply -f clusters/eks/flux-system/flux-instance.yaml
