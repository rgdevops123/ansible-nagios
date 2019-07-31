# ansible-nagios

- Install Nagios Servers and Clients with Ansible.
- OS: CentOS 7
- Nagios is wrapped in SSL via Apache.
- Sets the ```nagiosadmin``` password to ```changeme```.
- Creates a read-only user Username: ```guest``` & Password: ```guest```.

## Before Install
Use DNS Server or update /etc/hosts for all servers
Update the the variables in vars/main.yml

### Install Nagios Server and Clients.
Run the playbook.

```
ansible-playbook -i hosts nagios.yml
```

- Navigate to the server at https://<YOUR_NAGIOS_SERVER>/nagios.
- Login with ```nagiosadmin / changeme```. 

- Run the following on the Nagios Server to change the nagiosadmin password.
```
htpasswd /etc/nagios/passwd nagiosadmin
```
