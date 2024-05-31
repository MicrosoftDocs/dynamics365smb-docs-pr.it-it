---
title: Assegnazione e gestione di task
description: 'Scopri come assegnare task agli utenti, incluso il tuo contabile, in Business Central e come selezionare e completare le attività.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'tasks, work'
ms.search.form: '1164, 1170, 1171, 1172, 1175, 1176, 1177'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="define-user-tasks"></a>Definisci task dell'utente

In [!INCLUDE[prod_short](includes/prod_short.md)], è possibile creare task per ricordare le attività da svolgere. È possibile creare task per se stessi, ma è anche possibile assegnarli ad altri utenti o che un'altra persona nell'organizzazione assegni un task all'utente.  

## <a name="managing-user-tasks"></a>Gestione dei task degli utenti

La pagina **Task dell'utente** mostra tutti i task e consente di creare e assegnare facilmente nuovi task. Quando si crea un task, è possibile specificare la data di inizio e di fine e aggiungere un collegamento alla pagina o al report in [!INCLUDE[prod_short](includes/prod_short.md)] in cui l'utente deve svolgere l'attività.  

Ad esempio, è possibile creare un task per se stessi o un collaboratore per visualizzare tutte le fatture di vendita registrate. In tal caso, collegare il task alla pagina 143, **Fatture di vendita registrate**. Nello screenshot seguente, qualcuno sta creando un'attività per MeganB per rivedere le fatture di vendita registrate.  

:::image type="content" source="media/across-user-tasks/sample-user-task.png" alt-text="Esempio di un'attività utente.":::

> [!TIP]  
> Utilizzare la funzionalità di ricerca nel campo **Pagina**, quindi utilizzare il campo **Cerca** per identificare la pagina che si desidera.  
>
> È possibile collegare a qualsiasi pagina, ma non è possibile collegare singole voci, quindi rendere la descrizione il più esplicita possibile, ad esempio scrivendo "Osservare il cliente n. 10000 e assicurarsi che non abbia pagamenti scaduti.".

### <a name="picking-up-user-tasks"></a>Selezione dei task degli utenti

Nelle Gestioni ruolo utente di Manager aziendale, Contabile e Addetto contabile, un riquadro mostra i task in sospeso assegnati all'utente. Per selezionare un task, sceglierlo dall'elenco dei task in sospeso dell'utente. Nella barra multifunzione, il collegamento **Vai a elemento task** apre la pagina in cui è possibile svolgere l'attività.  

Una volta completato il task, contrassegnarlo come completato.  

### <a name="deleting-user-tasks"></a>Eliminazione di task degli utenti

Se si desidera eliminare tutti o alcuni task dell'utente, è possibile utilizzare il report **Elimina task dell'utente**. Nella pagina di richiesta, è possibile impostare i filtri per determinare quali task devono essere eliminati.  

## <a name="see-also"></a>Vedi anche

[Ricerca di una pagina o di un report](ui-search.md)  
[Esperienze di contabile in [!INCLUDE[prod_short](includes/prod_short.md)]](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
