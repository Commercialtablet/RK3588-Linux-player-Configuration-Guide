# RK3588-Linux-player-Configuration-Guide

This is the documentation for RK3588 Linux player Comfiguration Guide, written by Sales Team of HYY Technology Co.,Ltd.

## **1.0 Connection and startup**

Connect your screen to the HD Out1 port (Closest to the power plug) 

Then connect LAN and power connector. 

 

After starting up it will launch LoopSign demo page or Chrome error message if network is not 

connected.

***\*Press Alt+F4 to exit the kiosk browser to be able to configure the player\****

## **1.1 Configure localization (Optional)**

The Player is set up with English keyboard layout and TimeZone Central Europe 

Please note that the keyboard layout cannot be changed. 

 

To change timezone follow these steps:

\- Click on the “Arrow” in the upper right corner. 

\- Select “Settings”

\- Select “Date & Time” and set whatever settings you prefer.

## **1.2 Configure WIFI (Optional)**

If you need to connect to a WIFI network, 

 

\- Click on the “Arrow” in the upper right corner. 

\- Select “Settings”

\- Select “WI-FI” and connect to your preferred wireless network.

## **1.3** **Configure** **screen orientation or resolution (Optional)**

By default display runs in normal “landscape” mode 1080P 60Hz 

To change display settings, follow these steps:

 

\- Click on the “Arrow” in the upper right corner. 

\- Select “Settings”

\- Select “Displays” and set your preferred settings

 

# **2. LoopSign URL configuration**

To change the URL that is being played on the device you need to edit the file loopsign.desktop 

 

Start a Terminal window by selecting “Activities” in upper left corner and select 

“Terminal” icon that appears. (Last entry in favourites) 

![2](https://user-images.githubusercontent.com/126669652/223941655-bd1a5879-dc68-448f-b292-26f3bbc04fa9.png)

In the Terminal command windows, enter this command: 

***\*sudo nano /etc/xdg/autostart/loopsign.desktop\****

The editor will the show the following: 

[Desktop Entry]

Type=Application 

Exec = xhost +

Exec = bash -c "sleep 10 && chromium --kiosk "https://play.loopsign.eu/app/20/lsp" --disable- 

desktop-notifications --no-first-run --kiosk-printing"

 

\- Change the part of the URL shown in yellow to the corresponding URL for the screen you want the player to show. (Please note that it is English keyboard layout)

 

To save, press ‘Ctrl+O’ (WriteOut), then press ‘Enter’ when asked to confirm the filename. 

To exit, press ‘Ctrl+X’ (Exit). 

 

Write command ***sudo reboo*** to restart your player.

 

 

# **3. Known Issues**

## **3.1 Hang/Crash**

The player automatically reboots once every week. If you experience “hang” or “Crash” you will need 

to set reboot every day.

 

In the terminal window, write command: ***sudo crontab-e*** (Select to use Nano as editor) 

Add line in the end of the file (This will restart the player every day at 07:00.)

Or set whatever time you like it to reboot 

 

***\*00 7 \* \* \* /sbin/shutdown -r now\****

 

To save, press ‘Ctrl+O’ (WriteOut), then press ‘Enter’ when asked to confirm the filename. 

To exit, press ‘Ctrl+X’ (Exit). 

 

Write command ***sudo reboo*** to restart your player.

 

## **3.2 Automatic suspend messages**

If you experience these kinds of messages on the screen from time to time.

 
![3](https://user-images.githubusercontent.com/126669652/223941798-2e2c5efd-b87d-40ec-887f-1aaa0ee03b53.png)


 

It can be solved by turning off power notifications. 

Enter “Settings” and select Notifications.

 

![4](https://user-images.githubusercontent.com/126669652/223941865-5deb9186-0df8-4409-a80d-69290a459c5c.png)

 

Turn off notifications for power.


![5](https://user-images.githubusercontent.com/126669652/223941912-3a7152a4-a8a1-4cbd-b4de-f6a0d3684741.png)

 

## **3.3 Software Update messages**

If you experience OS update notifications and want to turn them off, select settings and 

Notifications. Then turn off notifications for software

 

![6](https://user-images.githubusercontent.com/126669652/223941964-060c1ef9-d081-48ff-bf69-e5ac73e85b0e.png)

# Contacts
- Website: www.we-signage.com
- https://we-signage.en.made-in-china.com/
- https://wesignage.en.alibaba.com/
- E-mail: sales3@we-signage.com
- MP/skype/Wechat: + 86 14715355256
- Whatsapp: +86 18025831950
