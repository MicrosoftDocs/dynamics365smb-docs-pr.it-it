---
title: Mappatura di società e Business Unit | Microsoft Docs
description: Le società sono sia persone giuridiche che entità aziendali e vengono utilizzate per proteggere e visualizzare i dati aziendali.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: CDS, Common Data Service, integration, sync
ms.date: 01/17/2020
ms.author: bholtorf
ms.openlocfilehash: ccd371711a53c598279fcc981c5581be5ee9bdaf
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196877"
---
# <a name="data-ownership-models"></a>Modelli di proprietà dei dati
[!INCLUDE[d365fin](includes/cds_long_md.md)] richiede di specificare un proprietario per i dati archiviati. Per ulteriori informazioni, vedere [Proprietà delle entità](https://docs.microsoft.com/powerapps/maker/common-data-service/types-of-entities#entity-ownership) nella documentazione di Power Apps. Quando si imposta l'integrazione tra [!INCLUDE[d365fin](includes/cds_long_md.md)] e [!INCLUDE[d365fin](includes/d365fin_md.md)] devi scegliere uno dei due modelli di proprietà per i record sincronizzati:

* Team 
* Persona (utente)

Le azioni che possono essere eseguite su questi record possono essere controllate a livello di utente. Per ulteriori informazioni, vedere [Entità utente e team](https://docs.microsoft.com/powerapps/developer/common-data-service/user-team-entities). Si consiglia di utilizzare il modello di proprietà Team perché semplifica la gestione della proprietà per più persone.

## <a name="team-ownership"></a>Proprietà del team
In [!INCLUDE[d365fin](includes/d365fin_md.md)], una società è una persona giuridica e un'entità aziendale che offre modi per proteggere e visualizzare i dati aziendali. Gli utenti lavorano sempre nel contesto di una società. L'entità in [!INCLUDE[d365fin](includes/cds_long_md.md)] che più si avvicina a questo concetto è l'entità Business Unit, che non ha implicazioni legali o commerciali.

Poiché le Business Unit non hanno implicazioni legali e commerciali, non è possibile forzare una mappatura uno a uno (1: 1) per sincronizzare i dati tra una società e una Business Unit, a senso unico o bidirezionale. Per rendere possibile la sincronizzazione, quando si abilita la sincronizzazione per una società in [!INCLUDE[d365fin](includes/d365fin_md.md)], succede quanto segue in [!INCLUDE[d365fin](includes/cds_long_md.md)]:

* Creiamo un'entità aziendale equivalente all'entità aziendale in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Il nome della società presenta il suffisso "ID società BC". Ad esempio, Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Creiamo una Business Unit predefinita con lo stesso nome della società. Ad esempio, Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Creiamo un team proprietario separato con lo stesso nome della società e lo associamo alla Business Unit. Il nome del team è preceduto dal prefisso "BCI -." Ad esempio, BCI - Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* I record creati e sincronizzati con [!INCLUDE[d365fin](includes/cds_long_md.md)] sono assegnati al team "Proprietario BCI" collegato alla Business Unit.

L'immagine seguente mostra un esempio di questa configurazione dei dati in [!INCLUDE[d365fin](includes/cds_long_md.md)].

![La Business Uni radice è in cima, i team sono al centro e le società sono in fondo.](media/cds_bu_team_company.png)

In questa configurazione, i record relativi alla società Cronus US saranno di proprietà di un team collegato a Cronus US <ID> Business Unit in [!INCLUDE[d365fin](includes/cds_long_md.md)]. Gli utenti che possono accedere a quella Business Unit tramite un ruolo di sicurezza impostato sulla visibilità a livello di Business Uni in [!INCLUDE[d365fin](includes/cds_long_md.md)] possono ora vedere tali record. L'esempio seguente mostra come utilizzare i team per fornire l'accesso a tali record.

* Il ruolo di Responsabile delle vendite è assegnato ai membri del team di vendita di Cronus US.
* Gli utenti che hanno il ruolo di Responsabile delle vendite possono accedere ai record degli account per i membri della stessa Business Unit.
* Il team di vendita di Cronus US è collegato alla Business Unit Cronus US menzionata in precedenza. I membri del team di vendita di Cronus US possono vedere qualsiasi account di proprietà di Cronus US <ID>utente, che proviene dall'entità aziendale Cronus US in [!INCLUDE[d365fin](includes/d365fin_md.md)].

Tuttavia, la mappatura 1: 1 tra Business Unit, società e team è solo un punto di partenza, come mostrato nella seguente immagine.

![Il ruolo di sicurezza controlla la visibilità dei dati.](media/cds_bu_team_company_2.png)

In questo esempio, viene creata una nuova Business Unit radice EUR (Europa) in [!INCLUDE[d365fin](includes/cds_long_md.md)] come padre di Cronus DE (Gernamy) e Cronus ES (Spagna). La Business Unit EUR non è correlata alla sincronizzazione. Tuttavia, può consentire ai membri del team di vendita EUR di accedere ai dati dell'account sia in Cronus DE che in Cronus ES impostando la visibilità dei dati su **BU padre/figlio** sul ruolo di sicurezza associato in [!INCLUDE[d365fin](includes/cds_long_md.md)].

La sincronizzazione determina a quale team devono appartenere i record. Questo è controllato dal campo **Team proprietario predefinito** sul record BCI - <ID>. Quando un record BCI - <ID> è abilitato per la sincronizzazione, viene automaticamente creata la Business Unit e il team proprietario associati (se non esiste già) e viene impostato il campo **Team proprietario predefinito**. Quando la sincronizzazione è abilitata per un'entità, gli amministratori possono cambiare il team proprietario, ma è sempre necessario assegnare un team.

> [!NOTE]
> I record diventano di sola lettura dopo che una società è stata aggiunta e salvata, quindi assicurati di scegliere la società corretta.

### <a name="choosing-a-different-business-unit"></a>Scelta di una Business Unit diversa
La selezione della Business Unit può essere modificata manualmente. Se scegli un'altra unità, ad esempio quella creata in precedenza in CDS, manterrà il nome originale. Cioè, non verrà aggiunto il suffisso con l'ID società. Creeremo un team che utilizza la convenzione di denominazione.

## <a name="person-ownership"></a>Proprietà della persona
Se scegli il modello di proprietà Persona, devi specificare ciascun venditore che sarà proprietario di nuovi record. La Business Unit e il team vengono creati come descritto nella sezione precedente.  

## <a name="see-also"></a>Vedere anche
[Informazioni su [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-common-data-service.md)