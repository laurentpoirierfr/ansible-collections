# ansible-collections

## Ansible collections repository

### homezone.desktop

Cette collection permet la d'installer un poste développeur.

Liste des outils installés :

- minikube
- kubectl 

en cours :

- k9s
- helm, helmfile
- kustomize
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

#### requirements.yml

```yaml
collections:
  - name: https://github.com/laurentpoirierfr/ansible-collections.git
    type: git
    version: main
```

#### playbook.yml

```yaml
---
- hosts: localhost
  collections:
    - homezone.desktop
  roles:
    - role: community
    - role: minikube
  vars:
    community_dir: "~/Community"
    community_bin_dir: "{{ community_dir }}/bin"
    minikube_install_dir: "{{ community_bin_dir }}"
    minikube_version: '1.31.2'   
```