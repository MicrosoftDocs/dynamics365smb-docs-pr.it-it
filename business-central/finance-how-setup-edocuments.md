---
title: Impostare documenti elettronici
description: Scopri come impostare la funzionalità Documenti elettronici.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 10/05/2023
ms.author: altotovi
---

# <a name="set-up-e-documents"></a>Impostare documenti elettronici

> [!IMPORTANT]
> Il modulo principale di Documenti elettronici è un framework. Per impostazione predefinita, non c'è un campo **Formato documento** o **Integrazione del servizio**. Questi dettagli fanno parte delle app di localizzazione perché sono entrambi specifici per requisiti locali.

> [!NOTE]
> A partire dalla versione 23.1, un formato di documento PEPPOL standard viene aggiunto come formato globale nel campo **Formato documento**.

Il primo passaggio nella configurazione di documenti elettronici è impostare il Servizio documenti elettronici dove configuri il comportamento completo del tuo sistema in relazione alla comunicazione di documenti elettronici.

## <a name="set-up-the-e-document-service"></a>Impostare il Servizio documenti elettronici

Segui questi passaggi per impostare il Servizio documenti elettronici.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Servizi documenti elettronici**, quindi seleziona il collegamento correlato.
2. Seleziona **Nuovo**, quindi nella pagina **Servizio documenti elettronici**, nella Scheda dettaglio **Generale** configura i campi come descritto nella tabella seguente.

    | Campo | Descrizione |
    |-------|-------------|
    | Codice | Seleziona il codice del setup esportazione elettronica. |
    | Descrizione | Immetti una breve descrizione del setup esportazione elettronica. |
    | Formato documento | <p>Il formato di esportazione del setup esportazione elettronica.</p><p>Per impostazione predefinita, non sono presenti opzioni in questo campo nel ciclo 1.</p> |
    | Integrazione del servizio | Seleziona il codice di integrazione per il setup esportazione elettronica. Nel ciclo 1, l'unica opzione è **Nessuna integrazione**. |
    | Usa elaborazione batch | Specifica se il servizio utilizza l'elaborazione batch per l'esportazione. |

4. Nella Scheda dettaglio **Parametri importati** configura i campi come descritto nella tabella seguente.

    | Campo | Descrizione |
    |-------|-------------|
    | Convalida società di destinazione | Specifica se durante l'importazione le informazioni sulla società di destinazione devono essere convalidate. |
    | Risolvi unità di misura | Specifica se durante l'importazione l'unità di misura deve essere risolta. |
    | Ricerca riferimento articolo | Specifica se durante l'importazione deve essere eseguita la ricerca di un articolo in base al riferimento articolo. |
    | Ricerca GTIN articolo | Specifica se durante l'importazione deve essere eseguita la ricerca di un articolo in base al codice GTIN (Global Trade Item Number). |
    | Ricerca mapping conto | Specifica se durante l'importazione la ricerca di un conto deve essere eseguita in **Mapping conto** in base al testo in entrata. |
    | Convalida sconto riga | Specifica se durante l'importazione deve essere convalidato uno sconto riga. |
    | Collega sconto fattura | Specifica se durante l'importazione deve essere applicato uno sconto fattura. |
    | Verifica totali | Specifica se durante l'importazione deve essere verificato un totale fattura. |
    | Aggiorna ordine | Specifica se l'ordine di acquisto corrispondente deve essere aggiornato. |
    | Crea righe di registrazione | Specifica se è necessario creare una riga di registrazione anziché un documento di acquisto. Seleziona questa opzione quando desideri utilizzare le registrazioni come destinazione delle tue fatture. |
    | Nome modello registrazioni COGE | Specifica il nome del modello delle registrazioni COGE utilizzato per la creazione di righe di registrazione. Questo campo è applicabile quando vuoi utilizzare le registrazioni come destinazione delle tue fatture. |
    | Nome batch registrazioni COGE | Specifica il nome del batch delle registrazioni COGE utilizzato per la creazione di righe di registrazione. Questo campo è applicabile quando vuoi utilizzare le registrazioni come destinazione delle tue fatture. |
    | Importazione automatica | Specifica se i documenti devono essere importati automaticamente dal servizio. |
    | Ora di inizio batch | Specifica l'ora di inizio per i processi di importazione. |
    | Minuti tra ogni esecuzione | Specifica il numero di minuti tra le esecuzioni dei processi di importazione. |

Se hai configurato il formato **Definizione di scambio dati** nella tua localizzazione, puoi aggiungere una riga per ogni tipo di documento di cui hai bisogno. Tuttavia, devi prima selezionare l'opzione **Tipo di documento** per ogni riga di cui hai bisogno. Per ogni tipo di dati, seleziona il valore **Importa codice definizione scambio dati** o **Esporta codice definizione scambio dati** che vuoi utilizzare.

Infine, se non utilizzi il formato **Definizione di scambio dati**, puoi configurare i formati tramite le righe **Mapping esportazione** e **Mapping importazione**, dove puoi individuare le tabelle e i campi da utilizzare per configurare le regole di trasformazione, se applicabile.

## <a name="set-up-a-document-sending-profile"></a>Impostare un profilo di invio documenti

