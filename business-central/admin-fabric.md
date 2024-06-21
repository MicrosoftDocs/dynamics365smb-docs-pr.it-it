---
title: Introduzione a Microsoft Fabric e Business Central
description: 'Ottenere una panoramica dell''utilizzo di Microsoft Fabric per avere informazioni dettagliate, business intelligence e KPI dai dati di Business Central.'
author: kennienp
ms.topic: overview
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.search.form: '6316, 6317'
ms.reviewer: bholtorf
ms.date: 04/24/2024
ms.author: kepontop
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="introduction-to-microsoft-fabric-and-business-central"></a>Introduzione a Microsoft Fabric e Business Central

[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] è una soluzione di analisi end-to-end con funzionalità di servizio completo tra cui spostamento dei dati, data lake, ingegneria dei dati, integrazione dei dati, data science, analisi in tempo reale e business intelligence, il tutto supportato da una piattaforma condivisa che fornisce sicurezza dei dati, governance e conformità affidabili. La tua organizzazione non avrà più bisogno di raggruppare singoli servizi di analisi di più fornitori, in quanto avrà a disposizione una soluzione semplificata facile da connettere, integrare e utilizzare.

> [!NOTE]
> Per ulteriori informazioni sul piano di rilascio di Microsoft Fabric, vedi [aka.ms/FabricRoadmap](https://aka.ms/FabricRoadmap)
> 
> La pubblicazione regolare di questa roadmap ti aiuterà a rimanere informato su come [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] soddisfa le tue esigenze.

## <a name="where-does--fit-into-includeprod_short-analytics"></a>Integrazione di [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] nell'analisi di [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[prod_short](includes/prod_short.md)] include numerosi report pronti all'uso e funzionalità di analisi dei dati come report finanziari, apertura in Excel e modalità di analisi di elenchi e query. Consente inoltre di definire facilmente report Power BI che leggono dati da API standard e personalizzate, definire scorecard di metriche Power BI e di incorporare il tutto direttamente nel client [!INCLUDE[prod_short](includes/prod_short.md)]. Tuttavia, per i clienti con scenari di data science o business intelligence più avanzati che richiedono un'ingegneria o un'integrazione dei dati più sofisticata, [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] potrebbe essere una buona opzione. 

## <a name="onelake"></a>OneLake

Una parte fondamentale dell'offerta [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] è OneLake. OneLake è un singolo data lake logico e unificato per l'intera organizzazione. Puoi considerare OneLake come servizio OneDrive per dati. Fornisce il data lake come servizio senza doverlo creare personalmente. OneLake viene fornito automaticamente con ogni tenant di [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] senza infrastrutture da gestire. Tutti i dati che arrivano in OneLake prendono automaticamente parte alla governance dei dati pronta all'uso come la derivazione e la protezione dei dati, la certificazione e l'integrazione del catalogo. Suddivide i silos di dati consentendo a diverse parti dell'organizzazione di lavorare in modo indipendente pur continuando a contribuire allo stesso data lake.

Gli elementi di [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] archiviano i tuoi dati in OneLake in un formato di file aperto. Per dati tabulari strutturati, questo formato è *delta parquet*. Il formato delta parquet consente a tutti i motori di analisi in [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] di accedere ai dati da altri motori di analisi. In questo modo, offre agli operatori di dati la flessibilità di utilizzare gli strumenti di tua scelta.

> [!NOTE]
> Prevediamo che mediante una delle nostre versioni future, i dati di [!INCLUDE[prod_short](includes/prod_short.md)] verranno resi disponibili in OneLake anche per i clienti che utilizzano [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] e [!INCLUDE[prod_short](includes/prod_short.md)] e che hanno requisiti univoci nelle aree che [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] supporta. La tempistica dipenderà da quella della disponibilità generale di [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] e dei relativi componenti necessari per abilitare questa esperienza. Aggiorneremo questo articolo con una tempistica più precisa, non appena ne sapremo di più.

## <a name="see-also"></a>Vedere anche
[Utilizzo di Power BI con Business Central](admin-powerbi.md)   

[!INCLUDE[footer-include](includes/footer-banner.md)]
