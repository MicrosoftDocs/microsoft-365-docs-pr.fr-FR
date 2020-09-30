---
title: Piloter Microsoft 365 depuis mon domaine personnalisé
f1.keywords:
- CSH
ms.author: pebaum
author: pebaum
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
ms.collection:
- Adm_O365
ms.custom: ''
search.appverid:
- BCS160
- MET150
- MOE150
description: Découvrez comment piloter la fonctionnalité de messagerie depuis mon domaine personnalisé vers une boîte aux lettres Microsoft 365 à l’aide de deux comptes de test uniquement.
ms.openlocfilehash: 8bb04edc9a7879edc2094f1fed667d5956174ea3
ms.sourcegitcommit: 15be7822220041c25fc52565f1c64d252e442d89
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48295033"
---
# <a name="pilot-microsoft-365-from-my-custom-domain"></a><span data-ttu-id="5d848-103">Piloter Microsoft 365 depuis mon domaine personnalisé</span><span class="sxs-lookup"><span data-stu-id="5d848-103">Pilot Microsoft 365 from my custom domain</span></span>

<span data-ttu-id="5d848-104">Vous pouvez piloter Microsoft 365 avec les conditions et limitations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5d848-104">You can pilot Microsoft 365 with these requirements and limitations:</span></span>

- <span data-ttu-id="5d848-105">Votre fournisseur de messagerie actuel doit fournir le transfert de messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="5d848-105">Your current email provider must provide email forwarding.</span></span>

