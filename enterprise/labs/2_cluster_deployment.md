```
{
  "timestamp" : "2018-03-14T09:26:12.242Z",
  "clusters" : [ {
    "name" : "jconca",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "977272832"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "2976907264"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "4115975372"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "692"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-10-0-0-148.eu-west-1.compute.internal"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-419b726ab1b9f506108f37b1bdb7e5f7",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0eae8383616d60f85"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-683b9b2d2eca908c1919c747fbd1018b",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0da5a5c0e686707f0"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-96dab90729516dc1747c675d67db8cf2",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0ec477e78a1613b2c"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-a01b0a09474085add084b7124139218d",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-05038fb8101d4ebc5"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-ce6319b3d52b08964b16feb81895d89b",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-05fc8238d16333b2a"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-ce6319b3d52b08964b16feb81895d89b",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "i-05fc8238d16333b2a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dra8qfvi3h8y8um5mvwpbcxxl"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-419b726ab1b9f506108f37b1bdb7e5f7",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "i-0eae8383616d60f85"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6n5r8z12om3ogvtyx4o72grf2"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SERVER",
          "items" : [ {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "977272832"
          } ]
        } ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-419b726ab1b9f506108f37b1bdb7e5f7",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0eae8383616d60f85"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bilsw55sjyxevy9fbapsz1n8n"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-683b9b2d2eca908c1919c747fbd1018b",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0da5a5c0e686707f0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bynde0bpal85ca7dvwniddv83"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-ce6319b3d52b08964b16feb81895d89b",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-05fc8238d16333b2a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "730kbgauvomdp9e7d1sp0a9mk"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-10-0-0-148.eu-west-1.compute.internal"
        }, {
          "name" : "database_password",
          "value" : "hue"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-419b726ab1b9f506108f37b1bdb7e5f7"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-ce6319b3d52b08964b16feb81895d89b",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "i-05fc8238d16333b2a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dzj52y3a5vha58ofvmst2pl74"
          }, {
            "name" : "secret_key",
            "value" : "tg4OGyR4Eut6cGtd8ipR3d393opVLe"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-10-0-0-148.eu-west-1.compute.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "oozie"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-419b726ab1b9f506108f37b1bdb7e5f7",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "i-0eae8383616d60f85"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ec7ur1le8fmpxyidxv9td3tdt"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "6"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "1"
          } ]
        }, {
          "roleType" : "JOBHISTORY",
          "items" : [ {
            "name" : "mr2_jobhistory_java_heapsize",
            "value" : "977272832"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "rm_cpu_shares",
            "value" : "1600"
          }, {
            "name" : "rm_io_weight",
            "value" : "800"
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/disk1/yarn/nm,/disk2/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs,/disk1/yarn/container-logs,/disk2/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "3"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "5949"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "5949"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "80"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "O2pAqfOSaLxu8wwqCE3NXZggTmNOpZ"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-ce6319b3d52b08964b16feb81895d89b",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "i-05fc8238d16333b2a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1k9brhnih4y6asq6zkdr7mc39"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-683b9b2d2eca908c1919c747fbd1018b",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0da5a5c0e686707f0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "34r9buo5541aijj4bh7qgv14u"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-96dab90729516dc1747c675d67db8cf2",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0ec477e78a1613b2c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dxpih2rtbxgy2kjs4mak0egxv"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-a01b0a09474085add084b7124139218d",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-05038fb8101d4ebc5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "exdsc0xr5xtwqskmvh9o0ufxe"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-419b726ab1b9f506108f37b1bdb7e5f7",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "i-0eae8383616d60f85"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "50"
          }, {
            "name" : "role_jceks_password",
            "value" : "1gbmpcgft4e1a2w190evwpzos"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/disk1/dfs/dn,/disk2/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "5367553638"
          }, {
            "name" : "dfs_datanode_failed_volumes_tolerated",
            "value" : "1"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          }, {
            "name" : "rm_cpu_shares",
            "value" : "400"
          }, {
            "name" : "rm_io_weight",
            "value" : "200"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/dfs/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "977272832"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "977272832"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "AffI64Y8Evl4xwvtMXMsqp8ttiDel7"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "e1DuYYGrljsPetgCdj0q8CyyBV5O3D"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "fCMfJZxGz3wWrMcLAExRbeYENBaWzh"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "20"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-419b726ab1b9f506108f37b1bdb7e5f7",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "i-0eae8383616d60f85"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-683b9b2d2eca908c1919c747fbd1018b",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0da5a5c0e686707f0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "10rm652dv2tmfk1l2l3m1w29"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-96dab90729516dc1747c675d67db8cf2",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0ec477e78a1613b2c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dw1n6qpnzvyi8vnj16vgflgc7"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-a01b0a09474085add084b7124139218d",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-05038fb8101d4ebc5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2sixa51oas0jgwc100ucln50b"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-419b726ab1b9f506108f37b1bdb7e5f7",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-0eae8383616d60f85"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "eu6bfrh6a9qdvjdlb8cs0airx"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-ce6319b3d52b08964b16feb81895d89b",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-05fc8238d16333b2a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9ytohbmqehkf11dch8w1hl7a8"
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-419b726ab1b9f506108f37b1bdb7e5f7",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "i-0eae8383616d60f85"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8vdyxtumuexnn0dfwgbcedfuu"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-419b726ab1b9f506108f37b1bdb7e5f7",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-0eae8383616d60f85"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "20wcu72vnyn8x6pyfuqfyph5j"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-683b9b2d2eca908c1919c747fbd1018b",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-0da5a5c0e686707f0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6drpm86m4hbc6yyhnsolt6net"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-ce6319b3d52b08964b16feb81895d89b",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-05fc8238d16333b2a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "b86bys412x6khf3tb9bffikfe"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-419b726ab1b9f506108f37b1bdb7e5f7",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-0eae8383616d60f85"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "hdfs-ha"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "hdfs-ha"
          }, {
            "name" : "namenode_id",
            "value" : "57"
          }, {
            "name" : "role_jceks_password",
            "value" : "5f4vjh8wwesp7jwfo6m68dcul"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-ce6319b3d52b08964b16feb81895d89b",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-05fc8238d16333b2a"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "hdfs-ha"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "hdfs-ha"
          }, {
            "name" : "namenode_id",
            "value" : "52"
          }, {
            "name" : "role_jceks_password",
            "value" : "58e2foyz70sa44sal49lsb0e"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "i-05fc8238d16333b2a",
    "ipAddress" : "10.0.0.148",
    "hostname" : "ip-10-0-0-148.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0da5a5c0e686707f0",
    "ipAddress" : "10.0.0.159",
    "hostname" : "ip-10-0-0-159.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0eae8383616d60f85",
    "ipAddress" : "10.0.0.166",
    "hostname" : "ip-10-0-0-166.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0ec477e78a1613b2c",
    "ipAddress" : "10.0.0.187",
    "hostname" : "ip-10-0-0-187.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-05038fb8101d4ebc5",
    "ipAddress" : "10.0.0.189",
    "hostname" : "ip-10-0-0-189.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-ce6319b3d52b08964b16feb81895d89b",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "5f38a78e630052c177c5cc20d6beb1cf566967a876b238e664f3c1a58496af84",
    "pwSalt" : -1675883543970371758,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-ce6319b3d52b08964b16feb81895d89b",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "25f6131d7aea4c582f9be9da3846d085169f1e9ff4932d6cc12e249baf8cb74f",
    "pwSalt" : 6426592498478038552,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-ce6319b3d52b08964b16feb81895d89b",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "daea9d58970dfc8e6175ba61a9be4a3daf64a222e08706747d47dac38829aed3",
    "pwSalt" : 714387884297127795,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-ce6319b3d52b08964b16feb81895d89b",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "6a84c1fc7e164e8d9a943ed5cbb47f84e6e6757e968702e1297f27ddc75dcb6e",
    "pwSalt" : -8482308051333967914,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "febef3e41beec11d0bb8f5a40af76c675f66d04e0209e4ee66ead04632d21ce7",
    "pwSalt" : -6626763880685141440,
    "pwLogin" : true
  }, {
    "name" : "jconca",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "15a15067cc830220ee5763bc02cb8e63aa4113c189b8527b8276dcf616690674",
    "pwSalt" : -6787098404420483527,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "7b983f3f72643059323c4839660853003db8cb62786b0a9351212f54372ba951",
    "pwSalt" : -8362941611121295251,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.9.3",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170627-1506",
    "gitHash" : "23506bb4e114dd460bdac64c57a672e6be631907",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "EVENTSERVER",
        "items" : [ {
          "name" : "event_server_heapsize",
          "value" : "977272832"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "977272832"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1269825536"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-10-0-0-148.eu-west-1.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        }, {
          "name" : "headlamp_heapsize",
          "value" : "977272832"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "977272832"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1269825536"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-ce6319b3d52b08964b16feb81895d89b",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "i-05fc8238d16333b2a"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "ap1pqtq0e03wblmn5kjr8pv49"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-ce6319b3d52b08964b16feb81895d89b",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "i-05fc8238d16333b2a"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "2pjmqao9zlmw65wofcpkxjhn3"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-ce6319b3d52b08964b16feb81895d89b",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "i-05fc8238d16333b2a"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "5517yubdt28zmah1wmnnse5jx"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-ce6319b3d52b08964b16feb81895d89b",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "i-05fc8238d16333b2a"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "5jo753w2muzjc8p2cm8u0f16f"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-ce6319b3d52b08964b16feb81895d89b",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "i-05fc8238d16333b2a"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "80ydqvbxnooje1hyqnixcs6n8"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/24/2012 19:40"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  }
}
```