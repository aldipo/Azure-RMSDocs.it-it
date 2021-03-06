---
# required metadata

title: Configurazione dei diritti di utilizzo per Azure Rights Management | Azure RMS
description:
keywords:
author: cabailey
manager: mbaldwin
ms.date: 06/08/2016
ms.topic: article
ms.prod: azure
ms.service: rights-management
ms.technology: techgroup-identity
ms.assetid: 97ddde38-b91b-42a5-8eb4-3ce6ce15393d

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: esaggese
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Configurazione dei diritti di utilizzo per Azure Rights Management

*Si applica a: Azure Rights Management, Office 365*

Quando si imposta la protezione su file o messaggi di posta elettronica mediante Azure Rights Management (Azure RMS) e non si usa un modello, è necessario configurare personalmente i diritti di utilizzo. Inoltre, quando si configurano modelli personalizzati per Azure RMS, si selezionano i diritti di utilizzo che verranno applicati automaticamente quando utenti, amministratori o servizi configurati selezionano il modello. Ad esempio, nel portale di Azure classico è possibile selezionare ruoli che configurano un raggruppamento logico di diritti di utilizzo oppure è possibile configurare singoli diritti.

Usare le informazioni incluse in questo articolo per configurare i diritti di utilizzo desiderati per l'applicazione in uso e comprendere come tali diritti vengono interpretati dalle applicazioni.

## Diritti di utilizzo e relative descrizioni
Le sezioni seguenti elencano e descrivono i diritti di utilizzo supportati da Rights Management e le relative modalità d'uso e interpretazione. Sono elencati in base al **Nome comune**, che corrisponde in genere al modo in cui il diritto di utilizzo viene visualizzato o indicato, una versione semplificata del valore costituito da una singola parola e usato nel codice, ovvero il valore **Codifica nei criteri**. Il valore **Costante o valore API** e il nome dell'SDK per una chiamata API MSIPC, usato quando si scrive un'applicazione abilitata per RMS che verifica un diritto di utilizzo o aggiunge un diritto di utilizzo a un criterio.


### Modifica contenuto, Modifica

Consente di modificare, riorganizzare, formattare o filtrare il contenuto all'interno dell'applicazione. Non concede il diritto di salvare la copia modificata.

**Codifica nei criteri**: DOCEDIT

**Implementazione nei diritti personalizzati di Office**: come parte delle opzioni *Modifica* e *Controllo completo*.

**Nome nel portale di Azure classico**: *Modifica contenuto*

**Nome nei modelli AD RMS**: *Modifica*

**Valore costante o valore API**: *non applicabile*

---

### Salva

Consente di salvare il documento nella posizione corrente.

**Codifica nei criteri**: EDIT

**Implementazione nei diritti personalizzati di Office**: come parte delle opzioni *Modifica* e *Controllo completo*.

**Nome nel portale di Azure classico**: *Salva file*

**Nome nei modelli AD RMS**: *Salva*

**Valore costante o valore API**: IPC_GENERIC_WRITEL"EDIT"

Nelle applicazioni di Office questo diritto consente anche di modificare il documento.

---

### Commento

Consente di aggiungere annotazioni o commenti al contenuto.

**Codifica nei criteri**: COMMENT

**Implementazione nei diritti personalizzati di Office**: non implementato.

**Nome nel portale di Azure classico**: non implementato.

**Nome nei modelli AD RMS**: non implementato.

**Valore costante o valore API**: IPC_GENERIC_COMMENTL"COMMENT"

Questo diritto è disponibile nell’SDK, è disponibile come criterio ad hoc nel modulo di protezione RMS per Windows PowerShell ed è stato implementato in alcune applicazioni di fornitori di software. Tuttavia, non è ampiamente utilizzato e non è attualmente supportato dalle applicazioni di Office.

---

### Salva con nome, Esporta

Abilita l'opzione per il salvataggio del contenuto con un nome file differente (Salva con nome). Per i documenti di Office, il file può essere salvato senza protezione.

