---
title: Modelli di proprietà dei dati per la sincronizzazione
description: Le società sono sia persone giuridiche che entità aziendali e vengono utilizzate per proteggere e visualizzare i dati aziendali.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'CDS, Dataverse, integration, sync'
ms.date: 04/01/2021
ms.author: bholtorf
---

# Modelli di proprietà dei dati per la sincronizzazione

[!INCLUDE[prod_short](includes/cds_long_md.md)] richiede di specificare un proprietario per i dati archiviati. Per ulteriori informazioni, vedi [Tipi di tabelle](/powerapps/maker/data-platform/types-of-entities) nella documentazione di Power Apps. Quando si imposta l'integrazione tra [!INCLUDE[prod_short](includes/cds_long_md.md)] e [!INCLUDE[prod_short](includes/prod_short.md)] è necessario scegliere la proprietà **Utente o team** per i record sincronizzati. Le azioni che possono essere eseguite su questi record possono essere controllate a livello di utente. <!--We recommend the Team ownership model because it makes it easier to manage ownership for multiple people.NO LONGER TRUE IN DATAVERSE-->

## Proprietà del team
In [!INCLUDE[prod_short](includes/prod_short.md)], una società è una persona giuridica e una tabella aziendale che offre modi per proteggere e visualizzare i dati aziendali. Gli utenti lavorano sempre nel contesto di una società. In [!INCLUDE[prod_short](includes/cds_long_md.md)] ciò che più si avvicina a questo concetto è la tabella Business Unit, che non ha implicazioni legali o commerciali.

Poiché le Business Unit non hanno implicazioni legali e commerciali, non è possibile forzare una mappatura uno a uno (1: 1) per sincronizzare i dati tra una società e una Business Unit, a senso unico o bidirezionale. Per rendere possibile la sincronizzazione, quando si abilita la sincronizzazione per una società in [!INCLUDE[prod_short](includes/prod_short.md)], succede quanto segue in [!INCLUDE[prod_short](includes/cds_long_md.md)]:

* Creiamo una tabella aziendale equivalente alla tabella aziendale in [!INCLUDE[prod_short](includes/prod_short.md)]. Il nome della società presenta il suffisso "ID società BC". Ad esempio, Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Creiamo una Business Unit predefinita con lo stesso nome della società. Ad esempio, Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Creiamo un team proprietario separato con lo stesso nome della società e lo associamo alla Business Unit. Il nome del team è preceduto dal prefisso "BCI -." Ad esempio, BCI - Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* I record creati e sincronizzati con [!INCLUDE[prod_short](includes/cds_long_md.md)] sono assegnati al team "Proprietario BCI" collegato alla Business Unit.

> [!NOTE]
> Se si rinomina una società in [!INCLUDE[prod_short](includes/prod_short.md)], i nomi della società, dell'attività e del team che creiamo automaticamente [!INCLUDE[prod_short](includes/cds_long_md.md)] non sono aggiornati. Poiché per l'integrazione viene utilizzato solo l'ID società, ciò non influisce sulla sincronizzazione. Se si desidera che i nomi corrispondano, è necessario aggiornare la società, la Business Unit e il team in [!INCLUDE[prod_short](includes/cds_long_md.md)].

L'immagine seguente mostra un esempio di questa configurazione dei dati in [!INCLUDE[prod_short](includes/cds_long_md.md)].

![La Business Uni radice è in cima, i team sono al centro e le società sono in fondo.](media/cds_bu_team_company.png)

In questa configurazione, i record relativi alla società Cronus US saranno di proprietà di un team collegato alla Business Unit Cronus US in [!INCLUDE[prod_short](includes/cds_long_md.md)]. Gli utenti che possono accedere a quella Business Unit tramite un ruolo di sicurezza impostato sulla visibilità a livello di Business Uni in [!INCLUDE[prod_short](includes/cds_long_md.md)] possono ora vedere tali record. L'esempio seguente mostra come utilizzare i team per fornire l'accesso a tali record.

