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

# 将 Hardware Firewall (Dedicated) 添加到公用 VLAN
{: #adding-a-hardware-firewall-dedicated-to-a-public-vlan}

无法将 Hardware Firewall (Dedicated) 作为服务器订单的一部分进行订购，必须在建立了至少一个公共计算节点和添加了关联 VLAN 后，才能下单。

要向 VLAN 添加保护，请从 VLAN 页面订购 Hardware Firewall (Dedicated)：

1. 从浏览器，打开[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/){: new_window}，并登录到帐户。
2. 在“客户门户网站”导航中，选择**网络 > IP 管理 > VLAN**，以转至 VLAN 页面。每行表示基础架构中的一个 VLAN。IBM© Cloud 会自动填充“VLAN 编号”和“主路由器”信息，以指示真实 VLAN 编号以及在其上配置 VLAN 的路由器。可以使用“名称”字段定义可识别名称。最右边的列“网关/防火墙”包含有关为该 VLAN 设置的任何防火墙保护（如有）的详细信息。 

	**提示：**要过滤 VLAN 表以仅显示公用 VLAN，请单击**过滤**选项卡，并在“主路由器”字段中输入“fcr”，然后单击**过滤**按钮。
3. 找到要保护的 VLAN，并单击相同行中的**添加防火墙**链接。此链接将打开**订购 Hardware Firewall (Dedicated)**页面。如果已填充“网关/防火墙”列，那么防火墙或网关已与 VLAN 关联，必须先除去设备，才可继续。
4. 选择 **Hardware Firewall (Dedicated)** 或 **Hardware Firewall（高可用性）**。 

	“高可用性”选项部署相同硬件和接口，但会部署另一个被动节点以在主动节点发生故障的情况下继续处理流量。“高可用性”降低停机时间过长的风险。 

5. 单击**此 VLAN 上的服务器**按钮以验证是否选择了合适的 VLAN。
6. 输入支付选项，并单击**继续**。
7. 在下一个屏幕中，输入促销代码（如果适用），阅读并同意“主服务协议”，然后单击**下订单**。 
