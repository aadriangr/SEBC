NO privileges
```
beeline> !connect jdbc:hive2://ip-10-0-0-166.eu-west-1.compute.internal:10000/default;principal=hive/_HOST@JCONCA.COM
Connecting to jdbc:hive2://ip-10-0-0-166.eu-west-1.compute.internal:10000/default;principal=hive/_HOST@JCONCA.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.3)
Driver: Hive JDBC (version 1.1.0-cdh5.9.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-10-0-0-166.eu-west-1.compu> show tables;
INFO  : Compiling command(queryId=hive_20180314165656_e050fb22-9c0f-4fb6-8f15-ff617091b3aa): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20180314165656_e050fb22-9c0f-4fb6-8f15-ff617091b3aa); Time taken: 0.646 seconds
INFO  : Executing command(queryId=hive_20180314165656_e050fb22-9c0f-4fb6-8f15-ff617091b3aa): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20180314165656_e050fb22-9c0f-4fb6-8f15-ff617091b3aa); Time taken: 0.252 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (2.235 seconds)
```

GRANT Permissions
```
0: jdbc:hive2://ip-10-0-0-166.eu-west-1.compu> CREATE ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20180314170505_4e1f0a8b-0b90-4b28-b9df-fd00e3a6aabe): CREATE ROLE
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20180314170505_4e1f0a8b-0b90-4b28-b9df-fd00e3a6aabe); T
INFO  : Executing command(queryId=hive_20180314170505_4e1f0a8b-0b90-4b28-b9df-fd00e3a6aabe): CREATE ROLE
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20180314170505_4e1f0a8b-0b90-4b28-b9df-fd00e3a6aabe); T
INFO  : OK
No rows affected (0.209 seconds)
0: jdbc:hive2://ip-10-0-0-166.eu-west-1.compu> GRANT ALL ON SERVER server1 TO ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20180314170606_e02104b8-717e-4a2b-860c-df806d8bfe6c): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20180314170606_e02104b8-717e-4a2b-860c-df806d8bfe6c); Time taken: 0.077 seconds
INFO  : Executing command(queryId=hive_20180314170606_e02104b8-717e-4a2b-860c-df806d8bfe6c): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20180314170606_e02104b8-717e-4a2b-860c-df806d8bfe6c); Time taken: 0.082 seconds
INFO  : OK
No rows affected (0.172 seconds)
0: jdbc:hive2://ip-10-0-0-166.eu-west-1.compu> GRANT ROLE sentry_admin TO GROUP hive;
INFO  : Compiling command(queryId=hive_20180314170707_68677205-69cf-4699-89f9-3469be713dfe): GRANT ROLE sentry_admin TO GROUP hive
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20180314170707_68677205-69cf-4699-89f9-3469be713dfe); Time taken: 0.054 seconds
INFO  : Executing command(queryId=hive_20180314170707_68677205-69cf-4699-89f9-3469be713dfe): GRANT ROLE sentry_admin TO GROUP hive
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20180314170707_68677205-69cf-4699-89f9-3469be713dfe); Time taken: 0.03 seconds
INFO  : OK
No rows affected (0.099 seconds)
0: jdbc:hive2://ip-10-0-0-166.eu-west-1.compu> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20180314170707_e8b5a7b5-4359-4d23-8a74-d3c6f9732693): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20180314170707_e8b5a7b5-4359-4d23-8a74-d3c6f9732693); Time taken: 0.058 seconds
INFO  : Executing command(queryId=hive_20180314170707_e8b5a7b5-4359-4d23-8a74-d3c6f9732693): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20180314170707_e8b5a7b5-4359-4d23-8a74-d3c6f9732693); Time taken: 0.151 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.264 seconds)
0: jdbc:hive2://ip-10-0-0-166.eu-west-1.compu> Closing: 0: jdbc:hive2://ip-10-0-0-166.eu-west-1.compute.internal:10000/default;principal=hive/_HOST@JCONCA.COM
```

Create Test Users
```
[centos@ip-10-0-0-148 ~]$ sudo groupadd selector
[centos@ip-10-0-0-148 ~]$ sudo groupadd inserters
[centos@ip-10-0-0-148 ~]$ sudo useradd -u 1100 -g                                                        selector george
[centos@ip-10-0-0-148 ~]$ sudo useradd -u 1200 -g                                                        inserters ferdinand
```

