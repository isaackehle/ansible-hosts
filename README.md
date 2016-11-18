# Ansible: setup-hosts

Update hosts file with a list of hosts

Available on Ansible Galaxy: [pgkehle.setup-hosts](https://galaxy.ansible.com/pgkehle/setup-hosts)

# Examples

```YAML
 # is_local_host can be saved in the host file defintions, or as extra vars
 - hosts: all
   gather_facts: "{{is_local_host is defined and is_local_host == true}}"
   roles:
     - pgkehle.setup-hosts
```

## License

MIT

## Author Information

Paul Kehle  
@pgkehle ([twitter](https://twitter.com/pgkehle), [github](https://github.com/pgkehle), [linkedin](https://www.linkedin.com/in/pgkehle))
