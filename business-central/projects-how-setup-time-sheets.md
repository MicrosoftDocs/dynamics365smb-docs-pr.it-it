---
title: Impostare i fogli di presenza e la loro approvazione
description: 'Si possono impostare i fogli presenze per tenere traccia del tempo utilizzato per attività e progetti al fine di semplificare la gestione dei progetti, i processi relativi al personale e la gestione della capacità'
ms.reviewer: jswymer
author: brentholtorf
ms.author: bholtorf
mw.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: 'project management, capacity, staff, resource, time sheet'
ms.search.form: '977, 462, 76, 77, 462'
ms.date: 07/27/2023
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="set-up-time-sheets"></a>Impostare fogli presenze

I fogli presenze di [!INCLUDE[prod_short](includes/prod_short.md)] consentono di gestire la registrazione del tempo in incrementi settimanali di sette giorni. Questi fogli possono essere usati per tenere traccia del tempo utilizzato nei progetti e per registrare semplicemente il tempo risorsa. Prima di utilizzare i fogli presenze, è necessario specificare quali utenti invieranno i fogli presenze e come si desidera configurare tali fogli.  

> [!TIP]
> Le persone che usano dei fogli presenze sono delle *risorse*. Ad esempio, puoi utilizzare i fogli presenze per tenere traccia del lavoro dei non dipendenti. Per tenere traccia del lavoro dei dipendenti o delle loro assenze, devi associare i dipendenti alle risorse. È disponibile una guida al setup assistito per aiutarti ad eseguire tale operazione. Per informazioni sulla guida, vedi [Impostare i fogli presenze con la guida al setup assistito](#set-up-time-sheets-with-the-assisted-setup-guide).  

Eventualmente, specifica se e come vengono approvati i fogli presenze. In base alle esigenze dell'organizzazione, è possibile indicare:

* Uno o più utenti come amministratore dei fogli presenze e come responsabile approvazione di tutti i fogli presenze.
* Un responsabile approvazione del foglio presenze di ogni risorsa.

Una volta configurati i fogli presenze, è possibile creare fogli presenze per le risorse, che possono registrare le righe dei fogli presenze. Facoltativamente, assegnare i fogli presenze alle righe di pianificazione commessa. Per saperne di più, vedi [Usare i fogli presenze](projects-how-use-time-sheets.md).  

## <a name="set-up-time-sheets-with-the-assisted-setup-guide"></a>Impostare i fogli di presenza con la guida all'impostazione assistita

Per impostare i fogli presenze è disponibile una guida al setup assistito.  

> [!TIP]
> Se disponi di una versione precedente al ciclo di rilascio 1 del 2023 (v22), devi abilitare la funzionalità **Aggiornamento funzionalità: nuova esperienza del foglio presenze** nella pagina [Gestione funzionalità](https://businesscentral.dynamics.com/?page=2610) per usare tale guida.
>
> Questa impostazione ti consente anche di utilizzare i fogli presenze nei dispositivi mobili.

Apri la guida alla configurazione assistita **Impostare fogli presenze** dalla pagina [Setup assistito](https://businesscentral.dynamics.com/?page=1801).

La guida all'installazione assistita vi porta attraverso i seguenti passi:

1. Impostare i partecipanti nei processi dei fogli presenze.

    La prima pagina della guida mostra il numero di utenti nell'istanza di [!INCLUDE [prod_short](includes/prod_short.md)] in uso. Mostra anche altre informazioni obbligatorie e facoltative.  
2. Specificare il primo giorno di una settimana lavorativa in questa organizzazione.

    Il primo giorno di una settimana lavorativa sarà il primo giorno predefinito per tutti i fogli di presenza.
3. Specificare la persona che amministra i fogli presenze.

    Questa persona può modificare e cancellare tutti i fogli di presenza. Opzionalmente, aggiungi lo stesso ruolo ad altre persone nella pagina **Configurazione utente** .
4. Impostare le risorse che useranno i fogli presenze e le persone che approveranno i fogli presenze.

Alla fine della guida alla configurazione, puoi scegliere di lasciare che [!INCLUDE [prod_short](includes/prod_short.md)] crei i fogli di presenza in base alla tua configurazione. Visualizzare i nuovi fogli presenze nella pagina **Fogli presenze**, che è possibile aprire [qui](https://businesscentral.dynamics.com/?page=951). In alternativa, esegui di nuovo la guida all'installazione assistita o completa l'installazione manualmente.

> [!IMPORTANT]
> Se utilizzi il primo ciclo di rilascio del 2023 (v22) o successivo, per assicurarti di poter gestire i fogli presenze nei dispositivi mobili, devi attivare manualmente l'opzione **Usa la nuova esperienza del foglio presenze** per il setup dei fogli presenze, come descritto nella procedura successiva.

## <a name="set-up-time-sheets-manually"></a>Impostare manualmente i fogli di presenza

Le sezioni seguenti descrivono come impostare i fogli presenze se non usi la guida al setup assistito **Impostare fogli presenze**.  

### <a name="to-set-up-general-information-for-time-sheets-manually"></a>Per impostare manualmente le informazioni generali per i fogli di presenza

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup risorse**, quindi scegli il collegamento correlato.  
1. Compila i campi in base alle esigenze. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!IMPORTANT]
   > Se utilizzi il primo ciclo di rilascio del 2023 (v22) o successivo, per assicurarti di poter gestire i fogli presenze nei dispositivi mobili, attiva l'opzione **Usa la nuova esperienza del foglio presenze**.
1. Per il campo **Foglio presenze per approvazione commesse** selezionare una delle opzioni indicate di seguito.

| Opzione | Descrizione |
| --- | --- |
| **Mai** |Il foglio presenze viene approvato dall'utente indicato nel campo **ID utente resp. approvazione foglio presenze** nella scheda risorsa. |
| **Sempre** |Il foglio presenze viene approvato dall'utente indicato nel campo **Persona responsabile** nella scheda commessa. |
| **Solo macchina** |Se il foglio presenze della macchina è collegato a una commessa, il foglio presenze viene approvato dall'utente indicato nel campo **Persona responsabile** della scheda commessa. Se il foglio presenze della macchina è collegato a una risorsa, il foglio presenze viene approvato dall'utente indicato nel campo **ID utente resp. approvazione foglio presenze** della scheda risorsa. |

### <a name="to-assign-a-time-sheet-administrator-manually"></a>Per assegnare manualmente un amministratore del foglio presenze

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup utente**, quindi scegli il collegamento correlato.  
3. Seleziona l'utente che sarà l'amministratore dei fogli presenze, quindi seleziona la casella di controllo **Amministratore foglio presenze**.  

> [!TIP]  
> Yi consigliamo di designare un solo utente come amministratore dei fogli presenze di una società. Nella procedura riportata di seguito, si impostano un proprietario e un responsabile approvazione del foglio presenze dove il responsabile approvazione è assegnato a ciascuna risorsa.  

### <a name="to-assign-a-time-sheets-owner-and-approver-manually"></a>Per assegnare manualmente un proprietario e un approvatore di fogli orari

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Risorse**, quindi scegli il collegamento correlato.
2. Seleziona la risorsa per cui desideri impostare la possibilità di utilizzare i fogli presenze, quindi seleziona la casella di controllo **Usa foglio presenze**.  
3. Nel campo **ID utente proprietario foglio presenze** immettere l'ID del proprietario del foglio presenze. Il proprietario può immettere l'utilizzo del tempo in un foglio presenze e inviarlo per l'approvazione. In generale quando la risorsa è una persona, è anche il proprietario.  
4. Nel campo **ID utente resp. approvazione foglio presenze** immettere l'ID del responsabile approvazione del foglio presenze. Il responsabile approvazione può approvare, rifiutare o riaprire un foglio presenze.  

> [!NOTE]  
> Non puoi modificare l'ID del responsabile dell'approvazione del foglio presenze in caso di fogli presenze non ancora elaborati e con lo stato **Inviato** o **Aperto**.

## <a name="see-also"></a>Vedere anche

[Utilizzare i fogli presenze per i progetti](projects-how-use-time-sheets.md)  
[Come creare fogli di presenza](projects-how-use-time-sheets.md#to-create-time-sheets)  
[Registrare il consumo o l'uso per i progetti](projects-how-record-job-usage.md)  
[Impostazione della Gestione progetti](projects-setup-projects.md)  
[Gestione progetti](projects-manage-projects.md)  
[Finanze](finance.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Vendite](sales-manage-sales.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
