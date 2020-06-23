---
title: Réponse à un compte de messagerie compromis
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: article
ms.collection:
- o365_security_incident_response
- M365-security-compliance
ms.custom:
- TopSMBIssues
- seo-marvel-apr2020
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
description: Découvrez comment reconnaître un compte de messagerie compromis et y répondre à l’aide des outils disponibles dans Microsoft 365.
ms.openlocfilehash: 8a7bb98432529bfca70764314d251810d3cdb2a4
ms.sourcegitcommit: 973f5449784cb70ce5545bc3cf57bf1ce5209218
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44819484"
---
# <a name="responding-to-a-compromised-email-account"></a><span data-ttu-id="d04a7-103">Réponse à un compte de messagerie compromis</span><span class="sxs-lookup"><span data-stu-id="d04a7-103">Responding to a Compromised Email Account</span></span>

<span data-ttu-id="d04a7-104">**Résumé** Découvrez comment reconnaître et répondre à un compte de messagerie compromis dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d04a7-104">**Summary** Learn how to recognize and respond to a compromised email account in Microsoft 365.</span></span>

## <a name="what-is-a-compromised-email-account-in-microsoft-365"></a><span data-ttu-id="d04a7-105">Qu’est un compte de messagerie compromis dans Microsoft 365 ?</span><span class="sxs-lookup"><span data-stu-id="d04a7-105">What is a Compromised Email Account in Microsoft 365?</span></span>

<span data-ttu-id="d04a7-106">L’accès aux boîtes aux lettres, données et autres services Microsoft 365 est contrôlé en utilisant des informations d’identification, par exemple un nom d’utilisateur et un mot de passe ou code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="d04a7-106">Access to Microsoft 365 mailboxes, data and other services, is controlled through the use of credentials, for example a user name and password or PIN.</span></span> <span data-ttu-id="d04a7-107">Lorsqu’une personne autre que l’utilisateur initial vole ces informations d’identification, les informations d’identification volées sont considérés comme être compromises.</span><span class="sxs-lookup"><span data-stu-id="d04a7-107">When someone other than the intended user steals those credentials, the stolen credentials are considered to be compromised.</span></span> <span data-ttu-id="d04a7-108">Avec ces informations, le pirate peut se connecter en tant qu’utilisateur d’origine et effectuer des actions illicites.</span><span class="sxs-lookup"><span data-stu-id="d04a7-108">With them the attacker can sign in as the original user and perform illicit actions.</span></span>
<span data-ttu-id="d04a7-109">En utilisant les informations d’identification volées, le pirate peut accéder à la boîte aux lettres de l'utilisateur Microsoft 365, aux dossiers SharePoint ou aux fichiers enregistrés dans le OneDrive de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d04a7-109">Using the stolen credentials, the attacker can access the user's Microsoft 365 mailbox, SharePoint folders, or files in the user's OneDrive.</span></span> <span data-ttu-id="d04a7-110">Souvent, les pirate envoient des messages électroniques en tant qu’utilisateur d’origine à des destinataires internes ou externes à l’organisation.</span><span class="sxs-lookup"><span data-stu-id="d04a7-110">One action commonly seen is the attacker sending emails as the original user to recipients both inside and outside of the organization.</span></span> <span data-ttu-id="d04a7-111">Lorsque l’utilisateur malveillant envoie des données par messages électroniques à des destinataires externes, il s’agit « d’exfiltration de données ».</span><span class="sxs-lookup"><span data-stu-id="d04a7-111">When the attacker emails data to external recipients, this is called data exfiltration.</span></span>

## <a name="symptoms-of-a-compromised-microsoft-email-account"></a><span data-ttu-id="d04a7-112">Symptômes d’un compte de messagerie Microsoft Corporation compromis</span><span class="sxs-lookup"><span data-stu-id="d04a7-112">Symptoms of a Compromised Microsoft Email Account</span></span>

<span data-ttu-id="d04a7-113">Les utilisateurs peuvent noter et rapporter des activités inhabituelles dans leur boîte aux lettres Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d04a7-113">Users might notice and report unusual activity in their Microsoft 365 mailboxes.</span></span> <span data-ttu-id="d04a7-114">Voici quelques symptômes courantes :</span><span class="sxs-lookup"><span data-stu-id="d04a7-114">Here are some common symptoms:</span></span>

