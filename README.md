

<b>Purpose:</b> Create a device to provide audio notifications triggered by events occurring in a DIY OpenHAB/MQTT system.

Hardware components:
     ESP-12 NodeMCU - 
     DFPlayer module - 
     Speaker -
     5v power supply -

Prerequisites:  The DFPlayer modules requires a FAT32 formatted SD card (max size 16GB) with the mp3 files needed for the project saved to it. The alphanumeric order of the mp3 file on the SD card determines the track number assigned when the DFPlayer module is initialized. For simplicity, it is easier to prefix the mp3 file name with a 3 digit track number beginning with 001 and continuing sequentially to 255. For example, the track named 003_NotificationCenterActive.mp3 will be played when the code DFPlayer.play(3) executes and there are 2 files listed before for it on the SD card, i.e. 001_xxxxxxx.mp3 and 002_xxxxxxx.mp3.

This table indicates the MP3 files I used for this project and the associated track numbers. These files were created using www.fromtexttospeech.com.
<table>
<tr><td>Track #</td><td>File name</td></tr>
<tr><td>1</td><td>001_xxxxxxxx.mp3</td></tr>
<tr><td>2</td><td>002_xxxxxxxx.mp3</td></tr>
</table>

Software Roadmap
     Hardware Capabilities Test
         On boot play audio file
         Connect to WIFI
         Set hostname
         Web Server publishing connects of SD Card with ability to play each notification listed
         Handle URL Request

     Enable generic MQTT Subscription notification

     Setup configuration through WIFI Access Point

     Allow for multiple MQTT subscriptions and configuration via web interface
