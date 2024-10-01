
# Installing Ansible on an Ubuntu Server

This guide explains how to install Ansible on an Ubuntu server with detailed steps.

## Prerequisites
- An Ubuntu server with `sudo` access.
- Internet connection to download the necessary packages.

## Installation Steps

### 1. Update the package list and install dependencies

Open a terminal and execute the following commands:

```bash
sudo apt update
sudo apt install -y software-properties-common
```

### 2. Add the official Ansible repository

Add the official Ansible PPA (Personal Package Archive) to get the latest version of Ansible:

```bash
sudo add-apt-repository --yes --update ppa:ansible/ansible
```

### 3. Install Ansible

Install Ansible by running the following command:

```bash
sudo apt install -y ansible
```

### 4. Verify the installation

To verify that Ansible is installed correctly, use the command:

```bash
ansible --version
```

You should see the information about the installed version of Ansible.

### 5. Create a local inventory file (optional)

If you want to test Ansible on the local server, create a simple inventory file:

```bash
sudo vi /etc/ansible/hosts
```

Add the following content to configure a basic inventory:

```
[local]
localhost ansible_connection=local
```

Save the file, and Ansible is now ready to be used for local testing.

## Additional Resources

- [Official Ansible Documentation](https://docs.ansible.com/)
- [Quick Start Guide with Ansible](https://docs.ansible.com/ansible/latest/user_guide/intro_getting_started.html)
