
<!---
Version: 1.0 
-->
# Take a tour of Kali
## INTRODUCTION MESSAGE
In this exercise, you will familiarize yourself with Kali User Interface and review some of the basic functionality of a default configuration of a Kali.
## COMPLETION MESSAGE
You have just completed a brief tour of Kali. In the next exercise, you will llearn how to change the Kali's MAC address.
### Log in to Kali
On the Kali log in screen, in Username, type **root,** and click **Next**. In password, type **Passw0rd!**, and click **Sign In**.

#### :warning: ALERT
As with any Linux-based system, all names are case sensitive. Please ensure, you enter **root** as lowercase letters.

#### :bulb: KNOWLEDGE
TIP: You can paste the username and password from the Commands menu in the lab UI. To do so, click **Commands**, and the click**Paste**.





### Examine toolbar
On the top right of the desktop, click the drop-down icon.  The drop-down box contains network, audio, and user information. Additionally, from here you can access the system settings, lock screen, and power control.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/765139.png
>* ShowAutomatically = Always





### Examine recording settings
To the left of the drop-down group, click the camera icon. Here you can configure and start recordings of activities you perform on the desktop.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/765140.png
>* ShowAutomatically = Always





### Examine workspace
To the left of the camera, click the workspace icon \)number in box).  You use workspaces to organize your programs and applications. You will always have at least one blank workspace that does not have any open applications.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/765141.png
>* ShowAutomatically = Always





### Examine favorites bar
On the left side of the screen, note the customizable favorites bar. The favorites bar groups commonly used tools for easy access. Hover the mouse over each of the applications shown in the favorites bar.

#### :bulb: KNOWLEDGE
NOTE: These, and other applications, are installed by default when you install Kali 2.0.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/763483.png





### Open Iceweasel
On the top of the favorites bar, double-click **Iceweasel**\)top application on favorites bar).  A re-branded version of Mozilla Extended Support Release \)ESR) appears.

#### :bulb: KNOWLEDGE
IceWweasel is a re-branded version of Mozilla Firefox ESR. For more information on the Iceweasel branding, please see [https://wiki.debian.org/Iceweasel](https://wiki.debian.org/Iceweasel). In the most recent version of Kali, the Iceweasel branding is replaced by the Mozilla branding.





### Change to Workspace 2
On the toolbar, click the workspace icon, and then click **Workspace 2**. Note that Iceweasel disappears from view. However, note the grey dot to the left of the Iceweasel icon to indicate that the application is open in another workspace. 





### Open Terminal
On the favorites bar, double-click **Terminal**.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/765143.png





### Close Terminal
Close the Terminal application.





### Change to Workspace 1
On the top right toolbar, click the workspace icon, and change to **Workspace 1**.





### Close Iceweasel
Close the Iceweasel browser.





### Show all applications
On the favorites bar, click **Show Applications** \)bottom icon). On the applications page, ensure that All is selected, as shown in the attached screenshot.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/765159.png





### Search for application
In the search box, type **Wireshark**.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/765169.png





### Cancel search
On the right of the search dialog box, click the **X** to close the search dialog box.





### Review Applications
On the left side of the toolbar, click **Applications**. The applications installed by default on Kali are displayed, organized by their functional category. Spend a few moments examining the application in their respective categories.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/765147.png





### Review Places
On the Toolbar, click **Places**. This provides you with quick access to frequently used places.






# Use Zenmap and Nmap to scan ports
## INTRODUCTION MESSAGE
Port scanning is used discover open ports on remote systems. Port scanning is useful for network discovery, security auditing, host monitoring and network administratiion functions. Although port scanning itself is benign and has many legitimate, unexpected or unauthorized port scans are  often viewed as  attacks because they are often used to discover vulnerabilites in preparation for an actual attack.   
  
By default, Kali includes a number of port scanners. The most popular and widely used port scanner and network discovery tool included in Kali is Namp.  
  
**IMPORTANT:** Using the more aggressive capabilities of Nmap without proper authorization and prior agreement could be evidence of a criminal activity. Please ensure you obtain proper authorization before using any tool in Kali that could potentially lead to unauthorized access of a computer system, which is a criminal offense.
## COMPLETION MESSAGE

