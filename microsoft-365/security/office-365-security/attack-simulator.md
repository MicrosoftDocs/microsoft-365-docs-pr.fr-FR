---
title: Simulateur d’attaques dans ATP
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
description: En tant qu’administrateur général, vous pouvez utiliser un simulateur d’attaques pour exécuter des scénarios d’attaques réalistes au sein de votre organisation. Cela peut vous aider à identifier les utilisateurs vulnérables avant qu’une véritable attaque ne touche votre entreprise.
ms.openlocfilehash: cac09ed48a46531ea2246f9c3ef798649dc73196
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43638571"
---
# <a name="attack-simulator-in-atp"></a><span data-ttu-id="becd0-104">Simulateur d’attaques dans ATP</span><span class="sxs-lookup"><span data-stu-id="becd0-104">Attack Simulator in ATP</span></span>

<span data-ttu-id="becd0-105">**Synthèse** Si vous êtes administrateur général ou administrateur de sécurité et que votre organisation est équipée du plan 2 de Office 365 ATP, qui inclut [l’examen des menaces et des fonctionnalités de réaction](office-365-ti.md), vous pouvez utiliser le simulateur d’attaque pour exécuter des scénarios d’attaques réalistes au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="becd0-105">**Summary** If you are a global administrator or a security administrator and your organization has Office 365 Advanced Threat Protection Plan 2, which includes [Threat Investigation and Response capabilities](office-365-ti.md), you can use Attack Simulator to run realistic attack scenarios in your organization.</span></span> <span data-ttu-id="becd0-106">Cela peut vous aider à identifier les utilisateurs vulnérables avant qu’une véritable attaque n’ait un impact sur votre chiffre d’affaires.</span><span class="sxs-lookup"><span data-stu-id="becd0-106">This can help you identify and find vulnerable users before a real attack impacts your bottom line.</span></span> <span data-ttu-id="becd0-107">Pour en savoir plus, lisez cet article.</span><span class="sxs-lookup"><span data-stu-id="becd0-107">Read this article to learn more.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="becd0-108">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="becd0-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="becd0-109">Pour ouvrir le Centre de conformité et sécurité, consultez <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="becd0-109">To open the Security & Compliance Center, go to <https://protection.office.com/>.</span></span> <span data-ttu-id="becd0-110">Le Simulateur d’attaques est disponible dans **Gestion des menaces** \> **Simulateur d’attaques**.</span><span class="sxs-lookup"><span data-stu-id="becd0-110">Attack simulator is available at **Threat management** \> **Attack simulator**.</span></span>

  ![Gestion des menaces : simulateur d’attaques](../../media/ThreatMgmt-AttackSimulator.png)

