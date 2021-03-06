---
# required metadata

title: Guida per gli sviluppatori di RMS | Azure RMS
description: Sono ora disponibili tre generazioni di Rights Management SDK.
keywords:
author: bruceperlerms
manager: mbaldwin
ms.date: 04/28/2016
ms.topic: article
ms.prod: azure
ms.service: rights-management
ms.technology: techgroup-identity
ms.assetid: 0510ead4-2fe7-4269-885b-fe16bcc69888
# optional metadata

#ROBOTS:
audience: developer
#ms.devlang:
ms.reviewer: shubhamp
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Guida per gli sviluppatori RMS

## Panoramica ##
Sono ora disponibili tre generazioni di Rights Management SDK: **Microsoft Rights Management SDK 4.2** per Android, iOS/OS X, dispositivi Windows e Linux, **Microsoft Rights Management SDK 2.1** per client Windows Desktop e l'obsoleto **AD RMS SDK**.

## Software Development Kit ##
| SDK | Descrizione |
|------|---------|
| [RMS SDK 4.2](active-directory-rights-management-services-multi-platform-thin-client-sdk-portal.md) | Semplice set di strumenti all'avanguardia che offre un'esperienza di sviluppo leggera per abilitare la protezione delle informazioni nelle app per dispositivi Android, iOS, Mac OS X, Windows Phone/RT e Linux/C++ tramite i servizi di Microsoft Rights Management |
| [RMS SDK 2.1](microsoft-information-protection-and-control-client-portal.md) | SDK potente che consente agli sviluppatori di applicazioni Windows Desktop e ai provider di soluzioni basate su server di abilitare la tecnologia Rights Management nei loro prodotti|
|[AD RMS SDK]()|** NOTA **: la funzionalità per l'uso di AD RMS SDK esposta dal client in Msdrm.dll è disponibile in Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Al suo posto, usare Microsoft Rights Management Services SDK 2.1, che sfrutta le funzionalità esposte dal client in Msipc.dll.|
|[API di script AD RMS]()| Usata per creare script per l'amministrazione di un'installazione di AD RMS|

## Esempi di codice e strumenti ##
Questa raccolta di esempi di codice RMS e strumenti di supporto per gli sviluppatori fornita da Microsoft è compatibile con tutti i sistemi operativi supportati, Android, iOS/OS X, Windows Phone e Windows Desktop, e viene aggiornata periodicamente per mantenere la compatibilità con l'SDK supportato.

