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

# Aggiunta di un Hardware Firewall (Dedicated) a una VLAN pubblica
{: #adding-a-hardware-firewall-dedicated-to-a-public-vlan}

Un Hardware Firewall (Dedicated) non può essere ordinato come parte di un ordine del server e deve essere inserito dopo che viene stabilito almeno un nodo di calcolo pubblico e che sia stata aggiunta la VLAN associata.

Per aggiungere la protezione a una VLAN, ordina un Hardware Firewall (Dedicated) dalla pagina delle VLAN:

1. Dal tuo browser, apri [Customer Portal ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window} e accedi al tuo account.
2. Nella navigazione del portale del cliente, seleziona **Network > IP Management > VLANs** per andare alla pagina delle VLAN. Ogni riga rappresenta una VLAN nella tua infrastruttura. IBM© Cloud popola le informazioni "VLAN Number" e "Primary Router" automaticamente, indicando il numero VLAN reale e il router su cui è configurata. Il campo "Name" può essere utilizzato per definire un nome riconoscibile. La colonna all'estrema destra "Gateway/Firewall" contiene i dettagli, se presenti, su quale protezione firewall è in uso. 

	**Suggerimento:** per filtrare la tabella delle VLAN in modo che mostri solo le VLAN pubbliche, fai clic sulla scheda **Filter**, immetti "fcr" nel campo Primary Router e fai clic sul pulsante **Filter**.
3. Trova la VLAN che vuoi proteggere e fai clic sul link **Add Firewall** nella stessa riga. Questo link apre la pagina **Order Hardware Firewall (Dedicated)**. Se la colonna "Gateway/Firewall" è già popolata, un firewall o un gateway di rete è già associato alla VLAN e il dispositivo deve essere rimosso prima che puoi continuare.
4. Seleziona **Hardware Firewall (Dedicated)** o **Hardware Firewall (High Availability)**. 

	L'opzione dell'elevata disponibilità distribuisce gli stessi hardware e interfaccia, ma anche un secondo nodo passivo per continuare con l'elaborazione del traffico se il nodo attivo ha un malfunzionamento. L'elevata disponibilità riduce il rischio di un eccessivo tempo di inattività. 

5. Fai clic sul pulsante **Servers on this VLAN** per verificare se stai selezionando la VLAN appropriata.
6. Immetti la tua scelta di pagamento e fai clic su **Continue**.
7. Nella schermata successiva, immetti i codici promozionali se applicabili, leggi e accetta il Master Service Agreement e fai clic su **Place Order**. 
