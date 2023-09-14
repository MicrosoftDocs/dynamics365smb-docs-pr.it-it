---
title: Condividere contatti tra Business Central e Outlook
description: Questo servizio è completamente integrato con Microsoft 365 pertanto è possibile condividere i contatti tra Outlook e Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'contacts, Microsoft 365'
ms.search.form: '6700, 5320, 5300, 5301, 5302, 5303, 5304, 5305, 5306, 5307, 5308, 5309, 5310, 5311'
ms.date: 03/17/2023
ms.author: bholtorf
---
# Sincronizzare i contatti di Business Central con i contatti di Microsoft Outlook

Puoi impostare la sincronizzazione dei contatti in modo che i tuoi contatti di [!INCLUDE[prod_short](includes/prod_short.md)] abbiano le stesse informazioni dei contatti in Microsoft Outlook. Ad esempio, se sei un addetto alle vendite, potresti lavorare in Outlook e [!INCLUDE[prod_short](includes/prod_short.md)] allo stesso tempo. Se i contatti sono uguali in entrambi i programmi, il lavoro è più semplice.  

Per impostazione predefinita, i contatti che stai sincronizzando vengono mantenuti in una cartella **Business Central** nei tuoi Preferiti nel riquadro delle cartelle in Outlook. La cartella Business Central può semplificare l'identificazione dei contatti che stai sincronizzando. Puoi impostare i filtri per sincronizzare solo contatti specifici da [!INCLUDE[prod_short](includes/prod_short.md)] a Outlook. Dopo aver impostato la sincronizzazione, puoi sincronizzare manualmente o automatizzare il processo per sincronizzare in base a una pianificazione.  

## Prerequisiti

- Il profilo utente in [!INCLUDE[prod_short](includes/prod_short.md)] deve specificare l'account e-mail di Microsoft 365.

  È possibile controllare questa impostazione nella sezione di **autenticazione Microsoft 365** del profilo utente nell'elenco **Utenti**.
- Con [!INCLUDE[prod_short](includes/prod_short.md)], hai configurato la sincronizzazione dei contatti come descritto in [Configurare la sincronizzazione dei contatti con Outlook per Business Central locale](admin-contact-sync-setup-onprem.md)

## Impostare la sincronizzazione

È possibile definire come sincronizzare i contatti con Outlook nella pagina **Setup sincronizzazione con Exchange** in [!INCLUDE[prod_short](includes/prod_short.md)]. 

Nella pagina **Setup sincronizzazione con Exchange** è possibile verificare che la connessione a Exchange funzioni e quindi configurare la sincronizzazione dei contatti. Dalla pagina **Setup sincronizzazione con Exchange** puoi aprire la pagina **Setup sincronizzazione contatti** e avviare la sincronizzazione. Facoltativamente, imposta un filtro per specificare i contatti da sincronizzare. Ad esempio, è possibile impostare un filtro in base a nome, tipo, azienda e così via. È inoltre possibile modificare il nome predefinito della cartella di Outlook in cui verranno sincronizzati i contatti.  

Ogni collega può anche configurare la propria sincronizzazione di Exchange e impostare i propri filtri sui contatti da sincronizzare.  

Dopo aver configurato la sincronizzazione, è possibile sincronizzare manualmente le modifiche al contatto oppure automatizzare il processo impostando una voce della coda dei lavori. Per ulteriori informazioni sull'automazione, vedi la sezione successiva in questo articolo.

### Automazione della sincronizzazione

È possibile creare un movimento coda processi che sincronizzerà i contatti in base a una pianificazione definita dall'utente. Per ulteriori informazioni, vedere [Utilizzare le code processi per pianificare i task](admin-job-queues-schedule-tasks.md). 

La tabella seguente elenca le impostazioni della pagina **Scheda movimento coda processi** dedicata alla sincronizzazione dei contatti:

|Campo|Impostazione per la sincronizzazione dei contatti|
|-----|-----|
|Tipo di oggetto da eseguire|Codeunit|
|ID oggetto da eseguire|6700|

## Sincronizzare i contatti

Se sei abituato a utilizzare i contatti in [!INCLUDE[prod_short](includes/prod_short.md)], sarà semplice avviare la sincronizzazione manualmente ogni volta che desideri dall'elenco **Contatti**. Esistono due modi per sincronizzare i contatti:

* **Sincronizza con Microsoft 365**

  Sincronizza tutte le modifiche di [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft 365 effettuate dopo l'ultima sincronizzazione in base all'ultima data di modifica. Inoltre, i nuovi contatti di Microsoft 365 verranno sincronizzati in [!INCLUDE[prod_short](includes/prod_short.md)]. Questa azione è in genere più veloce di una sincronizzazione completa. 

* **Sincronizzazione completa con Microsoft 365**

  Sincronizza tutti i contatti in entrambe le direzioni indipendentemente dall'ultima data di sincronizzazione e dall'ultima data di modifica.  

In entrambi i casi, i contatti vengono sincronizzati solo da Outlook se i campi richiesti sono compilati. I campi obbligatori per la sincronizzazione con Microsoft 365 sono **Nome**, **Indirizzo e-mail** e devono essere di tipo **Persona**. [!INCLUDE[prod_short](includes/prod_short.md)] è l'origine delle informazioni di contatto, quindi se duplicate verranno salvate le informazioni di contatto di [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]
> Se elimini un contatto in Outlook, ma lo mantieni in [!INCLUDE[prod_short](includes/prod_short.md)], il contatto verrà ricreato in Outlook alla successiva sincronizzazione. 

## Vedi anche

[Prepararsi a fare affari](ui-get-ready-business.md)  
[Finanze](finance.md)  
[Vendite](sales-manage-sales.md)  
[Acquisti](purchasing-manage-purchasing.md)  
[Utilizzare i contatti (Persone) in Outlook sul Web](https://support.office.com/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]