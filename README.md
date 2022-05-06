# Ansible Role - hosts

Update hosts file with a list of hosts

Available on Ansible Galaxy: [isaackehle.hosts](https://galaxy.ansible.com/isaackehle/hosts)

This project rolls through all of the host variables, looking for those with ip_address set.
When it is set, this assumes that the ip address is hard coded, thus not available in a DHCP server.
Thus, add the fqdn and ip address to the hosts file.

## Variables

```yaml
inventory_hostname: localhost or machine short hostname
```

## Examples

```yaml
- hosts: all
  gather_facts: inventory_hostname != 'localhost'
  roles:
    - isaackehle.hosts
```

## Linting

```bash
yamllint -c yamllint.yaml .
ansible-lint .
```

## License

MIT

## Author Information

Isaac Kehle
@isaackehle ([twitter](https://twitter.com/isaackehle), [github](https://github.com/isaackehle), [linkedin](https://www.linkedin.com/in/isaackehle))
