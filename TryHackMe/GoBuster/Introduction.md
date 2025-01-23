This room focuses on the offensive security tool Gobuster, often used for reconnaissance. We will explore how this tool can enumerate web directories, subdomains, and virtual hosts. This room will follow a hands-on approach where you can follow along with the commands explained and execute them yourself to see the results.

Gobuster is an open-source offensive tool written in Golang. It enumerates web directories, DNS subdomains, vhosts, Amazon S3 buckets, and Google Cloud Storage by brute force, using specific wordlists and handling the incoming responses. Many security professionals use this tool for penetration testing, bug bounty hunting, and cyber security assessments. Looking at the phases of ethical hacking, we can place Gobuster between the reconnaissance and scanning phases.

Before exploring Gobuster, let’s briefly discuss the concepts of enumeration and Brute Force.

**Enumeration**

Enumeration is the act of listing all the available resources, whether they are accessible or not. For example, Gobuster enumerates web directories.
The help page contains multiple sections:

- **Usage:** Shows the syntax on how to use the command.
- **Available Commands:** Multiple commands are available to aid us in enumerating directories, files, DNS subdomains, Google Cloud Storage buckets, and Amazon AWS S3 buckets. Throughout this room, we will focus on the `dir`, `dns`, and `vhost` commands. We will cover each of them in the following tasks.
- **Flags:** These are specific options we can configure to customize our commands. Let’s look at the flags we will often use throughout this room:
## Example

Let us look at an example of how we would use these commands and flags together to enumerate a web directory:

```
gobuster dir -u "http://www.example.thm/" -w /usr/share/wordlists/dirb/small.txt -t 64
```

- `gobuster dir` indicates that we will use the directory and file enumeration mode.
- `-u "http://www.example.thm/"` tells Gobuster that the target URL is [http://example.thm/](http://example.thm/).
- `-w /usr/share/wordlists/dirb/small.txt` directs Gobuster to use the _small.txt_ wordlist to brute force the web directories. Gobuster will use each entry in the wordlist to form a new URL and send a GET request to that URL. If the first entry of the wordlist were images, Gobuster would send a GET request to [http://example.thm/images/.](http://example.thm/images/)
- `-t 64` sets the number of threads Gobuster will use to 64. This improves the performance drastically.

Now that we have a quick overview of Gobuster, let’s explore the different modes and their use cases in the following tasks.