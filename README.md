# ansible-collections

## Ansible collections repository

### homezone.desktop

Cette collection permet la d'installer un poste développeur.

Liste des outils installés :

- minikube

en cours :

- kubectl                        
- helm, helmfile
- kustomize
- k9s
- argocd
- golang


### Testing

```bash
$ cd testing
$ make ansible
```


### Build collections

```bash
$ ./build.sh
$ Created collection for homezone.desktop at ansible-collections/homezone-desktop-1.0.0.tar.gz
```

### Usage

requirements.yml

```yaml
collections:
  - name: https://github.com/laurentpoirierfr/ansible-collections.git
    type: git
    version: main
```
