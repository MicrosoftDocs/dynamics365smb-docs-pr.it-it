---
title: Impostare o modificare il piano dei conti (video)
description: Il piano dei conti mostra i conti di contabilità che memorizzano i dati finanziari. Puoi modificare i conti predefiniti nel piano dei conti e aggiungere nuovi conti.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'COA, cha of acc'
ms.search.form: '16, 17, 18, 118, 386, 391'
ms.date: 01/21/2022
ms.author: edupont
---
# <a name="set-up-or-change-the-chart-of-accounts" />Impostare o modificare il piano dei conti

Il piano dei conti mostra i conti di contabilità che memorizzano i dati finanziari. [!INCLUDE[prod_short](includes/prod_short.md)] include un piano dei conti standard pronto per supportare l'azienda. Tuttavia, puoi modificare i conti predefiniti e aggiungere nuovi conti.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="add-or-change-accounts" />Aggiungere o cambiare conti

Nel piano dei conti, puoi aprire ogni conto di contabilità generale (C/G) e aggiungere o modificare le impostazioni. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 

In caso di necessità è possibile utilizzare più di una riga per il nome di un conto C/G. Nella pagina **Scheda conto C/G** nel gruppo **Conto** scegli **Testi estesi**, quindi compila una o più righe con il nome del conto e il testo copiato.  

Per i conti di tipo **Totale** compila il campo **Totale**. Per i conti di tipo **Totale finale** questo campo viene compilato automaticamente tramite la funzione di indentazione. Dopo aver impostato tutti gli account, scegli l'azione **Elabora**, quindi scegli **Indenta piano dei conti**.  

> [!IMPORTANT]
> Se le definizioni per i conti **Totale Finale** sono state immesse nei campi **Totale** prima di eseguire la funzione di indentazione, sarà necessario inserirle nuovamente in seguito poiché questa funzione sovrascrive i valori in tutti i campi **Totale finale**.

## <a name="delete-accounts" />Eliminare conti

È possibile eliminare un conto di contabilità generale. Tuttavia, prima che venga eliminato, è necessario soddisfare le seguenti condizioni:  

* Il saldo nel conto deve essere pari a zero.  
* Nel campo **Consenti Eliminaz. Conti C/G Anteriori a** della pagina **Setup Contabilità Generale** deve essere impostata una data ed è necessario che il conto non includa movimenti contabili in tale data o dopo tale data.  
* Se il campo **Verifica Uso Conti C/G** della pagina **Setup Contabilità Generale** è selezionato, il conto non deve essere utilizzato in tutte le categorie di registrazione o impostazioni delle registrazioni.  

[!INCLUDE[prod_short](includes/prod_short.md)] impedisce di eliminare un conto di contabilità generale che memorizza i dati necessari per il piano dei conti.  

## <a name="block-deletion-of-gl-accounts" />Blocca eliminazione conti C/G

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

Il secondo ciclo di rilascio del 2022 introduce un'ulteriore tutela contro la cancellazione accidentale dei conti C/G anche negli scenari in cui i criteri sono soddisfatti.  

Un nuovo campo, **Blocca eliminazione conti C/G**, è stato aggiunto alla pagina **Setup contabilità generale**. Quando è impostato su *Sì*, il campo funge da ulteriore convalida e quindi non è possibile eliminare i conti C/G con movimenti contabili successivi alla data presente nel campo **Verifica eliminazione conti C/G posteriori a**. Per eliminare tale conto, un utente con accesso alla pagina **Setup contabilità generale** deve prima impostare questo campo su *No*.  

L'impostazione del campo **Blocca eliminazione conti C/G** su *sì* può essere considerata una procedura consigliata, così come l'impostazione della data nel campo **Verifica eliminazione conti C/G posteriori a**, ad esempio la data entro la quale ti viene richiesto di archiviare i dati finanziari.  

## <a name="see-related-microsoft-trainingtrainingmoduleschart-accounts-dynamics--business-centralindex" />Vedi il relativo [training Microsoft](/training/modules/chart-accounts-dynamics-365-business-central/index)

## <a name="see-also" />Vedi anche

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

## <a name="includeprodshortincludesfreetrialmdmd" />[!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
