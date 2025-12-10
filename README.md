# Clash-For-Ubuntu
clash for unbuntu tutorial

* translate from [bywave](https://console.bywa.art/index.php/knowledgebase/4/)

Clash is a cross-platform agent program developed based on Go language.

Clash For Linux is a Linux agent developed based on Electron and Clash, which allows users to configure Clash intuitively through GUI.

Download and install Clash for Linux

~~[Network disk download](https://wwi.lanzouy.com/b07xybeid)~~

~~[github download](https://github.com/Dreamacro/clash/releases/download/v1.2.0/clash-linux-amd64-v1.2.0.gz)~~

[mirror address](https://drive.cn-v1-oss.eu.org/d/4b68087528ca4936b189/)

## Configure

* Create the directory where you want to store the files, decompress the gz package, e.g. the path store is /home/clash, you can rename the decompressed file to crash for easy reading

```
unzip /clash-linux-amd64-v0.18.0.gz
```

* Give the file execute permission

```
chmod +x clash
```

* Startup file

```
./clash
```

The first startup will automatically generate two files, Config.yaml and Country.mmdb, in the user directory.

The generated Config.yaml file is empty, and you need to fill in your own proxy information later.

The directory generated here is /home/.config/clash. If it is inconsistent, you can use the find command to find it.

* Add Clash configuration subscription

Go to the subscription center of the official website and select Copy Subscription, then visit [Add &client=clash after the subscription address] in the browser, then right-click the browser page and select "Save As" to save the page

Then modify the saved file to Config.yaml (the format should also be modified)

Then we edit the content of the file

First delete all the lines in front of port: 7890

After the modification is completed, save it and replace the empty Config.yaml file that was just unzipped

* Start crash

After the configuration is complete, re-execute the command to start the flash to load the modified configuration file

Open the URL below to access the management page

[https://clash.razord.top/#/proxies](http://clash.razord.top/#/proxies)

* Set up the virtual machine network, configure the proxy

Take centos7.4 as an example, open the system settings, select the network, click the network proxy, select manual, configure according to the port set in the yml configuration file, fill in the HTTP and HTTPS proxy as 127.0.0.1:7890, and fill in the Socks host as 127.0. 0.1:7891 to enable system proxy

## Set up diversion
Click on Proxies on the left side of the window.

By default, Clash uses Rule mode. Global and Direct modes are not recommended.

Clash supports the use of different policies for different websites through policy groups. Reasonable use of triage can improve your experience.

The line used by the proxy decision, where you can switch nodes.

Domestic decides all websites in mainland China, and the default DIRECT is direct connection.

Global decides to use a proxy as the default proxy for mainstream websites that cannot be accessed in mainland China.

Others decides unpopular websites that are not included in the Global rules, and the default Proxy is to use a proxy.

**Happy using!**

## Backup
clash/ is copied from my own device home/.config/, the clash.yaml file is set by using the [subscription](https://console.bywa.art/clientarea.php?action=productdetails&id=97175).