- <span data-ttu-id="becd0-112">Pour des informations supplémentaires sur la disponibilité du Simulateur d’attaques dans les différents abonnements Microsoft 365, consultez la [Description du service Office 365 ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="becd0-112">For more information about the availability of Attack Simulator across different Microsoft 365 subscriptions, see [Office 365 Advanced Threat Protection service description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>

- <span data-ttu-id="becd0-113">Vous devez être membre des groupes de rôles **Management de l’organisation** ou **Administrateur de sécurité**.</span><span class="sxs-lookup"><span data-stu-id="becd0-113">You need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span> <span data-ttu-id="becd0-114">Pour des informations supplémentaires sur les groupes de rôles dans le Centre de sécurité et conformité, voir [Autorisations dans le Centre de sécurité et conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="becd0-114">For more information about role groups in the Security & Compliance Center, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="becd0-115">Votre compte doit être configuré pour l’authentification multifacteur (MFA) afin que vous puissiez créer et gérer des campagnes dans le Simulateur d’attaques.</span><span class="sxs-lookup"><span data-stu-id="becd0-115">Your account needs to be configured for multi-factor authentication (MFA) to create and manage campaigns in Attack Simulator.</span></span> <span data-ttu-id="becd0-116">Pour consulter des instructions, voir [Configurer Multi-factor Authentification (MFA)](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication).</span><span class="sxs-lookup"><span data-stu-id="becd0-116">For instructions, see [Set up multi-factor authentication](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication).</span></span>

<span data-ttu-id="becd0-117">Pour qu’une attaque soit lancée avec succès, assurez-vous que le compte que vous utilisez pour exécuter des simulations d’attaques utilise l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="becd0-117">For an attack to be successfully launched, make sure that the account you are using to run simulated attacks is using multi-factor authentication.</span></span> <span data-ttu-id="becd0-118">De plus, vous devez être administrateur général ou administrateur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="becd0-118">In addition, you must be a global administrator or a security administrator.</span></span> <span data-ttu-id="becd0-119">(Pour en savoir plus sur les rôles et les autorisations, voir [Autorisations dans le Centre de sécurité et conformité](permissions-in-the-security-and-compliance-center.md).)</span><span class="sxs-lookup"><span data-stu-id="becd0-119">(To learn more about roles and permissions, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).)</span></span>

- <span data-ttu-id="becd0-120">Les campagnes d’hameçonnage collectent et traitent des événements sur une durée de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="becd0-120">Phishing campaigns will collect and process events for 30 days.</span></span> <span data-ttu-id="becd0-121">L’historique des données de la campagne est disponible pendant un maximum de 90 jours après le lancement de la campagne.</span><span class="sxs-lookup"><span data-stu-id="becd0-121">Historical campaign data will be available for up to 90 days after you launch the campaign.</span></span>

- <span data-ttu-id="becd0-122">Il n’existe pas d’applet de commande PowerShell correspondante pour le Simulateur d’attaques.</span><span class="sxs-lookup"><span data-stu-id="becd0-122">There are no corresponding PowerShell cmdlets for Attack Simulator.</span></span>

## <a name="spear-phishing-campaigns"></a><span data-ttu-id="becd0-123">Campagnes de Harponnage</span><span class="sxs-lookup"><span data-stu-id="becd0-123">Spear phishing campaigns</span></span>

<span data-ttu-id="becd0-124">Le *Hameçonnage* est un terme générique qui décrit les attaques par courrier électronique tentant d’accéder à des informations sensibles par le biais de messages qui paraissent provenir d’expéditeurs légitimes ou approuvés.</span><span class="sxs-lookup"><span data-stu-id="becd0-124">*Phishing* is a generic term for email attacks that try to steal sensitive information in messages that appear to be from legitimate or trusted senders.</span></span> <span data-ttu-id="becd0-125">Le *Harponnage* est une attaque ciblée par hameçonnage qui utilise un contenu très concentré et personnalisé conçu spécifiquement pour des destinataires particuliers (généralement, après reconnaissance des destinataires par l’attaquant).</span><span class="sxs-lookup"><span data-stu-id="becd0-125">*Spear phishing* is a targeted phishing attack that uses very focused and customized content that's specifically tailored to the targeted recipients (typically, after reconnaissance on the recipients by the attacker).</span></span>

- <span data-ttu-id="becd0-126">Vous êtes administrateur global ou administrateur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="becd0-126">You are a global administrator or security administrator</span></span>

<span data-ttu-id="becd0-127">Dans le Simulateur d’attaques, deux types différents de campagnes de harponnage sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="becd0-127">In Attack Simulator, two different types of spear phishing campaigns are available:</span></span>

- <span data-ttu-id="becd0-128">[L’authentification multifacteur/accès conditionnel](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication) est activée, au minimum pour le compte d’administrateur général et pour les administrateurs de sécurité qui utiliseront le simulateur d’attaques.</span><span class="sxs-lookup"><span data-stu-id="becd0-128">[Multi-factor authentication/Conditional Access](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication) is turned on, for at least the global administrator account and security administrators who will be using Attack Simulator.</span></span> <span data-ttu-id="becd0-129">(Idéalement, l’authentification multifacteur/accès conditionnel est activée pour tous les utilisateurs de votre organisation.)</span><span class="sxs-lookup"><span data-stu-id="becd0-129">(Ideally, multi-factor authentication/conditional access is turned on for all users in your organization.)</span></span>

  - <span data-ttu-id="becd0-130">Une page par défaut expliquant qu’il s’agit d’un test et donnant des conseils pour reconnaître les messages d’hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="becd0-130">A default page that explains this was a just a test, and gives tips for recognizing phishing messages.</span></span>

    ![Ce que l’utilisateur voit s’il clique sur le lien de hameçonnage, puis entre ses informations d’identification](../../media/attack-simulator-phishing-result.png)

  - <span data-ttu-id="becd0-132">Une page personnalisée (URL) que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="becd0-132">A custom page (URL) that you specify.</span></span>

- <span data-ttu-id="becd0-133">**Harponnage (pièce jointe)**  : l’attaque tente de convaincre le destinataire d’ouvrir une pièce jointe .docx ou .pdf contenue dans le message.</span><span class="sxs-lookup"><span data-stu-id="becd0-133">**Spear phishing (attachment)**: The attack tries to convince the recipients to open a .docx or .pdf attachment in the message.</span></span> <span data-ttu-id="becd0-134">La pièce jointe contient le même contenu que celui du lien d’hameçonnage par défaut, mais la première phrase commence par « \<Nom d’affichage\>, vous voyez ce message sous la forme d’un récent message électronique que vous avez ouvert... ».</span><span class="sxs-lookup"><span data-stu-id="becd0-134">The attachment contains the same content from the default phishing link, but the first sentence starts with "\<Display Name\>, you are seeing this message as a recent email message you opened...".</span></span>

> [!NOTE]
> <span data-ttu-id="becd0-135">Les campagnes de harponnage dans le Simulateur d’attaques n’arrivent pas à expiration pour le moment.</span><span class="sxs-lookup"><span data-stu-id="becd0-135">Currently, spear phishing campaigns in Attack Simulator don't expire.</span></span>

### <a name="create-a-spear-phishing-campaign"></a><span data-ttu-id="becd0-136">Création d’une campagne de harponnage</span><span class="sxs-lookup"><span data-stu-id="becd0-136">Create a spear phishing campaign</span></span>

<span data-ttu-id="becd0-137">L’apparence du message électronique envoyé aux destinataires ciblés est un élément important dans toute campagne de harponnage.</span><span class="sxs-lookup"><span data-stu-id="becd0-137">An important part of any spear phishing campaign is the look and feel of the email message that's sent to the targeted recipients.</span></span> <span data-ttu-id="becd0-138">Pour créer et configurer le courrier électronique, vous disposez des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="becd0-138">To create and configure the email message, you have these options:</span></span>

- <span data-ttu-id="becd0-139">**Utiliser un modèle d’e-mail intégré** : deux modèles prédéfinis sont disponibles : **Concours avec de nombreux prix à remporter** et **Mise à jour des données de paie**.</span><span class="sxs-lookup"><span data-stu-id="becd0-139">**Use a built-in email template**: Two built-in templates are available: **Prize Giveaway** and **Payroll Update**.</span></span> <span data-ttu-id="becd0-140">Vous pouvez personnaliser certaines, toutes ou aucune des propriétés de courrier à partir du modèle lorsque vous créez et lancez la campagne.</span><span class="sxs-lookup"><span data-stu-id="becd0-140">You can further customize some, all, or none of the email properties from the template when you create and launch the campaign.</span></span>

- <span data-ttu-id="becd0-141">**Créer un modèle d’e-mail réutilisable** : après la création et l’enregistrement du modèle de courrier, vous pouvez le réutiliser pour de prochaines campagnes de harponnage.</span><span class="sxs-lookup"><span data-stu-id="becd0-141">**Create a reusable email template**: After you create and save the email template, you can use it again in future spear phishing campaigns.</span></span> <span data-ttu-id="becd0-142">Vous pouvez personnaliser certaines, toutes ou aucune des propriétés de courrier à partir du modèle lorsque vous créez et lancez la campagne.</span><span class="sxs-lookup"><span data-stu-id="becd0-142">You can further customize some, all, or none of the email properties from the template when you create and launch the campaign.</span></span>

- <span data-ttu-id="becd0-143">**Créer le message électronique dans l’Assistant** : vous pouvez directement créer le message électronique dans l’Assistant lors de la création et du lancement de la campagne de harponnage.</span><span class="sxs-lookup"><span data-stu-id="becd0-143">**Create the email message in the wizard**: You can create the email message directly in the wizard as you create and launch the spear phishing campaign.</span></span>

#### <a name="step-1-optional-create-a-custom-email-template"></a><span data-ttu-id="becd0-144">Étape 1 (facultatif) : création d’un modèle d’e-mail personnalisé</span><span class="sxs-lookup"><span data-stu-id="becd0-144">Step 1 (Optional): Create a custom email template</span></span>

<span data-ttu-id="becd0-145">Si vous allez utiliser l’un des modèles intégrés ou créer le message directement dans l’Assistant, vous pouvez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="becd0-145">If you're going to use one of the built-in templates or create the email message directly in the wizard, you can skip this step.</span></span>

1. <span data-ttu-id="becd0-146">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Simulateur d’attaques**.</span><span class="sxs-lookup"><span data-stu-id="becd0-146">In the Security & Compliance Center, go to **Threat management** \> **Attack simulator**.</span></span>

2. <span data-ttu-id="becd0-147">Sur la page **Simulation d’attaques**, dans les sections **Harponnage (recueil des informations d’identification)** ou **Harponnage (pièce jointe)**, cliquez sur **Détails de l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="becd0-147">On the **Simulate attacks** page, in either the **Spear Phishing (Credentials Harvest)** or **Spear Phishing (Attachment)** sections, click **Attack Details**.</span></span>

   <span data-ttu-id="becd0-148">Peu importe l’emplacement où vous créez le modèle.</span><span class="sxs-lookup"><span data-stu-id="becd0-148">It doesn't matter where you create the template.</span></span> <span data-ttu-id="becd0-149">Les options disponibles dans le modèle sont identiques pour les deux types d’attaques par hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="becd0-149">The available options in the template are the same for both types of phishing attacks.</span></span>

3. <span data-ttu-id="becd0-150">Dans la page des **Détails de l’attaque** qui s’ouvre, dans la section **Modèles d’hameçonnage** de la zone **Créer des modèles**, cliquez sur **Nouveau modèle**.</span><span class="sxs-lookup"><span data-stu-id="becd0-150">In the **Attack details** page that opens, in the **Phishing Templates** section, in the **Create Templates** area, click **New Template**.</span></span>

4. <span data-ttu-id="becd0-151">L’Assistant **Configurer le modèle d’hameçonnage** démarre dans un nouveau menu volant.</span><span class="sxs-lookup"><span data-stu-id="becd0-151">The **Configure Phishing Template** wizard starts in a new flyout.</span></span> <span data-ttu-id="becd0-152">À l’étape **Démarrer**, entrez un nom d’affichage unique pour le modèle, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="becd0-152">In the **Start** step, enter a unique display name for the template, and then click **Next**.</span></span>

5. <span data-ttu-id="becd0-153">À l’étape **Configurer les détails du courrier**, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="becd0-153">In the **Configure email details** step, configure the following settings:</span></span>

   - <span data-ttu-id="becd0-154">**De (nom)**  : le nom d’affichage utilisé en tant qu’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="becd0-154">**From (Name)**: The display name that's used for the message sender.</span></span>

   - <span data-ttu-id="becd0-155">**De (adresse de courrier)**  : l’adresse de courrier de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="becd0-155">**From (Email)**: The sender's email address.</span></span>

   - <span data-ttu-id="becd0-156">**URL du serveur de connexion d’hameçonnage** : cliquez sur la liste déroulante, puis sélectionnez l’une des URL disponibles dans la liste.</span><span class="sxs-lookup"><span data-stu-id="becd0-156">**Phishing Login Server URL**: Click the drop down and select one of the available URLs from the list.</span></span> <span data-ttu-id="becd0-157">Elle représente l’URL sur laquelle les utilisateurs sont tentés de cliquer.</span><span class="sxs-lookup"><span data-stu-id="becd0-157">This is the URL that users will be tempted to click.</span></span> <span data-ttu-id="becd0-158">Les choix possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="becd0-158">The choices are:</span></span>

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
     > <ul><li><span data-ttu-id="becd0-159">Toutes les URL sont intentionnellement HTTP et non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="becd0-159">All of the URLs are intentionally http, not https.</span></span></li><li><span data-ttu-id="becd0-160">Un service de réputation d’URL peut identifier une ou plusieurs de ces URL comme étant non sécurisées.</span><span class="sxs-lookup"><span data-stu-id="becd0-160">A URL reputation service might identify one or more of these URLs as unsafe.</span></span> <span data-ttu-id="becd0-161">Vérifiez la disponibilité de l’URL dans vos navigateurs web pris en charge avant d’utiliser l’URL dans une campagne d’hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="becd0-161">Check the availability of the URL in your supported web browsers before you use the URL in a phishing campaign.</span></span></li></ul>

   - <span data-ttu-id="becd0-162">**URL de la page de destination personnalisée** : entrez une page de destination facultative vers laquelle les utilisateurs sont dirigés s’ils cliquent sur le lien d’hameçonnage et entrent leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="becd0-162">**Custom Landing Page URL**: Enter an optional landing page where users are taken if they click the phishing link and enter their credentials.</span></span> <span data-ttu-id="becd0-163">Ce lien remplace la page de destination par défaut.</span><span class="sxs-lookup"><span data-stu-id="becd0-163">This link replaces the default landing page.</span></span> <span data-ttu-id="becd0-164">Par exemple, si vous avez une formation interne de sensibilisation, vous pouvez spécifier cette URL ici.</span><span class="sxs-lookup"><span data-stu-id="becd0-164">For example, if you have internal awareness training, you can specify that URL here.</span></span>

   - <span data-ttu-id="becd0-165">**Catégorie** : ce paramètre n’est à ce jour pas utilisé (ce que vous entrez n’est pas pris en compte).</span><span class="sxs-lookup"><span data-stu-id="becd0-165">**Category**: Currently, this setting isn't used (anything you enter is ignored).</span></span>

   - <span data-ttu-id="becd0-166">**Objet** : le champ **Objet** du message électronique.</span><span class="sxs-lookup"><span data-stu-id="becd0-166">**Subject**: The **Subject** field of the email message.</span></span>

   <span data-ttu-id="becd0-167">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="becd0-167">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="becd0-168">À l’étape **Composer un message**, créez le corps du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="becd0-168">In the **Compose email** step, create the message body of the email message.</span></span> <span data-ttu-id="becd0-169">Vous pouvez utiliser l’onglet **Courrier** (éditeur HTML enrichi) ou l’onglet **Source** (code HTML brut).</span><span class="sxs-lookup"><span data-stu-id="becd0-169">You can use the **Email** tab (a rich HTML editor) or the **Source** tab (raw HTML code).</span></span>

   <span data-ttu-id="becd0-170">La mise en forme HTML peut être simple ou complexe, en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="becd0-170">The HTML formatting can be as simple or complex as you need it to be.</span></span> <span data-ttu-id="becd0-171">Vous pouvez insérer des images et du texte pour améliorer la crédibilité du message dans le client de courrier du destinataire.</span><span class="sxs-lookup"><span data-stu-id="becd0-171">You can insert images and text to enhance the believability of the message in the recipient's email client.</span></span>

   - <span data-ttu-id="becd0-172">`${username}` insère le nom du destinataire.</span><span class="sxs-lookup"><span data-stu-id="becd0-172">`${username}` inserts the recipient's name.</span></span>

   - <span data-ttu-id="becd0-173">`${loginserverurl}` insère l’**URL du serveur de connexion d’hameçonnage** de l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="becd0-173">`${loginserverurl}` inserts the **Phishing Login Server URL** value from the previous step.</span></span>

   <span data-ttu-id="becd0-174">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="becd0-174">When you're finished, click **Next**.</span></span>

7. <span data-ttu-id="becd0-175">À l’étape **Confirmer**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="becd0-175">In the **Confirm** step, click **Finish**.</span></span>

#### <a name="step-2-create-and-launch-the-spear-phishing-campaign"></a><span data-ttu-id="becd0-176">Étape 2 : création et lancement d’une campagne de harponnage</span><span class="sxs-lookup"><span data-stu-id="becd0-176">Step 2: Create and launch the spear phishing campaign</span></span>

1. <span data-ttu-id="becd0-177">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Simulateur d’attaques**.</span><span class="sxs-lookup"><span data-stu-id="becd0-177">In the Security & Compliance Center, go to **Threat management** \> **Attack simulator**.</span></span>

2. <span data-ttu-id="becd0-178">Dans la page **Simulation d’attaques**, effectuez l’une des sélections suivantes en fonction du type de campagne que vous voulez créer :</span><span class="sxs-lookup"><span data-stu-id="becd0-178">On the **Simulate attacks** page, make one of the following selections based on the type of campaign you want to create:</span></span>

   - <span data-ttu-id="becd0-179">Dans la section **Harponnage (recueil des informations d’identification)**, cliquez sur **Lancer l’attaque** ou sur **Détails de l’attaque** \> **Lancer l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="becd0-179">In the **Spear Phishing (Credentials Harvest)** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

   - <span data-ttu-id="becd0-180">Dans la section **Harponnage (pièce jointe)**, cliquez sur **Lancer l’attaque** ou sur **Détails de l’attaque** \> **Lancer l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="becd0-180">In the **Spear Phishing (Attachment)** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

3. <span data-ttu-id="becd0-181">L’Assistant **Configurer l’attaque par hameçonnage** démarre dans un nouveau menu volant.</span><span class="sxs-lookup"><span data-stu-id="becd0-181">The **Configure Phishing Attack** wizard starts in a new flyout.</span></span> <span data-ttu-id="becd0-182">À l’étape **Démarrer**, effectuez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="becd0-182">In the **Start** step, do one of the following steps:</span></span>

   - <span data-ttu-id="becd0-183">Dans la zone **Nom**, entrez un nom d’affichage unique pour la campagne.</span><span class="sxs-lookup"><span data-stu-id="becd0-183">In the **Name** box, enter a unique display name for the campaign.</span></span> <span data-ttu-id="becd0-184">Ne pas cliquer sur **Utiliser le modèle**, car vous allez plus tard créer le message électronique dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="becd0-184">Don't click **Use Template**, because you'll create the email message later in the wizard.</span></span>

   - <span data-ttu-id="becd0-185">Cliquez sur **Utiliser le modèle**, puis sélectionnez un modèle de courrier prédéfini ou personnalisé.</span><span class="sxs-lookup"><span data-stu-id="becd0-185">Click **Use Template** and select a built-in or custom email template.</span></span> <span data-ttu-id="becd0-186">Après avoir sélectionné le modèle, la boîte de dialogue **Nom** est automatiquement remplie en fonction du modèle, mais il vous est possible de modifier le nom.</span><span class="sxs-lookup"><span data-stu-id="becd0-186">After you select the template, the **Name** box is automatically filled based on the template, but you can change the name.</span></span>

   ![Page de démarrage du hameçonnage](../../media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)

   <span data-ttu-id="becd0-188">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="becd0-188">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="becd0-189">À l’étape **Destinataires cible**, effectuez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="becd0-189">In the **Target recipients** step, do one of the following steps:</span></span>

   - <span data-ttu-id="becd0-190">Cliquez sur le **Carnet d'adresses** pour sélectionner les destinataires (utilisateurs ou groupes) pour la campagne.</span><span class="sxs-lookup"><span data-stu-id="becd0-190">Click **Address Book** to select the recipients (users or groups) for the campaign.</span></span> <span data-ttu-id="becd0-191">Chaque destinataire ciblé doit avoir une boîte aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="becd0-191">Each targeted recipient must have an Exchange Online mailbox.</span></span> <span data-ttu-id="becd0-192">Si vous cliquez sur **Filtrer** et **Appliquer** sans entrer de critères de recherche, tous les destinataires sont renvoyés et ajoutés à la campagne.</span><span class="sxs-lookup"><span data-stu-id="becd0-192">If you click **Filter** and **Apply** without entering a search criteria, all recipients are returned and added to the campaign.</span></span>

   - <span data-ttu-id="becd0-193">Cliquez sur **Importer**, puis sur **Importation d’un fichier** pour importer un fichier de valeurs séparées par des virgules (CSV) ou d’adresses e-mail séparées par une ligne.</span><span class="sxs-lookup"><span data-stu-id="becd0-193">Click **Import** then **File Import** to import a comma-separated value (CSV) or line-separated file of email addresses.</span></span> <span data-ttu-id="becd0-194">Chaque ligne doit contenir l’adresse e-mail du destinataire.</span><span class="sxs-lookup"><span data-stu-id="becd0-194">Each line must contain the recipient's email address.</span></span>

   <span data-ttu-id="becd0-195">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="becd0-195">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="becd0-196">À l’étape **Configurer les détails du courrier**, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="becd0-196">In the **Configure email details** step, configure the following settings:</span></span>

   <span data-ttu-id="becd0-197">Si vous avez sélectionné un modèle au cours de l’étape **Démarrer**, la plupart de ces valeurs sont déjà configurées, mais vous pouvez les modifier.</span><span class="sxs-lookup"><span data-stu-id="becd0-197">If you selected a template in the **Start** step, most of these values are already configured, but you can change them.</span></span>

   - <span data-ttu-id="becd0-198">**De (nom)**  : le nom d’affichage utilisé en tant qu’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="becd0-198">**From (Name)**: The display name that's used for the message sender.</span></span>

   - <span data-ttu-id="becd0-199">**De (adresse de courrier)**  : l’adresse de courrier de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="becd0-199">**From (Email)**: The sender's email address.</span></span> <span data-ttu-id="becd0-200">Vous pouvez entrer une adresse de messagerie véritable ou fictive à partir du domaine de courrier de votre organisation ou vous pouvez saisir une adresse fausse ou réelle de courrier externe.</span><span class="sxs-lookup"><span data-stu-id="becd0-200">You can enter a real or fake email address from your organization's email domain, or you can enter a real or fake external email address.</span></span> <span data-ttu-id="becd0-201">Une adresse de messagerie d’expéditeur valide de votre organisation prend en réalité la forme du client de courrier du destinataire.</span><span class="sxs-lookup"><span data-stu-id="becd0-201">A valid sender email address from your organization will actually resolve in the recipient's email client.</span></span>

   - <span data-ttu-id="becd0-202">**URL du serveur de connexion d’hameçonnage** : cliquez sur la liste déroulante, puis sélectionnez l’une des URL disponibles dans la liste.</span><span class="sxs-lookup"><span data-stu-id="becd0-202">**Phishing Login Server URL**: Click the drop down and select one of the available URLs from the list.</span></span> <span data-ttu-id="becd0-203">Elle représente l’URL sur laquelle les utilisateurs sont tentés de cliquer.</span><span class="sxs-lookup"><span data-stu-id="becd0-203">This is the URL that users will be tempted to click.</span></span> <span data-ttu-id="becd0-204">Les choix possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="becd0-204">The choices are:</span></span>

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
     > <ul><li><span data-ttu-id="becd0-205">Toutes les URL sont intentionnellement HTTP et non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="becd0-205">All of the URLs are intentionally http, not https.</span></span></li><li><span data-ttu-id="becd0-206">Un service de réputation d’URL peut identifier une ou plusieurs de ces URL comme étant non sécurisées.</span><span class="sxs-lookup"><span data-stu-id="becd0-206">A URL reputation service might identify one or more of these URLs as unsafe.</span></span> <span data-ttu-id="becd0-207">Vérifiez la disponibilité de l’URL dans vos navigateurs web pris en charge avant d’utiliser l’URL dans une campagne d’hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="becd0-207">Check the availability of the URL in your supported web browsers before you use the URL in a phishing campaign.</span></span></li><li><span data-ttu-id="becd0-208">Vous devez sélectionner une URL.</span><span class="sxs-lookup"><span data-stu-id="becd0-208">You are required to select a URL.</span></span> <span data-ttu-id="becd0-209">Pour les campagnes d’<b>Harponnage (pièce jointe)</b>, vous pouvez supprimer le lien du corps du message à l’étape suivante (sinon, le message contient un lien <b>et</b> une pièce jointe).</span><span class="sxs-lookup"><span data-stu-id="becd0-209">For <b>Spear Phishing (Attachment)</b> campaigns, you can remove the link from the body of the message in the next step (otherwise, the message will contain both a link <b>and</b> an attachment).</span></span></li></ul>

   - <span data-ttu-id="becd0-210">**Type de pièce jointe** : ce paramètre n’est disponible que pour les campagnes de **Harponnage (pièce jointe)**.</span><span class="sxs-lookup"><span data-stu-id="becd0-210">**Attachment Type**: This setting is only available in **Spear Phishing (Attachment)** campaigns.</span></span> <span data-ttu-id="becd0-211">Cliquez sur la liste déroulante, puis sélectionnez **.DOCX** ou **.PDF** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="becd0-211">Click the drop down and select **.DOCX** or **.PDF** from the list.</span></span>

   - <span data-ttu-id="becd0-212">**Nom de pièce jointe** : ce paramètre n’est disponible que pour les campagnes d’**Harponnage (pièce jointe)**.</span><span class="sxs-lookup"><span data-stu-id="becd0-212">**Attachment Name**: This setting is only available in **Spear Phishing (Attachment)** campaigns.</span></span> <span data-ttu-id="becd0-213">Entrez un nom de fichier pour la pièce jointe .docx ou .pdf.</span><span class="sxs-lookup"><span data-stu-id="becd0-213">Enter a filename for the .docx or .pdf attachment.</span></span>

   - <span data-ttu-id="becd0-214">**URL de la page de destination personnalisée** : entrez une page de destination facultative vers laquelle les utilisateurs sont dirigés s’ils cliquent sur le lien d’hameçonnage et entrent leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="becd0-214">**Custom Landing Page URL**: Enter an optional landing page where users are taken if they click the phishing link and enter their credentials.</span></span> <span data-ttu-id="becd0-215">Ce lien remplace la page de destination par défaut.</span><span class="sxs-lookup"><span data-stu-id="becd0-215">This link replaces the default landing page.</span></span> <span data-ttu-id="becd0-216">Par exemple, si vous avez une formation interne de sensibilisation, vous pouvez spécifier cette URL ici.</span><span class="sxs-lookup"><span data-stu-id="becd0-216">For example, if you have internal awareness training, you can specify that URL here.</span></span>

   - <span data-ttu-id="becd0-217">**Objet** : le champ **Objet** du message électronique.</span><span class="sxs-lookup"><span data-stu-id="becd0-217">**Subject**: The **Subject** field of the email message.</span></span>

   <span data-ttu-id="becd0-218">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="becd0-218">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="becd0-219">À l’étape **Composer un message**, créez le corps du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="becd0-219">In the **Compose email** step, create the message body of the email message.</span></span> <span data-ttu-id="becd0-220">Si vous avez sélectionné un modèle au cours de l’étape **Démarrer**, le corps du message est déjà configuré, mais vous pouvez le modifier.</span><span class="sxs-lookup"><span data-stu-id="becd0-220">If you selected a template in the **Start** step, the message body is already configured, but you can customize it.</span></span> <span data-ttu-id="becd0-221">Vous pouvez utiliser l’onglet **Courrier** (éditeur HTML enrichi) ou l’onglet **Source** (code HTML brut).</span><span class="sxs-lookup"><span data-stu-id="becd0-221">You can use the **Email** tab (a rich HTML editor) or the **Source** tab (raw HTML code).</span></span>

   <span data-ttu-id="becd0-222">La mise en forme HTML peut être simple ou complexe, en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="becd0-222">The HTML formatting can be as simple or complex as you need it to be.</span></span> <span data-ttu-id="becd0-223">Vous pouvez insérer des images et du texte pour améliorer la crédibilité du message dans le client de courrier du destinataire.</span><span class="sxs-lookup"><span data-stu-id="becd0-223">You can insert images and text to enhance the believability of the message in the recipient's email client.</span></span>

   - <span data-ttu-id="becd0-224">`${username}` insère le nom du destinataire.</span><span class="sxs-lookup"><span data-stu-id="becd0-224">`${username}` inserts the recipient's name.</span></span>

   - <span data-ttu-id="becd0-225">`${loginserverurl}` insère la valeur de l’**URL du serveur de connexion d’hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="becd0-225">`${loginserverurl}` inserts the **Phishing Login Server URL** value.</span></span>

   <span data-ttu-id="becd0-226">Pour les campagnes d’**Harponnage (pièce jointe)**, il est recommandé de supprimer le lien du corps du message (sinon, le message contient un lien **et** une pièce jointe et les clics sur un lien ne sont pas suivis dans une campagne de pièce jointe).</span><span class="sxs-lookup"><span data-stu-id="becd0-226">For **Spear Phishing (Attachment)** campaigns, you should remove the link from the body of the message (otherwise, the message will contain both a link **and** an attachment, and link clicks aren't tracked in an attachment campaign).</span></span>

   ![Composer un message](../../media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)

   <span data-ttu-id="becd0-228">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="becd0-228">When you're finished, click **Next**.</span></span>

7. <span data-ttu-id="becd0-229">À l’étape **Confirmer**, cliquez sur **Terminer** pour lancer la campagne.</span><span class="sxs-lookup"><span data-stu-id="becd0-229">In the **Confirm** step, click **Finish** to launch the campaign.</span></span> <span data-ttu-id="becd0-230">Le message d’hameçonnage est remis aux destinataires ciblés.</span><span class="sxs-lookup"><span data-stu-id="becd0-230">The phishing message is delivered to the targeted recipients.</span></span>

## <a name="password-attack-campaigns"></a><span data-ttu-id="becd0-231">Campagnes d’attaques de mot de passe</span><span class="sxs-lookup"><span data-stu-id="becd0-231">Password attack campaigns</span></span>

<span data-ttu-id="becd0-232">Une *attaque de mot de passe* tente de deviner les mots de passe des comptes d’utilisateurs au sein d’une organisation, généralement une fois que l’attaquant a identifié un ou plusieurs comptes d’utilisateurs valides.</span><span class="sxs-lookup"><span data-stu-id="becd0-232">A *password attack* tries to guess passwords for user accounts in an organization, typically after the attacker has identified one or more valid user accounts.</span></span>

<span data-ttu-id="becd0-233">Dans le Simulateur d’attaques, deux types différents de campagnes d’attaque de mot de passe sont à votre disposition pour tester la complexité des mots de passe des utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="becd0-233">In Attack Simulator, two different types of password attack campaigns are available for you to test the complexity of your users' passwords:</span></span>

- <span data-ttu-id="becd0-234">**Mot de passe par force brute (attaque par dictionnaire)**  : une attaque par *force brute* ou *dictionnaire* utilise un grand fichier dictionnaire pour les mots de passe d’un compte utilisateur, avec l’espoir que l’un d’entre eux va réussir (de nombreux mots de passe pour un seul compte).</span><span class="sxs-lookup"><span data-stu-id="becd0-234">**Brute force password (dictionary attack)**: A *brute force* or *dictionary* attack uses a large dictionary file of passwords on a user account with the hope that one of them will work (many passwords against one account).</span></span> <span data-ttu-id="becd0-235">Un mot de passe incorrect permet de dissuader les attaques de mot de passe par force brute.</span><span class="sxs-lookup"><span data-stu-id="becd0-235">Incorrect password lock-outs help deter brute force password attacks.</span></span>

  <span data-ttu-id="becd0-236">Pour l’attaque par dictionnaire, vous pouvez spécifier un ou plusieurs mots de passe à tenter (entrés manuellement ou dans un fichier téléchargé), et vous pouvez spécifier un ou plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="becd0-236">For the dictionary attack, you can specify one or many passwords to try (manually entered or in an uploaded file), and you can specify one or many users.</span></span>

- <span data-ttu-id="becd0-237">L’**Attaque par pulvérisation de mots de passe** : une *pulvérisation de mots de passe* utilise le même mot de passe soigneusement étudié contre une liste de comptes d’utilisateurs (un mot de passe pour plusieurs comptes).</span><span class="sxs-lookup"><span data-stu-id="becd0-237">**Password spray attack**: A *password spray* attack uses the same carefully considered password against a list of user accounts (one password against many accounts).</span></span> <span data-ttu-id="becd0-238">Les attaques par pulvérisation de mots de passe sont plus difficiles à détecter que les attaques de mots de passe par force brute (la probabilité de réussite augmente lorsqu’un attaquant essaie un mot de passe sur des dizaines ou des centaines de comptes sans risquer de déclencher le verrouillage du mot de passe incorrect de l’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="becd0-238">Password spray attacks are harder to detect than brute force password attacks (the probability of success increases when an attacker tries one password across dozens or hundreds of accounts without the risk of tripping the user's incorrect password lock-out).</span></span>

  <span data-ttu-id="becd0-239">Pour l’attaque par pulvérisation de mots de passe, vous ne pouvez spécifier qu’un seul mot de passe et vous pouvez préciser un ou plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="becd0-239">For the password spray attack, you can only specify one password to try, and you can specify one or many users.</span></span>

> [!NOTE]
> <span data-ttu-id="becd0-240">Les attaques par mot de passe dans le Simulateur d’attaques transmettent les demandes d’authentification de base par nom d’utilisateur et mot de passe à un point de terminaison. Elles fonctionnent ainsi avec d’autres méthodes d’authentification (AD FS, synchronisation du hachage de mot de passe, directe, PingFederate, etc.).</span><span class="sxs-lookup"><span data-stu-id="becd0-240">The password attacks in Attack Simulator pass username and password Basic auth requests to an endpoint, so they also work with other authentication methods (AD FS, password hash sync, pass-through, PingFederate, etc.).</span></span> <span data-ttu-id="becd0-241">Pour les utilisateurs qui ont activé l’authentification multifacteur, même si l’attaque de mot de passe essaie son propre mot de passe, la tentative s’enregistre toujours en tant qu’échec (en d’autres termes, les utilisateurs de l’authentification multifacteur n’apparaissent jamais dans le nombre de **Tentatives réussies** de la campagne).</span><span class="sxs-lookup"><span data-stu-id="becd0-241">For users that have MFA enabled, even if the password attack tries their actual password, the attempt will always register as a failure (in other words, MFA users will never appear in the **Successful attempts** count of the campaign).</span></span> <span data-ttu-id="becd0-242">Il s'agit du résultat attendu.</span><span class="sxs-lookup"><span data-stu-id="becd0-242">This is the expected result.</span></span> <span data-ttu-id="becd0-243">L’authentification multifacteur est la méthode principale pour permettre de vous protéger contre des attaques par mot de passe.</span><span class="sxs-lookup"><span data-stu-id="becd0-243">MFA is a primary method to help protect against password attacks.</span></span>

### <a name="create-and-launch-a-password-attack-campaign"></a><span data-ttu-id="becd0-244">Création et lancement d’une campagne d’attaque par mot de passe</span><span class="sxs-lookup"><span data-stu-id="becd0-244">Create and launch a password attack campaign</span></span>

1. <span data-ttu-id="becd0-245">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Simulateur d’attaques**.</span><span class="sxs-lookup"><span data-stu-id="becd0-245">In the Security & Compliance Center, go to **Threat management** \> **Attack simulator**.</span></span>

2. <span data-ttu-id="becd0-246">Dans la page **Simulation d’attaques**, effectuez l’une des sélections suivantes en fonction du type de campagne que vous voulez créer :</span><span class="sxs-lookup"><span data-stu-id="becd0-246">On the **Simulate attacks** page, make one of the following selections based on the type of campaign you want to create:</span></span>

   - <span data-ttu-id="becd0-247">Dans la section **Mot de passe par force brute (attaque par dictionnaire)**, cliquez sur **Lancer l’attaque** ou sur **Détails de l’attaque** \> **Lancer l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="becd0-247">In the **Brute Force Password (Dictionary Attack)** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

   - <span data-ttu-id="becd0-248">Dans la section **Attaque par pulvérisation de mots de passe**, cliquez sur **Lancer l’attaque** ou sur **Détails de l’attaque** \> **Lancer l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="becd0-248">in the **Password spray attack** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

3. <span data-ttu-id="becd0-249">L’Assistant **Configurer l’attaque de mot de passe** démarre dans un nouveau menu volant.</span><span class="sxs-lookup"><span data-stu-id="becd0-249">The **Configure Password Attack** wizard starts in a new flyout.</span></span> <span data-ttu-id="becd0-250">À l’étape **Démarrer**, entrez un nom d’affichage unique pour la campagne, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="becd0-250">In the **Start** step, enter a unique display name for the campaign, and then click **Next**.</span></span>

4. <span data-ttu-id="becd0-251">À l’étape **Utilisateurs cible**, effectuez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="becd0-251">In the **Target users** step, do one of the following steps:</span></span>

   - <span data-ttu-id="becd0-252">Cliquez sur le **Carnet d'adresses** pour sélectionner les destinataires (utilisateurs ou groupes) pour la campagne.</span><span class="sxs-lookup"><span data-stu-id="becd0-252">Click **Address Book** to select the recipients (users or groups) for the campaign.</span></span> <span data-ttu-id="becd0-253">Chaque destinataire ciblé doit avoir une boîte aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="becd0-253">Each targeted recipient must have an Exchange Online mailbox.</span></span> <span data-ttu-id="becd0-254">Si vous cliquez sur **Filtrer** et **Appliquer** sans entrer de critères de recherche, tous les destinataires sont renvoyés et ajoutés à la campagne.</span><span class="sxs-lookup"><span data-stu-id="becd0-254">If you click **Filter** and **Apply** without entering a search criteria, all recipients are returned and added to the campaign.</span></span>

   - <span data-ttu-id="becd0-255">Cliquez sur **Importer**, puis sur **Importation d’un fichier** pour importer un fichier de valeurs séparées par des virgules (CSV) ou d’adresses e-mail séparées par une ligne.</span><span class="sxs-lookup"><span data-stu-id="becd0-255">Click **Import** then **File Import** to import a comma-separated value (CSV) or line-separated file of email addresses.</span></span> <span data-ttu-id="becd0-256">Chaque ligne doit contenir l’adresse e-mail du destinataire.</span><span class="sxs-lookup"><span data-stu-id="becd0-256">Each line must contain the recipient's email address.</span></span>

   <span data-ttu-id="becd0-257">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="becd0-257">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="becd0-258">À l’étape **Choix des paramètres de l’attaque**, sélectionnez ce que vous voulez faire en fonction du type de campagne :</span><span class="sxs-lookup"><span data-stu-id="becd0-258">In the **Choose attack settings** step, choose what to do based on the campaign type:</span></span>

   - <span data-ttu-id="becd0-259">**Mot de passe par force brute (attaque par dictionnaire)**  : effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="becd0-259">**Brute Force Password (Dictionary Attack)**: Do either of the following steps:</span></span>

     - <span data-ttu-id="becd0-260">**Entrez les mots de passe manuellement** : dans la boîte de dialogue **Appuyez sur Entrée pour ajouter un mot de passe**, tapez un mot de passe, puis appuyez sur ENTRÉE.</span><span class="sxs-lookup"><span data-stu-id="becd0-260">**Enter passwords manually**: In the **Press enter to add a password** box, type a password and then press ENTER.</span></span> <span data-ttu-id="becd0-261">Répétez cette étape autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="becd0-261">Repeat this step as many times as necessary.</span></span>

     - <span data-ttu-id="becd0-262">**Charger des mots de passe à partir d’un fichier dictionnaire**: cliquez sur **Télécharger** pour importer un fichier texte existant qui contient un mot de passe sur chaque ligne et une dernière ligne vide.</span><span class="sxs-lookup"><span data-stu-id="becd0-262">**Upload passwords from a dictionary file**: Click **Upload** to import an existing text file that contains one password on each line and a blank last line.</span></span> <span data-ttu-id="becd0-263">La taille du fichier texte doit être inférieure ou égale à 10 Mo et ne peut pas contenir plus de 30 000 mots de passe.</span><span class="sxs-lookup"><span data-stu-id="becd0-263">The text file must be 10 MB or less in size, and can't contain more than 30000 passwords.</span></span>

   - <span data-ttu-id="becd0-264">**Attaque par pulvérisation par mots de passe** : entrez un mot de passe dans la zone de dialogue **Le ou les mots de passe à utiliser dans le cadre de l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="becd0-264">**Password spray attack**: In **The password(s) to use in the attack** box, enter one password.</span></span>

   <span data-ttu-id="becd0-265">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="becd0-265">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="becd0-266">À l’étape **Confirmer**, cliquez sur **Terminer** pour lancer la campagne.</span><span class="sxs-lookup"><span data-stu-id="becd0-266">In the **Confirm** step, click **Finish** to launch the campaign.</span></span> <span data-ttu-id="becd0-267">Les mots de passe que vous avez spécifiés ont été essayés pour les utilisateurs que vous avez précisés.</span><span class="sxs-lookup"><span data-stu-id="becd0-267">The passwords you specified are tried on users you specified.</span></span>

## <a name="view-campaign-results"></a><span data-ttu-id="becd0-268">Afficher les résultats de la campagne</span><span class="sxs-lookup"><span data-stu-id="becd0-268">View campaign results</span></span>

<span data-ttu-id="becd0-269">Après avoir lancé une campagne, vous pouvez consulter l’avancement et les résultats sur la page principale **Simulation d’attaques**.</span><span class="sxs-lookup"><span data-stu-id="becd0-269">After you launch a campaign, you can check the progress and results on the main **Simulate attacks** page.</span></span>

<span data-ttu-id="becd0-270">Les campagnes actives affichent une barre de statut, une valeur de pourcentage terminée et un nombre « (utilisateurs terminés) sur (total des utilisateurs) ».</span><span class="sxs-lookup"><span data-stu-id="becd0-270">Active campaigns will show a status bar, a completed percentage value and "(completed users) of (total users)" count.</span></span> <span data-ttu-id="becd0-271">Le fait de cliquer sur le bouton **Actualiser** permet de mettre à jour l’avancement de toutes les campagnes actives.</span><span class="sxs-lookup"><span data-stu-id="becd0-271">Clicking the **Refresh** button will update the progress of any active campaigns.</span></span> <span data-ttu-id="becd0-272">Vous pouvez également cliquer sur **Terminer** pour arrêter une campagne active.</span><span class="sxs-lookup"><span data-stu-id="becd0-272">You can also click **Terminate** to stop an active campaign.</span></span>

<span data-ttu-id="becd0-273">Une fois la campagne terminée, le statut devient **Attaque achevée**.</span><span class="sxs-lookup"><span data-stu-id="becd0-273">When the campaign is finished, the status changes to **Attack completed**.</span></span> <span data-ttu-id="becd0-274">Vous pouvez afficher les résultats de la campagne en effectuant l’une des actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="becd0-274">You can view the results of the campaign by doing either of the following actions:</span></span>

- <span data-ttu-id="becd0-275">Dans la page principale **Simulation d’attaques**, cliquez sur **Afficher le rapport** sous le nom de la campagne.</span><span class="sxs-lookup"><span data-stu-id="becd0-275">On the main **Simulate attacks** page, click **View Report** under the name of the campaign.</span></span>

- <span data-ttu-id="becd0-276">Dans la page principale **Simulation d’attaques**, cliquez sur les **Détails de l’attaque** dans la section correspondant au type d’attaque.</span><span class="sxs-lookup"><span data-stu-id="becd0-276">On the main **Simulate attacks** page, click **Attack Details** in the section for the type of attack.</span></span> <span data-ttu-id="becd0-277">Dans la page **Détails de l’attaque** qui s’ouvre, sélectionnez la campagne dans la section **Historique des attaques**.</span><span class="sxs-lookup"><span data-stu-id="becd0-277">On the **Attack details** page that opens, select the campaign in the **Attack History** section.</span></span>

<span data-ttu-id="becd0-278">L’une des actions précédentes vous dirige vers une page intitulée **Détails de l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="becd0-278">Either of the previous actions will take you to a page named **Attack details**.</span></span> <span data-ttu-id="becd0-279">Les informations disponibles dans cette page pour chaque type de campagne sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="becd0-279">The information that's available on this page for each type of campaign is described in the following sections.</span></span>

### <a name="spear-phishing-credentials-harvest-campaign-results"></a><span data-ttu-id="becd0-280">Résultats de campagne de harponnage (recueil des informations d’identification)</span><span class="sxs-lookup"><span data-stu-id="becd0-280">Spear Phishing (Credentials Harvest) campaign results</span></span>

<span data-ttu-id="becd0-281">Les informations suivantes sont disponibles sur la page des **Détails de l’attaque** pour chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="becd0-281">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="becd0-282">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="becd0-282">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="becd0-283">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="becd0-283">**Total users targeted**</span></span>

- <span data-ttu-id="becd0-284">**Tentatives réussies** : le nombre d’utilisateurs qui ont cliqué sur le lien **et** entré leurs informations d’identification (*toute* valeur de nom d’utilisateur et de mot de passe).</span><span class="sxs-lookup"><span data-stu-id="becd0-284">**Successful attempts**: The number of users who clicked the link **and** entered their credentials (*any* username and password value).</span></span>

- <span data-ttu-id="becd0-285">**Taux de réussite globale** : un pourcentage calculé par **Tentatives réussies** / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="becd0-285">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>

- <span data-ttu-id="becd0-286">**Le plus rapide – Clic** : le temps qu’il a fallu au premier utilisateur pour cliquer sur le lien après le lancement de votre campagne.</span><span class="sxs-lookup"><span data-stu-id="becd0-286">**Fastest Click**: How long it took the first user to click the link after you launched the campaign.</span></span>

- <span data-ttu-id="becd0-287">**Moyenne – Clic** : le temps total qu’il a fallu à tous les utilisateurs pour cliquer sur le lien, divisé par le nombre d’utilisateurs qui ont cliqué sur le lien.</span><span class="sxs-lookup"><span data-stu-id="becd0-287">**Average Click**: The sum of how long it took everyone to click the link divided by the number of users who clicked the link.</span></span>

- <span data-ttu-id="becd0-288">**Taux de réussite – Clic** : un pourcentage calculé par le (nombre d’utilisateurs qui ont cliqué sur le lien) / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="becd0-288">**Click Success Rate**: A percentage that's calculated by (number of users who clicked the link) / **Total users targeted**.</span></span>

- <span data-ttu-id="becd0-289">**Le plus rapide – Informations d’identification** : le temps qu’il a fallu au premier utilisateur pour entrer ses informations d’identification après le lancement de votre campagne.</span><span class="sxs-lookup"><span data-stu-id="becd0-289">**Fastest Credentials**: How long it took the first user to enter their credentials after you launched the campaign.</span></span>

- <span data-ttu-id="becd0-290">**Moyenne – Informations d’identification** : le temps total qu’il a fallu à tous les utilisateurs pour entrer leurs informations d’identification divisé par le nombre d’utilisateurs qui ont entré leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="becd0-290">**Average Credentials**: The sum of how long it took everyone to enter their credentials divided by the number of users who entered their credentials.</span></span>

- <span data-ttu-id="becd0-291">**Taux de réussite – Informations d’identification** : un pourcentage calculé par le (nombre d’utilisateurs qui ont entré leurs informations d’identification) / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="becd0-291">**Credential Success Rate**: A percentage that's calculated by (number of users who entered their credentials) / **Total users targeted**.</span></span>

- <span data-ttu-id="becd0-292">Graphique à barres affichant le **Lien sur lequel un clic a été effectué** et le nombre d’**Informations d’identification fournies** par jour.</span><span class="sxs-lookup"><span data-stu-id="becd0-292">A bar graph that shows the **Link clicked** and **Credential supplied** numbers per day.</span></span>

- <span data-ttu-id="becd0-293">Graphique circulaire affichant les pourcentages **Lien sur lequel un clic a été effectué**, **Informations d’identification fournies**et **Aucun** pour la campagne.</span><span class="sxs-lookup"><span data-stu-id="becd0-293">A circle graph that shows the **Link clicked**, **Credential supplied**, and **None** percentages for the campaign.</span></span>

- <span data-ttu-id="becd0-294">La section **Utilisateurs compromis** répertorie des informations sur les utilisateurs qui ont cliqué sur le lien :</span><span class="sxs-lookup"><span data-stu-id="becd0-294">The **Compromised Users** section lists the details of the users who clicked the link:</span></span>

  - <span data-ttu-id="becd0-295">L’adresse de messagerie de l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="becd0-295">The user's email address</span></span>

  - <span data-ttu-id="becd0-296">Date/heure à laquelle il a cliqué sur le lien.</span><span class="sxs-lookup"><span data-stu-id="becd0-296">The date/time when they clicked the link.</span></span>

  - <span data-ttu-id="becd0-297">L’adresse IP du client.</span><span class="sxs-lookup"><span data-stu-id="becd0-297">The client IP address.</span></span>

  - <span data-ttu-id="becd0-298">Détails sur la version de Windows et le navigateur web de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="becd0-298">Details about the user's version of Windows and web browser.</span></span>

  <span data-ttu-id="becd0-299">Vous pouvez cliquer sur **Exporter** pour exporter les résultats dans un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="becd0-299">You can click **Export** to export the results to a CSV file.</span></span>

### <a name="spear-phishing-attachment-campaign-results"></a><span data-ttu-id="becd0-300">Résultats de la campagne de harponnage (pièce jointe)</span><span class="sxs-lookup"><span data-stu-id="becd0-300">Spear Phishing (Attachment) campaign results</span></span>

<span data-ttu-id="becd0-301">Les informations suivantes sont disponibles sur la page des **Détails de l’attaque** pour chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="becd0-301">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="becd0-302">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="becd0-302">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="becd0-303">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="becd0-303">**Total users targeted**</span></span>

- <span data-ttu-id="becd0-304">**Tentatives réussies** : nombre d’utilisateurs qui ont ouvert ou téléchargé et ouvert la pièce jointe (l’aperçu ne compte pas).</span><span class="sxs-lookup"><span data-stu-id="becd0-304">**Successful attempts**: The number of users who opened or downloaded and opened the attachment (preview doesn't count).</span></span>

- <span data-ttu-id="becd0-305">**Taux de réussite globale** : un pourcentage calculé par **Tentatives réussies** / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="becd0-305">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>

- <span data-ttu-id="becd0-306">**Délai d’ouverture des pièces jointes le plus rapide** : le temps qu’il a fallu au premier utilisateur pour ouvrir la pièce jointe après le lancement de votre campagne.</span><span class="sxs-lookup"><span data-stu-id="becd0-306">**Fastest attachment open time**: How long it took the first user to open the attachment after you launched the campaign.</span></span>

- <span data-ttu-id="becd0-307">**Délai moyen d’ouverture des pièces jointes** : le temps total qu’il a fallu à tous les utilisateurs pour ouvrir la pièce jointe divisé par le nombre de personnes qui ont ouvert la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="becd0-307">**Average attachment open time**: The sum of how long it took everyone to open the attachment divided by the number of users who opened the attachment.</span></span>

- <span data-ttu-id="becd0-308">**Taux d’ouverture réussie des pièces jointes ** : un pourcentage calculé par le (nombre d’utilisateurs qui ont ouvert la pièce jointe) / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="becd0-308">**Attachment open success rate**: A percentage that's calculated by (number of users who opened the attachment) / **Total users targeted**.</span></span>

### <a name="brute-force-password-dictionary-attack-campaign-results"></a><span data-ttu-id="becd0-309">Résultats de la campagne de mot de passe par force brute (attaque par dictionnaire)</span><span class="sxs-lookup"><span data-stu-id="becd0-309">Brute Force Password (Dictionary Attack) campaign results</span></span>

<span data-ttu-id="becd0-310">Les informations suivantes sont disponibles sur la page des **Détails de l’attaque** pour chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="becd0-310">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="becd0-311">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="becd0-311">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="becd0-312">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="becd0-312">**Total users targeted**</span></span>

- <span data-ttu-id="becd0-313">**Tentatives réussies** : nombre d’utilisateurs qui se sont avérées utiliser l’un des mots de passe spécifiés.</span><span class="sxs-lookup"><span data-stu-id="becd0-313">**Successful attempts**: The number of users who were found to be using one of the specified passwords.</span></span>

- <span data-ttu-id="becd0-314">**Taux de réussite globale** : un pourcentage calculé par **Tentatives réussies** / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="becd0-314">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>

- <span data-ttu-id="becd0-315">La section **Utilisateurs compromis** répertorie les adresses de courrier des utilisateurs concernés.</span><span class="sxs-lookup"><span data-stu-id="becd0-315">The **Compromised Users** section lists the email addresses of the affected users.</span></span> <span data-ttu-id="becd0-316">Vous pouvez cliquer sur **Exporter** pour exporter les résultats dans un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="becd0-316">You can click **Export** to export the results to a CSV file.</span></span>

### <a name="password-spray-attack-campaign-results"></a><span data-ttu-id="becd0-317">Résultats de la campagne d’attaque par pulvérisation par mots de passe</span><span class="sxs-lookup"><span data-stu-id="becd0-317">Password spray attack campaign results</span></span>

<span data-ttu-id="becd0-318">Les informations suivantes sont disponibles sur la page des **Détails de l’attaque** pour chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="becd0-318">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="becd0-319">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="becd0-319">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="becd0-320">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="becd0-320">**Total users targeted**</span></span>

- <span data-ttu-id="becd0-321">**Tentatives réussies** : nombre d’utilisateurs qui se sont avérées utiliser le mot de passe spécifié.</span><span class="sxs-lookup"><span data-stu-id="becd0-321">**Successful attempts**: The number of users who were found to be using the specified password.</span></span>

- <span data-ttu-id="becd0-322">**Taux de réussite globale** : un pourcentage calculé par **Tentatives réussies** / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="becd0-322">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>
