---
# required metadata

title: "Gestione del cliente: operazioni del ciclo di vita della chiave del tenant | Azure RMS"
description:
keywords:
author: cabailey
manager: mbaldwin
ms.date: 04/28/2016
ms.topic: article
ms.prod: azure
ms.service: rights-management
ms.technology: techgroup-identity
ms.assetid: c5b19c59-812d-420c-9c54-d9776309636c

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: esaggese
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---


# Gestione del cliente: operazioni del ciclo di vita della chiave del tenant

*Si applica a: Azure Rights Management, Office 365*

Se la gestione della chiave del tenant per Azure Rights Management viene eseguita dall'utente (scenario BYOK), usare le sezioni seguenti per ottenere altre informazioni sulle operazioni del ciclo di vita rilevanti per questa topologia.

## Revocare la chiave del tenant
Quando si annulla la sottoscrizione di Azure RMS, l'uso della chiave del tenant in Azure RMS viene interrotto e non è necessaria alcuna azione da parte dell'utente.

## Ridistribuire la chiave del tenant
Il processo di ridistribuzione della chiave è denominato anche rollover della chiave. Non ridistribuire la chiave tenant a meno che non sia effettivamente necessario. Alcuni client precedenti, ad esempio Office 2010, non erano progettati per gestire in modo efficiente le modifiche delle chiavi. In questo scenario è necessario cancellare lo stato di RMS nei computer tramite Criteri di gruppo o un meccanismo equivalente. In alcuni casi è tuttavia opportuno forzare la ridistribuzione della chiave del tenant, Ad esempio:

-   La società è stata divisa in due o più società. Quando si ridistribuisce la chiave del tenant, la nuova società non potrà accedere al nuovo contenuto pubblicato dai dipendenti e sarà in grado di accedere al vecchio contenuto se dispone di una copia della chiave del tenant precedente.

-   Eventuale violazione della copia master della chiave del tenant (copia in proprio possesso).

Quando si ridistribuisce la chiave del tenant, il nuovo contenuto è protetto tramite la nuova chiave. Poiché questo processo viene eseguito per fasi, per un certo periodo di tempo parte del nuovo contenuto continuerà a essere protetto tramite la chiave del tenant precedente. Il contenuto protetto in precedenza rimane tale rispetto alla chiave del tenant precedente. Per supportare questo scenario, Azure RMS mantiene la chiave del tenant precedente in modo da emettere licenze per il vecchio contenuto.

Per reimpostare la chiave del tenant, generare e creare una nuova chiave tramite Internet o di persona, usare le procedure descritte nella sezione [Implementazione della modalità BYOK](..\plan-design\plan-implement-tenant-key.md#implementing-your-azure-rights-management-tenant-key) dell'argomento [Pianificazione e implementazione della chiave del tenant di Azure Rights Management](..\plan-design\plan-implement-tenant-key.md).

## Eseguire il backup e il ripristino della chiave del tenant
L'utente è responsabile del backup della chiave del tenant. Se la chiave del tenant è stata generata dall'utente in un modulo di protezione hardware Thales, per eseguire il backup della chiave è sufficiente eseguire il backup del file della chiave in formato token, del file relativo all'ambiente e delle schede amministrative.

Se la chiave è stata trasferita tramite le procedure descritte nella sezione [Implementazione della modalità BYOK](../plan-design/plan-implement-tenant-key.md#implementing-your-azure-rights-management-tenant-key) dell'argomento [Pianificazione e implementazione della chiave del tenant di Azure Rights Management](../plan-design/plan-implement-tenant-key.md), Azure RMS manterrà il file della chiave in formato token come protezione da eventuali errori dei nodi di Azure RMS. È tuttavia opportuno tenere presente che questa azione non rappresenta un backup completo. Se ad esempio è necessaria una copia in testo non crittografato della chiave da usare all'esterno di un modulo di protezione hardware Thales, Azure RMS non sarà in grado di recuperarla perché dispone solo di una copia non recuperabile.

## Esportare la chiave del tenant
In uno scenario BYOK non è possibile esportare la chiave del tenant da Azure RMS. La copia presente in Azure RMS è non recuperabile. Per eliminare questa chiave in modo che non venga più usata, contattare il Servizio Supporto Tecnico Clienti Microsoft.

## Rispondere a una violazione di sicurezza
Indipendentemente dall'affidabilità, nessun sistema di sicurezza può considerarsi completo se non prevede un processo di risposta alle violazioni di sicurezza. La chiave del tenant può essere violata o rubata e anche se è protetta in modo efficiente, potrebbero essere presenti vulnerabilità nella tecnologia dei moduli di protezione hardware di generazione corrente e nella lunghezza e negli algoritmi correlati alle chiavi correnti.

Microsoft ha predisposto un team apposito per rispondere agli eventi imprevisti correlati alla sicurezza che possono verificarsi nei suoi prodotti e servizi. Non appena riceve un report plausibile su un evento imprevisto, il team si attiva per esaminarne l'ambito, la causa radice e le soluzioni. Se l'evento imprevisto influisce sulle risorse dell'utente, Microsoft invierà un messaggio di posta elettronica di notifica agli amministratori di tenant di Azure RMS all'indirizzo indicato al momento della sottoscrizione.

In caso di violazione di sicurezza, l'azione più efficace che l'utente o Microsoft possa intraprendere dipende dall'ambito della violazione stessa. Microsoft collaborerà con l'utente durante l'intero processo. Nella tabella seguente vengono descritte alcune situazioni tipiche e la risposta più probabile, sebbene la risposta esatta dipenda da tutte le informazioni raccolte durante l'analisi.

|Descrizione evento imprevisto|Risposta probabile|
|------------------------|-------------------|
|Perdita della chiave del tenant.|Ridistribuire la chiave del tenant. Vedere [Ridistribuire la chiave del tenant](#re-key-your-tenant-key).|
|Diritti di accesso alla chiave del tenant ottenuti da un utente non autorizzato o da malware, ma nessuna perdita della chiave.|La ridistribuzione della chiave del tenant non è sufficiente ed è necessaria un'analisi della causa radice. Se l'utente non autorizzato ha ottenuto l'accesso a causa di un bug del processo o del software, questo problema deve essere risolto.|
|Vulnerabilità scoperta nella tecnologia del moduli di protezione hardware di generazione corrente.|Microsoft deve aggiornare i moduli di protezione hardware. Se si ritiene che la vulnerabilità abbia provocato l'esposizione di chiavi, Microsoft inviterà tutti i clienti a rinnovare le chiavi tenant.|
|Vulnerabilità scoperta nell'algoritmo RSA o nella lunghezza della chiave oppure attacchi di forza bruta diventati realizzabili a livello di calcolo.|Microsoft deve aggiornare Azure RMS per supportare nuovi algoritmi e lunghezze maggiori della chiave che siano resilienti e invitare tutti i clienti a rinnovare le proprie chiavi tenant.|




<!--HONumber=Apr16_HO4-->


