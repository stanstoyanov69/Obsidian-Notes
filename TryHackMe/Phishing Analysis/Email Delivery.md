There are 3 specific protocols involved to facilitate the outgoing and incoming email messages, and they are briefly listed below.

- **SMTP** (**Simple Mail Transfer Protocol)** - It is utilized to handle the sending of emails. 

- **POP3 (Post Office Protocol)** - Is responsible transferring email between a client and a mail server. 

- **IMAP (Internet Message Access Protocol)** - Is responsible transferring email between a client and a mail server


	 # Email Headers
	Before we begin, we need to understand that there are two parts to an email:

- the email **header** (information about the email, such as the email servers that relayed the email)
- the email **body** (text and/or HTML formatted text)

The syntax for email messages is known as the **[Internet Message Format](https://datatracker.ietf.org/doc/html/rfc5322)** (**IMF**).

Let's look at email headers first. 

What do you look for when analyzing a potentially malicious email?  

Let's start with the following email header fields:

1. **From** - the sender's email address
2. **Subject** - the email's subject line
3. **Date** - the date when the email was sent
4. **To** - the recipient's email address

This is usually clearly visible in any email client. Let's look at an example of these fields in the below image.![[Pasted image 20241118094911.png]]

# EMAIL BODY
