# ageres210784/vminsert

An Ansible role which installs and configures [vminsert] on Linux

## Requirements

Ansible 2.8+

## Role Variables

You can see all vars in `defaults/main.yml` vars file.

If you use docker swarm, you should specify variables for the host on which
the container is supposed to be run, and also indicate the name of the swarm
manager through which the stack will be deployed in variable
`vm_swarm_manager`
```yaml
vm_swarm_manager: swarm-manager01
```

## Dependencies

None

## Example Playbook

```yaml
- name: Ensure prometheus_alertmanager DB
  hosts: vminserts
  remote_user: root

  roles:
    - ageres210784.vminsert
```

## License

Apache 2.0

## Author Information

This role was created by [Sergey Evseev].
