
### Hi Audiophile 👋


# Tidal Connect RopieeeXL setup instructions

###### Step by Step

#1./ **Download Tidal**
> wget https://github.com/dutu/Tidal-Connect-RopieeeXL/raw/main/opttidal.tar.gz
> 
> wget https://github.com/dutu/Tidal-Connect-RopieeeXL/raw/main/tidalservice.tar.gz
>
#2./ **Download Aarch64 package dependencies**
> wget https://github.com/dutu/Tidal-Connect-RopieeeXL/raw/main/tidallibs.tgz
> 
> 
####
####
#3./ **Extract Tidal Connect**
> tar -xf /root/opttidal.tar.gz --overwrite -C /
> 
> tar -xf /root/tidalservice.tar.gz --overwrite -C /
> 
> 
####
####
#4./ **Extract Aarch64 package dependencies**
> tar -xf /root/tidallibs.tgz -C /usr/lib/
>

#5./ **Check device**
> /opt/tidal/pa_devs/bin/ifi-pa-devs-get
> 
Copy device name, sample: snd_rpi_rpi_dac: RPi-DAC HiFi pcm1794a-codec-0 (hw:1,0)
> 
WinCSP edit this file or vi /etc/systemd/system/tidal.service
> 
To replace --playback-device, sample: --playback-device "snd_rpi_rpi_dac: RPi-DAC HiFi pcm1794a-codec-0 (hw:1,0)" \
> 
####

####
####
#6./ **Start**
> systemctl daemon-reload
> 
> systemctl enable tidal.service
> 
> systemctl restart tidal.service
> 
> systemctl status tidal.service
> 
####
####
