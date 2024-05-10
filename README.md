# setup-k3sup

Setup a k3s cluster with k3sup

Usage:

```yaml
    steps:
      - uses: actions/checkout@v4

      - name: Setup Kubernetes
        uses: self-actuated/setup-k3sup@master
        with:
          cache: 'true'
          
      - name: Get nodes
        run: |
          export KUBECONFIG=~/.kube/config
          kubectl get nodes -o wide
```

## Todo

* Add input for `--k3s-channel`
* Add input for skipping Traefik

