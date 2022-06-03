# flux

## Setting up flux on WSL

### Download latest flux

```bash
curl --silent "https://api.github.com/repos/fluxcd/flux2/releases/latest" | grep -o "https://.*linux_amd64.tar.gz" | xargs curl -Lo ./flux_linux_amd64.tar.gz
tar xzf ./flux_linux_amd64.tar.gz
mv flux ~/.local/bin/flux
```

### Add bash completion
```bash
mkdir -p ~/.local/share/bash-completion/completions
flux completion bash > ~/.local/share/bash-completion/completions/flux
```

## Links

- https://fluxcd.io/docs/installation/#github-and-github-enterprise
- https://github.com/stefanprodan/gitops-istio
