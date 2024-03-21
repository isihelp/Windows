# WINGET

### Here's the step by step instructions to install winget

Open up powershell with your a-account:
Then copy and paste the script below:


```
Add-AppxPackage -RegisterByFamilyName -MainPackage Microsoft.DesktopAppInstaller_8wekyb3d8bbwe
$progressPreference = 'silentlyContinue'
Write-Information "Downloading WinGet and its dependencies..."
Invoke-WebRequest -Uri https://aka.ms/getwinget -OutFile Microsoft.DesktopAppInstaller_8wekyb3d8bbwe.msixbundle
Invoke-WebRequest -Uri https://aka.ms/Microsoft.VCLibs.x64.14.00.Desktop.appx -OutFile Microsoft.VCLibs.x64.14.00.Desktop.appx
Invoke-WebRequest -Uri https://github.com/microsoft/microsoft-ui-xaml/releases/download/v2.7.3/Microsoft.UI.Xaml.2.7.x64.appx -OutFile Microsoft.UI.Xaml.2.7.x64.appx
Add-AppxPackage Microsoft.VCLibs.x64.14.00.Desktop.appx
Add-AppxPackage Microsoft.UI.Xaml.2.7.x64.appx
Add-AppxPackage Microsoft.DesktopAppInstaller_8wekyb3d8bbwe.msixbundle
```

