# kriemhild
ArgoCD manifsts for kriemhild.

# ArgoCD Autopilot patch
```
argocd-autopilot repo bootstrap --app 'github.com/jthetzel/kriemhild/manifests?ref=main'
git pull
