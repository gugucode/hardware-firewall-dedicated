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

# 檢視您的防火牆

若要查看哪些 VLAN 受防火牆保護，並且尋找個別防火牆的相關詳細資料，請前往 VLAN 頁面：

1. 從您的瀏覽器開啟[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/){: new_window} 並登入您的帳戶。
2. 在「客戶入口網站」導覽中，選取**網路 > IP 管理 > VLAN**。

表格中的每一列代表您基礎架構中的一個 VLAN。IBM Cloud 自動移入「VLAN 號碼」及「主要的路由器」資訊，指出真實的 VLAN 號碼及其配置的路由器。「名稱」欄位可用來提供 VLAN 一個可辨識的名稱（例如 DMZ、內部網路、公用或資料庫）。

最右側的「閘道/防火牆」直欄包含有什麼防火牆保護準備就緒的相關詳細資料，例如：

- **新增防火牆**指出此 VLAN 上的伺服器沒有防火牆準備就緒。
- **個別受保護的伺服器**指出一個以上的伺服器使用 Hardware Firewall (Shared)，而且沒有 Hardware Firewall (Dedicated)、FortiGate Security Appliance 或「網路匣道」準備就緒。VLAN 防火牆及網路閘道不能放置在具有個別保護的伺服器的 VLAN 上。
- **Firewall-vlanXXXX.networklayer.com** 指出 Hardware Firewall (Dedicated) 或 FortiGate Security Appliance 已準備就緒。僅一個 VLAN 防火牆或「網路閘道」可以與 VLAN 相關聯，但是可透過 VLAN 防火牆在公用 VLAN 上保護伺服器，並且使用「網路閘道」在專用網路上將其關聯。
- **GatewayName** 指出 VLAN 與該「網路閘道」關聯。

## 個別受保護的伺服器詳細資料

針對在「匣道/防火牆」欄位中具有**個別受保護的伺服器**的 VLAN，您可以按一下相關聯的 VLAN 號碼鏈結，以顯示 VLAN 的詳細資料（包括相關聯的裝置）。

在相關聯的裝置清單中，您可以按一下每一個裝置，並捲動至「配置」標籤底端。使用狀態的**已安裝**或**未安裝**，您將在插件區段中看到**防火牆**。

- **未安裝**指出此裝置沒有防火牆準備就緒。
- **已安裝**指出防火牆已準備就緒。將在裝置上提供**防火牆**標籤，您可以在其中管理防火牆配置。

## 專用的防火牆詳細資料

針對在「匣道/防火牆」欄位中具有 **Firewall-vlanXXXX.networklayer.com** 的 VLAN，您可以按一下該防火牆鏈結，以顯示「防火牆」的詳細資料。裝置詳細資料包括相關聯的路由器、VLAN、IPv4/IPv6 子網路、與該 VLAN 相關聯的裝置，以及經過或繞過防火牆路由資料流量的控制項。

FortiGate Security Appliance 裝置將具有管理 IP、使用者名稱及密碼。FortiGate Security Appliance 的管理已透過其擁有的 GUI 或 SSH 型主控台完成。

## 網路閘道詳細資料

針對「匣道/防火牆」欄位中具有「網路匣道」裝置名稱的 VLAN，您可以按一下「網路匣道」名稱，以顯示「網路匣道」的詳細資料。裝置詳細資料包括相關聯的前端 (FCR) 及後端 (BCR) VLAN 與「網路匣道」管理選項。
