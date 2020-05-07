# Disconnect WiFi clients from the AP based on their signal levels

**angry_wifi_with_params** is an enhanced version of the [angry_wifi.sh](<https://gist.githubusercontent.com/lg/e91d1c5c9640d963e13dbb1901bb4396/raw/3782c70c4cb7d2baa7a365fd85bb69293b0c8c07>) shell script that periodically tries to disconnect clients (STA) from an WiFi access point (SP) if the signal strength falls below a certain threshold.
It retains the features of the original angry_wifi.sh script plus adds new   ones as noted below.
Furthermore, parameters may be passed as options on the command line.

### Usage

```sh
  angry_wifi_with_params [-c maxcount] [-s minsignal] [-i wifi_interface] [-v] [-d] [-q]
```

### Notes

1. Tries to find the network interface for the access point automatically.
2. The number of runs can be limited (default: unlimited, i.e. maxcount=0).
3. Minimum signal strength before disconnection can be given on command line.
4. Different "reasons" are tried in sequence on the connected client (Only 5 is used as default).
5. There is a Lua version of the original script at <https://github.com/barbieri/barbieri-playground/tree/master/openwrt/wifi-disconnect-low-signal>.
7. The script is tested with the [ash](https://en.wikipedia.org/wiki/Almquist_shell) shell, but should run on [bash](https://www.gnu.org/software/bash), too. Just change the first line accordingly.
8. The script works with [BusyBox](https://busybox.net/) versions of common utilities as used in [LeDe/OpenWrt](https://openwrt.org/)
9. The script is tested with [Gluon](https://wiki.freifunk.net/Gluon) v2018.2.1, but it should run on other versions of Gluon, too.

### Known Issues

1. Disconnection seems to be limited to Apple (e.g. iPhones, IPads) products only.
2. Logs to syslog only, MQTT should be an option, too.

### Credits

1. To lantis_1008 as the probable creator of [angry_wifi.sh](<https://gist.githubusercontent.com/lg/e91d1c5c9640d963e13dbb1901bb4396/raw/3782c70c4cb7d2baa7a365fd85bb69293b0c8c07>).
