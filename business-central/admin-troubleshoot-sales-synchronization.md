---
title: Risoluzione dei problemi relativi agli errori di sincronizzazione
description: Questo argomento fornisce alcune indicazioni per l'identificazione e la risoluzione dei problemi e degli errori di sincronizzazione.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/14/2021
ms.author: bholtorf
---
# <a name="troubleshooting-synchronization-errors"></a>Risoluzione dei problemi relativi agli errori di sincronizzazione


Ci sono molte parti mobili coinvolte nell'integrazione di [!INCLUDE[prod_short](includes/prod_short.md)] con [!INCLUDE[prod_short](includes/cds_long_md.md)] e a volte le cose vanno male. Questo argomento evidenzia alcuni degli errori tipici che si verificano e fornisce alcuni suggerimenti su come risolverli.

Gli errori si verificano spesso a causa di un'operazione che un utente ha eseguito per i record associati o di un errore di impostazione dell'integrazione. Per gli errori relativi ai record associati, gli utenti possono risolverli da soli. Questi errori sono causati da azioni quali l'eliminazione di dati in una, ma non entrambe, le app aziendali e quindi la sincronizzazione. Per ulteriori informazioni, vedere [Visualizzare lo stato di una sincronizzazione](admin-how-to-view-synchronization-status.md).

Gli errori correlati all'impostazione dell'integrazione richiedono in genere l'attenzione dell'amministratore. È possibile visualizzare questi errori nella pagina **Errori di sincronizzazione integrazione**. 

La tabella seguente fornisce esempi di problemi tipici:  

|Problema  |Risoluzione  |
|---------|---------|
|Le autorizzazioni e i ruoli assegnati all'utente di integrazione non sono corretti. | Questo errore deriva da [!INCLUDE[prod_short](includes/cds_long_md.md)] e spesso include il seguente testo "All'utente principale (ID=\<user id>, tipo=8) manca il privilegio \<privilegeName>". Questo errore si verifica perché all'utente di integrazione manca un privilegio che gli consente di accedere a un'entità. In genere, questo errore si verifica se stai sincronizzando entità personalizzate o se hai un'app installata in [!INCLUDE[prod_short](includes/cds_long_md.md)] che richiede l'autorizzazione per accedere ad altre entità [!INCLUDE[prod_short](includes/cds_long_md.md)]. Per risolvere questo errore, assegna l'autorizzazione all'utente di integrazione in [!INCLUDE[prod_short](includes/cds_long_md.md)].<br><br> È possibile trovare il nome utente di integrazione nella pagina **Setup connessione a Dataverse**. Il messaggio di errore fornirà il nome dell'autorizzazione, che può aiutarti a identificare l'entità per cui hai bisogno dell'autorizzazione. Per aggiungere il privilegio mancante, accedi a [!INCLUDE[prod_short](includes/cds_long_md.md)] con un account amministratore e modifica il ruolo di sicurezza assegnato all'utente di integrazione. Per ulteriori informazioni, vedi [Creare o modificare un ruolo di sicurezza per gestire l'accesso](/power-platform/admin/create-edit-security-role). |
|Stai associando un record che utilizza un altro record non associato. Ad esempio, un cliente la cui valuta non è associata o un articolo per cui l'unità di misura non è associata. | È necessario prima associare il record dipendente, ad esempio una valuta o un'unità di misura, quindi riprovare l'associazione. |

Di seguito sono riportati alcuni strumenti nella pagina Errori di sincronizzazione di integrazione che possono aiutarti a risolvere manualmente questi problemi.  

* I campi **Origine** e **Destinazione** possono contenere collegamenti alla riga in cui è stato trovato l'errore. Fare clic sul collegamento per indagare sull'errore.  
* Le azioni **Elimina movimenti risalenti a più di 7 giorni prima**e **Elimina tutti i movimenti** puliranno l'elenco. In genere, si utilizzano queste azioni dopo aver risolto la causa di un errore che interessa molti record. Tuttavia, prestare attenzione. Queste azioni potrebbero eliminare errori che sono ancora rilevanti.
* L'azione **Mostra stack di chiamate errore** mostra informazioni che possono aiutare a identificare la causa dell'errore. Se non riesci a risolvere l'errore da solo e decidi di inviare una richiesta di supporto, includi le informazioni nella richiesta di supporto.

## <a name="see-also"></a>Vedere anche
[Integrazione con Microsoft Dataverse](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Impostazione di account utente per l'integrazione con Microsoft Dataverse](admin-setting-up-integration-with-dynamics-sales.md)  
[Impostare una connessione a Microsoft Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Associare e sincronizzare i record manualmente](admin-how-to-couple-and-synchronize-records-manually.md)  
[Visualizzare lo stato di una sincronizzazione](admin-how-to-view-synchronization-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
