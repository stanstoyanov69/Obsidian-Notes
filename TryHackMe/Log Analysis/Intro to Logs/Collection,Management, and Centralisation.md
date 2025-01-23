Log Collection

Log collection is an essential component of log analysis, involving the aggregation of logs from diverse sources such as servers, network devices, software, and databases.

For logs to effectively represent a chronological sequence of events, it's crucial to maintain the system's time accuracy during logging. Utilising the **Network Time Protocol (NTP)** is a method to achieve this synchronisation and ensure the integrity of the timeline stored in the logs.

As this is a foundational step to ensuring that a security analyst would have a comprehensive data set to review, the following is a simple step-by-step process to achieving this, bearing in mind the need to prioritise the collection based on significant information:

- **Identify Sources:** List all potential log sources, such as servers, databases, applications, and network devices.
- **Choose a Log Collector:** Opt for a suitable log collector tool or software that aligns with your infrastructure.
- **Configure Collection Parameters:** Ensure that time synchronisation is enabled through NTP to maintain accurate timelines, adjust settings to determine which events to log at what intervals, and prioritise based on importance.
- **Test Collection:** Once configured, run a test to ensure logs are appropriately collected from all sources.

**IMPORTANT:** Please be aware that NTP-based time synchronisation may not be possible to replicate with the VM since it has no internet connectivity. However, when performing this in practice, using **pool.ntp.org** to find an NTP server is best. Time synchronisation can be performed automatically on Linux-based systems or manually initiated by executing. `ntpdate pool.ntp.org`.

Example of Time Synchronisation with NTP on a Linux-based System

```shell-session
root@WEBSRV-02:~# ntpdate pool.ntp.org
12 Aug 21:03:44 ntpdate[2399365]: adjust time server 85.91.1.180 offset 0.000060 sec
root@WEBSRV-02:~# date
Saturday, 12 August, 2023 09:04:55 PM UTC
root@WEBSRV-02:~#
```

  

Log Management

Efficient Log Management ensures that every gathered log is stored securely, organised systematically, and is ready for swift retrieval. A hybrid approach can provide a balanced solution by hoarding all log files and selectively trimming.

Once you've collated your logs, effective management of them is paramount. These steps can be followed to achieve this:

- **Storage:** Decide on a secure storage solution, considering factors like retention period and accessibility.
- **Organisation:** Classify logs based on their source, type, or other criteria for easier access later.
- **Backup:** Regularly back up your logs to prevent data loss.
- **Review:** Periodically review logs to ensure they are correctly stored and categorised.

Log Centralisation

Centralisation is pivotal for swift log access, in-depth analysis, and rapid incident response. A unified system allows for efficient log management with tools that offer real-time detection, automatic notifications, and seamless integration with incident management systems.

Centralising your logs can significantly streamline access and analysis. Here's a simple process for achieving it:

- **Choose a Centralised System:** Opt for a system that consolidates logs from all sources, such as the Elastic Stack or Splunk.
- **Integrate Sources:** Connect all your log sources to this centralised system.
- **Set Up Monitoring:** Utilise tools that provide real-time monitoring and alerts for specified events.
- **Integration with Incident Management:** Ensure that your centralised system can integrate seamlessly with any incident management tools or protocols you have in place.

Practical Activity: Log Collection with rsyslog

This activity aims to introduce `rsyslog` and demonstrate how it can enhance the centralisation and management of logs. As part of the collection process, we will configure `rsyslog` to log all sshd messages to a specific file, such as `/var/log/websrv-02/rsyslog_sshd.log`. The steps below can be followed to achieve this:

1. **Open a Terminal.**
2. **Ensure rsyslog is Installed:** You can check if rsyslog is installed by running the command: `sudo systemctl status rsyslog`
3. **Create a Configuration File:** Use a text editor to create the following configuration file: `gedit /etc/rsyslog.d/98-websrv-02-sshd.conf`, `nano /etc/rsyslog.d/98-websrv-02-sshd.conf`, `vi /etc/rsyslog.d/98-websrv-02-sshd.conf`, or `vim /etc/rsyslog.d/98-websrv-02-sshd.conf`
4. **Add the Configuration:** Add the following lines in `/etc/rsyslog.d/98-websrv-02-sshd.conf` to direct the sshd messages to the specific log file:
    
    ```yaml
    $FileCreateMode 0644
    :programname, isequal, "sshd" /var/log/websrv-02/rsyslog_sshd.log
    ```
    
5. **Save and Close the Configuration File.**
6. **Restart rsyslog:** Apply the changes by restarting rsyslog with the command: `sudo systemctl restart rsyslog`
7. **Verify the Configuration:** You can verify the configuration works by initiating an SSH connection to localhost via `ssh localhost` or by checking the log file after a minute or two.

![Expected Output after rsyslog configuration to monitor sshd](https://tryhackme-images.s3.amazonaws.com/user-uploads/63da722f2d207d0049da10b1/room-content/541d9cd9d9bc4487ee7f6cbd2390f406.png)