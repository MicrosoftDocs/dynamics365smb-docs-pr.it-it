---
title: Introduzione ai dati demo Contoso Coffee
description: Panoramica degli scenari su come i dati demo di Contoso Coffee possono aiutarti a imparare a usare le funzionalità in Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# Introduzione ai dati demo Contoso Coffee

Contoso Coffee è un'azienda fittizia che produce caffettiere di consumo e commerciali. Le app **Contoso Coffee** per Business Central aggiungono i dati demo che puoi usare per imparare a usare le funzionalità in Business Central.  


## Impostare i dati di Contoso Coffee

Per usare i dati demo di Contoso Coffee, devi installare due app nell'azienda pertinente in [!INCLUDE [prod_short](../includes/prod_short.md)]:  

- **Set di dati demo Contoso Coffee**  

    Questa app fornisce i dati demo per l'applicazione di base.  
- **Set di dati demo Contoso Coffee (ID paese)**  

    Questa app aggiunge contenuti specifici per il paese oltre a quelli dell'applicazione di base.

Aggiungi le app a un'azienda vuota in un abbonamento a pagamento o come parte di una versione di valutazione. Ad esempio, crea una nuova società senza dati di esempio dalla guida setup assistito **Crea una nuova società** che puoi aprire dall'elenco **Società**. Quindi aggiungi le app dal [marketplace](../ui-extensions-install-uninstall.md#install) se non sono già elencate nella pagina **Gestione estensioni**.  

Dovresti quindi completare:
 - L'[Impostazione di produzione](manufacturing/contoso-coffee-manufacturing-intro.md) per prepararti all'uso degli [Scenari di produzione](#manufacturing-scenarios)
 - L'[Impostazione di magazzino](warehousing/contoso-coffee-warehousing-intro.md) per prepararti all'uso degli [Scenari di magazzino](#warehousing-scenarios)

## Scenari di produzione

I dati demo di Contoso Coffee attualmente supportano i seguenti scenari di produzione per il test e la formazione:

1. [Creare una nuova DBA di produzione e la versione DBA](manufacturing/create-new-production-bom-version.md)  
2. [Creare un nuovo ciclo](manufacturing/create-new-routing.md)  
3. [Creare un ordine di produzione confermato e modificarlo](manufacturing/create-firm-planned-production-order-change.md)  
4. [Combinare la consuntivazione automatica e manuale](manufacturing/combine-automatic-manual-flushing.md)  
5. [Usare la pianificazione degli ordini per creare e prenotare la fornitura](manufacturing/order-planning-create-reserve-supply.md)  
6. [Impostare ed elaborare un'operazione di subappalto](manufacturing/set-up-process-subcontracting-operation.md)  
7. [Impostare una nuova capacità](manufacturing/set-up-new-capacity.md)  
8. [Prevedere la domanda per varianti articolo con distinte base diverse assegnate](manufacturing/variants.md)  

Leggi i passaggi per ogni scenario nell'articolo pertinente.  

> [!IMPORTANT]
> Le procedure dettagliate di produzione richiedono che l'esperienza utente sia impostata su *Premium* nella pagina **Informazioni società**.

## Scenari di magazzino

I dati demo di Contoso Coffee attualmente supportano i seguenti scenari di magazzino per il test e la formazione:

1.  Configura le collocazioni predefinite, la ricezione e lo stoccaggio con lo stoccaggio dell'inventario, il prelievo e la spedizione con il prelievo dall'inventario in modalità ordine per ordine con [Procedura dettagliata del flusso in entrata e in uscita nelle configurazioni di base del magazzino](warehousing/warehouse-basic-flow-putaway-pick.md)
2.  Ricevi e stocca più ordini in entrata contemporaneamente con il ricevimento in magazzino, spedisci più ordini in una volta con la spedizione in magazzino, preleva con prelievi in magazzino con [Procedura dettagliata del flusso in entrata e in uscita nelle configurazioni di magazzino miste](warehousing/warehouse-mixed-flow-receive-pick-ship.md)
3.  Configura le collocazioni fisse per l'unità di misura dell'articolo, il cross-docking dell'utente per ridurre i movimenti fisici delle merci, ottimizza il posizionamento delle merci con il rifornimento delle collocazioni, separa le unità di misura di grande dimensione in unità più piccole, distribuisci il prelievo tra i dipendenti del magazzino con il foglio di lavoro di prelievo con [Procedura dettagliata del flusso in entrata e in uscita nella configurazione avanzata del magazzino con stoccaggio e prelievo diretti](warehousing/warehouse-directed-flow.md)

Leggi i passaggi per ogni scenario nell'articolo pertinente.
   
## Vedere anche

[Manufacturing](../production-manage-manufacturing.md)  
[Gestione della warehouse](../warehouse-manage-warehouse.md)  

