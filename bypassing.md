---

copyright:
  years: 2017
lastupdated: "2018-11-30"

keywords: bypass, firewall, rules,

subcollection: hardware-firewall-dedicated

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}
{:note: .note}
{:important: .important}

# Bypassing Hardware Firewall (Dedicated) Rules
{: #bypassing-hardware-firewall-dedicated-rules}

To bypass the firewall rules,

1. From your browser, open the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} and log into your account.
2. In the Customer Portal navigation, go to **Network > IP Management > VLANs** and click on the firewall device you want to bypass.
3. In the **Device Details** page, you can use the **Actions** drop down menu to choose **Set Rule Bypass** or in the **Status** section, you can click on the **Bypass Rules** button. Either way, you should get a confirmation dialog. Click **Yes** to confirm the action. Bypassing the rules takes approximately two minutes to take effect. While in bypass mode, the "Status" will be "Bypassing All Rules".

	Another option is to route around the firewall when you are doing trouble shooting or etc, you can use the **Actions** drop down menu to choose **Set Route Bypass** or in the **Status** section, you can click **Route Around**.

## Enable the Rules Again
{: #enable-the-rules-again}

To enable the rules again, follow the instructions above to reach the **Device Details** page, click on the **Actions** dropdown menu and choose **Set Route Bypass**. You will get a confirmation dialog. Click **Yes** to confirm the action. The "Status" will change back to "Routing THROUGH firewall" within two minutes.
