---
title: Introduzione ai dati demo Contoso Coffee
description: Panoramica degli scenari su come i dati demo di Contoso Coffee possono aiutarti a imparare a usare le funzionalità in Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.date: 09/20/2023
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '5194,'
ms.custom: bap-template
---

# Introduzione ai dati demo Contoso Coffee

Contoso Coffee è un'azienda fittizia che produce caffettiere di consumo e commerciali. Le app **Contoso Coffee** per [!INCLUDE [prod_short](../includes/prod_short.md)] aggiungono i dati demo che puoi usare per imparare a usare le funzionalità in [!INCLUDE [prod_short](../includes/prod_short.md)].  

## Impostare i dati di Contoso Coffee

[!INCLUDE [contoso-coffee-app-install](../includes/contoso-coffee-app-install.md)]

Una volta installate le app, nella pagina **Strumento demo Contoso** utilizza l'azione **Configura** per preparare i seguenti moduli. Puoi scegliere di installare tutti i dati disponibili, inclusi i dati di configurazione e produzione, oppure solo i dati di configurazione.

 - Il **Modulo comune** per preparare le impostazioni generali che [!INCLUDE [prod_short](../includes/prod_short.md)] richiede. Ad esempio, cose come serie numeriche. Tieni presente che il **Modulo comune** contiene dati supplementari solo per gli scenari Warehouse, Produzione e Assistenza. Non è consigliabile eseguirlo singolarmente.

Nella seguente tabella vengono illustrate le impostazioni:  

|Campo  |Descrizione  |
|---------|---------|
|**Anno di inizio** |Specifica il primo anno da usare per i dati dimostrativi di Contoso Coffee. A seconda della configurazione dell'azienda, l'anno può essere un anno solare o un anno fiscale.|
|**Codice paese/area geografica**|Specifica un codice paese/area per clienti e fornitori nazionali.|
|**Tipo di società**    |Specifica se la società corrente deve dichiarare l'IVA. |
|**Fattore prezzo**     |Specifica un fattore per convertire un prezzo da USD/EUR nella valuta locale. *1* significa che il prezzo è lo stesso in qualsiasi valuta. Un numero alto viene utilizzato per ottenere il prezzo nella valuta locale. |
|**Approssimazione di arrotondamento**  |Specifica l'approssimazione di arrotondamento con cui si desidera creare i dati demo.|

 - Il [Modulo di produzione](manufacturing/contoso-coffee-manufacturing-intro.md) per prepararti agli [scenari di produzione](manufacturing/contoso-coffee-manufacturing-intro.md#scenarios).
 - Il [Modulo di magazzino](warehousing/contoso-coffee-warehousing-intro.md) per prepararti agli [scenari di magazzino](warehousing/contoso-coffee-warehousing-intro.md#scenarios)
 - Il [Modulo di assistenza](service/contoso-coffee-service-intro.md) per prepararti agli [scenari di assistenza](service/contoso-coffee-service-intro.md#scenarios).

Dopo aver configurato i moduli che desideri provare, scegli l'azione **Genera** per creare dati dimostrativi per tali moduli.

## Vedere anche

[Produzione](../production-manage-manufacturing.md)  
[Warehousing](../warehouse-manage-warehouse.md)  
[Assistenza](../service-service.md)
<!-- [Projects and Jobs](../projects-manage-projects.md) -->

