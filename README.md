# osm_elasticSearch
This repo controls the Ansible Role for ElasticSearch.

Role Name

A brief description of the role goes here.

Requirements

None

Role Variables

Available variables are listed below, along with default values(see vars/mail.yml):

java_tmp_storage: /tmp/java_install
__java_oracle_rpm: java8u131
__java_oracle_download: http://download.oracle.com/otn-pub/java/jdk/8u131-b11/d54c1d3a095b4ff2b6607d096fa80163/jdk-8u131-linux-x64.rpm

jvm_options: jvm.options.j2
common_session: common-session.j2
common_session_ni: common-session-noninteractive.j2
elasticsearch: elasticsearch.yml.j2
environment_template: environment.j2
limits: limits.conf.j2
cluster_name: production
node_name: localhost
path_to_data: /var/lib/elasticsearch 
path_to_logs: /var/log/elasticsearch
locked_memory: unlimited
network_host: '{{ ansible_eth1["ipv4"]["address"] }}'
http_port: 9200
elasticsearch_script_inline: true
elasticsearch_script_indexed: true

oracle_java_dir_source: '/usr/local/src'
oracle_java_set_as_default: yes
oracle_java_version: "8"
oracle_java_version_string: "1.{{ oracle_java_version }}.0_{{ oracle_java_version_update }}"
oracle_java_ansible_arch_mappings:
  x86_64: x64
  i386: i586
oracle_java_cache_valid_time: 3600
oracle_java_home: "/usr/lib/jvm/java-{{ oracle_java_version }}-oracle"
oracle_java_os_supported: yes
oracle_java_state: latest

Dependencies

None.

Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

- hosts: "{{ host }}"
  roles:
     - { role: osm_elasticSearch }
License

BSD

Author Information

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
