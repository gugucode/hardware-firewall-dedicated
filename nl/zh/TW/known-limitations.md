---

copyright:
  years: 2017
lastupdated: "2018-11-30"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# 已知的限制
Hardware Firewall (Dedicated) 具有下列的已知限制：

* 因為處理 ARP 的方式，與 Windows Network Load Balancing (NLB) 不相容

* 不向使用者公開高可用性失效接手的功能。如果主防火牆發生故障，不會自動進行失效接手，需要填寫支援問題單。建議對重要服務進行裝置監視，以確保防火牆正確地傳輸資料流量。

* 無法在目前與網路匣道、Hardware Firewall 或 Fortigate Security Appliance 相關聯的 VLAN 上部署 Hardware Firewall (Dedicated)。
