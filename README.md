Logstash Forwarder
========

Installs Logstash Forwarder.

Installation
--------------

`ansible-galaxy install palkan.logstash-forwarder`

Role Variables
--------------

`defaults/main.yml`

| Name                        | Default Value |  Description    |
|-----------------------------|---------------|-----------------|
| logstash_forwarder.pkg_url              | "http://s3-eu-west-1.amazonaws.com/tbfiles/pkg/logstash-forwarder_0.4.0_amd64.deb"        | Package url |
| logstash_forwarder.servers               | [] | A list of servers to send logs to |
| logstash_forwarder.files               | [] | A list of files to watch |
| logstash_forwarder.timeout               | 15 |  |
| logstash_forwarder.ssl_crt               | '' | Path to ssl certificate |
| logstash_forwarder.ssl_key               | '' | Path to ssl key |


Example Playbook
-------------------------

  - hosts: servers
    roles:
       - palkan.logstash-forwarder