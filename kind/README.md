# kind

## Setting up kind on WSL

### Download latest kind

```bash
#curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.14.0/kind-linux-amd64
curl -Lo ./kind https://kind.sigs.k8s.io/dl/latest/kind-linux-amd64
chmod +x ./kind
mv kind ~/.local/bin/kind
```

### Add bash completion
```bash
mkdir -p ~/.local/share/bash-completion/completions
kind completion bash > ~/.local/share/bash-completion/completions/kind
```

### Create first cluster
```bash
kind create cluster --config cluster-config.yml
```

### Some other useful commands

#### List clusters
```bash
kind get clusters
```

#### Delete cluster
```bash
kind delete cluster wsl-kind-cluster
```

## Links

- https://kind.sigs.k8s.io/docs/user/quick-start/
- https://kind.sigs.k8s.io/docs/user/using-wsl2/