GRANTS to the users
```
[centos@ip-10-0-0-148 ~]$ beeline
Beeline version 1.1.0-cdh5.9.3 by Apache Hive
beeline> !connect jdbc:hive2://ip-10-0-0-166.eu-west-1.compute.internal:10000/default;principal=hive/_HOST@JCONCA.COM
scan complete in 2ms
Connecting to jdbc:hive2://ip-10-0-0-166.eu-west-1.compute.internal:10000/default;principal=hive/_HOST@JCONCA.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.3)
Driver: Hive JDBC (version 1.1.0-cdh5.9.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-10-0-0-166.eu-west-1.compu> CREATE ROLE reads;
INFO  : Compiling command(queryId=hive_20180314170909_8cef5740-1afd-4032-b1da-55ea1b6925ac): CREATE ROLE reads
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20180314170909_8cef5740-1afd-4032-b1da-55ea1b6925ac); Time taken: 0.054 seconds
INFO  : Executing command(queryId=hive_20180314170909_8cef5740-1afd-4032-b1da-55ea1b6925ac): CREATE ROLE reads
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20180314170909_8cef5740-1afd-4032-b1da-55ea1b6925ac); Time taken: 0.025 seconds
INFO  : OK
No rows affected (0.13 seconds)
0: jdbc:hive2://ip-10-0-0-166.eu-west-1.compu> CREATE ROLE writes;
INFO  : Compiling command(queryId=hive_20180314170909_ab2ef560-aab1-432b-b80c-1e4cb150c807): CREATE ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20180314170909_ab2ef560-aab1-432b-b80c-1e4cb150c807); Time taken: 0.051 seconds
INFO  : Executing command(queryId=hive_20180314170909_ab2ef560-aab1-432b-b80c-1e4cb150c807): CREATE ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20180314170909_ab2ef560-aab1-432b-b80c-1e4cb150c807); Time taken: 0.023 seconds
INFO  : OK
No rows affected (0.089 seconds)
0: jdbc:hive2://ip-10-0-0-166.eu-west-1.compu> GRANT SELECT ON DATABASE default TO ROLE reads;
INFO  : Compiling command(queryId=hive_20180314170909_c254304c-db8f-47f8-8803-4e4d87e13cb0): GRANT SELECT ON DATABASE default TO ROLE reads
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20180314170909_c254304c-db8f-47f8-8803-4e4d87e13cb0); Time taken: 0.053 seconds
INFO  : Executing command(queryId=hive_20180314170909_c254304c-db8f-47f8-8803-4e4d87e13cb0): GRANT SELECT ON DATABASE default TO ROLE reads
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20180314170909_c254304c-db8f-47f8-8803-4e4d87e13cb0); Time taken: 0.028 seconds
INFO  : OK
No rows affected (0.095 seconds)
0: jdbc:hive2://ip-10-0-0-166.eu-west-1.compu> GRANT ROLE reads TO GROUP selector;
INFO  : Compiling command(queryId=hive_20180314170909_904fb53e-f80f-4cb6-9e63-e85a623dfb61): GRANT ROLE reads TO GROUP selector
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20180314170909_904fb53e-f80f-4cb6-9e63-e85a623dfb61); Time taken: 0.052 seconds
INFO  : Executing command(queryId=hive_20180314170909_904fb53e-f80f-4cb6-9e63-e85a623dfb61): GRANT ROLE reads TO GROUP selector
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20180314170909_904fb53e-f80f-4cb6-9e63-e85a623dfb61); Time taken: 0.029 seconds
INFO  : OK
No rows affected (0.094 seconds)
0: jdbc:hive2://ip-10-0-0-166.eu-west-1.compu> REVOKE ALL ON DATABASE default FROM ROLE writes;
INFO  : Compiling command(queryId=hive_20180314171010_e3232649-7b70-48d5-8080-1897739f7acd): REVOKE ALL ON DATABASE default FROM ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20180314171010_e3232649-7b70-48d5-8080-1897739f7acd); Time taken: 0.055 seconds
INFO  : Executing command(queryId=hive_20180314171010_e3232649-7b70-48d5-8080-1897739f7acd): REVOKE ALL ON DATABASE default FROM ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20180314171010_e3232649-7b70-48d5-8080-1897739f7acd); Time taken: 0.084 seconds
INFO  : OK
No rows affected (0.151 seconds)
0: jdbc:hive2://ip-10-0-0-166.eu-west-1.compu> GRANT INSERT ON default.sample_07 TO ROLE writes;
INFO  : Compiling command(queryId=hive_20180314171010_5008e722-0884-44bc-997e-e167c314da61): GRANT INSERT ON default.sample_07 TO ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20180314171010_5008e722-0884-44bc-997e-e167c314da61); Time taken: 0.056 seconds
INFO  : Executing command(queryId=hive_20180314171010_5008e722-0884-44bc-997e-e167c314da61): GRANT INSERT ON default.sample_07 TO ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20180314171010_5008e722-0884-44bc-997e-e167c314da61); Time taken: 0.03 seconds
INFO  : OK
No rows affected (0.099 seconds)
0: jdbc:hive2://ip-10-0-0-166.eu-west-1.compu> GRANT ROLE writes TO GROUP inserters;
INFO  : Compiling command(queryId=hive_20180314171010_f34511df-ac0a-455d-9bd5-32eaa95da4e9): GRANT ROLE writes TO GROUP inserters
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20180314171010_f34511df-ac0a-455d-9bd5-32eaa95da4e9); Time taken: 0.054 seconds
INFO  : Executing command(queryId=hive_20180314171010_f34511df-ac0a-455d-9bd5-32eaa95da4e9): GRANT ROLE writes TO GROUP inserters
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20180314171010_f34511df-ac0a-455d-9bd5-32eaa95da4e9); Time taken: 0.026 seconds
INFO  : OK
No rows affected (0.093 seconds)
0: jdbc:hive2://ip-10-0-0-166.eu-west-1.compu> Closing: 0: jdbc:hive2://ip-10-0-0-166.eu-west-1.compute.internal:10000/default;principal=hive/_HOST@JCONCA.COM
```