- <span data-ttu-id="d04a7-115">Des « activités douteuses », comme des courriers électroniques manquants ou supprimées.</span><span class="sxs-lookup"><span data-stu-id="d04a7-115">Suspicious activity, such as missing or deleted emails.</span></span>

- <span data-ttu-id="d04a7-116">D’autres utilisateurs peuvent recevoir des messages électroniques du compte compromis sans que ces courriers correspondant n’apparaissent dans le dossier **Éléments envoyés** de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="d04a7-116">Other users might receive emails from the compromised account without the corresponding email existing in the **Sent Items** folder of the sender.</span></span>

- <span data-ttu-id="d04a7-117">La présence de règles de boîte de réception qui n’ont pas été créées par l’utilisateur initial ou l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="d04a7-117">The presence of inbox rules that weren't created by the intended user or the administrator.</span></span> <span data-ttu-id="d04a7-118">Ces règles peuvent automatiquement transférer des messages électroniques à des adresses inconnues ou les déplacer vers les dossiers **Notes**, **Courrier indésirable**, ou **Abonnements RSS**.</span><span class="sxs-lookup"><span data-stu-id="d04a7-118">These rules may automatically forward emails to unknown addresses or move them to the **Notes**, **Junk Email**, or **RSS Subscriptions** folders.</span></span>

- <span data-ttu-id="d04a7-119">Le nom d’affichage de l’utilisateur peut être modifié dans la liste d’adresses globale.</span><span class="sxs-lookup"><span data-stu-id="d04a7-119">The user's display name might be changed in the Global Address List.</span></span>

- <span data-ttu-id="d04a7-120">La boîte aux lettres de l’utilisateur peut se trouver bloquée et ne peut plus envoyer de messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="d04a7-120">The user's mailbox is blocked from sending email.</span></span>

- <span data-ttu-id="d04a7-121">Les dossiers Éléments envoyés ou Éléments supprimés dans Microsoft Outlook ou Outlook sur le web (anciennement Outlook Web App) contiennent des messages communs aux comptes piratés, comme par exemple « Je suis bloquée à Londres, envoyez-moi de l’argent. »</span><span class="sxs-lookup"><span data-stu-id="d04a7-121">The Sent or Deleted Items folders in Microsoft Outlook or Outlook on the web (formerly known as Outlook Web App) contain common hacked-account messages, such as "I'm stuck in London, send money."</span></span>

- <span data-ttu-id="d04a7-122">Des modifications inhabituelle du profil, telles que le nom, le numéro de téléphone ou le code postal qui ont été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="d04a7-122">Unusual profile changes, such as the name, the telephone number, or the postal code were updated.</span></span>

- <span data-ttu-id="d04a7-123">Des modifications inhabituelle des informations d’identification, comme par exemple plusieurs requêtes de modification du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="d04a7-123">Unusual credential changes, such as multiple password changes are required.</span></span>

- <span data-ttu-id="d04a7-124">La fonctionnalité de transfert du courrier a été ajoutée récemment.</span><span class="sxs-lookup"><span data-stu-id="d04a7-124">Mail forwarding was recently added.</span></span>

- <span data-ttu-id="d04a7-125">Une signature inhabituelle a été récemment ajoutée, par exemple, une signature apocryphe prétendant être une banque ou faisant référence à une ordonnance médicale.</span><span class="sxs-lookup"><span data-stu-id="d04a7-125">An unusual signature was recently added, such as a fake banking signature or a prescription drug signature.</span></span>

<span data-ttu-id="d04a7-126">Si un utilisateur rapporte un des symptômes ci-dessus, vous devez lancer un examen approfondi.</span><span class="sxs-lookup"><span data-stu-id="d04a7-126">If a user reports any of the above symptoms, you should perform further investigation.</span></span> <span data-ttu-id="d04a7-127">Le centre de sécurité et conformité de Microsoft 365 et le portail Azure proposent des outils pour vous aider à investiguer les activités d’un compte d’utilisateur qui semble avoir été compromis.</span><span class="sxs-lookup"><span data-stu-id="d04a7-127">The Microsoft 365 Security & Compliance Center and the Azure Portal offer tools to help you investigate the activity of a user account that you suspect may be compromised.</span></span>

