# ansible-kubernetes
## Fork of https://github.com/gantsign/ansible-role-kubernetes

### Example of playbook

```yaml
---
- hosts: all
  roles:
    - kubernetes

- hosts: localhost
  gather_facts: yes
  roles:
    - { role: kubernetes_local_config, when: kubernetes_copy_config }
```