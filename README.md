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
 














