---

copyright:
  years: 2017,2018
lastupdated: "2018-01-19"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Eine Hardware-Firewall (dediziert) zu einem öffentlichen VLAN hinzufügen

Eine Hardware-Firewall (dediziert) kann nicht als Teil einer Serverbestellung bestellt werden. Die Bestellung muss aufgegeben werden, nachdem mindestens ein öffentlicher Rechenknoten eingerichtet und das zugehörige VLAN hinzugefügt wurden.

Um einen Schutz zu einem VLAN hinzuzufügen, bestellen Sie eine Hardware-Firewall (dediziert) auf der VLAN-Seite:

1. Öffnen Sie im Browser das [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window} und melden Sie sich bei Ihrem Konto an.
2. Wählen Sie in der Navigation des Kundenportals **Netz > IP-Verwaltung > VLANs** aus und gehen Sie zur Seite "VLANs". Jede Zeile stellt ein VLAN in Ihrer Infrastruktur dar. IBM Cloud gibt die Informationen für "VLAN-Nummer" und "Primärer Router" automatisch ein. Dabei werden die echte VLAN-Nummer und der Router angegeben, auf die sie konfiguriert ist. Das Feld "Name" kann verwendet werden, um für das VLAN einen erkennbaren Namen zu definieren. Die rechte Spalte "Gateway/Firewall" enthält Details über den implementierten Firewallschutz (wenn vorhanden). Beispiel: 

	**Tipp:** Um die VLANs-Tabelle so zu filtern, dass nur öffentliche VLANs angezeigt werden, klicken Sie auf die Registerkarte **Filtern**, geben Sie "fcr" in das Feld für den primären Router ein und klicken Sie auf die Schaltfläche **Filtern**.
3. Suchen Sie das VLAN, das Sie schützen möchten, und klicken Sie auf den Link **Firewall hinzufügen** in derselben Zeile. Über diesen Link öffnet sich die Seite **Hardware-Firewall (dediziert) bestellen**. Wenn die Spalte "Gateway/Firewall" bereits ausgefüllt ist, ist dem VLAN bereits eine Firewall oder ein Netzgateway zugeordnet. Das Gerät muss entfernt werden, bevor Sie fortfahren können.
4. Wählen Sie **Hardware Firewall (dediziert)** oder **Hardware-Firewall (Hochverfügbarkeit)** aus. 

	Die Hochverfügbarkeitsoption implementiert dieselbe Hardware und Schnittstelle, stellt jedoch einen zweiten passiven Knoten bereit, um die Verarbeitung des Datenverkehrs fortzusetzen, wenn der aktive Knoten ausfällt. Die Hochverfügbarkeit reduziert das Risiko von längeren Ausfallzeiten. 

5. Klicken Sie auf die Schaltfläche **Server in diesem VLAN**, um zu überprüfen, ob das richtige VLAN ausgewählt wurde.
6. Geben Sie Ihre gewünschte Zahlungsart ein und klicken Sie auf **Weiter**.
7. Geben Sie auf dem nächsten Bildschirm die Werbeaktionscodes (wenn vorhanden) ein, lesen Sie die Rahmenvereinbarung und stimmen Sie ihr zu. Klicken Sie dann auf **Bestellen**. 
