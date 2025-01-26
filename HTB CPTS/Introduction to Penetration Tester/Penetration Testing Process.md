## Penetration Testing Stages

The most effective way to represent and define these is through interdependent `stages`. We often find in our research that these processes are presented in the form of a circular process. If we look at this more closely and imagine that even a single component of the circular process does not apply, the entire process is disrupted. Strictly defined, the whole process fails. If we assume that we start this process from the beginning, but already with the newly acquired information, it is already a new process approach that does not undo the previous one.

The problem is that with these representations and approaches, there is often nothing to fall back on to extend our penetration testing process. As we have discussed, there is no step-by-step guide we can follow but `stages` that allow the individual steps and approaches to be flexibly varied and adapted to the results and information we receive. We can develop our own playbook for various things we try at different stages of a penetration test, but every environment is different, and thus, we need to adapt constantly.

![](https://academy.hackthebox.com/storage/modules/90/0-PT-Process.png)

#### Pre-Engagement

`Pre-engagement` is educating the client and adjusting the contract. All necessary tests and their components are strictly defined and contractually recorded. In a face-to-face meeting or conference call, many arrangements are made, such as:

- `Non-Disclosure Agreement`
- `Goals`
- `Scope`
- `Time Estimation`
- `Rules of Engagement`

#### Information Gathering

`Information gathering` describes how we obtain information about the necessary components in various ways. We search for information about the target company and the software and hardware in use to find potential security gaps that we may be able to leverage for a foothold.

#### Vulnerability Assessment

Once we get to the `Vulnerability Assessment` stage, we analyze the results from our `Information Gathering` stage, looking for known vulnerabilities in the systems, applications, and various versions of each to discover possible attack vectors. Vulnerability assessment is the evaluation of potential vulnerabilities, both manually and through automated means. This is used to determine the threat level and the susceptibility of a company's network infrastructure to cyber-attacks.

#### Exploitation

In the `Exploitation` stage, we use the results to test our attacks against the potential vectors and execute them against the target systems to gain initial access to those systems.

#### Post-Exploitation

At this stage of the penetration test, we already have access to the exploited machine and ensure that we still have access to it even if modifications and changes are made. During this phase, we may try to escalate our privileges to obtain the highest possible rights and hunt for sensitive data such as credentials or other data that the client is concerned with protecting (pillaging). Sometimes we perform post-exploitation to demonstrate to a client the impact of our access. Other times we perform post-exploitation as an input to the lateral movement process described next.

#### Lateral Movement

Lateral movement describes movement within the internal network of our target company to access additional hosts at the same or a higher privilege level. It is often an iterative process combined with post-exploitation activities until we reach our goal. For example, we gain a foothold on a web server, escalate privileges and find a password in the registry. We perform further enumeration and see that this password works to access a database server as a local admin user. From here, we can pillage sensitive data from the database and find other credentials to further our access deeper into the network. In this stage, we will typically use many techniques based on the information found on the exploited host or server.

#### Proof-of-Concept

In this stage, we document, step-by-step, the steps we took to achieve network compromise or some level of access. Our goal is to paint a picture of how we were able to chain together multiple weaknesses to reach our goal so they can see a clear picture of how each vulnerability fits in and help prioritize their remediation efforts. If we don't document our steps well, it's hard for the client to understand what we were able to do and, thus, makes their remediation efforts more difficult. If feasible, we could create one or more scripts to automate the steps we took to assist our client in reproducing our findings. We cover this in-depth in the `Documentation & Reporting` module.

#### Post-Engagement

During post-engagement, detailed documentation is prepared for both administrators and client company management to understand the severity of the vulnerabilities found. At this stage, we also clean up all traces of our actions on all hosts and servers. During this stage, we create the deliverables for our client, hold a report walkthrough meeting, and sometimes deliver an executive presentation to target company executives or their board of directors. Lastly, we will archive our testing data per our contractual obligations and company policy. We will typically retain this data for a set period or until we perform a post-remediation assessment (retest) to test the client's fixes.