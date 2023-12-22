## Disable ping-analytics

> `/optRoPieee/sbin/ping-analytics`  script collects various system information from a RoPieee device, and sends it to a specified backend URL for analytics or monitoring purposes

* Check services status  
```shell
systemctl status ropieee-analytics.timer
systemctl status ropieee-analytics.service
```

```shell
cat /etc/systemd/system/ropieee-analytics.timer
cat /etc/systemd/system/ropieee-analytics.service
cat /opt/RoPieee/sbin/ping-analytics
```

* Disable `ropieee-analytics.timer`
```shell
systemctl disable ropieee-analytics.timer
systemctl stop ropieee-analytics.timer
systemctl status ropieee-analytics.timer
```

