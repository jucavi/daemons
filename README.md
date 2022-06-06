# HOW TO

1. Create service:
```
$ sudo systemctl --force --full edit <SCRIPT-NAME>.service
```
And paste the content of <SCRIPT-NAME>.service file located in this folder (e.g. filterbot.service)


2.Save it and reload all Systemd services via
```
$ sudo systemctl daemon-reload
```

3. Enable autostart on boot of your new service
```
$ sudo systemctl enable <SCRIPT-NAME>.service
```



# Stop & Restart

You can stop your service by executing
```
$ sudo systemctl stop <SCRIP-NAME>.service
```

You can restart your service by executing
```
$ sudo systemctl restart <SCRIPT-NAME>.service
```

# Status & Basic logs

Check if your service is running or crashed
```
$ sudo systemctl status <SCRIPT-NAME>.service
```
This will also show you the last few lines logged by your script (e.g. print statements).

# Disable autostart again

Disable autostart for your new service at any time
```
$ sudo systemctl disable <SCRIPT-NAME>.service
```
