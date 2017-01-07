# TangoAnsible

After a couple years of managing Cowrie honeypots, I set out to make management and setup of them much easier. Thus here is my Ansible playbook for setting up a new honeypot using Cowrie for integration with Tango Honeypot Intelligence. 

For software and users which the playbook removes - I have discoverered a lot of VPS providers put extra and unneeded software/users on the VPS images they provide. Thus this playbook will remove those to harden the honeypot.

For all of the configuration files copies to the destination honeypot, I keep all of these on my Anisble server so I can keep a master copy of the configs and push out to all the honeypots. This makes it easier to progate a change to all of them and standarize deployment.

This script has been tested on Ubuntu 14.04 and 16.04 across various VPS providers. May add support for CentOS soon.

Prior to running, you MUST take these steps:
  1. Download a copy of Splunk Forwarder for Linux (.tgz version) and place it in the /conf folder. Ensure the file name matches the            Splunk install filename listed in the Ansible script or update it.
     https://www.splunk.com/en_us/download/universal-forwarder.html#
  2. Update the iptables rules file (/conf/rules.v4) with what ssh port you moved it to and your source mgmt IP
  3. Update the Splunk outputs file (/conf/tango/tango_input/default/outputs.conf) with your Splunk server IP.
