# osm_elasticSearch
This repo controls the Ansible Role for ElasticSearch.

# Role Name
osm_elasticSearch

# Prerequisites
The only prerequisites is that java is installed on that machine in which you want to install elasticsearch.

# Variables/Default for elasticsearch

 This role was built using [Variables](https://github.com/opstree-ansible/osm_elasticSearch/blob/release-1.0/vars/main.yml).

# Example Playbook

```
- hosts: "{{ host }}"
  roles:
     - { role: osm_elasticSearch }
```

# License

BSD
