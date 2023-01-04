Role docker_teamspeak
=========

This role configures and starts docker-composed based teamspeak servers.

Role Variables
--------------

```yaml
ts_releases_image: "3.13.7"
ts_container_state: 'present'

ts_volumes_local_path: "/teamspeak"

ts_variables_local_path: ""

# a default server instance
docker_teamspeak_servers:
  - server: ts3server
    voice_server_port: 9987
    server_query_port: 10077
    file_transfer_port: 30033
    restart: always
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
  - name: Setup TeamSpeak with docker
    hosts: localhost
    connection: local
    become: true
    gather_facts: true

    tasks:
      - name: Setup TeamSpeak
        include_role:
          name: docker_teamspeak
        vars:
          ts_releases_image: "3.13.7"
          ts_container_state: 'present'
          ts_volumes_local_path: "/teamspeak"
```

License
-------

BSD

Author Information
------------------

@DenAV
https://github.com/DenAV
