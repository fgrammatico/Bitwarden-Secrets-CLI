Bitwarden Secret CLI Role
==========================

This Ansible role installs the Bitwarden Secret CLI on a Linux system.

Requirements
------------

- Ansible 2.9 or higher
- `unzip` package should be installed on the target system

Role Variables
--------------

The following variables are available for this role and can be customized as needed:

- `bitwarden_cli_url`: URL to download the Bitwarden CLI zip file. Default is `https://github.com/bitwarden/sdk/releases/download/bws-v1.0.0/bws-x86_64-unknown-linux-gnu-1.0.0.zip`.
- `bitwarden_cli_dest`: Destination path for the downloaded zip file. Default is `/tmp/bws-x86_64-unknown-linux-gnu-1.0.0.zip`.
- `bitwarden_cli_bin`: Path where the Bitwarden CLI binary will be moved. Default is `/usr/local/bin/bws`.

Dependencies
------------

None.

Example Playbook
----------------

Here is an example of how to use this role in a playbook:

```yaml
- hosts: localhost
  roles:
    - role: bitwarden_cli
      vars:
        bitwarden_cli_url: "https://github.com/bitwarden/sdk/releases/download/bws-v1.0.0/bws-x86_64-unknown-linux-gnu-1.0.0.zip"
        bitwarden_cli_dest: "/tmp/bws-x86_64-unknown-linux-gnu-1.0.0.zip"
        bitwarden_cli_bin: "/usr/local/bin/bws"
