---
title: Suggerimenti e consigli - RapidStart Services | Microsoft Docs
description: Quando si configurano le società utilizzando RapidStart Services, vi sono alcuni suggerimenti e trucchi che è possibile adottare per semplificare l'implementazione.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: acdac865286577b30f9fe036cca8a50eb7e143a0
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/03/2019
ms.locfileid: "2878988"
---
# <a name="tips-and-tricks-rapidstart-services"></a>Suggerimenti e consigli: RapidStart Services
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

## <a name="see-also"></a>Vedere anche  
[Impostazione una società con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Amministrazione](admin-setup-and-administration.md)
