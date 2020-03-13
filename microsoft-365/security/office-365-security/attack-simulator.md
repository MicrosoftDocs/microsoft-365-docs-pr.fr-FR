---
title: Simulateur d’attaque dans Office 365 ATP
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
ms.collection:
- M365-security-compliance
description: Utilisez un simulateur d’attaque pour exécuter des attaques simulant le hameçonnage et les mots de passe dans votre organisation plan 2 Office 365 E5 ou ATP, ce qui peut vous aider à identifier les utilisateurs vulnérables avant qu’une véritable attaque ne touche votre entreprise.
ms.openlocfilehash: 5e924ebe43a6d7fd1af460b304e862207baffb61
ms.sourcegitcommit: 9afcc63b1a7e73f6946f67207337f10b71a5d7f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2020
ms.locfileid: "42612634"
---
# <a name="attack-simulator-in-office-365-atp"></a><span data-ttu-id="cf538-103">Simulateur d’attaque dans Office 365 ATP</span><span class="sxs-lookup"><span data-stu-id="cf538-103">Attack Simulator in Office 365 ATP</span></span>

<span data-ttu-id="cf538-104">Le simulateur d’attaque dans Office 365 Advanced Threat Protection Plan 2 (ATP plan 2) vous permet d’exécuter des campagnes d’hameçonnage et de mot de passe réalistes, mais simulées dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cf538-104">Attack Simulator in Office 365 Advanced Threat Protection Plan 2 (ATP Plan 2) allows you to run realistic, but simulated phishing and password attack campaigns in your organization.</span></span> <span data-ttu-id="cf538-105">Vous pouvez utiliser les résultats des campagnes pour identifier et former les utilisateurs vulnérables.</span><span class="sxs-lookup"><span data-stu-id="cf538-105">You can use the results of campaigns to identify and train vulnerable users.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="cf538-106">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="cf538-106">What do you need to know before you begin?</span></span>

- <span data-ttu-id="cf538-107">Pour ouvrir le centre de sécurité & conformité d’Office 365, <https://protection.office.com/>accédez à.</span><span class="sxs-lookup"><span data-stu-id="cf538-107">To open the Office 365 Security & Compliance Center, go to <https://protection.office.com/>.</span></span> <span data-ttu-id="cf538-108">Le simulateur d’attaque est disponible dans le **simulateur d’attaques** **Threat Management** \> .</span><span class="sxs-lookup"><span data-stu-id="cf538-108">Attack simulator is available at **Threat management** \> **Attack simulator**.</span></span>

  ![Gestion des menaces-simulateur d’attaque](../../media/ThreatMgmt-AttackSimulator.png)

