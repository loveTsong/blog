# linux

## service

systemctl

- 编写xxx.service 放到/etc/systemmd/system目录

```ini
[Unit]
Description=xxx
After=xx
StartLimitIntervaSec=0
[Service]
Type=simple
Restart=always
RestartSec=1
EsecStart=script
ExecReload=script
ExecStop=script

[Install]
WantedBy=multi-user.target
```

生效
systemctl daemon-reload
控制服务
systemctl start/stop/restart xxx.service
服务自启动
systemctl enable xxx.service
systemctl is-enabled xxx.service
