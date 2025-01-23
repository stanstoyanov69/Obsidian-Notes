Log Storage

Logs can be stored in various locations, such as the local system that generates them, a centralised repository, or cloud-based storage.

The choice of storage location typically depends on multiple factors:

|   |   |
|---|---|
|![All Green Operational Server](https://tryhackme-images.s3.amazonaws.com/user-uploads/63da722f2d207d0049da10b1/room-content/da93c2361ca46942723723d0d03454e8.svg)|- **Security Requirements:** Ensuring that logs are stored in compliance with organisational or regulatory security protocols.<br>- **Accessibility Needs:** How quickly and by whom the logs need to be accessed can influence the choice of storage.<br>- **Storage Capacity:** The volume of logs generated may require significant storage space, influencing the choice of storage solution.<br>- **Cost Considerations:** The budget for log storage may dictate the choice between cloud-based or local solutions.<br>- **Compliance Regulations:** Specific industry regulations governing log storage can affect the choice of storage.<br>- **Retention Policies:** The required retention time and ease of retrieval can affect the decision-making process.<br>- **Disaster Recovery Plans:** Ensuring the availability of logs even in system failure may require specific storage solutions.|

Log Retention

It is vital to recognise that log storage is not infinite. Therefore, a reasonable balance between retaining logs for potential future needs and the storage cost is necessary. Understanding the concepts of Hot, Warm, and Cold storage can aid in this decision-making:

|   |   |
|---|---|
|- **Hot Storage:** Logs from the past **3-6 months** that are most accessible. Query speed should be near real-time, depending on the complexity of the query.<br>- **Warm Storage:** Logs from **six months to 2 years**, acting as a data lake, easily accessible but not as immediate as Hot storage.<br>- **Cold Storage:** Archived or compressed logs from **2-5 years**. These logs are not easily accessible and are usually used for retroactive analysis or scoping purposes.|![Log Retention Calendar](https://tryhackme-images.s3.amazonaws.com/user-uploads/63da722f2d207d0049da10b1/room-content/ffc7ff68c1584d3c5ddf13b47c237c69.png)|

Managing the cost of storing logs is critical for organisations, and carefully selecting Hot, Warm, or Cold storage strategies can help keep these costs in check.

Log Deletion

Log deletion must be performed carefully to avoid removing logs that could still be of value. The backup of log files, especially crucial ones, is necessary before deletion.

It is essential to have a well-defined deletion policy to ensure compliance with data protection laws and regulations. Log deletion helps to:

- Maintain a manageable size of logs for analysis.
- Comply with privacy regulations, such as GDPR, which require unnecessary data to be deleted.
- Keep storage costs in balance.

Best Practices: Log Storage, Retention and Deletion

- Determine the storage, retention, and deletion policy based on both business needs and legal requirements.
- Regularly review and update the guidelines per changing conditions and regulations.
- Automate the storage, retention, and deletion processes to ensure consistency and avoid human errors.
- Encrypt sensitive logs to protect data.
- Regular backups should be made, especially before deletion.

Practical Activity: Log Management with logrotate

This activity aims to introduce `logrotate`, a tool that automates log file rotation, compression, and management, ensuring that log files are handled systematically. It allows automatic rotation, compression, and removal of log files. As an example, here's how we can set it up for `/var/log/websrv-02/rsyslog_sshd.log`:

1. **Create a Configuration File:** `sudo gedit /etc/logrotate.d/98-websrv-02_sshd.conf`, `sudo nano /etc/logrotate.d/98-websrv-02_sshd.conf`, `sudo vi /etc/logrotate.d/98-websrv-02_sshd.conf`, or `sudo vim /etc/logrotate.d/98-websrv-02_sshd.conf`
2. **Define Log Settings:**
    
    ```yaml
    /var/log/websrv-02/rsyslog_sshd.log {
        daily
        rotate 30
        compress
        lastaction
            DATE=$(date +"%Y-%m-%d")
            echo "$(date)" >> "/var/log/websrv-02/hashes_"$DATE"_rsyslog_sshd.txt"
            for i in $(seq 1 30); do
                FILE="/var/log/websrv-02/rsyslog_sshd.log.$i.gz"
                if [ -f "$FILE" ]; then
                    HASH=$(/usr/bin/sha256sum "$FILE" | awk '{ print $1 }')
                    echo "rsyslog_sshd.log.$i.gz "$HASH"" >> "/var/log/websrv-02/hashes_"$DATE"_rsyslog_sshd.txt"
                fi
            done
            systemctl restart rsyslog
        endscript
    }
    ```