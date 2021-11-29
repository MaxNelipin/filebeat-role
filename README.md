kibana-role
=========

Роль  установки filebeat на rpm-системы

Requirements
------------

Role Variables
--------------
| Variable name | Default | Description |
|-----------------------|----------|-------------------------|
| filebeat_version | "7.15.0" | Версия Kibana |
| el_instance_ip | "{{hostvars['el-instance']['ansible_facts']['default_ipv4']['address']}}" | IP-адрес сервера Elasticsearch |
| kb_instance_ip |"{{ hostvars['kb-instance']['ansible_facts']['default_ipv4']['address'] }}" | IP-адрес сервера Kibana |
| supported_systems |  | Список поддерживаемых ОС |


Dependencies
------------

Example Playbook
----------------


    - hosts: servers
      roles:
         - { role: filebeat-role, filebeat_version: 7.15.1, el_instance_ip: 10.1.1.1, kb_instance_ip: 10.1.1.2  }

License
-------

BSD

Author Information
------------------

MaxNelipin