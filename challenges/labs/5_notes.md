I'm with not enough time to finish this challenge. This is what i'm doing


In all nodes
<code>sudo yum -y install krb5-workstation krb5-libs krb5-auth-dialog</code>

edit /etc/krb5.conf file
```
  [logging]
    default = FILE:/var/log/krb5libs.log
    kdc = FILE:/var/log/krb5kdc.log
    admin_server = FILE:/var/log/kadmind.log

  [libdefaults]
    default_realm = JCONCA.NL
    dns_lookup_realm = false
    dns_lookup_kdc = false
    ticket_lifetime = 24h
    renew_lifetime = 7d
    forwardable = true
    udp_preference_limit = 1
    default_tgs_enctypes = arcfour-hmac
    default_tkt_enctypes = arcfour-hmac 

  [realms] 
    JCONCA.NL = {
    kdc = ip-10-0-0-33.eu-west-1.compute.internal
    admin_server = ip-10-0-0-33.eu-west-1.compute.internal
  }
```

In second node install kdc
<code>sudo yum -y install krb5-server krb5-libs krb5-auth-dialog krb5-workstation
</code>

edit kdc.conf
``` 
  [realms]
    JCONCA.NL = {
    #master_key_type = aes256-cts
    acl_file = /var/kerberos/krb5kdc/kadm5.acl
    dict_file = /usr/share/dict/words
    admin_keytab = /var/kerberos/krb5kdc/kadm5.keytab
    supported_enctypes = aes256-cts:normal aes128-cts:normal des3-hmac-sha1:normal arcfour-hmac:normal des-hmac-sha1:normal des-cbc-md5:normal des-cbc-crc:normal
    max_life = 1d
    max_renewable_life = 7d
  }
```

