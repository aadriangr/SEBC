```
[logging]
 default = FILE:/var/log/krb5libs.log
 kdc = FILE:/var/log/krb5kdc.log
 admin_server = FILE:/var/log/kadmind.log

[libdefaults]
 dns_lookup_realm = false
 dns_lookup_kdf = false
 ticket_lifetime = 24h
 renew_lifetime = 7d
 forwardable = true
 default_realm = JCONCA.COM
 udp_preference_limit = 1
 default_tgs_enctypes = arcfour-hmac
 default_tkt_enctypes = arcfour-hmac

[realms]
 JCONCA.COM = {
  kdc = ip-10-0-0-166.eu-west-1.compute.internal
  admin_server = ip-10-0-0-166.eu-west-1.compute.internal
 }

[domain_realm]
 .example.com = JCONCA.COM
 example.com = JCONCA.COM
```