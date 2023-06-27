---
title: Gestione dei valori delle opzioni mancanti
description: Scopri come impedire la mancata sincronizzazione completa poiché le opzioni differiscono nei campi mappati. Questo processo richiede l'aiuto di uno sviluppatore.
author: brentholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.topic: conceptual
ms.date: 03/23/2022
---

# <a name="handling-missing-option-values" />Gestione dei valori delle opzioni mancanti
> [!NOTE]
> Nel primo ciclo di rilascio del 2022 puoi creare i mapping delle opzioni. Per ulteriori informazioni, vedi [Personalizzazione dei mapping di opzione con Microsoft Dataverse](/dynamics365/business-central/dev-itpro/administration/administration-custom-option-mapping). Le nuove funzionalità richiedono che l'amministratore abiliti **Aggiornamento della funzionalità: mapping all'opzione impostata in Dataverse senza codice** nella pagina **Gestione funzionalità**. Per ulteriori informazioni, vedi [Abilitazione di funzionalità imminenti in anticipo](/dynamics365/business-central/dev-itpro/administration/feature-management).

Questo argomento è destinato a utenti esperti. I processi descritti richiedono l'aiuto di uno sviluppatore.

[!INCLUDE[prod_short](includes/cds_long_md.md)] contiene tre campi di set di opzioni che includono valori che è possibile mappare ai campi [!INCLUDE[prod_short](includes/prod_short.md)] di tipo Opzione per la sincronizzazione automatica. Durante la sincronizzazione, le opzioni non mappate vengono ignorate e le opzioni mancanti vengono aggiunte alla relativa tabella [!INCLUDE[prod_short](includes/prod_short.md)] e quindi alla tabella di sistema **Mappatura opzione Dataverse** da gestire manualmente in seguito. Ad esempio, aggiungendo le opzioni mancanti in entrambi i prodotti e quindi aggiornando la mappatura.

La pagina **Mapping tabella integrazione** contiene tre campi che includono uno o più valori di opzione mappati. Dopo una sincronizzazione completa, la pagina **Mappatura opzione Dataverse** contiene le opzioni non mappate nei tre campi.

|         Record             | Valore opzione | Didascalia valore opzione |
|----------------------------|--------------|----------------------|
| Condizioni pagamento: NET30       | 1            | Importo netto a 30               |
| Condizioni pagamento: 2%10NET30   | 2            | 2% a 10; importo netto a 30        |
| Condizioni pagamento: NET45       | 3            | Importo netto a 45               |
| Condizioni pagamento: NET60       | 4            | Importo netto a 60               |
| Metodo di spedizione: FOB       | 1            | FOB                  |
| Metodo di spedizione: NOCHARGE  | 2            | Nessun addebito            |
| Spedizioniere: AIRBORNE   | 1            | Trasporto aereo             |
| Spedizioniere: DHL        | 2            | DHL                  |
| Spedizioniere: FEDEX      | 3            | FedEx                |
| Spedizioniere: UPS        | 4            | UPS                  |
| Spedizioniere: POSTALMAIL | 5            | Posta ordinaria          |
| Spedizioniere: FULLLOAD   | 6            | Carico completo            |
| Spedizioniere: WILLCALL   | 7            | Chiamata            |

Il contenuto della pagina **Mappatura opzione Dataverse** si basa su valori di enumerazione nella tabella **Account CRM**. In [!INCLUDE[prod_short](includes/cds_long_md.md)], i seguenti campi nella tabella account vengono mappati ai campi nei record cliente e fornitore:

- **Indirizzo 1: termini di spedizione** del tipo di dati Enum, dove i valori sono definiti come segue:

```
enum 5335 "CDS Shipment Method Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "FOB") { Caption = 'FOB'; }
    value(2; "NoCharge") { Caption = 'No Charge'; }
}
```

- **Indirizzo 1: metodo di spedizione** del tipo di dati Enum, dove i valori sono definiti come segue:

```
enum 5336 "CDS Shipping Agent Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Airborne") { Caption = 'Airborne'; }
    value(2; "DHL") { Caption = 'DHL'; }
    value(3; "FedEx") { Caption = 'FedEx'; }
    value(4; "UPS") { Caption = 'UPS'; }
    value(5; "PostalMail") { Caption = 'Postal Mail'; }
    value(6; "FullLoad") { Caption = 'Full Load'; }
    value(7; "WillCall") { Caption = 'Will Call'; }
}
```

- **Condizioni pagamento** del tipo di dati Enum, dove i valori sono definiti come segue:

```
enum 5334 "CDS Payment Terms Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Net30") { Caption = 'Net 30'; }
    value(2; "2%10Net30") { Caption = '2% 10; Net 30'; }
    value(3; "Net45") { Caption = 'Net 45'; }
    value(4; "Net60") { Caption = 'Net 60'; }
}
```

Tutti i valori di enumerazione di [!INCLUDE[prod_short](includes/prod_short.md)] precedenti sono mappati ai set di opzioni in [!INCLUDE[prod_short](includes/cds_long_md.md)].

### <a name="extending-option-sets-in-" />Estensione dei set di opzioni in [!INCLUDE[prod_short](includes/prod_short.md)]
1. Crea una nuova estensione AL.

