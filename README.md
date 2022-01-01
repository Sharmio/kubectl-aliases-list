# kubectl-aliases-list
Kubectl aliases for daily use
## Kubectl autocomplete

### BASH

```bash
source <(kubectl completion bash) # setup autocomplete in bash into the current shell, bash-completion package should be installed first.
echo "source <(kubectl completion bash)" >> ~/.bashrc # add autocomplete permanently to your bash shell.
```

You can also use a shorthand alias for `kubectl` that also works with completion:

```bash
alias k=kubectl
complete -F __start_kubectl k
```

### ZSH

```bash
source <(kubectl completion zsh)  # setup autocomplete in zsh into the current shell
echo "[[ $commands[kubectl] ]] && source <(kubectl completion zsh)" >> ~/.zshrc # add autocomplete permanently to your zsh shell
### Examples
```

### Creating Object 
```sh
alias k='kubectl'
alias kc='kubectl create'
alias kcf='kubectl create -f'     

# creating clusterrole
alias kccr='kubectl create clusterrole' #kubectl create clusterrole pod-reader --verb=get,list,watch --resource=pods
clusterrolebinding
alias kccr='kubectl create clusterrole' #kubectl create clusterrole pod-reader --verb=get,list,watch --resource=pods

```
