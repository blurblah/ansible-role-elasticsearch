# ansible-role-elasticsearch

Tested on Ansible 2.4.2 and Ubuntu 16.04

This role depends on a
[docker](https://github.com/blurblah/ansible-role-docker) role and installs elasticsearch running on a docker container.

Referenced by a
[Install Elastic with Docker](https://www.elastic.co/guide/en/elasticsearch/reference/6.2/docker.html) document.

## Playbook sample
This sample playbook installs production mode single es instance versioned 6.2.3 with the name, sample_cluster.

* **cluster.name (optional)** : default is es_cluster
* **version (optional)** : default is 6.2.3

```yaml
- hosts: es_host
  become: yes
  roles:
    - role: elasticsearch
      cluster:
        name: sample_cluster
```
