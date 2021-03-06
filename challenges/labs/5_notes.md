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

Initializing database
```
sudo kdb5_util create -s
```


Creating cloudera-sm as an admin
```
[centos@ip-10-0-0-33 ~]$ sudo kadmin.local
Authenticating as principal root/admin@JCONCA.NL with password.
kadmin.local:    addprinc cloudera-scm@JCONCA.NL
WARNING: no policy specified for cloudera-scm@JCONCA.NL; defaulting to no policy
Enter password for principal "cloudera-scm@JCONCA.NL":
Re-enter password for principal "cloudera-scm@JCONCA.NL":
Principal "cloudera-scm@JCONCA.NL" created.
kadmin.local:  q
```

```
sudo vi /var/kerberos/krb5kdc/kadm5.acl 
  */admin@JCONCA.COM *
  cloudera-scm@JCONCA.COM admilc
```

```
sudo vi /var/kerberos/krb5kdc/kadm5.acl 
  */admin@JCONCA.NL *
  cloudera-scm@JCONCA.NL admilc

sudo kadmin.local
  addpol admin
  addpol users
  addpol hosts
  exit

sudo systemctl enable krb5kdc
sudo systemctl start krb5kdc
sudo systemctl enable kadmin
sudo systemctl start kadmin
```

```
[centos@ip-10-0-0-33 ~]$ kinit cloudera-scm
Password for cloudera-scm@JCONCA.NL:
[centos@ip-10-0-0-33 ~]$ klist
Ticket cache: FILE:/tmp/krb5cc_1000
Default principal: cloudera-scm@JCONCA.NL

Valid starting       Expires              Service principal
03/16/2018 11:18:16  03/17/2018 11:18:16  krbtgt/JCONCA.NL@JCONCA.NL
        renew until 03/23/2018 11:18:16
[centos@ip-10-0-0-33 ~]$
```
  
  