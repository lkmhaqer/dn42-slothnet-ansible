# dn42-slothnet-ansible
A couple of playbooks to stand up openvpn p2p links, and run bird or quagga.

## Roles

### Common
Will update and install packages. Some extra tasks (bird-cmd.yml, vtysh-cmd.yml) for running routing commands over all nodes.

### OVPN
Installs OpenVPN, configures a tunnel per interface in the host_vars. Generates a pre-shared key if none exists, and copies to hosts as needed.

### BIRD
Installs the BIRD routing daemon, generate a basic ospf and bgp config. Create bgp peer config file per entry in host_vars.

## TODO

### Distro Support
Ubuntu 12, 14, 16 LTS are supported currently. Looking to also include support for CentOS and Alpine Linux.

### Routing Support
BIRD is supported today, hoping to include support for quagga, and JunOS.

### Tunnel Support
Supports just OpenVPN p2p. Plans include ipsec with strongswan and JunOS.
