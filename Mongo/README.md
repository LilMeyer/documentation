MongoDB
---

## Dev ops manager

[Download](https://www.mongodb.com/subscription/downloads/ops-manager)
[Installation](https://docs.opsmanager.mongodb.com/current/tutorial/install-simple-test-deployment/?_ga=1.88311387.1703987670.1431251377)

### Start service

```sh
sudo start mongodb-mms-monitoring-agent
```

### Ops Manager Application conf file
```sh
sudo vim /opt/mongodb/mms/conf/conf-mms.properties
```

### Monitoring agent conf file

```sh
sudo vim /etc/mongodb-mms/monitoring-agent.config
```

### Log location [[*]](https://docs.mms.mongodb.com/tutorial/rotate-agent-log-files/)
```sh
vim /var/log/mongodb-mms/monitoring-agent.log
```


References
---
