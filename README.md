Role Name
=========
ansible-cis-redhat

Description
---------------
Ansible role to apply the [CIS 2.0](https://www.cisecurity.org/benchmark/red_hat_linux/) security rule fixes to a Red Hat Linux 7 system.

This role was developed and tested on a Mint 20.2 system using [Molecule 3](https://molecule.readthedocs.io/en/latest/). Some ideas for testing these rules with container are provided here but you'll need to modify these for your own environment. (Using containers on a Red Hat host with an active subscription is strongly recommended.) A Molecule setup, simple Dockerfile for the Docker driver and Red Hat 7 and 8 containers from [Red Hat's Container Registry](https://catalog.redhat.com/software/containers/explore) are included as well.

Molecule 3 changed the default verifier to Ansible (from testinfra). A basic test setup for Molecule 3 is included as well.

Full instructions for setting up this environment are available at [GeoffStratton.com](https://www.geoffstratton.com/test-ansible-roles-molecule-3-and-red-hat-docker-images-linux-mint).

To use official RHEL images you'll need to generate a Red Hat Container Registry [service account](https://access.redhat.com/terms-based-registry/). (Yes, you can do this with the free Red Hat Developer subscription.) You'll then need to provide your username and password token to the molecule.yml file; I just used shell variables but you could also use a CI/CD tool like Travis or other methods.

Requirements
--------------
* ansible
* molecule
* python

License
-------
GNU General Public License v3.0

Author Information
------------------
Geoff Stratton
