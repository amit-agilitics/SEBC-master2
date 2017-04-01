
```
centos@ip-172-31-2-214 krb5kdc]$ sudo cat kdc.conf
[kdcdefaults]
 kdc_ports = 88
 kdc_tcp_ports = 88

[realms]
AMIT-AGILITICS.HQ= {
  #master_key_type = aes256-cts
  acl_file = /var/kerberos/krb5kdc/kadm5.acl
  dict_file = /usr/share/dict/words
  admin_keytab = /var/kerberos/krb5kdc/kadm5.keytab
  supported_enctypes = aes256-cts-hmac-sha1-96:normal arcfour-hmac-md5:normal
   max_renewable_life = 7d
 }


 [centos@ip-172-31-2-214 krb5kdc]$ sudo cat  kadm5.acl
*/admin@AMIT-AGILITICS.HQ	*
cloudera-scm@AMIT-AGILITICS.HQ *
[centos@ip-172-31-2-214 krb5kdc]$

```
