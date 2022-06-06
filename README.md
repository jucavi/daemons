# HOW TO

1. Find the path to your python runtime.
```
$ which python3
```
This will return something like /usr/bin/python, use this later as <PYTHON-PATH>

2. Create service:
```
$ sudo systemctl --force --full- edit <SCRIPT-NAME>.service
```
And paste the content of <SCRIPT-NAME>.service file located in this folder


3.Save it and reload all Systemd services via
```
$ sudo systemctl daemon-reload
```

4. Enable autostart on boot of your new service
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
