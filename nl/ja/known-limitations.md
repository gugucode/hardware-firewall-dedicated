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

# 既知の制限
ハードウェア・ファイアウォール (専用) には、以下の既知の制限があります。

* ARP の処理方法が原因で、Windows ネットワーク負荷分散 (NLB) とは互換性がありません。

* 高可用性のフェイルオーバー機能はユーザーに公開されません。マスター・ファイアウォールが誤動作するが自動的にフェイルオーバーしない場合は、サポート・チケットが必要になります。ファイアウォールが適切にトラフィックを受け渡していることを確認できるように、重要なサービスに関してデバイスをモニタリングすることが推奨されます。

* 現在ネットワーク・ゲートウェイ、ハードウェア・ファイアウォール、または Fortigate Security Appliance が関連付けられている VLAN 上には、ハードウェア・ファイアウォール (専用) を配備できません。
