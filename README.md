# Hybrid profiles for Gentoo

These essentially mix the Hardened/SELinux and Systemd profiles. Each profile uses `parent` to define itself in terms of other Gentoo profiles.

- `hardened-plus-17`: 
  - `default/linux/amd64/17.0/systemd`
  - `default/linux/amd64/17.0/hardened/selinux`
- `hardened-plus`:
  - `default/linux/amd64/17.1/systemd` 
  - `default/linux/amd64/17.1/hardened/selinux`
- `hardened-plus/plasma`: 
  - `hardened-plus`
  - `default/linux/amd64/17.1/desktop/plasma/systemd`
