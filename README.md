WIP -- ansible-role-openshift4-cis
=========

Based on [CIS Kubernetes Benchmark v1.5.1](docs/CIS_Kubernetes_Benchmark_v1.5.1.pdf) [14 Feb 2020].

Requirements
------------

Tested on ansible `2.9.4`. It also requires `kubectl` for the category `5` tasks.

Role Variables
--------------

* `scored`
* `not_scored`
* `level_1`
* `level_2`
* `path_to_cni_files`
* `proxy_kubeconfig_file`
* `client_ca_file`
* `kubelet_config`

Dependencies
------------

Unknown at the moment

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

* `requirements.yml`:

```yaml
- src: https://github.com/luckylittle/ansible-role-openshift4-cis
  version: master
```

* `playbook.yaml`:

```yaml
- hosts: all
  remote_user: core
  roles:
    - ansible-role-openshift4-cis
```

* Execution:

```bash
ansible-galaxy install --force -r requirements.yml -p roles/
ansible-playbook -i inventory
```

The `inventory` must contain specific host groups, that the role relies on:

```ini
[localhost]
localhost

[masters]
master[0:2]

[etcd:children]
masters

[workers]
worker[0:4]
```

License
-------

MIT

Author Information
------------------

Lucian Maly <<lucian@redhat.com>>

Some inspiration from [this source](https://github.com/aquasecurity/kube-bench/tree/5f34058dc789e481ccc3b49248ebb02763bdce40/cfg/rh-0.7) was used.

---

_Last update: Mon Mar 30 04:25:20 UTC 2020_
