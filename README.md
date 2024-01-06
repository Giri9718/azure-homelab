# Microsoft Azure Homelab
<h1>Mapping Failed Logon RDP to Geolocation</h1>





<h2>Description</h2>
<b>The Powershell script in this repository is responsible for parsing out Windows Event Log information for failed RDP attacks and using a third-party API to collect geographic information about the attackers' geo location.
</b>
<br />
<br />
KQL is used for scipting purpose and script is used in this demo where I set up Azure Sentinel (SIEM) and connect it to a live virtual machine acting as a honey pot.
We will observe live attacks (RDP Brute Force) from all around the world. For the very purpose I use a custom PowerShell script to
Look up the attackers' Geolocation information and plot it on an Azure Sentinel Map. The script also icludes the time ,hostname, user ids etc used by the attackers.
For failed logon we extract data from windows event viewer corresponding to port 4625. In future I will integrate successful logons also in to this lab by exctracting info from port 4624.
<br />
<br />

<p align="center">
<img src="https://i.imgur.com/TmEMcM5.jpg"(https://imgur.com/TmEMcM5)" height="85%" width="85%" alt="RDP event fail logs to iP Geographic information"/>
</p>
<h2>Languages Used</h2>

- <b>PowerShell:</b> Extract RDP failed logon logs from Windows Event Viewer 

<h2>Third Party site used</h2>

- <b>ipgeolocation.io:</b> IP Address to Geolocation API

<h2>Attacks from China coming in; Custom logs being output with geodata</h2>

<p align="center">
<img src="https://i.imgur.com/2MViSiL.jpg" (https://imgur.com/2MViSiL) height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<h2>World map of incoming attacks after 24 hours (built custom logs including geodata)</h2>

<p align="center">
<img src="https://i.imgur.com/krRFrK5.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
