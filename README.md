# Ansible Role - Install openitcockpit

#### Variables

* openitcockpit_license: The license key (default: 0dc0d951-e34e-43d0-a5a5-a690738e6a49)
* openitcockpit_core: naemon or nagios (default: naemon)
* openitcockpit_instance: standalone, master or satellite (default=standalone)

#### Additional notes

You still have to run /usr/share/openitcockpit/app/SETUP.sh after the first run.
