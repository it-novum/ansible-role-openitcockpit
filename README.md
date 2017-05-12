# Ansible Role - Install openitcockpit

#### Variables

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

#### Additional notes

You still have to run /usr/share/openitcockpit/app/SETUP.sh after the first run.
