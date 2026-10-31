# kriemhild
ArgoCD manifsts for kriemhild.

# ArgoCD Autopilot patch
```
argocd-autopilot repo bootstrap --app 'github.com/jthetzel/kriemhild/manifests?ref=main'
git pull
```
  Preview with a server-side dry run first:
  kubectl --context <ctx> apply --server-side --force-conflicts --dry-run=server \
    -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml \
    -l app.kubernetes.io/name=applicationsets.argoproj.io

  Then apply for real by dropping --dry-run=server:
  kubectl --context <ctx> apply --server-side --force-conflicts \
    -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml \
    -l app.kubernetes.io/name=applicationsets.argoproj.io
