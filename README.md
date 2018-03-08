## Intro
- Ubuntu 16.04 version using systemd as default init system
- Anything process you want to automatically start in Ubuntu 16.04 should use this role template
- The service will be restart automatically if crashed or failure

## Commands
- The service can be stop/start via commands:
``` sh
sudo service custom_service start|stop|restart
```
- check status
``` sh
sudo service custom_service status
```
- Reload service config at /etc/systemd/system/ if changed 
``` sh
sudo systemctl daemon-reload
```


## Reference
- https://stackoverflow.com/questions/40113964/install-systemd-service-ansible
- https://www.freedesktop.org/software/systemd/man/systemd.service.html
- http://docs.ansible.com/ansible/latest/systemd_module.html

