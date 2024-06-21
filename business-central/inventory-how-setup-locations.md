---
title: Impostare una scheda ubicazione e definire i percorsi di trasferimento (video)
description: 'Se acquisti, immagazzini o vendi articoli in più di un luogo, puoi impostare ogni luogo come ubicazione.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'warehouse, distribution center'
ms.search.forms: '5703, 15'
ms.date: 03/25/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-locations"></a>Impostare le ubicazioni

Le ubicazioni sono luoghi come i magazzini in cui acquisti, stocchi o vendi articoli. [!INCLUDE [prod_short](includes/prod_short.md)] utilizza le ubicazioni per tenere traccia dell'inventario sia nei casi semplici che nei processi di magazzino complessi.

È quindi possibile creare le righe del documento per una specifica ubicazione, visualizzare la disponibilità per ubicazione e trasferire il magazzino tra le ubicazioni. Per saperne di più, vai a [Gestire l'inventario](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a>Schede Ubicazione

Specifica le informazioni su un'ubicazione, ad esempio un warehouse o un centro di distribuzione nella pagina **Scheda ubicazione**. A ogni ubicazione vengono assegnati un nome e un codice che la rappresenta. Quando si desidera registrare le transazioni per una determinata ubicazione, è possibile immettere il codice ubicazione in altre aree del programma.  

È possibile immettere informazioni sui criteri di logistica warehouse per ogni ubicazione. In base ai criteri di magazzino, puoi utilizzare le opzioni nella scheda dettaglio **Collocazioni** per specificare le collocazioni da utilizzare per impostazione predefinita per le transazioni. Se è previsto l'utilizzo di stoccaggi e prelievi guidati, utilizza le opzioni della Scheda dettaglio **Criteri per collocazione** per definire le modalità di utilizzo delle funzioni di logistica avanzate.  

Alcuni campi opzione dipendono da altre impostazioni nella pagina **Scheda Ubicazione** per limitare le combinazioni di setup non supportate.  

Seleziona l'azione **Zone** o **Collocazioni** per visualizzare le informazioni relative a zone e collocazioni che sono definite per l'ubicazione.

### <a name="to-set-up-a-location"></a>Per impostare un'ubicazione

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Ubicazioni**, quindi scegli il collegamento correlato.
2. Scegliere l'azione **Nuovo**.
3. Nella pagina **Scheda ubicazione** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Ripetere i passaggi 2 e 3 per ogni ubicazione in cui si desidera mantenere il magazzino.

> [!NOTE]  
> Molti campi della pagina Scheda ubicazione fanno riferimento alla gestione degli articoli nei processi della warehouse in entrata e in uscita. Questi campi non sono rilevanti per le aziende che non richiedono la funzionalità di magazzino complessa. Per ulteriori informazioni, vedi [Impostazione di Warehouse Management](warehouse-setup-warehouse.md).

Puoi modificare la configurazione di un'ubicazione purché non includa movimenti contabili articoli.  

Se disponi di più ubicazioni, puoi definire percorsi di trasferimento tra le ubicazioni. Per ulteriori informazioni sui percorsi di trasferimento, vai a [Per creare un percorso di trasferimento](inventory-how-setup-locations.md#to-create-a-transfer-route).

### <a name="to-create-a-transfer-route"></a>Per creare i percorsi di trasferimento

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Percorsi di trasferimento**, quindi scegli il collegamento correlato.
2. Scegli l'azione **Nuovo**.
4. Nella pagina **Scheda ubicazione** compilare i campi secondo le necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

A questo punto è possibile trasferire agli articoli di magazzino tra due ubicazioni. Per ulteriori informazioni sui trasferimenti, vai a [Trasferire scorte tra ubicazioni](inventory-how-transfer-between-locations.md).

## <a name="bins"></a>Collocazioni

Le collocazioni rappresentano la struttura di base del magazzino e possono suggerire dove riporre gli articoli. Le tue collocazioni possono avere contenuto o essere collocazioni mobili senza contenuto specifico.

Per utilizzare la funzionalità di collocazione in una ubicazione, devi prima attivare la funzionalità sulla pagina **Scheda ubicazione** selezionando il campo **Collocazione obbligatoria** sulla Scheda dettaglio **Warehouse**. È possibile progettare il flusso di articoli nell'ubicazione specificando i codici collocazione nei campi per i processi di magazzino nelle Schede rapide **Collocazioni** e **Criteri per collocazione**.

> [!NOTE]
> Prima di poter specificare i codici di collocazione in una ubicazione, è necessario creare i codici di collocazione. Per ulteriori informazioni sulle collocazioni, vai a [Creare le collocazioni](warehouse-how-to-create-individual-bins.md) e [Impostare i tipi di collocazione](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones"></a>Zone

Se vuoi strutturare le tue collocazioni in zone, puoi farlo nella pagina **Zone**. Quando si assegna una zona alle collocazioni, [!INCLUDE [prod_short](includes/prod_short.md)] copia le informazioni dalla zona nelle collocazioni. Puoi anche scegliere di impostare una zona e utilizzare le collocazioni da sole per organizzare il tuo magazzino. Per ulteriori informazioni sulle zone, vedi [Impostazione di Warehouse Management](warehouse-setup-warehouse.md).  

## <a name="default-dimensions-for-locations"></a>Dimensioni predefinite per le ubicazioni

Le dimensioni sono valori che categorizzano i movimenti in modo da poterli seguire e analizzare usando diversi strumenti di report. Ad esempio, le dimensioni possono indicare il reparto o il progetto da cui un movimento proviene. Avere dimensioni predefinite aiuta le persone a evitare di commettere errori e di dover inserire manualmente le dimensioni a livello di transazione se tutte le merci provengono da un'unica ubicazione e reparto.

Imposti le dimensioni predefinite per un'ubicazione nella pagina **Scheda ubicazione** scegliendo **Dimensioni**. Successivamente, le dimensioni predefinite dell'ubicazione vengono assegnate ai documenti seguenti quando scegli l'ubicazione su una riga.

* Ordini di trasferimento
* Ordini inventario fisico
* Spedizioni magazzino
* Carichi magazzino
* Registrazioni articoli

Se necessario, puoi eliminare o modificare le dimensioni nella riga. Nel campo **Registrazione valore** puoi richiedere che le persone specifichino le dimensioni per ubicazioni specifiche prima di poter registrare una voce. Se desideri consentire alle persone di scegliere solo determinati valori di dimensione, puoi specificarli nel campo **Filtro valori consentiti**. Puoi anche includere i valori delle dimensioni ubicazione nella pagina **Priorità dimensione predefinita** e per combinazioni di priorità e regole di dimensioni nella pagina **Combinazioni dimensioni**.

Poiché i documenti dell'ordine di trasferimento e le registrazioni di riclassificazione riguardano più ubicazioni, l'ordine in cui si inseriscono i dati è importante. Le dimensioni predefinite vengono copiate dall'ultimo campo dell'ubicazione (l'ubicazione in transito viene ignorata).

### <a name="example-of-default-dimensions-on-locations"></a>Esempio di dimensioni predefinite per le ubicazioni

Gli esempi seguenti illustrano come viene utilizzata la dimensione predefinita.

Hai le seguenti impostazioni di dimensione:

* Ubicazione EAST. La dimensione del reparto è ADM
* Ubicazione WEST. La dimensione del reparto è PROD

Specifica l'ubicazione su un ordine di trasferimento come segue:

1. Da ubicazione = EST
2. A ubicazione = WEST

La dimensione PROD verrà copiata dall'ubicazione WEST.

Compila i campi nell'ordine opposto, come indicato di seguito:

1. A ubicazione = WEST
2. Da ubicazione = EST

La dimensione ADM verrà copiata dall'ubicazione EAST.

## <a name="see-also"></a>Vedere anche

[Gestire i costi del magazzino](inventory-manage-inventory.md)  
[Trasferire il magazzino tra le ubicazioni](inventory-how-transfer-between-locations.md)  
[Creare collocazioni](warehouse-how-to-create-individual-bins.md)  
[Impostare i tipi di collocazioni](warehouse-how-to-set-up-bin-types.md)  
[Impostazione Warehouse Management](warehouse-setup-warehouse.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modifica delle funzionalità visualizzate](ui-experiences.md)  
[Funzionalità aziendali generali](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
