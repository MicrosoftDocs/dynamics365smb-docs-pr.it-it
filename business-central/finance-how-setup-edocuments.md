---
title: Impostare documenti elettronici
description: Scopri come impostare la funzionalità Documenti elettronici.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 05/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="set-up-e-documents"></a>Impostare documenti elettronici

> [!IMPORTANT]
> Il modulo principale di Documenti elettronici è un framework. Per impostazione predefinita, non c'è un campo **Integrazione del servizio**. Se trovi le opzioni **Formato documento** per impostazione predefinita, tieni presente che vengono offerte come esempio e che la localizzazione deve fornire un formato dettagliato. Questi dettagli fanno parte delle app di localizzazione perché sono specifici per requisiti locali.

> [!NOTE]
> A partire dalla versione 23.2, un formato di documento PEPPOL standard viene aggiunto come formato globale nel campo **Formato documento**. Tieni presente che probabilmente non puoi utilizzare questo formato così com'è. È un formato W1 fornito per mostrare come utilizzare questa funzionalità. Ti consigliamo di verificare il formato PEPPOL esistente prima di iniziare a utilizzare questo formato.

Il primo passaggio nella configurazione di documenti elettronici è impostare il Servizio documenti elettronici dove configuri il comportamento completo del tuo sistema in relazione alla comunicazione di documenti elettronici.

## <a name="set-up-the-e-document-service"></a>Impostare il servizio documenti elettronici

Segui questi passaggi per impostare il Servizio documenti elettronici.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Servizi documenti elettronici**, quindi seleziona il collegamento correlato.
2. Seleziona **Nuovo**, quindi nella pagina **Servizi documenti elettronici**, nella Scheda dettaglio **Generale** configura i campi come descritto nella tabella seguente.

    | Campo | Descrizione |
    |-------|-------------|
    | Codice | Seleziona il codice del setup esportazione elettronica. |
    | Descrizione | Immetti una breve descrizione del setup esportazione elettronica. |
    | Formato documento | <p>Il formato di esportazione del setup esportazione elettronica.</p><p>Per impostazione predefinita, sono presenti due opzioni in questo campo. Puoi selezionare **PEPPOL BIS 3** come formato generico basato su codice o **Scambio dati** quando devi impostare pre-documenti di formati specifici nella Scheda dettaglio **Definizione di scambio dati**.</p> |
    | Integrazione del servizio | Seleziona il codice di integrazione per il setup esportazione elettronica. Nel ciclo 1, l'unica opzione è **Nessuna integrazione**. |
    | Usa elaborazione batch | Specifica se il servizio utilizza l'elaborazione batch per l'esportazione. |

3. Nella Scheda dettaglio **Parametri importati** configura i campi come descritto nella tabella seguente.

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

4. Se hai selezionato **Scambio dati** nel campo **Formato documento** nella Schda dettaglio **Generale**, utilizza la Scheda dettaglio **Definizione di scambio dati** per impostare i seguenti campi.

    | Campo | Descrizione |
    |-------|-------------|
    | Tipo di documento | Specifica il tipo di documento che usa lo scambio dati per importare ed esportare i dati. Gli esempi includono **Fattura di vendita**, **Nota credito vendita** e **Fattura di acquisto**. |
    | Importa codice definizione scambio dati | Specifica il codice di scambio dati utilizzato per importare i dati. Utilizza questo campo solo per ricevere un documento nel processo di acquisto. |
    | Esporta codice definizione scambio dati | Specifica il codice di scambio dati utilizzato per esportare i dati. Utilizza questo campo solo per consegnare documenti nel processo di vendita. |

> [!NOTE]
> Sono disponibili definizioni di scambio dati preparate per il formato PEPPOL correlate al documento di vendita e acquisto standard. Tuttavia, probabilmente non puoi utilizzare queste definizioni così come sono. Sono tutte in formato W1 fornito per mostrare come utilizzare questa funzionalità. Ti consigliamo di verificare il formato PEPPOL esistente prima di iniziare a utilizzarle.

Se hai configurato il formato **Definizione di scambio dati** nella tua localizzazione, puoi aggiungere una riga per ogni tipo di documento di cui hai bisogno. Aggiungi righe che corrispondono all'esempio di scambio dati predefinito per il formato W1 PEPPOL. Tuttavia, prima seleziona l'opzione **Tipo di documento** per ogni riga di cui hai bisogno. Per ogni tipo di dati, seleziona il valore **Importa codice definizione scambio dati** o **Esporta codice definizione scambio dati** che vuoi utilizzare.

Se non utilizzi il formato **Definizione di scambio dati**, puoi creare e configurare i formati utilizzando l'[interfaccia](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments). Modifica le informazioni nelle righe **Mapping esportazione** e **Mapping importazione**, dove puoi trovare le tabelle e i campi per configurare regole di trasformazione. In questo caso, devi aggiungere una nuova opzione nel campo **Formato documento** correlato al tuo formato.  

### <a name="supported-document-types"></a>Tipi di documenti supportati

I tipi di documenti supportati si basano sul **Formato documento** scelto. Per verificare quali tipi di documenti sono supportati, nella pagina **Servizi documenti elettronici**, scegli l'azione **Tipi di documenti supportati**. Si apre **Tipi di documenti di origine supportati dal servizio documenti elettronici** e nella colonna **Tipo di documenti di origine** è possibile scegliere differenti tipi di documento per supportarli per il formato che prevedi di utilizzare. Assicurati di non utilizzare il tipo di documento se quel documento non è selezionato in questa pagina.   

