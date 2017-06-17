## Setup script for installing kat5200 (atari 5200 emulator) in retropie.


### Usage:
**from a (SSH) terminal:**<br>
*wget https://raw.githubusercontent.com/futurechild/Kat5200-Retropie/master/install*<br>
*chmod +x install*<br>
*sudo ./install*<br>
 
 
**Notes:** 

By default a (default) config gets copied over everytime the emulator is started, this can be stopped by editing emulators.cfg and removing the following:<br>
*yes | cp -rf /opt/retropie/configs/atari5200/default_config.db3 /home/pi/.kat5200/kat5200.db3 ;*<br>
Configuration file can be saved by entering the following command:<br>
*cp /home/pi/.kat5200/kat5200.db3 /opt/retropie/configs/atari5200/default_config.db3*<br>

or:<br>
*cp /home/pi/.kat5200/kat5200.db3 /opt/retropie/configs/atari5200/config1.db3*<br>

At this point the emulator does not support specifying config files, future versions should have this option according to it's developer. Below is a way to get around this until a new version is available.

Different config files can be achieved by editing emulators.cfg and making a new entry with changed filename,
replacing the emulator name and config file.

i.e. add the following line:<br>
*config1 = "yes | cp -rf /opt/retropie/configs/atari5200/config1.db3 /home/pi/.kat5200/kat5200.db3 ;/opt/retropie/emulators/retroarch/bin/retroarch -L /usr/local/bin/kat5200 %ROM%"*<br>

or:<br>
*Config2 = "yes | cp -rf /opt/retropie/configs/atari5200/anotherconfig.db3 /home/pi/.kat5200/kat5200.db3 ;/opt/retropie/emulators/retroarch/bin/retroarch -L /usr/local/bin/kat5200 %ROM%"*<br>
 
 


