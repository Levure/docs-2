---
title: FAQ
excerpt: FAQ per le istanze Public Cloud OVHcloud
slug: public-cloud-faq
section: 'Per iniziare'
order: 3
---

> [!primary]
> Questa traduzione è stata generata automaticamente dal nostro partner SYSTRAN. I contenuti potrebbero presentare imprecisioni, ad esempio la nomenclatura dei pulsanti o alcuni dettagli tecnici. In caso di dubbi consigliamo di fare riferimento alla versione inglese o francese della guida. Per aiutarci a migliorare questa traduzione, utilizza il pulsante "Modifica" di questa pagina.
>

**Ultimo aggiornamento: 06/09/2021**

## FAQ Public Cloud

### Come connettersi a un'istanza Public Cloud?

La connessione avviene tramite una coppia di chiavi SSH da configurare durante la creazione dell'istanza Public Cloud.

Per effettuare questa operazione, consulta la guida [Creare e connettersi a un’istanza Public Cloud](../primi-passi-public-cloud/).

### Ho perso o voglio cambiare la mia chiave SSH, come fare?

Se non riesci più a connetterti in seguito alla perdita della chiave privata, modifica la chiave pubblica della tua istanza passando in modalità Rescue.

In caso di perdita, consulta la guida [Sostituisci la tua chiave SSH in caso di perdita](../sostituisci_la_tua_chiave_ssh_in_caso_di_perdita/).

### Quali sono le possibilità di backup della tua istanza?

Dallo Spazio Cliente OVHcloud è possibile creare il backup di un'istanza in qualsiasi momento. che permette di ripristinare l'istanza su una configurazione precedente o di poterla ricreare.

Per eseguire questa operazione, consulta la guida [Effettuare lo Snapshot di un’istanza](../effettuare-snapshot-di-un-istanza/).

### Come creare e gestire gli utenti OpenStack?  

Per utilizzare le API Horizon o OpenStack, è necessario creare un utente OpenStack. È possibile crearne un numero illimitato.

Per effettuare questa operazione, consulta la guida [Creare e rimuovere un utente OpenStack](../creation-and-deletion-of-openstack-user/).

### Come funziona la fatturazione del Public Cloud?

La fatturazione dei tuoi consumi avviene tra il 1° e il 5° giorno del mese successivo al periodo di utilizzo. In caso di tariffazione mensile, il forfait del mese successivo viene fatturato insieme agli eventuali costi aggiuntivi del mese precedente (istanze, Object Storage). Se passi alla tariffa mensile nel corso del mese, il prorata temporis per il mese in corso viene addebitato immediatamente.
Ti ricordiamo che tutte le istanze vengono fatturate fino a quando non vengono eliminate dallo Spazio Cliente OVHcloud.
Per monitorare i consumi in modo ancora più preciso, è possibile affidarsi alle proiezioni elaborate sulla base dei consumi precedenti oppure applicare una fatturazione differente ai diversi progetti Public Cloud, in modo da gestire al meglio le spese della tua azienda.

Per passare da una modalità di fatturazione all'altra, consulta la nostra guida [Passare dalla fatturazione oraria a quella mensile](../cambiare-tipo-fatturazione-public-cloud/).

### Come aggiungere o rimuovere risorse alle istanze?

Tutte le istanze possono essere scalate verso una gamma superiore dalla stessa gamma dallo Spazio Cliente, cliccando su `Modifica`{.action} nella pagina dell'istanza. Se lanciata con l'opzione "flex", è possibile ridimensionarla verso un modello inferiore. Questa opzione richiede una dimensione disco di 50 GB per tutti i modelli e permette quindi il ridimensionamento in entrambe le direzioni.
In tutti i casi, il ridimensionamento di un'istanza comporta il riavvio.

### Le istanze Public Cloud sono compatibili con cloud-init?

Sì, le immagini Cloud fornite da OVHcloud includono gli script cloud-init che permettono di personalizzare le istanze all'avvio. L'infrastruttura fornisce le informazioni di personalizzazione dell'istanza tramite un server di metadati contattato direttamente da cloud-init.

### È possibile effettuare un backup dei server Public Cloud?

Sì, è possibile creare Instance Backup dei server in qualsiasi momento e senza limiti.  Questi backup sono salvati e fatturati allo stesso modo delle immagini contenute in "Private Image". Le API OpenStack permettono di scaricarle al di fuori dell'infrastruttura OVHcloud o su altri progetti.

Per eseguire questa operazione, consulta la guida [Effettuare lo Snapshot di un’istanza](../effettuare-snapshot-di-un-istanza/).

### È possibile aumentare la dimensione di un volume in modo dinamico, continuando a scrivere sul disco?

No, per poter aumentare la dimensione di un volume è necessario scollegarlo.

### C'è un numero massimo di volumi aggiuntivi associabili alle istanze?

Sì, a ogni istanza si può associare un massimo di 26 volumi aggiuntivi.

### In che modo vengono protetti i server?

OVHcloud protegge l'intera infrastruttura grazie alla sua soluzione anti-DDoS esclusiva. a cui è possibile aggiungere gruppi di sicurezza OpenStack: equiparabili a un firewall, sono gestiti direttamente a livello dell’infrastruttura OpenStack, a monte delle istanze.

Per maggiori informazioni, consulta la guida [Creare e configurare un gruppo di sicurezza su Horizon](../configura_un_gruppo_di_sicurezza/).

Queste protezioni, combinate alle ulteriori misure che puoi adottare sulle macchine, consentono di ottimizzare l’affidabilità dei deploy effettuati.

### Come creare una rete privata tra server?

Il Public Cloud integra una soluzione SDN (Software-defined Network) che permette di creare reti private in modo dinamico e connetterle alle istanze tramite lo Spazio Cliente o tramite l'API.
Queste reti private sono basate sulla tecnologia vRack di OVHcloud comune agli altri servizi della società, come Private Cloud o i server dedicati. In questo modo è possibile far comunicare in modo isolato e sicuro tutti gli elementi dell'infrastruttura OVHcloud.

Per maggiori informazioni, consulta la guida [Configurazione della vRack Public Cloud](https://docs.ovh.com/gb/en/public-cloud/public-cloud-vrack/) (EN).

### È possibile modificare l'IP pubblico della tua istanza?

Gli IP pubblici sono assegnati automaticamente alle istanze e non sono quindi modificabili. Per utilizzare il controllo dell'IP pubblico di un'istanza, ti consigliamo di utilizzare un IP Failover. In questo modo, indipendentemente dall'indirizzo pubblico assegnato automaticamente all'istanza, hai la possibilità di aggiungere uno o più IP Failover alla tua istanza.

Per maggiori informazioni, consulta la guida [Acquista un IP Failover](../acquista_un_ip_failover/).

## Per saperne di più

Contatta la nostra Community di utenti all’indirizzo <https://community.ovh.com/en/>.