Puoi impostare un metodo preferito di invio di documenti di vendita per ogni cliente. In tal modo, non devi selezionare un'opzione di invio ogni volta che selezioni l'azione **Registra e invia**. Nella pagina **Profili di invio documenti** puoi impostare differenti profili di invio e quindi selezionarne uno nel campo **Profilo di invio documenti** nella scheda cliente. Puoi selezionare la casella di controllo **Predefinito** per specificare che un profilo di invio documenti è il profilo predefinito per tutti i clienti, eccetto per quelli per i quali il campo **Profilo di invio documenti** è impostato su un profilo di invio differente.

Questa funzionalità viene utilizzata per impostare l'automazione della fatturazione elettronica. Quando selezioni **Registra e invia** in un documento di vendita, nella finestra di dialogo **Registra e invia conferma** viene visualizzato il profilo di invio utilizzato, ovvero quello impostato per il cliente o quello predefinito per tutti i clienti.

Per impostare un profilo di invio documenti, procedi come segue.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Profili di invio documenti**, quindi seleziona il collegamento correlato.
2. Nella pagina **Profili di invio documenti** seleziona **Nuovo**.
3. Nella Scheda dettaglio **Generale** immetti le eventuali informazioni richieste.
4. Nella Scheda dettaglio **Opzioni di invio** configura i campi come descritto nella tabella riportata di seguito.

    | Campo | Descrizione |
    |-------|-------------|
    | Documento elettronico | Specifica se il documento viene inviato come documento elettronico che il cliente può importare nel sistema quando selezioni **Registra e invia**. Per utilizzare questa opzione, devi impostare anche il campo **Formato** o **Codice flusso del servizio documenti elettronici**. In alternativa, il file può essere salvato su disco. |
    | Formato | Specifica il formato da utilizzare per inviare un documento elettronico. Questo campo è obbligatorio se selezioni **Tramite il servizio di scambio documenti** nel campo **Documento elettronico**. |
    | Codice flusso del servizio documenti elettronici | Specifica il flusso del servizio elettronico utilizzato per inviare documenti. Questo campo è obbligatorio se selezioni **Flusso esteso del servizio documenti elettronici** nel campo **Documento elettronico**. |

    > [!NOTE]
    > Se selezioni **Flusso esteso del servizio documenti elettronici** nel campo **Documento elettronico**, devi avere già configurato il workflow per i tuoi documenti elettronici.

## <a name="set-up-the-workflow"></a>Impostare il workflow

Segui questi passaggi per impostare il workflow utilizzato nella funzionalità Documenti elettronici.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Dimmi cosa vuoi fare"), immetti **Modelli del workflow**, quindi seleziona il collegamento correlato.
2. Se non puoi trovare **Modelli di workflow per documenti elettronici** nella pagina **Modelli del workflow**, seleziona **Reimposta i modelli Microsoft**. Dovrebbe apparire **Modelli di workflow per documenti elettronici**. Chiudere la pagina.
3. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Workflow**, quindi seleziona il collegamento correlato.
4. Esegui l'azione **Nuovo workflow da modello** per selezionare un modello per il processo dei documenti elettronici. I modelli disponibili sono **Invia a un servizio** e **Invia a più servizi**.
5. Seleziona **OK** per completare il setup del workflow.
6. Nel campo **Risposta**, seleziona **Invia documento elettronico utilizzando il setup** per configurare le risposte del workflow.
7. Seleziona il Servizio documenti elettronici che hai creato come opzione, seleziona **OK**, quindi abilita il workflow.

> [!NOTE]
> Puoi creare il tuo workflow per documenti elettronici senza utilizzare modelli di workflow predefiniti. Se disponi di più servizi, puoi utilizzare workflow differenti.

## <a name="set-up-a-retention-policy-for-e-documents"></a>Impostare criteri di conservazione per documenti elettronici

I documenti elettronici possono essere oggetto di diverse legislazioni locali relative al periodo di conservazione dei documenti elettronici. Pertanto, abbiamo aggiunto un setup di criteri di conservazione per tutte le informazioni importanti relative a documenti elettronici. Gli amministratori possono definire criteri di conservazione che specificano la frequenza alla quale Dynamics 365 Business Central elimina i record obsoleti correlati a documenti elettronici. Per altre informazioni su criteri di conservazione, vedi [Definire i criteri di conservazione](admin-data-retention-policies.md).

Per impostare i criteri di conservazione relativi a documenti elettronici, procedi come segue.

1. Nella pagina **Servizi documenti elettronici**, esegui l'azione **Criteri di conservazione**.
2. Una volta completata l'azione, seleziona uno dei seguenti criteri di conservazione da impostare:

    - Log documenti elettronici
    - Log di integrazione documenti elettronici
    - Log mapping di documenti elettronici
    - Archiviazione dati di documenti elettronici

## <a name="see-also"></a>Vedere anche

[Come utilizzare documenti elettronici in Business Central](finance-how-use-edocuments.md)  
[Come estendere documenti elettronici in Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Gestione contabile](finance.md)  
[Fatturazione delle vendite](sales-how-invoice-sales.md)  
[Registrare gli acquisti con le fatture e gli ordini di acquisto](purchasing-how-record-purchases.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
