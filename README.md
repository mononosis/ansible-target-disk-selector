# Disk Setup Role

This role performs disk setup operations, determining the largest disk device and optionally confirming the target device interactively.

## Variables

The following variables are used by the role:

### Defaults (can be overridden):

- `skip_confirmation`: Whether to skip the confirmation of the target device. Default is `false`.
- `disk_filter_patterns`: List of regex patterns to filter out devices. Defaults to filtering out loop, ram, and dm devices.

## Usage

Include the role in your playbook and override the defaults as needed:

```yaml
- hosts: all
  roles:
    - role: disk_setup
      vars:
        skip_confirmation: true

