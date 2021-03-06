# Installation

## Prerequisites

You will need a machine from which to run Ansible. In addition, your target
machine should meet the following requirements:

* Ubuntu installed (preferably minimal, for the cleanest effects; I use Ubuntu
  Server, 20.04)
* OpenSSH installed (with Ubuntu, you can select this as an option during O/S
  installation)
* A user account set up, with a password and sudo capability (I use 'ansible';
  Ubuntu automatically sets up sudo)
* Public/private keys set up for this user (TODO: document this)
* The latest version of Python installed (installed by default with Ubuntu
  Server)
* An internet connection, to download the necessary additional packages

Having installed your base operating system, it is recommended to run update
fully; e.g. under Ubuntu:

    sudo -i
    apt update
    apt -y upgrade

## Setup and run

In brief (TODO: expand):

1. Edit `config.yml` to suit your preferences (see annotations in that file)
2. In the `ansible.cfg` file, specify the path for `private_key_file`
3. Enter your target machine[s] DNS name[s] or IP address[es] into `inventory`
4. On your Ansible control machine, run `ansible-galaxy install -r
   requirements.yml` to pull down the required external roles
5. Run `ansible-playbook main.yml --ask-become-pass` (once you've run the
   playbook, the default sudo group is given passwordless sudo, so you can drop
   the "`--ask-become-pass`" after that)

The final step will take some considerable time, particularly during the
installation of packages. Unfortunately Ansible does not have good facilities
for showing progress during package installation. Patience will usually be
rewarded; the installation make take some hours.

Note: for advanced use (e.g. during further development of the playbook), you
can use `[--skip-tags "tag1"] [--tags "tag2"]` to skip or target specific
features as required.