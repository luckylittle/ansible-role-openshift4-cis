ansible-role-openshift4-cis
=========

Based on [CIS Kubernetes Benchmark v1.5.1.](docs/CIS_Kubernetes_Benchmark_v1.5.1.pdf).

Requirements
------------

Tested on ansible `2.9.4`

Role Variables
--------------

* `scored`
* `not_scored`

Dependencies
------------

Unknown at the moment

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: localhost
  roles:
    - ansible-role-openshift4-cis
```

License
-------

MIT

Author Information
------------------

Lucian Maly <<lucian@redhat.com>>

Some inspiration from [this source](https://github.com/aquasecurity/kube-bench/tree/5f34058dc789e481ccc3b49248ebb02763bdce40/cfg/rh-0.7) was used.
