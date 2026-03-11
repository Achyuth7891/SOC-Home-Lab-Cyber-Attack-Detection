<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">



</head>

<body>

<div class="container">

<h1>SOC Home Lab – Cyber Attack Detection</h1>

<p>
A practical <b>Security Operations Center (SOC) home lab</b> built to simulate real-world cyber attacks and investigate security events.
The lab uses <b>Kali Linux as an attacker machine</b> and a <b>Windows host system as the target</b>, allowing analysis of attack activity through system logs and network scans.
</p>

<p>
This project demonstrates how <b>SOC analysts detect suspicious activity</b> through log monitoring and network reconnaissance analysis.
</p>

<h2>Lab Architecture</h2>

<div class="architecture">

Kali Linux (Attacker VM) <br><br>
↓ <br><br>
Network Reconnaissance (Nmap) <br><br>
↓ <br><br>
Windows Host Machine (Target) <br><br>
↓ <br><br>
Windows Security Event Logs <br><br>
↓ <br><br>
Security Monitoring & Investigation

</div>

<h2>Tools Used</h2>

<table>

<tr>
<th>Tool</th>
<th>Purpose</th>
</tr>

<tr>
<td>Kali Linux</td>
<td>Attacker machine used to perform reconnaissance</td>
</tr>

<tr>
<td>Nmap</td>
<td>Network scanning and port discovery</td>
</tr>

<tr>
<td>Windows Event Viewer</td>
<td>Monitoring Windows security logs</td>
</tr>

<tr>
<td>VirtualBox</td>
<td>Creating a virtual cybersecurity lab environment</td>
</tr>

<tr>
<td>Splunk (Optional)</td>
<td>Security Information and Event Management (SIEM) platform</td>
</tr>

</table>

<h2>Attack Scenario</h2>

<p>
The attacker machine performs <b>network reconnaissance</b> on the target Windows system using <b>Nmap</b>.
</p>

<p>The goal is to identify:</p>

<ul>

<li>Open ports</li>
<li>Running services</li>
<li>Network distance</li>
<li>Operating system fingerprint</li>

</ul>

<h2>Commands Used</h2>

<p>Basic SYN scan:</p>

<code>
nmap -sS &lt;target-ip&gt;
</code>

<p>Aggressive scan:</p>

<code>
nmap -A &lt;target-ip&gt;
</code>

<h2>Network Scan Results</h2>

<p>The attacker discovers open ports and services on the target system.</p>

<ul>

<li>Open ports</li>
<li>Service detection</li>
<li>Host availability</li>

</ul>

<img src="screenshots/nmap_scan.png" alt="Nmap Scan Result">

<h2>Operating System Detection</h2>

<p>
Using aggressive scanning techniques, Nmap attempts to identify the operating system and services running on the target host.
</p>

<img src="screenshots/nmap_os_detection.png" alt="OS Detection">

<h2>Failed Login Detection</h2>

<p>
Windows records failed authentication attempts in the <b>Security Log</b>.
</p>

<p><b>Event ID:</b> 4625</p>

<p><b>Meaning:</b> An account failed to log on</p>

<p>Security analysts monitor this event to detect:</p>

<ul>

<li>Brute force attacks</li>
<li>Unauthorized login attempts</li>
<li>Credential abuse</li>

</ul>

<h2>Security Log Investigation</h2>

<p>Example failed login event recorded in Windows Event Viewer.</p>

<img src="screenshots/failed_login_event.png" alt="Windows Failed Login Event">

<p><b>Key fields analyzed:</b></p>

<ul>

<li>Logon Type</li>
<li>Account Name</li>
<li>Failure Reason</li>
<li>Source IP Address</li>

</ul>

<p>
These logs help SOC analysts <b>identify suspicious login patterns</b>.
</p>

<h2>SOC Investigation Workflow</h2>

<ol>

<li><b>Reconnaissance Detection</b> – Identify suspicious network scanning activity</li>

<li><b>Log Analysis</b> – Investigate authentication events in Windows Security logs</li>

<li><b>Threat Identification</b> – Determine whether activity is malicious</li>

<li><b>Incident Documentation</b> – Record evidence and findings</li>

</ol>

<h2>Skills Demonstrated</h2>

<ul>

<li>Network reconnaissance analysis</li>
<li>Port scanning investigation</li>
<li>Windows security log analysis</li>
<li>Cyber attack simulation</li>
<li>SOC monitoring fundamentals</li>
<li>Incident investigation workflow</li>

</ul>

<h2>Learning Outcomes</h2>

<ul>

<li>Understanding network scanning techniques</li>
<li>Analyzing reconnaissance phase of cyber attacks</li>
<li>Monitoring Windows authentication failures</li>
<li>Performing basic SOC investigations</li>

</ul>

<h2>Future Improvements</h2>

<ul>

<li>Integrating Splunk SIEM for centralized log monitoring</li>
<li>Adding Wireshark packet analysis</li>
<li>Creating automated alert rules for brute force detection</li>
<li>Implementing threat detection dashboards</li>

</ul>

<div class="footer">

<b>Author</b><br>
Geerla Achyutha<br>
Cybersecurity Enthusiast<br>
GitHub: https://github.com/Achyuth7891

</div>

</div>

</body>
</html>
