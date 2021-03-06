---
# required metadata

title: Configurazione di applicazioni per Azure Rights Management | Azure RMS
description:
keywords:
author: cabailey
manager: mbaldwin
ms.date: 04/28/2016
ms.topic: article
ms.prod: azure
ms.service: rights-management
ms.technology: techgroup-identity
ms.assetid: ea09cbc5-b98b-444e-8b60-5bc3cb199c36

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: esaggese
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Configurazione di applicazioni per Rights Management di Windows Azure

*Si applica a: Azure Rights Management, Office 365*

> [!NOTE]
> Queste informazioni sono destinate agli amministratori e ai consulenti IT che hanno distribuito Azure Rights Management. Per una guida per l'utente e informazioni su come usare Rights Management per una specifica applicazione o come aprire un file protetto tramite diritti, vedere la guida e le informazioni aggiuntive fornite in dotazione con l'applicazione.
>
> Ad esempio, per le applicazioni Office fare clic sull'icona della Guida e immettere i termini di ricerca, ad esempio **Rights Management** o **IRM**. Per l'applicazione di condivisione RMS per Windows, vedere [Guida dell'utente dell'applicazione di condivisione Rights Management](../rms-client/sharing-app-user-guide.md).

Dopo avere distribuito Azure Rights Management (RMS) per l'organizzazione, usare le informazioni seguenti per configurare applicazioni e servizi per il supporto di Azure RMS. Sono incluse le applicazioni di Office quali Word 2013 e Word 2010 e i servizi come Exchange Online (le regole di trasporto, la prevenzione della perdita di dati, l'opzione Non inoltrare e la crittografia messaggi) e SharePoint Online (librerie protette). Per informazioni sul supporto di Rights Management da parte di queste applicazioni e servizi, vedere [Supporto di Microsoft Azure Rights Management da parte delle applicazioni](../understand-explore/applications-support.md).

> [!IMPORTANT]
> Per informazioni sulle versioni supportate e altri requisiti, vedere [Requisiti per Azure Rights Management](../get-started/requirements-azure-rms.md).

-   [Office 365: configurazione di client e servizi online](configure-office365.md)

    -   [Exchange Online: configurazione di IRM](configure-office365.md#exchange-online-irm-configuration)

    -   [SharePoint Online e OneDrive for Business: configurazione di IRM](configure-office365.md#sharepoint-online-and-onedrive-for-business-irm-configuration)

- [Applicazioni di Office: configurazione dei client](configure-office-apps.md)

    -   [Office 2016 e Office 2013](configure-office-apps.md#office-2016-and-office-2013)

    -   [Office 2010](configure-office-apps.md#office-2010)

-   [Applicazione Rights Management sharing: installazione e configurazione dei client](configure-sharing-app.md)

    -   [Applicazione RMS sharing per Windows: installazione e configurazione](configure-sharing-app.md#the-rms-sharing-application-for-windows-installation-and-configuration)

    -   [Applicazione RMS sharing per piattaforme mobili: Installazione e gestione](configure-sharing-app.md#the-rms-sharing-application-for-mobile-platforms-installation-and-management)


Per configurare i server locali, ad esempio Exchange Server e SharePoint Server, vedere [Distribuzione del connettore di Azure Rights Management](deploy-rms-connector.md).

> [!TIP]
> Per esempi generali e screenshot delle applicazioni configurate per l'uso di Azure RMS, vedere [Azure RMS in azione: Cosa vedono gli amministratori e gli utenti](../understand-explore/what-admins-users-see.md)..


Oltre a queste applicazioni e a questi servizi, esistono altre applicazioni che supportano le API di RMS. Questa categoria include le applicazioni line-of-business scritte internamente mediante RMS SDK, nonché le applicazioni di produttori software scritte mediante RMS SDK. Per tali applicazioni, seguire le istruzioni fornite con esse.

## Passaggi successivi
Dopo aver configurato le applicazioni per il supporto di Azure Rights Management, usare la [Guida di orientamento per la distribuzione di Azure Rights Management](../plan-design/deployment-roadmap.md) per verificare se può essere necessario eseguire operazioni di configurazione aggiuntive prima di distribuire [!INCLUDE[aad_rightsmanagement_1](../includes/aad_rightsmanagement_1_md.md)] a utenti e amministratori. Se tali operazioni non sono necessarie, possono risultare utili le informazioni operative seguenti:

- [Verifica di Azure Rights Management](verify.md)

- [Consentire agli utenti di proteggere i file tramite Azure Rights Management](help-users.md)

- [Registrazione e analisi dell'utilizzo di Azure Rights Management](log-analyze-usage.md)

- [Operazioni relative alla chiave del tenant di Azure Rights Management](operations-tenant-key.md)




<!--HONumber=Apr16_HO4-->


