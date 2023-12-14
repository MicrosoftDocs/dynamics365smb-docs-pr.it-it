---
title: Introduzione a Contoso Coffee
description: Panoramica degli scenari su come i dati demo di Contoso Coffee possono aiutarti a imparare a usare le funzionalità di magazzino in Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4764
author: brentholtorf
ms.author: bholtorf
---

# <a name="introduction-to-contoso-coffee-warehousing"></a>Introduzione alla gestione magazzino Contoso Coffee

Contoso Coffee è un'azienda fittizia che produce caffettiere di consumo e commerciali. Le app **Contoso Coffee** per Business Central aggiungono i dati demo che puoi usare per imparare a usare le funzionalità di magazzino in Business Central. Puoi configurare le funzionalità del magazzino in vari modi, vedi [Panoramica delle diverse opzioni di configurazione](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

L'app fornisce tre ubicazioni ottimizzate per diversi scenari:

- **ARGENTO**  

  Questa ubicazione è configurata per utilizzare le collocazioni. Può essere facilmente configurata per il supporto di base o avanzato. 

- **GIALLO**  

  Questa ubicazione utilizza la configurazione avanzata del magazzino, ma non utilizza le collocazioni. Può essere riconfigurata per supportare le configurazioni di base.

- **BIANCO**  

  Questa ubicazione utilizza la configurazione magazzino avanzata con stoccaggi e prelievi diretti, che abilita regole più avanzate su come gli articoli si spostano all'interno del magazzino.

## <a name="set-up-contoso-coffee-warehousing-data"></a>Impostare i dati di magazzino Contoso Coffee

[!INCLUDE [contoso-coffee-app-install](../contoso-coffee-app-install.md)].

Una volta installate le app pertinenti, vai alla pagina [Strumento demo Contoso](https://businesscentral.dynamics.com/?page=5194) in [!INCLUDE [prod_short](../../includes/prod_short.md)], seleziona la riga *Modulo Warehouse* e utilizza l'azione **Configura** per preparare i moduli. Nelle seguenti tabelle vengono illustrate le impostazioni:  

|Campo  |Descrizione  |
|---------|---------|
|**Collocazione ubicazione**  |L'ubicazione da usare per scenari di ubicazione di base.|
|**Ubicazione avanzata**  |L'ubicazione da usare per scenari di logistica semplice.|
|**Ubicazione con prelievo e stoccaggio diretti**  |L'ubicazione da usare per scenari di logistica avanzata.|
|**Ubicazione in transito**  |L'ubicazione da utilizzare per l'ubicazione in transito negli scenari di trasferimento.|
|**Nr. cliente**  |Il cliente da utilizzare per gli scenari di base e semplici nelle operazioni di vendita.|
|**N. fornitore**  |Il fornitore da utilizzare per tutti gli scenari nelle operazioni di acquisto.|
|**Nr. articolo 1**  |L'articolo principale da utilizzare per tutti gli scenari.|
|**Nr. articolo 2**  |L'articolo aggiuntivo da utilizzare per tutti gli scenari.|
|**Nr. articolo 3**  |L'articolo con tracciabilità.|

Quando sei pronto, scegli l'azione **Crea dati demo**. Occorrono alcuni minuti per aggiungere i dati al database sottostante, ma poi sei pronto per eseguire i vari scenari.  

> [!IMPORTANT]
> Se stai eseguendo gli scenari, potresti voler verificare che il tuo utente sia stato aggiunto per le ubicazioni selezionate. Per ulteriori informazioni, vedere [Impostare impiegati warehouse](../../warehouse-how-to-set-up-warehouse-employees.md).

## <a name="scenarios"></a>Scenari

I dati demo di magazzino Contoso Coffee attualmente supportano i seguenti scenari per il test e la formazione:

1.  [Procedura dettagliata del flusso in entrata e in uscita nelle configurazioni di warehouse di base](warehouse-basic-flow-putaway-pick.md)
2.  [Procedura dettagliata per il flusso in entrata e in uscita nelle configurazioni della warehouse miste](warehouse-mixed-flow-receive-pick-ship.md)
3.  [Procedura dettagliata del flusso in entrata e in uscita nella configurazione avanzata del magazzino con stoccaggio e prelievo diretti](warehouse-directed-flow.md)

Leggi i passaggi per ogni scenario nell'articolo pertinente.  

## <a name="see-also"></a>Vedere anche

[Impostazione del magazzino](../../inventory-setup-inventory.md) 
[Come impostare le ubicazioni](../../inventory-how-setup-locations.md) 
[Warehouse](../../warehouse-manage-warehouse.md) 
[Dettagli di progettazione](../../design-details-warehouse-overview.md) 
