---
title: Impostare e gestire un budget per un progetto
description: 'Descrive come pianificare le risorse, prevedere e controllare i costi di un progetto impostando un budget per ciascun progetto.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'project budget, forecast'
ms.search.form: '1002, 1007'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Gestione dei budget dei progetti

È possibile impostare un budget per ogni progetto. Il budget viene utilizzato per pianificare le risorse allocate a un progetto. Il budget può essere generale con pochi movimenti oppure può contenere più movimenti divisi in livelli di attività. È quindi possibile confrontare gli importi previsti con l'utilizzo effettivo come registrato nella registrazione progetti. Monitorando le differenze tra l'utilizzo effettivo e quello a budget, è possibile controllare un progetto in corso e migliorare la qualità di progetti futuri riducendo il rischio di sottovalutazione dei costi.

Di seguito viene descritto come stimare i costi a budget durante la pianificazione. Per informazioni su come registrare i prezzi e i costi di progetti a budget rispetto a quelli effettivi, vedere [Registrare l'utilizzo nei progetti](projects-how-record-job-usage.md).  

## <a name="JobBudgetCosts"></a> Per stimare i costi a budget per un progetto

Quando un cliente desidera conoscere il prezzo di un progetto che verrà fatturata in base all'utilizzo, è necessario determinare i costi a budget per il progetto. A tale scopo, utilizza la pagina **Righe attività di progetto**.

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Progetti**, quindi scegli il collegamento correlato.  
2. Apri un progetto pertinente.
3. Selezionare una riga di attività di tipo Registrazione quindi scegliere l'azione **Righe di pianificazione progetto**.
4. In una nuova riga, compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Per il campo **Tipo riga** fare riferimento alle seguenti informazioni.  

| Tipo riga | Descrizione |
| --- | --- |
| **Sia Budget sia fatturabile** |Gli importi relativi a costi e prezzo immessi nella riga di pianificazione sono i costi a budget per la riga di pianificazione specifica. L'importo dei prezzi verrà fatturato. |
| **Budget** |Al cliente non viene addebitato l'utilizzo. L'utilizzo non viene trasferito a una fattura, ma viene utilizzato per calcolare il WIP. |
| **Fatturabile** |Al cliente viene addebitato l'utilizzo. La quantità viene trasferita nella fattura, in base alla quantità specificata nel campo **Qtà da trasferire in fattura**. |

> [!NOTE]  
> Il campo **Data di consegna pianificata** per la riga di pianificazione contiene la data in cui è previsto il completamento dell'utilizzo correlato alla riga di pianificazione. È inoltre la data in cui la riga di pianificazione può essere trasferita a una fattura vendita ed essere registrata. <br /><br /> Nell'attività di progetto sottostante nella pagina **Scheda progetto**, i campi **Data di inizio** e **Data di fine** contengono rispettivamente il valore del campo **Data di consegna pianificata** nella prima e ultima riga di pianificazione progetto nella pagina **Righe pianificazione progetto** relativa.

> [!NOTE]  
> Quando si compila il campo **Quantità**, tutte le informazioni sul prezzo totale e i costi totali saranno calcolate e immesse per quella riga di registrazione. È possibile modificarle in qualsiasi momento.

Nella pagina **Scheda progetto**, è possibile ora vedere un riepilogo dei costi a budget totali, del prezzo a budget, del costo e del prezzo fatturabili per ciascuna attività.

Per informazioni su come registrare i prezzi e i costi di progetti a budget rispetto a quelli effettivi, vedere [Registrare l'utilizzo nei progetti](projects-how-record-job-usage.md).

## Vedere anche

[Gestione progetti](projects-manage-projects.md)  
[Dati finanziari](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
