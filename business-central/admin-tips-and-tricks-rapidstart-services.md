---
title: Suggerimenti e trucchi - RapidStart Services | Documenti Microsoft
description: Quando si configurano le società utilizzando RapidStart Services, vi sono alcuni suggerimenti e trucchi che è possibile adottare per semplificare l'implementazione.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6a10ab0d2e4658eba4824e44527d45cbf0f33dd8
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "936914"
---
# <a name="tips-and-tricks-rapidstart-services"></a>Suggerimenti e trucchi: servizi di RapidStart
Quando si configurano le società utilizzando RapidStart Services, vi sono alcuni suggerimenti e trucchi che è possibile adottare per semplificare l'implementazione.  

## <a name="take-advantage-of-configuration-templates"></a>Sfruttare i modelli di configurazione  
I modelli di configurazione consentono di migliorare il processo dell'implementazione rapida. Utilizzando tali modelli, è possibile includere clienti simili in segmenti e quindi elaborare un protocollo di implementazione che gestisca tutti i clienti in un segmento in modo analogo. In tal modo, è possibile collegare un livello di preconfigurazione a ciascun segmento e procedere a un'implementazione rapida.  

## <a name="configuration-questionnaires"></a>Questionari di configurazione  
Per migliorare il processo di compilazione di un questionario di configurazione, valutare di definire risposte di default per indicare le procedure ottimali.  

## <a name="batch-creation-of-journal-lines"></a>Creazione batch delle righe di registrazione  
È consigliabile utilizzare gli strumenti di migrazione dati forniti per eseguire la migrazione dei movimenti delle registrazioni. In caso contrario, se si utilizza un processo batch per creare le righe delle registrazioni, con un ambito di tempo limitato e vengono generati solo i campi precedenti al default nelle registrazioni. Il resto delle registrazioni quindi deve essere completato manualmente.  

## <a name="migrating-transactions"></a>Migrazione delle transazioni  
È consigliabile eseguire la migrazione dei bilanci di apertura nel seguente ordine.  

1.  Eseguire il migrazione dei bilanci di apertura di contabilità generale senza utilizzare i registri secondari del conto di contabilità generale. Utilizzare i conti di compensazione specifici del bilancio di apertura, un setup per ogni registro secondario. Impostare i conti di compensazione per abilitare le registrazioni dirette.  
2.  Eseguire la migrazione dei movimenti contabili clienti aperti.  
3.  Eseguire la migrazione dei movimenti contabili articoli aperti.  
4.  Eseguire la migrazione i movimenti di cespiti aperti.  

## <a name="see-also"></a>Vedi anche  
[Impostare una società con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Amministrazione](admin-setup-and-administration.md)
