# wsl2-setup-ansible
Contains the WSL Setup Scripts for Azure.

This will install all the required dependencies for development with azure.

## Install
```
# Switch to python3 by default and install venv
sudo apt install -y python-is-python3
sudo apt install -y python3.8-venv

# Activate venv and install ansible
python -m venv ~/venv/ansible
source ~/venv/ansible/bin/activate
pip install ansible

# Run Playbook in virtualenv
ansible-playbook setup-playbook.yml --ask-become
```