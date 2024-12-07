There are various actions a defender can take to help protect the users from falling victim to a malicious email. 

Some examples of these actions are listed below:

- Email Security (SPF, DKIM, DMARC)
- SPAM Filters (flags or blocks incoming emails based on reputation)
- Email Labels (alert users that an incoming email is from an outside source)
- Email Address/Domain/URL Blocking (based on reputation or explicit denylist)
- Attachment Blocking (based on the extension of the attachment)
- Attachment Sandboxing (detonating email attachments in a sandbox environment to detect malicious activity)
- Security Awareness Training (internal phishing campaigns)

## SPF (Sender Policy Framework)

Per [dmarcian](https://dmarcian.com/what-is-spf/), "_Sender Policy Framework (SPF) is used to authenticate the sender of an email. With an SPF record in place, Internet Service Providers can verify that a mail server is authorized to send email for a specific domain. An SPF record is a DNS TXT record containing a list of the IP addresses that are allowed to send email on behalf of your domain._"

Below is a visual workflow for SPF.
![[Pasted image 20241118134130.png]]
An explanation for the above record:

- `v=spf1` -> This is the start of the SPF record
- `ip4:127.0.0.1` -> This specifies which IP (in this case version IP4 & not IP6) can send mail
- `include:_spf.google.com` -> This specifies which domain can send mail
- `-all` -> non-authorized emails will be rejected


## DKIM (DomainKeys Identified Mail)

What is **DKIM**?

Per [dmarcian](https://dmarcian.com/what-is-dkim/), "_DKIM stands for DomainKeys Identified Mail and is used for the authentication of an email that’s being sent. Like SPF, DKIM is an open standard for email authentication that is used for DMARC alignment. A DKIM record exists in the DNS, but it is a bit more complicated than SPF. DKIM’s advantage is that it can survive forwarding, which makes it superior to SPF and a foundation for securing your email._"

How does a DKIM record look like?
`v=DKIM1; k=rsa; p=MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAxTQIC7vZAHHZ7WVv/5x/qH1RAgMQI+y6Xtsn73rWOgeBQjHKbmIEIlgrebyWWFCXjmzIP0NYJrGehenmPWK5bF/TRDstbM8uVQCUWpoRAHzuhIxPSYW6k/w2+HdCECF2gnGmmw1cT6nHjfCyKGsM0On0HDvxP8I5YQIIlzNigP32n1hVnQP+UuInj0wLIdOBIWkHdnFewzGK2+qjF2wmEjx+vqHDnxdUTay5DfTGaqgA9AKjgXNjLEbKlEWvy0tj7UzQRHd24a5+2x/R4Pc7PF/y6OxAwYBZnEPO0sJwio4uqL9CYZcvaHGCLOIMwQmNTPMKGC9nt3PSjujfHUBX3wIDAQAB`

An explanation of the above record:

- `v=DKIM1`-> This is the version of the DKIM record. This is optional. 
- `k=rsa` -> This is the key type. The default value is RSA. RSA is an encryption algorithm (cryptosystem).
- `p=` -> This is the public key that will be matched to the private key, which was created during the DKIM setup process. 

Refer to the DKIM resource [here](https://dmarcian.com/dkim-selectors/) and [here](https://help.returnpath.com/hc/en-us/articles/222481088-DKIM-DNS-record-overview) for additional information. 

The below image is a snippet of an email header for an email flagged as spam that contained a potentially malicious attachment.


## DMARC (Domain-Based Message Authentication, Reporting, and Conformance)

How does a basic DMARC record look like?

`v=DMARC1; p=quarantine; rua=mailto:postmaster@website.com` 

An explanation of the above record:  

- `v=DMARC1` -> Must be in all caps, and it's not optional
- `p=quarantine` -> If a check fails, then an email will be sent to the spam folder (DMARC Policy)
- `rua=mailto:postmaster@website.com` -> Aggregate reports will be sent to this email address


## S/MIME (Secure/Multipurpose Internet Mail Extensions)


What is **[S/MIME](https://docs.microsoft.com/en-us/exchange/security-and-compliance/smime-exo/smime-exo)**?  

Per Microsoft, "_S/MIME (Secure/Multipurpose internet Mail Extensions) is a widely accepted protocol for sending digitally signed and encrypted messages_."

As you can tell from the definition above, the 2 main ingredients for S/MIME are:

1. **Digital Signatures**
2. **Encryption**

Using [Public Key Cryptography](https://www.ibm.com/docs/en/ztpf/2023?topic=concepts-public-key-cryptography), S/MIME guarantees data integrity and nonrepudiation.   

- If Bob wishes to use S/MIME, then he'll need a digital certificate. This digital certificate will contain his public key. 
- With this digital certificate, Bob can "sign" the email message with his private key. 
- Mary can then decrypt Bob's message with Bob's public key. 
- Mary will do the same (send her certificate to Bob) when she replies to his email, and Bob complete the same process on his end.
- Both will now have each other's certificates for future correspondence. 

The illustration below will help you understand how public key cryptography works.![[Pasted image 20241118231910.png]]


## SMTP Status Codes
### General SMTP status codes

SMTP codes that start with 2 and 3 are general status messages that are sent in reply to requests from the sending server. They do not indicate errors in the mail delivery but are used as prompts in the exchange between the mail servers.

|   |   |   |
|---|---|---|
|**SMTP code**|**Description**|**Meaning**|
|214|Help message|A response to the HELP command that usually includes a link or URL to the FAQ page.|
|220|SMTP Service ready|The receiving server is ready for the next command.|
|221|Service closing transmission channel|The receiving server is closing the SMTP connection.|
|235|2.7.0 Authentication succeeded|The sending server’s authentication is successful.|
|250|Requested mail action okay, completed|Success! The email was delivered.|
|251|User not local; will forward to <forward-path>|The receiving server doesn’t recognize the recipient but it will forward it to another email address.|
|252|Cannot VRFY user, but will accept message and attempt delivery|The receiving server doesn’t recognize the recipient but it will try to deliver the email anyway.|
|334|Reponse to email authentication AUTH command when the authentication method is accepted|Authentication has been successful.|
|354|Start mail input|The email “header” has been received, the server is now waiting for the “body” of the message.|

### Temporary SMTP error codes

SMTP 400 codes are transient errors and are usually related to issues at the receiving mail server. Messages are returned as a soft bounce and the sender may try again after, for example, reducing the size of the attachments in the email.

|   |   |   |
|---|---|---|
|**SMTP code**|**Description**|**Meaning**|
|421|Service not available, closing transmission channel|The receiving server or sending server is not reachable but another mail delivery will be attempted. If you are using a remote server like MailerSend's SMTP relay to send emails, test that you can connect to it successfully. Otherwise, you may wish to check the receiving server’s availability.|
|450|Requested mail action not taken: mailbox unavailable|This error could mean that the recipient does not exist, the mailbox does not have permission to receive the email, or the message was rejected due to a blocklist or filter.  <br>  <br>To fix this, you should confirm the recipient’s email address, see if [your IP address is on a blocklist](https://www.mailercheck.com/articles/email-blocklist-removal), test your email for spam-like content, or try sending an email without an attachment.|
|451|Requested action aborted: error in processing|The receiving server is unable to process the message due to [email authentication rules](https://www.mailersend.com/blog/email-authentication). For example, if Sender Policy Framework (SPF) is being used, you should confirm that a DNS lookup can be made for your sending domain and that the domain’s name server is functioning properly.|
|452|Requested action not taken: insufficient system storage|The receiving server is overwhelmed by too many messages being sent at once or is out of memory or storage space. Review your sending rate by looking at your mail-sending queue and logs, or inform the server’s mail administrator about the storage and free memory issues.|
|455|Server unable to accommodate the parameters|The server cannot process the command at this time. You can retry after waiting a while or contact the receiving server’s mail administrator if the error persists.|

### Permanent SMTP error codes

SMTP 500 reply codes are mail delivery errors of a permanent nature that are usually caused by the sender. The receiving server returns the message as a hard bounce and prefers that the sender not try again unless the problem is fixed.

The 500 series starts with errors in issuing SMTP commands like the following examples:

|   |   |   |
|---|---|---|
|**SMTP code**|**Description**|**Meaning**|
|500|Syntax error, command unrecognized|The receiving server does not recognize the command. If your server is using antivirus or firewall software, try disabling them before sending the message again.|
|501|Syntax error in parameters or arguments|The command is recognized but there are errors with its options or command arguments. This server error is sometimes returned for an invalid or incorrect email! But it may be due to your antivirus or firewall software as well.|
|502|Command not implemented|The command is currently not supported on the receiving server. Review your sending commands as well as your MTA’s configuration.|
|503|Bad sequence of commands|The receiving server recognizes the command but its parameters or options are in the wrong sequence. This sometimes appears when the email account is not authenticated. Do review your MTA’s configuration as well.|
|504|Command parameter not implemented|Similar to 502, the command is recognized but its parameters or options are not supported on the receiving server. You may wish to review your sending commands as well as your MTA’s configuration.|
|521|Server does not accept mail|The server does not receive or send mail. This may be because the server is part of a mail relay. The email may fail or be relayed to another mail server. Check if the email has been delivered to confirm.|

The SMTP error codes then get more serious, like being suspected of sending spam or appearing in a blocklist. As an email sender, you should pay attention to the following codes because they can affect your sending reputation and [email deliverability](https://www.mailersend.com/help/improve-email-deliverability).

|   |   |   |
|---|---|---|
|**SMTP code**|**Description**|**Meaning**|
|535|Authentication credentials are invalid|There is an issue with client authentication with the email server. This may be because of incorrect credentials, invalid authentication methods, or invalid encryption settings.|
|541|The recipient address rejected your message|The mail from the sender has been flagged as spam or blocked by the receiving server’s rules. Find out if your IP address is in a blocklist and [scan your emails for content](https://www.mailercheck.com/articles/improve-your-deliverability-with-inbox-insights) that could trigger spam filters. If you’re clear, ask the administrator of the server to put you on their safelist.|
|550|Requested action not taken: mailbox unavailable|The recipient’s email address does not exist. Verify the email address by making sure it is free of typos or use an [email verification tool](https://www.mailersend.com/features/email-verification-tool) like MailerSend's inbuilt feature.<br><br>Error code 550 is sometimes used as a generic error code and it can also appear as **550 Blocked error** or **550 Invalid recipient** depending on the server's configuration. If you get the blocked error message, check to see if your IP address is in a blocklist.|
|551|User not local; please try <forward-path>|The recipient was not found on the server but the message will be forwarded to another email. Used for spam prevention, this error is shown when you are not authorized to relay mail through the server. Review your authentication records to see if you can use an SMTP relay.|
|552|Requested mail action aborted: exceeded storage allocation|The user’s mailbox is full! Besides waiting for messages to be deleted, you can try to contact them through other means and inform them that their inbox is full.|
|553|Requested action not taken: mailbox name not allowed|The recipient cannot be found due to errors in the email address. Check that the email addresses are correct in the To, Cc and Bcc fields.|
|554|Transaction failed|This is bad news! The receiving mail server will not accept your message because, for example, you’re on a blocklist. Confirm whether your IP address appears in a blocklist. If you’re good, send a request to the receiving server to put your IP in their safelist.|