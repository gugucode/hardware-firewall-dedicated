---

copyright:
  years: 2017,2018
lastupdated: "2018-11-30"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# 查看您的 IBM 防火墙
{: #viewing-your-ibm-firewalls}

要查看哪些 VLAN 受防火墙保护以及了解有关单个防火墙的更多详细信息，请转至 VLAN 页面：

1. 从浏览器，打开[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/){: new_window}，并登录到帐户。
2. 在“客户门户网站”导航中，选择**网络 > IP 管理 > VLAN**。

表中每行表示基础架构中的一个 VLAN。IBM© Cloud 会自动填充“VLAN 编号”和“主路由器”信息，以指示真实 VLAN 编号以及在其上配置 VLAN 的路由器。“名称”字段可用于为 VLAN 指定可识别的名称（例如，DMZ、内部网、公共或数据库）。

最右边的列“网关/防火墙”包含有关所设置的防火墙保护的详细信息，例如：

- **添加防火墙**指示没有针对此 VLAN 上的服务器设置防火墙。
- **单独保护的服务器**指示一个或多个服务器正在利用 Hardware Firewall (Shared)，且没有设置 Hardware Firewall、FortiGate Security Appliance 或网关。无法在具有单独保护的服务器的 VLAN 上设置 VLAN 防火墙和网关。
- **Firewall-vlanXXXX.networklayer.com** 指示设置了 Hardware Firewall (Dedicated) 或 FortiGate Security Appliance。仅可以将一个 VLAN 防火墙或网关与 VLAN 关联，但服务器可以在公用 VLAN 上通过 VLAN 防火墙进行保护，并可以在专用网络上与网关相关联。
- **网关名称**指示 VLAN 与该网关相关联。

## 单独保护的服务器详细信息

针对在“网关/防火墙”字段中具有**单独保护的服务器**的 VLAN，可以单击关联的 VLAN 编号链接以显示此 VLAN 的详细信息，包括关联的设备。

在关联设备的列表中，可以单击每个设备，并滚动到“配置”选项卡的底部。将在“附加组件”部分中看到状态为**已安装**或**未安装**的**防火墙**。

- **未安装**指示没有针对此设备设置防火墙。
- **已安装**指示设置了防火墙。设备上将显示**防火墙**选项卡，可在其中管理防火墙配置。

## 专用防火墙详细信息

针对在“网关/防火墙”字段中具有 **Firewall-vlanXXXX.networklayer.com** 的 VLAN，可以单击该防火墙链接以显示防火墙的详细信息。设备详细信息包括关联路由器、VLAN、IPv4/IPv6 子网、与该 VLAN 关联的设备以及针对通过或绕过防火墙路由流量的控制。

FortiGate Security Appliance 设备将具有管理 IP、用户名和密码。FortiGate Security Appliance 的管理通过其基于 GUI 或 SSH 的控制台完成。

## 网关详细信息

针对在“网关/防火墙”字段中具有网关设备名称的 VLAN，可以单击网关名称以显示网关的详细信息。设备详细信息包括关联前端 (FCR) 和后端 (BCR) VLAN 以及网关管理选项。
