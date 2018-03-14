kinit
```
sudo kinit -kt /etc/cloudera-scm-server/cmf.keytab cloudera-scm@JCONCA.COM
```

klist
```
sudo klist -e -f
Ticket cache: FILE:/tmp/krb5cc_0
Default principal: cloudera-scm@JCONCA.COM

Valid starting       Expires              Service principal
03/14/2018 14:04:42  03/15/2018 14:04:42  krbtgt/JCONCA.COM@JCONCA.COM
        renew until 03/21/2018 14:04:42, Flags: FRI
        Etype (skey, tkt): arcfour-hmac, aes256-cts-hmac-sha1-96
```