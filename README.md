# ansible-role-sysbox

An Ansible role that installs [Sysbox](https://github.com/nestybox/sysbox)
on Ubuntu.

## Variables

The role uses the following variables:

- `sysbox_version` (string) The Sysbox version (e.g. 0.5.2).
- `sysbox_deb_sha256` (string) The Sysbox deb package SHA256 checksum.
All available Sysbox versions and their SHA256 checksums of deb packages can be found in
[GitHub](https://github.com/nestybox/sysbox/releases).
- `sysbox_deb_destination` (string) The destination of the downloaded Sysbox deb package.
- `sysbox_docker_remove_containers` (boolean) Controls whether existing Docker containers shall be removed.
If Docker is not running, this variable is ignored.

The default values of the variables are defined in [defaults/main.yml](./defaults/main.yml)

## Important notes

- This role installs Sysbox regardless if Docker is installed.
- This role does not verify if Sysbox requirements are satisfied.
  Please advise [Sysbox Installation](https://github.com/nestybox/sysbox#installation) before using.
- Sysbox installation may affect other existing software.

## Supported platforms

- Ubuntu 22.04
- Ubuntu 20.04
- Ubuntu 18.04

## Dependencies

None

## Test Dependencies

- [Molecule Vagrant Driver](https://github.com/ansible-community/molecule-vagrant)
- [Ansible role for Docker](https://galaxy.ansible.com/geerlingguy/docker)
