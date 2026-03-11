<h1 align="center">SOC Home Lab – Cyber Attack Detection</h1>

<p align="center">
A practical <b>Security Operations Center (SOC) Home Lab</b> project demonstrating how cyber attacks can be simulated and investigated using security monitoring tools.
</p>

<hr>

<h2>Project Overview</h2>

<p>
This project demonstrates a simulated cyber attack scenario where an attacker machine (<b>Kali Linux</b>) performs reconnaissance and network scanning against a target Windows system.
</p>

<p>
The activity is then analyzed using:
</p>

<ul>
<li>Windows Security Logs</li>
<li>Splunk SIEM Dashboard</li>
<li>Network Packet Analysis using Wireshark</li>
</ul>

<p>
The goal of this lab is to understand how <b>Security Operations Center (SOC) analysts detect suspicious activities and investigate potential security incidents.</b>
</p>

<hr>

<h2>Lab Architecture</h2>

<pre>
Kali Linux (Attacker VM)
        |
        |  Network Reconnaissance (Nmap)
        |
Windows Host Machine (Target)
        |
        |  Security Event Logs
        |
Splunk SIEM Monitoring
        |
SOC Investigation
</pre>

<hr>

<h2>Tools Used</h2>

<table>
<tr>
<th>Tool</th>
<th>Purpose</th>
</tr>

<tr>
<td>Kali Linux</td>
<td>Attacker machine used to perform network reconnaissance</td>
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
<td>Splunk SIEM</td>
<td>Security monitoring and threat detection</td>
</tr>

<tr>
<td>Wireshark</td>
<td>Network traffic packet analysis</td>
</tr>

<tr>
<td>VirtualBox</td>
<td>Virtual lab environment</td>
</tr>

</table>

<hr>

<h2>Attack Simulation</h2>

<p>
The attacker machine performs network reconnaissance using <b>Nmap</b> to identify open ports and services on the target system.
</p>

<h3>Command Used</h3>

<pre>
nmap -sS &lt;target-ip&gt;
</pre>

<h3>Aggressive Scan</h3>

<pre>
nmap -A &lt;target-ip&gt;
</pre>

<p>
These scans help attackers discover:
</p>

<ul>
<li>Open ports</li>
<li>Running services</li>
<li>Operating system information</li>
<li>Network distance</li>
</ul>

<hr>

<h2>Network Scan Result</h2>

<p>The attacker discovers open ports and services running on the target system.</p>

<img src="screenshots/Namp_Scan.jpg" width="800">

<p><b>Key Findings</b></p>

<ul>
<li>Open TCP ports detected</li>
<li>Service versions identified</li>
<li>Operating system fingerprinting</li>
</ul>

<hr>

<h2>Windows Security Log Analysis</h2>

<p>
Windows records failed authentication attempts in the <b>Security Event Log</b>.
</p>

<p><b>Event ID:</b> 4625</p>

<p><b>Description:</b> An account failed to log on</p>

<img src="screenshots/Windows_Event_Viewer_Logs.jpg" width="800">

<p>
SOC analysts monitor this event to detect potential security threats such as:
</p>

<ul>
<li>Brute force login attacks</li>
<li>Unauthorized login attempts</li>
<li>Credential abuse</li>
</ul>

<hr>

<h2>Splunk SIEM Monitoring</h2>

<p>
Splunk is used to collect and analyze security logs from the system.
</p>

<p>The dashboard visualizes authentication failures and suspicious activity.</p>

<img src="screenshots/Splunk_Dashboard_Logs.jpg" width="800">

<p>
SOC analysts use this dashboard to identify attack patterns and monitor system security.
</p>

<hr>

<h2>Splunk Alert Rule</h2>

<p>
An alert rule was configured in Splunk to detect excessive Nmap scanning activity.
</p>

<img src="screenshots/Splunk_Alert_Rule.jpg" width="800">

<p>
The alert triggers when multiple scanning attempts are detected from a single source IP address.
</p>

<hr>

<h2>Network Traffic Analysis</h2>

<p>
Wireshark was used to capture and analyze network packets generated during the scanning activity.
</p>

<img src="screenshots/WireShark_Traffic_Capture.jpg" width="800">

<p>
Packet analysis allows SOC analysts to understand the communication between the attacker and target machine.
</p>

<hr>

<h2>SOC Investigation Workflow</h2>

<ol>

<li><b>Reconnaissance Detection</b> – Identify suspicious network scanning activity</li>

<li><b>Log Analysis</b> – Investigate authentication failures in Windows logs</li>

<li><b>Threat Identification</b> – Determine whether activity is malicious</li>

<li><b>Incident Documentation</b> – Record evidence and findings</li>

</ol>

<hr>

<h2>Skills Demonstrated</h2>

<ul>

<li>Network reconnaissance analysis</li>
<li>Port scanning investigation</li>
<li>Windows security log analysis</li>
<li>SIEM monitoring using Splunk</li>
<li>Network packet analysis with Wireshark</li>
<li>Cyber attack simulation</li>

</ul>

<hr>

<h2>Learning Outcomes</h2>

<ul>

<li>Understanding reconnaissance phase of cyber attacks</li>
<li>Investigating authentication failure logs</li>
<li>Monitoring security events using SIEM tools</li>
<li>Analyzing network packets for suspicious activity</li>

</ul>

<hr>

<h2>Future Improvements</h2>

<ul>

<li>Automated brute force detection rules</li>
<li>Integration with threat intelligence feeds</li>
<li>Real-time SIEM alert notifications</li>
<li>Advanced anomaly detection dashboards</li>

</ul>

<hr>

<h2>Author</h2>

<p>
<b>Geerla Achyutha</b><br>
Cybersecurity Enthusiast<br>
GitHub: https://github.com/Achyuth7891
</p>
