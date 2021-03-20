---
title: Migrer le courrier électronique et le calendrier d’entreprise à partir de Google Workspace
f1.keywords:
- NOCSH
ms.author: twerner
author: twernermsft
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
ms.custom:
- AdminSurgePortfolio
- adminvideo
monikerRange: o365-worldwide
search.appverid:
- BCS160
- MET150
- MOE150
description: Découvrez comment migrer le courrier électronique, les contacts et le calendrier de Google Workspace vers Microsoft 365 pour les entreprises.
ms.openlocfilehash: d6639032b379a2cd632b6ab6ee7e4082b1e7be0b
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50913621"
---
# <a name="migrate-business-email-and-calendar-from-google-workspace"></a><span data-ttu-id="2cafc-103">Migrer le courrier électronique et le calendrier d’entreprise à partir de Google Workspace</span><span class="sxs-lookup"><span data-stu-id="2cafc-103">Migrate business email and calendar from Google Workspace</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4LPt6?autoplay=false]

<span data-ttu-id="2cafc-104">Vous pouvez utiliser une migration d’administration vers Exchange Online à partir de Google Workspace.</span><span class="sxs-lookup"><span data-stu-id="2cafc-104">You can use an admin-ran migration to Exchange Online from Google Workspace.</span></span> <span data-ttu-id="2cafc-105">Vous pouvez migrer le courrier en une seule fois ou par étapes.</span><span class="sxs-lookup"><span data-stu-id="2cafc-105">You can migrate the mail either all at once, or in stages.</span></span> <span data-ttu-id="2cafc-106">Les étapes suivantes montrent comment migrer les données de courrier à la fois.</span><span class="sxs-lookup"><span data-stu-id="2cafc-106">The following steps show how to migrate the email data at once.</span></span> <span data-ttu-id="2cafc-107">Pour plus d’informations, [voir Effectuer une migration G Suite.](/exchange/mailbox-migration/perform-g-suite-migration)</span><span class="sxs-lookup"><span data-stu-id="2cafc-107">For more information, see [Perform a G Suite migration](/exchange/mailbox-migration/perform-g-suite-migration).</span></span>

<span data-ttu-id="2cafc-108">Le processus de migration prend plusieurs étapes et peut prendre de plusieurs heures à quelques jours en fonction de la quantité de données que vous migrez.</span><span class="sxs-lookup"><span data-stu-id="2cafc-108">The migration process takes several steps and can take from several hours to a couple of days depending on the amount of data you are migrating.</span></span>

## <a name="try-it"></a><span data-ttu-id="2cafc-109">Essayez !</span><span class="sxs-lookup"><span data-stu-id="2cafc-109">Try it!</span></span>

### <a name="create-a-google-service-account"></a><span data-ttu-id="2cafc-110">Créer un compte de service Google</span><span class="sxs-lookup"><span data-stu-id="2cafc-110">Create a Google Service Account</span></span>

