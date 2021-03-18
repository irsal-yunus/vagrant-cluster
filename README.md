# Vagrant Quickstart

This folder contains Vagrant code to stand up a single Rancher server instance with a single node cluster attached to it.

## Requirements

- [Vagrant](https://www.vagrantup.com)
- [VirtualBox](https://www.virtualbox.org)
- [Hyper-V] platform windows & Hyper-V managements tools

# enable Hyper-V powershell
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V -All

# enable Hyper-V CMD & DISM
DISM /Online /Enable-Feature /All /FeatureName:Microsoft-Hyper-V
- 6GB unused RAM

## Deploy

0. Clone this repository and go into the vagrant subfolder
# checking syntax vagrant
0. Run vagrant validate 
0. Run `vagrant up`

When provisioning is finished the Rancher UI will become accessible on [193.1.1.4](http://193.1.1.4).
The default password is `admin`, but this can be updated in the config.yaml file.

If you want to keep the configuration changes outside the git repository you can copy the config.yaml file to local_config.yaml and make changes there.

## Remove

To remove the VMs that have been deployed run `vagrant destroy -f`
