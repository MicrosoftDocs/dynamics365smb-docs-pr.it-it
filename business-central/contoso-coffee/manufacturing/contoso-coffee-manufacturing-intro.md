---
title: Introduzione alla produzione di Contoso Coffee
description: Panoramica degli scenari su come i dati demo di Contoso Coffee possono aiutarti a imparare a usare le funzionalità di produzione in Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4765
author: brentholtorf
ms.author: bholtorf
---

# Introduzione alla produzione di Contoso Coffee

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

Le attività di produzione per tutti gli scenari utilizzano l'ubicazione *PRINCIPALE*.  

> [!IMPORTANT]
> Prima di eseguire uno qualsiasi degli scenari per Contoso Coffee, registra le righe di registrazione articolo con i saldi di apertura. Per ulteriori requisiti, vedi la sezione [Impostare i dati di Contoso Coffee](#set-up-contoso-coffee-manufacturing-data).

## Impostare i dati di produzione Contoso Coffee

[!INCLUDE [contoso-coffee-app-install](../contoso-coffee-app-install.md)].

|Campo  |Descrizione  |
|---------|---------|
|**Ubicazione produzione** |Specifica il magazzino da usare per le operazioni di produzione. L'impostazione predefinita è *PRINCIPALE*, ma puoi modificarla in base alle tue esigenze.|


Quando sei pronto, scegli l'azione **Crea dati demo**. Occorrono alcuni minuti per aggiungere i dati al database sottostante, ma poi sei pronto per eseguire i vari scenari.  

## Scenari

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

## Vedere anche

[Manufacturing](../../production-manage-manufacturing.md)  
[Report di produzione e analisi in Business Central](../../production-reports.md)  
