---
authors: 
- "Matthew Lamont"
categories:
- Introduction to Computers
- Windows
date: "2018-08-11T18:02:46Z"
tags:
- Command Line
- ipconfig
- Maintenance
- Windows
title: ipconfig | A Guide
aliases:
  - /ipconfig-a-guide/
slug: /ipconfig-a-guide/
---

Sometimes we need to know our IP Address or troubleshoot internet connection issues. How do we do that? Well we have a handy tool built into Windows, ipconfig.

{{< figure src="./img/ipconfig.png" alt="Image: ipconfig">}}

ipconfig is a Windows command line utility and network troubleshooting tool. To access it you just need to open the windows command line by pressing start and typing in cmd.

ipconfig has many arguments and follows the syntax:

```
ipconfig /argument
```
## Arguments

Many command line programs can be given additional options called arguments. These arguments usually start with a /. Here is a list of all the arguments that ipconfig has:

| Argument                   | Description                                                   |
|----------------------------|---------------------------------------------------------------|
| /?                         | Displays Help File                                            |
| /all                       | Display full configuration information                        |
| /release /release6         | Release the IP address for IPv4/IPv6 for specified adapter   |
| /renew /renew6             | Renew the IPv4/IPv6 address for the specified adapter        |
| /flushdns                  | Purges the DNS Resolver cache                                 |
| /registerdns               | Refreshes all DHCP leases and re-registers DNS names          |
| /displaydns                | Display the contents of the DNS Resolver Cache                |
| /showclassid /showclassid6 | Displays all the IPv4/IPv6 dhcp class IDs allowed for adapter |
| /setclassid /setclassid6   | Modifies the IPv4/IPv6 DHCP class id                          |

With these commands you can find a lot out about your wireless and wireless connections. A lot of connectivity issues can be fixed simply by using /renew and /flushdns.

We will continue to cover command line programs in the future.