# DevopsPro
Curso criado por- Fabricio Veronez

# Instalando o argocd sem HA
  raw.githubusercontent.com/argoproj/argo-cd/refs/heads/master/manifests/install.yaml

# Instalando argocd HA
  helm upgrade --install argocd argo/argo-cd --values ./values.yaml -n argocd --version 7.7.3

# Fazendo redirect
  kubectl port-forward service/argocd-server -n argocd 8080:443

# Pegando valor Secret
  kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
