---
title: Come impostare oggetti di costo | Microsoft Docs
description: Informazioni su come impostare oggetti di costo, i quali sono simili alle dimensioni relative alla contabilità generale.
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
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 725ad9ed12dd32dc1cc3257c266efa274ea964a0
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2019
ms.locfileid: "923273"
---
# <a name="set-up-cost-objects"></a>Impostare gli oggetti di costo
Gli oggetti di costo sono i progetti, i prodotti o i servizi di una società. Il grafico degli oggetti di costo è simile alle informazioni sulle dimensioni relative alla contabilità generale. È possibile impostare il grafico degli oggetti di costo nelle modalità seguenti:  

* Trasferendo i valori dimensioni nella contabilità generale al grafico degli oggetti di costo. È possibile apportare tutte le rettifiche necessarie dopo il trasferimento.  
* Creando un nuovo grafico dell'oggetto di costo che sia indipendente dalla contabilità generale o aggiungendo un nuovo oggetto di costo a un grafico degli oggetti di costo esistente. È necessario creare ogni oggetto di costo singolarmente.  

## <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a>Per trasferire i valori dimensioni dalla contabilità generale al grafico degli oggetti di costo  
1.  Impostare una dimensione come dimensione dell'oggetto di costo nella pagina **Aggiorna dimensioni contabilità industriale**. Solo i valori di questa dimensione vengono trasferiti.  
2.  Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Piano degli oggetti di costo** e quindi scegliere il collegamento correlato.  
3.  Scegliere l'azione **Ottieni oggetti di costo da dimensione** per trasferire i valori dimensioni al piano degli oggetti di costo. Con la funzione è possibile trasferire i valori dimensioni definiti nel passaggio 1.  

    > [!NOTE]  
    >  È possibile impostare il campo **Allinea dimensione oggetto di costo** per definire una sincronizzazione unidirezionale dei valori delle dimensioni della contabilità generale con il piano degli oggetti di costo. Non è possibile definire una sincronizzazione del grafico degli oggetti di costo con i valori dimensioni della contabilità generale.  

Il grafico degli oggetti di costo contiene ora tutti i valori dimensioni specificati della contabilità generale e include i titoli e i subtotali.  

## <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-page"></a>Per creare nuovi oggetti di costo nella pagina Piano degli oggetti di costo  
È possibile impostare e gestire oggetti di costo nella scheda **Scheda oggetto di costo** o nella pagina **Piano degli oggetti di costo**. In questa procedura è possibile impostare gli oggetti di costo nella pagina **Piano degli oggetti di costo**.  

1.  Aprire la pagina **Piano dei tipi di costo** in modalità di modifica.  
2.  Nel campo  **Codice** immettere il codice oggetto di costo. Tutti gli oggetti di costo devono disporre di un codice.  
3.  Nel campo **Nome** immettere il nome dell'oggetto di costo.  
4.  Fare clic sulla freccia a discesa nel campo **Tipo riga** per specificare lo scopo dell'oggetto di costo.  

    * Per gli oggetti di costo di tipo riga **Totale** compilare il campo **Totale da/a**. Utilizzare l'operatore **or**, vale a dire una riga verticale (**&#124;**), per impostare gli intervalli degli oggetti di costo.  
    * Per gli oggetti di costo del tipo di riga **Fine-Totale**, questo campo viene compilato automaticamente quando si utilizza la funzione di indentazione.  
5.  Compilare il campo **Ordinamento**.  
6.  Selezionare la successiva riga vuota per creare un nuovo oggetto di costo, quindi ripetere i passaggi da 2 a 5.  
7.  Dopo aver impostato tutti gli oggetti di costo, scegliere l'azione **Indentazione oggetti di costo**. Scegliere il pulsante **Sì**.  

> [!IMPORTANT]  
>  Se sono state immesse definizioni nei campi **Totale da/a** per gli oggetti di costo **Fine-Totale** prima di eseguire la funzione di indentazione, è necessario inserirle di nuovo. Questa funzione consente di sovrascrivere i valori in tutti i campi **Fine-Totale**.  

## <a name="see-also"></a>Vedi anche  
[Contabilizzazione dei costi](finance-manage-cost-accounting.md)  
[Definizione dei centri di costo e degli oggetti di costo per il piano dei conti](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md)   
[Saldi tra tipo di costo, centro di costo e oggetto di costo](finance-balances-between-cost-type-cost-center-and-cost-object.md)   
[Impostazione della contabilità industriale](finance-set-up-cost-accounting.md)   
[Terminologia della contabilità industriale](finance-terminology-in-cost-accounting.md)   
[Informazioni sulla contabilità industriale](finance-about-cost-accounting.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