2. Aggiungi un'estensione Enum per le opzioni che desideri estendere. Assicurati di utilizzare lo stesso valore. 

```
enumextension 50100 "CDS Payment Terms Code Extension" extends "CDS Payment Terms Code"
{
    value(779800001; "Cash Payment") { Caption = 'Cash Payment'; }
    value(779800002; "Transfer") { Caption = 'Transfer'; }
}
```

> [!IMPORTANT]  
> È necessario utilizzare gli stessi valori ID opzione da [!INCLUDE[prod_short](includes/cds_long_md.md)]quando estendi il valore di enumerazione [!INCLUDE[prod_short](includes/prod_short.md)]. In caso contrario la sincronizzazione non riesce.

> [!IMPORTANT]  
> Non utilizzare il carattere "," nelle didascalie e nei valori Enum. Questo non è attualmente supportato dal runtime [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> I primi dieci caratteri dei nomi e delle didascalie della nuova opzione devono essere univoci. Ad esempio, due opzioni denominate "Trasferimento 20 giorni lavorativi" e "Trasferimento 20 giorni di calendario" causeranno un errore perché entrambi hanno gli stessi primi 10 caratteri, "Trasferimento 2". Denominali, ad esempio "TRF20 WD" e "TRF20 CD".

### <a name="update--option-mapping" />Aggiornare la mappatura delle opzioni [!INCLUDE[prod_short](includes/cds_long_md.md)]
Ora puoi ricreare la mappatura tra le opzioni [!INCLUDE[prod_short](includes/cds_long_md.md)] e i record [!INCLUDE[prod_short](includes/prod_short.md)].

Nella pagina **Mapping tabella integrazione**, scegli la riga per il mapping **Condizioni pagamento**, quindi scegliere l'azione **Sincronizza record modificati**. La pagina **Mappatura opzione Dataverse** viene aggiornata con i record aggiuntivi di seguito.

|         Record                 | Valore opzione   | Didascalia valore opzione |
|--------------------------------|----------------|----------------------|
| Condizioni pagamento: NET30           | 1              | Importo netto a 30               |
| Condizioni pagamento: 2%10NET30       | 2              | 2% a 10; importo netto a 30        |
| Condizioni pagamento: NET45           | 3              | Importo netto a 45               |
| Condizioni pagamento: NET60           | 4              | Importo netto a 60               | 
| **Condizioni pagamento: CASH PAYME**  | **779800001**  | **Pagamento contante**     |
| **Condizioni pagamento: TRANSFER**    | **779800002**  | **Trasferimento**         |

La tabella **Condizioni pagamento** in [!INCLUDE[prod_short](includes/prod_short.md)] avrà quindi nuovi record per le opzioni [!INCLUDE[prod_short](includes/cds_long_md.md)]. Nella tabella seguente le nuove opzioni sono in grassetto. Le righe in corsivo rappresentano tutte le opzioni che ora possono essere sincronizzate. Le righe rimanenti rappresentano le opzioni non utilizzate e che verranno ignorate durante la sincronizzazione. È possibile rimuoverle o estendere le opzioni Dataverse con gli stessi nomi.

| Code       | Calcolo Data di Scadenza | Calcolo Sconto per Data | Sconto % | Calc. sc. pagam. su note credito | Descrizione       |
|------------|----------------------|---------------------------|------------|-------------------------------|-------------------|
| 10 GIORNI    | 10G                  |                           | 0.         | FALSE                         | 10 GG data fattura       |
| 14 GIORNI    | 14D                  |                           | 0.         | FALSE                         | 14 GG data fattura       |
| 15 GIORNI    | 15D                  |                           | 0.         | FALSE                         | 15 GG data fattura       |
| 1M(8G)     | 1M                   | 8G                        | 2.         | FALSE                         | 1 mese sconto cassa 2% (8G) |
| 2 GIORNI     | 2G                   |                           | 0.         | FALSE                         | 2 GG data fattura        |
| *2%10NET30* |                      |                           | 0.         | FALSE                         |                   |
| 21 GIORNI    | 21G                  |                           | 0.         | FALSE                         | 21 GG data fattura       |
| 30 GIORNI    | 30G                  |                           | 0.         | FALSE                         | 30 GG data fattura       |
| 60 GIORNI    | 60G                  |                           | 0.         | FALSE                         | 60 GG data fattura       |
| 7 GIORNI     | 7G                   |                           | 0.         | FALSE                         | 7 GG data fattura        |
| ***CASH PAYME*** |                      |                           | 0.         | FALSE                         |                   |
| MC         | MC                   |                           | 0.         | FALSE                         | Mese corrente     |
| PAC        | 0G                   |                           | 0.         | FALSE                         | Pagamento alla consegna  |
| *NET30*      |                      |                           | 0.         | FALSE                         |                   |
| *NET45*      |                      |                           | 0.         | FALSE                         |                   |
| *NET60*      |                      |                           | 0.         | FALSE                         |                   |
| ***TRANSFER*** |                      |                           | 0.         | FALSE                         |                   |

## <a name="see-also" />Vedere anche
[Mapping delle tabelle e dei campi da sincronizzare](admin-how-to-modify-table-mappings-for-synchronization.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
