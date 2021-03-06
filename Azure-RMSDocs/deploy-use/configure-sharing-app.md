---
# required metadata

title: Applicazione di condivisione Rights Management&colon; installazione e configurazione dei client | Azure RMS
description:
keywords:
author: cabailey
manager: mbaldwin
ms.date: 04/28/2016
ms.topic: article
ms.prod: azure
ms.service: rights-management
ms.technology: techgroup-identity
ms.assetid: b9af5dc3-73d4-4147-b7ef-f6803b0d5216

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: esaggese
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Applicazione Rights Management sharing: installazione e configurazione dei client

*Si applica a: Azure Rights Management, Office 365*

L'applicazione di condivisione Rights Management (RMS) è necessaria affinché i computer client possano usare Azure RMS con Office 2010 ed è consigliata per tutti i computer e i dispositivi mobili che supportano Azure RMS. L'applicazione di condivisione RMS si integra con le applicazioni di Office installando un componente aggiuntivo di Office per consentire agli utenti di proteggere facilmente i file e i messaggi e-mail direttamente dalla barra multifunzione. Offre anche protezione generica per tipi di file non supportati in modalità nativa da Azure RMS e un sito per il rilevamento dei documenti che permette agli utenti di tenere traccia dei file protetti e di revocarli.

## Applicazione RMS sharing per Windows: installazione e configurazione
Per installare e configurare l'applicazione di condivisione RMS per Windows per una distribuzione aziendale, vedere [Guida dell'amministratore dell'applicazione di condivisione Rights Management](../rms-client/sharing-app-admin-guide.md).

> [!TIP]
> Se si vuole installare e testare rapidamente l'applicazione di condivisione RMS per un singolo computer, vedere [Scaricare e installare l'applicazione di condivisione Rights Management](../rms-client/install-sharing-app.md) in [Guida dell'utente dell'applicazione di condivisione Rights Management](../rms-client/sharing-app-user-guide.md).

## Applicazione RMS sharing per piattaforme mobili: Installazione e gestione
Per installare l'applicazione RMS sharing per le piattaforme mobili, è possibile scaricare l'app rilevante usando i collegamenti disponibili nella [pagina di Microsoft Rights Management](http://go.microsoft.com/fwlink/?LinkId=303970). Non è necessaria alcuna configurazione per usare Azure RMS con questa app.

**Se si ha Microsoft Intune**: poiché l'app RMS sharing include il kit di distribuzione del software per l'app Microsoft Intune, sono disponibili le opzioni seguenti:

-   Per i dispositivi registrati da Intune, è possibile distribuire e gestire l'app RMS sharing per i dispositivi che eseguono iOS e Android. Per altre informazioni, vedere l'articolo relativo alla [configurazione e distribuzione dei criteri di gestione delle applicazioni per dispositivi mobili nella console di Microsoft Intune](/intune/deploy-use/configure-and-deploy-mobile-application-management-policies-in-the-microsoft-intune-console) nella documentazione di Intune Per il passaggio 2, usare le istruzioni per pubblicare un'app gestita da criteri.

-   Per i dispositivi non registrati da Intune, è possibile gestire l'app RMS sharing per i dispositivi che eseguono Android. Per altre informazioni, vedere [Creare e distribuire i criteri di gestione delle app per dispositivi mobili con Microsoft Intune](/intune/deploy-use/create-and-deploy-mobile-app-management-policies-with-microsoft-intune).



<!--HONumber=Apr16_HO4-->


