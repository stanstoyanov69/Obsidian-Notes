First, let's verify snort is installed. The following command will show you the instance version.
```
user@ubuntu$ snort -V
```

Before getting your hands dirty, we should ensure our configuration file is valid.  

Here **"-T"** is used for testing configuration, and **"-c"** is identifying the configuration file **(snort.conf)**.  
Note that it is possible to use an additional configuration file by pointing it with **"-c"**.

```
sudo snort -c /etc/snort/snort.conf -T
```