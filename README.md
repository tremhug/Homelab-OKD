# Homelab-OKD
This repo is a set of scripts needed to deploy an OKD cluster on homelab. The cluster will be composed of 3 Virtualbox VMs.

I run this cluster on a refurbished HP Proliant ML350p Gen8 on which I have installed Ubuntu server 24.04.1 LTS.
This server has the following description:
HP Proliant ML 350p Gen8
1. CPU         -    2x E5-2670 @ 2.6 GHz (16 Cores) 
2. RAM         -    128GB DDR3 ECC RAM (16x 8GB) 
3. Hard Drives -    2x 900GB 10K SAS Drives 

This does not mean that the script won't run on anything else, but it has been deployed on that environment. 

## Objective
The goal of this scripts is to automate the deployment of 3 VM such that one will be the Control plane while the other two will be used as workers.

I'm sure this has been done many times. I just want to play with it and share my experience through this journey. And if it helps someone, then it is great! 

##Prerequesite
Before being able to build the cluster, we need to validate some items are present on the host.
1. The host OS is Ubuntuserver 24.04.1 LTS
2. VirtualBox: 7.0.16
3. Ansible: 9.10.0
4. Ansible-core: 2.16.11
5. Vagrant: 2.4.1-1

Once again, I write the version number here because this is what I have tested but it will likely work with other permutation of versions.

##
