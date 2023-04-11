---
title: Associazione e sincronizzazione (video)
description: La sincronizzazione del mapping della tabella di integrazione consente la sincronizzazione di dati in tutti i record in una tabella in Business Central e in una tabella in Dynamics 365 Sales che sono associate.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'crm, sales, couple, decouple, synchronize'
ms.search.form: '6250,'
---

# Accoppiamento e sincronizzazione dei record tra Dataverse e Business Central

In questo argomento viene descritto come associare uno o più record in [!INCLUDE[prod_short](includes/prod_short.md)] a record in Dataverse o [!INCLUDE[crm_md](includes/crm_md.md)]. L'associazione di record consente di visualizzare le infomazioni di Dataverse da [!INCLUDE[prod_short](includes/prod_short.md)] e viceversa. L'associazione consente inoltre di sincronizzare dati tra i record. È possibile associare i record esistenti, oppure creare e associare nuovi record.

> [!NOTE]
> L'associazione e la sincronizzazione dei dati è disponibile solo se l'amministratore di sistema ha creato una connessione tra [!INCLUDE[prod_short](includes/prod_short.md)] e Dataverse o [!INCLUDE[crm_md](includes/crm_md.md)]. Un modo rapido di verificare è di aprire la scheda **Cliente** e di cercare l'azione **Imposta associazione**. Se l'azione è disponibile, le app sono collegate.

## Esempio di video

Questo video mostra l'associazione e la sincronizzazione dei dati nel contesto di un'integrazione con [!INCLUDE[crm_md](includes/crm_md.md)].

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## Per associare un record  

1. In [!INCLUDE[prod_short](includes/prod_short.md)], aprire la scheda del record da associare. Ad esempio, la scheda Cliente o Contatto.  

    È inoltre possibile aprire la pagina elenco e selezionare il record che si desidera associare.  

2. Scegliere l'azione **Imposta associazione**.  
3. Compilare i campi e scegliere **OK**.  

## Per sincronizzare un singolo record  

1. In [!INCLUDE[prod_short](includes/prod_short.md)], aprire la scheda del record da associare. Ad esempio, la scheda Cliente o Contatto.  
2. Scegliere l'azione **Sincronizza adesso**.  
3. Se un record può essere sincronizzato in una direzione, selezionare l'opzione che specifica la direzione di aggiornamento dei dati e scegliere **OK**.  

## Per sincronizzare un singolo record da [!INCLUDE[crm_md](includes/crm_md.md)]  

1. In [!INCLUDE[crm_md](includes/crm_md.md)], aprire il modulo del record da associare. Ad esempio, la scheda Account o il modulo scheda Contatto.  
2. Scegli l'azione **[!INCLUDE[prod_short](includes/prod_short.md)]** nella barra multifunzione per aprire e associare automaticamente il record.

    > [!Note]
    > È possibile sincronizzare un singolo record da [!INCLUDE[crm_md](includes/crm_md.md)] automaticamente solo quando **Sinc. solo record associati** è disabilitata e la direzione di sincronizzazione è impostata su Bidirezionale o Da tabella di integrazione nella pagina **Integration Table Mapping** per il record. Per ulteriori informazioni, vedere [Mappatura delle tabelle e dei campi da sincronizzare](admin-how-to-modify-table-mappings-for-synchronization.md#create-new-records).     

## Per accoppiare più record usando l'accoppiamento basato sulla corrispondenza

Specifica i dati da sincronizzare per un'entità, come un cliente o un contatto, accoppiando i record in base alle corrispondenze. Raffina le corrispondenze rendendo la ricerca sensibile alle maiuscole e assegnando una priorità per ogni corrispondenza. Se non viene trovata alcuna corrispondenza, si può anche specificare che si vuole creare l'entità in Dataverse. Per maggiori informazioni, vedi [Personalizzare l'accoppiamento basato sulla corrispondenza](admin-how-to-set-up-a-dynamics-crm-connection.md#customize-the-match-based-coupling).  

> [!NOTE]
> Il processo di associazione basata su corrispondenza ignora i record che sono già stati abbinati. Per includere questi record quando esegui l'associazione basata su corrispondenza, annulla l'associazione dei record e riprova. Per saperne di più sull'annullamento dell'associazione dei record, vai a [Annullare l'associazione di record](#uncoupling-records).

1. In [!INCLUDE[prod_short](includes/prod_short.md)], aprire la pagina elenco per il record, ad esempio le pagine elenco Clienti o Contatti.
2. scegli l'azione **Accoppiamento basato su corrispondenza** .
3. Compilare i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Per sincronizzare più record  

1. In [!INCLUDE[prod_short](includes/prod_short.md)], apri la pagina elenco per il record, ad esempio le pagine Clienti o Contatti.  
2. Selezionare i record che si intende sincronizzare, quindi scegliere **Sincronizza adesso**.  
3. Se i record possono essere sincronizzati in una direzione, selezionare l'opzione che specifica la direzione e scegliere **OK**.  

## Annullare l'associazione di record

È possibile annullare l'associazione di uno o più record nelle pagine di elenco o nella pagina **Errori di sincronizzazione dati associati** scegliendo una o più righe e quindi **Elimina associazione**. È inoltre possibile rimuovere tutte le associazioni per una o più mapping di tabella nella pagina **Mapping tabella integrazione**.

## Vedere anche  

[Utilizzare Dynamics 365 Sales da Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]