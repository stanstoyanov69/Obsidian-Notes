In the Heart of Data: Logs

Just as a physical tree's rings reveal its life story – indicating good years with thick curls and challenging ones with thin – a digital log provides a historical record of system activity.

Both embody a fundamental principle of growth over time and serve as living records in their respective domains – physical and digital.

In the digital world, every interaction with a computer system – from authentication attempts, granting authorisation, accessing a file, and connecting to a network to encountering a system error – will always leave a digital footprint in the form of logs.

|   |   |
|---|---|
|![Components of a digital log](https://tryhackme-images.s3.amazonaws.com/user-uploads/63da722f2d207d0049da10b1/room-content/624b4e33606f8b0e1dc2ff887eb70c3f.svg)|Logs are a record of events within a system. These records provide a detailed account of what a system has been doing, capturing a wide range of events such as user logins, file accesses, system errors, network connections, and changes to data or system configurations.<br><br>While the specific details may differ based on the type of log, a log entry usually includes the following information:<br><br>- A timestamp of when an event was logged<br>- The name of the system or application that generated the log entry<br>- The type of event that occurred<br>- Additional details about the event, such as the user who initiated the event or the device's IP address that generated the event<br><br>This information is typically stored in a **log file**, which contains aggregated entries of what occurred at any given time on a system.|

However, since digital interactions are continuous and fast-paced, the log file's size may exponentially grow depending on the activities logged on a system.

The True Power of Logs: Contextual Correlation

A single log entry may seem insignificant on its own. But when log data is aggregated, analysed, and cross-referenced with other sources of information, it becomes a potent investigation tool. Logs can answer critical questions about an event, such as:

- **What** happened?
- **When** did it happen?
- **Where** did it happen?
- **Who** is responsible?
- **Were** their actions **successful**?
- **What** was the result of their action?

The following hypothetical scenario can illustrate this aspect. Suppose a student allegedly accessed inappropriate content on a University network. By reviewing the logs, a systems administrator could then answer the following:

|Question|Answer|
|---|---|
|What happened?|An adversary was confirmed to have accessed SwiftSpend Financial's GitLab instance.|
|When did it happen?|Access started at 22:10 on Wednesday, September 8th, 2023.|
|Where did it happen?|The event originated from a device with an IP address of 10.10.133.168 within the VPN Users' segment (10.10.133.0/24).|
|Who is responsible?|Upon examining the network logs, it was observed that the device, identified by the User-Agent "Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0", was allocated the IP address 10.10.133.168.|
|Were they successful?|Yes, since an API Key was found to be publicly exposed on the GitLab instance. Moreover, the web proxy logs confirm that the adversary device reached _gitlab.swiftspend.finance_ and maintained access through their uploaded web shell.|
|What is the result of their action?|The adversary achieved remote code execution on _gitlab.swiftspend.finance_ and performed post-exploitation activities.|

The example above emphasises how logs are instrumental in piecing together a complete picture of an event, thereby enhancing our understanding and ability to respond effectively.


