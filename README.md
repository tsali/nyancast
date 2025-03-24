##############################################################################
 Description: sm0l script to cast NyanCat Dubstep to all LAN Chromecasts
 Author: Tsali - A network engineer of boredom
 Date: 2020/09/03                              
 OnlyFans: Tsali                               
 Twitch: TsaliThighmane
 Website: cultofjames.org                      

##############################################################################

This is a simple script that will allow you to cast Nyan Cat Dubstep by Alex S. (AKA Andromulus) to all Chromecast capable devices on a LAN, simultaneously.

ASSUMPTIONS:
1. You own the chromecasts and aren't doing anything malicious with this
2. You're using a Debian (apt) based system, but this could easily be converted to other linux systems
3. The script SHOULD download the necessary utilities, it did on my 4 test boxes (3 pi's and ubuntu server)

To install
1. Log into the bash capable server you're installing it in
2. git clone https://github.com/tsali/nyancast
3. cd into the nyancast directory
4. chmod +x nyancast
5. use from within the nyancast directory (IE ./nyancast or bash nyancast,) or copy to /bin or /usr/bin as necessary

For the copy/paste inclined:                                                                                      

```
git clone https://github.com/tsali/nyancast.git && cd nyancast && chmod +x nyancast && bash nyancast
```

Example usage:

```
pi@retropi3:~ $ ./nyancast
Get:1 http://archive.raspberrypi.org/debian buster InRelease [32.6 kB]
Hit:2 https://dtcooper.github.io/raspotify raspotify InRelease
Get:3 http://raspbian.raspberrypi.org/raspbian buster InRelease [15.0 kB]
Hit:4 https://repo.openwebrx.de/debian buster InRelease
Get:5 http://archive.raspberrypi.org/debian buster/main armhf Packages [330 kB]
Fetched 378 kB in 3s (108 kB/s)
Reading package lists... Done
Building dependency tree
Reading state information... Done
1 package can be upgraded. Run 'apt list --upgradable' to see it.
ffmpeg is installed, continuing
python3 is installed, continuing
python3-pip is installed, continuing
parallel is installed, continuing
catt is installed, continuing
Found the following chromecast IPs, sending /home/pi/music/NyanCatAlexSDub320b.mp3 to them now, enjoy
192.168.20.235
192.168.20.6
192.168.20.243
192.168.20.252
Casting local file /home/pi/music/NyanCatAlexSDub320b.mp3...
Playing "NyanCatAlexSDub320b" on "Bathroom"...
Serving local file(s).
192.168.20.243 - - [03/Sep/2020 21:59:39] "GET /?loaded_from_catt HTTP/1.1" 206 - audio/mp3 - 8.12 MB
Casting local file /home/pi/music/NyanCatAlexSDub320b.mp3...
Playing "NyanCatAlexSDub320b" on "Basement TV"...
Serving local file(s).
192.168.20.235 - - [03/Sep/2020 21:59:42] "GET /?loaded_from_catt HTTP/1.1" 206 - audio/mp3 - 8.12 MB
Casting local file /home/pi/music/NyanCatAlexSDub320b.mp3...
Playing "NyanCatAlexSDub320b" on "Living Room TV"...
Serving local file(s).
192.168.20.252 - - [03/Sep/2020 21:59:43] "GET /?loaded_from_catt HTTP/1.1" 206 - audio/mp3 - 8.12 MB
Casting local file /home/pi/music/NyanCatAlexSDub320b.mp3...
Playing "NyanCatAlexSDub320b" on "Basement speaker"...
Serving local file(s).
192.168.20.6 - - [03/Sep/2020 21:59:39] "GET /?loaded_from_catt HTTP/1.1" 206 - audio/mp3 - 8.12 MB
```
