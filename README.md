
### Hi Audiophile 👋


# Tidal Connect RopieeeXL setup instructions

###### Step by Step

* Download Tidal:
```shell
wget https://github.com/dutu/Tidal-Connect-RopieeeXL/raw/main/opttidal.tar.gz
wget https://github.com/dutu/Tidal-Connect-RopieeeXL/raw/main/tidalservice.tar.gz
```

* Download Aarch64 package dependencies:
```shell
wget https://github.com/dutu/Tidal-Connect-RopieeeXL/raw/main/tidallibs.tgz
```

* Extract Tidal Connect:
```shell
tar -xf /root/opttidal.tar.gz --overwrite -C /
tar -xf /root/tidalservice.tar.gz --overwrite -C /
```

* Extract Aarch64 package dependencies:
```shell
tar -xf /root/tidallibs.tgz -C /usr/lib/
```

* Check device: 
```shell
/opt/tidal/pa_devs/bin/ifi-pa-devs-get
```

You get an output like this, from which you have to read the "name" of the DAC device you wish to use. While you are doing this the connected DAC must be plugged in, switched on and configured in RoPieee interface (`Audio HAT` field):

```text
ALSA lib confmisc.c:767:(parse_card) cannot find card '0'
ALSA lib conf.c:4745:(_snd_config_evaluate) function snd_func_card_driver returned error: No such file or directory
ALSA lib confmisc.c:392:(snd_func_concat) error evaluating strings
ALSA lib conf.c:4745:(_snd_config_evaluate) function snd_func_concat returned error: No such file or directory
ALSA lib confmisc.c:1246:(snd_func_refer) error evaluating name
ALSA lib conf.c:4745:(_snd_config_evaluate) function snd_func_refer returned error: No such file or directory
ALSA lib conf.c:5233:(snd_config_expand) Evaluate error: No such file or directory
ALSA lib pcm.c:2660:(snd_pcm_open_noupdate) Unknown PCM sysdefault
ALSA lib confmisc.c:767:(parse_card) cannot find card '0'
ALSA lib conf.c:4745:(_snd_config_evaluate) function snd_func_card_driver returned error: No such file or directory
ALSA lib confmisc.c:392:(snd_func_concat) error evaluating strings
ALSA lib conf.c:4745:(_snd_config_evaluate) function snd_func_concat returned error: No such file or directory
ALSA lib confmisc.c:1246:(snd_func_refer) error evaluating name
ALSA lib conf.c:4745:(_snd_config_evaluate) function snd_func_refer returned error: No such file or directory
ALSA lib conf.c:5233:(snd_config_expand) Evaluate error: No such file or directory
ALSA lib pcm.c:2660:(snd_pcm_open_noupdate) Unknown PCM sysdefault
ALSA lib pcm.c:2660:(snd_pcm_open_noupdate) Unknown PCM cards.pcm.front
ALSA lib pcm.c:2660:(snd_pcm_open_noupdate) Unknown PCM cards.pcm.rear
ALSA lib pcm.c:2660:(snd_pcm_open_noupdate) Unknown PCM cards.pcm.center_lfe
ALSA lib pcm.c:2660:(snd_pcm_open_noupdate) Unknown PCM cards.pcm.side
ALSA lib pcm.c:2660:(snd_pcm_open_noupdate) Unknown PCM cards.pcm.surround21
ALSA lib pcm.c:2660:(snd_pcm_open_noupdate) Unknown PCM cards.pcm.surround21
ALSA lib pcm.c:2660:(snd_pcm_open_noupdate) Unknown PCM cards.pcm.surround40
ALSA lib pcm.c:2660:(snd_pcm_open_noupdate) Unknown PCM cards.pcm.surround41
ALSA lib pcm.c:2660:(snd_pcm_open_noupdate) Unknown PCM cards.pcm.surround50
ALSA lib pcm.c:2660:(snd_pcm_open_noupdate) Unknown PCM cards.pcm.surround51
ALSA lib pcm.c:2660:(snd_pcm_open_noupdate) Unknown PCM cards.pcm.surround71
ALSA lib confmisc.c:767:(parse_card) cannot find card '0'
ALSA lib conf.c:4745:(_snd_config_evaluate) function snd_func_card_driver returned error: No such file or directory
ALSA lib confmisc.c:392:(snd_func_concat) error evaluating strings
ALSA lib conf.c:4745:(_snd_config_evaluate) function snd_func_concat returned error: No such file or directory
ALSA lib confmisc.c:1246:(snd_func_refer) error evaluating name
ALSA lib conf.c:4745:(_snd_config_evaluate) function snd_func_refer returned error: No such file or directory
ALSA lib conf.c:5233:(snd_config_expand) Evaluate error: No such file or directory
ALSA lib pcm.c:2660:(snd_pcm_open_noupdate) Unknown PCM iec958
ALSA lib confmisc.c:767:(parse_card) cannot find card '0'
ALSA lib conf.c:4745:(_snd_config_evaluate) function snd_func_card_driver returned error: No such file or directory
ALSA lib confmisc.c:392:(snd_func_concat) error evaluating strings
ALSA lib conf.c:4745:(_snd_config_evaluate) function snd_func_concat returned error: No such file or directory
ALSA lib confmisc.c:1246:(snd_func_refer) error evaluating name
ALSA lib conf.c:4745:(_snd_config_evaluate) function snd_func_refer returned error: No such file or directory
ALSA lib conf.c:5233:(snd_config_expand) Evaluate error: No such file or directory
ALSA lib pcm.c:2660:(snd_pcm_open_noupdate) Unknown PCM spdif
ALSA lib confmisc.c:767:(parse_card) cannot find card '0'
ALSA lib conf.c:4745:(_snd_config_evaluate) function snd_func_card_driver returned error: No such file or directory
ALSA lib confmisc.c:392:(snd_func_concat) error evaluating strings
ALSA lib conf.c:4745:(_snd_config_evaluate) function snd_func_concat returned error: No such file or directory
ALSA lib confmisc.c:1246:(snd_func_refer) error evaluating name
ALSA lib conf.c:4745:(_snd_config_evaluate) function snd_func_refer returned error: No such file or directory
ALSA lib conf.c:5233:(snd_config_expand) Evaluate error: No such file or directory
ALSA lib pcm.c:2660:(snd_pcm_open_noupdate) Unknown PCM spdif
ALSA lib pcm.c:2660:(snd_pcm_open_noupdate) Unknown PCM cards.pcm.hdmi
ALSA lib pcm.c:2660:(snd_pcm_open_noupdate) Unknown PCM cards.pcm.hdmi
ALSA lib pcm.c:2660:(snd_pcm_open_noupdate) Unknown PCM cards.pcm.modem
ALSA lib pcm.c:2660:(snd_pcm_open_noupdate) Unknown PCM cards.pcm.modem
ALSA lib pcm.c:2660:(snd_pcm_open_noupdate) Unknown PCM cards.pcm.phoneline
ALSA lib pcm.c:2660:(snd_pcm_open_noupdate) Unknown PCM cards.pcm.phoneline
D: bluealsa-pcm.c:1057: Getting BlueALSA PCM: CAPTURE 00:00:00:00:00:00 a2dp
ALSA lib bluealsa-pcm.c:1061:(_snd_pcm_bluealsa_open) Couldn't get BlueALSA PCM: The name org.bluealsa was not provided by any .service files
D: bluealsa-pcm.c:1057: Getting BlueALSA PCM: PLAYBACK 00:00:00:00:00:00 a2dp
ALSA lib bluealsa-pcm.c:1061:(_snd_pcm_bluealsa_open) Couldn't get BlueALSA PCM: The name org.bluealsa was not provided by any .service files
ALSA lib confmisc.c:767:(parse_card) cannot find card '0'
ALSA lib conf.c:4745:(_snd_config_evaluate) function snd_func_card_driver returned error: No such file or directory
ALSA lib confmisc.c:392:(snd_func_concat) error evaluating strings
ALSA lib conf.c:4745:(_snd_config_evaluate) function snd_func_concat returned error: No such file or directory
ALSA lib confmisc.c:1246:(snd_func_refer) error evaluating name
ALSA lib conf.c:4745:(_snd_config_evaluate) function snd_func_refer returned error: No such file or directory
ALSA lib conf.c:5233:(snd_config_expand) Evaluate error: No such file or directory
ALSA lib pcm.c:2660:(snd_pcm_open_noupdate) Unknown PCM dmix
connect(2) call to /dev/shm/jack-0/default/jack_0 failed (err=No such file or directory)
attempt to connect to server failed
device#0=snd_rpi_hifiberry_digi: HifiBerry Digi HiFi wm8804-spdif-0 (hw:1,0)
Number of devices = 1
```


