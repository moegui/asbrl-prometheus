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
- CADVISOR_HOSTS: ''  
- TRAEFIK_HOSTS: ''
- CONTAINER_NAME: "prometheus"
- DOCKER_CPU_PERIOD: 0
- DOCKER_CPU_QUOTA: 0
- DOCKER_MEMORY: 0
- CONTAINER_STATE: 'started'
- VOLUME_STATE: 'present'
- DOCKER_LABELS:
    tag1: test
- DOCKER_PUBLISHED_PORTS:
    - "9090:9090"
- DOCKER_EXPOSED_PORTS:
    - "9090"

Dependencies
------------

None

Example Playbook
----------------

      - name: Deploy Prometheus
        include_role:
          name: asbrl-prometheus
        vars:
          LINUX_HOSTS: "{{ PROM_LINUX_HOSTS }}"
          MONGO_HOSTS: "{{ PROM_MONGO_HOSTS }}"
          PG_HOSTS: "{{ PROM_PG_HOSTS }}"
        tags:
          - asbrl-prometheus

License
-------

BSD

Author Information
------------------

Moegui.com
