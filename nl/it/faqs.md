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

# FAQ
Le seguenti sono le FAQ (frequently asked question) quando si utilizza il firewall FortiGate Security Appliance 1g.

## Cosa è un firewall?

Un firewall è un dispositivo di rete collegato in upstream da un server. Il firewall blocca il traffico non desiderato da un server prima che venga raggiunto.

## Perché dovrei utilizzare un firewall?

Il vantaggio principale di avere un firewall è che il tuo server deve gestire solo il traffico “buono” – questo significa che la tua risorsa viene utilizzata solamente per lo scopo previsto invece di gestire anche il traffico non desiderato.

## Quali prodotti firewall offre IBM?
Puoi trovare un confronto dettagliato di tutti i prodotti firewall offerti in IBM Cloud controllando questo [argomento ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://console.bluemix.net/docs/infrastructure/fortigate-10g/explore-firewalls.html#explore-firewalls){: new_window}. 

## L'Hardware Firewall (Dedicated) è compatibile con i prodotti del programma di bilanciamento del carico di IBM?

Sì. L'Hardware Firewall (Dedicated) è compatibile con i programmi di bilanciamento del carico dedicato e standard, nonché Citrix Netscaler VPX e MPX.

## Posso avere un firewall hardware dedicato e un gateway di rete associati alla stessa VLAN?

No, non è possibile avere un servizio firewall (condiviso o dedicato) e un dispositivo gateway di rete assegnati alla stessa VLAN. 

## Il traffico pubblico passa prima nel mio programma di bilanciamento del carico o nell'Hardware Firewall?

Per il traffico proveniente da internet pubblico, i prodotti dei programmi di bilanciamento del carico aziendale o dedicato e locale vengono prima, i prodotti Hardware Firewall vengono dopo e i prodotti NetScaler vengono per ultimi (insieme ai server dei clienti).

## SoftLayer effettua un addebito per la larghezza di banda del firewall?

L'Hardware Firewall (Shared), l'Hardware Firewall (Dedicated) e FortiGate Security Appliance non vengono misurati per la larghezza di banda.  In aggiunta, questi prodotti possono ridurre l'utilizzo della larghezza di banda totale limitando il traffico a cui devono rispondere i server.

## Cosa sono le porte in grigio nel mio firewall Windows?

SoftLayer offre molti servizi differenti che puoi utilizzare con il tuo server, inclusi il monitoraggio Nagios, SNMP e Evault. Questi servizi richiedono che i tuoi sistemi interni comunichino con il tuo server in qualche modo. Le porte in grigio che vedi nell'elenco delle eccezioni sono porte aperte solo nella porta di rete interna. Rimangono ancora bloccate nella connessione di rete (internet) pubblica. Poiché la rete interna è una rete protetta, avere queste porte aperte viene considerato sicuro.

Queste porte generalmente non possono essere modificate, tuttavia se reimposti le regole del firewall, le eliminerà dall'elenco delle eccezioni. Tieni presente che reimpostando le regole del firewall potresti avere un impatto negativo non solo su questi servizi aggiuntivi ma puoi anche causare altri problemi a seconda della tua configurazione del server corrente.

## Quali opzioni dell'Hardware Firewall sono disponibili per i server 10Gbps?

Se 10Gbps è necessario solo per la rete privata (per il database, il backup, l'archiviazione, ecc), i clienti possono richiedere un downgrade di soltanto i propri uplink pubblici e ordinare un qualsiasi prodotto Hardware Firewall. Se 10Gbps è necessario nella rete pubblica, è necessario un gateway di rete o il Fortigate Security Appliance 10Gbps.

## Quali intervalli di IP consento tramite il firewall?

Per l'elenco degli indirizzi IP e di intervalli di IP da consentire tramite il firewall, vai [qui](ips.html). 

## Qual è il numero massimo di server che l'Hardware Firewall (Dedicated) o il Fortigate Security Appliance proteggerà?

Sia l'Hardware Firewall (Dedicated) che il Fortigate Security Appliance possono proteggere tutti i server in una VLAN pubblica.  Tuttavia è importante notare che poiché questi dispositivi FW sono collegati con uplink a 2Gbps Uplink, consigliamo di ridimensionare il numero di istanze firewall che soddisfano i requisiti delle prestazioni della tua applicazione. I clienti possono far ciò in modo semplice distribuendo ulteriori firewall della VLAN pubblica in un pod per consentire l'aggiunta di ulteriori firewall e risorse di calcolo associate.

## Quali opzioni VPN sono incluse con ogni prodotto firewall?

Non tutti i firewall offrono la VPN e non tutte le opzioni VPN sono uguali.  Le opzioni generali della VPN sono:

* Ogni cliente riceve connessioni VPN SSL illimitate alla nostra rete privata. Queste connessioni possono essere stabilite facendo clic sul link della VPN all'inizio della pagina quando si ha eseguito l'accesso al portale del cliente.
* I clienti ricevono inoltre una VPN PPTP per account. Possono aggiungere ulteriori utenti VPN PPTP ai propri account in pacchetti di 5 per ulteriori 5$/mese.
* SoftLayer offre inoltre un servizio VPN IPSec a più tenant di base a partire da 99$/mese.
* Il FortiGate Security Appliance fornisce le opzioni VPN SSL e IPSec con l'accesso solo alla rete pubblica (nessun accesso alla rete privata SoftLayer).
* Il gateway di rete fornisce le funzionalità SSL, IPSec e OpenVPN nella rete privata o pubblica
* I prodotti NetScaler possono fornire la VPN SSL e IPSec nella rete privata o pubblica.
* I clienti possono inoltre distribuire una soluzione VPN nel server all'interno del loro ambiente SoftLayer.

## Quando seleziono l'opzione dell'elevata disponibilità per l'Hardware Firewall (Dedicated) o per il Fortigate Security Appliance, quale procedura devo seguire per utilizzare questa funzione?

Nessuno. Quando ordinato con HA, SoftLayer esegue automaticamente il provisioning delle applicazioni nella configurazione HA.  Nel caso in cui il dispositivo primario abbia un malfunzionamento, un dispositivo passivo secondario prende il posto dell'istanza attiva primaria e inizia a passare il traffico.  Mentre questo failover è normalmente automatico, è una procedura consigliata monitorare i server e assicurarsi che il traffico venga trasmesso correttamente.

## Quali prodotti firewall supportano il NAT da pubblico a privato e/o la segmentazione della VLAN privata?

Fortigate Security Appliance 10Gbps supporta il NAT da pubblico a privato e la segmentazione della VLAN privata. 
