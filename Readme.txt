
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