**Codifica nei criteri**: EXPORT

**Implementazione nei diritti personalizzati di Office:** come parte delle opzioni *Modifica* e *Controllo completo*.

**Nome nel portale di Azure classico**: *Esporta contenuto (Salva con nome)*

**Nome nei modelli AD RMS**: *Esporta (Salva con nome*

**Valore costante o valore API**: IPC_GENERIC_EXPORTL"EXPORT"

Consente di eseguire anche altre opzioni di esportazione nelle applicazioni, ad esempio *Invia a OneNote*.

---

### Inoltra

Abilita l'opzione per l'inoltro di un messaggio di posta elettronica e per l'aggiunta di destinatari nelle righe *A* e *Cc* . Questo diritto non si applica ai documenti, ma solo ai messaggi di posta elettronica.

**Codifica nei criteri**: FORWARD

**Implementazione nei diritti personalizzati di Office:** negata quando si usa il criterio standard *Non inoltrare*.

**Nome nel portale di Azure classico:** *Inoltra*

**Nome nei modelli AD RMS:** *Inoltra*

**Valore costante o valore API:** IPC_EMAIL_FORWARDL"FORWARD"

Non consente al server d'inoltro di concedere diritti ad altri utenti come parte dell'azione di inoltro.

---

### Controllo completo

Concede tutti i diritti al documento. È possibile eseguire tutte le azioni disponibili.

**Codifica nei criteri**: OWNER

**Implementazione nei diritti personalizzati di Office:** come le opzioni personalizzate *Controllo completo*.

**Nome nel portale di Azure classico:** *Controllo completo*

**Nome nei modelli AD RMS:** *Controllo completo*

**Valore costante o valore API**: IPC_GENERIC_ALLL"OWNER"

Include la possibilità di rimuovere la protezione.

---

### Stampa

Abilita le opzioni per la stampa del contenuto.

**Codifica nei criteri**: PRINT

**Implementazione nei diritti personalizzati di Office:** come l'opzione *Stampa contenuto* nelle autorizzazioni personalizzate. Non è un'impostazione per ogni destinatario.

**Nome nel portale di Azure classico:** *Stampa*

**Nome nei modelli AD RMS:** *Stampa*

**Valore costante o valore API**: IPC_GENERIC_PRINTL"PRINT"

---

### Rispondi

Abilita l'opzione Rispondi in un client di posta elettronica. Non sono consentite modifiche delle righe *A* o *Cc* .

**Codifica nei criteri**: REPLY

**Implementazione nei diritti personalizzati di Office**: non applicabile

**Nome nel portale di Azure classico:** *Rispondi*

**Nome nei modelli AD RMS:** *Rispondi*

**Valore costante o valore API:** IPC_EMAIL_REPLY

---

### Rispondi a tutti

Abilita l'opzione *Rispondi a tutti* in un client di posta elettronica, ma non consente di aggiungere destinatari nelle righe *A* o *Cc* .

**Codifica nei criteri**: REPLYALL

**Implementazione nei diritti personalizzati di Office**: non applicabile

**Nome nel portale di Azure classico:** *Rispondi a tutti*

**Nome nei modelli AD RMS:** *Rispondi a tutti*

**Valore costante o valore API:** IPC_EMAIL_REPLYALLL"REPLYALL"

---

### Visualizza, Apri, Leggi

Consente all’utente di aprire il documento e visualizzarne il contenuto.

**Codifica nei criteri**: VIEW

**Implementazione nei diritti personalizzati di Office:** come il diritto personalizzato *Leggi*, opzione *Visualizza*.

**Nome nel portale di Azure classico**: *Visualizza contenuto*

**Nome nei modelli AD RMS:** *Visualizza*

**Valore costante o valore API**: IPC_GENERIC_READL"VIEW"

---

### Copia

Abilita le opzioni per la copia dei dati, inclusa l'acquisizione di schermate, nello stesso documento o in un altro.

**Codifica nei criteri:** EXTRACT

**Implementazione nei diritti personalizzati di Office:** come l'opzione di diritto personalizzato *Consenti agli utenti con accesso in lettura di copiare il contenuto*.

**Nome nel portale di Azure classico:** *Copia ed estrai contenuto*

**Nome nei modelli AD RMS:** *Estrai*

**Costante API o valore:** IPC_GENERIC_EXTRACTL"EXTRACT"

In alcune applicazioni consente anche di salvare l'intero documento in un formato non protetto.

---


### Consenti macro

Abilita l'opzione per l'esecuzione di macro o per l'accesso, a livello di programmazione o in remoto, al contenuto di un documento.

**Codifica nei criteri**: OBJMODEL

**Implementazione nei diritti personalizzati di Office:** come l'opzione del criterio personalizzato *Consenti accesso a livello di programmazione*. Non è un'impostazione per ogni destinatario.

**Nome nel portale di Azure classico:** *Consenti Macro*

**Nome nei modelli AD RMS:** *Consenti Macro*

**Valore costante o valore API:** non applicabile


## Diritti inclusi nei livelli di autorizzazioni

Alcune applicazioni raggruppano i diritti di utilizzo in livelli di autorizzazioni, per semplificare la selezione dei diritti di utilizzo che in genere vengono usati insieme. Questi livelli di autorizzazioni consentono di astrarre un livello di complessità dagli utenti, in modo che questi possano scegliere opzioni che sono basate sul ruolo.  Ad esempio, **Revisore** e **Coautore**. Anche se queste opzioni spesso mostrano agli utenti un riepilogo dei diritti, potrebbero non includere tutti i diritti elencati nella tabella precedente.

Usare la tabella seguente per un elenco di questi livelli di autorizzazioni e un elenco completo dei diritti che contengono.

|Livello di autorizzazioni|Applicazioni|Diritti inclusi (nome comune)|
|---------------------|----------------|---------------------------------|
|Visualizzatore|Portale di Azure classico<br /><br />Applicazione di condivisione Rights Management per Windows|Visualizza, Apri, Leggi; Rispondi; Rispondi a tutti|
|Revisore|Portale di Azure classico<br /><br />Applicazione di condivisione Rights Management per Windows|Visualizza, Apri, Leggi; Salva; Modifica contenuto, Modifica; Rispondi [[1]](#footnote-1); Rispondi a tutti [[1]](#footnote-1); Inoltra [[1]](#footnote-1)|
|Coautore|Portale di Azure classico<br /><br />Applicazione di condivisione Rights Management per Windows|Visualizza, Apri, Leggi; Salva; Modifica contenuto, Modifica; Copia; Visualizza diritti; Modifica diritti; Consenti macro; Salva con nome, Esporta; Stampa; Rispondi [[1]](#footnote-1); Rispondi a tutti [[1]](#footnote-1); Inoltra [[1]](#footnote-1)|
|Comproprietario|Portale di Azure classico<br /><br />Applicazione di condivisione Rights Management per Windows|Visualizza, Apri, Leggi; Salva; Modifica contenuto, Modifica; Copia; Visualizza diritti; Modifica diritti; Consenti macro; Salva con nome, Esporta; Stampa; Rispondi [[1]](#footnote-1); Rispondi a tutti [[1]](#footnote-1); Inoltra [[1]](#footnote-1); Controllo completo|

----

###### Nota 1
Non applicabile per l'applicazione di condivisione Microsoft Rights Management per Windows.

## Diritti inclusi nei modelli predefiniti
I diritti inclusi con i modelli predefiniti sono i seguenti:

|Nome visualizzato|Diritti inclusi (nome comune)|
|----------------|---------------------------------|
|&lt;*nome organizzazione*&gt; *- Solo visualizzazione riservata*|Visualizza, Apri, Leggi|
|&lt;*nome organizzazione*&gt; *- Riservato*|Visualizza, Apri, Leggi; Salva; Modifica contenuto, Modifica; Visualizza diritti; Consenti macro; Inoltra; Rispondi; Rispondi a tutti|

## Opzione Non inoltrare per i messaggi di posta elettronica

I client di Exchange e i servizi, ad esempio il client Outlook, l'app Outlook Web Access e le regole di trasporto di Exchange, offrono un'opzione aggiuntiva per la protezione dei diritti sulle informazioni relativa ai messaggi di posta elettronica: **Non inoltrare**. 

Anche se questa opzione viene visualizzata dagli utenti e dagli amministratori di Exchange come se fosse un modello predefinito di Rights Management selezionabile, l'opzione **Non inoltrare** non è un modello. È per questo motivo che non viene visualizzata nel portale di Azure classico quando si visualizzano e si gestiscono i modelli per Azure RMS. L'opzione **Non inoltrare** è invece un insieme di diritti che viene applicato in modo dinamico dagli utenti ai destinatari di posta elettronica.

Quando l'opzione **Non inoltrare** viene applicata a un messaggio di posta elettronica, i destinatari non possono inoltrarlo, stamparlo, copiarne il contenuto, salvarne gli allegati né salvarlo come un nome diverso. Ad esempio, nel client di Outlook, il pulsante Inoltra non è disponibile, le voci di menu **Salva con nome**, **Salva allegato** e **Stampa** non sono disponibili e non è possibile aggiungere o modificare i destinatari nei campi **A**, **Cc** e **Ccn**.

È importante distinguere tra l'applicazione dell'opzione **Non inoltrare** e l'applicazione di un modello che non concede il diritto di inoltro di un messaggio di posta elettronica: l'opzione **Non inoltrare** usa un elenco dinamico di utenti autorizzati in base ai destinatari scelti dall'utente del messaggio originale, mentre i diritti nel modello sono associati a un elenco statico di utenti autorizzati che l'amministratore ha specificato in precedenza. Qual è la differenza? Si consideri un esempio: 

Un utente vuole inviare per posta elettronica alcune informazioni a utenti specifici del reparto marketing, che non devono condividerle con nessun altro. Dovrà proteggere il messaggio di posta elettronica con un modello che limiti i diritti (visualizzazione, risposta e salvataggio) del reparto marketing?  Oppure dovrà scegliere l'opzione **Non inoltrare**? Entrambe le opzioni impediscono ai destinatari di inoltrare il messaggio di posta elettronica. 

- Se viene applicato il modello, i destinatari possono comunque condividere le informazioni con altri utenti del reparto marketing. Ad esempio, un destinatario potrebbe utilizzare Esplora risorse per trascinare il messaggio di posta elettronica in un percorso condiviso o in un'unità USB. Così il proprietario del messaggio di posta elettronica e tutti gli utenti del reparto marketing che hanno accesso a questo percorso potrebbero visualizzare le informazioni contenute nel messaggio di posta elettronica.
 
- Se invece si applica l'opzione **Non inoltrare**, i destinatari non possono condividere le informazioni con nessun altro utente del reparto marketing spostando il messaggio di posta elettronica in un altro percorso. In questo scenario, solo i destinatari originali e il proprietario del messaggio di posta elettronica saranno in grado di visualizzare le informazioni contenute nel messaggio di posta elettronica.

> [!NOTE] Usare l'opzione **Non inoltrare** quando è importante che soltanto i destinatari selezionati dal mittente possano visualizzare le informazioni contenute nel messaggio di posta elettronica. Utilizzare un modello per i messaggi di posta elettronica per limitare i diritti di un gruppo di persone specificato prima dall'amministratore, a prescindere dai destinatari scelti dal mittente.




## Vedere anche
[Configurazione di modelli personalizzati per Azure Rights Management](configure-custom-templates.md)



<!--HONumber=Jun16_HO2-->


