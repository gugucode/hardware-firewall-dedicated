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
{:faq: data-hd-content-type='faq'}

# 常見問題
在使用 Fortigate Security Appliance 1g 防火牆時，下列是常見問題。

## 何謂防火牆？
{:faq}

防火牆是一個從伺服器上游連接的網路裝置。抵達伺服器之前，防火牆會封鎖來自伺服器不必要的資料流量。

## 為何應該使用防火牆？
{:faq}

具有防火牆的主要優點在於您的伺服器只需處理「良好」的資料流量 - 這表示您的資源僅用於其預期目的，而非處理不必要的資料流量。

## IBM 提供哪些防火牆產品？
{:faq}

透過檢閱此
[ 主題
![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](/docs/infrastructure/fortigate-10g/explore-firewalls.html#explore-firewalls){: new_window}，您可以找到
IBM Cloud 中提供的所有防火牆產品的詳細比較。 

## Hardware Firewall (Dedicated) 是否與 IBM 負載平衡器產品相容？
{:faq}

是。Hardware Firewall (Dedicated) 與標準及專用的負載平衡器、Citrix Netscaler VPX 及 MPX 相容。

## 我可以擁有專用硬體防火牆以及與同一個 VLAN 相關聯的「網路閘道」嗎？
{:faq}

不可以，無法將防火牆服務（共用或專用）及「網路匣道」裝置指派到相同的 VLAN。 

## 公用資料流量是否會先通過負載平衡器或 Hardware Firewall？
{:faq}

從公用網際網路中進入，首先會經過本端的負載平衡器、專用負載平衡器或企業負載平衡器產品，然後是 Hardware Firewall 產品，最後則是 NetScaler 產品（與客戶伺服器一起）。

## SoftLayer 是否收取防火牆頻寬費用？
{:faq}

Hardware Firewall (Shared)、Hardware Firewall (Dedicated) 及 Fortigate Security Appliance 不針對頻寬進行計量。此外，這些產品還可以透過限制伺服器必須回應的資料流量來減少總頻寬使用率。

## 在 Windows 防火牆中變灰的連接埠為何？
{:faq}

SoftLayer 提供許多不同的服務，讓您可以使用包括 Evault、SNMP 及 Nagios 監視的伺服器。這些服務要求我們的內部系統在一定程度上與您的伺服器通訊。您在「異常狀況」清單中看到變成灰色的連接埠是僅在內部網路埠上開啟的連接埠。仍在公用（網際網路）網路連線上封鎖他們。由於內部網路是安全網路，因此開啟這些連接埠被認為是安全的。

通常無法修改這些連接埠，但是如果您重設防火牆規則，將會從「異常狀況」清單中清除這些連接埠。請注意，重設防火牆規則不僅會對這些額外的服務產生不利影響，還會導致伺服器出現其他問題，而這些都會根據其目前配置而定。

## 哪些 Hardware Firewall 選項適用於 10Gbps 伺服器？
{:faq}

如果只有專用網路需要 10Gbps（用於資料庫、備份、儲存等等），則客戶可以僅針對其公用上行鏈路要求降級，並訂購任何一種 Hardware Firewall 產品。如果公用網路需要 10Gbps，則需要「網路閘道」或 Fortigate Security Appliance 10Gbps。

## 哪些 IP 範圍容許通過防火牆？
{:faq}

如需容許通過防火牆的 IP 位址及 IP 範圍清單，請前往[這裡](ips.html)。 

##  Hardware Firewall (Dedicated) 或 Fortigate Security Appliance 將保護的伺服器數目上限為何？
{:faq}

Hardware Firewall (Dedicated) 與 Fortigate Security Appliance 在公用 VLAN 上可以保護每一台伺服器。但是，需要注意的是 FW 裝置連接 2Gbps 上行鏈路，因此我們建議調整防火牆實例的數量以滿足您的應用程式效能需求。客戶可以簡易地透過在 pod 內部署其他公用 VLAN 防火牆來達成此目的，以容許新增其他的防火牆及相關聯的計算資源。

## 每一個防火牆產品隨附哪些 VPN 選項？
{:faq}

不是所有防火牆都提供 VPN，且不是所有 VPN 選項都相同。VPN 的一般選項為：

* 每一個客戶可以透過我們的專用網路接收無限制的 SSL VPN 連線。登入客戶入口網站時，透過按一下頁面頂端的 VPN 鏈結，可以建立這些連線。
* 客戶的每個帳戶都會收到一個 PPTP VPN。他們可以將其他 PPTP VPN 使用者新增至其帳戶，每新增一個 PPTV VPN 使用者以每個月 5 美元的額外套件價格收取費用。
* SoftLayer 還提供基本的多方承租戶 IPSec VPN 服務，起始價為每個月 99 美元。
* Fortigate Security Appliance 提供 SSL 及 IPSec VPN 選項，僅限於「公用」網路存取（無法存取 SoftLayer 專用網路）。
* 「網路閘道」在公用或專用網路上提供 SSL、IPSec 及 OpenVPN 功能。
* NetScaler 產品在公用或專用網路上可以提供 SSL 及 IPSec VPN。
* 客戶還可以將 VPN 解決方案部署至其 SoftLayer 環境內的伺服器。

## 選取 Hardware Firewall (Dedicated) 或 Fortigate Security Appliance 的「高可用性」選項時，需要採取哪些步驟來運用此特性？
{:faq}

無。當訂購 HA 後，SoftLayer 會自動佈建 HA 配置中的應用裝置。如果主要裝置失敗，次要被動裝置將接管主要作用中的實例，並且開始傳輸資料流量。雖然這種失效接手通常是自動的，但最佳作法是監視伺服器並且確保資料流量順利通過。

## 哪些防火牆產品支援公用到專用 NAT 及/或專用 VLAN 區段？
{:faq}

Fortigate Security Appliance 10Gbps 支援公用到專用 NAT 以及專用 VLAN 區段。 
