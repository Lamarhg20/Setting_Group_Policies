<h1>Setting_Group_Policies</h1>

<h2>Description</h2>
How to set group policies in windows active directory with win server 2019
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 

<h2>Environments Used </h2>

- <b>Windows server 2019</b> 

<h2>Setting a GPO:</h2>

<p align="center">
In order to create a new group policy from the tools menu, select group policy management: <br/>
<img src="https://i.imgur.com/oNxPucn.png"/>
<br />
<br />
Select the forest for your domain controller:  <br/>
<img src="https://i.imgur.com/tituHDQ.png" height="80%" width="80%" alt="Setting_Group_Policies"/>
<br />
<br />
Select the organizational unit you’d like to create the policy for: <br/>
<img src="https://i.imgur.com/iDb4vk3.png" height="80%" width="80%" alt="Setting_Group_Policies"/>
<br />
<br />
Right click your organizational unit and select "create a GPO in this domain and link it here":  <br/>
<img src="https://i.imgur.com/XZjtF0u.png" height="80%" width="80%" alt="Setting_Group_Policies"/>
<br />
<br />
Name your group policy object click OK and right click the object select edit:  <br/>
<img src="https://i.imgur.com/ABtElG4.png" height="80%" width="80%" alt="Setting_Group_Policies"/>
<br />
<br />
The policies are organized into user configurations. And computer configurations. Because we want to create a policy to limit access to control panel for specific users, we’re going to select user configurations-->administrative templates--> control panel:  <br/>
<img src="https://i.imgur.com/XfXkk67.png" height="80%" width="80%" alt="Setting_Group_Policies"/>
<br />
<br />
In that selection that we’re going to select prohibit access to control panel and PC settings:  <br/>
<img src="https://i.imgur.com/WOibtIw.png" height="80%" width="80%" alt="Setting_Group_Policies"/>
<br />
<br />
﻿﻿﻿Select "Enabled" and Click Apply. Control Panel and Setting will no longer be accessible to users in the OU that you selected <br/>

</p>

<h2>Other Group Policy Best Practices to Secure Small Organizations:</h2>

<br />
<b>Prevent Windows from Storing Hashes of Passwords:</b> <br/>
<br/>
"Computer Configuration"--> "Windows Settings"--> "Security Settings" -->"Local Policies"--> "Security Options".﻿﻿﻿ <br/>
In the right pane, double-click "Network security: Do not store LAN Manager hash value on next password change" policy.<br/>
Select "Define this policy setting" and click "Enabled.<br/>
Click "Apply" and "OK"
<br/>
<br/>
<b>Control Access to Command Prompt:</b><br/> 
<br/>
"User Configuration" "Windows Settings" "Policies" "Administrative Templates" "System".﻿﻿﻿<br/>
In the right pane, double-click "Prevent access to the command prompt" policy.<br/>
Click "Enabled" to apply the policy.﻿﻿﻿ <br/>
Click "Apply" and "OK"
<br/>
<br/>
<b>Disable Forced System Restarts:</b><br/> 
<br/>
"ComputerConfiguration" "Administrative Templates" "Windows Component" "Windows Update".﻿﻿﻿<br/>
In the right pane, double-click "No auto-restart with logged on users for scheduled automatic updates installations" policy.<br/>
Click "Enabled" to enable the policy.<br/>
Click "Apply" and "OK".
<br/>
<br/>
<b>Disallow Removable Media Drives to Prevent Introduction of Malware:</b> <br/>
<br/>
"User Configuration" "Policies" "Administrative Templates" "System" "Removable Storage Access".<br/>
In the right pane, double-click "All removable storage classes: Deny all accesses" policy﻿﻿﻿<br/>
Click "Enabled" to enable the policy.﻿﻿﻿<br/>
Click "Apply" and "OK".
<br/>
<br/>
<b>Restrict Unauthorized Software Installations:</b><br/>
<br/>
"Computer Configuration" "Administrative Templates" "Windows Component" "Windows Installer".<br/>
In the right pane, double-click "Prohibit User Install" policy.﻿﻿﻿<br/>
Click "Enabled" to enable the policy﻿﻿﻿<br/>
Click "Apply" and "OK".
<br/>
<br/>
<b>Disable Guest Account:</b><br/>
<br/>
"Computer Configuration" "Windows Settings" "Security Settings" "Local Policies" "Security Options"<br/>
In the right pane, double-click "Accounts: Guest Account Status" policy.<br/>
Select "Define this policy setting" and click "Disabled".<br/>
Click "Apply" and "OK".
<br/>
<br/>
<b>Set Minimum Password Length:</b><br/>
<br/>
"Computer Configuration" "Windows Settings" "Security Settings" "Account Policies" "Password Policy".<br/>
In the right pane, double-click "Minimum password length" policy<br/> 
select "Define this policy setting" ﻿﻿﻿Specity a length for the password<br/>
Click "Apply" and "OK".
<br/>
<br/>
<b>Set How Frequently Password Must Be Changed:</b><br/>
<br/>
"Computer Configuration""Windows Settings" "Security Settings" "Account Policies" "Password Policy".﻿﻿<br/>
In the right pane, double-click "Maximum password age" policy.<br/>
Select "Define this policy setting" and Type how long in days.<br/>
Click "Apply" and "OK".
<br/>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
