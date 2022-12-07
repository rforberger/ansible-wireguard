# A wireguard ansible role with optional full automatic configuration of peers

Example data:

```
wireguard:
  peers:
    - { client_name: "192.168.1.2", interface_name: "wgclient1", client_ip: "192.168.108.2", allowed_ips: "192.168.108.0/24", auto_config: True }
    - { client_name: "tablet01", client_ip: "192.168.108.3", allowed_ips: "192.168.108.1/32", auto_config: False }
    - { client_name: "laptop02", client_ip: "192.168.108.4", allowed_ips: "192.168.108.1/32", auto_config: False }
    - { client_name: "laptop04", client_ip: "192.168.108.5", allowed_ips: "192.168.108.1/32", auto_config: False }
    - { client_name: "other.host", interface_name: "wgclient0", client_ip: "192.168.108.6", allowed_ips: "192.168.108.0/24", auto_config: True }
  ips:
    internal: "192.168.108.1"
    subnet_prefix: "24"
  interface_name: "wg0"
  server_port: 60004
```