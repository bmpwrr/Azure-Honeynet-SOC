# Azure-Honeynet-SOC
Introduction & Objective
- 
In this project, we set up a small security network on the Azure platform. The goal was to collect and study logs from different sources, which were then brought together in a central workspace called Log Analytics. We used a tool called Microsoft Sentinel to make use of these logs. It helped us create visual maps of potential attacks, set up alerts for suspicious activities, and generate reports on any incidents. For a full day, we kept an eye on the security of this environment. After that, we added extra layers of protection to make it even more secure. Then, we monitored it again for another day to see how effective these changes were.

Here are the things we looked at:

- SecurityEvent (These are logs from Windows systems)
- Syslog (These are logs from Linux systems)
- SecurityAlert (These are alerts that were triggered in Log Analytics)
- SecurityIncident (These are incidents that were identified by Sentinel)
- AzureNetworkAnalytics (These are records of suspicious activities that were allowed into our security network)

Technologies, Azure Components, and Regulations Employed
- 
- Virtual Network (VNet)
- Network Security Group (NSG)
- Virtual Machines (2 windows, 1 linux)
- Log Analytics Workspace for performing Kusto Query (KQL) queries to filters data
- Azure Key Vault to securely store secrets
- Azure Storage Account for storing data
- Microsoft Sentinel for Security Information and Event Management (SIEM)
- Microsoft Defender for Cloud to monitor resources and ingest logs from virtual machines into Log Analytic Workspace
- Powershell for performing simulated attacks
- Command Line Interface (CLI) to verify connection to virtual machine
- Windows Remote Desktop to remotely connect to virtual machines
- NIST SP 800-53 Revision 4 for Security Controls
- NIST SP 800-61 Revision 2 for Incident Handling Guidance

Architecture Before Hardening
- 
![before_harden](https://github.com/bmpwrr/Azure-Honeynet-SOC/assets/144153997/eed9e200-2ea2-4f6f-bced-c5e7d410e4e3)

Architecture After Hardening
- 
![after_harden](https://github.com/bmpwrr/Azure-Honeynet-SOC/assets/144153997/69c516ad-686a-472e-b85e-540748a48c5f)

Attack Maps Before Hardening
- 
This attack map shows the traffic allowed by a Network Security Group with all traffic allowed inbound
![nsg](https://github.com/bmpwrr/Azure-Honeynet-SOC/assets/144153997/81a1ae00-4814-4a0d-b122-b2fa9cded590)

This attack map shows all the attempts that the threat actors tries to access the Linux virtual machine
![linux](https://github.com/bmpwrr/Azure-Honeynet-SOC/assets/144153997/c20fb8c0-79e9-4a6b-9084-6a2fe400e08c)

This attach map shows all the attempts that the threat actors tries to get into the Windows Virtual Machine
![mssql](https://github.com/bmpwrr/Azure-Honeynet-SOC/assets/144153997/8cbef024-55d7-40af-8133-9208d0c885bc)

Metrics Before Hardening
-
![metric_before](https://github.com/bmpwrr/Azure-Honeynet-SOC/assets/144153997/72661f42-0917-480b-895f-ddc407f5cc21)

Metric After Hardening
-
![metric_after](https://github.com/bmpwrr/Azure-Honeynet-SOC/assets/144153997/95b15faf-1407-496e-a37b-39441aa59b4e)

Conclusion
- 
In this project, we set up a small yet powerful security network in Microsoft Azure. We collected logs from various sources and organized them in a central space called Log Analytics. We also set up Microsoft Sentinel to notify us and generate incident reports based on these logs.

We initially measured the performance in the unprotected environment. Then, we enhanced security measures. After implementing these measures, we observed significant improvements: a 34% decrease in Windows Security Events, a 77% decrease in Linux Events, and a 54% decrease in security alerts, incidents, and suspicious inbound network activity. This indicates that the added security measures were highly effective.













