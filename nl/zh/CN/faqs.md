---

copyright:
  years: 2017
lastupdated: "2017-10-30"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# 常见问题及解答
以下是使用 Fortigate Security Appliance 1g 防火墙时的常见问题。

## 什么是防火墙？

防火墙是服务器所连接的上游网络设备。防火墙用于阻止不需要的流量到达服务器。

## 为何应该使用防火墙？

部署防火墙的主要优势在于，服务器仅需要处理“好”流量，这表示您的资源仅用于预期目的，而不是处理不需要的流量。

## IBM 提供哪些防火墙产品？
您可以通过查看此[主题 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://console.bluemix.net/docs/infrastructure/fortigate-10g/explore-firewalls.html#explore-firewalls){: new_window}，找到 IBM Cloud 中提供的所有防火墙产品的详细对比。 

## 硬件防火墙（专用）是否与 IBM 的负载均衡器产品兼容？

是。 硬件防火墙（专用）与标准和专用负载均衡器（Citrix Netscaler VPX 和 MPX）兼容。

## 可以将专用硬件防火墙和网关与相同 VLAN 关联吗？

不可以，无法将硬件防火墙（共享或专用）和网关设备分配给相同 VLAN。 

## 公用流量是首先通过负载均衡器还是硬件防火墙？

来自公共因特网的流量首先会通过本地负载均衡、专用负载均衡器或企业负载均衡器，然后通过硬件防火墙产品，最后通过 NetScaler 产品（以及客户服务器）。

## SoftLayer 是否针对防火墙带宽收费？

硬件防火墙（共享）、硬件防火墙（专用）和 Fortigate Security Appliance 不占用带宽。而且，这些产品可通过限制服务器必须响应的流量降低总带宽利用率。

## 我的 Windows 防火墙上的哪些端口处于灰显状态？

SoftLayer 提供很多不同服务，可用于诸如 Evault、SNMP 和 Nagios 监控的服务器。这些服务需要内部系统与服务器在一定程度上进行通信。“异常”列表中的灰显端口为仅在内部网络端口上打开的端口。这些端口在公共（因特网）网络连接上也被阻止。由于内部网络是安全网络，打开这些端口可确保网络安全。

通常，无法修改这些端口；但是，如果重置防火墙规则，会从“异常”列表清除这些端口。请注意，重置防火墙规则不仅可能会对这些额外的服务产生负面影响，根据服务器配置，还可能会导致其他问题。

## 哪些硬件防火墙选项适用于 10Gbps 服务器？

如果仅在专用网络（针对数据库、备份和存储等）上需要 10Gbps，那么客户可仅请求降级其公共上行链路，并订购任何硬件防火墙产品。如果公共网络上需要 10Gbps，那么需要网关或 Fortigate Security Appliance 10Gbps。

## 我允许哪些 IP 范围通过防火墙？

有关允许通过防火墙的 IP 地址和 IP 范围的列表，请转至[此处](ips.html)。 

## 硬件防火墙（专用）或 Fortigate Security Appliance 可保护的最大服务器数量是多少？

专用硬件防火墙和 Fortigate Security Appliance 都可保护公共 VLAN 上的每台服务器。但是，请务必注意，由于这些防火墙设备通过 2Gbps 上行链路，我们建议扩展防火墙实例数以满足应用程序的性能需求。客户只需通过在生产环境中部署更多公共 VLAN 防火墙以允许添加更多防火墙和关联计算资源来实现此目的。

## 每个防火墙产品提供了哪些 VPN 选项？

不是所有的防火墙都提供 VPN，也不是所有的 VPN 选项都相同。VPN 的常规选项为：

* 每个客户收到专用网络的不受限制的 SSL VPN 连接。可以在登录到客户门户网站时单击页面顶部的 VPN 链路来建立这些连接。
* 针对每个帐户，客户还会收到一个 PPTP VPN。客户可以向其帐户成批添加更多 PPTP VPN 用户，每个月添加 5 个用户额外收取 5 美元。
* SoftLayer 还提供基本多租户 IPSec VPN 服务，最低每月 99 美元。

* Fortigate Security Appliance 提供 SSL 和 IPSec VPN 选项且仅允许访问公共网络（无法访问 IBM Cloud 专用网络）。
* 网关提供公共或专用网络上的 SSL、IPSec 和 OpenVPN 功能。
* NetScaler 产品可提供公共或专用网络上的 SSL 和 IPSec VPN。
* 客户还可在其 SoftLayer 环境中将 VPN 解决方案部署到服务器上。

## 在为硬件防火墙（专用）或 Fortigate Security Appliance 选择“高可用性”选项时，需要执行哪些步骤以利用此功能？

无。在 HA 中订购后，SoftLayer 会自动以 HA 配置供应设备。如果主设备发生故障，那么辅助备用设备会接管主活动实例，并开始传递流量。虽然此故障转移是自动的，但是最好监视服务器并确保成功传递流量。

## 哪些防火墙产品支持公用到专用 NAT 和/或专用 VLAN 分段？

Fortigate Security Appliance 10Gbps 支持公共到专用 NAT 和专用 VLAN 分段。 