1. <span data-ttu-id="2cafc-111">À l’aide d’un navigateur Chrome, connectez-vous à votre console d’administration Google Workspace [admin.google.com](https://admin.google.com).</span><span class="sxs-lookup"><span data-stu-id="2cafc-111">Using a Chrome browser, sign into your Google Workspace admin console at [admin.google.com](https://admin.google.com).</span></span> 
1. <span data-ttu-id="2cafc-112">Dans un nouvel onglet ou une nouvelle fenêtre, accédez à la page [Comptes de](https://console.developers.google.com/iam-admin/serviceaccounts) service.</span><span class="sxs-lookup"><span data-stu-id="2cafc-112">In a new tab or window, navigate to the [Service Accounts](https://console.developers.google.com/iam-admin/serviceaccounts) page.</span></span> 
1. <span data-ttu-id="2cafc-113">Sélectionnez **Créer un** projet, nommez le projet et choisissez **Créer.**</span><span class="sxs-lookup"><span data-stu-id="2cafc-113">Select **Create project**, name the project and choose **Create**.</span></span> 
1. <span data-ttu-id="2cafc-114">Sélectionnez **Créer un compte de service,** entrez un nom, choisissez **Créer,** puis **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="2cafc-114">Select **Create service account**, enter a name, choose **Create** and then **Done**.</span></span> 
1. <span data-ttu-id="2cafc-115">Ouvrez le menu **Actions,** **sélectionnez Modifier** et prenez note de l’ID unique.</span><span class="sxs-lookup"><span data-stu-id="2cafc-115">Open the **Actions** menu, select **Edit**, and take note of the Unique ID.</span></span> <span data-ttu-id="2cafc-116">Vous aurez besoin de cet ID plus tard dans le processus.</span><span class="sxs-lookup"><span data-stu-id="2cafc-116">You’ll need this ID later in the process.</span></span> 
1. <span data-ttu-id="2cafc-117">Ouvrez la section **Afficher la délégation à l’échelle du** domaine.</span><span class="sxs-lookup"><span data-stu-id="2cafc-117">Open the **Show domain-wide delegation** section.</span></span> 
1. <span data-ttu-id="2cafc-118">Sélectionnez Activer la délégation à l’échelle du domaine **G Suite,** entrez un nom de produit pour l’écran de consentement, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="2cafc-118">Select **Enable G Suite Domain-wide Delegation**, enter a product name for the consent screen, and choose **Save**.</span></span> 

    > [!NOTE]
> <span data-ttu-id="2cafc-119">Le nom du produit n’est pas utilisé par le processus de migration, mais est nécessaire pour l’enregistrer dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="2cafc-119">The product name is not used by the migration process, but is needed to save in the dialog.</span></span>     

1. <span data-ttu-id="2cafc-120">Ouvrez **de nouveau le** menu Actions et **sélectionnez Créer une clé.**</span><span class="sxs-lookup"><span data-stu-id="2cafc-120">Open the **Actions** menu again and select **Create key**.</span></span> 
1. <span data-ttu-id="2cafc-121">Choose **JSON,** then **Create**.</span><span class="sxs-lookup"><span data-stu-id="2cafc-121">Choose **JSON**, then **Create**.</span></span> 

     <span data-ttu-id="2cafc-122">La clé privée est enregistrée dans le dossier de téléchargement de votre appareil.</span><span class="sxs-lookup"><span data-stu-id="2cafc-122">The private key is saved to the download folder on your device.</span></span>
 
1. <span data-ttu-id="2cafc-123">Sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="2cafc-123">Select **Close**.</span></span> 

### <a name="enable-api-usage-for-the-project"></a><span data-ttu-id="2cafc-124">Activer l’utilisation de l’API pour le projet</span><span class="sxs-lookup"><span data-stu-id="2cafc-124">Enable API usage for the project</span></span>

1. <span data-ttu-id="2cafc-125">Accédez à [la page API.](https://console.developers.google.com/apis/library)</span><span class="sxs-lookup"><span data-stu-id="2cafc-125">Navigate to the [APIs page](https://console.developers.google.com/apis/library).</span></span> 
1. <span data-ttu-id="2cafc-126">Dans la barre de recherche, entrez **l’API Gmail.**</span><span class="sxs-lookup"><span data-stu-id="2cafc-126">In the search bar, enter **Gmail API**.</span></span>
1. <span data-ttu-id="2cafc-127">Sélectionnez-le, puis choisissez **Activer.**</span><span class="sxs-lookup"><span data-stu-id="2cafc-127">Select it and then choose **Enable**.</span></span>
1. <span data-ttu-id="2cafc-128">Répétez ce processus pour l’API Calendrier Google et l’API Contacts.</span><span class="sxs-lookup"><span data-stu-id="2cafc-128">Repeat this process for Google Calendar API and Contacts API.</span></span> 

### <a name="grant-access-to-the-service-account"></a><span data-ttu-id="2cafc-129">Accorder l’accès au compte de service</span><span class="sxs-lookup"><span data-stu-id="2cafc-129">Grant access to the service account</span></span>

1. <span data-ttu-id="2cafc-130">Revenir à la console d’administration Google Workspace.</span><span class="sxs-lookup"><span data-stu-id="2cafc-130">Return to the Google Workspace admin console.</span></span> 
1. <span data-ttu-id="2cafc-131">Sélectionnez **Sécurité,** faites défiler vers le bas et ouvrez les **contrôles d’API.**</span><span class="sxs-lookup"><span data-stu-id="2cafc-131">Select **Security**, scroll down and open **API controls**.</span></span> 
1. <span data-ttu-id="2cafc-132">Faites défiler vers le bas et **sélectionnez Gérer la délégation à l’échelle du domaine.**</span><span class="sxs-lookup"><span data-stu-id="2cafc-132">Scroll down and select **Manage Domain-wide Delegation**.</span></span>
1. <span data-ttu-id="2cafc-133">Sélectionnez **Ajouter nouveau** et entrez l’ID client que vous avez pris note précédemment.</span><span class="sxs-lookup"><span data-stu-id="2cafc-133">Select **Add new** and enter the Client ID you made note of earlier.</span></span>
1. <span data-ttu-id="2cafc-134">Entrez ensuite les étendues OAuth pour les API Google.</span><span class="sxs-lookup"><span data-stu-id="2cafc-134">Then enter the OAuth scopes for Google APIs.</span></span> <span data-ttu-id="2cafc-135">Ceux-ci sont disponibles [aka.ms/GoogleWorkspaceMigration](/exchange/mailbox-migration/perform-g-suite-migration#grant-access-to-the-service-account-for-your-google-tenant) l’étape 5 et sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2cafc-135">These are available at [aka.ms/GoogleWorkspaceMigration](/exchange/mailbox-migration/perform-g-suite-migration#grant-access-to-the-service-account-for-your-google-tenant) in step 5 and are:</span></span>

    `https://mail.google.com/,https://www.googleapis.com/auth/calendar,https://www.google.com/m8/feeds/,https://www.googleapis.com/auth/gmail.settings.sharing`
 
1. <span data-ttu-id="2cafc-136">Choose **Authorize**.</span><span class="sxs-lookup"><span data-stu-id="2cafc-136">Choose **Authorize**.</span></span> 

### <a name="create-a-sub-domain-for-mail-going-to-microsoft-365"></a><span data-ttu-id="2cafc-137">Créer un sous-domaine pour le courrier électronique envoyé à Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2cafc-137">Create a sub-domain for mail going to Microsoft 365</span></span>

1. <span data-ttu-id="2cafc-138">Revenir à la console **d’administration Google Workspace.**</span><span class="sxs-lookup"><span data-stu-id="2cafc-138">Return to the **Google Workspace admin** console.</span></span>
1. <span data-ttu-id="2cafc-139">Select **Domains**, **Manage domains**, then, **Add a domain alias**.</span><span class="sxs-lookup"><span data-stu-id="2cafc-139">Select **Domains**, **Manage domains**, then, **Add a domain alias**.</span></span> 
1. <span data-ttu-id="2cafc-140">Entrez un alias de domaine comme `m365.contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="2cafc-140">Enter a domain alias like `m365.contoso.com`.</span></span>
1. <span data-ttu-id="2cafc-141">Ensuite, **sélectionnez Continuer et vérifiez la propriété du domaine.**</span><span class="sxs-lookup"><span data-stu-id="2cafc-141">Then select **Continue and verify domain ownership**.</span></span> 

    <span data-ttu-id="2cafc-142">La vérification de domaine ne prend généralement que quelques minutes, mais elle peut prendre jusqu’à 48 heures.</span><span class="sxs-lookup"><span data-stu-id="2cafc-142">Domain verification usually takes just a few minutes, but it can take up to 48 hours.</span></span>

1. <span data-ttu-id="2cafc-143">Go to the [Microsoft 365 admin center](https://admin.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="2cafc-143">Go to the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>
1. <span data-ttu-id="2cafc-144">Dans le **Centre d’administration Microsoft 365,** dans le navigation de gauche, sélectionnez Afficher **tout,** **Paramètres,** **Domaines,** puis Ajouter **un domaine.**</span><span class="sxs-lookup"><span data-stu-id="2cafc-144">In the **Microsoft 365 admin center**, in the left nav, select **Show all**, **Settings**, **Domains**, and then **Add domain**.</span></span> 
1. <span data-ttu-id="2cafc-145">Entrez le sous-domaine que vous avez créé précédemment, puis **sélectionnez Utiliser ce domaine.**</span><span class="sxs-lookup"><span data-stu-id="2cafc-145">Enter the subdomain you previously created, then select **Use this domain**.</span></span> 
1. <span data-ttu-id="2cafc-146">Pour connecter le domaine, sélectionnez **Continuer.**</span><span class="sxs-lookup"><span data-stu-id="2cafc-146">To connect the domain, select **Continue**.</span></span> 
1. <span data-ttu-id="2cafc-147">Faites défiler vers le bas et prenez note des enregistrements MX, CNAME et TXT.</span><span class="sxs-lookup"><span data-stu-id="2cafc-147">Scroll down and take note of the MX records, CNAME records, and TXT records.</span></span> 
1. <span data-ttu-id="2cafc-148">Revenir à la **console d’administration Google.**</span><span class="sxs-lookup"><span data-stu-id="2cafc-148">Return to the **Google admin console**.</span></span>
1. <span data-ttu-id="2cafc-149">Select **Domains**, select **Manage domains**, **Verify Details** and then, **Manage domain**.</span><span class="sxs-lookup"><span data-stu-id="2cafc-149">Select **Domains**, select **Manage domains**, **Verify Details** and then, **Manage domain**.</span></span> 
1. <span data-ttu-id="2cafc-150">Dans le navigation de gauche, choisissez **DNS et** faites défiler vers le bas **jusqu’aux enregistrements de ressource personnalisés.**</span><span class="sxs-lookup"><span data-stu-id="2cafc-150">In the left nav, choose **DNS** and scroll down to **Custom resource records**.</span></span> 
1. <span data-ttu-id="2cafc-151">Ouvrez la dropdown du type d’enregistrement et sélectionnez **MX,** entrez ou copiez-collez les informations d’enregistrement MX que vous avez précédemment notées, puis choisissez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="2cafc-151">Open the record type dropdown and select **MX**, enter or copy and paste the MX record information you previously noted,then choose **Add**.</span></span> 
1. <span data-ttu-id="2cafc-152">Répétez le processus pour l’enregistrement CNAME et l’enregistrement TXT.</span><span class="sxs-lookup"><span data-stu-id="2cafc-152">Repeat the process for the CNAME record and the TXT record.</span></span> 

    <span data-ttu-id="2cafc-153">L’application de ces modifications peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="2cafc-153">It may take some time for these changes to take effect.</span></span>  

1. <span data-ttu-id="2cafc-154">Revenir à l’endroit où vous vous êtes laissé dans le Centre d’administration **Microsoft 365,** puis sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="2cafc-154">Return to where you left off in **Microsoft 365 admin center**, and select **Continue**.</span></span> 

<span data-ttu-id="2cafc-155">Votre domaine est maintenant installé.</span><span class="sxs-lookup"><span data-stu-id="2cafc-155">Your domain is now set up.</span></span>  

### <a name="create-email-aliases-in-microsoft-365"></a><span data-ttu-id="2cafc-156">Créer des alias de messagerie dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2cafc-156">Create email aliases in Microsoft 365</span></span>

<span data-ttu-id="2cafc-157">Avant de commencer la migration, vous devez créer des alias de messagerie pour vos utilisateurs avec le nouveau sous-domaine.</span><span class="sxs-lookup"><span data-stu-id="2cafc-157">Before migration can begin, you need to create email aliases for your users with the new subdomain.</span></span> 

1. <span data-ttu-id="2cafc-158">Pour commencer l’étape  suivante, dans l’Assistant Ajouter des domaines dans le Centre d’administration Microsoft 365, sélectionnez Go **to Active users**.</span><span class="sxs-lookup"><span data-stu-id="2cafc-158">To start the next step, in the **Add Domains** wizard in the Microsoft 365 admin center, select **Go to Active users**.</span></span> 
1. <span data-ttu-id="2cafc-159">Sélectionnez un utilisateur, puis **gérez le nom d’utilisateur et le courrier électronique.**</span><span class="sxs-lookup"><span data-stu-id="2cafc-159">Select a user, then, **Manage username and email**.</span></span> 
1. <span data-ttu-id="2cafc-160">Dans ladown **Domains (Domaines),** sélectionnez le sous-domaine que vous avez précédemment créé.</span><span class="sxs-lookup"><span data-stu-id="2cafc-160">From the **Domains** dropdown, select the subdomain you previously created.</span></span> 
1. <span data-ttu-id="2cafc-161">Entrez un nom d’utilisateur, **sélectionnez Ajouter,** **Enregistrer les modifications** et fermer la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="2cafc-161">Enter a username, select **Add**, **Save changes**, and close the window.</span></span> 

    <span data-ttu-id="2cafc-162">Répétez ce processus pour chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2cafc-162">Repeat this process for each user.</span></span> 

### <a name="start-the-migration-process"></a><span data-ttu-id="2cafc-163">Démarrer le processus de migration</span><span class="sxs-lookup"><span data-stu-id="2cafc-163">Start the migration process</span></span>

<span data-ttu-id="2cafc-164">Une fois que vous avez terminé, vous êtes prêt à migrer.</span><span class="sxs-lookup"><span data-stu-id="2cafc-164">Once you’ve finished, you’re ready to migrate.</span></span> 

1. <span data-ttu-id="2cafc-165">Dans le navigation gauche du Centre d’administration **Microsoft 365,** faites défiler vers le bas jusqu’aux centres d’administration, puis sélectionnez **Exchange.**</span><span class="sxs-lookup"><span data-stu-id="2cafc-165">In the left nav of the **Microsoft 365 admin center**, scroll down to **Admin centers**,and select **Exchange**.</span></span> 
1. <span data-ttu-id="2cafc-166">Sous **les destinataires**, choisissez **la migration,** sélectionnez **Nouveau**, Migrer vers **Exchange Online,** choisir **la migration G Suite,** puis **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="2cafc-166">Under **recipients**, choose **migration**, select **New**, **Migrate to Exchange Online**, choose **G Suite migration**, and then **Next**.</span></span> 
1. <span data-ttu-id="2cafc-167">Créez un fichier CSV avec une liste des boîtes aux lettres que vous souhaitez migrer.</span><span class="sxs-lookup"><span data-stu-id="2cafc-167">Create a CSV file with a list of the mailboxes you want to migrate.</span></span> <span data-ttu-id="2cafc-168">Assurez-vous que le fichier suit ce format :</span><span class="sxs-lookup"><span data-stu-id="2cafc-168">Make sure the file follows this format:</span></span> 

    ```CSV
    EmailAddress
    will@fabrikaminc.net
    user123@fabrikaminc.net
    ```

      <span data-ttu-id="2cafc-169">Pour plus [d’informations, voir aka.ms/GoogleWorkspaceMigration](/exchange/mailbox-migration/perform-g-suite-migration#start-a-g-suite-migration-batch-with-the-exchange-admin-center-eac).</span><span class="sxs-lookup"><span data-stu-id="2cafc-169">For details see [aka.ms/GoogleWorkspaceMigration](/exchange/mailbox-migration/perform-g-suite-migration#start-a-g-suite-migration-batch-with-the-exchange-admin-center-eac).</span></span> 

1. <span data-ttu-id="2cafc-170">Sélectionnez **Choisir** un fichier, accédez au fichier CSV, choisissez-le, sélectionnez **Ouvrir,** puis **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="2cafc-170">Select **Choose File**, navigate to the CSV file, choose it, select **Open**, then **Next**.</span></span> 
1. <span data-ttu-id="2cafc-171">Vérifiez l’adresse de messagerie de l’administrateur que vous souhaitez utiliser pour le test.</span><span class="sxs-lookup"><span data-stu-id="2cafc-171">Verify the admin email address you want to use for testing.</span></span> 
1. <span data-ttu-id="2cafc-172">Sélectionnez **Choisir** un fichier, accédez au fichier JSON que vous avez créé précédemment (généralement dans le dossier Téléchargements de votre ordinateur), choisissez-le, sélectionnez **Ouvrir,** puis **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="2cafc-172">Select **Choose File**, navigate to the JSON file you created earlier (usually in the Downloads folder on your computer), choose it, select **Open**, then **Next**.</span></span> 
1. <span data-ttu-id="2cafc-173">Entrez un nom dans le **champ Nouveau nom de lot de migration.**</span><span class="sxs-lookup"><span data-stu-id="2cafc-173">Enter a name in the **New migration batch name field**.</span></span>
1. <span data-ttu-id="2cafc-174">Entrez le sous-domaine que vous avez créé dans le champ de domaine de **remise** cible, sélectionnez **Suivant,** puis **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="2cafc-174">Enter the subdomain you created in the **Target delivery domain** field, select **Next**, and then **New**.</span></span> 
1. <span data-ttu-id="2cafc-175">Une fois les informations enregistrées, sélectionnez **OK.**</span><span class="sxs-lookup"><span data-stu-id="2cafc-175">Once the information is saved, select **OK**.</span></span> 

    <span data-ttu-id="2cafc-176">Vous pouvez désormais afficher l’état de votre migration.</span><span class="sxs-lookup"><span data-stu-id="2cafc-176">You can now view the status of your migration.</span></span> 

1. <span data-ttu-id="2cafc-177">Après un certain temps, en fonction du nombre d’utilisateurs que vous migrez, sélectionnez **Actualiser**.</span><span class="sxs-lookup"><span data-stu-id="2cafc-177">After some time has passed, depending on how many users you are migrating, select **Refresh**.</span></span> 
1. <span data-ttu-id="2cafc-178">Une fois que l’état est **devenu Synchronisé,** **sélectionnez Terminer ce lot de migration,** puis **Oui**.</span><span class="sxs-lookup"><span data-stu-id="2cafc-178">Once the status has changed to **Synced**, select **Complete this migration batch**,then **Yes**.</span></span> 
1. <span data-ttu-id="2cafc-179">Une fois le processus terminé, votre statut est **terminé.**</span><span class="sxs-lookup"><span data-stu-id="2cafc-179">Once the process is complete, your status will change to **Completed**.</span></span> 
1. <span data-ttu-id="2cafc-180">Si vous le souhaitez, vous pouvez sélectionner **Afficher les détails** pour plus d’informations sur la migration.</span><span class="sxs-lookup"><span data-stu-id="2cafc-180">If you want, you can select **View details** for more information about the migration.</span></span> 
1. <span data-ttu-id="2cafc-181">Sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="2cafc-181">Select **Close**.</span></span> 
1. <span data-ttu-id="2cafc-182">Ouvrez Outlook pour vérifier que tous les e-mails de Google Workspace ont été correctement migrés.</span><span class="sxs-lookup"><span data-stu-id="2cafc-182">Open Outlook to verify that all the emails from Google Workspace were successfully migrated.</span></span>
<span data-ttu-id="2cafc-183">Vous pouvez également répéter cette situation pour les éléments de calendrier et les contacts.</span><span class="sxs-lookup"><span data-stu-id="2cafc-183">You can repeat this for calendar items and contacts as well.</span></span>