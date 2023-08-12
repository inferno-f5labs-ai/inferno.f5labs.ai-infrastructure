ArgoCD sync order for DeployKF

```Bash
argocd app sync "deploykf-app-of-apps"
argocd app sync -l "app.kubernetes.io/component=deploykf-dependencies"
argocd app sync -l "app.kubernetes.io/component=deploykf-core"
argocd app sync -l "app.kubernetes.io/component=deploykf-opt"
argocd app sync -l "app.kubernetes.io/component=deploykf-tools"
argocd app sync -l "app.kubernetes.io/component=kubeflow-dependencies"
argocd app sync -l "app.kubernetes.io/component=kubeflow-tools"
```
