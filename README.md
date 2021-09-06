# wsl2-setup-ansible
Contains the WSL Setup Scripts for Azure

## Install
```
sudo apt update
sudo apt install -y ansible

# Switch to python3 by default
sudo apt install -y python-is-python3

# Install virtual env for python packages
apt install -y python3.8-venv
python -m venv ~/venv/ansible
source ~/venv/ansible/bin/activate

# Run Playbook in virtualenv
ansible-playbook setup-playbook.yml --ask-become

# Install Ansible Azure Requirements (see github dir)
curl -O https://raw.githubusercontent.com/ansible-collections/azure/dev/requirements-azure.txt && \
python -m pip install --upgrade --no-cache-dir -r requirements-azure.txt && \
rm requirements-azure.txt

```