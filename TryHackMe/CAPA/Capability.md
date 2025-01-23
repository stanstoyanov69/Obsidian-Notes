

### Capability

Below is a table with the **Capability and its related TLN, namespace, and the rules associated** with the yaml file. Please have a good look.

|Capability|Top-Level Namespace (TLN)|Namespaces|Rule YAML file|Notes|
|---|---|---|---|---|
|reference anti-VM strings|[**Anti-Analysis**](https://github.com/MBCProject/capa-rules-1/tree/master/anti-analysis)|anti-vm/vm-detection|reference-anti-vm-strings.yml|To check all rules under this namespace, click [here](https://github.com/MBCProject/capa-rules-1/tree/master/anti-analysis/anti-vm/vm-detection)|
|reference anti-VM strings targeting VMWare|**Anti-Analysis**|anti-vm/vm-detection|reference-anti-vm-strings-targeting-vmware.yml|To check all rules under this namespace, click [here](https://github.com/MBCProject/capa-rules-1/tree/master/anti-analysis/anti-forensic)|
|reference anti-VM strings targeting VirtualBox|**Anti-Analysis**|anti-vm/vm-detection|reference-anti-vm-strings-targeting-virtualbox.yml|You may check the TLN(Top-Level Namespace).|
|reference HTTP User-Agent string|[**Communication**](https://github.com/MBCProject/capa-rules-1/tree/master/communication)|http/client|reference-http-user-agent-string.yml|To check all rules under this namespace, click [here](https://github.com/MBCProject/capa-rules-1/tree/master/communication/http/client))|
|check HTTP status code|**Communication**|http|check-http-status-code.yml|To check all rules under this namespace, click [here](https://github.com/MBCProject/capa-rules-1/tree/master/communication/http)|

**View More Capability**

|reference Base64 string|[**Data Manipulation**](https://github.com/MBCProject/capa-rules-1/tree/master/data-manipulation)|encoding/base64|reference-base64-string.yml|To check all rules under this namespace, click [here](https://github.com/MBCProject/capa-rules-1/tree/master/data-manipulation/encoding/base64)|
|---|---|---|---|---|
|encode data using XOR|**Data Manipulation**|encoding/XOR|encode-data-using-xor.yml|To check all rules under this namespace, click [here](https://github.com/MBCProject/capa-rules-1/tree/master/data-manipulation/encoding/xor)|
|---|---|---|---|---|
|contain a thread local storage (.tls) section|[**Executable**](https://github.com/MBCProject/capa-rules-1/tree/master/executable)|pe/section/tls|contain-a-thread-local-storage-tls-section.yml|You may check the TLN(Top-Level Namespace) for more rules.|
|---|---|---|---|---|
|get common file path|[**Host-Interaction**](https://github.com/MBCProject/capa-rules-1/tree/master/host-interaction)|file-system|get-common-file-path.yml|You may check the TLN(Top-Level Namespace) for more rules.|
|---|---|---|---|---|
|create directory|**Host-Interaction**|file-system/create|create-directory.yml|You may check the TLN(Top-Level Namespace) for more rules.|
|---|---|---|---|---|
|delete file|**Host-Interaction**|file-system/delete|delete-file.yml|To check all rules under this namespace, click [here](https://github.com/MBCProject/capa-rules-1/tree/master/host-interaction/file-system/delete)|
|---|---|---|---|---|
|read file on Windows|**Host-Interaction**|file-system/read|read-file-on-windows.yml|To check all rules under this namespace, click [here](https://github.com/MBCProject/capa-rules-1/tree/master/host-interaction/file-system/read)|
|---|---|---|---|---|
|write file on Windows|**Host-Interaction**|file-system/write|write-file-on-windows.yml|To check all rules under this namespace, click [here](https://github.com/MBCProject/capa-rules-1/tree/master/host-interaction/file-system/write)|
|---|---|---|---|---|
|get thread local storage value|**Host-Interaction**|process|get-thread-local-storage-value.yml|This rule is found under **TLN [Nursery](https://github.com/mandiant/capa-rules/tree/master/nursery),** a staging ground for unpolished rules.|
|---|---|---|---|---|
|allocate or change RWX memory|**Host-Interaction**|process/inject|allocate-or-change-rwx-memory.yml|To check all rules under this namespace, click [here](https://github.com/MBCProject/capa-rules-1/tree/master/host-interaction/process/inject)|
|---|---|---|---|---|
|create process on Windows|**Host-Interaction**|process create|create-process-on-windows.yml|To check all rules under this namespace, click [here](https://github.com/MBCProject/capa-rules-1/tree/master/host-interaction/process/create)|
|---|---|---|---|---|
|reference cryptocurrency strings|[**Impact**](https://github.com/MBCProject/capa-rules-1/tree/master/impact)|impact/cryptocurrency|reference-cryptocurrency-strings.yml|This rule is found under **TLN [Nursery](https://github.com/mandiant/capa-rules/tree/master/nursery),** a staging ground for unpolished rules.|
|---|---|---|---|---|
|link function at runtime on Windows|[**Linking**](https://github.com/MBCProject/capa-rules-1/tree/master/linking)|runtime-linking|link-function-at-runtime-on-windows.yml|To check all rules under this namespace, click [here](https://github.com/MBCProject/capa-rules-1/tree/master/linking/runtime-linking)|
|---|---|---|---|---|
|parse PE header|[**load-code**](https://github.com/MBCProject/capa-rules-1/tree/master/load-code)|load-code/pe|parse-pe-header.yml  <br>  <br>resolve-function-by-parsing-pe-exports.yml|To check all rules under this namespace, click [here](https://github.com/MBCProject/capa-rules-1/tree/master/load-code/pe)|
|---|---|---|---|---|
|resolve function by parsing PE exports|[**load-code**](https://github.com/MBCProject/capa-rules-1/tree/master/load-code)|load-code/pe|resolve-function-by-parsing-pe-exports.yml|To check all rules under this namespace, click [here](https://github.com/MBCProject/capa-rules-1/tree/master/load-code/pe)|
|---|---|---|---|---|
|run PowerShell expression|[**load-code**](https://github.com/MBCProject/capa-rules-1/tree/master/load-code/powershell)|load-code/PowerShell|run-powershell-expression.yml|To check all rules under this namespace, click [here](https://github.com/MBCProject/capa-rules-1/tree/master/linking/runtime-linking)|
|---|---|---|---|---|
|schedule task via at|[**persistence**](https://github.com/MBCProject/capa-rules-1/tree/master/persistence)|scheduled-tasks|schedule-task-via-at.yml|You may check the TLN(Top-Level Namespace) for more rules.|
|---|---|---|---|---|
|schedule task via schtasks|[**persistence**](https://github.com/MBCProject/capa-rules-1/tree/master/persistence)|scheduled-tasks|schedule-task-via-schtasks.yml|You may check the TLN(Top-Level Namespace) for more rules.|
|---|---|---|---|---|

  

To further explain this, let’s check the first capability on the table, “**reference anti-VM strings”**.

- We note that the related rules in YML format are **reference-anti-vm-strings.yml**
- This is under the namespace **anti-vm/vm-detection**
- which is also under the Top-Level Namespace **Anti-Analysis**

This tells us that CAPA was able to identify that the potentially malicious software **searches for VMware-specific registry keys**, the **presence of VMware tools**, or other **VM-related elements** by using the **reference-anti-vm-strings.yml** rule yaml file. Malware typically does this behaviour to avoid detection. That is why CAPA flagged this one.

Let’s have another example. Let’s look at "_**schedule task via schtasks**_"_._

- We note that the related rules in YML format is **schedule-task-via-schtasks.yml***
- This is under the namespace **scheduled-tasks**
- which is also under the Top-Level Namespace **persistence**

This tells us that CAPA could identify behaviours related to scheduled tasks within the Windows operating system. It might have recognized patterns indicating that the executable registers itself as a scheduled task to maintain persistence using the rule defined in **schedule-task-via-schtasks.yml.**

Hold on! Have you noticed something?

That’s right! The item under Capability has the same name as the YML files under the Rules, with the addition of a dash (-) character between spaces! Simple because Capability is the name of the rule.

Now, we want to take note of some exceptions here. Where the Capability or rules are not located under its Namespace, let’s take the Capability **reference cryptocurrency strings** from the table above; this should be under the **Impact** Top-Level Namespace, right? However, if you go through the folders, you won’t be able to find the corresponding rules. It will be located under the **Nursery** TLN. This is the placeholder for rules that are not quite polished yet.

Now that we have a good overview and understanding of the Capability and Namespace contents, we should be able to explain the sample result from the previous tasks. Therefore, let’s do a quick recap using one of the results. Shall we?

Malware Behavior Catalogue

```powershell
┌───────────────────────────────────────────┬───────────────────────────────────────────┐
│ Capability                                │ Namespace                                 │
├───────────────────────────────────────────┼───────────────────────────────────────────┤
│ reference Base64 string                   │ data-manipulation/encoding/base64         │
└───────────────────────────────────────────┴───────────────────────────────────────────┘
```

  

Here's the explanation for the above result. See the table below.

|Label|Value|Explanation|
|---|---|---|
|Capability|**reference base64 string**|Malware has the capability to encode data using a base64 scheme.|
|Top-Level Namespace|**data-manipulation**|contains a set of rules that govern the behaviors involved in altering data within executable files. This aspect can be considered the “data transformation” component of malware behaviour, encompassing actions such as String Encryption and Data Encoding.|
|Namespace|**encoding/base64**|this namespace consists of rules for encoding and decoding data using Base64 and XOR|
|Rule YAML File Matched?|**reference-base64-string.yml**|Remember that the capability's name is also the rule's name with an additional dash (-) character between spaces.|

Knowing this information, you may say this file can use the base64 encoding scheme!  

  

Now we’re done dissecting the results from the sample run from the previous task!