What Information should we colletct.
- Sender email address
- Sender IP address
- Reverse lookup of the sender IP address
- Email subject line
- Recipient email address (this information might be in the CC/BCC field)
- Reply-to email address (if any)
- Date/time
Afterward, we draw our attention to the email body and attachment(s) (if any).

Below is a checklist of the artifacts an analyst (you) needs to collect from the email body:

- Any URL links (if an URL shortener service was used, then we'll need to obtain the real URL link)
- The name of the attachment
- The hash value of the attachment (hash type MD5 or SHA256, preferably the latter)


# EMAIL HEADER ANALYSIS

Some of the pertinent information that we need to collect can be obtained visually from an email client or web client (such as Gmail, Yahoo!, etc.). But some information, such as the sender's IP address and reply-to information, can only be obtained via the email header.

## Usefull Tools
- **Messageheader**: [https://toolbox.googleapps.com/apps/messageheader/analyzeheader](https://toolbox.googleapps.com/apps/messageheader/analyzeheader)
- - **Message Header Analyzer**: [https://mha.azurewebsites.net/](https://mha.azurewebsites.net/)
- [mailheader.org](https://mailheader.org/).
- The tools below can help you analyze information about the sender's IP address:

- IPinfo.io: [https://ipinfo.io/](https://ipinfo.io/)
- - URLScan.io: [https://urlscan.io/](https://urlscan.io/)
- - Talos Reputation Center: [https://talosintelligence.com/reputation](https://talosintelligence.com/reputation)


## EMAIL BODY ANALYSIS

Now it's time to direct your focus to the email body. This is where the malicious payload may be delivered to the recipient either as a link or an attachment. 

Links can be extracted manually, either directly from an HTML formatted email or by sifting through the raw email header.

Below is an example of obtaining a link manually from an email by right-clicking the link and choosing **Copy Link Loca**tion
![[Pasted image 20241118125813.png]]The same can be accomplished with the assistance of a tool. One tool that can aid us with this task is URL Extractor. 

- URL Extractor: [https://www.convertcsv.com/url-extractor.htm](https://www.convertcsv.com/url-extractor.htm)[](https://www.convertcsv.com/url-extractor.htm)

You can copy and paste the raw header into the text box for **Step 1: Select your input**.![[Pasted image 20241118125823.png]]