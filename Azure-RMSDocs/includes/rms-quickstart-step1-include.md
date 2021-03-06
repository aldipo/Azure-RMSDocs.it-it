![Passaggio 1 dell'esercitazione introduttiva](../media/AzRMS_QuickStartSteps1.PNG)

Anche se si dispone di una sottoscrizione che supporta Azure Rights Management, il servizio è disabilitato per impostazione predefinita. Per attivarlo, usare l'interfaccia di amministrazione di Office 365 o il portale di Azure classico:

-   Se è disponibile una sottoscrizione di Office 365 che include Azure Rights Management o una sottoscrizione di Office 365 che esclude Azure Rights Management, ma è disponibile una sottoscrizione di Azure RMS Premium: **usare l'interfaccia di amministrazione di Office 365**.

-   Se non si ha una sottoscrizione di Office 365: **usare il portale di Azure classico**.

![Portale di Azure classico](../media/AzRMS_Tutorial_1_Screenshots.png)

#### Per attivare Rights Management mediante l'interfaccia di amministrazione di Office 365

1.  Passare al [portale di Office 365](https://portal.office.com/) e accedere con l'account aziendale o dell’istituto di istruzione.

2.  Se l'interfaccia di amministrazione di Office 365 non viene visualizzata automaticamente, selezionare l'icona di avvio dell'app in alto a sinistra e scegliere **Amministratore**. Il riquadro **Amministratore** viene visualizzato solo dagli amministratori di Office 365.

    > [!TIP]
    > Per la guida all'interfaccia di amministrazione, vedere [Informazioni sull'interfaccia di amministrazione di Office 365 - Guida per gli amministratori](https://support.office.com/article/About-the-Office-365-admin-center-Admin-Help-58537702-d421-4d02-8141-e128e3703547).

3.  Nel riquadro sinistro fare clic su **IMPOSTAZIONI SERVIZIO**.

4.  Fare clic su **Rights Management**.

5.  Nella pagina **RIGHTS MANAGEMENT** fare clic su **Gestione**.

6.  Nella pagina **Rights Management** fare clic su **attiva**.

7.  Quando viene chiesto **se si desidera attivare Rights Management**, fare clic **attiva**.

Viene visualizzato il messaggio di avvenuta attivazione di Rights management e l'opzione di disattivazione (potrebbe essere necessario aggiornare manualmente la pagina) **** .

A questo punto, non scegliere **funzionalità avanzate**. Con questa operazione viene infatti visualizzato il portale di Azure classico in cui è possibile configurare i modelli, che non sono necessari per questa esercitazione. Chiudere invece l’interfaccia di amministrazione di Office 365.

#### Per attivare Rights Management dal portale di Azure

1.  Passare al [portale di Azure classico](http://go.microsoft.com/fwlink/p/?LinkID=275081) e accedere.

2.  Nel riquadro sinistro fare clic su **ACTIVE DIRECTORY**.

3.  Nella pagina **active directory** fare clic su **RIGHTS MANAGEMENT**.

4.  Selezionare la directory da gestire per [!INCLUDE[aad_rightsmanagement_2](../includes/aad_rightsmanagement_2_md.md)], fare clic su **ATTIVA** e quindi confermare l'azione.

Come **STATO RIGHTS MANAGEMENT** ora verrà visualizzato **Attivo** e l'opzione **ATTIVA** verrà sostituita da **DISATTIVA**.

Sebbene nel portale sia possibile configurare anche altre opzioni relative a Rights Management, queste non sono necessarie ai fini dell'esercitazione ed è pertanto possibile chiudere il portale di Azure classico.

Quelle sopra indicate sono tutte le operazioni da eseguire per il primo passaggio. Il servizio viene attivato in modo che a questo punto tutti gli utenti dell'organizzazione possano iniziare a proteggere i documenti riservati e importanti. In un ambiente di produzione è possibile limitare inizialmente gli utenti che possono effettuare questa operazione, in modo da eseguire un'implementazione graduale. Questo tuttavia non è necessario ai fini dell'esercitazione.

Anche se la procedura corrispondente non è inclusa in questa esercitazione, è probabile che per una distribuzione di produzione si desideri configurare modelli personalizzati. I modelli consentono agli utenti di applicare rapidamente le impostazioni corrette quando ne hanno bisogno per proteggere i file. Quando si attiva Rights Management, si ottengono automaticamente 2 modelli predefiniti ed è probabile che, in un ambiente di produzione, si desideri integrare tali modelli con modelli personalizzati. I modelli, tuttavia, non sono necessari per questa esercitazione ed è pertanto possibile procedere con il passaggio successivo.

|Se si desiderano altre informazioni|Informazioni aggiuntive|
|--------------------------------|--------------------------|
|Informazioni sull'attivazione di Rights Management e sul controllo di chi può proteggere file e messaggi di posta elettronica quando il servizio è attivato   →|[Attivazione di Azure Rights Management](../deploy-use/activate-azure-classic.md)|
|Informazioni sui modelli predefiniti e su come creare nuovi modelli personalizzati   →|[Configurazione di modelli personalizzati per Azure Rights Management](../deploy-use/create-template.md)|


<!--HONumber=Apr16_HO3-->


