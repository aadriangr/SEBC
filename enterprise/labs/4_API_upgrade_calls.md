The last version of the CM API is 19 (http://cloudera.github.io/cm_api/docs/releases/)

Version of the CM
```
curl -u jconca:cloudera 'http://localhost:7180/api/v19/cm/version'
{
  "version" : "5.14.1",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20180207-1728",
  "gitHash" : "f253d8e2b9cf5cb61a2f1ba1bf71de6fb603add0",
  "snapshot" : false
}
```

List Users
```
 curl -u jconca:cloudera 'http://localhost:7180/api/v19/users'
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ]
  }, {
    "name" : "jconca",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  } ]
}
```

CM Database type
```
curl -u jconca:cloudera 'http://localhost:7180/api/v19/cm/scmDbInfo'
{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}
```
