# Ansible Role - hosts

Update hosts file with a list of hosts

Available on Ansible Galaxy: [pgkehle.hosts](https://galaxy.ansible.com/pgkehle/hosts)

This project rolls through all of the host variables, looking for those with ip_address set.
When it is set, this assumes that the ip address is hard coded, thus not available in a DHCP server.
Thus, add the fqdn and ip address to the hosts file.

## Variables
```yaml
ansible_host: localhost or machine short hostname
```

## Examples

```yaml
 - hosts: all
   gather_facts: "{{ansible_host != 'localhost'}}"
   roles:
     - pgkehle.hosts
```

## License

MIT

## Author Information

Paul Kehle  
@pgkehle ([twitter](https://twitter.com/pgkehle), [github](https://github.com/pgkehle), [linkedin](https://www.linkedin.com/in/pgkehle))


