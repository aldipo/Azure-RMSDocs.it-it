---
# required metadata

title: Come usare il rilevamento dei documenti | Azure RMS
description: La funzionalità di rilevamento dei documenti richiede la comprensione di alcuni aspetti semplici relativi alla gestione dei metadati associati e alla registrazione con il servizio.
keywords:
author: bruceperlerms
manager: mbaldwin
ms.date: 04/28/2016
ms.topic: article
ms.prod: azure
ms.service: rights-management
ms.technology: techgroup-identity
ms.assetid: 70E10936-7953-49B0-B0DC-A5E7C4772E60
# optional metadata

#ROBOTS:
audience: developer
#ms.devlang:
ms.reviewer: shubhamp
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Procedura: Usare il rilevamento dei documenti

L'uso della funzionalità di rilevamento dei documenti richiede la comprensione di alcuni aspetti semplici relativi alla gestione dei metadati associati e alla registrazione con il servizio.

## Gestione dei metadati associati al rilevamento dei documenti

Tutti i sistemi operativi che supportano il rilevamento dei documenti presentano implementazioni simili, tra cui un set di proprietà che rappresentano i metadati, un nuovo parametro aggiunto ai metodi di creazione dei criteri utente e un metodo per la registrazione dei criteri di cui tenere traccia con il servizio di rilevamento dei documenti.

Dal punto di vista operativo, solo le proprietà relative al **nome contenuto** e al **tipo di notifica** sono necessarie per rilevamento dei documenti.

La sequenza di passaggi da usare per configurare il rilevamento dei documenti per un dato contenuto è la seguente:

-   Creare un oggetto **metadati di licenza**.

    Per altre informazioni, vedere [**LicenseMetadata**](/rights-management/sdk/4.2/api/android/com.microsoft.rightsmanagement#msipcthin2_licensemetadata_interface_java) o [**MSLicenseMetadata**](/rights-management/sdk/4.2/api/iOS/mslicensemetadata#msipcthin2_mslicensemetadata_class_objc).

-   Impostare il **nome contenuto** e il **tipo di notifica**. Queste sono le uniche proprietà necessarie.

    Per altre informazioni, vedere i metodi di accesso alle proprietà per la classe di metadati di licenza appropriata per la piattaforma, ovvero [**LicenseMetadata**](/rights-management/sdk/4.2/api/android/com.microsoft.rightsmanagement#msipcthin2_licensemetadata_interface_java) o [**MSLicenseMetadata**](/rights-management/sdk/4.2/api/iOS/mslicensemetadata#msipcthin2_mslicensemetadata_class_objc).

-   Per il tipo di criteri, modello o ad hoc:

    -   Per il rilevamento dei documenti basato su modello, creare un oggetto **criteri utente** passando i metadati di licenza come parametro.

        Per altre informazioni, vedere [**UserPolicy.create**](/rights-management/sdk/4.2/api/android/userpolicy#msipcthin2_userpolicy_class_java) e [**MSUserPolicy.userPolicyWithTemplateDescriptor**](/rights-management/sdk/4.2/api/iOS/msuserpolicy#msipcthin2_msuserpolicy_templatedescriptor_property_objc).

    -   Per il rilevamento dei documenti su base ad hoc, impostare la proprietà **metadati di licenza** sull’oggetto **descrittore criteri**.

        Per altre informazioni, vedere [**PolicyDescriptor.getLicenseMetadata**](/rights-management/sdk/4.2/api/android/policydescriptor#msipcthin2_policydescriptor_interface_java), [**PolicyDescriptor.setLicenseMetadata**](/rights-management/sdk/4.2/api/android/policydescriptor#msipcthin2_policydescriptor_setlicensemetadata_java) e [**MSPolicyDescriptor.licenseMetadata**](/rights-management/sdk/4.2/api/iOS/mspolicydescriptor#msipcthin2_mspolicydescriptor_licensemetadata_property_objc).

    **Nota** È possibile accedere direttamente all’oggetto  metadati di licenza solo durante il processo di configurazione del rilevamento dei documenti per i criteri utente specificati. Dopo la creazione dell'oggetto criteri utente, i metadati di licenza associati non sono accessibili, ovvero la modifica dei valori dei metadati di licenza non produce alcun effetto.

     

-   Chiamare il metodo di registrazione alla piattaforma per il rilevamento dei documenti.

    Vedere [**MSUserPolicy.registerForDocTracking**](/rights-management/sdk/4.2/api/iOS/msuserpolicy#msipcthin2_msuserpolicy_registerfordoctracking_userid_authenticationcallback_completionblock_method_objc) o [**UserPolicy.registerForDocTracking**](/rights-management/sdk/4.2/api/iOS/msuserpolicy#msipcthin2_msuserpolicy_registerfordoctracking_userid_authenticationcallback_completionblock_method_objc).

 

 


<!--HONumber=Jun16_HO2-->


