[![CI](https://github.com/StoneSoupKitchen/ansible-role-fail2ban/actions/workflows/ci.yml/badge.svg)](https://github.com/StoneSoupKitchen/ansible-role-fail2ban/actions/workflows/ci.yml)

# Ansible role: fail2ban

An Ansible role for configuring fail2ban.

## Requirements

Supported operating systems:
* Debian 10 (Buster)
* Debian 11 (Bullseye)

## Role Variables

The following table lists all variables that can be overridden
and their default values.

| Name                     | Default Value | Description                      |
| ------------------------ | ------------- | -------------------------------- |
| `fail2ban_package` | fail2ban | Name of the fail2ban package. Use `name=ver` format to pin. |
| `fail2ban_package_state` | present | Installation state for the fail2ban package. |

## Examples

```yaml
- hosts: all
  roles:
    - stonesoupkitchen.fail2ban
```

## Development

A Makefile is included for easier development with `pipenv`.
After cloning this repository,
use the following commands to set up an environment.

    pipenv install --dev

To lint your changes with ansible-lint:

    make lint

To run tests with molecule:

    make test

## License

See [LICENSE](./LICENSE).

