# Demo Ping Role

This is an Ansible role that demonstrates basic network connectivity testing by pinging the Semaphore UI website. The role is designed to work on both macOS and Linux systems.

## Description

The role performs a simple ping test to `semaphoreui.com` with the following characteristics:
- Sends a single ping packet
- Uses platform-specific timeout parameters:
  - macOS: 2-second timeout
  - Linux: 2-second timeout
- Displays the ping results

## Requirements

- Ansible 2.9 or higher
- Target system must have `ping` command available
- Target system must be either macOS or Linux

## Usage

To use this role in your playbook:

```yaml
- hosts: your_target_hosts
  roles:
    - demo-ping-role
```

## Role Variables

This role does not require any variables to be set.

## Example Output

The role will output the ping results in the following format:
```
TASK [demo-ping-role : Ping result] *******************************************
ok: [localhost] => {
    "msg": [
        "PING semaphoreui.com (x.x.x.x): 56 data bytes",
        "64 bytes from x.x.x.x: icmp_seq=0 ttl=xx time=xx.xxx ms"
    ]
}
```

## License

MIT © [Denis Gukov](https://github.com/fiftin)
