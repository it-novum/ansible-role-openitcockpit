# Ansible Role - Install openitcockpit

## Variables

* openitcockpit_license: The license key (default: 0dc0d951-e34e-43d0-a5a5-a690738e6a49)
* openitcockpit_core: naemon or nagios (default: naemon)
* openitcockpit_instance: standalone, master or satellite (default=standalone)
* openitcockpit_module_autoreport: (default=yes)
* openitcockpit_module_evc: (default=no)
* openitcockpit_module_idoit: (default=yes)
* openitcockpit_module_map: (default=yes)
* openitcockpit_module_massenversand: (default=yes)
* openitcockpit_module_mk: (default=no)
* openitcockpit_module_sap: (default=no)
* openitcockpit_module_nrpe: (default=yes)
* openitcockpit_module_design: (default=no)
* openitcockpit_module_alfresco: (default=no)
* openitcockpit_module_linux_basic_monitoring: (default=no)
* openitcockpit_module_nwc: (default=no)
* openitcockpit_module_postgres: (default=no)
* openitcockpit_module_wmi: (default=no)
* openitcockpit_module_grafana: (default=no)
* openitcockpit_module_pagerduty: (default=no)
* openitcockpit_satellite_frontend: Install satellite frontend (default=no)
* openitcockpit_repo: overwrite repo settings (default=oitc default)
* openitcockpit_ssh_key: Set ssh key for satellite connection of phpnsta
* openitcockpit_ssh_pubkey: Set ssh pubkey for satellite connection of phpnsta

The following variables are only used on the first run:

* openitcockpit_user_firstname: (default=itn)
* openitcockpit_user_surname: (default=itn)
* openitcockpit_user_email: (default=admin@it-novum.com)
* openitockcpit_user_password: (required)
* openitcockpit_senderaddress: (default=admin@it-novum.com)
* openitcockpit_smtp_host: (default=127.0.0.1)
* openitcockpit_smtp_port: (default=25)
* openitcockpit_smtp_user: (default="")
* openitcockpit_smtp_password: (default="")

You should set openitockcpit_user_password on the first run like this:

```bash
ansible-playbook -i myinventory site.yml -e openitockcpit_user_password=mysecret
```

## SSH keys for satellites

You should create the ssh keys for satellite connections in the playbook directory:
```bash
ssh-keygen -t rsa -b 4096 -f oitc_id_rsa -N "" -C "oitc-master" -q
```
Then set the variables
```yaml
openitcockpit_ssh_key: oitc_id_rsa
openitcockpit_ssh_pubkey: oitc_id_rsa.pub
```
If you have multiple environments you should specify them in your group_vars. You could also specify them in the Playbook.
