---
title: Creare una scheda cliente per registrare un nuovo cliente | Documenti Microsoft
description: Descrive come creare una scheda cliente per registrare informazioni su ogni nuovo cliente a cui sono rivolte le vendite.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 06/24/2020
ms.author: sgroespe
ms.openlocfilehash: cc48c7c55edac8af9333dd04661a828c528621b8
ms.sourcegitcommit: 63102669366eb26f9c32729848170bc2e5c4d6ae
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/25/2020
ms.locfileid: "3503975"
---
# <a name="register-new-customers"></a>Registrare nuovi clienti

I clienti sono l'origine del reddito. È necessario registrare ogni cliente, cui è stata effettuata una vendita, come una scheda cliente. Le schede cliente contengono le informazioni richieste per la vendita dei prodotti al cliente. Per ulteriori informazioni, vedere [Fatturare le vendite](sales-how-invoice-sales.md) e [Registrare nuovi articoli](inventory-how-register-new-items.md).  

Prima di registrare nuovi clienti, è necessario impostare vari codici di vendita selezionabili durante la compilazione delle schede cliente. Per ulteriori informazioni, vedere [Setup Vendite](sales-setup-sales.md).

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers"></a>Aggiunta di nuovi clienti

Per registrare un nuovo cliente, è necessario compilare una scheda cliente. È possibile stabilire modelli per profili di clienti diversi oppure aggiungere clienti senza modelli.  

> [!NOTE]  
> Se esistono i modelli cliente per diversi tipi di cliente, quando si crea una nuova scheda cliente, verrà visualizzata una pagina automaticamente da cui sarà possibile selezionare un modello appropriato. Se esiste solo un modello cliente, allora le nuove schede cliente utilizzeranno sempre tale modello.  

### <a name="to-create-a-new-customer-card"></a>Per creare una nuova scheda cliente

1. Scegliere l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immettere **Clienti** e quindi scegliere il collegamento correlato.  
2. Nella pagina **Clienti** scegliere l'azione **Nuovo**.

    Se esiste solo un modello cliente, allora verrà visualizzata una nuova scheda cliente con alcuni campi compilati con le informazioni derivanti dal modello.

    Se esistono più modelli cliente, verrà aperta una pagina nella quale sarà possibile selezionare un modello cliente. In questo caso, seguire i due passaggi successivi.
3. Nella pagina **Selezionare un modello per un nuovo cliente** scegliere il modello da utilizzare per la nuova scheda cliente.
4. Scegliere il pulsante **OK**. Una nuova scheda cliente verrà visualizzata con alcuni campi compilati con le informazioni del modello.  
5. Continuare a compilare o a modificare i campi della scheda cliente in base alle necessità. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Nella Scheda dettaglio **Prezzi vendita** è possibile visualizzare gli sconti o i prezzi speciali che si concedono al cliente se vengono soddisfatti determinati criteri come un articolo, la quantità minima di ordine o la data di scadenza. Ogni riga rappresenta un prezzo speciale o uno sconto riga. Ogni colonna rappresenta un criterio da applicare per garantire il prezzo speciale immesso nel campo **Prezzo unitario** o lo sconto riga immesso nel campo **Sconto riga**. Per ulteriori informazioni, vedere [Registrazione di prezzi, sconti e contratti di pagamento per le vendite](sales-how-record-sales-price-discount-payment-agreements.md).

Il cliente è ora registrato e la scheda cliente è pronta per essere utilizzata nei documenti di vendita.

Se si desidera utilizzare questa scheda cliente come modello quando si creano nuove schede cliente, è possibile salvarla come modello. Per ulteriori informazioni, vedere la seguente sezione:  

### <a name="to-save-the-customer-card-as-a-template"></a>Per salvare la scheda cliente come modello

1. Nella pagina **Scheda cliente** scegliere l'azione **Salva come modello**. Nella pagina **Modello cliente** verrà visualizzata la scheda cliente come modello.
2. Compilare i campi come necessario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Per riutilizzare le dimensioni nei modelli, selezionare l'azione **Dimensioni**. Nella pagina **Modelli dimensioni** verranno visualizzati tutti i codici di dimensione impostati per il cliente.
4. Modificare o immettere i codici di dimensione da collegare alle nuove schede cliente create utilizzando la definizione.  
5. Una volta completato il nuovo modello cliente, fare clic su **OK**.

Il modello cliente viene aggiunto all'elenco dei modelli cliente, in modo che sia possibile utilizzarlo per creare nuove schede cliente.

## <a name="deleting-customer-cards"></a>Eliminazione di schede cliente

Se è stata registrata una transazione per un cliente, non è possibile eliminare la scheda perché i movimenti contabili potrebbero essere necessari per il controllo. Per eliminare le schede cliente con i movimenti contabili, contattare il partner Microsoft per effettuare l'operazione tramite il codice.  

## <a name="see-also"></a>Vedere anche

[Definizione dei metodi di pagamento](finance-payment-methods.md)  
[Unire record duplicati](sales-how-merge-duplicate-records.md)  
[Creazione di numerazioni](ui-create-number-series.md)  
[Vendite](sales-manage-sales.md)  
[Setup Vendite](sales-setup-sales.md)  
[Utilizzo di [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