* Copy device name, sample: `snd_rpi_hifiberry_digi: HifiBerry Digi HiFi wm8804-spdif-0 (hw:1,0)`

* Edit file `/etc/systemd/system/tidal.service`
```shell
vi /etc/systemd/system/tidal.service
```

* Replace `--playback-device` line, sample: `--playback-device "snd_rpi_hifiberry_digi: HifiBerry Digi HiFi wm8804-spdif-0 (hw:1,0)" \`

Example:
```text
[Unit]
Description=Tidal Connect Service
[Service]
Restart=on-failure
#Environment=LD_LIBRARY_PATH=/usr/local/share/lib
ExecStart=/opt/tidal/bin/tidal_connect \
                                --tc-certificate-path "/opt/tidal/id_certificate/IfiAudio_ZenStream.dat" \
                                -f "KEF Audio Streamer" \
                                --codec-mpegh true \
                                --codec-mqa false \
                                --model-name "KEF Audio Streamer" \
                                --disable-app-security false \
                                --disable-web-security false \
                                --enable-mqa-passthrough false \
                                --playback-device "snd_rpi_hifiberry_digi: HifiBerry Digi HiFi wm8804-spdif-0 (hw:1,0)" \
                                --log-level 3 \
                                --enable-websocket-log "0"

User=root
Group=root
RestartSec=1
KillMode=control-group
[Install]
WantedBy=multi-user.target
```

* Download the new certificate
```shell
cd /tmp
wget https://raw.githubusercontent.com/dutu/Tidal-Connect-RopieeeXL/main/IfiAudio_ZenStream.dat
ls -lsa /opt/tidal/id_certificate/
cp IfiAudio_ZenStream.dat /opt/tidal/id_certificate/
```

* Start the service:
```shell
systemctl daemon-reload
systemctl enable tidal.service
systemctl restart tidal.service
```

* Check status:
```shell
systemctl status tidal.service
```
