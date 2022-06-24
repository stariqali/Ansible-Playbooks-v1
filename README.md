
# Ansible Automation for Consultants
Playbooks listed here can be leveraged to assist with a number of repetivie BIG-IP tasks.
There are no warranties for these playbooks implied or otherwise
Thoroughly test all code within a test lab before using it in the production environment


## Additional Info
This section will be udpated to reflect any new playbooks.
See example Playbooks for the following scenarios:

- Add/ Modify User
## Environment details:

Playbooks are based on the following configuration.


| Device Name                | Username | Password                   |
| :------------------------- | :------- | :------------------------- |
| `big-ip-a 10.1.1.5`        | `admin`  | `automate@dmin`            |
| `big-ip-a 10.1.1.6`        | `admin`  | `automate@dmin`            |
| `big-ip-a 10.1.1.9`        | `admin`  | `automate@dmin`            |
| `big-ip-a 10.1.1.10`        | `admin`  | `automate@dmin`            |
| `big-ip-a 10.1.1.11`        | `admin`  | `automate@dmin`            |


## How to run a Playbook

| Device.                    | Ansible Vault Password     |
| :------------------------- | :------------------------- |
| `big-ip-a 10.1.1.5`        | `encryptme`                |
| `big-ip-a 10.1.1.6`        | `encryptme`                |
| `big-ip-a 10.1.1.9`        | `encryptme`                |
| `big-ip-a 10.1.1.10`       | `encryptme`                |
| `big-ip-a 10.1.1.11`       | `encryptme`                |

- cd to the project root directory and run the command below
```bash
    ansible-playbook 1.1_mod-usershell-0.1-adduser.yml --ask-vault-password
```
- When prompted enter the ansible vault password


## Ansible Vault

Review K64450989 on how to create appropriate files for ansible vault

Run the following command to decrypt the file and modify the device group settings/ password
- cd to the project root directory and run the command below
```bash
    ansible-vault decrypt group_vars/my_dg/vault.yml
```
- When prompted enter the ansible vault password


To re-encrypt or change the vault pass
```bash
    ansible-vault encrypt group_vars/my_dg/vault.yml
```
- When prompted enter the existing ansible vault password or to change the password enter a new one.

To re-encrypt or change the vault pass
```bash
    ansible-vault encrypt group_vars/my_dg/vault.yml
```

To edit vault file
```bash
    ansible-vault edit group_vars/my_dg1/vault.yml
```
When prompted enter the existing ansible vault password or to change the password enter a new one.


## Authors

- [@stariqali](https://github.com/stariqali/Ansible-Playbooks-v1)

[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)