[https://aka.ms/winget](https://aka.ms/winget)
[https://learn.microsoft.com/en-us/windows/iot/iot-enterprise/deployment/install-winget-windows-iot](https://learn.microsoft.com/en-us/windows/iot/iot-enterprise/deployment/install-winget-windows-iot)





### After the install:

#### Search
```
winget search -q `"`"
winget search displaylink
```

```
winget install displaylink.graphicsDriver
winget install 9N09F8V8FS02
```

#### HP PC Hardware Diagnostics Windows

```winget install 9P4PNDG7L782```

#### HP Smart
```winget install 9WZDNCRFHWLH```

#### HP Scan and Capture
```winget install 9WZDNCRFHWL0```

### Better version of MPV
```winget install mpv.net```
```
winget search mpv
winget install 9P3JFR0CLLL6 --accept-package-agreements --accept-source-agreements -h
```

```winget install yt-dlp.yt-dlp```

```winget search OpenSpeedTest-Server```
```winget install 9PBKQKR4X79R```


```
ECHO Y | cmd /c winget upgrade --all --silent
```
```winget upgrade -uhr --accept-source-agreements --accept-package-agreements```


```ECHO Y | cmd /c winget upgrade -uhr --accept-source-agreements --accept-package-agreements -h  --silent```



### Displaying installed
```winget list --name Poly```

```winget list --upgrade-available```

#### Uninstalling
```winget uninstall Docker.DockerDesktop --disable-interactivity --silent```
```winget uninstall Ghisler.TotalCommander --disable-interactivity --silent```
```winget install Ghisler.TotalCommander --disable-interactivity --silent```

#### Install Dell Support Assistant
```winget install Dell.CommandUpdate.Universal```

#### MediaInfo
```winget install MediaArea.MediaInfo.GUI```

#### Python 3.12
```winget install 9NCVDN91XZQP```

#### FFmpeg
```winget install Gyan.FFmpeg```

#### or get Handbrake
```winget install HandBrake.HandBrake```

#### Installing VSC | for all user | no interactivity | force install | silent install
```winget install Microsoft.VisualStudioCode --scope machine --disable-interactivity --force -h```

#### UnInstalling VSC | for all user | no interactivity | force install | silent install
```winget usinstall Microsoft.VisualStudioCode --scope machine --disable-interactivity --force -h```

#### Installing PotPlayer | for all user | no interactivity | force install | silent install
```winget install Daum.PotPlayer --scope machine --disable-interactivity --force -h```

# 
```

winget install --id nomacs.nomacs --scope user --disable-interactivity --force -h
winget install --id KDE.Kdenlive --scope machine --disable-interactivity --force -h
winget install --id CPUID.CPU-Z --scope machine --disable-interactivity --force -h
winget install --id KDE.Krita --scope machine --disable-interactivity --force -h


winget install --id Audacity.Audacity --scope machine --disable-interactivity --force -h
winget install --id MiXXX.MiXXX --scope machine --disable-interactivity --force -h


winget install --id OBSProject.OBSStudio --scope machine --disable-interactivity --force -h
winget install --id NewTek.NDI5Runtime --scope machine --disable-interactivity --force -h
winget install --id NewTek.NDI5Tools --scope machine --disable-interactivity --force -h
```


#### Get version
```(get-appxpackage microsoft.desktopappinstaller).version```

#### How to update/upgrade you current App Installer
```winget upgrade Microsoft.AppInstaller```

#### If you want to download the program and install it manually then you can use this command
```winget download --id Microsoft.PowerShell```

#

### Great Tool for Backup that works for all OS
[FreeFileSync](https://freefilesync.org/download.php)


#

## Timezone

Get the current time zone
   - `Get-Timezone` or `Get-CimInstance Win32_TimeZone | select *`

Get time zones that match a specified string
   - `Get-TimeZone -Name "*pac*"`

Get all available time zones
   - `Get-TimeZone -ListAvailable`

Set the time zone by Id
   - `Set-TimeZone -Id "Pacific Standard Time" -PassThru`

```
w32tm / query / configuration
w32tm /config /manualpeerlist:132.189.40.119 /syncfromflags:manual /reliable:yes /update
w32tm /config /manualpeerlist:172.17.32.253 /syncfromflags:manual /reliable:yes /update
w32tm /config /manualpeerlist:time.windows.com /syncfromflags:manual /reliable:yes /update 'Use this if the time doesn't fixed it.
W32tm /resync /force
```

##### Added in 2021
In Windows Task Scheduler
Create Daily Task

Called it `Daily Auto Force shutdown`
```
schtasks /create /sc daily /tn "Daily auto force shutdown" /tr "c:\windows\system32\shutdown.exe /t 0 /s /f" /st 21:59
```

***_Now get in to NUC BIOS and get to the Power Setting
change the following_***

  -  `After Power Failure "Power On"`
  -  `Deep S4/5" "Check the mark"`
  -  `Wake on LAN from S4/S5 "Power On - Normal Boot"`
  -  `Wake System from S5 "Check the mark"`
  -  `Recurrence "Daily"`
     -  `Wakeup Hour "23"`
     -  `Wakeup Minutes "59"`
     -  `Wakeup Second"59"`
  -  `PCIe ASPM Support "unCheck the mark"`

The reset of the field should be set to default.



[Install Logitech Sync](https://download01.logi.com/web/ftp/pub/techsupport/cameras/LogiSyncInstaller_2.0.412.exe)

[Install VNC Viewer](https://www.tightvnc.com/download/2.8.27/tightvnc-2.8.27-gpl-setup-64bit.msi)

- Enable Remote Desktop

Execute this command in NUC PC

#### ***_Commands in the elevated Powershell:_***
```
Enable-PSRemoting -SkipNetworkProfileCheck -Force
Set-Item WSMan:\localhost\Client\TrustedHosts * -Force
Restart-Service WinRM
Get-Item WSMan:\localhost\Client\TrustedHosts
Get-NetConnectionProfile | Set-NetConnectionProfile -NetworkCategory Private
Set-NetFirewallProfile -Profile Private -Enabled False
winrm quickconfig -force
```

  - `Test-WSMan {enter ComputerName or IP Address}`
  - `winrs -r:IP Address or Computername -u:Computername\admin -p:password cmd or powershell`

Commands in the elevated command prompt:
```
netsh advfirewall firewall add rule name="ICMP allow incoming V4 echo request" protocol=icmpv4:8,any dir=in action=allow
```

##### This command will stop windows update
```
net stop wuauserv
net stop bits
net stop dosvc
sc config wuauserv start=disabled
```

###### If you want to re-enable the Windows updates at any later time, then give these commands in the elevated command prompt:
```
sc config wuauserv start=auto
sc start wuauserv
net start wuauserv
net start bits
net start dosvc
```

###### Schedule automatic restart
- `schtasks /create /sc daily /tn "Daily auto force shutdown" /tr "c:\windows\system32\shutdown.exe /t 0 /s /f" /st 21:59`

- `schtasks /create /sc daily /tn "Auto force reboot 3am" /tr "c:\windows\system32\shutdown.exe /t 0 /r /f" /st 03:00`

Make sure when to used powershell command
- `winrs -r:IP Address or Computername -u:Computername\admin -p:password powershell`

To View the currently
Powershell command remotely

- `Get-ItemProperty -Path HKLM:\Software\Microsoft\Windows\CurrentVersion\OEMInformation | Select-Object Model`

Set new Model name
- `Set-ItemProperty -Path HKLM:\Software\Microsoft\Windows\CurrentVersion\OEMInformation -name "Model" -Value "Logitech Image:M203"`

Set need to re-image
- `Set-ItemProperty -Path HKLM:\Software\Microsoft\Windows\CurrentVersion\OEMInformation -name "Model" -Value "Needs to be RE-IMAGE"`

- `Invoke-WebRequest -Uri https://www.gyan.dev/ffmpeg/builds/ffmpeg-release-essentials.zip -OutFile c:\yt\test1\test2\ffmpeg.zip`

- `shutdown /t 0 /r /f`

###### FFMPEG command
[FFMPEG](https://trac.ffmpeg.org/wiki/DirectShow)

Example to list dshow input devices:
- `ffmpeg -list_devices true -f dshow -i dummy`

Example to print a list of options from a selected device:
- `ffmpeg -f dshow -list_options true -i video="Integrated Camera"`

Example to use a dshow device as an input:
- `ffmpeg -f dshow -i video="Integrated Camera" out.mp4`

Example to use audio and video dshow device as an input:
- `ffmpeg -f dshow -i video="Integrated Camera":audio="Microphone name here" out.mp4`

Logitech Rally System
- `ffmpeg -f dshow -i video="Logi Rally Camera":audio="Echo Cancelling Speakerphone (3- Logi Rally Audio)" LRally.mp4`

###### Logitech Meetup System
- `ffmpeg -f dshow -i video="Logitech MeetUp":audio="Echo Cancelling Speakerphone (Logitech MeetUp Speakerphone)" LMeetup.mp4`
```
TRS.BAT
@echo off
rem net use x: \\fileserver\Sharefolder /user:domain\username password-here
c:
mkdir c:\ffmpeg
cd\ffmpeg
```

- `curl https://ffmpeg.zeranoe.com/builds/win64/static/ffmpeg-20200324-e5d25d1-win64-static.zip -O ffmpeg`
- `powershell expand-archive -path "c:\ffmpeg\ffmpeg-20200324-e5d25d1-win64-static.zip" -DestinationPath c:\ffmpeg\`
- `copy c:\ffmpeg\ffmpeg-20200324-e5d25d1-win64-static\bin\*.* c:\ffmpeg\`
- `ffmpeg -list_devices true -f dshow -i dummy`
- `Rem  the command below will only record meetup camera without audio.`
- `ffmpeg -f dshow -i video="Logitech MeetUp" meetupcam.mp4`
- `Rem this will only record video without audio.  => ffmpeg -f dshow -i video="Logi Rally Camera" Rallycam.mp4`
- `copy webcam.mp4 x:\it\filename`


This is command from your PC 
- `ffmpeg -f dshow -i video="Logitech MeetUp":audio="Echo Cancelling Speakerphone (Logitech MeetUp Speakerphone)" -profile:v high -pix_fmt yuvj420p -level:v 4.1 -preset ultrafast -tune zerolatency -vcodec libx264 -r 10 -b:v 512k -s 640x360 -acodec aac -ac 2 -ab 32k -ar 44100 -f mpegts -flush_packets 0 udp://192.177.6.85:5000?pkt_size=1316`

note: the IP Address 192.177.6.85 is your PC, that where you want to send the video feed
so now open up another cmd again.
change dir to yt
type in ffplay -i udp://0.0.0.0:5000
you'll get alot of error
it's okay just wait until you see the video feed.

- `ffmpeg -f dshow -video_size 1280x720 -framerate 30 -vcodec mjpeg -i video="Logitech MeetUp":audio="Echo Cancelling Speakerphone (Logitech MeetUp Speakerphone)" -preset ultrafast -tune zerolatency -vcodec libx264 -r 10 -b:v 512k -acodec aac -ac 2 -ab 32k -ar 44100 -f mpegts -flush_packets 0 udp://192.177.7.70:8090`

Same PC
type in this
- `ffplay udp://127.0.0.1:8090`
- `ffplay -f dshow -video_size 1280x720 -framerate 30 -vcodec mjpeg -i video="Logitech MeetUp":audio="Echo Cancelling Speakerphone (Logitech MeetUp Speakerphone)"`

###### Startup Command
- `shell:startup    ' current default account startup`
- `shell:common statrup ' common startup`
 
###### Sample command for capturing Video and Audio with Logitech Rally Plus System

                   [ Using Logitech Rally ]               [ Using Logitech Rally Plus Microphones ]  Filename 4 output         
`ffmpeg -f dshow -i video="Logi Rally Camera" -f dshow -i audio="Echo Cancelling Speakerphone (Logi Rally Audio)" output.mp4`


### Manually update MTR apps via Powershell command
[See section -Software updates via Powershell](https://docs.microsoft.com/en-us/microsoftteams/rooms/rooms-operations)
 
Note the trick is to download the [updated MSI](https://go.microsoft.com/fwlink/?linkid=851168) from the endpoint itself, while logged in with admin.

After you download the latest MSI install it, leave it as default location for installation folder. (Microsoft Teams Room App v4.5.35.0)
Once installation is complete then create new share, follow the instruction below

- Open Explorer in C:\Program Files (x86)
- Now select and right click on “Skype Room System Deployment Kit” folder, 
- Select properties, click tab Sharing, click Advanced Sharing.
- Click Share this folder, in Share name: called it MTR, 
- Click permissions, check allow for Full control, 
- Change and read. Click Apply, ok, Apply.

Now right click windows logo in the lower left corner, 
Select Windows Powershell(admin).
In the Powershell Window Terminal, 
Create new map to x by using net use example below.

Just copy and paste the command below to your powershell window
 
copy and paste the command, then press enter to execute it.

- `Net use x: \\localhost\mtr`

Now let’s do the update by copying the command below and pasting it to your powershell window
 
copy and paste the command, then press enter to execute it.

-     Add-AppxPackage  -ForceApplicationShutdown -Path 'x:\$oem$\$1\Rigel\x64\Ship\AppPackages\*\*.appx' -DependencyPath (Get-ChildItem 'x:\$oem$\$1\Rigel\x64\Ship\AppPackages\*\Dependencies\x64\*.appx' | Foreach-Object {$_.FullName})


Once it’s complete reboot the MTR system, it will reboot twice 
That’s it, you done.

## Logitech Recommended NUC updates process.

There are a few primary things that need to be done to alleviate this situation but I am going to provide you the recommended list of NUC updates that are recommended to minimize Teams related system issues.

### Recommended NUC updates process
On the NUC PC perform the following steps: (We recommend that the NUC power settings be set to always On never shutdown due to Tap Screen going to sleep and not waking due to Intel Power management of the internal motherboard USB/HDMI ports.

#### A. Boot into the Windows Admin account and change the Power setting (see attached) Note the power settings may be different depending on the version of Windows 10 your are using. The Intel Motherboard has power save options enabled that reduce power to sections of the circuits which cause issues with the displays and USB connections. So all power save options must be disabled.

In addition to the power setting changes on the attached document Microsoft has recently recommended going into the Device Manager and  then disable the "turn this device off to save power" feature on all USB Root Hubs on a given device. Select the USB Controllers - Root Hub device then right click then select "Properties" then select the "Power management" tab and un-check " Allow computer to turn this device off to save power".

### Disable USB HUB Allow Computer Turn Off Save Power
[Disable USB HUB](https://community.spiceworks.com/topic/2190400-disable-usb-hub-allow-computer-turn-off-save-power)
Before you can run make sure you execute this command first "Powershell -ExecutionPolicy Bypass" under (Admin).
```
$USBHubs = Get-WmiObject -Class Win32_USBHub
$PowerMgmt = Get-WmiObject -Class MSPower_DeviceEnable -Namespace root\wmi

ForEach ($Hub in $USBHubs) {
    Write-Host
    Write-Host -Object "Checking USB Hub '$($Hub.Name)'..."
    $VarPowerSettings = $PowerMgmt | Where {$_.InstanceName -like "*$($Hub.DeviceID)*"}
    If (($VarPowerSettings | Measure).Count -eq 1) {
        If (($VarPowerSettings | Select -ExpandProperty Enable) -eq $False) {Write-Host -Object "USB Hub '$($Hub.Name)' already has power saving disabled" -ForegroundColor Green}
        Else {
            Try {
                $VarPowerSettings.Enable = $False
                $Null = $VarPowerSettings.psbase.Put()
                Write-Host -Object "Disabled power saving features for USB Hub '$($Hub.Name)'" -ForegroundColor Green
            }
            Catch {Write-Warning -Message "One or more exceptions occurred when trying to set power saving settings for USB Hub '$($Hub.Name)'"}
        }
    }
    ElseIf (($VarPowerSettings | Measure).Count -gt 1) {Write-Warning -Message "More than one WMI object representing power settings was found for '$($Hub.Name)', no settings have been changed for this device"}
    Else {Write-Warning -Message "No power settings were found for '$($Hub.Name)', please check if the device supports power saving features"}
}
```

#### "Power Saver MTR"


<img width="1024" alt="mssrs" src="https://github.com/nucpc/info/blob/main/docs/images/PowerNUC.png?raw=true">

### Force Windows to remove and re-detect an USB 3 Device
<img width="1024" alt="mssrs" src="https://github.com/nucpc/info/blob/main/docs/images/reset_USB3.png?raw=true">

[URL info](https://knowledge.ni.com/KnowledgeArticleDetails?id=kA00Z000000P7bZSAS)


Boot into Windows
To boot into Windows connect a Keyboard to the NUC then reboot it while it is coming up tap the Windows Key over and over until the Windows Login comes up on the screen. The select the Teams Admin account - password is sfb once completed with changes logout then login to the User account same password.

#### B. Install the intel driver and support assistant (Intel DSA) in the Windows Admin account and run the Intel Device Driver Assistant to ensure that the NUC is running the most updated versions of all required drivers.

[Link - Intel Support Assistant](https://www.intel.com/content/www/us/en/support/detect.html)


By default, the Intel® Driver & Support Assistant places downloaded drivers in
- `C:\ProgramData\Intel\DSA\Downloads`



Press WinKey+R > type taskschd.msc 
and press Enter (it will launch Task Scheduler)
Left click from the right pane on the Task Scheduler Library > 
Open Action from the top menu > New Folder... > name it MyTasks > click OK
Left click on the MyTasks > choose Action from menu > 
Create Basic Task... (it will open task wizard)
You can enter the Name , for example "Restart", and press Next
In Trigger section you can specify when you want to run your task, for example:
Select Daily , and press Next
Now you can specify the day, the hour and set to recur every day, 
After that press Next
In Action section you can choose what you want to run, 
for example restart your system, to do this:
choose Start a program , 
and press Next in the Program/script field 
type shutdown /r , and press Next
And that's all, you can press Finish

or can be done via CMD, script below.
schtasks /create /sc daily /tn "Daily auto force reboot" /tr "c:\windows\system32\shutdown.exe /t 0 /r /f" /st 23:59






##### Windows Shell Commands
[Shell Commands for Windows 10: Navigating Common Folders in Windows](https://www.mirazon.com/shell-commands-for-windows-10-navigating-common-folders-in-windows/)

#### Create God Mode folder in your Desktop


Create a folder in your desktop called it 
- `"GodMode.{ED7BA470-8E54-465E-825C-99712043E01C}"`

You call also run it by hold Windows Key + R to open Run command and then paste this
- `shell:::{ED7BA470-8E54-465E-825C-99712043E01C}`

###### Good to remember command with shell commands

- `shell:Startup               - Current User Startup`
- `shell:Common Startup        - All Startup`
- `shell:connectionsfolder     - It will bring you to the network connection`
- `shell:Downloads`
- `shell:Favorites`
- `shell:Profile`
- `shell:UserProfiles`
- `shell:Windows`




[myForm](https://forms.office.com/Pages/ResponsePage.aspx?id=g7S4tZdV50qOJ_zEZKO1hAhlnEPJ44dOhJgtFWeMOhNUMkcxWEZGTVA2UjVVVUswTkM0MFdMRlNVTC4u) 
-

`find it (Get-WmiObject -query ‘select * from SoftwareLicensingService’).OA3xOriginalProductKey`

Get present PnP devices in specified states

***_Run it under Powershell command_***
-

***_Display only Logitech devices_***
 - `get-pnpdevice -friendlyname *logi* | select status, Class, FriendlyName, InstanceID`   
***_Display all AudioEndpoint, MEDIA, USBDevice devices_***
 - `Get-PnpDevice -Class AudioEndpoint,MEDIA,USBDevice`     
***_Display only Unknown devices_***               
 - `Get-PnpDevice -Class AudioEndpoint, MEDIA, USBDevice -Status Unknown`  
***_Display only Unknown devices for Logitech_***               
 - `Get-PnpDevice -friendlyname *logi* -Status Unknown | Select Status, InstanceID, FriendlyName`  
***_Will disable only Unknown devices for Logitech_***               
 - `Get-PnpDevice -friendlyname *logi* -Status Unknown | % { Disable-PnpDevice -InputObject $_ -ErrorAction SilentlyContinue }`  


<img width="1024" alt="getpnpdevice" src="https://github.com/nucpc/info/blob/main/Sardegna.jpg?raw=true">



***_First type in_***
Powershell Admin command
- 'get-pnpdevice -FriendlyName '*Poly*' | Select Stauts, Class, FriendlyName, InstanceID'

or

- 'get-pnpdevice -Class AudioEndpoint | Where-Object {$_.FriendlyName -like "*Poly*"} | ft status, FriendlyName, InstanceID'

- 'get-pnpdevice  | Where-Object {$_.Class -like "*AudioEndpoint*"} | ft status, FriendlyName, InstanceID'


okay from the list
to remove it
- 'pnputil /remove-device 'enter InstanceID HERE''

or you can create this via powershell
this command will capture all unknown device as AudioEndpoint
- '$unknown = get-pnpdevice -Class AudioEndpoint | Where-Object {$_.Status -eq "Unknown"} | ft status, FriendlyName, InstanceID, Class'

to save it in txt file
type in
$unknown >> 1.txt

to remove it
type in

- 'pnputil /remove-device "SWD\MMDEVAPI\{0.0.0.00000000}.{D7350DC7-645C-4E5A-85CF-9E9D19C822EA}"'

### If you are getting this error message below, when finishing up the MTR Setup Wizard.
#### "insert room console into the dock"
<img width="1024" alt="mssrs" src="https://github.com/nucpc/info/blob/main/mssrs.jpg?raw=true">


More details click [HERE](https://support.hp.com/us-en/document/c06155011) under Troubleshooting search for `"Can't complete MS SRS Setup".`

That's usually means you need to have a HDMI/Display Port connected to the Ingest/Input source.
but if you are helping to configure the unit, workaround is to create a custom XML setting.

````
<SkypeSettings>
<UserAccount>
    <SkypeSignInAddress>test@test.com</SkypeSignInAddress>
    <ExchangeAddress>test@test.com</ExchangeAddress>
    <Password>test</Password>
</UserAccount>
</SkypeSettings>
````

Save it as 
`skypesettings.xml`   
copy it to MTR unit under the folder called `C:\Users\Skype\AppData\Local\Packages\Microsoft.SkypeRoomSystem_8wekyb3d8bbwe\LocalState`

Restart the device.


### ***_MTR Scripts files from re-install USB by Microsoft_***
```
srs.partition
srs-restore.cmd
restore_.swm
```

srs.partition
-
```
SELECT DISK 1
CLEAN
CONVERT GPT
CREATE PARTITION EFI SIZE=300
FORMAT FS=FAT32 QUICK
ASSIGN LETTER=Z
CREATE part PRIMARY
FORMAT FS=NTFS QUICK
ASSIGN LETTER=C
```

srs-restore.cmd
-
```
@ECHO OFF
ECHO Please wait.

diskpart /s %~dp0srs.partition >NUL

dism /Quiet /Apply-Image /ApplyDir:c:\ /Index:1 /ImageFile:Y:\restore_.swm /SWMFile:Y:\restore_*.swm
bcdboot c:\Windows /c >NUL
wpeutil reboot
```

#

### Here's how you can use FFmpeg to convert your .mov file to an .mp4 file that's optimized for PowerPoint without losing quality:
```
1. **Install FFmpeg**: If you haven't already, download and install FFmpeg on your computer.

2. **Open Command Prompt**: Open the command prompt on your computer.

3. **Navigate to the Directory**: Navigate to the directory where your .mov file is located.

4. **Run the FFmpeg Command**: Run the following command in the command prompt:
```
``` terminal command:
ffmpeg -i input_filename.mov -c:v libx264 -preset slow -profile:v high -level:v 4.0 -pix_fmt yuv420p -crf 22 -codec:a aac output_filename.mp4
```


#### In this command:
- `input_filename.mov` is the name of your .mov file.
- `output_filename.mp4` is the name you want for your converted .mp4 file.
- `-c:v libx264` sets the video codec to H.264, which is recommended for PowerPoint.
- `-preset slow` sets the encoding speed to slow, which provides a balance between encoding speed and video quality.
- `-profile:v high -level:v 4.0` sets the H.264 profile to high and the level to 4.0.
- `-pix_fmt yuv420p` sets the pixel format to YUV 4:2:0, which is widely supported.
- `-crf 22` sets the Constant Rate Factor to 22, which is a good balance between quality and file size.
- `-codec:a aac` sets the audio codec to AAC, which is recommended for PowerPoint.

#### This command should convert your .mov file to an .mp4 file that's optimized for PowerPoint without losing quality.
### 'Source: '
[(1) Convert Videos with FFMPEG to PowerPoint 2016 compatible video format.](https://stackoverflow.com/questions/44130350/convert-videos-with-ffmpeg-to-powerpoint-2016-compatible-video-format)

[(2) ffmpeg - Converting MOV files to MP4 - Stack Overflow.](https://stackoverflow.com/questions/12026381/ffmpeg-converting-mov-files-to-mp4)

[(3) [Step-by-Step] How to Convert MOV to MP4 with FFmpeg?](https://www.videoconverterfactory.com/tips/ffmpeg-mov-to-mp4.html)

[(4) ffmpeg convert mov to mp4 without reduction of bit rate. ](https://stackoverflow.com/questions/66248307/ffmpeg-convert-mov-to-mp4-without-reduction-of-bit-rate)



#### Google Chrome - allow updates
```
reg add "HKLM\SOFTWARE\Policies\Google\Update" /v "AutoUpdateCheckPeriodMinutes" /t REG_DWORD /d 1 /f
reg add "HKLM\SOFTWARE\Policies\Google\Update" /v "Install{8A69D345-D564-463C-AFF1-A69D9E530F96}" /t REG_DWORD /d 1 /f
reg add "HKLM\SOFTWARE\Policies\Google\Update" /v "Update{8A69D345-D564-463C-AFF1-A69D9E530F96}" /t REG_DWORD /d 1 /f
```