* Il ruolo di Responsabile delle vendite è assegnato ai membri del team di vendita di Cronus US.
* Gli utenti che hanno il ruolo di Responsabile delle vendite possono accedere ai record degli account per i membri della stessa Business Unit.
* Il team di vendita di Cronus US è collegato alla Business Unit Cronus US menzionata in precedenza. I membri del team di vendita di Cronus US possono vedere qualsiasi account di proprietà dall'utente Cronus US, che proviene dalla tabella aziendale Cronus US in [!INCLUDE[prod_short](includes/prod_short.md)].

Tuttavia, la mappatura 1: 1 tra Business Unit, società e team è solo un punto di partenza, come mostrato nella seguente immagine.

![Il ruolo di sicurezza controlla la visibilità dei dati.](media/cds_bu_team_company_2.png)

In questo esempio, viene creata una nuova Business Unit radice EUR (Europa) in [!INCLUDE[prod_short](includes/cds_long_md.md)] come padre di Cronus DE (Gernamy) e Cronus ES (Spagna). La Business Unit EUR non è correlata alla sincronizzazione. Tuttavia, può consentire ai membri del team di vendita EUR di accedere ai dati dell'account sia in Cronus DE che in Cronus ES impostando la visibilità dei dati su **BU padre/figlio** sul ruolo di sicurezza associato in [!INCLUDE[prod_short](includes/cds_long_md.md)].

La sincronizzazione determina a quale team devono appartenere i record. Questo è controllato dal campo **Team proprietario predefinito** nella riga BCI. Quando un record BCI è abilitato per la sincronizzazione, viene automaticamente creata la Business Unit e il team proprietario associati (se non esiste già) e viene impostato il campo **Team proprietario predefinito**. Quando la sincronizzazione è abilitata per una tabella, gli amministratori possono cambiare il team proprietario, ma è sempre necessario assegnare un team.

> [!NOTE]
> I record diventano di sola lettura dopo che una società è stata aggiunta e salvata, quindi assicurati di scegliere la società corretta.

## Scelta di una Business Unit diversa
È possibile modificare la selezione della Business Unit se si utilizza il modello di proprietà Team. Se si utilizza il modello di proprietà Persona, la Business Unit predefinita è sempre selezionata. 

Se si sceglie un'altra Business Unit, ad esempio quella creata in precedenza in [!INCLUDE[prod_short](includes/cds_long_md.md)], manterrà il nome originale. Cioè, non verrà aggiunto il suffisso con l'ID società. Creeremo un team che utilizza la convenzione di denominazione.

Quando si cambia una Business Unit, è possibile scegliere solo le Business Unit che si trovano a un livello al di inferiore alla Business Unit principale.

## Proprietà della persona
Se scegli il modello di proprietà Persona, devi specificare ciascun venditore che sarà proprietario di nuovi record. La Business Unit e il team vengono creati come descritto nella sezione precedente [Proprietà del team](admin-cds-company-concept.md#team-ownership).

La Business Unit predefinita viene utilizzata quando viene scelto il modello di proprietà Persona e non è possibile scegliere un'altra Business Unit. Il team associato alla Business Unit predefinita disporrà di record per tabelle comuni, come la tabella Prodotto, che non sono correlate a specifici venditori.

Quando si associano gli agenti in [!INCLUDE[prod_short](includes/prod_short.md)] agli utenti in [!INCLUDE[prod_short](includes/cds_long_md.md)], [!INCLUDE[prod_short](includes/prod_short.md)] aggiungerà l'utente al team predefinito in [!INCLUDE[prod_short](includes/cds_long_md.md)]. È possibile verificare che gli utenti siano stati aggiunti guardando la colonna **Membro del team predefinito** nella pagina **Utenti - Common Data Service**. Se l'utente non viene aggiunto, è possibile aggiungerlo manualmente utilizzando l'azione **Aggiungi utenti associati al team**. Per ulteriori informazioni, vedere [Sincronizzazione dei dati in Business Central con Dataverse](admin-synchronizing-business-central-and-sales.md).

## Vedere anche
[Informazioni su [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-common-data-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]