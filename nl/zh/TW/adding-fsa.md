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

# 將 Hardware Firewall (Dedicated) 新增至公用 VLAN

無法將 Hardware Firewall (Dedicated) 作為服務訂單的一部分訂購，必須至少在建立一個公用運算節點及新增關聯的 VLAN 後才能下訂單。

若要新增 VLAN 的保護，請從 VLAN 頁面訂購 Hardware Firewall (Dedicated)：

1. 從您的瀏覽器開啟[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/){: new_window} 並登入您的帳戶。
2. 在「客戶入口網站」導覽中，選取**網路 > IP 管理 > VLAN**，前往 VLAN 頁面。每一列代表您基礎架構中的一個 VLAN。IBM Cloud 自動移入「VLAN 號碼」及「主要的路由器」資訊，指出真實的 VLAN 號碼及其配置的路由器。可以使用「名稱」欄位定義可辨識的名稱。最右側的「閘道/防火牆」直欄包含對該 VLAN 有什麼防火牆保護準備就緒（如果有的話）的詳細資料。 

	**提示：**若要過濾 VLAN 表格，以僅顯示公用 VLAN，請按一下**過濾**標籤，在「主要的路由器」欄位輸入 "fcr"，然後按一下**過濾**按鈕。
3. 尋找您要保護的 VLAN，然後在相同列中按一下**新增防火牆**鏈結。此鏈結會開啟**訂購 Hardware Firewall (Dedicated)** 頁面。如果已移入「閘道/防火牆」直欄，則「防火牆」或「網路閘道」已與 VLAN 關聯，並且必須先移除裝置，您才能夠再繼續。
4. 選取 **Hardware Firewall (Dedicated)** 或 **Hardware Firewall（高可用性）**。 

	「高可用性」選項部署相同的硬體及介面，但如果作用中節點失敗，則部署第二個被動節點以繼續處理。「高可用性」會減少過多關閉時間的風險。 

5. 按一下**在此 VLAN 上的伺服器**按鈕，以驗證您選擇適當的 VLAN。
6. 輸入您的付款選項並按一下**繼續**。
7. 在下一個畫面中，輸入促銷代碼（如果適用），閱讀並且同意「主要服務合約」，然後按一下**下訂單**。 
