# Raspberry Pi

**Connect to WiFi**

Edit  `/etc/wpa_supplicant/wpa_supplicant.conf` and append the following content:

```text
network={
    ssid="WiFi SSID"
    psk="WiFi Password"
}
```

### **SSH to Raspberry Pi**

**Enable SSH:**

put a file called `ssh` into `/boot` directory \([more](https://www.raspberrypi.org/documentation/remote-access/ssh/)\)

`ssh pi@[ip]`

**find the raspberry pi IP in the same network:**

```text
nmap -sP 192.168.0.0/24
```

**Default ssh password**:`raspberry`

**Open a GUI app \(VLC\) via ssh**

```text
export DISPLAY=:0 && vlc
```

