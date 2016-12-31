# TangoAnsible

After a couple years of managing Cowrie honeypots, I set out to make management and setup of them much easier. Thus here is my Ansible playbook for setting up a new honeypot using Cowrie for integration with Tango Honeypot Intelligence. 

For software and users which the playbook removes - I have discoverered a lot of VPS providers put extra and unneeded software/users on the VPS images they provide. Thus this playbook will remove those to harden the honeypot.

For all of the configuration files copies to the destination honeypot, I keep all of these on my Anisble server so I can keep a master copy of the configs and push out to all the honeypots. This makes it easier to progate a change to all of them and standarize deployment.
