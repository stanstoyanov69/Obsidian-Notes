
Wazuh's security event monitor is capable to actively record both successful and unsuccessful authentication attempts. The rule with an id of 5710 detects attempted connections that are unsuccessful for the SSH protocol. Let's look at this animated picture below as an example.![[17572a8abaac35f9e281c54a8b861836.gif]]


The alert was created because someone tried to log onto the agent "**ip-10-10-73- 118**" with the user "**cmnatic**" which does not exist. I have summarized this alert into the table below:

|   |   |   |
|---|---|---|
|**Field**|**Value**|**Description**|
|agent.ip|10.10.73.118|This is the IP address of the agent that the alert was triggered on.|
|agent.name|ip-10-10-73-118|This is the hostname of the agent that the alert was triggered on.|
|rule.description|sshd: Attempt to login using a non-existent user|This field is a brief description of what the event is alerting to.|
|rule.mitre.technique|Brute-Force|This field explains the MITRE technique that the alert pertains to.|
|rule.mitre.id|T1110|This field is the MITRE ID of the alert|
|rule.id|5710|This field is the ID assigned to the alert by Wazuh's ruleset|
|location|/var/log/auth.log|This field is the location of the file that the alert was generated from on the agent. In this example, it is the authentication log on the linux agent.|
For reference, this alert is stored in a specific file on the Wazuh management server: `/var/ossec/logs/alerts/alerts.log`. We can use a command such as grep or nano to search through this file on the management server manually.