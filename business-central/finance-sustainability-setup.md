---
title: Setup sostenibilità
description: Scopri come impostare funzionalità di sostenibilità.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD'
ms.search.form: null
ms.date: 04/24/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Setup sostenibilità  

Per far funzionare correttamente il modulo Sostenibilità, devi prima impostare alcuni controlli e istruzioni di base relativi all'intera funzionalità.  

Per impostare un modulo di sostenibilità, segui i passaggi successivi:  

1. Scegli l'icona ![lampadina che apre la funzione Dimmi.](media/ui-search/search_small.png "Dimmi cosa vuoi fare") immetti **Setup sostenibilità**, quindi scegli il collegamento correlato.  
2. Nella Scheda dettaglio **Generale**, configura i campi obbligatori relativi a questo modulo:   

|  Campo  |  Descrizione  |  
|--------|--------------| 
| **Codice unità di misura emissioni** | Specifica il codice dell'unità di misura utilizzato per registrare le emissioni. |
| **Posizioni decimali emissioni** | Specifica il numero di cifre decimali visualizzate per gli importi delle emissioni. L'impostazione predefinita, 2:5, specifica che tutti gli importi vengono visualizzati con un minimo di 2 cifre decimali e un massimo di 5 cifre decimali. Puoi anche immettere un numero fisso, come 2, il che significa anche che gli importi verranno visualizzati con due cifre decimali. |
| **Paese/area geografica obbligatorio** | Specifica se paese/area geografica è obbligatorio. Puoi utilizzare questo campo nelle registrazioni senza configurarlo, ma puoi selezionarlo se desideri imporre agli utenti di compilare il campo prima della pubblicazione. |
| **Centro di responsabilità obbligatorio** | Specifica se il centro di responsabilità è obbligatorio, poiché il centro di responsabilità può essere utilizzato come struttura per misurare le emissioni basate sulla struttura. Puoi utilizzare questo campo nelle registrazioni senza configurarlo, ma puoi selezionarlo se desideri imporre agli utenti di compilare il campo prima della pubblicazione. |
| **Modifica della base di calcolo dei blocchi se esistono movimenti contabili** | Specifica se la modifica della base di calcolo nella Categoria conto è bloccata al momento dell'immissione della sostenibilità, il che significa che questa formula è già stata applicata. |
| **Abilita verifica errori in background** | Specifica se il controllo degli errori in background delle righe di registrazione della sostenibilità è abilitato. |

> [!NOTE]
> Dopo aver abilitato o disattivato il **controllo errori in background** nei giornali di registrazione, dovrai effettuare nuovamente l'accesso prima di iniziare la nuova configurazione.
 

3.  Nella Scheda dettaglio **Calcoli**, configura i campi obbligatori relativi alle formule utilizzate per il calcolo delle emissioni:  

|  Campo  |  Descrizione  |  
|--------|--------------| 
| **Posizioni decimali combustibile/elettricità** | Specifica il numero di cifre decimali visualizzate per gli importi di combustibile/elettricità. L'impostazione predefinita, 2:5, specifica che tutti gli importi vengono visualizzati con un minimo di 2 cifre decimali e un massimo di 5 cifre decimali. Puoi anche immettere un numero fisso, come 2, il che significa anche che gli importi verranno visualizzati con due cifre decimali. |
| **Posizioni decimali distanza** | Specifica il numero di cifre decimali visualizzate per le misurazioni della distanza. L'impostazione predefinita, 2:5, specifica che tutti gli importi vengono visualizzati con un minimo di 2 cifre decimali e un massimo di 5 cifre decimali. Puoi anche immettere un numero fisso, come 2, il che significa anche che gli importi verranno visualizzati con due cifre decimali. |
| **Posizioni decimali importo personalizzato** | Specifica il numero di cifre decimali visualizzate per gli importi personalizzati. L'impostazione predefinita, 2:5, specifica che tutti gli importi vengono visualizzati con un minimo di 2 cifre decimali e un massimo di 5 cifre decimali. Puoi anche immettere un numero fisso, come 2, il che significa anche che gli importi verranno visualizzati con due cifre decimali. |

4.  Completa la configurazione nella Scheda dettaglio **Reporting**, per il reporting alle autorità:   

|  Campo  |  Descrizione  |  
|--------|--------------| 
| **Codice unità gerarchica di misura delle emissioni** | Specifica il codice dell'unità di misura utilizzato per segnalare le emissioni, poiché è possibile utilizzare unità di misura diverse per il reporting alle autorità. Questo campo non è applicabile ai report standard. |
| **Creazione report fattore UOM** | Specifica il fattore dell'unità di misura utilizzato per registrare le emissioni se utilizzi unità di misura diverse per il reporting alle autorità. |
| **Approssimazione di arrotondamento delle emissioni** | Specifica le dimensioni dell'intervallo da utilizzare quando si arrotondano gli importi delle emissioni per il reporting alle autorità. |
| **Tipo di arrotondamento delle emissioni** | Specifica il modo in cui il programma arrotonda un importo di emissione per il reporting alle autorità, utilizzando le opzioni Più vicino, Su o Giù. |

>[!NOTE]
> Nella versione 24.0, [!INCLUDE[prod_short](includes/prod_short.md)] non supporta il reporting ad alcuna autorità. Quindi, il campo relativo alla configurazione nella Scheda dettaglio **Reporting** verrà utilizzato per future funzionalità di reporting, ma può essere utilizzato anche dai partner nelle versioni localizzate.

## Vedere anche  
[Dati finanziari](finance.md)  
[Panoramica della gestione della sostenibilità](finance-manage-sustainability.md)    
[Contabilità generale e grafico dei conti di sostenibilità](finance-sustainability-accounts-ledger.md)    
[Come registrare le emissioni](finance-sustainability-journal.md)  
[Usare [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
