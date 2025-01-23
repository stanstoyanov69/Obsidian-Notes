As mentioned in the previous task, the results of running CAPA against cryptbot.bin  will be discussed in the succeeding task. As such, we will dissect the results per block and topic.

The first block contains basic information about the file. This includes the following:

- The cryptographic algorithms, such as the `md5`, and `sha1/256`.
- The `analysis` field tells us how CAPA performed its analysis on the file.
- The `os` field reveals the operating system (OS) context for which the identified capabilities apply.
- The `arch` field allows us to determine whether we are dealing with a binary related to x86 architecture.
- The `path` where the analyzed file was located.

Terminal

```powershell
┌─────────────┬────────────────────────────────────────────────────────────────────────────────────┐
│ md5         │ 3b9d26d2e7433749f2c32edb13a2b0a2                                                   │
│ sha1        │ 969437df8f4ad08542ce8fc9831fc49a7765b7c5                                           │
│ sha256      │ ae7bc6b6f6ecb206a7b957e4bb86e0d11845c5b2d9f7a00a482bef63b567ce4c                   │
│ analysis    │ static                                                                             │
│ os          │ windows                                                                            │
│ format      │ pe                                                                                 │
│ arch        │ i386                                                                               │
│ path        │ /home/strategos/Room-CAPA/cryptbot.bin                                             │
└─────────────┴────────────────────────────────────────────────────────────────────────────────────┘
```

  

###   

### MITRE ATT&CK

The MITRE ATT&CK (Adversarial Tactics, Techniques, and Common Knowledge) framework is a comprehensive global knowledge repository that meticulously documents the tactics and techniques employed by threat actors at every stage of a cyber-attack. It functions as a strategic playbook, providing detailed insights into attackers' methods, from **gaining initial access** to **maintaining a presence**, **escalating privileges**, **evading defenses**, **moving laterally within a network**, and much more. 

CAPA uses this format for the output. Note that some results may or may not contain the Technique and Sub-technique Identifier.

|Format|Sample|Explanation|
|---|---|---|
|**ATT&CK Tactic**::**ATT&CK Technique**::**Technique Identifier**|Defense Evasion::Obfuscated Files or Information::T1027|**DEFENSE EVASION =** ATT&CK Tactic  <br>**Obfuscated Files or Information =** ATT&CK Technique  <br>**T1027 =** Technique Identifier|
|**ATT&CK Tactic**::**ATT&CK Technique**::**ATT&CK Sub-Technique**::**Technique Identifier**[.]Sub-technique **Identifier**|Defense Evasion::Obfuscated Files or Information::Indicator Removal from Tools T1027.005|**DEFENSE EVASION** = ATT&CK Tactic  <br>**Obfuscated Files or Information** = ATT&CK Technique  <br>**Indicator Removal from Tools** = ATT&CK Sub-Technique  <br>**T1027 =** Technique Identifier  <br>**005** = Sub-Technique Identifier|

  
  

MITREATT&CK

```powershell
┌──────────────────────┬───────────────────────────────────────────────────────────────────────────┐
│ ATT&CK Tactic        │ ATT&CK Technique                                                          │
├──────────────────────┼───────────────────────────────────────────────────────────────────────────┤
│ DEFENSE EVASION      │ Obfuscated Files or Information [T1027]                                   │
│                      │ Obfuscated Files or Information::Indicator Removal from Tools [T1027.005] │
│                      │ Virtualization/Sandbox Evasion::System Checks [T1497.001]                 │
│ DISCOVERY            │ File and Directory Discovery [T1083]                                      │
│ EXECUTION            │ Command and Scripting Interpreter::PowerShell [T1059.001]                 │
│                      │ Shared Modules [T1129]                                                    │
│ IMPACT               │ Resource Hijacking [T1496]                                                │
│ PERSISTENCE          │ Scheduled Task/Job::At [T1053.002]                                        │
│                      │ Scheduled Task/Job::Scheduled Task [T1053.005]                            │
└──────────────────────┴───────────────────────────────────────────────────────────────────────────┘
```

  
In CAPA's final output, they referenced the MITRE Framework. This helps analysts or defenders map the file's behaviour to the adversary's playbook, which can help narrow down the scope of the investigation during an incident. To dig deeper into this topic, you might want to check out our room for [MITRE ATT&CK Framework](https://tryhackme.com/r/room/mitre).  

###   

### MAEC

**Malware Attribute Enumeration and Characterization** is a specialized language designed to encode and communicate complex details concerning malware. It contains an extensive range of attributes, including behaviours, artefacts, and interconnections among various instances of malware. This language functions as a standardized system for tracking and analyzing the complicated complexities of malware.

Malware Attribute Enumeration and Characterization

```powershell
┌─────────────────────────────┬────────────────────────────────────────────────────────────────────┐
│ MAEC Category               │ MAEC Value                                                         │
├─────────────────────────────┼────────────────────────────────────────────────────────────────────┤
│ malware-category            │ launcher                                                           │
└─────────────────────────────┴────────────────────────────────────────────────────────────────────┘
```

  

Let’s check the table below to see the most commonly used MAEC values by CAPA: **Downloader** and **Launcher**.

|**MAEC Value**|Description|
|---|---|
|Launcher|Exhibits behaviours that trigger specific actions similar to malware behaviour.|
|Downloader|Exhibits behaviours wherein it downloads and executes other files, usually seen on more complex malware.|

  

When CAPA tags a file with a “**launcher**” MAEC value, it indicates that the file demonstrates behaviour similar to but not limited to:

- Dropping additional payloads
- Activating persistence mechanisms
- Connecting to command-and-control (C2) servers
- Executing specific functions

This is interesting! Some of these behaviours are also present in the Malware Behavior Catalogue (MBC)  and Capability block, which we will discuss in the next task!

  

Additionally, when CAPA tags a file with a “**Downloader**” MAEC value, it indicates that the file demonstrates behaviour similar but not limited to:

- Fetching additional payloads or resources from the internet  
    
- pulling in updates
- executing secondary stages
- retrieving configuration files