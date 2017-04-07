The command and output for hdfs dfs -ls /user
==============================================

```````
[centos@ip-172-31-0-59 ~]$ hdfs dfs -ls /user
Found 7 items
drwxr-xr-x   - hdfs   supergroup          0 2017-03-24 18:50 /user/berkeley  <-- permissions
drwxr-xr-x   - hdfs   supergroup          0 2017-03-24 18:50 /user/hdfs
drwxrwxrwx   - mapred hadoop              0 2017-03-24 18:48 /user/history
drwxrwxr-t   - hive   hive                0 2017-03-24 18:49 /user/hive
drwxrwxr-x   - hue    hue                 0 2017-03-24 18:49 /user/hue
drwxrwxr-x   - oozie  oozie               0 2017-03-24 18:49 /user/oozie
drwxr-xr-x   - hdfs   supergroup          0 2017-03-24 18:51 /user/stanford  <-- permissions
[centos@ip-172-31-0-59 ~]$
````````


The output from the CM API call ../api/v14/hosts
=================================================

`````````
[centos@ip-172-31-0-59 ~]$ curl -X GET -u "admin:admin" -i http://ec2-54-169-203-13.ap-southeast-1.compute.amazonaws.com:7180/api/v14/hosts


HTTP/1.1 200 OK
Expires: Thu, 01-Jan-1970 00:00:00 GMT
Set-Cookie: CLOUDERA_MANAGER_SESSIONID=xk60npugpruwa3iowz0z05bs;Path=/;HttpOnly
Content-Type: application/json
Date: Fri, 24 Mar 2017 18:53:51 GMT
Transfer-Encoding: chunked
Server: Jetty(6.1.26.cloudera.4)

{
  "items" : [ {
    "hostId" : "8912daff-f911-4203-89b4-58f1745202ce",
    "ipAddress" : "172.31.0.59",
    "hostname" : "ip-172-31-0-59.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-2-214.ap-southeast-1.compute.internal:7180/cmf/hostRedirect/8912daff-f911-4203-89b4-58f1745202ce",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15332438016
  }, {
    "hostId" : "ee2b3c14-2206-4901-9e49-e374f771109a",
    "ipAddress" : "172.31.2.150",
    "hostname" : "ip-172-31-2-150.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-2-214.ap-southeast-1.compute.internal:7180/cmf/hostRedirect/ee2b3c14-2206-4901-9e49-e374f771109a",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15332438016
  }, {
    "hostId" : "96c99c39-29dc-409e-822a-9536fcdb666d",
    "ipAddress" : "172.31.2.214",
    "hostname" : "ip-172-31-2-214.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-2-214.ap-southeast-1.compute.internal:7180/cmf/hostRedirect/96c99c39-29dc-409e-822a-9536fcdb666d",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15332438016
  }, {
    "hostId" : "70e12cc4-0c84-4926-8b62-1b4072d0ef63",
    "ipAddress" : "172.31.9.165",
    "hostname" : "ip-172-31-9-165.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-2-214.ap-southeast-1.compute.internal:7180/cmf/hostRedirect/70e12cc4-0c84-4926-8b62-1b4072d0ef63",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15332438016
  }, {
    "hostId" : "76747b45-b35b-45da-ac06-a53134f0af84",
    "ipAddress" : "172.31.9.167",
    "hostname" : "ip-172-31-9-167.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-2-214.ap-southeast-1.compute.internal:7180/cmf/hostRedirect/76747b45-b35b-45da-ac06-a53134f0af84",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15332438016
  } ]
``````````````` <--- this won't do anything in Markdown, by the way. It reads for three ` once only at the beginning of a line.