## <a name="set-up-a-document-sending-profile"></a>Impostare un profilo di invio documenti

Puoi impostare un metodo preferito di invio di documenti di vendita per ogni cliente. In tal modo, non devi scegliere un'opzione di invio ogni volta che scegli l'azione **Registra e invia**. Nella pagina **Profili di invio documenti** puoi impostare differenti profili di invio e quindi selezionarne uno nel campo **Profilo di invio documenti** nella scheda cliente. Puoi selezionare la casella di controllo **Predefinito** per specificare che un profilo di invio documenti è il profilo predefinito per tutti i clienti, eccetto per quelli per i quali il campo **Profilo di invio documenti** è impostato su un profilo di invio differente.

Questa funzionalità viene utilizzata per impostare l'automazione della fatturazione elettronica. Quando scegli **Registra e invia** in un documento di vendita, nella finestra di dialogo **Registra e invia conferma** viene visualizzato il profilo di invio utilizzato, ovvero quello impostato per il cliente o quello predefinito per tutti i clienti.

Per impostare un profilo di invio documenti, procedi come segue.

1. Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Dimmi cosa vuoi fare"), immetti **Profili di invio documenti**, quindi seleziona il collegamento correlato.
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
4. Scegli l'azione **Nuovo workflow da modello** per selezionare un modello per il processo dei documenti elettronici. I modelli disponibili sono **Invia a un servizio** e **Invia a più servizi**.
5. Seleziona **OK** per completare il setup del workflow.
6. Nel campo **Risposta**, seleziona **Invia documento elettronico utilizzando il setup** per configurare le risposte del workflow.
7. Seleziona il Servizio documenti elettronici che hai creato come opzione, scegli **OK**, quindi abilita il workflow.

> [!NOTE]
> Puoi creare il tuo workflow per documenti elettronici senza utilizzare modelli di workflow predefiniti. Se disponi di più servizi, puoi utilizzare workflow differenti.

Per utilizzare più flussi di lavoro, configurali tramite i profili di invio documenti per diversi clienti. Quando imposti il flusso di lavoro, specifica il profilo di invio documenti nella colonna **Condizione** della Scheda dettaglio **Fasi workflow**, perché non è possibile avere due servizi che utilizzano lo stesso profilo di invio documenti nei workflow.

Quando configuri il workflow nella pagina **Workflow**, punta al campo **Condizione** nella Scheda dettaglio **Fasi workflow**. Nella pagina **Condizioni evento**, nel campo **Filtro**, seleziona il profilo di invio documenti che desideri utilizzare.

## <a name="set-up-a-retention-policy-for-e-documents"></a>Impostare criteri di conservazione per documenti elettronici

I documenti elettronici possono essere oggetto di diverse legislazioni locali relative al periodo di conservazione dei documenti elettronici. Pertanto, abbiamo aggiunto un setup di criteri di conservazione per tutte le informazioni importanti relative a documenti elettronici. Gli amministratori possono definire criteri di conservazione che specificano la frequenza alla quale Dynamics 365 Business Central elimina i record obsoleti correlati a documenti elettronici. Per altre informazioni su criteri di conservazione, vedi [Definire i criteri di conservazione](admin-data-retention-policies.md).

Per impostare i criteri di conservazione relativi a documenti elettronici, procedi come segue.

1. Nella pagina **Servizi documenti elettronici**, scegli l'azione **Criteri di conservazione**.
2. Una volta completata l'azione, seleziona uno dei seguenti criteri di conservazione da impostare:

    - Log documenti elettronici
    - Log di integrazione documenti elettronici
    - Log mapping di documenti elettronici
    - Archiviazione dati di documenti elettronici

## <a name="e-documents-demo-data"></a>Dati dimostrativi dei documenti elettronici

> [!NOTE]
> A partire dalla versione 24.0 di Business Central, è possibile impostare dati dimostrativi per documenti elettronici.

Per fornire modalità più semplici per testare e dimostrare le funzionalità di **Documenti elettronici**, Microsoft ha creato un nuovo modulo demo per i documenti elettronici. Per abilitare questo modulo, segui i passaggi:  

1.  Seleziona l'icona ![lampadina che apre la funzionalità Dimmi](media/ui-search/search_small.png "Informazioni sull'operazione che si desidera eseguire"), immetti **Strumento demo Contoso**, quindi seleziona il collegamento correlato.  
2.  Prima di abilitare il **Modulo Contoso documenti elettronici**, a causa delle dipendenze è necessario aver abilitato i seguenti moduli: **Modulo comune** e **Modulo Warehouse**. 
3.  Dopo aver abilitato questi moduli, seleziona il **Modulo Contoso documenti elettronici**, quindi scegli l'azione **Genera**. 
4.  Segui i passaggi.  
5.  Chiudere la pagina.   

Una volta abilitato il modulo, avrai creato nuovi elementi demo, importato sei documenti elettronici (basati su Peppol BIS 3) e già configurato il **Servizi documenti elettronici** con flussi di lavoro creati.  

## <a name="see-also"></a>Vedere anche

[Come usare documenti elettronici nelle vendite](finance-how-use-edocuments.md)    
[Come usare documenti elettronici negli acquisti](finance-how-use-edocuments-purchase.md)  
[Come estendere documenti elettronici in Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)    
[Gestione contabile](finance.md)    
[Fatturare le vendite](sales-how-invoice-sales.md)    
[Registrare gli acquisti con le fatture e gli ordini di acquisto](purchasing-how-record-purchases.md)    
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
