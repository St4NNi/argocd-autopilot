## argocd-autopilot repo bootstrap

Bootstrap a new installation

```
argocd-autopilot repo bootstrap [flags]
```

### Examples

```

# To run this command you need to create a personal access token for your git provider
# and provide it using:

    export GIT_TOKEN=<token>

# or with the flag:

    --git-token <token>

# Install argo-cd on the current kubernetes context in the argocd namespace
# and persists the bootstrap manifests to the root of gitops repository

    argocd-autopilot repo bootstrap --repo https://github.com/example/repo

# Install argo-cd on the current kubernetes context in the argocd namespace
# and persists the bootstrap manifests to a specific folder in the gitops repository

    argocd-autopilot repo bootstrap --repo https://github.com/example/repo/path/to/installation_root

```

### Options

```
      --app string                 The application specifier (e.g. github.com/argoproj-labs/argocd-autopilot/manifests?ref=v0.2.5), overrides the default installation argo-cd manifests
      --context string             The name of the kubeconfig context to use
      --dry-run                    If true, print manifests instead of applying them to the cluster (nothing will be commited to git)
  -t, --git-token string           Your git provider api token [GIT_TOKEN]
  -u, --git-user string            Your git provider user name [GIT_USER] (not required in GitHub)
  -h, --help                       help for bootstrap
      --hide-password              If true, will not print initial argo cd password
      --insecure                   Run Argo-CD server without TLS
      --installation-mode string   One of: normal|flat. If flat, will commit the bootstrap manifests, otherwise will commit the bootstrap kustomization.yaml (default "normal")
      --kubeconfig string          Path to the kubeconfig file to use for CLI requests.
  -n, --namespace string           If present, the namespace scope for this CLI request
      --provider string            The git provider, one of: gitea|github|gitlab
      --repo string                Repository URL [GIT_REPO]
      --request-timeout string     The length of time to wait before giving up on a single server request. Non-zero values should contain a corresponding time unit (e.g. 1s, 2m, 3h). A value of zero means don't timeout requests. (default "0")
```

### SEE ALSO

* [argocd-autopilot repo](argocd-autopilot_repo.md)	 - Manage gitops repositories

