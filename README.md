# Ansible-Role: Kyoushi Gather

This role can be used to gather log files, configuration files and facts about hosts used
for generating data for intrusion detection system datasets.

## Requirements

- Debian or Ubuntu (18.04 or newer)

## Example Playbook

```
- hosts: localhost
  roles:
    - kyoushi-gather
  vars:
    kyoushi_gather_logs:
      - /var/log

    kyoushi_gather_configs:
      - /etc
```

## Example Playbook with excludes
```
- hosts: localhost
  roles:
    - kyoushi-gather
  vars:
    kyoushi_gather_logs:
      - src: /var/log
        exclude:
          - *.pcap*
    kyoushi_gather_configs:
      - src: /etc
        exclude:
          - *.bk
```


## License

GPL-3.0