| Elemento | Sistema operativo | Supporto versione SDK | Descrizione |
|------|------------------|------------------------|-------------|
| [Lettura di un PDF protetto da PFILE](https://blogs.msdn.microsoft.com/rms/2015/11/09/reading-a-pfile-protected-pdf/) | Desktop Windows| [RMS SDK 2.1](microsoft-information-protection-and-control-client-portal.md) e versioni successive dell'SDK 2.x | L'esempio di codice relativo alla **lettura di un PDF protetto da PFILE** è un semplice esempio disponibile nel blog per sviluppatori RMS che usa l'API file MSIPC per decrittografare e aprire un documento PDF protetto da PFILE.|
| [IpcManagedAPI](https://github.com/Azure-Samples/active-directory-dotnet-rms) | Desktop Windows | [RMS SDK 2.1](microsoft-information-protection-and-control-client-portal.md) e versioni successive dell'SDK 2.x | **IpcManagedAPI** è una rappresentazione .NET (C#) di RMS SDK 2.1 che consente di abilitare in modo semplice le applicazioni gestite per RMS.|
| [IPCNotepad](https://code.msdn.microsoft.com/ipcnotepad-sample-f67dae80) | Desktop Windows | [RMS SDK 2.1](microsoft-information-protection-and-control-client-portal.md) e versioni successive dell'SDK 2.x| **IPCNotepad** è un'applicazione di esempio abilitata per RMS che illustra l'esecuzione dei passaggi di base che deve eseguire un'applicazione abilitata per RMS per la protezione e l'utilizzo di contenuto con restrizioni.|
| [IpcDlp](https://github.com/Azure-Samples/active-directory-dotnet-rms)|Desktop Windows|[RMS SDK 2.1](microsoft-information-protection-and-control-client-portal.md) e versioni successive dell'SDK 2.x|**IpcDlp** è un'applicazione di esempio di protezione dalla perdita di dati abilitata per RMS che illustra l'esecuzione dei passaggi di base che deve eseguire un'applicazione di protezione dalla perdita di dati abilitata per RMS usando l'API file per la protezione e l'utilizzo di contenuto con restrizioni.|
| [IpcAzureApp](https://github.com/Azure-Samples/active-directory-dotnet-rms) | Desktop Windows|[RMS SDK 2.1](microsoft-information-protection-and-control-client-portal.md) e versioni successive dell'SDK 2.x|**IpcAzureApp** è un esempio che illustra come usare RMS SDK nell'applicazione Azure per proteggere i dati nell'archiviazione BLOB di Azure.|
| [RmsDocumentInspector](https://github.com/Azure-Samples/active-directory-dotnet-rms) | Desktop Windows|[RMS SDK 2.1](microsoft-information-protection-and-control-client-portal.md) e versioni successive dell'SDK 2.x|**RmsDocumentInspector** è uno strumento in grado di fornire informazioni su qualsiasi file protetto da RMS, ad esempio per quanto riguarda i diritti utente o l'ID contenuto.|
| [RmsFileWatcher](https://github.com/Azure-Samples/active-directory-dotnet-rms) | Desktop Windows|[RMS SDK 2.1](microsoft-information-protection-and-control-client-portal.md) e versioni successive dell'SDK 2.x|**RmsFileWatcher** è un esempio che illustra come creare un'applicazione Windows che controlla le directory nel file system e applica i criteri di protezione RMS a ogni modifica, ad esempio per i file modificati o aggiunti.|
| [Scenari di utilizzo di iOS/OS X](https://msdn.microsoft.com/en-us/library/dn758307(v=vs.85).aspx) |iOS/OS X|[RMS SDK 4.2](active-directory-rights-management-services-multi-platform-thin-client-sdk-portal.md) e versioni successive dell'SDK 4.x|Esempi di codice **Objective C** che rappresentano importanti scenari di sviluppo per familiarizzare con RMS SDK. Gli esempi includono l'uso del formato Microsoft Protected File, di formati di file protetti personalizzati e di controlli dell'interfaccia utente personalizzati.|
| [Libreria dell'interfaccia utente e app di esempio](https://github.com/AzureAD/rms-sdk-ui-for-ios) |iOS|[RMS SDK 4.2](active-directory-rights-management-services-multi-platform-thin-client-sdk-portal.md) e versioni successive dell'SDK 4.x|**Librerie dell'interfaccia utente e app di esempio per iOS** in GitHub, per essere operativi in tempi brevi e riutilizzare l'interfaccia utente standard nelle app.|
| [Libreria dell'interfaccia utente e app di esempio](https://github.com/AzureAD/rms-sdk-ui-for-android) |Android|[RMS SDK 4.2](active-directory-rights-management-services-multi-platform-thin-client-sdk-portal.md) e versioni successive dell'SDK 4.x|**Librerie dell'interfaccia utente e app di esempio per Android** in GitHub, per essere operativi in tempi brevi e riutilizzare l'interfaccia utente standard nelle app.|
| [Scenari di utilizzo di Android](https://msdn.microsoft.com/en-us/library/dn758246(v=vs.85).aspx) |Android|[RMS SDK 4.2](active-directory-rights-management-services-multi-platform-thin-client-sdk-portal.md) e versioni successive dell'SDK 4.x|**Esempi di codice Java** che rappresentano importanti scenari di sviluppo per familiarizzare con RMS SDK. Gli esempi includono l'uso del formato Microsoft Protected File, di formati di file protetti personalizzati e di controlli dell'interfaccia utente personalizzati.|


<!--HONumber=Apr16_HO4-->


