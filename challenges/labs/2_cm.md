
List the command and output for ls /etc/yum.repos.d

``````````````
Ajits-MacBook-Air:Downloads ajitkumaramit$ sh clustercmd.sh ls /etc/yum.repos.d
]CentOS-Base.repo       CentOS-Media.repo    CentOS-fasttrack.repo	 mysql-community.repo
CentOS-CR.repo	       CentOS-Sources.repo  cloudera-manager.repo
CentOS-Debuginfo.repo  CentOS-Vault.repo    mysql-community-source.repo
Connection to ec2-54-179-176-155.ap-southeast-1.compute.amazonaws.com closed.

CentOS-Base.repo       CentOS-Media.repo    CentOS-fasttrack.repo	 mysql-community.repo
CentOS-CR.repo	       CentOS-Sources.repo  cloudera-manager.repo
CentOS-Debuginfo.repo  CentOS-Vault.repo    mysql-community-source.repo
Connection to ec2-54-169-203-13.ap-southeast-1.compute.amazonaws.com closed.

CentOS-Base.repo       CentOS-Media.repo    CentOS-fasttrack.repo	 mysql-community.repo
CentOS-CR.repo	       CentOS-Sources.repo  cloudera-manager.repo
CentOS-Debuginfo.repo  CentOS-Vault.repo    mysql-community-source.repo
Connection to ec2-54-169-180-247.ap-southeast-1.compute.amazonaws.com closed.

CentOS-Base.repo       CentOS-Media.repo    CentOS-fasttrack.repo	 mysql-community.repo
CentOS-CR.repo	       CentOS-Sources.repo  cloudera-manager.repo
CentOS-Debuginfo.repo  CentOS-Vault.repo    mysql-community-source.repo
Connection to ec2-54-169-128-206.ap-southeast-1.compute.amazonaws.com closed.

CentOS-Base.repo       CentOS-Media.repo    CentOS-fasttrack.repo	 mysql-community.repo
CentOS-CR.repo	       CentOS-Sources.repo  cloudera-manager.repo
CentOS-Debuginfo.repo  CentOS-Vault.repo    mysql-community-source.repo
Connection to ec2-52-221-196-174.ap-southeast-1.compute.amazonaws.com closed.
Ajits-MacBook-Air:Downloads ajitkumaramit$ 
```````````````


Prepare database from CM node:
===============================

```````````
[centos@ip-172-31-2-214 yum.repos.d]$ sudo /usr/share/cmf/schema/scm_prepare_database.sh -h ip-172-31-9-165.ap-southeast-1.compute.internal  mysql scm cloudera-scm
Enter SCM password:
JAVA_HOME=/usr/java/jdk1.8.0_111
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.8.0_111/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
[                          main] DbCommandExecutor              INFO  Successfully connected to database.
All done, your SCM database is configured correctly!

`````


