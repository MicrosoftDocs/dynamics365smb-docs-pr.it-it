---
title: Impostare o modificare il piano dei conti (video)
description: Informazioni su come configurare il piano dei conti per mostrare i conti di contabilità che memorizzano i dati finanziari.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'COA, cha of acc'
ms.search.form: '16, 17, 18, 118, 386, 391'
ms.date: 12/19/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="set-up-or-change-the-chart-of-accounts"></a>Impostare o modificare il piano dei conti

Il piano dei conti mostra i conti di contabilità che memorizzano i dati finanziari. [!INCLUDE[prod_short](includes/prod_short.md)] include un piano dei conti standard pronto per supportare l'azienda. Tuttavia, puoi modificare i conti predefiniti e aggiungere nuovi conti.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="add-or-change-accounts"></a>Aggiungere o cambiare conti

Nel piano dei conti, puoi aprire ogni conto di contabilità generale (C/G) e aggiungere o modificare le impostazioni. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 

In caso di necessità è possibile utilizzare più di una riga per il nome di un conto C/G. Nella pagina **Scheda conto C/G** nel gruppo **Conto** scegli **Testi estesi**, quindi compila una o più righe con il nome del conto e il testo copiato.  

Per i conti di tipo **Totale** compila il campo **Totale**. Per i conti di tipo **Totale finale** questo campo viene compilato automaticamente tramite la funzione di indentazione. Dopo aver impostato tutti gli account, scegli l'azione **Elabora**, quindi scegli **Indenta piano dei conti**.  

> [!IMPORTANT]
> Se le definizioni per i conti **Totale Finale** sono state immesse nei campi **Totale** prima di eseguire la funzione di indentazione, sarà necessario inserirle nuovamente in seguito poiché questa funzione sovrascrive i valori in tutti i campi **Totale finale**.

## <a name="delete-accounts"></a>Eliminare conti

È possibile eliminare un conto di contabilità generale. Tuttavia, prima che venga eliminato, è necessario soddisfare le seguenti condizioni:  

* Il saldo nel conto deve essere pari a zero.  
* Nel campo **Consenti Eliminaz. Conti C/G Anteriori a** della pagina **Setup Contabilità Generale** deve essere impostata una data ed è necessario che il conto non includa movimenti contabili in tale data o dopo tale data.  
* Se il campo **Verifica Uso Conti C/G** della pagina **Setup Contabilità Generale** è selezionato, il conto non deve essere utilizzato in tutte le categorie di registrazione o impostazioni delle registrazioni.  

[!INCLUDE[prod_short](includes/prod_short.md)] impedisce di eliminare un conto di contabilità generale che memorizza i dati necessari per il piano dei conti.  

Puoi anche specificare quando consentire alle persone di eliminare gli account. Nella pagina **Setup contabilità generale**, l'interruttore **Blocca eliminazione conti C/G** funziona insieme alla data nel campo **Verifica eliminazione conti C/G posteriori a** per fungere da convalida aggiuntiva. Se attivi l'interruttore **Blocca eliminazione conti C/G è**, non è possibile eliminare i conti C/G con movimenti contabili successivi alla data presente nel campo **Verifica eliminazione conti C/G posteriori a**. Per eliminare un account di questo tipo, qualcuno con accesso alla pagina **Setup contabilità generale** deve disattivare l'interruttore **Blocca eliminazione conti C/G**.  

L'attivazione del campo **Blocca eliminazione conti C/G** spesso è una procedura consigliata, così come l'impostazione della data nel campo **Verifica eliminazione conti C/G posteriori a**, ad esempio la data entro la quale ti viene richiesto di archiviare i dati finanziari.  

### <a name="video-guidance"></a>Guida video

Questo video mostra come specificare se e quando gli utenti possono eliminare i conti CoGe.

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1g3oY]

## <a name="see-also"></a>Vedi anche

[Contabilità generale e piano dei conti](finance-general-ledger.md)  
[Riconciliazione dei conti correnti bancari](bank-manage-bank-accounts.md)  
[Utilizzare le dimensioni](finance-dimensions.md)  
[Importazione dei dati aziendali da altri sistemi contabili](across-import-data-configuration-packages.md)  
[Utilizzare i report finanziari](bi-how-work-account-schedule.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Chiudere i conti del conto economico nella versione francese](LocalFunctionality/France/how-to-close-income-statement-accounts.md)  
[Stampare il conto economico nella versione australiana](LocalFunctionality/Australia/how-to-print-income-statements.md)  
[Stampare il conto economico nella versione della Nuova Zelanda](LocalFunctionality/NewZealand/how-to-print-income-statements.md)  
[Impostare e chiudere i saldi di conto economico nella versione spagnola](LocalFunctionality/Spain/how-to-set-up-and-close-income-statement-balances.md)  
[Indentare e convalidare il piano dei conti nella versione spagnola](LocalFunctionality/Spain/how-to-indent-and-validate-chart-of-accounts.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
