---
title: Vendere articoli assemblati su ordine
description: Scopri come vendere un articolo assemblato su ordine.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/23/2022
ms.search.keywords: 'kit, kitting, substitute items'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.custom: bap-template
---
# Vendere articoli assemblati su ordine

Non è previsto che gli articoli che sono configurati per assemblaggio su ordine siano in magazzino e verranno assemblati quando verranno inclusi in un ordine di vendita. Un articolo è impostato per l'assemblaggio su ordine quando il campo **Criteri di assemblaggio** sulla scheda articolo contiene **Assemblaggio su ordine**. Quando si immette l'articolo in una riga dell'ordine di vendita, un ordine di assemblaggio viene automaticamente creato e collegato all'ordine di vendita.  

> [!NOTE]  
> Se articoli di assemblaggio su ordine sono già in magazzino, è possibile dedurne la relativa quantità dall'ordine di assemblaggio e impegnarla dal magazzino. Ulteriori informazioni in [Vendere gli articoli di magazzino nei flussi da assemblare su ordine](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

In questa procedura, si elabora la vendita di un articolo che verrà assemblato in base alle specifiche richieste dal cliente. Questi passaggi includono: 

* La creazione di una riga per l'ordine di vendita.
* La personalizzazione dell'articolo dell'assieme modificandone i componenti e le risorse.
* Verifica disponibilità per stabilire una data di consegna.
* Rilascio dell'ordine di vendita da assemblare e spedire immediatamente.  

> [!NOTE]  
> La procedura seguente non include i passaggi per la creazione di ordini di vendita standard prima del passaggio in cui inserisci l'articolo assemblaggio su ordine o su una riga dell'ordine di vendita. Scopri di più sulla creazione di ordini di vendita su [Vendere prodotti con un ordine di vendita al cliente](sales-how-sell-products.md).  

## Per vendere un articolo assemblato su ordine

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Ordini vendita**, quindi seleziona il collegamento correlato.  
2. Creare un ordine di vendita. 
3. Nel campo **Nr.** immettere un articolo impostato per l'assemblaggio su ordine.  
4. Nel campo **Cod. ubicazione** specificare da quale ubicazione verrà venduto l'articolo. Il processo di assemblaggio avverrà in tale ubicazione.  
5. Nel campo **Quantità** immettere il numero di unità da vendere.  

    > [!NOTE]  
    >  Se uno o più componenti della quantità richiesta dell'articolo di assemblaggio non sono disponibili, viene aperta una pagina di avviso di disponibilità. <!-- Check whether the field help would be useful. For more information, see Assembly Availability.  -->

    Un ordine di assemblaggio viene creato automaticamente e collegato alla riga dell'ordine di vendita. La data di scadenza dell'ordine di assemblaggio è la data di spedizione della riga dell'ordine di vendita.  

    La quantità da vendere viene copiata nel campo **Qtà per assemblaggio su ordine**, in cui si indica che la configurazione dell'articolo prevede l'assemblaggio dell'intera quantità presente nella riga di vendita. È possibile ridurre la quantità da assemblare, ad esempio, se si è a conoscenza che alcuni articoli sono già disponibili. Ulteriori informazioni in [Vendere gli articoli di magazzino nei flussi da assemblare su ordine](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

6. S il cliente desidera un articolo aggiuntivo in un kit, nella Scheda dettaglio **Righe** scegliere l'azione **Riga**, l'azione **Assemblaggio su ordine**, quindi l'azione **Righe di assemblaggio su ordine** per visualizzare e modificare i componenti di assemblaggio standard. In alternativa, scegliere il campo **Qtà per assemblaggio su ordine** .  
7. Nella pagina **Righe di assemblaggio su ordine** creare una nuova riga di tipo **Articolo** per il componente dell'assieme aggiuntivo.  

    Puoi anche personalizzare l'ordine aumentando la quantità di un articolo standard nel kit. È possibile eseguire questa operazione aumentando il valore del campo **Quantità per** nella riga specifica dell'ordine di assemblaggio.  

    > [!NOTE]  
    >  La pagina **Righe di assemblaggio su ordine** contiene solo i campi di base per personalizzare l'elenco dei componenti, aggiungendo i numeri di tracciabilità articolo o risolvendo i problemi di disponibilità dei componenti. Per aggiungere altre informazioni sull'ordine di assemblaggio, ad esempio la data di inizio dell'ordine di assemblaggio, scegli l'azione **Mostra documenti**. Viene aperta una visualizzazione completa dell'ordine di assemblaggio collegato alla riga dell'ordine di vendita. Non è possibile modificare il contenuto della maggior parte dei campi nell'intestazione dell'ordine di assemblaggio e non è possibile pubblicarne l'output di assemblaggio. È necessario registrare la spedizione della riga ordine cliente.  
    >
    >  Negli ordini di assemblaggio collegati, è possibile modificare solo il campo **Data di inizio**. La modifica della data di inizio consente agli addetti all'assemblaggio di specificare che stanno iniziando l'assemblaggio prima della data di scadenza. È possibile modificare tutti i campi nelle righe dell'ordine di assemblaggio collegato in modo da permettere agli addetti alla warehouse di immettere i dati relativi al consumo durante il processo.  

8. Esaminare o rispondere ai problemi di disponibilità dei componenti. Ad esempio, seleziona un articolo sostitutivo.  
9. Chiudere la pagina **Righe di assemblaggio su ordine**. L'ordine di assemblaggio è pronto e i lavoratori possono iniziare l'assemblaggio degli articoli personalizzati.  
10. Nell'ordine di vendita, scegliere l'azione **Rilascio** per notificare al reparto di assemblaggio che il processo di assemblaggio può iniziare. Ulteriori informazioni in [Assemblare articoli](assembly-how-to-assemble-items.md).  

> [!NOTE]  
> Le sostituzioni degli articoli non sostituiscono automaticamente un articolo con un altro articolo, ad esempio durante la creazione di un ordine di vendita o in una distinta base. Invece, sarai avvisato del fatto che un articolo sostitutivo è disponibile.

## Vedi il relativo [training Microsoft](/training/modules/assemble-to-order-dynamics-365-business-central/)

## Vedere anche

[Gestione assemblaggio](assembly-assemble-items.md)  
[Usare le distinte base assemblaggio](assembly-how-work-assembly-boms.md)  
[Registrare nuovi articoli](inventory-how-register-new-items.md)  
[Magazzino](inventory-manage-inventory.md)  
[Panoramica di Warehouse Management](design-details-warehouse-management.md)
[Utilizzare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]