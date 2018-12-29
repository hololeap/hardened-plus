# Hybrid profiles for Gentoo

These essentially mix the Hardened/SELinux and Systemd profiles. The idea is to try to get as many benefits from Hardened Gentoo as possible on a "modern" desktop system. **The result is a somewhat softened system.** _These profiles are for experimental use only._

Each profile uses `parent` to define itself in terms of other Gentoo profiles:

- `hardened-plus-17`
  - `default/linux/amd64/17.0/systemd`
  - `default/linux/amd64/17.0/hardened/selinux`
- `hardened-plus`
  - `default/linux/amd64/17.1/systemd` 
  - `default/linux/amd64/17.1/hardened/selinux`
- `hardened-plus/plasma`
  - `hardened-plus`
  - `default/linux/amd64/17.1/desktop/plasma/systemd`

## Other Changes

Some restrictions added by the Hardened profiles have been removed:

- Systemd packages are [unmasked](https://github.com/hololeap/hardened-plus/blob/master/profiles/hardened-plus/package.mask).
- Gecko Media Plugins for Firefox are [unmasked](https://github.com/hololeap/hardened-plus/blob/master/profiles/hardened-plus/package.use.mask).
- NVidia graphics cards and the `systemd` USE flag are [unmasked](https://github.com/hololeap/hardened-plus/blob/master/profiles/hardened-plus/use.mask).

In addition, some restrictions have been added:

- The `pax_kernel` USE flag has been [masked](https://github.com/hololeap/hardened-plus/blob/master/profiles/hardened-plus/use.mask). Some packages still use this apparently.
