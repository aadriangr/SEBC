```
[hdfs@ip-10-0-0-33 centos]$ hdfs dfs -ls /user
Found 7 items
drwxr-xr-x   - hdfs   supergroup          0 2018-03-16 10:25 /user/anupam
drwxr-xr-x   - hdfs   supergroup          0 2018-03-16 10:25 /user/hilary
drwxrwxrwx   - mapred hadoop              0 2018-03-16 10:17 /user/history
drwxrwxr-t   - hive   hive                0 2018-03-16 10:18 /user/hive
drwxrwxr-x   - hue    hue                 0 2018-03-16 10:18 /user/hue
drwxrwxr-x   - impala impala              0 2018-03-16 10:18 /user/impala
drwxrwxr-x   - oozie  oozie               0 2018-03-16 10:18 /user/oozie
```


http://ip-10-0-0-33.eu-west-1.compute.internal:7180/api/v14/hosts
```
{
  "items" : [ {
    "hostId" : "60b37179-9bb2-424e-bb49-111fcc0d88dd",
    "ipAddress" : "10.0.0.212",
    "hostname" : "ip-10-0-0-212.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-0-0-33.eu-west-1.compute.internal:7180/cmf/hostRedirect/60b37179-9bb2-424e-bb49-111fcc0d88dd",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 16656699392
  }, {
    "hostId" : "5e263397-9c2a-4827-94d4-e5eae774f1fd",
    "ipAddress" : "10.0.0.33",
    "hostname" : "ip-10-0-0-33.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-0-0-33.eu-west-1.compute.internal:7180/cmf/hostRedirect/5e263397-9c2a-4827-94d4-e5eae774f1fd",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 16656961536
  }, {
    "hostId" : "89d3a0a1-dd45-4c66-aca5-28812afce6e9",
    "ipAddress" : "10.0.0.51",
    "hostname" : "ip-10-0-0-51.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-0-0-33.eu-west-1.compute.internal:7180/cmf/hostRedirect/89d3a0a1-dd45-4c66-aca5-28812afce6e9",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 16656961536
  }, {
    "hostId" : "d97f16ce-a21d-4e67-bee0-30be76bf8d6e",
    "ipAddress" : "10.0.0.7",
    "hostname" : "ip-10-0-0-7.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-0-0-33.eu-west-1.compute.internal:7180/cmf/hostRedirect/d97f16ce-a21d-4e67-bee0-30be76bf8d6e",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 16656961536
  }, {
    "hostId" : "4e647d38-d5f2-4881-9c65-36d81c041e1e",
    "ipAddress" : "10.0.0.77",
    "hostname" : "ip-10-0-0-77.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-0-0-33.eu-west-1.compute.internal:7180/cmf/hostRedirect/4e647d38-d5f2-4881-9c65-36d81c041e1e",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 16656699392
  } ]
}
```

http://ip-10-0-0-33.eu-west-1.compute.internal:7180/api/v8/clusters
```
{
  "items" : [ {
    "name" : "cluster",
    "displayName" : "jconca",
    "version" : "CDH5",
    "fullVersion" : "5.13.2",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ]
  } ]
}
```

http://ip-10-0-0-33.eu-west-1.compute.internal:7180/api/v8/clusters/jconca/services
```
{
  "items" : [ {
    "name" : "hive",
    "type" : "HIVE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-10-0-0-33.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hive",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HIVE_HIVEMETASTORES_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "HIVE_HIVESERVER2S_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hive"
  }, {
    "name" : "zookeeper",
    "type" : "ZOOKEEPER",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-10-0-0-33.eu-west-1.compute.internal:7180/cmf/serviceRedirect/zookeeper",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "ZOOKEEPER_CANARY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "ZOOKEEPER_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "ZooKeeper"
  }, {
    "name" : "hue",
    "type" : "HUE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-10-0-0-33.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hue",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HUE_HUE_SERVERS_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "HUE_LOAD_BALANCER_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hue"
  }, {
    "name" : "oozie",
    "type" : "OOZIE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-10-0-0-33.eu-west-1.compute.internal:7180/cmf/serviceRedirect/oozie",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "OOZIE_OOZIE_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Oozie"
  }, {
    "name" : "impala",
    "type" : "IMPALA",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-10-0-0-33.eu-west-1.compute.internal:7180/cmf/serviceRedirect/impala",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "IMPALA_ASSIGNMENT_LOCALITY",
      "summary" : "DISABLED"
    }, {
      "name" : "IMPALA_CATALOGSERVER_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "IMPALA_IMPALADS_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "IMPALA_STATESTORE_HEALTH",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Impala"
  }, {
    "name" : "yarn",
    "type" : "YARN",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-10-0-0-33.eu-west-1.compute.internal:7180/cmf/serviceRedirect/yarn",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "YARN_JOBHISTORY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_NODE_MANAGERS_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_RESOURCEMANAGERS_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_USAGE_AGGREGATION_HEALTH",
      "summary" : "DISABLED"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "YARN (MR2 Included)"
  }, {
    "name" : "hdfs",
    "type" : "HDFS",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-10-0-0-33.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hdfs",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HDFS_BLOCKS_WITH_CORRUPT_REPLICAS",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_CANARY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_DATA_NODES_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_FREE_SPACE_REMAINING",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_HA_NAMENODE_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_MISSING_BLOCKS",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_UNDER_REPLICATED_BLOCKS",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "HDFS"
  } ]
}
```
