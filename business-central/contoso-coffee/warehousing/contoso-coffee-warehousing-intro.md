---
title: Introduzione a Contoso Coffee
description: Panoramica degli scenari su come i dati demo di Contoso Coffee possono aiutarti a imparare a usare le funzionalità di magazzino in Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# Introduzione alla gestione magazzino Contoso Coffee

Contoso Coffee è un'azienda fittizia che produce caffettiere di consumo e commerciali. Le app **Contoso Coffee** per Business Central aggiungono i dati demo che puoi usare per imparare a usare le funzionalità di magazzino in Business Central. Puoi configurare le funzionalità del magazzino in vari modi, vedi [Panoramica delle diverse opzioni di configurazione](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

L'app fornisce tre ubicazioni ottimizzate per diversi scenari:

- **ARGENTO**  

  Questa ubicazione è configurata per utilizzare le collocazioni. Può essere facilmente configurata per il supporto di base o avanzato. 

- **GIALLO**  

  Questa ubicazione utilizza la configurazione avanzata del magazzino, ma non utilizza le collocazioni. Può essere riconfigurata per supportare le configurazioni di base.

- **BIANCO**  

  Questa ubicazione utilizza la configurazione magazzino avanzata con stoccaggi e prelievi diretti, che abilita regole più avanzate su come gli articoli si spostano all'interno del magazzino.

## Impostare i dati di magazzino Contoso Coffee

Per usare i dati demo di magazzino di Contoso Coffee, devi installare due app nell'azienda pertinente in [!INCLUDE [prod_short](../../includes/prod_short.md)]:  

- **Set di dati demo Contoso Coffee**  

    Questa app fornisce i dati demo per l'applicazione di base.  
- **Set di dati demo Contoso Coffee (ID paese)**  

    Questa app aggiunge contenuti specifici per il paese oltre a quelli dell'applicazione di base.

Aggiungi le app a un'azienda vuota in un abbonamento a pagamento o come parte di una versione di valutazione. Ad esempio, crea una nuova società senza dati di esempio dalla guida setup assistito **Crea una nuova società** che puoi aprire dall'elenco **Società**. Quindi aggiungi le app dal [marketplace](../../ui-extensions-install-uninstall.md#install) se non sono già elencate nella pagina **Gestione estensioni**.  

Una volta installate le app pertinenti, vai alla pagina [Dati demo di magazzino Contoso Coffee](https://businesscentral.dynamics.com/?page=4761) in [!INCLUDE [prod_short](../../includes/prod_short.md)] e modifica le impostazioni predefinite in base alle tue esigenze. Nella seguente tabella vengono illustrate le impostazioni:  

|Campo  |Descrizione  |
|---------|---------|
|**Anno di inizio** |Specifica il primo anno da usare per i dati dimostrativi di Contoso Coffee. A seconda della configurazione dell'azienda, l'anno può essere un anno solare o un anno fiscale.|
|**Collocazione ubicazione**  |L'ubicazione da usare per scenari di ubicazione di base.|
|**Ubicazione e logistica**  |L'ubicazione da usare per scenari di logistica semplice.|
|**Ubicazione con prelievo e stoccaggio diretti**  |L'ubicazione da usare per scenari di logistica avanzata.|
|**Ubicazione in transito**  |L'ubicazione da utilizzare per l'ubicazione in transito negli scenari di trasferimento.|
|**Nr. cliente**  |Il cliente da utilizzare per gli scenari di base e semplici nelle operazioni di vendita.|
|**N. fornitore**  |Il fornitore da utilizzare per tutti gli scenari nelle operazioni di acquisto.|
|**Nr. articolo principale**  |L'articolo da utilizzare per tutti gli scenari nelle operazioni di vendita.|
|**Nr. articolo 1**  |L'articolo principale da utilizzare per tutti gli scenari.|
|**Nr. articolo 2**  |L'articolo aggiuntivo da utilizzare per tutti gli scenari.|
|**Cat. reg. cliente**|Specifica un codice aziendale per clienti nazionali. I codici aziendali vengono utilizzati durante la registrazione delle transazioni. |
|**Categoria registrazione business generale clienti**|Specifica un codice aziendale per clienti nazionali. I codici aziendali vengono utilizzati durante la registrazione delle transazioni. |
|**Cat. reg. fornitore**|Specifica un codice aziendale per clienti e fornitori nazionali. I codici aziendali vengono utilizzati durante la registrazione delle transazioni. |
|**Categoria registrazione business generale fornitori**|Specifica un codice aziendale per clienti e fornitori nazionali. I codici aziendali vengono utilizzati durante la registrazione delle transazioni. |
|**Nazionale - Categoria registrazione business IVA**|Specifica un codice business IVA per clienti e fornitori per la registrazione dell'IVA, se l'IVA è abilitata.|
|**Rivendita - Categoria di registrazione magazzino**    |Specifica un codice per gli articoli che devono essere utilizzati per la registrazione della vendita.|
|**Vendita al dettaglio - Categoria registrazione articoli/servizi**    |Specifica un codice per gli articoli che devono essere utilizzati per la registrazione della vendita al dettaglio.|
|**Cat. reg. art./serv. IVA**    |Specifica un codice prodotto IVA per articoli per la registrazione dell'IVA, se l'IVA è abilitata.|
|**Fattore prezzo**     |Specifica un fattore per convertire un prezzo da USD/EUR nella valuta locale. *1* significa che il prezzo è lo stesso in qualsiasi valuta. Un numero alto viene utilizzato per ottenere il prezzo nella valuta locale. |
|**Precisione arrotondamento**  |Definisce il modo in cui le quantità di consumo calcolate vengono arrotondate una volta immesse nelle righe di registrazione consumi. Le quantità minori di 0,5 verranno arrotondate per difetto. Le quantità uguali a maggiori di 0,5 saranno arrotondate per eccesso.|

Quando sei pronto, scegli l'azione **Crea dati demo**. Occorrono alcuni minuti per aggiungere i dati al database sottostante, ma poi sei pronto per eseguire i vari scenari.  

> [!IMPORTANT]
> Se stai eseguendo gli scenari, potresti voler verificare che il tuo utente sia stato aggiunto per le ubicazioni selezionate. Per ulteriori informazioni, vedere [Impostare impiegati warehouse](../../warehouse-how-to-set-up-warehouse-employees.md).

## Scenari

I dati demo di magazzino Contoso Coffee attualmente supportano i seguenti scenari per il test e la formazione:

1.  [Procedura dettagliata del flusso in entrata e in uscita nelle configurazioni di warehouse di base](warehouse-basic-flow-putaway-pick.md)
2.  [Procedura dettagliata del flusso in entrata e in uscita nelle configurazioni di warehouse miste](warehouse-mixed-flow-receive-pick-ship.md)
3.  [Procedura dettagliata del flusso in entrata e in uscita nella configurazione avanzata del magazzino con stoccaggio e prelievo diretti](warehouse-directed-flow.md)

Leggi i passaggi per ogni scenario nell'articolo pertinente.  

## Vedere anche

[Impostazione del magazzino](../../inventory-setup-inventory.md) 
[Come impostare le ubicazioni](../../inventory-how-setup-locations.md) 
[Warehouse](../../warehouse-manage-warehouse.md) 
[Dettagli di progettazione](../../design-details-warehouse-overview.md) 
