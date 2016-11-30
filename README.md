# Ansible: hosts

Update hosts file with a list of hosts

Available on Ansible Galaxy: [pgkehle.hosts](https://galaxy.ansible.com/pgkehle/hosts)

This project rolls through all of the host variables, looking for those with ip_address set.
When it is set, this assumes that the ip address is hard coded, thus not available in a DHCP server.
Thus, add the fqdn and ip address to the hosts file.

## Variables
```yaml
is_local_host: true   # set when using a local machine, not a remote server
```

## Examples

```YAML
 # is_local_host can be saved in the host file defintions, or as extra vars
 - hosts: all
   gather_facts: "{{is_local_host is defined and is_local_host == true}}"
   roles:
     - pgkehle.hosts
```

## License

MIT

## Author Information

Paul Kehle  
@pgkehle ([twitter](https://twitter.com/pgkehle), [github](https://github.com/pgkehle), [linkedin](https://www.linkedin.com/in/pgkehle))
