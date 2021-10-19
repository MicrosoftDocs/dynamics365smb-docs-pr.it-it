---
title: Impostare i fogli di presenza e la loro approvazione
description: Si possono impostare i fogli presenze per tenere traccia del tempo utilizzato per le commesse e l'utilizzo delle risorse, per semplificare la gestione dei progetti, i processi relativi al personale e la gestione della capacità.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource, time sheet
ms.date: 10/01/2021
ms.author: edupont
ms.openlocfilehash: 72618aaeddae0a72a0c699f19a04a388ced0b9c1
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2021
ms.locfileid: "7589209"
---
# <a name="set-up-time-sheets"></a>Impostare fogli presenze

I fogli presenze di [!INCLUDE[prod_short](includes/prod_short.md)] consentono di gestire la registrazione del tempo in incrementi settimanali di sette giorni. Questi fogli possono essere usati per tenere traccia del tempo utilizzato nelle commesse e per registrare la semplice registrazione del tempo risorsa. Prima di poter utilizzare i fogli presenze, è necessario specificare come si desidera impostarli e configurarli.

Dopo aver impostato la modalità con cui l'organizzazione utilizzerà i fogli presenze, è possibile specificare se e come approvarli. In base alle esigenze dell'organizzazione, è possibile indicare:

* Uno o più utenti come amministratore dei fogli presenze e come responsabile approvazione di tutti i fogli presenze.
* Un responsabile approvazione del foglio presenze di ogni risorsa.

Una volta impostati dei fogli presenze, è possibile creare fogli presenze per le risorse, assegnarli alle righe di pianificazione commessa e registrare le righe dei fogli presenze. Per ulteriori informazioni, vedere [Utilizzare i fogli presenze](projects-how-use-time-sheets.md).  

## <a name="set-up-time-sheets-with-the-assisted-setup-guide"></a>Impostare i fogli di presenza con la guida all'impostazione assistita

[!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]

A partire dalla release 2021 wave 2, puoi usare una guida di configurazione assistita per aiutarti a impostare i fogli di presenza.  

> [!TIP]
> È necessario abilitare l'**aggiornamento delle funzionalità: Nuova funzione di esperienza del foglio di presenza** nella pagina di [gestione delle funzionalità](https://businesscentral.dynamics.com/?page=2610) per usare questa funzione.
>
> La stessa funzione facilita anche la gestione dei fogli di presenza su un dispositivo mobile.

La guida all'installazione assistita vi porta attraverso i seguenti passi:

1. Impostare i partecipanti nei processi dei fogli di presenza
2. Specificare il primo giorno di una settimana lavorativa in questa organizzazione

    Il primo giorno di una settimana lavorativa sarà il primo giorno predefinito per tutti i fogli di presenza.
3. Specificare la persona che amministra i fogli di presenza

    Questa persona può modificare e cancellare tutti i fogli di presenza. Opzionalmente, aggiungi lo stesso ruolo ad altre persone nella pagina **Configurazione utente** .
4. Impostare le risorse che useranno i fogli di presenza e le persone che approveranno i fogli di presenza

    > [!NOTE]
    > Per i progetti e i lavori, gli utenti dei fogli di presenza sono *risorse*, non dipendenti. Quindi, per essere in grado di tracciare il lavoro dei tuoi dipendenti, devi associare le risorse ai dipendenti nella guida di configurazione.

Alla fine della guida alla configurazione, puoi scegliere di lasciare che [!INCLUDE [prod_short](includes/prod_short.md)] crei i fogli di presenza in base alla tua configurazione. In alternativa, esegui di nuovo la guida all'installazione assistita o completa l'installazione manualmente.  

## <a name="set-up-time-sheets-manually"></a>Impostare manualmente i fogli di presenza

Le sezioni seguenti descrivono come impostare i fogli di presenza se non si usa la guida di impostazione assistita **Impostare i fogli presenze** .  

### <a name="to-set-up-general-information-for-time-sheets-manually"></a>Per impostare manualmente le informazioni generali per i fogli di presenza

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup risorse**, quindi scegli il collegamento correlato.  
2. Compilare i campi, se necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Per il campo **Foglio presenze per approvazione commesse** selezionare una delle opzioni indicate di seguito.

| Opzione | Descrizione |
| --- | --- |
| **Mai** |Il foglio presenze viene approvato dall'utente indicato nel campo **ID utente resp. approvazione foglio presenze** nella scheda risorsa. |
| **Sempre** |Il foglio presenze viene approvato dall'utente indicato nel campo **Persona responsabile** nella scheda commessa. |
| **Solo macchina** |Se il foglio presenze della macchina è collegato a una commessa, il foglio presenze viene approvato dall'utente indicato nel campo **Persona responsabile** della scheda commessa. Se il foglio presenze della macchina è collegato a una risorsa, il foglio presenze viene approvato dall'utente indicato nel campo **ID utente resp. approvazione foglio presenze** della scheda risorsa. |

### <a name="to-assign-a-time-sheet-administrator-manually"></a>Per assegnare manualmente un amministratore del foglio presenze

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Setup utente**, quindi scegli il collegamento correlato.  
2. Aggiungere un nuovo utente se la lista degli utenti non include la persona che si desidera nominare come amministratore del foglio presenze. Per ulteriori informazioni, vedere [Assegnare autorizzazioni a utenti e gruppi](ui-define-granular-permissions.md).
3. Selezionare un utente come amministratore del foglio presenze, quindi selezionare la casella di controllo **Amministratore foglio presenze**.  

> [!TIP]  
> Si consiglia di designare un solo utente come amministratore del foglio presenze di un'azienda. Nella procedura riportata di seguito, si impostano un proprietario e un responsabile approvazione del foglio presenze dove il responsabile approvazione è assegnato a ciascuna risorsa.  

### <a name="to-assign-a-time-sheets-owner-and-approver-manually"></a>Per assegnare manualmente un proprietario e un approvatore di fogli orari

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") immetti **Risorse**, quindi scegli il collegamento correlato.
2. Selezionare la risorsa per cui si desidera impostare la possibilità di utilizzare i fogli presenze, quindi selezionare la casella di controllo **Usa foglio presenze**.  
3. Nel campo **ID utente proprietario foglio presenze** immettere l'ID del proprietario del foglio presenze. Il proprietario può immettere l'utilizzo del tempo in un foglio presenze e inviarlo per l'approvazione. In generale quando la risorsa è una persona, è anche il proprietario.  
4. Nel campo **ID utente resp. approvazione foglio presenze** immettere l'ID del responsabile approvazione del foglio presenze. Il responsabile approvazione può approvare, rifiutare o riaprire un foglio presenze.  

> [!NOTE]  
> Non è possibile modificare l'ID del responsabile approvazione del foglio presenze in caso di fogli presenze non ancora elaborati e con lo stato **Inviato** o **Aperto**.

## <a name="see-also"></a>Vedere anche

[Utilizzare i fogli presenze per le commesse](projects-how-use-time-sheets.md)  
[Per creare fogli di presenza](projects-how-use-time-sheets.md#to-create-time-sheets)  
[Registrare il consumo o l'uso per i lavori](projects-how-record-job-usage.md)  
[Impostazione della Gestione progetti](projects-setup-projects.md)  
[Gestione progetti](projects-manage-projects.md)  
[Finanze](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzo di [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]