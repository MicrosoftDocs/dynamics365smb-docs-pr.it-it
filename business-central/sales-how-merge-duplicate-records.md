---
title: Unire record duplicati relativi a clienti o fornitori
description: Descrive come consolidare le informazioni su clienti o fornitori quando si hanno voci duplicate su alcuni di essi.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 04/01/2021
ms.author: edupont
---
# Unire record duplicati

Poiché utenti diversi creano nel tempo nuove schede cliente, fornitore o contatto, oppure nuovi record vengono creati automaticamente durante la migrazione, un cliente, un fornitore o un contatto possono essere rappresentati nel sistema con più di un record. In tal caso, è possibile utilizzare la pagina **Unisci duplicato** nella scheda del record che si desidera mantenere. La pagina fornisce una panoramica dei valori di campo duplicati e funzioni per selezionare i valori da mantenere o eliminare quando si uniscono due record.

> [!NOTE]
> Solo gli utenti con il set di autorizzazioni UNISCI DUPLICATI possono utilizzare questa funzionalità.

> [!TIP]
> La pagina **Unisci duplicato** mostra tutti i campi in cui i valori sono diversi per i due record che vengono confrontati. Di conseguenza, un duplicato è indicato dalla pagina quando visualizza pochissimi campi. Se invece la pagina visualizza molti campi, il record sospetto non è probabilmente un duplicato.

La seguente procedura è basata su una scheda cliente. I passaggi sono simili per una scheda contatto o fornitore.

1. Scegli l'icona a forma di ![lampadina che consente di aprire la funzionalità delle informazioni.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Clienti**, quindi scegli il collegamento correlato.
2. Selezionare il cliente per il quale un record duplicato esiste o se ne sospetta l'esistenza, quindi scegliere l'azione **Modifica**.
3. Nella pagina **Scheda cliente** scegliere l'azione **Unisci con**.
4. Nella pagina **Unisci duplicato**, nel campo **Unisci con**, selezionare il cliente che si ritiene sia un duplicato di quello aperto, indicato nel campo **Corrente**.

    La Scheda dettaglio **Campi** elenca i campi dove i valori sono diversi per i due clienti. Ciò significa che se il cliente selezionato è effettivamente un duplicato, solo pochissimi campi devono essere elencati, come errori di digitazione e altri errori nell'immissione dei dati.

    La Scheda dettaglio **Tabelle correlate** elenca le tabelle in cui vi sono campi relativi a entrambi i clienti. I campi **Conteggio corrente** e **Conteggio duplicati** visualizzano il numero di campi nelle tabelle correlate in cui viene utilizzato il valore **Nr.** del cliente corrente e di quello duplicato. Nella pagina **Unisci duplicato**, questa sezione è solo informativa, tuttavia, se vi sono conflitti di unione, possono essere risolti nella pagina **Unisci conflitti duplicati**. Vedere i passaggi da 8 a 12.   

5. Per ciascun campo in cui si intende utilizzare un altro valore da quello corrente, selezionare la casella di controllo **Ignora**. Il valore nel campo **Valore alternativo** verrà quindi trasferito al record corrente quando si completa il processo.
6. Al termine della selezione di quali valori mantenere o ignorare, scegliere l'azione **Unione**.

    Il sistema verifica se l'unione dei valori per il cliente duplicato nel cliente corrente causa eventuali conflitti. Un conflitto esiste se un valore in almeno un campo di chiave primaria è uguale per entrambi i clienti mentre il valore nel campo **Nr.** è differente per i due clienti.

7. Se non vengono rilevati conflitti, scegliere il pulsante **Sì** nella finestra di conferma del messaggio.

    Il cliente duplicato viene rinominato di modo che l'utilizzo del relativo valore **Nr.** in tutti i campi relativi alla tabella di clienti verrà sostituito con il valore **Nr.** del cliente corrente.
8. Se esistono dei conflitti, scegliere l'azione **Risolvere (xx) conflitti prima dell'unione.** nella Scheda dettaglio **Conflitti**, che verrà visualizzata se esistono dei conflitti.
9. Nella pagina **Unisci conflitti duplicati**, selezionare la riga per una tabella correlata con un conflitto, quindi scegliere l'azione **Visualizza dettagli**.

    La pagina **Unisci duplicato** ora visualizza i campi nella tabella selezionata che provocano un conflitto di unione tra i due record cliente. Da notare nei valori riepilogativi dei campi **Corrente** e **Conflitti con** e nelle righe che almeno un campo di chiave primaria è uguale per entrambi i clienti e che il valore del campo **Nr.** è differente per i due clienti.   
10. Se non si desidera conservare il record cliente duplicato, scegliere l'azione **Rimuovi duplicato** quindi scegliere il pulsante **Chiudi**.

    I valori di campo identici, differenti dal valore nel campo **Nr.** vengono rimossi dal record duplicato e inseriti nel record corrente.
11. Se si desidera mantenere il record cliente duplicato dopo l'unione, scegliere **Rinomina duplicato**.
12. Sulle righe, non per il campo**Nr.**, dove il campo ha lo stesso valore in entrambi i record, modificare il valore nel campo **Valore alternativo**, quindi scegliere il pulsante **Chiudi**.

    Il valore di campo in conflitto viene aggiornato nel record duplicato di modo che possa essere unito al record corrente. Il record duplicato continua a esistere dopo l'unione.
13. Ripetere i passaggi da 8 a 12 fino a risolvere tutti i conflitti. La Scheda dettaglio **Conflitti** non è più visualizzata.
14. Nella pagina **Unisci duplicato**, scegliere di nuovo l'azione **Unisci** quindi selezionare il pulsante **Sì** nella finestra di conferma del messaggio.

> [!NOTE]
> Per i contatti, è possibile utilizzare la funzionalità per trovare contatti duplicati prima di utilizzare la pagina **Unisci duplicato**. Per ulteriori informazioni, vedere [Ricerca di contatti duplicati](marketing-setup-contacts.md#searching-for-duplicate-contacts).

## Vedi il relativo [training Microsoft](/training/modules/trade-master-data-dynamics-365-business-central/)

## Vedere anche

[Vendite](sales-manage-sales.md)  
[Setup contatti](marketing-setup-contacts.md)  
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
