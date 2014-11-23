# Ansible Raspberry Pi

Ansible Playbooks for configuring my Raspberry Pi.

## Setup

1. Make sure the hosts file is pointing at the correct IP address.
2. Configure group\_vars for the __raspberries__ group.

    ```yaml
    timezone: 'America/New_York'
    wpa_ssid: 'Your SSID'
    wpa_psk: 'Your Password'
    ```

## Usage

Apply the playbooks and their configuration to your raspberry pi.

```bash
$ ansible-playbook -s pi.yml -i hosts
```

Apply to a specific host:

```bash
$ ansible-playbook -s pi.yml -i hosts -l wired-pi
```
