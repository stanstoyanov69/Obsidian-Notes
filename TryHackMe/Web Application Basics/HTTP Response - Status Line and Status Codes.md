When you interact with a web application, the server sends back an **HTTP response** to let you know whether your request was successful or something went wrong. These responses include a **status code** and a short explanation (called the **Reason Phrase**) that gives insight into how the server handled your request.

### Status Line

The first line in every HTTP response is called the **Status Line**. It gives you three key pieces of info:

1. **HTTP Version**: This tells you which version of HTTP is being used.
2. **Status Code**: A three-digit number showing the outcome of your request.
3. **Reason Phrase**: A short message explaining the status code in human-readable terms.
**Informational Responses (100-199)**  
These codes mean the server has received part of the request and is waiting for the rest. It’s a "keep going" signal.

**Successful Responses (200-299)**  
These codes mean everything worked as expected. The server processed the request and sent back the requested data.

**Redirection Messages (300-399)**  
These codes tell you that the resource you requested has moved to a different location, usually providing the new URL.

**Client Error Responses (400-499)**  
These codes indicate a problem with the request. Maybe the URL is wrong, or you’re missing some required info, like authentication.

**Server Error Responses (500-599)**  
These codes mean the server encountered an error while trying to fulfil the request. These are usually server-side issues and not the client’s fault.