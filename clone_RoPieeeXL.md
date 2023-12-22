# How to clone a RoPieee installation

* Clone the RoPieee SD card

* Reinstall Roon Bridge

* Remove a previous Roon installation
```shell
rm -rf /opt/RoonBridge
rm -rf /var/roon
```

* Download Roon Bridge installer
```shell
cd /tmp
wget https://download.roonlabs.net/builds/roonbridge-installer-linuxarmv7hf.sh
chmod +x roonbridge-installer-linuxarmv7hf.sh
```

* Update the installation file:
```shell
vi roonbridge-installer-linuxarmv7hf.sh
```

Replace `curl -L -# -o "$TMPDIR/$PACKAGE_FILE" "$PACKAGE_URL"` with `wget -O "$TMPDIR/$PACKAGE_FILE" "$PACKAGE_URL"`

* Install Roon Bridge
```shell
./roonbridge-installer-linuxarmv7hf.sh
```

## Update Tidal Connect service

* Follow the steps in section **Configure Tidal Connect service**
