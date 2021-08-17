# [Ansible] Upgrade Debian 10 to Debian 11 Bullseye

1. Backup your system
2. Edit inventory file
3. Run step 1 which is for apply all security patches and pending upgrades to Debian 10 itself.

```console
ansible-playbook main.yml --tag step1
```

4. If you run locally reboot. If your run remotly it will be rebooted.
5. Run step 2 which:
a. reconfigure APT’s source-list files
b. update package list
c. upgrade Debian 10 to Debian 11
d. reboot if run remotly

```console
ansible-playbook main.yml --tag step2
```
