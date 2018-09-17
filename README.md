## Intro
- Ubuntu 16.04 version using systemd as default init system
- Anything process you want to automatically start in Ubuntu 16.04 should use this role template
- The service will be restart automatically after system reboot or crashed during running

## Commands
- The service can be start/stop/restart via commands:
``` sh
sudo systemctl start|stop|restart SERVICENAME.service
```
- check status
``` sh
sudo systemctl status SERVICENAME.service
```
- Add/Enable the service to auto-start after system reboot
```sh
sudo systemctl enable SERVICENAME.service
```
- Remove/Disable the service to system reboot auto-start services list
```sh
sudo systemctl disable SERVICENAME.service
```
- Check the service will be auto-started after system reboot
```sh
sudo systemctl is-enabled SERVICENAME.service
```

- Reload service config if changed 
``` sh
sudo systemctl daemon-reload
```


## Reference
- https://www.digitalocean.com/community/tutorials/how-to-configure-a-linux-service-to-start-automatically-after-a-crash-or-reboot-part-1-practical-examples
- https://stackoverflow.com/questions/40113964/install-systemd-service-ansible
- https://www.freedesktop.org/software/systemd/man/systemd.service.html
- http://docs.ansible.com/ansible/latest/systemd_module.html
- https://www.digitalocean.com/community/questions/convert-run-at-startup-script-from-upstart-to-systemd-for-ubuntu-16
