ASBRL-PROMETHEUS
=========

Deploy a Prometheus as a Docker container.

Requirements
------------

Need to be Docker engine installed.

Role Variables
--------------

- default_user: 'ubuntu'
- TZ: 'Etc/GMT'
- BUILD: 'v2.20.1'
- RETENTION_TIME: '30d'
- SCRAPE_INTERVAL: '15s'
- EVALUATION_INTERVAL: '15s'
- MYSQL_HOSTS: ''
- LINUX_HOSTS: ''
- PG_HOSTS:  ''
- MONGO_HOSTS: ''  

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

      - name: Deploy Prometheus
        include_role:
          name: asbrl-prometheus
        vars:
          LINUX_HOSTS: "{{ PROM_LINUX_HOSTS }}"
          MONGO_HOSTS: "{{ PROM_MONGO_HOSTS }}"
          PG_HOSTS: "{{ PROM_PG_HOSTS }}"
        tags:
          - prometheus

License
-------

BSD

Author Information
------------------

Moegui.com