- <span data-ttu-id="d04a7-128">**Journaux d’audit unifiés dans le Centre de sécurité et conformité** : passez en revue toutes les activités du compte suspect en filtrant les résultats pour la plage de dates couvrant depuis immédiatement avant une activité suspecte jusqu’à la date du jour.</span><span class="sxs-lookup"><span data-stu-id="d04a7-128">**Unified Audit Logs in the Security & Compliance Center**: Review all the activities for the suspected account by filtering the results for the date range spanning from immediately before the suspicious activity occurred to the current date.</span></span> <span data-ttu-id="d04a7-129">Ne pas filtrer sur les activités au cours de la recherche.</span><span class="sxs-lookup"><span data-stu-id="d04a7-129">Do not filter on the activities during the search.</span></span>

- <span data-ttu-id="d04a7-130">**Journaux d’audit de l’administrateur dans le Centre d'administration Exchange** : vous pouvez utiliser le Centre d’administration Exchange (EAC) dans Exchange Online pour rechercher et afficher les entrées dans le journal d’audit de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="d04a7-130">**Admin Audit logs in the EAC**: In Exchange Online, you can use the Exchange admin center (EAC) to search for and view entries in the administrator audit log.</span></span> <span data-ttu-id="d04a7-131">Le journal d’audit de l’administrateur enregistre des actions spécifiques, basées sur les cmdlets Exchange Online PowerShell, effectuées par les administrateurs et les utilisateurs disposant de privilèges d’administration.</span><span class="sxs-lookup"><span data-stu-id="d04a7-131">The administrator audit log records specific actions, based on Exchange Online PowerShell cmdlets, performed by administrators and users who have been assigned administrative privileges.</span></span> <span data-ttu-id="d04a7-132">Les entrées du journal d’audit de l’administrateur vous fournissent des informations sur la cmdlet qui a été exécutée, les paramètres utilisés, l’utilisateur qui a exécuté la cmdlet et les objets concernés.</span><span class="sxs-lookup"><span data-stu-id="d04a7-132">Entries in the administrator audit log provide you with information about what cmdlet was run, which parameters were used, who ran the cmdlet, and what objects were affected.</span></span>

- <span data-ttu-id="d04a7-133">**Utilisez les journaux de connexion Azure AD et autres rapports de risque du portail Azure AD** : examinez les valeurs de ces colonnes :</span><span class="sxs-lookup"><span data-stu-id="d04a7-133">**Azure AD Sign-in logs and other risk reports in the Azure AD portal**: Examine the values in these columns:</span></span>

  - <span data-ttu-id="d04a7-134">Examen des adresses IP</span><span class="sxs-lookup"><span data-stu-id="d04a7-134">Review IP address</span></span>

  - <span data-ttu-id="d04a7-135">emplacements de connexion</span><span class="sxs-lookup"><span data-stu-id="d04a7-135">sign-in locations</span></span>

  - <span data-ttu-id="d04a7-136">heure de connexion</span><span class="sxs-lookup"><span data-stu-id="d04a7-136">sign-in times</span></span>

  - <span data-ttu-id="d04a7-137">réussite ou échec des connexions</span><span class="sxs-lookup"><span data-stu-id="d04a7-137">sign-in success or failure</span></span>

## <a name="how-to-secure-and-restore-email-function-to-a-suspected-compromised-microsoft-365-account-and-mailbox"></a><span data-ttu-id="d04a7-138">Comment sécuriser et restaurer la fonction de messagerie pour un compte Microsoft 365 supposé compromis et ses boîtes aux lettres</span><span class="sxs-lookup"><span data-stu-id="d04a7-138">How to secure and restore email function to a suspected compromised Microsoft 365 account and mailbox</span></span>

