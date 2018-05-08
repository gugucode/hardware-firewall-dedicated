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

# Configura il firewall hardware (dedicato)

Quando il firewall viene aggiunto per la prima volta alla VLAN, viene inizialmente messa in uso una serie di regole che consente tutto il traffico. La configurazione del firewall è semplice così come la creazione di una serie di regole per consentire l'accesso ad alcuni indirizzi IP/porte da indirizzi internet specifici mentre si nega il traffico da altre origini. 

## Modifica le regole 

Per modificare le regole del firewall: 

1. Dal tuo browser, apri [Customer Portal ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window} e accedi al tuo account. 
2. Nella navigazione del portale del cliente, seleziona **Network > IP Management > VLANs**. Ogni riga rappresenta una VLAN nella tua infrastruttura.  Fai clic sul link Firewall-vlanXXXX.networklayer.com associato alla VLAN che vuoi gestire per passare alla pagina **Device Details**. Assicurati che "Status" indichi che il firewall sia "Processing All Rules." Gli utenti possono scegliere di escludere le regole nel caso in cui le regole implementate abbiano un impatto non desiderato sul proprio ambiente facendo clic su "Bypass Rules" in questa area.
3. Per iniziare ad aggiornare le regole, fai clic sulla scheda **Rules**. La pagina visualizzerà le sezioni che indicano le regole correnti in vigore per gli indirizzi IPv4 e IPv6.  Se non viene implementata alcuna regola, verrà visualizzato un segnaposto sbiadito. Modifica le regole individuali facendo clic sulla riga corrispondente. Questo elenco di regole è noto come 'working config'. Un 'working config' è una serie di regole che sono in fase di creazione ma che non sono ancora state applicate al firewall. Un utente può modificare, aggiungere ed eliminare le regole finché non viene completata la serie di regole. Le regole sono visualizzate nell'ordine in cui vengono elaborate, con le regole con numeri più piccoli che hanno la precedenza su quelle con numeri più grandi (se la regola 1 consente l'attraversamento di un pacchetto, le regole da 2 in poi vengono ignorate dal pacchetto). 
4. Fai clic su una regola per modificarla o sul segno più alla fine della tabella per aggiungere una ulteriore regola. Facendo clic sull'icona meno si eliminerà la regola. Le regole sono automaticamente convalidate come le inserisci. 

    I campi sono: 

    **Order:** il numero d'ordine della regola. Le regole possono essere spostate in alto o in basso nell'elenco con le frecce fornite e sono applicate dall'inizio alla fine. 

    **Action:** 'consente' o 'nega' il traffico che corrisponde a questa regola 

    **Source:** può essere 'uno qualsiasi' o un indirizzo IP specifico o l'indirizzo di rete di una sottorete specifica.

    **CIDR** indica l'annotazione CIDR standard dell'origine selezionata. "32" implementerà la regola per un solo IP, mentre, ad esempio, "24" implementerà la regola per 256 IP. 

    **Destination:** può essere 'uno qualsiasi' o un indirizzo IP specifico o l'indirizzo di rete di una sottorete specifica.

    **CIDR** indica l'annotazione CIDR standard della destinazione selezionata. 

    **Port Range:** questi 2 campi indicano l'intervallo di porte (tra 1 e 65535) a cui sarà applicata la regola.

    **Protocol:** seleziona il protocollo a cui sarà applicata la regola (TCP/GRE/ICMP/UDP/PPTP/AH/ESP)

    **Notes:** campo per inserire qualsiasi nota riguardante questa regola.
    
5. Dopo aver completato il 'working config', premi il pulsante **Update Rules** in modo che 'working config' venga applicato al firewall. Le regole dovrebbero avere effetto in due minuti. 

## Porte comuni 

| Protocollo | Porta |
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
| Desktop remoto | 3389 |
| PostgreSQL | 5432 |
| VNC Web | 5800 |
| VNC Client | 5900 |
| Urchin | 9999 o 10000 ||