- <span data-ttu-id="5d848-106">Vous devez gérer vos enregistrements DNS Microsoft 365 auprès de votre fournisseur d’hébergement DNS, plutôt que de laisser Microsoft 365 les gérer pour vous.</span><span class="sxs-lookup"><span data-stu-id="5d848-106">You must manage your Microsoft 365 DNS records at your DNS hosting provider, rather than have Microsoft 365 manage these records for you.</span></span>

    <span data-ttu-id="5d848-107">Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Ajouter des enregistrements DNS pour connecter votre domaine](https://docs.microsoft.com/microsoft-365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider).</span><span class="sxs-lookup"><span data-stu-id="5d848-107">To learn more, see [Add DNS records to connect your domain](https://docs.microsoft.com/microsoft-365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider).</span></span>

- <span data-ttu-id="5d848-108">Les informations de disponibilité des utilisateurs sur l’autre serveur de messagerie ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="5d848-108">Free/busy information for users on the other email server is not available.</span></span>

- <span data-ttu-id="5d848-109">Les administrateurs ne peuvent pas administrer tous les comptes d’utilisateurs depuis un seul emplacement.</span><span class="sxs-lookup"><span data-stu-id="5d848-109">Admins can't administer all user accounts from a single location.</span></span>

- <span data-ttu-id="5d848-110">Les utilisateurs risquent de ne pas pouvoir utiliser le filtrage du courrier indésirable Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5d848-110">Users might not be able to use Microsoft 365 spam filtering.</span></span>

## <a name="set-up-a-microsoft-365-pilot"></a><span data-ttu-id="5d848-111">Configurer un pilote Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="5d848-111">Set up a Microsoft 365 pilot</span></span>

<span data-ttu-id="5d848-112">Pour configurer un pilote Microsoft 365, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="5d848-112">Follow these steps to set up a Microsoft 365 pilot:</span></span>

### <a name="step-1-sign-in-to-the-microsoft-365-admin-center"></a><span data-ttu-id="5d848-113">Étape 1 : connectez-vous au Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="5d848-113">Step 1: Sign in to the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="5d848-114">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) avec votre compte professionnel ou scolaire.</span><span class="sxs-lookup"><span data-stu-id="5d848-114">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) with your work or school account.</span></span>

2. <span data-ttu-id="5d848-115">Dans le volet de navigation gauche, sélectionnez **Paramètres** > **Domaines**.</span><span class="sxs-lookup"><span data-stu-id="5d848-115">Select **Settings** > **Domains** in the left navigation pane.</span></span>

### <a name="step-2-verify-that-you-own-the-domain-you-want-to-use"></a><span data-ttu-id="5d848-116">Étape 2 : vérifiez que vous êtes propriétaire du domaine que vous voulez utiliser</span><span class="sxs-lookup"><span data-stu-id="5d848-116">Step 2: Verify that you own the domain you want to use</span></span>

1. <span data-ttu-id="5d848-117">Dans la page **Domaines**, sélectionnez **Ajouter un domaine**.</span><span class="sxs-lookup"><span data-stu-id="5d848-117">On the **Domains** page, select **Add domain**.</span></span>

2. <span data-ttu-id="5d848-118">Tapez le nom de domaine dans la zone, sélectionnez **Utiliser ce domaine**, puis sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="5d848-118">Type the domain name in the box, select **Use this domain**, and then select **Continue**.</span></span>

3. <span data-ttu-id="5d848-119">Sélectionnez les services que vous souhaitez tester avec votre domaine, tels que la messagerie électronique et la messagerie instantanée.</span><span class="sxs-lookup"><span data-stu-id="5d848-119">Select the services you want to test with your domain, like email and instant messaging.</span></span>

5. <span data-ttu-id="5d848-120">Sur la page **Vérifier** le domaine, suivez les instructions détaillées, puis sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="5d848-120">On the **Verify** domain page, follow the step-by-step instructions, amd then select **Verify**.</span></span>

    <span data-ttu-id="5d848-121">La prise en compte des modifications DNS peut prendre de quelques minutes à 72 heures.</span><span class="sxs-lookup"><span data-stu-id="5d848-121">It takes between a few minutes and 72 hours for DNS changes to take effect.</span></span>

    <span data-ttu-id="5d848-122">Une fois la vérification effectuée avec succès, vous êtes invité à modifier vos enregistrements DNS.</span><span class="sxs-lookup"><span data-stu-id="5d848-122">When verification is successful, you are asked to modify your DNS records.</span></span>

### <a name="step-3-mark-the-domain-as-shared-in-exchange-online"></a><span data-ttu-id="5d848-123">Étape 3 : marquez le domaine comme partagé dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="5d848-123">Step 3: Mark the domain as shared in Exchange Online</span></span>

1. <span data-ttu-id="5d848-124">Dans le centre d’administration Exchange, dans la section **Flux de courrier**, sélectionnez **Domaines acceptés**, puis sélectionnez le domaine que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="5d848-124">In the Exchange admin center, in the **Mail flow** section, select **Accepted domains**, and then select the domain you want to modify.</span></span>

2. <span data-ttu-id="5d848-125">Double-cliquez pour ouvrir la fenêtre, puis sélectionnez **Relais interne**.</span><span class="sxs-lookup"><span data-stu-id="5d848-125">Double-click to open the window, and then select **Internal Relay**.</span></span> 

3. <span data-ttu-id="5d848-126">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="5d848-126">Select **Save**.</span></span>

    <span data-ttu-id="5d848-127">La prise en compte de ce paramètre peut nécessiter quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="5d848-127">This setting might require a few minutes to take effect.</span></span>

### <a name="step-4-unblock-the-existing-email-server-optional"></a><span data-ttu-id="5d848-128">Étape 4 : débloquez éventuellement le serveur de messagerie existant (facultatif)</span><span class="sxs-lookup"><span data-stu-id="5d848-128">Step 4: Unblock the existing email server (optional)</span></span>

<span data-ttu-id="5d848-129">Microsoft 365 utilise Exchange Online Protection (EOP) pour la protection contre le courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="5d848-129">Microsoft 365 uses Exchange Online Protection (EOP) for spam protection.</span></span> <span data-ttu-id="5d848-130">EOP peut bloquer votre serveur de messagerie existant s’il détecte un nombre élevé de courrier indésirable transmis par votre serveur de messagerie actuel.</span><span class="sxs-lookup"><span data-stu-id="5d848-130">EOP might block your existing mail server if it detects a high volume of spam being forwarded by your current mail server.</span></span> <span data-ttu-id="5d848-131">Si vous faites confiance à la protection contre le courrier indésirable pour votre autre fournisseur de messagerie, vous pouvez débloquer le serveur dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5d848-131">If you trust the spam protection for your other email provider, you can unblock the server in Microsoft 365.</span></span>

> [!NOTE]
> <span data-ttu-id="5d848-132">Le déblocage de votre serveur de messagerie existant permet aux courriers indésirables transmis par votre serveur d’origine d’être transmis aux boîtes aux lettres Microsoft 365. Ensuite, vous ne pouvez pas évaluer la façon dont Microsoft 365 bloque le courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="5d848-132">Unblocking your existing email server allows any spam that arrives through your original server to come to the Microsoft 365 mailboxes, and you can’t evaluate how well Microsoft 365 prevents spam.</span></span>

1. <span data-ttu-id="5d848-133">Dans le volet de navigation du centre d’administration Exchange, sélectionnez **Protection**, puis **Filtre de connexion**.</span><span class="sxs-lookup"><span data-stu-id="5d848-133">In the Exchange admin center navigation pane, select **Protection**, and then select **Connection filter**.</span></span>

2. <span data-ttu-id="5d848-134">Dans la **liste d’adresses IP autorisées**, sélectionnez **+**, puis ajoutez l’adresse IP du serveur de messagerie de votre fournisseur de messagerie actuel.</span><span class="sxs-lookup"><span data-stu-id="5d848-134">In the **IP Allow list**, select **+**, and add the mail server IP address for your current email provider.</span></span> 

### <a name="step-5-create-user-accounts-and-set-the-primary-reply-to-address"></a><span data-ttu-id="5d848-135">Étape 5 : créez des comptes d’utilisateurs et définissez l’adresse de réponse principale</span><span class="sxs-lookup"><span data-stu-id="5d848-135">Step 5: Create user accounts and set the primary reply-to address</span></span>

1. <span data-ttu-id="5d848-136">Dans le volet de navigation gauche du Centre d’administration Microsoft 365, sélectionnez **Utilisateurs** > \*\* Utilisateurs actifs\*\*.</span><span class="sxs-lookup"><span data-stu-id="5d848-136">In the Microsoft 365 admin center left navigation, select **Users** > **Active Users**.</span></span>

2. <span data-ttu-id="5d848-137">Créez deux comptes de test en ajoutant deux utilisateurs existants.</span><span class="sxs-lookup"><span data-stu-id="5d848-137">Create two test accounts by adding two existing users.</span></span>

    <span data-ttu-id="5d848-138">Pour chaque compte, sélectionnez **+ Ajouter un utilisateur**, puis renseignez les informations requises, y compris la méthode de mot de passe que vous souhaitez tester.</span><span class="sxs-lookup"><span data-stu-id="5d848-138">For each account, select **+ Add a user**, and fill out the required information, including the password method you want to test.</span></span>

    <span data-ttu-id="5d848-139">Pour vous assurer que les messages électroniques d’un utilisateur restent identiques, le champ **Nom d’utilisateur** doit correspondre à l’adresse de messagerie actuelle de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5d848-139">To ensure a user’s email stays the same, the **User name** field must match the user’s current email address.</span></span>

3. <span data-ttu-id="5d848-140">Sélectionnez la licence appropriée, cliquez sur **Suivant**, puis sur **Terminer l’ajout**.</span><span class="sxs-lookup"><span data-stu-id="5d848-140">Choose the appropriate license, click **Next**, and then click **Finish adding**.</span></span> 

4. <span data-ttu-id="5d848-141">En regard de **Nom d’utilisateur**, sélectionnez votre nom de domaine personnalisé dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="5d848-141">Next to **User name**, select your custom domain name from the drop-down list.</span></span> 

5. <span data-ttu-id="5d848-142">Sélectionnez **Créer** > **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="5d848-142">Select **Create** > **Close**.</span></span>

### <a name="step-6-configure-mail-to-flow-from-microsoft-365-or-office-365-to-email-server"></a><span data-ttu-id="5d848-143">Étape 6 : Configurer la messagerie pour que les messages circulent depuis Microsoft 365 ou Office 365 vers un serveur de messagerie</span><span class="sxs-lookup"><span data-stu-id="5d848-143">Step 6: \*\*Configure mail to flow from Microsoft 365 or Office 365 to Email server</span></span>

<span data-ttu-id="5d848-144">Voici les deux étapes à suivre :</span><span class="sxs-lookup"><span data-stu-id="5d848-144">There are two steps for this:</span></span>

1. <span data-ttu-id="5d848-145">Configurer votre environnement Microsoft 365 ou Office 365.</span><span class="sxs-lookup"><span data-stu-id="5d848-145">Configure your Microsoft 365 or Office 365 environment.</span></span>

2. <span data-ttu-id="5d848-146">Configurer un connecteur depuis Microsoft 365 ou Office 365 vers votre serveur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="5d848-146">Set up a connector from Microsoft 365 or Office 365 to your email server.</span></span>

### <a name="1-configure-your-microsoft-365-or-office-365-environment"></a><span data-ttu-id="5d848-147">1. Configurer votre environnement Microsoft 365 ou Office 365</span><span class="sxs-lookup"><span data-stu-id="5d848-147">1. Configure your Microsoft 365 or Office 365 environment</span></span>

<span data-ttu-id="5d848-148">Assurez-vous que vous avez effectué les opérations suivantes dans Microsoft 365 ou Office 365 :</span><span class="sxs-lookup"><span data-stu-id="5d848-148">Make sure you have completed the following in Microsoft 365 or Office 365:</span></span>

1. <span data-ttu-id="5d848-149">Pour configurer des connecteurs, vous avez besoin d’autorisations attribuées avant de commencer.</span><span class="sxs-lookup"><span data-stu-id="5d848-149">To set up connectors, you need permissions assigned before you can begin.</span></span> <span data-ttu-id="5d848-150">Pour vérifier les autorisations dont vous avez besoin, consultez l’entrée sur les connecteurs Microsoft 365 et Office 365 dans la rubrique [Autorisations de fonctionnalité dans EOP](https://docs.microsoft.com/microsoft-365/security/office-365-security/feature-permissions-in-eop).</span><span class="sxs-lookup"><span data-stu-id="5d848-150">To check what permissions you need, see the Microsoft 365 and Office 365 connectors entry in the [Feature permissions in EOP](https://docs.microsoft.com/microsoft-365/security/office-365-security/feature-permissions-in-eop) topic.</span></span>

2. <span data-ttu-id="5d848-151">Si vous voulez que vos courriers électroniques soient relayés par EOP ou Exchange Online de vos serveurs de messagerie vers Internet, deux solutions sont possibles :</span><span class="sxs-lookup"><span data-stu-id="5d848-151">If you want EOP or Exchange Online to relay email from your email servers to the Internet, either:</span></span>

   - <span data-ttu-id="5d848-152">Vous pouvez utiliser un certificat configuré avec un nom d’objet qui correspond à un domaine accepté dans Microsoft 365 ou Office 365.</span><span class="sxs-lookup"><span data-stu-id="5d848-152">Use a certificate configured with a subject name that matches an accepted domain in Microsoft 365 or Office 365.</span></span> <span data-ttu-id="5d848-153">Nous recommandons que le nom commun ou l’autre nom d’objet de votre certificat corresponde au domaine SMTP principal de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="5d848-153">We recommend that your certificate's common name or subject alternative name matches the primary SMTP domain for your organization.</span></span> <span data-ttu-id="5d848-154">Pour obtenir des détails, voir [Conditions requises pour votre environnement de messagerie locale](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail#prerequisites-for-your-on-premises-email-environment).</span><span class="sxs-lookup"><span data-stu-id="5d848-154">For details, see [Prerequisites for your on-premises email environment](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail#prerequisites-for-your-on-premises-email-environment).</span></span>

   <span data-ttu-id="5d848-155">- OU -</span><span class="sxs-lookup"><span data-stu-id="5d848-155">-OR-</span></span>

   - <span data-ttu-id="5d848-156">Vous pouvez vérifier que tous les domaines et sous-domaines d'expéditeurs de votre organisation sont des domaines acceptés dans Microsoft 365 ou Office 365.</span><span class="sxs-lookup"><span data-stu-id="5d848-156">Make sure that all your organization sender domains and subdomains are configured as accepted domains in Microsoft 365 or Office 365.</span></span>

   <span data-ttu-id="5d848-157">Pour obtenir plus d’informations sur la définition de domaines acceptés, voir [Gestion des domaines acceptés dans Exchange Online](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) et [Activer le flux de messagerie pour les sous-domaines dans Exchange Online](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/enable-mail-flow-for-subdomains). </span><span class="sxs-lookup"><span data-stu-id="5d848-157">For more information about defining accepted domains, see [Manage accepted domains in Exchange Online](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) and [Enable mail flow for subdomains in Exchange Online](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/enable-mail-flow-for-subdomains).</span></span>

3. <span data-ttu-id="5d848-158">Indiquez si vous souhaitez utiliser des règles de flux de courrier (également appelées règles de transport) ou des noms de domaine pour remettre le courrier de Microsoft 365 ou Office 365 vers vos serveurs de courrier.</span><span class="sxs-lookup"><span data-stu-id="5d848-158">Decide whether you want to use mail flow rules (also known as transport rules) or domain names to deliver mail from Microsoft 365 or Office 365 to your email servers.</span></span> <span data-ttu-id="5d848-159">La plupart des entreprises choisit de remettre les messages pour tous les domaines acceptés.</span><span class="sxs-lookup"><span data-stu-id="5d848-159">Most businesses choose to deliver mail for all accepted domains.</span></span> <span data-ttu-id="5d848-160">Pour plus d'informations, consultez la rubrique [Scénario : routage des messages conditionnels dans Exchange Online](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/conditional-mail-routing).</span><span class="sxs-lookup"><span data-stu-id="5d848-160">For more information, see [Scenario: Conditional mail routing in Exchange Online](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/conditional-mail-routing).</span></span>

> [!NOTE]
> <span data-ttu-id="5d848-161">Vous pouvez configurer des règles de flux de courrier, comme décrit dans [Actions de règle de flux de courrier dans Exchange Online](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).</span><span class="sxs-lookup"><span data-stu-id="5d848-161">You can set up mail flow rules as described in [Mail flow rule actions in Exchange Online](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).</span></span> <span data-ttu-id="5d848-162">Par exemple, vous pouvez utiliser des règles de flux de courrier avec des connecteurs si votre courrier électronique est actuellement redirigé via des listes de distribution vers plusieurs sites.</span><span class="sxs-lookup"><span data-stu-id="5d848-162">For example, you might want to use mail flow rules with connectors if your mail is currently directed via distribution lists to multiple sites.</span></span>

### <a name="2-set-up-a-connector-from-microsoft-365-or-office-365-to-your-email-server"></a><span data-ttu-id="5d848-163">2. Configurer un connecteur depuis Microsoft 365 ou Office 365 vers votre serveur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="5d848-163">2. Set up a connector from Microsoft 365 or Office 365 to your email server</span></span>

<span data-ttu-id="5d848-164">Pour créer un connecteur dans Microsoft 365 ou Office 365, cliquez sur **Administrateur**, puis sur **Exchange** pour accéder au Centre d'administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="5d848-164">To create a connector in Microsoft 365 or Office 365, click **Admin**, and then click **Exchange** to go to the Exchange admin center.</span></span> <span data-ttu-id="5d848-165">Cliquez ensuite sur **flux de messagerie**, puis sur **connecteurs**.</span><span class="sxs-lookup"><span data-stu-id="5d848-165">Next, click **mail flow**, and click **connectors**.</span></span>

<span data-ttu-id="5d848-166">Configuration de connecteurs à l’aide de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="5d848-166">Set up connectors using the wizard.</span></span>

<span data-ttu-id="5d848-167">Pour démarrer l’Assistant, cliquez sur le signe plus **+**.</span><span class="sxs-lookup"><span data-stu-id="5d848-167">To start the wizard, click the plus symbol **+**.</span></span> <span data-ttu-id="5d848-168">Dans le premier écran, sélectionnez **De** Office 365 et **À** votre serveur de courrier de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="5d848-168">On the first screen, choose **From** Office 365 and **To** Your Organization Mail server.</span></span>

<span data-ttu-id="5d848-169">Cliquez sur **Suivant**, et suivez les instructions de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="5d848-169">Click **Next**, and follow the instructions in the wizard.</span></span> <span data-ttu-id="5d848-170">Cliquez sur les liens « **Aide** » ou « **En savoir plus** » pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="5d848-170">Click the **Help** or **Learn More** links if you need more information.</span></span> <span data-ttu-id="5d848-171">L’Assistant vous guidera à chaque étape de la configuration.</span><span class="sxs-lookup"><span data-stu-id="5d848-171">The wizard will guide you through setup.</span></span> <span data-ttu-id="5d848-172">À la fin, vérifiez que votre connecteur est validé.</span><span class="sxs-lookup"><span data-stu-id="5d848-172">At the end, make sure your connector validates.</span></span> <span data-ttu-id="5d848-173">Si le connecteur n’est pas validé, double-cliquez sur le message affiché pour obtenir plus d’informations, et consultez la rubrique [Valider des connecteurs](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/validate-connectors) pour obtenir de l’aide afin de résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="5d848-173">If the connector does not validate, double-click the message displayed to get more information, and see [Validate connectors](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/validate-connectors) for help resolving issues.</span></span>



### <a name="step-7-update-dns-records-at-your-dns-hosting-provider"></a><span data-ttu-id="5d848-174">Étape 7 : mettez à jour les enregistrements DNS auprès de votre fournisseur d’hébergement DNS</span><span class="sxs-lookup"><span data-stu-id="5d848-174">Step 7: Update DNS records at your DNS hosting provider</span></span>

<span data-ttu-id="5d848-175">Connectez-vous au site Web de votre fournisseur d’hébergement DNS, puis suivez les instructions de la rubrique [Ajouter des enregistrements DNS pour connecter votre domaine](https://docs.microsoft.com/microsoft-365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider).</span><span class="sxs-lookup"><span data-stu-id="5d848-175">Sign in to your DNS hosting provider's website, and follow the instructions at [Add DNS records to connect your domain](https://docs.microsoft.com/microsoft-365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider).</span></span>

<span data-ttu-id="5d848-176">**Prévoyez les deux exceptions suivantes :**</span><span class="sxs-lookup"><span data-stu-id="5d848-176">**Make the following two exceptions:**</span></span>

- <span data-ttu-id="5d848-177">Ne créez pas d’enregistrement MX et n’en modifiez pas un existant.</span><span class="sxs-lookup"><span data-stu-id="5d848-177">Do not create a new MX record or change your existing MX record.</span></span>

- <span data-ttu-id="5d848-178">Si vous disposez déjà d’un enregistrement SPF (Sender Policy Framework) pour votre fournisseur de messagerie précédent, au lieu de créer un enregistrement SPF (TXT) pour Exchange Online, ajoutez simplement « include:spf.protection.outlook.com » à l’enregistrement TXT actuel.</span><span class="sxs-lookup"><span data-stu-id="5d848-178">If you already have a Sender Policy Framework (SPF) record for your previous email provider, instead of creating a new SPF (TXT) record for Exchange Online, add "include:spf.protection.outlook.com" to the current TXT record.</span></span>

    <span data-ttu-id="5d848-179">Par exemple, « v=spf1 mx include:adatum.com include:spf.protection.outlook.com ~all ».</span><span class="sxs-lookup"><span data-stu-id="5d848-179">For example, "v=spf1 mx include:adatum.com include:spf.protection.outlook.com ~all".</span></span>

    <span data-ttu-id="5d848-180">Si vous ne disposez pas encore d’enregistrement SPF, modifiez celui recommandé par Microsoft 365 pour y inclure le domaine de votre fournisseur de messagerie actuel, puis ajoutez spf.protection.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="5d848-180">If you don't have an SPF record, modify the one recommended by Microsoft 365 to include the domain for your current email provider, and add spf.protection.outlook.com.</span></span> <span data-ttu-id="5d848-181">Cette action autorise les messages sortants provenant des deux systèmes de courrier.</span><span class="sxs-lookup"><span data-stu-id="5d848-181">This authorizes outgoing messages from both email systems.</span></span>

### <a name="step-8-set-up-email-forwarding-at-your-current-provider"></a><span data-ttu-id="5d848-182">Étape 8 : configurez le transfert de messages électroniques sur votre fournisseur actuel</span><span class="sxs-lookup"><span data-stu-id="5d848-182">Step 8: Set up email forwarding at your current provider</span></span>

<span data-ttu-id="5d848-183">Sur votre fournisseur de messagerie actuel, configurez le transfert pour les comptes de messagerie de vos utilisateurs vers votre domaine onmicrosoft.com :</span><span class="sxs-lookup"><span data-stu-id="5d848-183">At your current email provider, set up forwarding for your users email accounts to your onmicrosoft.com domain:</span></span>

- <span data-ttu-id="5d848-184">Transférez une boîte aux lettres d’un utilisateur A vers usera@yourcompany.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="5d848-184">Forward User A mailbox to usera@yourcompany.onmicrosoft.com</span></span>

- <span data-ttu-id="5d848-185">Transférez une boîte aux lettres d’un utilisateur B vers usera@yourcompany.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="5d848-185">Forward User B mailbox to userb@yourcompany.onmicrosoft.com</span></span>

<span data-ttu-id="5d848-186">Une fois cette étape terminée, tous les messages envoyés à usera@yourcompany.com et userb@yourcompany.com sont disponibles dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5d848-186">When you complete this step, all email sent to usera@yourcompany.com and userb@yourcompany.com is available in Microsoft 365.</span></span>

> [!NOTE]
> <span data-ttu-id="5d848-187">Contactez votre fournisseur de messagerie actuel pour connaître les étapes exactes relatives à la configuration du transfert de messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="5d848-187">Contact your current email provider for the exact steps to set up email forwarding.</span></span><br/>
> <span data-ttu-id="5d848-188">Il n’est pas nécessaire de conserver une copie des messages sur le fournisseur de messagerie actuel.</span><span class="sxs-lookup"><span data-stu-id="5d848-188">You don't need to keep a copy of messages at the current email provider.</span></span><br/>
> <span data-ttu-id="5d848-189">La plupart des fournisseurs transfèrent les messages électroniques sans toucher à l’adresse de réponse de l’expéditeur, afin que les réponses parviennent à l’expéditeur d’origine.</span><span class="sxs-lookup"><span data-stu-id="5d848-189">Most providers forward email by leaving the Reply-to address of the sender intact so that replies go to the original sender.</span></span>

### <a name="step-9-test-mail-flow"></a><span data-ttu-id="5d848-190">Étape 9 : testez le flux de courrier</span><span class="sxs-lookup"><span data-stu-id="5d848-190">Step 9: Test mail flow</span></span>

1. <span data-ttu-id="5d848-191">Connectez-vous à Outlook Web App à l’aide des informations d’identification de l’utilisateur A.</span><span class="sxs-lookup"><span data-stu-id="5d848-191">Sign in to Outlook Web App using the credentials for User A.</span></span>

2. <span data-ttu-id="5d848-192">Effectuez ces tests :</span><span class="sxs-lookup"><span data-stu-id="5d848-192">Perform these tests:</span></span>

    - <span data-ttu-id="5d848-193">Testez le courrier électronique local de Microsoft en envoyant un courrier électronique, par exemple, à l’utilisateur B. Le courrier électronique est remis immédiatement.</span><span class="sxs-lookup"><span data-stu-id="5d848-193">Test local Microsoft email by sending an email, for example, to User B. The email is delivered immediately.</span></span> <span data-ttu-id="5d848-194">Dans ce scénario, le message n’est pas acheminé vers la boîte aux lettres de l’utilisateur B sur votre serveur d’origine, car la boîte aux lettres Microsoft 365 est locale.</span><span class="sxs-lookup"><span data-stu-id="5d848-194">In this scenario, the message is not routed to the mailbox for User B on your original server because the Microsoft 365 mailbox is local.</span></span>

    - <span data-ttu-id="5d848-195">Testez le courrier électronique à un utilisateur sur le système de messagerie existant en envoyant un courrier électronique, par exemple, à l’utilisateur C. Le courrier électronique est remis à la boîte aux lettres de l’utilisateur C sur votre serveur de messagerie d’origine.</span><span class="sxs-lookup"><span data-stu-id="5d848-195">Test email to a user on the existing email system by sending an email, for example, to User C. The email is delivered to the mailbox for User C on your original mail server.</span></span>

    - <span data-ttu-id="5d848-196">Vérifiez que le transfert est correctement configuré depuis un compte externe, ou depuis un compte de messagerie d’employé sur le système de messagerie existant.</span><span class="sxs-lookup"><span data-stu-id="5d848-196">Verify that forwarding is set up properly from an outside account, or from an employee email account on the existing email system.</span></span> <span data-ttu-id="5d848-197">Par exemple, depuis le compte de serveur d’origine pour l’utilisateur C ou un compte Hotmail, envoyez un courrier électronique à l’utilisateur A, puis vérifiez qu’il arrive dans la boîte aux lettres Microsoft 365 de l’utilisateur A.</span><span class="sxs-lookup"><span data-stu-id="5d848-197">For example, from the original server account for User C or a Hotmail account, send User A an email and verify that it arrives in the Microsoft 365 mailbox for User A.</span></span>

### <a name="step-10-move-mailbox-contents"></a><span data-ttu-id="5d848-198">Étape 10 : déplacez le contenu de la boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="5d848-198">Step 10: Move mailbox contents</span></span>

<span data-ttu-id="5d848-199">Étant donné que vous déplacez uniquement deux utilisateurs de test, et que l’utilisateur A et l’utilisateur B utilisent Outlook, vous pouvez déplacer le courrier électronique en ouvrant l’ancien fichier .PST dans le nouveau profil Outlook et en copiant les messages, les éléments de calendrier, les contacts, etc.</span><span class="sxs-lookup"><span data-stu-id="5d848-199">Because you are moving only two test users, and User A and User B are both using Outlook, you can move the email by opening the old .PST file in the new Outlook profile and copying the messages, calendar items, contacts, and so on.</span></span> <span data-ttu-id="5d848-200">Si vous souhaitez en savoir plus, veuillez consulter la rubrique [Importer le courrier, les contacts et le calendrier à partir d’un fichier .pst Outlook](https://support.microsoft.com/office/import-email-contacts-and-calendar-from-an-outlook-pst-file-431a8e9a-f99f-4d5f-ae48-ded54b3440ac).</span><span class="sxs-lookup"><span data-stu-id="5d848-200">For more information, see [Import email, contacts, and calendar from an Outlook .pst file](https://support.microsoft.com/office/import-email-contacts-and-calendar-from-an-outlook-pst-file-431a8e9a-f99f-4d5f-ae48-ded54b3440ac).</span></span>

<span data-ttu-id="5d848-201">Une fois que vous les avez importés aux emplacements appropriés dans la boîte aux lettres Microsoft 365, ces éléments sont accessibles à partir de n’importe quel appareil, où que vous soyez.</span><span class="sxs-lookup"><span data-stu-id="5d848-201">After they’re imported to the appropriate locations in the Microsoft 365 mailbox, the items can be accessed from any device, anywhere.</span></span>

<span data-ttu-id="5d848-202">Lorsque d’autres boîtes aux lettres sont concernées, ou si les employés n’utilisent pas Outlook, vous pouvez utiliser les outils de migration disponibles dans le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="5d848-202">When more mailboxes are involved, or if employees are not using Outlook, you can use the migration tools available in the Exchange admin center.</span></span> <span data-ttu-id="5d848-203">Pour commencer, accédez au centre d’administration Exchange, puis suivez les instructions de la rubrique [Migrer du courrier électronique depuis un serveur IMAP vers des boîtes aux lettres Exchange Online](https://docs.microsoft.com/exchange/mailbox-migration/migrating-imap-mailboxes/migrating-imap-mailboxes).</span><span class="sxs-lookup"><span data-stu-id="5d848-203">To get started, go to Exchange admin center, and follow the directions in [Migrate Email from an IMAP Server to Exchange Online Mailboxes](https://docs.microsoft.com/exchange/mailbox-migration/migrating-imap-mailboxes/migrating-imap-mailboxes).</span></span>
