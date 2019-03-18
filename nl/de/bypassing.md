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

# Regeln für die Hardware-Firewall (dediziert) umgehen
{: #bypassing-hardware-firewall-dedicated-rules}

Führen Sie die folgenden Schritte aus, um die Firewallregeln zu umgehen:

1. Öffnen Sie im Browser das [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window} und melden Sie sich bei Ihrem Konto an.
2. Wählen Sie in der Navigation des Kundenportals **Netz > IP-Verwaltung > VLANs** aus und klicken Sie auf das Firewallgerät, das Sie umgehen möchten.
3. Auf der Seite **Gerätedetails** können Sie über das Dropdown-Menü **Aktionen** die Option **Route-Umgehung einrichten** auswählen oder Sie können im Abschnitt **Status:** auf **Regeln umgehen** klicken.  

	Eine weitere Möglichkeit ist die Umgehung der Firewall per Routing. Sie können im Dropdown-Menü **Aktionen** die Option **Route-Umgehung einrichten** auswählen oder Sie können im Abschnitt **Status:** auf die Schaltfläche **Umgehen** klicken. Bei beiden Möglichkeiten wird ein Bestätigungsdialog angezeigt. Klicken Sie auf **Ja**, um die Aktion zu bestätigen. Die Umgehung wird in etwa zwei Minuten wirksam. Im Umgehungsmodus gibt der Status an, dass der Datenverkehr um die Firewall herum geleitet wird.

## Regeln wieder aktivieren

Wenn Sie die Regeln wieder aktivieren möchten, führen Sie die oben beschriebenen Anweisungen aus, um die Seite **Gerätedetails** aufzurufen, klicken Sie auf das Dropdown-Menü **Aktionen** und wählen Sie **Route-Umgehung einrichten** aus. Es wird ein Bestätigungsdialog angezeigt. Klicken Sie auf **Ja**, um die Aktion zu bestätigen. Der Status gibt in etwa zwei Minuten wieder an, dass der Datenverkehr DURCH die Firewall geleitet wird.