- <span data-ttu-id="cf538-110">Pour plus d’informations sur la disponibilité d’un simulateur d’attaque sur différents abonnements Office 365, consultez la rubrique [Description du service protection avancée contre les menaces d’office 365](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="cf538-110">For more information about the availability of Attack Simulator across different Office 365 subscriptions, see [Office 365 Advanced Threat Protection service description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>

- <span data-ttu-id="cf538-111">Vous devez être membre des groupes de rôles **gestion** de l’organisation ou **administrateur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="cf538-111">You need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span> <span data-ttu-id="cf538-112">Pour plus d’informations sur les groupes de rôles dans le centre de sécurité & conformité, consultez [la rubrique autorisations dans le centre de sécurité & conformité Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="cf538-112">For more information about role groups in the Security & Compliance Center, see [Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="cf538-113">Votre compte doit être configuré pour l’authentification multifacteur (MFA) pour créer et gérer des campagnes dans un simulateur d’attaque.</span><span class="sxs-lookup"><span data-stu-id="cf538-113">Your account needs to be configured for multi-factor authentication (MFA) to create and manage campaigns in Attack Simulator.</span></span> <span data-ttu-id="cf538-114">Pour obtenir des instructions, consultez la rubrique [set up Multi-Factor Authentication](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication).</span><span class="sxs-lookup"><span data-stu-id="cf538-114">For instructions, see [Set up multi-factor authentication](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication).</span></span>

- <span data-ttu-id="cf538-115">Vous pouvez uniquement exécuter des campagnes d’hameçonnage ou d’attaque par mot de passe sur les utilisateurs disposant de boîtes aux lettres dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="cf538-115">You can only run phishing or password attack campaigns on users with mailboxes in Exchange Online.</span></span>

- <span data-ttu-id="cf538-116">Les campagnes de hameçonnage recueillent et traitent les événements pendant 30 jours.</span><span class="sxs-lookup"><span data-stu-id="cf538-116">Phishing campaigns will collect and process events for 30 days.</span></span> <span data-ttu-id="cf538-117">Les données de la campagne historique seront disponibles pendant 90 jours après le lancement de la campagne.</span><span class="sxs-lookup"><span data-stu-id="cf538-117">Historical campaign data will be available for up to 90 days after you launch the campaign.</span></span>

- <span data-ttu-id="cf538-118">Il n’existe pas d’applet de commande PowerShell correspondante pour un simulateur d’attaque.</span><span class="sxs-lookup"><span data-stu-id="cf538-118">There are no corresponding PowerShell cmdlets for Attack Simulator.</span></span>

## <a name="spear-phishing-campaigns"></a><span data-ttu-id="cf538-119">Campagnes de phishing pour le Spear</span><span class="sxs-lookup"><span data-stu-id="cf538-119">Spear phishing campaigns</span></span>

<span data-ttu-id="cf538-120">Le *hameçonnage* est un terme générique pour les attaques par courrier électronique qui tentent de voler des informations sensibles dans les messages semblant provenir d’expéditeurs légitimes ou approuvés.</span><span class="sxs-lookup"><span data-stu-id="cf538-120">*Phishing* is a generic term for email attacks that try to steal sensitive information in messages that appear to be from legitimate or trusted senders.</span></span> <span data-ttu-id="cf538-121">Le *Spear Phishing* est une attaque de hameçonnage ciblée qui utilise un contenu très ciblé et personnalisé qui est spécifiquement adapté aux destinataires ciblés (en général, après la reconnaissance des destinataires par l’agresseur).</span><span class="sxs-lookup"><span data-stu-id="cf538-121">*Spear phishing* is a targeted phishing attack that uses very focused and customized content that's specifically tailored to the targeted recipients (typically, after reconnaissance on the recipients by the attacker).</span></span>

<span data-ttu-id="cf538-122">Pour plus d’informations sur le hameçonnage et le Spear Phishing, consultez la rubrique [hameçonnage](https://docs.microsoft.com/windows/security/threat-protection/intelligence/phishing).</span><span class="sxs-lookup"><span data-stu-id="cf538-122">For more information about phishing and spear phishing, see [Phishing](https://docs.microsoft.com/windows/security/threat-protection/intelligence/phishing).</span></span>

<span data-ttu-id="cf538-123">Dans un simulateur d’attaque, deux types différents de campagnes de Spear Phishing sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="cf538-123">In Attack Simulator, two different types of spear phishing campaigns are available:</span></span>

- <span data-ttu-id="cf538-124">**Spear Phishing (informations d’identification)**: l’attaque tente de convaincre les destinataires de cliquer sur une URL dans le message.</span><span class="sxs-lookup"><span data-stu-id="cf538-124">**Spear phishing (credentials harvest)**: The attack tries to convince the recipients to click a URL in the message.</span></span> <span data-ttu-id="cf538-125">S’ils cliquent sur le lien, les utilisateurs sont invités à entrer leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="cf538-125">If they click the link, users are asked to enter their credentials.</span></span> <span data-ttu-id="cf538-126">Si c’est le cas, ils sont dirigés vers l’un des emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="cf538-126">If they do, they're taken to one of the following locations:</span></span>

  - <span data-ttu-id="cf538-127">Page par défaut qui explique qu’il s’agissait d’un simple test et fournit des conseils pour la reconnaissance des messages de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="cf538-127">A default page that explains this was a just a test, and gives tips for recognizing phishing messages.</span></span>

    ![Ce que les utilisateurs voient s’ils cliquent sur le lien d’hameçonnage et entrent leurs informations d’identification](../../media/attack-simulator-phishing-result.png)

  - <span data-ttu-id="cf538-129">Une page personnalisée (URL) que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="cf538-129">A custom page (URL) that you specify.</span></span>

- <span data-ttu-id="cf538-130">**Spear Phishing (pièce jointe)**: l’attaque tente de convaincre les destinataires d’ouvrir une pièce jointe. docx ou. pdf dans le message.</span><span class="sxs-lookup"><span data-stu-id="cf538-130">**Spear phishing (attachment)**: The attack tries to convince the recipients to open a .docx or .pdf attachment in the message.</span></span> <span data-ttu-id="cf538-131">La pièce jointe contient le même contenu que le lien de hameçonnage par défaut, mais la première phrase\<commence par\>« nom complet, vous voyez ce message en tant que message électronique récent que vous avez ouvert... ».</span><span class="sxs-lookup"><span data-stu-id="cf538-131">The attachment contains the same content from the default phishing link, but the first sentence starts with "\<Display Name\>, you are seeing this message as a recent email message you opened...".</span></span>

> [!NOTE]
> <span data-ttu-id="cf538-132">Actuellement, les campagnes de phishing de Spear dans un simulateur d’attaque n’expirent pas.</span><span class="sxs-lookup"><span data-stu-id="cf538-132">Currently, spear phishing campaigns in Attack Simulator don't expire.</span></span>

### <a name="create-a-spear-phishing-campaign"></a><span data-ttu-id="cf538-133">Créer une campagne de phishing pour le Spear</span><span class="sxs-lookup"><span data-stu-id="cf538-133">Create a spear phishing campaign</span></span>

<span data-ttu-id="cf538-134">Une partie importante de toute campagne de hameçonnage est l’apparence du message électronique envoyé aux destinataires ciblés.</span><span class="sxs-lookup"><span data-stu-id="cf538-134">An important part of any spear phishing campaign is the look and feel of the email message that's sent to the targeted recipients.</span></span> <span data-ttu-id="cf538-135">Pour créer et configurer le message électronique, vous disposez des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="cf538-135">To create and configure the email message, you have these options:</span></span>

- <span data-ttu-id="cf538-136">**Utilisez un modèle de courrier intégré**: les deux modèles prédéfinis sont disponibles : **prix des cadeaux** et **mise à jour**de la paie.</span><span class="sxs-lookup"><span data-stu-id="cf538-136">**Use a built-in email template**: Two built-in templates are available: **Prize Giveaway** and **Payroll Update**.</span></span> <span data-ttu-id="cf538-137">Vous pouvez personnaliser davantage certaines, toutes ou aucune des propriétés de messagerie à partir du modèle lors de la création et du lancement de la campagne.</span><span class="sxs-lookup"><span data-stu-id="cf538-137">You can further customize some, all, or none of the email properties from the template when you create and launch the campaign.</span></span>

- <span data-ttu-id="cf538-138">**Créer un modèle de courrier réutilisable**: après avoir créé et enregistré le modèle de courrier, vous pouvez le réutiliser dans les futures campagnes de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="cf538-138">**Create a reusable email template**: After you create and save the email template, you can use it again in future spear phishing campaigns.</span></span> <span data-ttu-id="cf538-139">Vous pouvez personnaliser davantage certaines, toutes ou aucune des propriétés de messagerie à partir du modèle lors de la création et du lancement de la campagne.</span><span class="sxs-lookup"><span data-stu-id="cf538-139">You can further customize some, all, or none of the email properties from the template when you create and launch the campaign.</span></span>

- <span data-ttu-id="cf538-140">**Créer le message électronique dans l’Assistant**: vous pouvez créer le message électronique directement dans l’Assistant lors de la création et du lancement de la campagne de hameçonnage du Spear.</span><span class="sxs-lookup"><span data-stu-id="cf538-140">**Create the email message in the wizard**: You can create the email message directly in the wizard as you create and launch the spear phishing campaign.</span></span>

#### <a name="step-1-optional-create-a-custom-email-template"></a><span data-ttu-id="cf538-141">Étape 1 (facultatif) : créer un modèle de courrier électronique personnalisé</span><span class="sxs-lookup"><span data-stu-id="cf538-141">Step 1 (Optional): Create a custom email template</span></span>

<span data-ttu-id="cf538-142">Si vous envisagez d’utiliser l’un des modèles intégrés ou de créer le message électronique directement dans l’Assistant, vous pouvez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="cf538-142">If you're going to use one of the built-in templates or create the email message directly in the wizard, you can skip this step.</span></span>

1. <span data-ttu-id="cf538-143">Dans le centre de sécurité & conformité, accédez à **Threat Management** \> **Attack Simulator**.</span><span class="sxs-lookup"><span data-stu-id="cf538-143">In the Security & Compliance Center, go to **Threat management** \> **Attack simulator**.</span></span>

2. <span data-ttu-id="cf538-144">Sur la page **simuler les attaques** , dans les sections **Spear Phishing (Credentials Harvest)** ou **Spear Phishing (pièce jointe)** , cliquez sur informations sur les **attaques**.</span><span class="sxs-lookup"><span data-stu-id="cf538-144">On the **Simulate attacks** page, in either the **Spear Phishing (Credentials Harvest)** or **Spear Phishing (Attachment)** sections, click **Attack Details**.</span></span>

   <span data-ttu-id="cf538-145">La création du modèle n’a pas d’importance.</span><span class="sxs-lookup"><span data-stu-id="cf538-145">It doesn't matter where you create the template.</span></span> <span data-ttu-id="cf538-146">Les options disponibles dans le modèle sont les mêmes pour les deux types d’attaques par hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="cf538-146">The available options in the template are the same for both types of phishing attacks.</span></span>

3. <span data-ttu-id="cf538-147">Dans la page **Détails** de l’attaque qui s’ouvre, dans la section **modèles d’hameçonnage** , dans la zone créer des **modèles** , cliquez sur **nouveau modèle**.</span><span class="sxs-lookup"><span data-stu-id="cf538-147">In the **Attack details** page that opens, in the **Phishing Templates** section, in the **Create Templates** area, click **New Template**.</span></span>

4. <span data-ttu-id="cf538-148">L’Assistant **configurer le modèle d’hameçonnage** démarre dans une nouvelle fenêtre mobile.</span><span class="sxs-lookup"><span data-stu-id="cf538-148">The **Configure Phishing Template** wizard starts in a new flyout.</span></span> <span data-ttu-id="cf538-149">À l’étape de **démarrage** , entrez un nom complet unique pour le modèle, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf538-149">In the **Start** step, enter a unique display name for the template, and then click **Next**.</span></span>

5. <span data-ttu-id="cf538-150">Dans l’étape **configurer les détails du courrier** , configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="cf538-150">In the **Configure email details** step, configure the following settings:</span></span>

   - <span data-ttu-id="cf538-151">**From (Name)**: nom complet utilisé pour l’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="cf538-151">**From (Name)**: The display name that's used for the message sender.</span></span>

   - <span data-ttu-id="cf538-152">**De (courrier électronique)**: adresse de messagerie de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="cf538-152">**From (Email)**: The sender's email address.</span></span>

   - <span data-ttu-id="cf538-153">**URL du serveur de connexion d’hameçonnage**: cliquez sur le menu déroulant et sélectionnez l’une des URL disponibles dans la liste.</span><span class="sxs-lookup"><span data-stu-id="cf538-153">**Phishing Login Server URL**: Click the drop down and select one of the available URLs from the list.</span></span> <span data-ttu-id="cf538-154">Il s’agit de l’URL sur laquelle les utilisateurs seront tentés de cliquer.</span><span class="sxs-lookup"><span data-stu-id="cf538-154">This is the URL that users will be tempted to click.</span></span> <span data-ttu-id="cf538-155">Les possibilités suivantes s'offrent à vous :</span><span class="sxs-lookup"><span data-stu-id="cf538-155">The choices are:</span></span>

     - <http://portal.docdeliveryapp.com>
     - <http://portal.docdeliveryapp.net>
     - <http://portal.docstoreinternal.com>
     - <http://portal.docstoreinternal.net>
     - <http://portal.hardwarecheck.net>
     - <http://portal.hrsupportint.com>
     - <http://portal.payrolltooling.com>
     - <http://portal.payrolltooling.net>
     - <http://portal.prizegiveaway.net>
     - <http://portal.prizesforall.com>
     - <http://portal.salarytoolint.com>
     - <http://portal.salarytoolint.net>

     > [!NOTE]
     > <ul><li><span data-ttu-id="cf538-156">Toutes les URL sont intentionnellement http, et non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cf538-156">All of the URLs are intentionally http, not https.</span></span></li><li><span data-ttu-id="cf538-157">Un service de réputation d’URL peut identifier une ou plusieurs de ces URL comme non sécurisées.</span><span class="sxs-lookup"><span data-stu-id="cf538-157">A URL reputation service might identify one or more of these URLs as unsafe.</span></span> <span data-ttu-id="cf538-158">Vérifiez la disponibilité de l’URL dans vos navigateurs Web pris en charge avant d’utiliser l’URL d’une campagne de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="cf538-158">Check the availability of the URL in your supported web browsers before you use the URL in a phishing campaign.</span></span></li></ul>

   - <span data-ttu-id="cf538-159">**URL de la page d’accueil personnalisée**: entrez une page d’accueil facultative où les utilisateurs sont pris s’ils cliquent sur le lien d’hameçonnage et entrez leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="cf538-159">**Custom Landing Page URL**: Enter an optional landing page where users are taken if they click the phishing link and enter their credentials.</span></span> <span data-ttu-id="cf538-160">Ce lien remplace la page d’accueil par défaut.</span><span class="sxs-lookup"><span data-stu-id="cf538-160">This link replaces the default landing page.</span></span> <span data-ttu-id="cf538-161">Par exemple, si vous avez une formation interne à la sensibilisation, vous pouvez spécifier cette URL ici.</span><span class="sxs-lookup"><span data-stu-id="cf538-161">For example, if you have internal awareness training, you can specify that URL here.</span></span>

   - <span data-ttu-id="cf538-162">**Catégorie**: actuellement, ce paramètre n’est pas utilisé (tout ce que vous entrez n’est pas pris en compte).</span><span class="sxs-lookup"><span data-stu-id="cf538-162">**Category**: Currently, this setting isn't used (anything you enter is ignored).</span></span>

   - <span data-ttu-id="cf538-163">**Subject**: champ **Subject** du message électronique.</span><span class="sxs-lookup"><span data-stu-id="cf538-163">**Subject**: The **Subject** field of the email message.</span></span>

   <span data-ttu-id="cf538-164">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf538-164">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="cf538-165">Dans l’étape **composer un courrier électronique** , créez le corps du message électronique.</span><span class="sxs-lookup"><span data-stu-id="cf538-165">In the **Compose email** step, create the message body of the email message.</span></span> <span data-ttu-id="cf538-166">Vous pouvez utiliser l’onglet **messagerie** (éditeur HTML enrichi) ou l’onglet **source** (code HTML brut).</span><span class="sxs-lookup"><span data-stu-id="cf538-166">You can use the **Email** tab (a rich HTML editor) or the **Source** tab (raw HTML code).</span></span>

   <span data-ttu-id="cf538-167">La mise en forme HTML peut être simple ou complexe, comme vous en avez besoin.</span><span class="sxs-lookup"><span data-stu-id="cf538-167">The HTML formatting can be as simple or complex as you need it to be.</span></span> <span data-ttu-id="cf538-168">Vous pouvez insérer des images et du texte pour améliorer la convivialité du message dans le client de messagerie du destinataire.</span><span class="sxs-lookup"><span data-stu-id="cf538-168">You can insert images and text to enhance the believability of the message in the recipient's email client.</span></span>

   - <span data-ttu-id="cf538-169">`${username}`insère le nom du destinataire.</span><span class="sxs-lookup"><span data-stu-id="cf538-169">`${username}` inserts the recipient's name.</span></span>

   - <span data-ttu-id="cf538-170">`${loginserverurl}`insère la valeur de l' **URL du serveur de connexion de hameçonnage** à partir de l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="cf538-170">`${loginserverurl}` inserts the **Phishing Login Server URL** value from the previous step.</span></span>

   <span data-ttu-id="cf538-171">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf538-171">When you're finished, click **Next**.</span></span>

7. <span data-ttu-id="cf538-172">Dans l’étape **confirmer** , cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="cf538-172">In the **Confirm** step, click **Finish**.</span></span>

#### <a name="step-2-create-and-launch-the-spear-phishing-campaign"></a><span data-ttu-id="cf538-173">Étape 2 : créer et lancer la campagne de hameçonnage de la sonde</span><span class="sxs-lookup"><span data-stu-id="cf538-173">Step 2: Create and launch the spear phishing campaign</span></span>

1. <span data-ttu-id="cf538-174">Dans le centre de sécurité & conformité, accédez à **Threat Management** \> **Attack Simulator**.</span><span class="sxs-lookup"><span data-stu-id="cf538-174">In the Security & Compliance Center, go to **Threat management** \> **Attack simulator**.</span></span>

2. <span data-ttu-id="cf538-175">Sur la page **simuler des attaques** , effectuez l’une des sélections suivantes en fonction du type de campagne que vous souhaitez créer :</span><span class="sxs-lookup"><span data-stu-id="cf538-175">On the **Simulate attacks** page, make one of the following selections based on the type of campaign you want to create:</span></span>

   - <span data-ttu-id="cf538-176">Dans la section **Spear Phishing (informations d’identification)** , cliquez sur **lancer une attaque** ou **sur attaquer les** **Détails** \> de l’attaque.</span><span class="sxs-lookup"><span data-stu-id="cf538-176">In the **Spear Phishing (Credentials Harvest)** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

   - <span data-ttu-id="cf538-177">Dans la **section Spear Phishing (pièce jointe)** , cliquez sur **lancer une attaque** ou \> sur attaques pour **lancer** **une attaque.**</span><span class="sxs-lookup"><span data-stu-id="cf538-177">In the **Spear Phishing (Attachment)** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

3. <span data-ttu-id="cf538-178">L’Assistant **configurer une attaque de hameçonnage** démarre dans une nouvelle fenêtre mobile.</span><span class="sxs-lookup"><span data-stu-id="cf538-178">The **Configure Phishing Attack** wizard starts in a new flyout.</span></span> <span data-ttu-id="cf538-179">Dans l’étape de **démarrage** , effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="cf538-179">In the **Start** step, do one of the following steps:</span></span>

   - <span data-ttu-id="cf538-180">Dans la zone **nom** , entrez un nom complet unique pour la campagne.</span><span class="sxs-lookup"><span data-stu-id="cf538-180">In the **Name** box, enter a unique display name for the campaign.</span></span> <span data-ttu-id="cf538-181">Ne cliquez pas sur **utiliser le modèle**, car vous allez créer le message électronique plus tard dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="cf538-181">Don't click **Use Template**, because you'll create the email message later in the wizard.</span></span>

   - <span data-ttu-id="cf538-182">Cliquez sur **utiliser le modèle** et sélectionnez un modèle de courrier intégré ou personnalisé.</span><span class="sxs-lookup"><span data-stu-id="cf538-182">Click **Use Template** and select a built-in or custom email template.</span></span> <span data-ttu-id="cf538-183">Une fois que vous avez sélectionné le modèle, la zone **nom** est automatiquement remplie en fonction du modèle, mais vous pouvez modifier le nom.</span><span class="sxs-lookup"><span data-stu-id="cf538-183">After you select the template, the **Name** box is automatically filled based on the template, but you can change the name.</span></span>

   ![Page de démarrage du hameçonnage](../../media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)

   <span data-ttu-id="cf538-185">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf538-185">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="cf538-186">Dans l’étape **destinataires cibles** , effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="cf538-186">In the **Target recipients** step, do one of the following steps:</span></span>

   - <span data-ttu-id="cf538-187">Cliquez sur **carnet d’adresses** pour sélectionner les destinataires (utilisateurs ou groupes) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="cf538-187">Click **Address Book** to select the recipients (users or groups) for the campaign.</span></span> <span data-ttu-id="cf538-188">Chaque destinataire ciblé doit disposer d’une boîte aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="cf538-188">Each targeted recipient must have an Exchange Online mailbox.</span></span> <span data-ttu-id="cf538-189">Si vous cliquez sur **Filtrer** et **appliquer** sans entrer de critère de recherche, tous les destinataires sont renvoyés et ajoutés à la campagne.</span><span class="sxs-lookup"><span data-stu-id="cf538-189">If you click **Filter** and **Apply** without entering a search criteria, all recipients are returned and added to the campaign.</span></span>

   - <span data-ttu-id="cf538-190">Cliquez sur **Importer** , puis sur **importation de fichiers** pour importer un fichier de valeurs séparées par des virgules (CSV) ou séparé par une ligne d’adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="cf538-190">Click **Import** then **File Import** to import a comma-separated value (CSV) or line-separated file of email addresses.</span></span> <span data-ttu-id="cf538-191">Chaque ligne doit contenir l’adresse de messagerie du destinataire.</span><span class="sxs-lookup"><span data-stu-id="cf538-191">Each line must contain the recipient's email address.</span></span>

   <span data-ttu-id="cf538-192">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf538-192">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="cf538-193">Dans l’étape **configurer les détails du courrier** , configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="cf538-193">In the **Configure email details** step, configure the following settings:</span></span>

   <span data-ttu-id="cf538-194">Si vous avez sélectionné un modèle dans l’étape de **démarrage** , la plupart de ces valeurs sont déjà configurées, mais vous pouvez les modifier.</span><span class="sxs-lookup"><span data-stu-id="cf538-194">If you selected a template in the **Start** step, most of these values are already configured, but you can change them.</span></span>

   - <span data-ttu-id="cf538-195">**From (Name)**: nom complet utilisé pour l’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="cf538-195">**From (Name)**: The display name that's used for the message sender.</span></span>

   - <span data-ttu-id="cf538-196">**De (courrier électronique)**: adresse de messagerie de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="cf538-196">**From (Email)**: The sender's email address.</span></span> <span data-ttu-id="cf538-197">Vous pouvez entrer une adresse de messagerie réelle ou fictive à partir du domaine de messagerie de votre organisation, ou vous pouvez entrer une adresse de messagerie externe réelle ou fictive.</span><span class="sxs-lookup"><span data-stu-id="cf538-197">You can enter a real or fake email address from your organization's email domain, or you can enter a real or fake external email address.</span></span> <span data-ttu-id="cf538-198">Une adresse de messagerie d’expéditeur valide de votre organisation est en fait résolue dans le client de messagerie du destinataire.</span><span class="sxs-lookup"><span data-stu-id="cf538-198">A valid sender email address from your organization will actually resolve in the recipient's email client.</span></span>

   - <span data-ttu-id="cf538-199">**URL du serveur de connexion d’hameçonnage**: cliquez sur le menu déroulant et sélectionnez l’une des URL disponibles dans la liste.</span><span class="sxs-lookup"><span data-stu-id="cf538-199">**Phishing Login Server URL**: Click the drop down and select one of the available URLs from the list.</span></span> <span data-ttu-id="cf538-200">Il s’agit de l’URL sur laquelle les utilisateurs seront tentés de cliquer.</span><span class="sxs-lookup"><span data-stu-id="cf538-200">This is the URL that users will be tempted to click.</span></span> <span data-ttu-id="cf538-201">Les possibilités suivantes s'offrent à vous :</span><span class="sxs-lookup"><span data-stu-id="cf538-201">The choices are:</span></span>

     - <http://portal.docdeliveryapp.com>
     - <http://portal.docdeliveryapp.net>
     - <http://portal.docstoreinternal.com>
     - <http://portal.docstoreinternal.net>
     - <http://portal.hardwarecheck.net>
     - <http://portal.hrsupportint.com>
     - <http://portal.payrolltooling.com>
     - <http://portal.payrolltooling.net>
     - <http://portal.prizegiveaway.net>
     - <http://portal.prizesforall.com>
     - <http://portal.salarytoolint.com>
     - <http://portal.salarytoolint.net>

     > [!NOTE]
     > <ul><li><span data-ttu-id="cf538-202">Toutes les URL sont intentionnellement http, et non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cf538-202">All of the URLs are intentionally http, not https.</span></span></li><li><span data-ttu-id="cf538-203">Un service de réputation d’URL peut identifier une ou plusieurs de ces URL comme non sécurisées.</span><span class="sxs-lookup"><span data-stu-id="cf538-203">A URL reputation service might identify one or more of these URLs as unsafe.</span></span> <span data-ttu-id="cf538-204">Vérifiez la disponibilité de l’URL dans vos navigateurs Web pris en charge avant d’utiliser l’URL d’une campagne de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="cf538-204">Check the availability of the URL in your supported web browsers before you use the URL in a phishing campaign.</span></span></li><li><span data-ttu-id="cf538-205">Vous devez sélectionner une URL.</span><span class="sxs-lookup"><span data-stu-id="cf538-205">You are required to select a URL.</span></span> <span data-ttu-id="cf538-206">Pour les campagnes de **hameçonnage (de pièces jointes)** , vous pouvez supprimer le lien du corps du message à l’étape suivante (dans le cas contraire, le message contiendra un lien **et** une pièce jointe).</span><span class="sxs-lookup"><span data-stu-id="cf538-206">For **Spear Phishing (Attachment)** campaigns, you can remove the link from the body of the message in the next step (otherwise, the message will contain both a link **and** an attachment).</span></span></li></ul>

   - <span data-ttu-id="cf538-207">**Type de pièce jointe**: ce paramètre est disponible uniquement dans les campagnes de **hameçonnage (de pièces jointes)** .</span><span class="sxs-lookup"><span data-stu-id="cf538-207">**Attachment Type**: This setting is only available in **Spear Phishing (Attachment)** campaigns.</span></span> <span data-ttu-id="cf538-208">Cliquez sur le menu déroulant et sélectionnez **. DOCX** ou **. PDF** à partir de la liste.</span><span class="sxs-lookup"><span data-stu-id="cf538-208">Click the drop down and select **.DOCX** or **.PDF** from the list.</span></span>

   - <span data-ttu-id="cf538-209">**Nom de la pièce jointe**: ce paramètre est disponible uniquement dans les campagnes de **hameçonnage (de pièces jointes)** .</span><span class="sxs-lookup"><span data-stu-id="cf538-209">**Attachment Name**: This setting is only available in **Spear Phishing (Attachment)** campaigns.</span></span> <span data-ttu-id="cf538-210">Entrez un nom de fichier pour la pièce jointe. docx ou. pdf.</span><span class="sxs-lookup"><span data-stu-id="cf538-210">Enter a filename for the .docx or .pdf attachment.</span></span>

   - <span data-ttu-id="cf538-211">**URL de la page d’accueil personnalisée**: entrez une page d’accueil facultative où les utilisateurs sont pris s’ils cliquent sur le lien d’hameçonnage et entrez leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="cf538-211">**Custom Landing Page URL**: Enter an optional landing page where users are taken if they click the phishing link and enter their credentials.</span></span> <span data-ttu-id="cf538-212">Ce lien remplace la page d’accueil par défaut.</span><span class="sxs-lookup"><span data-stu-id="cf538-212">This link replaces the default landing page.</span></span> <span data-ttu-id="cf538-213">Par exemple, si vous avez une formation interne à la sensibilisation, vous pouvez spécifier cette URL ici.</span><span class="sxs-lookup"><span data-stu-id="cf538-213">For example, if you have internal awareness training, you can specify that URL here.</span></span>

   - <span data-ttu-id="cf538-214">**Subject**: champ **Subject** du message électronique.</span><span class="sxs-lookup"><span data-stu-id="cf538-214">**Subject**: The **Subject** field of the email message.</span></span>

   <span data-ttu-id="cf538-215">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf538-215">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="cf538-216">Dans l’étape **composer un courrier électronique** , créez le corps du message électronique.</span><span class="sxs-lookup"><span data-stu-id="cf538-216">In the **Compose email** step, create the message body of the email message.</span></span> <span data-ttu-id="cf538-217">Si vous avez sélectionné un modèle dans l’étape de **démarrage** , le corps du message est déjà configuré, mais vous pouvez le personnaliser.</span><span class="sxs-lookup"><span data-stu-id="cf538-217">If you selected a template in the **Start** step, the message body is already configured, but you can customize it.</span></span> <span data-ttu-id="cf538-218">Vous pouvez utiliser l’onglet **messagerie** (éditeur HTML enrichi) ou l’onglet **source** (code HTML brut).</span><span class="sxs-lookup"><span data-stu-id="cf538-218">You can use the **Email** tab (a rich HTML editor) or the **Source** tab (raw HTML code).</span></span>

   <span data-ttu-id="cf538-219">La mise en forme HTML peut être simple ou complexe, comme vous en avez besoin.</span><span class="sxs-lookup"><span data-stu-id="cf538-219">The HTML formatting can be as simple or complex as you need it to be.</span></span> <span data-ttu-id="cf538-220">Vous pouvez insérer des images et du texte pour améliorer la convivialité du message dans le client de messagerie du destinataire.</span><span class="sxs-lookup"><span data-stu-id="cf538-220">You can insert images and text to enhance the believability of the message in the recipient's email client.</span></span>

   - <span data-ttu-id="cf538-221">`${username}`insère le nom du destinataire.</span><span class="sxs-lookup"><span data-stu-id="cf538-221">`${username}` inserts the recipient's name.</span></span>

   - <span data-ttu-id="cf538-222">`${loginserverurl}`insère la valeur de l' **URL du serveur de connexion de hameçonnage** .</span><span class="sxs-lookup"><span data-stu-id="cf538-222">`${loginserverurl}` inserts the **Phishing Login Server URL** value.</span></span>

   <span data-ttu-id="cf538-223">Pour les campagnes de **hameçonnage (de pièces jointes)** , vous devez supprimer le lien du corps du message (dans le cas contraire, le message contient à la fois un lien **et** une pièce jointe, et les clics de liens ne sont pas suivis dans une campagne de pièces jointes).</span><span class="sxs-lookup"><span data-stu-id="cf538-223">For **Spear Phishing (Attachment)** campaigns, you should remove the link from the body of the message (otherwise, the message will contain both a link **and** an attachment, and link clicks aren't tracked in an attachment campaign).</span></span>

   ![Composer le corps du message électronique](../../media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)

   <span data-ttu-id="cf538-225">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf538-225">When you're finished, click **Next**.</span></span>

7. <span data-ttu-id="cf538-226">Dans l’étape **confirmer** , cliquez sur **Terminer** pour lancer la campagne.</span><span class="sxs-lookup"><span data-stu-id="cf538-226">In the **Confirm** step, click **Finish** to launch the campaign.</span></span> <span data-ttu-id="cf538-227">Le message de hameçonnage est remis aux destinataires ciblés.</span><span class="sxs-lookup"><span data-stu-id="cf538-227">The phishing message is delivered to the targeted recipients.</span></span>

## <a name="password-attack-campaigns"></a><span data-ttu-id="cf538-228">Campagnes d’attaque par mot de passe</span><span class="sxs-lookup"><span data-stu-id="cf538-228">Password attack campaigns</span></span>

<span data-ttu-id="cf538-229">Une *attaque par mot de passe* tente de deviner les mots de passe des comptes d’utilisateur d’une organisation, généralement après que l’agresseur a identifié un ou plusieurs comptes d’utilisateurs valides.</span><span class="sxs-lookup"><span data-stu-id="cf538-229">A *password attack* tries to guess passwords for user accounts in an organization, typically after the attacker has identified one or more valid user accounts.</span></span>

<span data-ttu-id="cf538-230">Dans un simulateur d’attaque, deux types différents de campagnes d’attaque de mot de passe sont disponibles pour vous permettre de tester la complexité des mots de passe des utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="cf538-230">In Attack Simulator, two different types of password attack campaigns are available for you to test the complexity of your users' passwords:</span></span>

- <span data-ttu-id="cf538-231">**Mot de passe en force (attaque de dictionnaire)**: une attaque *brutale*\* ou une attaque de *dictionnaire* utilise un fichier dictionnaire volumineux de mots de passe sur un compte d’utilisateur en espérant que l’un d’entre eux fonctionnera (de nombreux mots de passe par rapport à un compte).</span><span class="sxs-lookup"><span data-stu-id="cf538-231">**Brute force password (dictionary attack)**: A *brute force*\* or *dictionary* attack uses a large dictionary file of passwords on a user account with the hope that one of them will work (many passwords against one account).</span></span> <span data-ttu-id="cf538-232">Le verrouillage de mot de passe incorrect permet de dissuader les attaques de mot de passe en force.</span><span class="sxs-lookup"><span data-stu-id="cf538-232">Incorrect password lock-outs help deter brute force password attacks.</span></span>

  <span data-ttu-id="cf538-233">Pour l’attaque de dictionnaire, vous pouvez spécifier un ou plusieurs mots de passe à essayer (entrés manuellement ou dans un fichier téléchargé) et vous pouvez spécifier un ou plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="cf538-233">For the dictionary attack, you can specify one or many passwords to try (manually entered or in an uploaded file), and you can specify one or many users.</span></span>

- <span data-ttu-id="cf538-234">**Attaque par pulvérisation de mot de passe**: une attaque par *pulvérisation de mot de passe* utilise le même mot de passe soigneusement considéré avec une liste de comptes d’utilisateurs (un mot de passe par rapport à de nombreux comptes).</span><span class="sxs-lookup"><span data-stu-id="cf538-234">**Password spray attack**: A *password spray* attack uses the same carefully considered password against a list of user accounts (one password against many accounts).</span></span> <span data-ttu-id="cf538-235">Les attaques par pulvérisation de mot de passe sont plus difficiles à détecter que les attaques de mot de passe en force (la probabilité de réussite augmente lorsqu’un agresseur tente un mot de passe entre des dizaines ou des centaines de comptes sans risque de faire passer le verrouillage incorrect du mot de passe de l’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="cf538-235">Password spray attacks are harder to detect than brute force password attacks (the probability of success increases when an attacker tries one password across dozens or hundreds of accounts without the risk of tripping the user's incorrect password lock-out).</span></span>

  <span data-ttu-id="cf538-236">Pour l’attaque par pulvérisation par mot de passe, vous ne pouvez spécifier qu’un seul mot de passe à essayer et vous pouvez spécifier un ou plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="cf538-236">For the password spray attack, you can only specify one password to try, and you can specify one or many users.</span></span>

> [!NOTE]
> <span data-ttu-id="cf538-237">Les attaques de mot de passe dans le simulateur de test du nom d’utilisateur et du mot de passe des demandes d’authentification de base à un point de terminaison fonctionnent également avec d’autres méthodes d’authentification (AD FS, synchronisation de hachage de mot de passe, direct, PingFederate, etc.).</span><span class="sxs-lookup"><span data-stu-id="cf538-237">The password attacks in Attack Simulator pass username and password Basic auth requests to an endpoint, so they also work with other authentication methods (AD FS, password hash sync, pass-through, PingFederate, etc.).</span></span> <span data-ttu-id="cf538-238">Pour les utilisateurs pour lesquels l’authentification multifacteur (MFA) est activée, même si l’attaque par mot de passe essaie son mot de passe réel, la tentative s’inscrit toujours comme un échec (en d’autres termes, les utilisateurs MFA n’apparaissent jamais dans le nombre de **tentatives réussies** de la campagne).</span><span class="sxs-lookup"><span data-stu-id="cf538-238">For users that have MFA enabled, even if the password attack tries their actual password, the attempt will always register as a failure (in other words, MFA users will never appear in the **Successful attempts** count of the campaign).</span></span> <span data-ttu-id="cf538-239">Il s’agit du résultat attendu.</span><span class="sxs-lookup"><span data-stu-id="cf538-239">This is the expected result.</span></span> <span data-ttu-id="cf538-240">MFA est une méthode principale pour vous protéger contre les attaques par mot de passe.</span><span class="sxs-lookup"><span data-stu-id="cf538-240">MFA is a primary method to help protect against password attacks.</span></span>

### <a name="create-and-launch-a-password-attack-campaign"></a><span data-ttu-id="cf538-241">Créer et lancer une campagne d’attaque par mot de passe</span><span class="sxs-lookup"><span data-stu-id="cf538-241">Create and launch a password attack campaign</span></span>

1. <span data-ttu-id="cf538-242">Dans le centre de sécurité & conformité, accédez à **Threat Management** \> **Attack Simulator**.</span><span class="sxs-lookup"><span data-stu-id="cf538-242">In the Security & Compliance Center, go to **Threat management** \> **Attack simulator**.</span></span>

2. <span data-ttu-id="cf538-243">Sur la page **simuler des attaques** , effectuez l’une des sélections suivantes en fonction du type de campagne que vous souhaitez créer :</span><span class="sxs-lookup"><span data-stu-id="cf538-243">On the **Simulate attacks** page, make one of the following selections based on the type of campaign you want to create:</span></span>

   - <span data-ttu-id="cf538-244">Dans la **section mot de passe en force (attaque de dictionnaire)** , cliquez sur **lancer une attaque** ou sur attaque des **Détails** \> de l' **attaque.**</span><span class="sxs-lookup"><span data-stu-id="cf538-244">In the **Brute Force Password (Dictionary Attack)** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

   - <span data-ttu-id="cf538-245">dans la section **attaque par pulvérisation par mot de passe** , cliquez sur lancer une **attaque** **ou sur** \> attaques pour **lancer**une attaque.</span><span class="sxs-lookup"><span data-stu-id="cf538-245">in the **Password spray attack** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

3. <span data-ttu-id="cf538-246">L’Assistant Configuration d’une **attaque de mot de passe** démarre dans une nouvelle fenêtre mobile.</span><span class="sxs-lookup"><span data-stu-id="cf538-246">The **Configure Password Attack** wizard starts in a new flyout.</span></span> <span data-ttu-id="cf538-247">À l’étape de **démarrage** , entrez un nom complet unique pour la campagne, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf538-247">In the **Start** step, enter a unique display name for the campaign, and then click **Next**.</span></span>

4. <span data-ttu-id="cf538-248">Dans l’étape **utilisateurs cibles** , effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="cf538-248">In the **Target users** step, do one of the following steps:</span></span>

   - <span data-ttu-id="cf538-249">Cliquez sur **carnet d’adresses** pour sélectionner les destinataires (utilisateurs ou groupes) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="cf538-249">Click **Address Book** to select the recipients (users or groups) for the campaign.</span></span> <span data-ttu-id="cf538-250">Chaque destinataire ciblé doit disposer d’une boîte aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="cf538-250">Each targeted recipient must have an Exchange Online mailbox.</span></span> <span data-ttu-id="cf538-251">Si vous cliquez sur **Filtrer** et **appliquer** sans entrer de critère de recherche, tous les destinataires sont renvoyés et ajoutés à la campagne.</span><span class="sxs-lookup"><span data-stu-id="cf538-251">If you click **Filter** and **Apply** without entering a search criteria, all recipients are returned and added to the campaign.</span></span>

   - <span data-ttu-id="cf538-252">Cliquez sur **Importer** , puis sur **importation de fichiers** pour importer un fichier de valeurs séparées par des virgules (CSV) ou séparé par une ligne d’adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="cf538-252">Click **Import** then **File Import** to import a comma-separated value (CSV) or line-separated file of email addresses.</span></span> <span data-ttu-id="cf538-253">Chaque ligne doit contenir l’adresse de messagerie du destinataire.</span><span class="sxs-lookup"><span data-stu-id="cf538-253">Each line must contain the recipient's email address.</span></span>

   <span data-ttu-id="cf538-254">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf538-254">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="cf538-255">Dans l’étape **choisir les paramètres d’attaque** , choisissez ce qu’il faut faire en fonction du type de campagne :</span><span class="sxs-lookup"><span data-stu-id="cf538-255">In the **Choose attack settings** step, choose what to do based on the campaign type:</span></span>

   - <span data-ttu-id="cf538-256">**Mot de passe en force (attaque de dictionnaire)**: effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="cf538-256">**Brute Force Password (Dictionary Attack)**: Do either of the following steps:</span></span>

     - <span data-ttu-id="cf538-257">**Entrez les mots de passe manuellement**: dans la zone **Appuyez sur entrée pour ajouter un mot de passe** , tapez un mot de passe, puis appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="cf538-257">**Enter passwords manually**: In the **Press enter to add a password** box, type a password and then press ENTER.</span></span> <span data-ttu-id="cf538-258">Répétez cette étape autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="cf538-258">Repeat this step as many times as necessary.</span></span>

     - <span data-ttu-id="cf538-259">**Charger les mots de passe à partir d’un fichier de dictionnaire**: cliquez sur **Télécharger** pour importer un fichier texte existant qui contient un mot de passe sur chaque ligne et une dernière ligne vide.</span><span class="sxs-lookup"><span data-stu-id="cf538-259">**Upload passwords from a dictionary file**: Click **Upload** to import an existing text file that contains one password on each line and a blank last line.</span></span> <span data-ttu-id="cf538-260">La taille du fichier texte doit être inférieure ou égale à 10 Mo et ne peut pas contenir plus de 30000 mots de passe.</span><span class="sxs-lookup"><span data-stu-id="cf538-260">The text file must be 10 MB or less in size, and can't contain more than 30000 passwords.</span></span>

   - <span data-ttu-id="cf538-261">**Attaque par pulvérisation de mot de passe**: dans **le champ mot de passe à utiliser dans la zone attaque** , entrez un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="cf538-261">**Password spray attack**: In **The password(s) to use in the attack** box, enter one password.</span></span>

   <span data-ttu-id="cf538-262">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cf538-262">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="cf538-263">Dans l’étape **confirmer** , cliquez sur **Terminer** pour lancer la campagne.</span><span class="sxs-lookup"><span data-stu-id="cf538-263">In the **Confirm** step, click **Finish** to launch the campaign.</span></span> <span data-ttu-id="cf538-264">Les mots de passe que vous avez spécifiés sont testés sur les utilisateurs que vous avez spécifiés.</span><span class="sxs-lookup"><span data-stu-id="cf538-264">The passwords you specified are tried on users you specified.</span></span>

## <a name="view-campaign-results"></a><span data-ttu-id="cf538-265">Afficher les résultats de la campagne</span><span class="sxs-lookup"><span data-stu-id="cf538-265">View campaign results</span></span>

<span data-ttu-id="cf538-266">Une fois que vous avez lancé une campagne, vous pouvez vérifier la progression et les résultats sur la page principale **attaques par simulation** .</span><span class="sxs-lookup"><span data-stu-id="cf538-266">After you launch a campaign, you can check the progress and results on the main **Simulate attacks** page.</span></span>

<span data-ttu-id="cf538-267">Les campagnes actives affichent une barre d’État, une valeur de pourcentage terminé et le nombre de (utilisateurs terminés) de (nombre total d’utilisateurs).</span><span class="sxs-lookup"><span data-stu-id="cf538-267">Active campaigns will show a status bar, a completed percentage value and "(completed users) of (total users)" count.</span></span> <span data-ttu-id="cf538-268">Cliquez sur le bouton **Actualiser** pour mettre à jour la progression de toutes les campagnes actives.</span><span class="sxs-lookup"><span data-stu-id="cf538-268">Clicking the **Refresh** button will update the progress of any active campaigns.</span></span> <span data-ttu-id="cf538-269">Vous pouvez également cliquer sur **Terminer** pour arrêter une campagne active.</span><span class="sxs-lookup"><span data-stu-id="cf538-269">You can also click **Terminate** to stop an active campaign.</span></span>

<span data-ttu-id="cf538-270">Une fois la campagne terminée, l’État devient **attaque terminée**.</span><span class="sxs-lookup"><span data-stu-id="cf538-270">When the campaign is finished, the status changes to **Attack completed**.</span></span> <span data-ttu-id="cf538-271">Vous pouvez afficher les résultats de la campagne en effectuant l’une des actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="cf538-271">You can view the results of the campaign by doing either of the following actions:</span></span>

- <span data-ttu-id="cf538-272">Sur la page principale **attaques de simulation** , cliquez sur Afficher le **rapport** sous le nom de la campagne.</span><span class="sxs-lookup"><span data-stu-id="cf538-272">On the main **Simulate attacks** page, click **View Report** under the name of the campaign.</span></span>

- <span data-ttu-id="cf538-273">Sur la page principale **attaques de simulation** , cliquez sur informations sur les **attaques** dans la section correspondant au type d’attaque.</span><span class="sxs-lookup"><span data-stu-id="cf538-273">On the main **Simulate attacks** page, click **Attack Details** in the section for the type of attack.</span></span> <span data-ttu-id="cf538-274">Sur la page Détails de l' **attaque** qui s’ouvre, sélectionnez la campagne dans la section **historique des attaques** .</span><span class="sxs-lookup"><span data-stu-id="cf538-274">On the **Attack details** page that opens, select the campaign in the **Attack History** section.</span></span>

<span data-ttu-id="cf538-275">L’une des actions précédentes vous permet d’accéder à une page intitulée **informations d’attaque**.</span><span class="sxs-lookup"><span data-stu-id="cf538-275">Either of the previous actions will take you to a page named **Attack details**.</span></span> <span data-ttu-id="cf538-276">Les informations qui sont disponibles sur cette page pour chaque type de campagne sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="cf538-276">The information that's available on this page for each type of campaign is described in the following sections.</span></span>

### <a name="spear-phishing-credentials-harvest-campaign-results"></a><span data-ttu-id="cf538-277">Résultats de la campagne de Spear Phishing (informations d’identification)</span><span class="sxs-lookup"><span data-stu-id="cf538-277">Spear Phishing (Credentials Harvest) campaign results</span></span>

<span data-ttu-id="cf538-278">Les informations suivantes sont disponibles dans la page Détails de l' **attaque** de chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="cf538-278">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="cf538-279">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="cf538-279">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="cf538-280">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="cf538-280">**Total users targeted**</span></span>

- <span data-ttu-id="cf538-281">**Tentatives réussies**: nombre d’utilisateurs ayant cliqué sur le lien **et** entré leurs informations d’identification (*n’importe quel* nom d’utilisateur et mot de passe).</span><span class="sxs-lookup"><span data-stu-id="cf538-281">**Successful attempts**: The number of users who clicked the link **and** entered their credentials (*any* username and password value).</span></span>

- <span data-ttu-id="cf538-282">**Taux de réussite global**: pourcentage calculé en / **nombre total d’utilisateurs ciblés**par des **tentatives réussies**.</span><span class="sxs-lookup"><span data-stu-id="cf538-282">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>

- <span data-ttu-id="cf538-283">Le **plus rapide**est de cliquer sur le lien après avoir lancé la campagne.</span><span class="sxs-lookup"><span data-stu-id="cf538-283">**Fastest Click**: How long it took the first user to click the link after you launched the campaign.</span></span>

- <span data-ttu-id="cf538-284">**Moyenne : cliquez sur**le nombre de fois que tout le monde a pris le temps de cliquer sur le lien, divisé par le nombre d’utilisateurs ayant cliqué sur le lien.</span><span class="sxs-lookup"><span data-stu-id="cf538-284">**Average Click**: The sum of how long it took everyone to click the link divided by the number of users who clicked the link.</span></span>

- <span data-ttu-id="cf538-285">**Cliquez sur taux de réussite**: pourcentage calculé par (nombre d’utilisateurs ayant cliqué sur le lien)/ **nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="cf538-285">**Click Success Rate**: A percentage that's calculated by (number of users who clicked the link) / **Total users targeted**.</span></span>

- <span data-ttu-id="cf538-286">**Informations d’identification les plus rapides**: combien de temps a duré le premier utilisateur pour entrer ses informations d’identification après avoir lancé la campagne.</span><span class="sxs-lookup"><span data-stu-id="cf538-286">**Fastest Credentials**: How long it took the first user to enter their credentials after you launched the campaign.</span></span>

- <span data-ttu-id="cf538-287">**Moyenne des informations d’identification**: somme du temps nécessaire à l’utilisateur pour entrer ses informations d’identification divisée par le nombre d’utilisateurs qui ont entré leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="cf538-287">**Average Credentials**: The sum of how long it took everyone to enter their credentials divided by the number of users who entered their credentials.</span></span>

- <span data-ttu-id="cf538-288">**Taux de réussite des informations d’identification**: pourcentage calculé par (nombre d’utilisateurs qui ont entré leurs informations d’identification)/ **nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="cf538-288">**Credential Success Rate**: A percentage that's calculated by (number of users who entered their credentials) / **Total users targeted**.</span></span>

- <span data-ttu-id="cf538-289">Graphique à barres qui affiche le **lien sur lequel l’utilisateur a cliqué** et les numéros **d’identification fournis** par jour.</span><span class="sxs-lookup"><span data-stu-id="cf538-289">A bar graph that shows the **Link clicked** and **Credential supplied** numbers per day.</span></span>

- <span data-ttu-id="cf538-290">Graphique circulaire qui affiche le **lien sur lequel l’utilisateur a cliqué**, les **informations d’identification fournies**et **aucun** pourcentage de la campagne.</span><span class="sxs-lookup"><span data-stu-id="cf538-290">A circle graph that shows the **Link clicked**, **Credential supplied**, and **None** percentages for the campaign.</span></span>

- <span data-ttu-id="cf538-291">La section **utilisateurs compromis** répertorie les détails des utilisateurs qui ont cliqué sur le lien :</span><span class="sxs-lookup"><span data-stu-id="cf538-291">The **Compromised Users** section lists the details of the users who clicked the link:</span></span>

  - <span data-ttu-id="cf538-292">Adresse de messagerie de l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="cf538-292">The user's email address</span></span>

  - <span data-ttu-id="cf538-293">Date/heure à laquelle l’utilisateur a cliqué sur le lien.</span><span class="sxs-lookup"><span data-stu-id="cf538-293">The date/time when they clicked the link.</span></span>

  - <span data-ttu-id="cf538-294">Adresse IP du client.</span><span class="sxs-lookup"><span data-stu-id="cf538-294">The client IP address.</span></span>

  - <span data-ttu-id="cf538-295">Détails sur la version de l’utilisateur de Windows et du navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="cf538-295">Details about the user's version of Windows and web browser.</span></span>

  <span data-ttu-id="cf538-296">Vous pouvez cliquer sur **Exporter** pour exporter les résultats dans un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="cf538-296">You can click **Export** to export the results to a CSV file.</span></span>

### <a name="spear-phishing-attachment-campaign-results"></a><span data-ttu-id="cf538-297">Résultats de la campagne de hameçonnage (pièce jointe)</span><span class="sxs-lookup"><span data-stu-id="cf538-297">Spear Phishing (Attachment) campaign results</span></span>

<span data-ttu-id="cf538-298">Les informations suivantes sont disponibles dans la page Détails de l' **attaque** de chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="cf538-298">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="cf538-299">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="cf538-299">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="cf538-300">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="cf538-300">**Total users targeted**</span></span>

- <span data-ttu-id="cf538-301">**Tentatives réussies**: nombre d’utilisateurs qui ont ouvert ou téléchargé la pièce jointe et qui l’a ouverte (l’aperçu n’est pas compté).</span><span class="sxs-lookup"><span data-stu-id="cf538-301">**Successful attempts**: The number of users who opened or downloaded and opened the attachment (preview doesn't count).</span></span>

- <span data-ttu-id="cf538-302">**Taux de réussite global**: pourcentage calculé en / **nombre total d’utilisateurs ciblés**par des **tentatives réussies**.</span><span class="sxs-lookup"><span data-stu-id="cf538-302">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>

- <span data-ttu-id="cf538-303">**Durée maximale d’ouverture des pièces jointes**: durée de l’ouverture de la pièce jointe par le premier utilisateur après le lancement de la campagne.</span><span class="sxs-lookup"><span data-stu-id="cf538-303">**Fastest attachment open time**: How long it took the first user to open the attachment after you launched the campaign.</span></span>

- <span data-ttu-id="cf538-304">**Durée moyenne d’ouverture des pièces jointes : durée**totale de l’ouverture de la pièce jointe, divisée par le nombre d’utilisateurs ayant ouvert la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="cf538-304">**Average attachment open time**: The sum of how long it took everyone to open the attachment divided by the number of users who opened the attachment.</span></span>

- <span data-ttu-id="cf538-305">**Taux de réussite d’ouverture des pièces jointes**: pourcentage calculé par (nombre d’utilisateurs ayant ouvert la pièce jointe)/ **nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="cf538-305">**Attachment open success rate**: A percentage that's calculated by (number of users who opened the attachment) / **Total users targeted**.</span></span>

### <a name="brute-force-password-dictionary-attack-campaign-results"></a><span data-ttu-id="cf538-306">Résultats de la campagne de mot de passe en force (attaque de dictionnaire)</span><span class="sxs-lookup"><span data-stu-id="cf538-306">Brute Force Password (Dictionary Attack) campaign results</span></span>

<span data-ttu-id="cf538-307">Les informations suivantes sont disponibles dans la page Détails de l' **attaque** de chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="cf538-307">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="cf538-308">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="cf538-308">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="cf538-309">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="cf538-309">**Total users targeted**</span></span>

- <span data-ttu-id="cf538-310">**Tentatives réussies**: nombre d’utilisateurs pour lesquels l’un des mots de passe spécifiés a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="cf538-310">**Successful attempts**: The number of users who were found to be using one of the specified passwords.</span></span>

- <span data-ttu-id="cf538-311">**Taux de réussite global**: pourcentage calculé en / **nombre total d’utilisateurs ciblés**par des **tentatives réussies**.</span><span class="sxs-lookup"><span data-stu-id="cf538-311">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>

- <span data-ttu-id="cf538-312">La section **utilisateurs compromis** répertorie les adresses de messagerie des utilisateurs concernés.</span><span class="sxs-lookup"><span data-stu-id="cf538-312">The **Compromised Users** section lists the email addresses of the affected users.</span></span> <span data-ttu-id="cf538-313">Vous pouvez cliquer sur **Exporter** pour exporter les résultats dans un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="cf538-313">You can click **Export** to export the results to a CSV file.</span></span>

### <a name="password-spray-attack-campaign-results"></a><span data-ttu-id="cf538-314">Résultats de la campagne d’attaque par pulvérisation</span><span class="sxs-lookup"><span data-stu-id="cf538-314">Password spray attack campaign results</span></span>

<span data-ttu-id="cf538-315">Les informations suivantes sont disponibles dans la page Détails de l' **attaque** de chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="cf538-315">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="cf538-316">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="cf538-316">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="cf538-317">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="cf538-317">**Total users targeted**</span></span>

- <span data-ttu-id="cf538-318">**Tentatives réussies**: nombre d’utilisateurs qui ont été identifiés comme utilisant le mot de passe spécifié.</span><span class="sxs-lookup"><span data-stu-id="cf538-318">**Successful attempts**: The number of users who were found to be using the specified password.</span></span>

- <span data-ttu-id="cf538-319">**Taux de réussite global**: pourcentage calculé en / **nombre total d’utilisateurs ciblés**par des **tentatives réussies**.</span><span class="sxs-lookup"><span data-stu-id="cf538-319">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>
