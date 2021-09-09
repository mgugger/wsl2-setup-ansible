# wsl2-setup-ansible
Contains the WSL Setup Scripts for Azure on WSL with Ubuntu 20.04. Run the following steps within wsl.

This will install all the required dependencies for development with azure such as ansible, azcollection modules, terraform etc.

## Install
```
# Switch to python3 by default and install venv
sudo apt install -y python-is-python3
sudo apt install -y python3.8-venv

# Activate venv and install ansible
python -m venv ~/venv/ansible
source ~/venv/ansible/bin/activate
pip install ansible
deactivate

# Run Playbook in virtualenv
source ~/venv/ansible/bin/activate
ansible-playbook setup-playbook.yml --ask-become
deactivate
```