### Open Zenmap
On the favorites bar, click **Show Applications**. In the Search box, type **Zenmap**, and press **ENTER**. Zenmap opens.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/765198.png
>* ShowAutomatically = No





### View available scan profiles
In Zenmap, click the down arrow to the right of the Profile field to show the available port scan profiles. Select a scan profile, and note that the Nmap command for the scan profile is displayed in the command field.

#### :bulb: KNOWLEDGE
**NOTE:** The various scan profiles allow you to select from a range of scan types from a simple ping scan to  more comprehensive scans.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/765209.png





### Configure scan target
In the Target field, type **192.168.1.0/24**.

#### :bulb: KNOWLEDGE
**NOTE:** In the target field you are configuring Zenmap to scan that entire subnet described by the 24-bit subnet mask \)255.255.255.0). If you want to scan for a single host, you can specify its IP address without providing the mask \)/n).





### Select scan profile
In the Profile field, select **Ping scan**.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/765218.png





### Scan subnet
In Zenmap, click **Scan**. After a few moments, the scan output is displayed in the Nmap Output tab.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/765219.png





### Perform a Quick scan plus
In Profile, select **Quick scan plus**. In target, type **192.168.1.3**. Click **Scan**. After 30 - 45 seconds, the scan results appear, as shown in the attached screen shot.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/765221.png





### View host details
In the left pane, click **192.168.1.3**, and then click the **Host Details** tab.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/765239.png





### View scan history
Click the Scans tab. The Scans tab saves details of previously run scans. These scans can be saved upon exiting the application.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/765242.png





### Close Zenmap
Close Zenmap.





### Open Terminal
On the favorites bar, click **Terminal**.





### Perform a ping scan of subnet
At the terminal prompt, type **nmap -sn 192.168.1.0/24**, and press **ENTER**.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/765250.png





### Perform an intense scan of host
At the terminal prompt, type **nmap -T4 -A -v 192.168.1.3**, and press **ENTER**. The scan will take a few minutes to complete.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/765252.png





### Close Terminal
Close Terminal.






# Use Macchanger to change MAC address
## INTRODUCTION MESSAGE
When performing penetration testing, it is often desireable to change the MAC address of the Kali host. The reasons for changing the MAC will vary according to the situation. For example, you may need to hide the permanent MAC address or spoof a MAC address of another host on the netwwork.  
  
In this exercise, you will learn how to use the Macchanger application to temporarily change the MAC address.
## COMPLETION MESSAGE
Congratulations, you have successfully used Macchanger to change the MAC address of the host.
### Open Macchanger
On the favorites bar, click **Show Applications**. In the Search box, type **Macchanger**, and press**ENTER**. The terminal window opens with the Macchanger help menu displayed.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/765154.png
>* ShowAutomatically = No





### View current MAC address
At the terminal prompt, type i**fconfig**, and press **ENTER**.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/765192.png





### Turn off network interface
At the terminal prompt, type **ifconfig eth0 down**, and press **ENTER**.

#### :bulb: KNOWLEDGE
**NOTE:** You need to turn off the network adapter to change the MAC address.





### Change MAC address
At the terminal prompt, type **macchanger -m A0:8C:FD:BE:07:D1 eth0**, and press **ENTER**.

#### :bulb: KNOWLEDGE
NOTE: You can change the MAC address back to its original value by using the command **macchanger -p**.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/765193.png





### Turn on network interface
At the terminal prompt, type **ifconfig eth0 up**, and press **ENTER**.





### View available scan profiles
In Zenmap, click the Profile field to show the available port scan profiles.

#### :bulb: KNOWLEDGE
**NOTE:** The various scan profiles allow you to select from a range of scan types from a simple ping scan to more comprehensive scans.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/765208.png





### View current MAC address
At the terminal prompt, type **ifconfig** and press **ENTER**. The output displays the new MAC address.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/765196.png





### Close Terminal
Close the Terminal application