> [!VIDEO https://videoplayercdn.osi.office.net/hub/?csid=ux-cms-en-us-msoffice&uuid=RE2jvOb&AutoPlayVideo=false]

<span data-ttu-id="d04a7-139">Même après avoir récupéré l’accès à votre compte, l’utilisateur malveillant peut avoir ajouté des portes d’entrée malveillantes (back-door) qui lui permettront de reprendre le contrôle du compte.</span><span class="sxs-lookup"><span data-stu-id="d04a7-139">Even after you've regained access to your account, the attacker may have added back-door entries that enable the attacker to resume control of the account.</span></span>

<span data-ttu-id="d04a7-140">Vous devez effectuer au plus vite toutes les étapes suivantes pour récupérer l’accès à votre compte, pour vous assurer que l’utilisateur malveillant ne reprenne pas le contrôle de votre compte.</span><span class="sxs-lookup"><span data-stu-id="d04a7-140">You must perform all the following steps to regain access to your account the sooner the better to make sure that the hijacker doesn't resume control your account.</span></span> <span data-ttu-id="d04a7-141">Ces étapes permettent de supprimer les portes d’entrée malveillantes que le pirate peut avoir ajouté à votre compte.</span><span class="sxs-lookup"><span data-stu-id="d04a7-141">These steps help you remove any back-door entries that the hijacker may have added to your account.</span></span> <span data-ttu-id="d04a7-142">Une fois ces étapes effectuées, nous vous recommandons d’exécuter une analyse antivirus pour vous assurer que votre ordinateur n’est pas compromis.</span><span class="sxs-lookup"><span data-stu-id="d04a7-142">After you perform these steps, we recommend that you run a virus scan to make sure that your computer isn't compromised.</span></span>

### <a name="step-1-reset-the-users-password"></a><span data-ttu-id="d04a7-143">Étape 1 : Réinitialisez le mot de passe de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d04a7-143">Step 1 Reset the user's password</span></span>

> [!WARNING]
> <span data-ttu-id="d04a7-144">Ne pas envoyer de nouveau mot de passe à l’utilisateur initial par courrier électronique, car l’utilisateur malveillant a toujours accès à la boîte aux lettres à ce stade.</span><span class="sxs-lookup"><span data-stu-id="d04a7-144">Do not send the new password to the intended user through email as the attacker still has access to the mailbox at this point.</span></span>

1. <span data-ttu-id="d04a7-145">Suivez les procédures de réinitialisation du mot de passe Microsoft 365 Apps pour entreprise pour quelqu’un d’autre décrites dans [Réinitialiser les mots de passe Microsoft 365 Apps pour entreprise](https://docs.microsoft.com/microsoft-365/admin/add-users/reset-passwords)</span><span class="sxs-lookup"><span data-stu-id="d04a7-145">Follow the Reset a Microsoft 365 Apps for business password for someone else procedures in [Reset Microsoft 365 Apps for business passwords](https://docs.microsoft.com/microsoft-365/admin/add-users/reset-passwords)</span></span>

<span data-ttu-id="d04a7-146">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="d04a7-146">**Notes**:</span></span>

- <span data-ttu-id="d04a7-147">Assurez-vous que le mot de passe est robuste et qu’il contient des lettres majuscules et minuscules, au moins un chiffre et au moins un caractère spécial.</span><span class="sxs-lookup"><span data-stu-id="d04a7-147">Make sure that the password is strong and that it contains upper and lowercase letters, at least one number, and at least one special character.</span></span>

- <span data-ttu-id="d04a7-148">Ne pas réutiliser un de vos cinq derniers mots de passe.</span><span class="sxs-lookup"><span data-stu-id="d04a7-148">Don't reuse any of your last five passwords.</span></span> <span data-ttu-id="d04a7-149">Même si l’exigence de l’historique de mot de passe vous permet de réutiliser un mot de passe plus récent, vous devez en sélectionner un que l’utilisateur malveillant ne peut pas deviner.</span><span class="sxs-lookup"><span data-stu-id="d04a7-149">Even though the password history requirement lets you reuse a more recent password, you should select something that the attacker can't guess.</span></span>

- <span data-ttu-id="d04a7-150">Si votre identité locale est fédérée avec Microsoft 365, vous devez modifier votre mot de passe local, puis vous devez informer votre administrateur de l’attaque.</span><span class="sxs-lookup"><span data-stu-id="d04a7-150">If your on-premises identity is federated with Microsoft 365, you must change your password on-premises, and then you must notify your administrator of the compromise.</span></span>

> [!TIP]
> <span data-ttu-id="d04a7-151">Nous vous recommandons vivement d’activer l’authentification multifacteur (MFA) pour éviter les compromissions, en particulier pour les comptes avec des privilèges d’administration.</span><span class="sxs-lookup"><span data-stu-id="d04a7-151">We highly recommended that you enable Multi-Factor Authentication (MFA) in order to prevent compromise, especially for accounts with administrative privileges.</span></span>  <span data-ttu-id="d04a7-152">Pour en savoir plus sur l’authentification multifacteur, voir [configurer l’authentification multifacteur] ((https://docs.microsoft.com/microsoft-365/admin/security-and-compliance/set-up-multi-factor-authentication).</span><span class="sxs-lookup"><span data-stu-id="d04a7-152">To learn more about MFA, go to [Set up multi-factor authentication]((https://docs.microsoft.com/microsoft-365/admin/security-and-compliance/set-up-multi-factor-authentication).</span></span>

### <a name="step-2-remove-suspicious-email-forwarding-addresses"></a><span data-ttu-id="d04a7-153">Étape 2 : Supprimer des adresses de transfert de courrier suspectes</span><span class="sxs-lookup"><span data-stu-id="d04a7-153">Step 2 Remove suspicious email forwarding addresses</span></span>

1. <span data-ttu-id="d04a7-154">Ouvrez le **Centre d’administration Microsoft 365 > Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="d04a7-154">Open the **Microsoft 365 admin center > Active Users**.</span></span>

2. <span data-ttu-id="d04a7-155">Recherchez le compte d’utilisateur en question et développez les **paramètres de courrier**.</span><span class="sxs-lookup"><span data-stu-id="d04a7-155">Find the user account in question and expand **Mail Settings**.</span></span>

3. <span data-ttu-id="d04a7-156">Pour **transfert des courriers électroniques**, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="d04a7-156">For **Email forwarding**, click **Edit**.</span></span>

4. <span data-ttu-id="d04a7-157">Supprimer des adresses de transfert suspectes.</span><span class="sxs-lookup"><span data-stu-id="d04a7-157">Remove any suspicious forwarding addresses.</span></span>

### <a name="step-3-disable-any-suspicious-inbox-rules"></a><span data-ttu-id="d04a7-158">Étape 3 : Désactiver toutes règles de boîte de réception suspectes</span><span class="sxs-lookup"><span data-stu-id="d04a7-158">Step 3 Disable any suspicious inbox rules</span></span>

1. <span data-ttu-id="d04a7-159">Ouvrez la boîte aux lettres d’archivage avec Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="d04a7-159">Sign in to the user's mailbox using Outlook on the web.</span></span>

2. <span data-ttu-id="d04a7-160">Cliquez sur l’icône en forme d’engrenage, puis **Courrier**.</span><span class="sxs-lookup"><span data-stu-id="d04a7-160">Click on the gear icon and click **Mail**.</span></span>

3. <span data-ttu-id="d04a7-161">Cliquez sur **Règles de boîte de réception et de rangement** et passer en revue les règles.</span><span class="sxs-lookup"><span data-stu-id="d04a7-161">Click **Inbox and sweep rules** and review the rules.</span></span>

4. <span data-ttu-id="d04a7-162">Désactiver ou supprimer des règles suspectes.</span><span class="sxs-lookup"><span data-stu-id="d04a7-162">Disable or delete suspicious rules.</span></span>

### <a name="step-4-unblock-the-user-from-sending-mail"></a><span data-ttu-id="d04a7-163">Étape 4 : Redonner à l’utilisateur l’autorisation d’envoyer des messages électroniques</span><span class="sxs-lookup"><span data-stu-id="d04a7-163">Step 4 Unblock the user from sending mail</span></span>

<span data-ttu-id="d04a7-164">Si la boîte aux lettres soupçonnée d'avoir été compromise a été utilisée illicitement pour envoyer des pourriels, il est probable que la boîte aux lettres ne peut plus envoyer de messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="d04a7-164">If the suspected compromised mailbox was used illicitly to send spam email, it is likely that the mailbox has been blocked from sending mail.</span></span>

<span data-ttu-id="d04a7-165">Pour débloquer la boîte aux lettres et permettre l’envoi de messages électroniques, suivez les procédures décrites dans [Suppression d’un utilisateur du portail Utilisateurs restreints après l’envoi de courrier indésirable](removing-user-from-restricted-users-portal-after-spam.md).</span><span class="sxs-lookup"><span data-stu-id="d04a7-165">To unblock a mailbox from sending mail, follow the procedures in [Removing a user from the Restricted Users portal after sending spam email](removing-user-from-restricted-users-portal-after-spam.md).</span></span>

### <a name="step-5-optional-block-the-user-account-from-signing-in"></a><span data-ttu-id="d04a7-166">Étape 5 (facultatif) : Empêcher le compte d’utilisateur de se connecter</span><span class="sxs-lookup"><span data-stu-id="d04a7-166">Step 5 Optional: Block the user account from signing-in</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d04a7-167">Vous pouvez bloquer le compte soupçonné d'avoir été compromis et l’empêcher de se connecter jusqu'à ce qu’à votre avis, il est sûr de réactiver l’accès.</span><span class="sxs-lookup"><span data-stu-id="d04a7-167">You can block the suspected compromised account from signing-in until you believe it is safe to re-enable access.</span></span>

1. <span data-ttu-id="d04a7-168">Aller au Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d04a7-168">Go to the Microsoft 365 admin center.</span></span>

2. <span data-ttu-id="d04a7-169">Dans le centre d’administration Microsoft 365, sélectionnez **Utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="d04a7-169">In the Microsoft 365 admin center, select **Users**.</span></span>

3. <span data-ttu-id="d04a7-170">Sélectionnez l'employé que vous voulez bloquer, puis choisissez **Modifier** en regard d'**État de la connexion** dans le volet de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d04a7-170">Select the employee that you want to block, and then choose **Edit** next to **Sign-in status** in the user pane.</span></span>

4. <span data-ttu-id="d04a7-171">Dans le volet **État de la connexion**, choisissez **Connexion bloquée**, puis **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="d04a7-171">On the **Sign-in status** pane, choose **Sign-in blocked** and then **Save**.</span></span>

5. <span data-ttu-id="d04a7-172">Dans le Centre d'administration, dans le volet de navigation en bas à gauche, développez **Centres d'administration**, puis sélectionnez **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="d04a7-172">In the Admin center, in the lower-left navigation pane, expand **Admin Centers** and select **Exchange**.</span></span>

6. <span data-ttu-id="d04a7-173">Dans le Centre d’administration Exchange, accédez à **Destinataires > Boîtes aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="d04a7-173">In the Exchange admin center, navigate to **Recipients > Mailboxes**.</span></span>

7. <span data-ttu-id="d04a7-174">Sélectionnez l'utilisateur. Dans la page des propriétés de l'utilisateur, sous **Périphériques mobiles**, cliquez sur **Désactiver ActiveSync Exchange** et sur **Désactiver OWA pour les appareils**, puis répondez **oui** à chaque fois.</span><span class="sxs-lookup"><span data-stu-id="d04a7-174">Select the user, and on the user properties page, under **Mobile Devices**, click **Disable Exchange ActivcSync** and **Disable OWA for Devices** and answer **yes** to both.</span></span>

8. <span data-ttu-id="d04a7-175">Sous **Connectivité de courrier**, **Désactiver**, puis répondez **oui**.</span><span class="sxs-lookup"><span data-stu-id="d04a7-175">Under **Email Connectivity**, **Disable** and answer **yes**.</span></span>

### <a name="step-6-optional-remove-the-suspected-compromised-account-from-all-administrative-role-groups"></a><span data-ttu-id="d04a7-176">Étape 6 (facultatif) : Supprimer le compte soupçonné d'avoir été compromis de tous les groupes de rôles d’administration</span><span class="sxs-lookup"><span data-stu-id="d04a7-176">Step 6 Optional: Remove the suspected compromised account from all administrative role groups</span></span>

> [!NOTE]
> <span data-ttu-id="d04a7-177">L’appartenance au groupe de rôles d’administration peut être restaurée une fois que le compte a été sécurisé.</span><span class="sxs-lookup"><span data-stu-id="d04a7-177">Administrative role group membership can be restored after the account has been secured.</span></span>

1. <span data-ttu-id="d04a7-178">Connectez-vous au Centre d’administration Microsoft 365 avec votre compte d’administrateur général et ouvrez **Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="d04a7-178">Sign in to the Microsoft 365 admin center with a global administrator account and open **Active Users**.</span></span>

2. <span data-ttu-id="d04a7-179">Trouvez le compte soupçonné d'avoir été compromis et vérifiez manuellement si des rôles d’administration sont attribués au compte.</span><span class="sxs-lookup"><span data-stu-id="d04a7-179">Find the suspected compromised account and manually check to see if there are any administrative roles assigned to the account.</span></span>

3. <span data-ttu-id="d04a7-180">Ouvrir le **Centre de sécurité et conformité**.</span><span class="sxs-lookup"><span data-stu-id="d04a7-180">Open the **Security & Compliance Center**.</span></span>

4. <span data-ttu-id="d04a7-181">Cliquez sur **Autorisations**.</span><span class="sxs-lookup"><span data-stu-id="d04a7-181">Click **Permissions**.</span></span>

5. <span data-ttu-id="d04a7-182">Passer en revue manuellement les groupes de rôles pour déterminer si le compte soupçonné d'avoir été compromis est membre de l’un des groupes.</span><span class="sxs-lookup"><span data-stu-id="d04a7-182">Manually review the role groups to see if the suspected compromised account is a member of any of them.</span></span>  <span data-ttu-id="d04a7-183">Si ce n’est pas le cas et que ce bouton est défini sur :</span><span class="sxs-lookup"><span data-stu-id="d04a7-183">If it is:</span></span>

   <span data-ttu-id="d04a7-184">a.</span><span class="sxs-lookup"><span data-stu-id="d04a7-184">a.</span></span> <span data-ttu-id="d04a7-185">Cliquez sur le groupe de rôles, puis sur **Modifier un groupe de rôles**.</span><span class="sxs-lookup"><span data-stu-id="d04a7-185">Click the role group and click **Edit Role Group**.</span></span>

   <span data-ttu-id="d04a7-186">b.</span><span class="sxs-lookup"><span data-stu-id="d04a7-186">b.</span></span> <span data-ttu-id="d04a7-187">Cliquez sur **Choisir les membres** et **Modifier** pour supprimer l’utilisateur du groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="d04a7-187">Click **Chose Members** and **Edit** to remove the user from the role group.</span></span>

6. <span data-ttu-id="d04a7-188">Ouvrez le **Centre d’administration Exchange**.</span><span class="sxs-lookup"><span data-stu-id="d04a7-188">Open the **Exchange admin center**.</span></span>

7. <span data-ttu-id="d04a7-189">Cliquez sur **Autorisations**.</span><span class="sxs-lookup"><span data-stu-id="d04a7-189">Click **Permissions**.</span></span>

8. <span data-ttu-id="d04a7-190">Passer en revue manuellement les groupes de rôles pour déterminer si le compte soupçonné d'avoir été compromis est membre de l’un des groupes.</span><span class="sxs-lookup"><span data-stu-id="d04a7-190">Manually review the role groups to see if the suspected compromised account is a member of any of them.</span></span> <span data-ttu-id="d04a7-191">Si ce n’est pas le cas et que ce bouton est défini sur :</span><span class="sxs-lookup"><span data-stu-id="d04a7-191">If it is:</span></span>

   <span data-ttu-id="d04a7-192">a.</span><span class="sxs-lookup"><span data-stu-id="d04a7-192">a.</span></span> <span data-ttu-id="d04a7-193">Cliquez sur le groupe de rôles, puis sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="d04a7-193">Click the role group and click **Edit**.</span></span>

   <span data-ttu-id="d04a7-194">b.</span><span class="sxs-lookup"><span data-stu-id="d04a7-194">b.</span></span> <span data-ttu-id="d04a7-195">Utilisez la section **Membres** pour supprimer l’utilisateur du groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="d04a7-195">Use the **members** section to remove the user from the role group.</span></span>

### <a name="step-7-optional-additional-precautionary-steps"></a><span data-ttu-id="d04a7-196">Étape 7 (facultatif) : Mesures de précaution supplémentaires</span><span class="sxs-lookup"><span data-stu-id="d04a7-196">Step 7 Optional: Additional precautionary steps</span></span>

1. <span data-ttu-id="d04a7-197">Vérifiez vos éléments envoyés.</span><span class="sxs-lookup"><span data-stu-id="d04a7-197">Make sure that you verify your sent items.</span></span> <span data-ttu-id="d04a7-198">Vous devriez peut-être informer les membres de votre liste de contacts que votre compte a été compromis.</span><span class="sxs-lookup"><span data-stu-id="d04a7-198">You may have to inform people on your contacts list that your account was compromised.</span></span> <span data-ttu-id="d04a7-199">L’utilisateur malveillant les a peut-être contacté pour demander de l’argent ou tenter d’usurper leur identité, par exemple, a déclaré que vous étiez bloqué dans un pays étranger et que vous aviez besoin d'argent, ou leur a peut-être envoyé un virus pour pirater leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d04a7-199">The attacker may have asked them for money, spoofing, for example, that you were stranded in a different country and needed money, or the attacker may send them a virus to also hijack their computers.</span></span>

2. <span data-ttu-id="d04a7-200">Tout autre service qui utilise ce compte Exchange en tant que compte de courrier en alternative a pu être compromis.</span><span class="sxs-lookup"><span data-stu-id="d04a7-200">Any other service that used this Exchange account as its alternative email account may have been compromised.</span></span> <span data-ttu-id="d04a7-201">Tout d’abord, effectuez ces étapes pour votre abonnement Microsoft 365, puis effectuez ces étapes pour vos autres comptes.</span><span class="sxs-lookup"><span data-stu-id="d04a7-201">First, perform these steps for your Microsoft 365 subscription, and then perform these steps for your other accounts.</span></span>

3. <span data-ttu-id="d04a7-202">Assurez-vous que vos informations de contact, tels que les numéros de téléphone et adresses, sont correctes.</span><span class="sxs-lookup"><span data-stu-id="d04a7-202">Make sure that your contact information, such as telephone numbers and addresses, is correct.</span></span>

## <a name="secure-microsoft-365-like-a-cybersecurity-pro"></a><span data-ttu-id="d04a7-203">Sécuriser Microsoft 365 comme un pro de la cyber-sécurité</span><span class="sxs-lookup"><span data-stu-id="d04a7-203">Secure Microsoft 365 like a cybersecurity pro</span></span>

<span data-ttu-id="d04a7-204">Votre abonnement Microsoft 365 inclut un ensemble puissant de fonctionnalités de sécurité que vous pouvez utiliser pour protéger vos données et vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d04a7-204">Your Microsoft 365 subscription comes with a powerful set of security capabilities that you can use to protect your data and your users.</span></span>  <span data-ttu-id="d04a7-205">Utilisez la [Feuille de route du Centre de sécurité Microsoft 365 : principales priorités pour les 30 premiers jours, 90 premiers jours et au-delà](security-roadmap.md), pour implémenter les meilleures pratiques recommandées par Microsoft pour sécuriser votre client Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d04a7-205">Use the [Microsoft 365 security roadmap - Top priorities for the first 30 days, 90 days, and beyond](security-roadmap.md) to implement Microsoft recommended best practices for securing your Microsoft 365 tenant.</span></span>

- <span data-ttu-id="d04a7-206">Tâches à effectuer lors des 30 premiers jours.</span><span class="sxs-lookup"><span data-stu-id="d04a7-206">Tasks to accomplish in the first 30 days.</span></span>  <span data-ttu-id="d04a7-207">Elle ont un effet immédiat et n’ont qu’un faible impact négatif sur vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d04a7-207">These have immediate affect and are low-impact to your users.</span></span>

- <span data-ttu-id="d04a7-208">Tâches à accomplir dans les 90 premiers jours.</span><span class="sxs-lookup"><span data-stu-id="d04a7-208">Tasks to accomplish in 90 days.</span></span> <span data-ttu-id="d04a7-209">Ces tâches prennent un peu plus de temps à planifier et à implémenter, mais augmentent considérablement votre sécurité.</span><span class="sxs-lookup"><span data-stu-id="d04a7-209">These take a bit more time to plan and implement but greatly improve your security posture.</span></span>

- <span data-ttu-id="d04a7-210">Au-delà de 90 jours.</span><span class="sxs-lookup"><span data-stu-id="d04a7-210">Beyond 90 days.</span></span> <span data-ttu-id="d04a7-211">Ces améliorations sont à mettre en place pendant les 90 premiers jours.</span><span class="sxs-lookup"><span data-stu-id="d04a7-211">These enhancements build in your first 90 days work.</span></span>

## <a name="see-also"></a><span data-ttu-id="d04a7-212">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d04a7-212">See also</span></span>

- [<span data-ttu-id="d04a7-213">Détecter et résoudre les attaques par injections sur les règles d’Outlook et les formulaires personnalisés dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="d04a7-213">Detect and Remediate Outlook Rules and Custom Forms Injections Attacks in Microsoft 365</span></span>](detect-and-remediate-outlook-rules-forms-attack.md)

- [<span data-ttu-id="d04a7-214">Centre de plaintes contre la criminalité sur Internet </span><span class="sxs-lookup"><span data-stu-id="d04a7-214">Internet Crime Complaint Center</span></span>](https://www.ic3.gov/preventiontips.aspx)

- [<span data-ttu-id="d04a7-215">Securities and Exchange Commission (SEC) : fraude à « l’hameçonnage » (phishing)</span><span class="sxs-lookup"><span data-stu-id="d04a7-215">Securities and Exchange Commission - "Phishing" Fraud</span></span>](https://www.sec.gov/investor/pubs/phishing.htm)

- <span data-ttu-id="d04a7-216">Pour signaler un courrier électronique indésirable directement à Microsoft et à votre administrateur [Utiliser le complément Message de Rapport](https://support.microsoft.com/office/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)</span><span class="sxs-lookup"><span data-stu-id="d04a7-216">To report spam email directly to Microsoft and your admin [Use the Report Message add-in](https://support.microsoft.com/office/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)</span></span>
