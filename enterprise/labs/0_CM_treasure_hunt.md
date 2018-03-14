<b>What is ubertask optimization?</b>
Whether to enable ubertask optimization, which runs "sufficiently small" jobs sequentially within a single JVM. "Small" is defined by the mapreduce.job.ubertask.maxmaps, mapreduce.job.ubertask.maxreduces, and mapreduce.job.ubertask.maxbytes settings.

<b>Where in CM is the Kerberos Security Realm value displayed?</b>
Administration => Settings

<b>Which CDH service(s) host a property for enabling Kerberos authentication?</b>
Zookeepere, HDFS, YARN

<b>How do you upgrade the CM agents?</b>
Is part of the Upgrade Wizard of Cloudera Manager Server
https://www.cloudera.com/documentation/enterprise/latest/topics/cm_ag_ug_cm5.html#concept_gs4_bsg_xw

<b>Give the tsquery statement used to chart Hue's CPU utilization?</b>
select cpu_system_rate + cpu_user_rate where category=ROLE and serviceName=$SERVICENAME

<b>Name all the roles that make up the Hive service</b>
Gateway, Hive Metastore Server, HiveServer2

<b>What steps must be completed before integrating Cloudera Manager with Kerberos?</b>
Set up a working KDC. Cloudera Manager supports MIT KDC and Active Directory.  
The KDC should be configured to have non-zero ticket lifetime and renewal lifetime. CDH will not work properly if tickets are not renewable.  
OpenLdap client libraries should be installed on the Cloudera Manager Server host if you want to use Active Directory. Also, Kerberos client libraries should be installed on ALL hosts.  
Cloudera Manager needs an account that has permissions to create other accounts in the KDC.  
