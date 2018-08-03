# Ansible Role: Gitlab

Configure Gitlab Omnibus installation

## Requirements

The role assumes that there is an existing installation of gitlab

## Role Variables

All role variables are listed in default/main.yml.

## Dependencies

None.

## Example Playbook

    - hosts: gitlab
      become: yes
      vars_files:
        - vars/main.yml
      roles:
        - { role: ansible-role-gitlab }

*Inside `vars/main.yml`*:

    gitlab_enable_tls: true
    gitlab_certificate_file: /Certificate.pem
    gitlab_private_key_file: /Private_key.pem


## License

MIT / BSD
