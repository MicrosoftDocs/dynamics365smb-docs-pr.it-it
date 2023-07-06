---
title: Introduzione alla produzione di Contoso Coffee
description: Panoramica degli scenari su come i dati demo di Contoso Coffee possono aiutarti a imparare a usare le funzionalità di produzione in Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# <a name="introduction-to-contoso-coffee-manufacturing"></a><a name="introduction-to-contoso-coffee-manufacturing"></a><a name="introduction-to-contoso-coffee-manufacturing"></a>Introduzione alla produzione di Contoso Coffee

Contoso Coffee è un'azienda fittizia che produce caffettiere di consumo e commerciali. Le app **Contoso Coffee** per Business Central aggiungono i dati demo che puoi usare per imparare a usare le funzionalità di produzione in Business Central.  

L'app fornisce quattro prodotti ottimizzati per diversi scenari:

- **SP-SCM1009 Airpot**  

  Questo prodotto è una distinta base (DB) con un subassemblaggio, **Ciclo**. Usalo per dimostrare il flusso di produzione standard. È impostato con cicli alternativi che puoi usare per dimostrare vari scenari che coinvolgono i subappaltatori. Il metodo di costing è *Standard*.  

- **SP-SCM1011 Airpot Duo**  

  Questo prodotto richiede la tracciabilità degli articoli e ha un componente che richiede anche la tracciabilità degli articoli. Il metodo di costing è *Specifico*.  

- **SP-SCM1004 Autodrip**  

  Questo prodotto è una distinta base con un subassemblaggio, **Ciclo**. Lo consigliamo per dimostrare i vari metodi di consuntivazione sia per i componenti che per le operazioni. Il metodo di costing è *Standard*.

- **SP-SCM1006 AutoDripLite**

  Questo prodotto ha tre varianti e tre distinte base (DB) che possono essere assegnate alle unità di stockkeeping. Il prodotto utilizza il concetto di distinta base fantasma. Il metodo di costing è *Standard*.

Le attività di produzione per tutti gli scenari utilizzano la località *NORD*.  

> [!IMPORTANT]
> Prima di eseguire uno qualsiasi degli scenari per Contoso Coffee, registra le righe di registrazione articolo con i saldi di apertura. Per ulteriori requisiti, vedi la sezione [Impostare i dati di Contoso Coffee](#set-up-contoso-coffee-manufacturing-data).

## <a name="set-up-contoso-coffee-manufacturing-data"></a><a name="set-up-contoso-coffee-manufacturing-data"></a><a name="set-up-contoso-coffee-manufacturing-data"></a>Impostare i dati di produzione Contoso Coffee

Per usare i dati demo di produzione Contoso Coffee, devi installare due app nell'azienda pertinente in [!INCLUDE [prod_short](../../includes/prod_short.md)]:  

- **Set di dati demo Contoso Coffee**  

    Questa app fornisce i dati demo per l'applicazione di base.  
- **Set di dati demo Contoso Coffee (ID paese)**  

    Questa app aggiunge contenuti specifici per il paese oltre a quelli dell'applicazione di base.

Aggiungi le app a un'azienda vuota in un abbonamento a pagamento o come parte di una versione di valutazione. Ad esempio, crea una nuova società senza dati di esempio dalla guida setup assistito **Crea una nuova società** che puoi aprire dall'elenco **Società**. Quindi aggiungi le app dal [marketplace](../../ui-extensions-install-uninstall.md#install) se non sono già elencate nella pagina **Gestione estensioni**.  

Una volta installate le app pertinenti, vai alla pagina [Dati demo di Contoso Coffee](https://businesscentral.dynamics.com/?page=4760) in [!INCLUDE [prod_short](../../includes/prod_short.md)] e modifica le impostazioni predefinite in base alle tue esigenze. Nella seguente tabella vengono illustrate le impostazioni:  

|Campo  |Descrizione  |
|---------|---------|
|**Anno di inizio** |Specifica il primo anno da usare per i dati dimostrativi di Contoso Coffee. A seconda della configurazione dell'azienda, l'anno può essere un anno solare o un anno fiscale.|
|**Ubicazione produzione** |Specifica il magazzino da usare per le operazioni di produzione. L'impostazione predefinita è *NORD*, ma puoi modificarla in base alle tue esigenze.|
|**Tipo di società**    |Specifica se la società corrente deve dichiarare l'IVA. |
|**Nazionale - Categoria registrazione business generale**|Specifica un codice aziendale per clienti e fornitori nazionali. I codici aziendali vengono utilizzati durante la registrazione delle transazioni. |
|**Capacità - Categoria registrazione articoli/servizi**    |Specifica un codice per gli articoli o le risorse che devono essere utilizzati per la registrazione della capacità.|
|**Vendita al dettaglio - Categoria registrazione articoli/servizi**    |Specifica un codice per gli articoli o le risorse che devono essere utilizzati per la registrazione della vendita al dettaglio.|
|**Mat. prime - Categoria registrazione articoli/servizi**    |Specifica un codice per gli articoli o le risorse che devono essere utilizzati per la registrazione delle materie prime. |
|**Codice imponibile IVA**    |Specifica un gruppo di prodotti IVA esistente che viene utilizzato per gli articoli.|
|**Codice finito**    |Specifica un gruppo di prodotti esistente che viene utilizzato per gli articoli finiti.|
|**Fattore prezzo**     |Specifica un fattore per convertire un prezzo da USD/EUR nella valuta locale. *1* significa che il prezzo è lo stesso in qualsiasi valuta. Un numero alto viene utilizzato per ottenere il prezzo nella valuta locale. |
|**Precisione arrotondamento**  |Definisce il modo in cui le quantità di consumo calcolate vengono arrotondate una volta immesse nelle righe di registrazione consumi. Le quantità minori di 0,5 verranno arrotondate per difetto. Le quantità uguali a maggiori di 0,5 saranno arrotondate per eccesso.|

Quando sei pronto, scegli l'azione **Crea dati demo**. Occorrono alcuni minuti per aggiungere i dati al database sottostante, ma poi sei pronto per eseguire i vari scenari.  

## <a name="scenarios"></a><a name="scenarios"></a><a name="scenarios"></a>Scenari

I dati demo di produzione Contoso Coffee attualmente supportano i seguenti scenari per il test e la formazione:

1. [Creare una nuova DBA di produzione e la versione DBA](create-new-production-bom-version.md)  
2. [Creare un nuovo ciclo](create-new-routing.md)  
3. [Creare un ordine di produzione confermato e modificarlo](create-firm-planned-production-order-change.md)  
4. [Combinare la consuntivazione automatica e manuale](combine-automatic-manual-flushing.md)  
5. [Usare la pianificazione degli ordini per creare e prenotare la fornitura](order-planning-create-reserve-supply.md)  
6. [Impostare ed elaborare un'operazione di subappalto](set-up-process-subcontracting-operation.md)  
7. [Impostare una nuova capacità](set-up-new-capacity.md)  
8. [Prevedere la domanda per varianti articolo con distinte base diverse assegnate](variants.md)  

Leggi i passaggi per ogni scenario nell'articolo pertinente.  

> [!IMPORTANT]
> Queste procedure dettagliate richiedono che l'esperienza utente sia impostata su *Premium* nella pagina **Informazioni società**.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Vedere anche

[Manufacturing](../../production-manage-manufacturing.md)  
[Report di produzione e analisi in Business Central](../../production-reports.md)  