Testing George
```
[centos@ip-10-0-0-148 ~]$ kinit george
Password for george@JCONCA.COM:
[centos@ip-10-0-0-148 ~]$ beeline
Beeline version 1.1.0-cdh5.9.3 by Apache Hive
beeline> !connect jdbc:hive2://ip-10-0-0-166.eu-west-1.compute.internal:10000/default;principal=hive/_HOST@JCONCA.COM
scan complete in 1ms
Connecting to jdbc:hive2://ip-10-0-0-166.eu-west-1.compute.internal:10000/default;principal=hive/_HOST@JCONCA.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.3)
Driver: Hive JDBC (version 1.1.0-cdh5.9.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-10-0-0-166.eu-west-1.compu> show tables;
INFO  : Compiling command(queryId=hive_20180314171010_009c799f-0aa4-4d6f-afec-60f4ed865782): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20180314171010_009c799f-0aa4-4d6f-afec-60f4ed865782); Time taken: 0.061 seconds
INFO  : Executing command(queryId=hive_20180314171010_009c799f-0aa4-4d6f-afec-60f4ed865782): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20180314171010_009c799f-0aa4-4d6f-afec-60f4ed865782); Time taken: 0.155 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.309 seconds)
0: jdbc:hive2://ip-10-0-0-166.eu-west-1.compu> Closing: 0: jdbc:hive2://ip-10-0-0-166.eu-west-1.compute.internal:10000/default;principal=hive/_HOST@JCONCA.COM
```


Testing ferdinand
```
[centos@ip-10-0-0-148 ~]$ kinit ferdinand
Password for ferdinand@JCONCA.COM:
[centos@ip-10-0-0-148 ~]$ beeline
Beeline version 1.1.0-cdh5.9.3 by Apache Hive
beeline> !connect jdbc:hive2://ip-10-0-0-166.eu-west-1.compute.internal:10000/default;principal=hive/_HOST@JCONCA.COM
scan complete in 1ms
Connecting to jdbc:hive2://ip-10-0-0-166.eu-west-1.compute.internal:10000/default;principal=hive/_HOST@JCONCA.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.3)
Driver: Hive JDBC (version 1.1.0-cdh5.9.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-10-0-0-166.eu-west-1.compu> show tables;
INFO  : Compiling command(queryId=hive_20180314171111_7e2cfd0c-5b40-4a89-9854-cd30785598b6): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20180314171111_7e2cfd0c-5b40-4a89-9854-cd30785598b6); Time taken: 0.075 seconds
INFO  : Executing command(queryId=hive_20180314171111_7e2cfd0c-5b40-4a89-9854-cd30785598b6): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20180314171111_7e2cfd0c-5b40-4a89-9854-cd30785598b6); Time taken: 0.119 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.284 seconds)
0: jdbc:hive2://ip-10-0-0-166.eu-west-1.compu>
```
