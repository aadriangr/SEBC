Stop Hive
```
curl -X POST -u jconca:cloudera 'http://localhost:7180/api/v12/clusters/jconca/services/hive/commands/stop'
{
  "id" : 442,
  "name" : "Stop",
  "startTime" : "2018-03-14T09:59:02.064Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}
```

Command Status
```
curl -u jconca:cloudera 'http://localhost:7180/api/v12/commands/442'
{
  "id" : 442,
  "name" : "Stop",
  "startTime" : "2018-03-14T09:59:02.064Z",
  "endTime" : "2018-03-14T09:59:03.850Z",
  "active" : false,
  "success" : true,
  "resultMessage" : "Successfully stopped service.",
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  },
  "children" : {
    "items" : [ {
      "id" : 443,
      "name" : "Stop",
      "startTime" : "2018-03-14T09:59:02.067Z",
      "endTime" : "2018-03-14T09:59:03.784Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully stopped process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVEMETASTORE-ce6319b3d52b08964b16feb81895d89b"
      }
    }, {
      "id" : 444,
      "name" : "Stop",
      "startTime" : "2018-03-14T09:59:02.070Z",
      "endTime" : "2018-03-14T09:59:03.843Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully stopped process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVESERVER2-419b726ab1b9f506108f37b1bdb7e5f7"
      }
    } ]
  },
  "canRetry" : false
}
```


Hive Status
```
curl -u jconca:cloudera 'http://localhost:7180/api/v12/clusters/jconca/services/hive'
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-10-0-0-148.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://ip-10-0-0-148.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hive/instances",
  "serviceState" : "STOPPED",
  "healthSummary" : "DISABLED",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "DISABLED",
    "suppressed" : false
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "DISABLED",
    "suppressed" : false
  } ],
  "configStalenessStatus" : "FRESH",
  "clientConfigStalenessStatus" : "FRESH",
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive",
  "entityStatus" : "STOPPED"
}
```


Start Hive
```
curl -X POST -u jconca:cloudera 'http://localhost:7180/api/v12/clusters/jconca/services/hive/commands/start'
{
  "id" : 446,
  "name" : "Start",
  "startTime" : "2018-03-14T10:01:22.382Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}
```

Command Status
```
curl -u jconca:cloudera 'http://localhost:7180/api/v12/commands/446'
{
  "id" : 446,
  "name" : "Start",
  "startTime" : "2018-03-14T10:01:22.382Z",
  "endTime" : "2018-03-14T10:01:44.678Z",
  "active" : false,
  "success" : true,
  "resultMessage" : "Successfully started service.",
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  },
  "children" : {
    "items" : [ {
      "id" : 448,
      "name" : "Start",
      "startTime" : "2018-03-14T10:01:22.445Z",
      "endTime" : "2018-03-14T10:01:44.631Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully started process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVESERVER2-419b726ab1b9f506108f37b1bdb7e5f7"
      }
    }, {
      "id" : 447,
      "name" : "Start",
      "startTime" : "2018-03-14T10:01:22.397Z",
      "endTime" : "2018-03-14T10:01:44.670Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully started process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVEMETASTORE-ce6319b3d52b08964b16feb81895d89b"
      }
    } ]
  },
  "canRetry" : false
}
```


Hive Status
```
curl -u jconca:cloudera 'http://localhost:7180/api/v12/clusters/jconca/services/hive'
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-10-0-0-148.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://ip-10-0-0-148.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hive/instances",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  } ],
  "configStalenessStatus" : "FRESH",
  "clientConfigStalenessStatus" : "FRESH",
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive",
  "entityStatus" : "GOOD_HEALTH"
}
```
