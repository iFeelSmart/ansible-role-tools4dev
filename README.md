# Tools4Dev

An Ansible role that installs and sets up Tools4dev for Linux & MacOS.

## Requirements

None.

## Role Variables

```yaml
t4d_autoload: true
```
Defines if t4dtools has to be auto-loaded when logging to a shell

```yaml
t4d_user: "{{ ansible_remote_user }}"
t4d_group: t4d
t4d_homedir: ~/.tools4dev
```
Define tools4dev user that will be used for installation.

```yaml
t4d_version: 5.0.0
t4d_download_url: "https://github.com/iFeelSmart/Tools4Dev/archive/refs/tags/{{ t4d_version }}.tar.gz"
```
Define tools4dev version & url to retrieve and download for installation.

```yaml
t4d_bindir: "{{ t4d_homedir }}/bin"
t4d_shellrc: ~/.zshrc
```


```yaml
t4d_team_enabled: false
t4d_team_src: ""
t4d_team_dest: ~/Git/team
t4d_team_name: Defaul
```
Define tools4dev team configuration to install and enable.

## Dependencies

None.

## Example Playbook

```yaml
- hosts: servers
  roles:
     - ifeelsmart.tools4dev
```

## License

MIT

## Author Information

This Ansible role was created by iFeelSmart DevOps team in 2023
