# setup-k3sup

Setup a k3s cluster with k3sup

Usage:

```yaml
    steps:
      - uses: actions/checkout@v4

      - name: Setup Kubernetes
        uses: self-actuated/setup-k3sup@v1
          
      - name: Get nodes
        run: |
          export KUBECONFIG=~/.kube/config
          kubectl get nodes -o wide
```

The k3sup binary can be cached if desired:

```yaml
        with:
          cache: 'true'
```

## Todo

* Add input for `--k3s-channel`
* Add input for skipping Traefik

