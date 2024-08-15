---
title: Assegnare layout di documenti a clienti o fornitori
description: Utilizza i layout dei documenti per controllare l'aspetto e il formato di documenti come fatture e ordini che invii a clienti e fornitori.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '21, 9650'
ms.date: 07/05/2024
ms.service: dynamics-365-business-central
---
# <a name="define-document-layouts-for-customers-and-vendors"></a>Definire i layout di documenti per clienti e fornitori

I layout dei documenti utilizzano i layout dei report per definire l'aspetto dei documenti inviati a clienti e fornitori. Business Central fornisce layout standard, ma puoi anche personalizzare layout personalizzati per ciascuno dei tuoi partner commerciali. Per ulteriori informazioni, vedere [Creare e modificare layout di report personalizzati](ui-how-create-custom-report-layout.md). Puoi selezionare layout di documenti standard e personalizzati dalle schede cliente e fornitore scegliendo l'azione **Layout dei documenti**. Il valore nel campo **Utilizzo** definisce il processo per il quale viene utilizzato il layout del documento. Ad esempio, per i clienti, potresti utilizzare i tipi di **Promemoria**, **Spedizione** e **Conferma** di layout dei documenti.

I layout dei documenti possono anche farti risparmiare tempo quando invii documenti ai contatti di clienti o fornitori tramite e-mail. Per ogni layout che assegni al cliente o al contatto, puoi specificare uno o più indirizzi e-mail di contatto. Ad esempio, puoi inviare una fattura ai contatti di acquisto e di warehouse del cliente. L'aggiunta di indirizzi e-mail di contatto è facile. Nella pagina **Layout documento**, l'azione **Seleziona Email dai contatti** consente di scegliere da un elenco di indirizzi email di contatto registrati per il cliente o il fornitore. Puoi anche aggiungere indirizzi e-mail manualmente. Se inserisci più indirizzi, separali con un punto e virgola e non aggiungere spazi tra gli indirizzi.

Prima di poter definire quale layout di documento utilizzare per quali processi e a quale contatto inviare il documento, è necessario caricare tutti i report (documenti) disponibili dalla pagina **Selezioni report**. È possibile caricare rapidamente i documenti utilizzando l'azione **Copia da selezione report** nella pagina **Layout documenti**.

I passaggi nelle seguenti sezioni descrivono come definire layout di documenti di vendita dalla pagina **Scheda cliente**. Per i fornitori, i passaggi sono gli stessi dalla pagina **Scheda fornitore**.

## <a name="to-load-the-standard-document-layouts-for-sales-documents-for-a-customer"></a>Per caricare i layout dei documenti standard per i documenti di vendita per un cliente

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") , immetti **Clienti**, quindi scegli il collegamento correlato.
2. Apri la pagina **Scheda cliente** per il cliente, quindi scegliere l'azione **Layout documenti**.
3. Nella pagina **Layout documento**, scegliere l'azione **Copia da selezione report**.

La pagina **Layout documenti** visualizza tutti i layout disponibili per i documenti di vendita. 

## <a name="to-select-a-custom-report-layout-to-use-for-the-sales-document-layout"></a>Per selezionare un layout di report personalizzato da utilizzare per un layout di documento di vendita

I passaggi seguenti presuppongono che tu disponga già di un report personalizzato area di disposizione per il tipo di documento. Se non hai ancora un report personalizzato area di disposizione, devi prima crearne uno. Per ulteriori informazioni, vedi [Creare e modificare layout di report personalizzati](ui-how-create-custom-report-layout.md).

1. Scegli la ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire") , immetti **Clienti**, quindi scegli il collegamento correlato.
2. Apri la pagina **Scheda cliente** per il cliente, quindi scegliere l'azione **Layout documenti**.
3. Nella pagina **Layout documento**, nella riga di un layout di report per il quale si desidera utilizzare un layout personalizzato, scegliere il campo **Descrizione layout personalizzato**.

   > [!TIP]
   > Per impostazione predefinita, il campo Descrizione personalizzata area di disposizione è nascosto. Se il campo non è disponibile, puoi personalizzare la pagina per aggiungerlo. Per personalizzare la pagina, seleziona :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="l'icona Impostazioni."::: Icona, quindi scegli **Personalizza**. Per saperne di più sulla personalizzazione delle pagine, vai a [Personalizza il tuo spazio di lavoro](ui-personalization-user.md).

1. Nella pagina **Layout report personalizzati**, selezionare il layout di documento che si desidera utilizzare per il tipo di documento di vendita. Per ulteriori informazioni, vedi [Creare e modificare layout di report personalizzati](ui-how-create-custom-report-layout.md).

## <a name="to-specify-which-contact-receives-which-document-layout-for-a-customer"></a>Per specificare quale contatto riceve quale documento area di disposizione per un cliente

Per risparmiare tempo quando invii documenti ai contatti di clienti e fornitori tramite e-mail, specifica i loro indirizzi e-mail sui layout dei documenti. Ad esempio, puoi sempre inviare gli estratti conto dei clienti ai contatti del commercialista e gli ordini di vendita agli acquirenti dei clienti o gli ordini di acquisto ai venditori dei fornitori.

1. Nella pagina **Layout documento** nella riga di un layout di report che si desidera inviare a un contatto specifico per il cliente, scegliere l'azione **Seleziona e-mail da contatti**.
2. Nella pagina **Contatti**, seleziona uno o più contatti, quindi scegli **OK**.

## <a name="see-also"></a>Vedi anche

[Aggiornare layout report personalizzati](ui-update-report-layouts.md)  
[Creare e modificare layout di report personalizzati](ui-how-create-custom-report-layout.md)  
[Importare ed esportare un layout di report o documento personalizzato](ui-how-import-and-export-report-layout.md)  
[Inviare documenti via e-mail](ui-how-send-documents-email.md)  
[Gestione dei layout di report](ui-manage-report-layouts.md)  
[Utilizzare report, processi batch e XMLport](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
