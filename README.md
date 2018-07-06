# Trust issues

Having trust issues? Need to install client-provided vpn? Then this is probably for you.

I'm using version 2.4.x of ansible. Earlier versions _might_ work...

## variables.yml

In order not to leak sensitive information, most settings are extracted to a simple yaml-file called `variables.yml` which should be placed next to the `Vagrantfile`. Below is an example. 

```yaml
---
default:
  certificate_file: <the zip-archive with certificates>
  personal_certificate_name: <certificate for you vpn user>
  vpn_host: vpn.superawesome.net
  vpn_user: <username for vpn>
  vpn_group: <authgroup for vpn>
  vpn_password: <password for you vpn user>

  dns_zone: <domain to forward dns for>
  dns_forwarders:
    <list of dnsservers separated by semicolon>;
    8.8.8.8; 8.8.4.4;
    208.67.222.222; 208.67.220.220;

  timezone: Europe/Stockholm
```
