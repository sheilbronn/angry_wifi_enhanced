# angry_wifi_enhanced

**angry_wifi_with_params** is an enhanced version of the [angry_wifi.sh](<https://gist.githubusercontent.com/lg/e91d1c5c9640d963e13dbb1901bb4396/raw/3782c70c4cb7d2baa7a365fd85bb69293b0c8c07>) shell script.
It retains the features of the original script plus additional ones as noted below.
Furthermore, parameters may be passed as options on the command line.

### Usage
```sh
  angry_wifi_with_params [-c maxcount] [-s minsignal] [-i wifi_interface] [-v]
```

### Notes

1. Tries to find the network interface for the access point automatically. Caches the result.
2. The number of runs can be limited (default: unlimited)
3. Minimum signal strength before disconnection can be given on command line.
4. Different "reasons" are tried in sequence on the connected client (Only 5 is used as default)
5. Should run on any Linux, not only OpenWrt (let me know if not)

### Known Issues

1. Disconnection seems to be limited to Apple products only.
2. Logs to syslog only, MQTT should be an option, too.
