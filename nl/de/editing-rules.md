---

copyright:
  years: 2017,2018
lastupdated: "2018-01-22"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Die Hardware-Firewall (dediziert) konfigurieren

Wenn die Firewall erstmalig zum VLAN hinzugefügt wird, wird zunächst ein Regelsatz eingerichtet, mit dem der gesamte Datenverkehr durch die Firewall geleitet wird. Das Konfigurieren der Firewall ist so einfach wie das Erstellen eines Regelsatzes, der den Zugriff auf bestimmte IP-Adressen/Ports von spezifischen Internetadressen erlaubt, während der Datenverkehr aus anderen Quellen abgewiesen wird.

## Regeln bearbeiten

Gehen Sie wie folgt vor, um Firewallregeln zu bearbeiten:

1. Öffnen Sie im Browser das [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window} und melden Sie sich bei Ihrem Konto an.
2. Wählen Sie in der Navigation des Kundenportals **Netz > IP-Verwaltung > VLANs** aus. Jede Zeile stellt ein VLAN in Ihrer Infrastruktur dar.  Klicken Sie auf den Link "Firewall-vlanXXXX.networklayer.com", der dem VLAN zugeordnet wurde, das Sie verwalten möchten. Daraufhin wird die Seite **Gerätedetails** angezeigt. Stellen Sie sicher, dass der Status angibt, dass die Firewall alle Regeln verarbeitet.  Benutzer können die Regeln umgehen, wenn implementierte Regeln unbeabsichtigte Auswirkungen auf die Umgebung haben. Klicken Sie dazu in diesem Bereich auf "Regeln umgehen".
3. Um die Regeln zu aktualisieren, klicken Sie auf die Registerkarte **Regeln**. Die Seite zeigt die aktuellen Regeln für IPv4- und IPv6-Adressen an.  Wenn keine Regeln implementiert sind, wird ein ausgeblendeter Platzhalter angezeigt.  Bearbeiten Sie einzelne Regeln, indem Sie auf die entsprechende Zeile klicken.  Diese Liste aus Regeln ist auch als 'working config' (Arbeitskonfiguration) bekannt. Die 'working config' ist ein Satz von Regeln, der erstellt, aber noch nicht auf die Firewall angewendet wurde. Ein Benutzer kann so lange Regeln bearbeiten, hinzufügen und löschen, bis der Regelsatz abgeschlossen ist.  Regeln werden in der Reihenfolge angezeigt, in der sie verarbeitet werden. Regeln mit geringeren Nummern erhalten Vorrang vor Regeln mit höheren Nummern. (Wenn Regel 1 ein Paket durchlässt, werden die Regeln 2 und höher vom Paket nicht angewendet.)
4. Klicken Sie auf eine Regel, um sie zu bearbeiten, oder klicken Sie auf das Pluszeichen am Ende der Tabelle, um eine zusätzliche Regel hinzuzufügen. Beim Klicken auf das Minus-Symbol wird die Regel gelöscht. Die Regeln werden während der Eingabe automatisch validiert.

    Felder:

    **Reihenfolge:** Die Folgenummer der Regel. Regeln können mit den angezeigten Pfeilen in der Liste nach oben oder nach unten verschoben werden und werden von oben nach unten umgesetzt.

    **Aktion:** Um den Datenverkehr, der dieser Regel entspricht, zuzulassen oder abzulehnen.

    **Ziel:** Kann entweder 'alle' oder eine bestimmte IP-Adresse oder die Netzadresse für ein Teilnetz sein.

    **CIDR:** Gibt die Standard-CIDR-Notation für die ausgewählte Quelle an.  Mit "32" wird die Regel für eine einzelne IP-Adresse implementiert, und beispielsweise mit "24" wird die Regel für 256 IP-Adressen implementiert.

    **Quelle:** Kann entweder 'alle' oder eine bestimmte IP-Adresse oder die Netzadresse für ein Teilnetz sein.

    **CIDR:** Gibt die Standard-CIDR-Notation für das ausgewählte Ziel an.

    **Portbereich:** Die zwei Felder geben den Bereich der Ports (zwischen 1 und 65535) an, auf die die Regel angewendet wird.

    **Protokoll:** Damit wird das Protokoll (TCP/GRE/ICMP/UDP/PPTP/AH/ESP) ausgewählt, auf das die Regel angewendet wird.

    **Anmerkungen:** Feld, um für diese Regel eine Anmerkung einzugeben.
    
5. Wenn die Arbeitskonfiguration 'working config' abgeschlossen ist, klicken Sie auf die Schaltfläche **Regeln aktualisieren**, damit die 'working config' auf die Firewall angewendet wird. Die Regeln werden innerhalb von zwei Minuten wirksam.

## Allgemeine Ports

| Protokoll | Port |
| :-----: | :-----: |
| FTP | 21 |
| SSH | 22 |
| Telnet | 23 |
| SMTP | 25 |
| DNS | 53 |
| HTTP | 80 |
| POP3 | 110 |
| IMAP | 143 |
| HTTPS | 443 |
| MSSQL | 1433 |
| MySQL | 3306 |
| Remote Desktop | 3389 |
| PostgreSQL | 5432 |
| VNC Web | 5800 |
| VNC Client | 5900 |
| Urchin | 9999 oder 10000 ||
