### Pre Requisite
Install python bcrypt
```
**Ubuntu**
apt install python3-bcryp

**CentOS/Amazon Linux***
yum install python36-bcryp
```

Run `prom-passwd.py` to generate a password for prometheus. Then update the line 10 in prometheus/config-map.yml. Default username/password is admin/admin
`$ python3 prom-passwd.py`

### Resource
https://prometheus.io/docs/guides/basic-auth/
https://prometheus.io/docs/prometheus/latest/configuration/https/
