---
title: Simulateur d’attaques dans ATP
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à utiliser un simulateur d’attaque pour exécuter des attaques de hameçonnage et de mot de passe simulées dans les organisations plan 2 de Microsoft 365 E5 ou ATP.
ms.openlocfilehash: 017376d8002811398fe3ce2d94f7c207cd718a78
ms.sourcegitcommit: e12fa502bc216f6083ef5666f693a04bb727d4df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "46825832"
---
# <a name="attack-simulator-in-atp"></a><span data-ttu-id="094ea-103">Simulateur d’attaques dans ATP</span><span class="sxs-lookup"><span data-stu-id="094ea-103">Attack Simulator in ATP</span></span>

<span data-ttu-id="094ea-104">Si votre organisation dispose d’Office 365 Advanced Threat Protection (ATP) plan 2, qui inclut des [fonctionnalités d’enquête et de réponse aux menaces](office-365-ti.md), vous pouvez utiliser un simulateur d’attaque dans le centre de sécurité & conformité pour exécuter des scénarios d’attaque réaliste dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="094ea-104">If your organization has Office 365 Advanced Threat Protection (ATP) Plan 2, which includes [Threat Investigation and Response capabilities](office-365-ti.md), you can use Attack Simulator in the Security & Compliance Center to run realistic attack scenarios in your organization.</span></span> <span data-ttu-id="094ea-105">Ces attaques simulées peuvent vous aider à identifier et à trouver des utilisateurs vulnérables avant qu’une véritable attaque n’influe sur votre ligne de base.</span><span class="sxs-lookup"><span data-stu-id="094ea-105">These simulated attacks can help you identify and find vulnerable users before a real attack impacts your bottom line.</span></span> <span data-ttu-id="094ea-106">Pour en savoir plus, lisez cet article.</span><span class="sxs-lookup"><span data-stu-id="094ea-106">Read this article to learn more.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="094ea-107">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="094ea-107">What do you need to know before you begin?</span></span>

- <span data-ttu-id="094ea-108">Pour ouvrir le Centre de conformité et sécurité, consultez <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="094ea-108">To open the Security & Compliance Center, go to <https://protection.office.com/>.</span></span> <span data-ttu-id="094ea-109">Le Simulateur d’attaques est disponible dans **Gestion des menaces** \> **Simulateur d’attaques**.</span><span class="sxs-lookup"><span data-stu-id="094ea-109">Attack simulator is available at **Threat management** \> **Attack simulator**.</span></span> <span data-ttu-id="094ea-110">Accédez directement à simulateur d’attaque, ouvrez <https://protection.office.com/attacksimulator> .</span><span class="sxs-lookup"><span data-stu-id="094ea-110">Go go directly to attack simulator, open <https://protection.office.com/attacksimulator>.</span></span>

- <span data-ttu-id="094ea-111">Pour des informations supplémentaires sur la disponibilité du Simulateur d’attaques dans les différents abonnements Microsoft 365, consultez la [Description du service Office 365 ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="094ea-111">For more information about the availability of Attack Simulator across different Microsoft 365 subscriptions, see [Office 365 Advanced Threat Protection service description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>

- <span data-ttu-id="094ea-112">Vous devez être membre des groupes de rôles **Management de l’organisation** ou **Administrateur de sécurité**.</span><span class="sxs-lookup"><span data-stu-id="094ea-112">You need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span> <span data-ttu-id="094ea-113">Pour des informations supplémentaires sur les groupes de rôles dans le Centre de sécurité et conformité, voir [Autorisations dans le Centre de sécurité et conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="094ea-113">For more information about role groups in the Security & Compliance Center, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="094ea-114">Votre compte doit être configuré pour l’authentification multifacteur (MFA) afin que vous puissiez créer et gérer des campagnes dans le Simulateur d’attaques.</span><span class="sxs-lookup"><span data-stu-id="094ea-114">Your account needs to be configured for multi-factor authentication (MFA) to create and manage campaigns in Attack Simulator.</span></span> <span data-ttu-id="094ea-115">Pour consulter des instructions, voir [Configurer Multi-factor Authentification (MFA)](https://docs.microsoft.com/microsoft-365/admin/security-and-compliance/set-up-multi-factor-authentication).</span><span class="sxs-lookup"><span data-stu-id="094ea-115">For instructions, see [Set up multi-factor authentication](https://docs.microsoft.com/microsoft-365/admin/security-and-compliance/set-up-multi-factor-authentication).</span></span>

- <span data-ttu-id="094ea-116">Les campagnes d’hameçonnage collectent et traitent des événements sur une durée de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="094ea-116">Phishing campaigns will collect and process events for 30 days.</span></span> <span data-ttu-id="094ea-117">L’historique des données de la campagne est disponible pendant un maximum de 90 jours après le lancement de la campagne.</span><span class="sxs-lookup"><span data-stu-id="094ea-117">Historical campaign data will be available for up to 90 days after you launch the campaign.</span></span>

- <span data-ttu-id="094ea-118">Il n’existe pas d’applet de commande PowerShell correspondante pour le Simulateur d’attaques.</span><span class="sxs-lookup"><span data-stu-id="094ea-118">There are no corresponding PowerShell cmdlets for Attack Simulator.</span></span>

## <a name="spear-phishing-campaigns"></a><span data-ttu-id="094ea-119">Campagnes de Harponnage</span><span class="sxs-lookup"><span data-stu-id="094ea-119">Spear phishing campaigns</span></span>

<span data-ttu-id="094ea-120">Le *Hameçonnage* est un terme générique qui décrit les attaques par courrier électronique tentant d’accéder à des informations sensibles par le biais de messages qui paraissent provenir d’expéditeurs légitimes ou approuvés.</span><span class="sxs-lookup"><span data-stu-id="094ea-120">*Phishing* is a generic term for email attacks that try to steal sensitive information in messages that appear to be from legitimate or trusted senders.</span></span> <span data-ttu-id="094ea-121">Le *Spear Phishing* est une attaque par hameçonnage ciblée qui utilise du contenu ciblé et personnalisé qui est spécifiquement adapté aux destinataires ciblés (en général, après la reconnaissance des destinataires par l’agresseur).</span><span class="sxs-lookup"><span data-stu-id="094ea-121">*Spear phishing* is a targeted phishing attack that uses focused and customized content that's specifically tailored to the targeted recipients (typically, after reconnaissance on the recipients by the attacker).</span></span>

<span data-ttu-id="094ea-122">Dans le Simulateur d’attaques, deux types différents de campagnes de harponnage sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="094ea-122">In Attack Simulator, two different types of spear phishing campaigns are available:</span></span>

- <span data-ttu-id="094ea-123">**Spear Phishing (informations d’identification)**: l’attaque tente de convaincre les destinataires de cliquer sur une URL dans le message.</span><span class="sxs-lookup"><span data-stu-id="094ea-123">**Spear phishing (credentials harvest)**: The attack tries to convince the recipients to click a URL in the message.</span></span> <span data-ttu-id="094ea-124">S’ils cliquent sur le lien, ils sont invités à entrer leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="094ea-124">If they click the link, they're asked to enter their credentials.</span></span> <span data-ttu-id="094ea-125">Si c’est le cas, ils sont dirigés vers l’un des emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="094ea-125">If they do, they're taken to one of the following locations:</span></span>

  - <span data-ttu-id="094ea-126">Page par défaut qui explique qu’il s’agissait d’un simple test et fournit des conseils pour la reconnaissance des messages de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="094ea-126">A default page that explains that this was a just a test, and gives tips for recognizing phishing messages.</span></span>

    ![Ce que l’utilisateur voit s’il clique sur le lien de hameçonnage, puis entre ses informations d’identification](../../media/attack-simulator-phishing-result.png)

  - <span data-ttu-id="094ea-128">Une page personnalisée (URL) que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="094ea-128">A custom page (URL) that you specify.</span></span>

- <span data-ttu-id="094ea-129">**Harponnage (pièce jointe)**  : l’attaque tente de convaincre le destinataire d’ouvrir une pièce jointe .docx ou .pdf contenue dans le message.</span><span class="sxs-lookup"><span data-stu-id="094ea-129">**Spear phishing (attachment)**: The attack tries to convince the recipients to open a .docx or .pdf attachment in the message.</span></span> <span data-ttu-id="094ea-130">La pièce jointe contient le même contenu que le lien de hameçonnage par défaut, mais la première phrase commence par " \<Display Name\> , vous voyez ce message en tant que message récent que vous avez ouvert...".</span><span class="sxs-lookup"><span data-stu-id="094ea-130">The attachment contains the same content from the default phishing link, but the first sentence starts with "\<Display Name\>, you are seeing this message as a recent email message you opened...".</span></span>

> [!NOTE]
> <span data-ttu-id="094ea-131">Les campagnes de harponnage dans le Simulateur d’attaques n’arrivent pas à expiration pour le moment.</span><span class="sxs-lookup"><span data-stu-id="094ea-131">Currently, spear phishing campaigns in Attack Simulator don't expire.</span></span>

### <a name="create-a-spear-phishing-campaign"></a><span data-ttu-id="094ea-132">Création d’une campagne de harponnage</span><span class="sxs-lookup"><span data-stu-id="094ea-132">Create a spear phishing campaign</span></span>

<span data-ttu-id="094ea-133">L’apparence du message électronique envoyé aux destinataires ciblés est un élément important dans toute campagne de harponnage.</span><span class="sxs-lookup"><span data-stu-id="094ea-133">An important part of any spear phishing campaign is the look and feel of the email message that's sent to the targeted recipients.</span></span> <span data-ttu-id="094ea-134">Pour créer et configurer le courrier électronique, vous disposez des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="094ea-134">To create and configure the email message, you have these options:</span></span>

- <span data-ttu-id="094ea-135">**Utiliser un modèle d’e-mail intégré** : deux modèles prédéfinis sont disponibles : **Concours avec de nombreux prix à remporter** et **Mise à jour des données de paie**.</span><span class="sxs-lookup"><span data-stu-id="094ea-135">**Use a built-in email template**: Two built-in templates are available: **Prize Giveaway** and **Payroll Update**.</span></span> <span data-ttu-id="094ea-136">Vous pouvez personnaliser certaines, toutes ou aucune des propriétés de courrier à partir du modèle lorsque vous créez et lancez la campagne.</span><span class="sxs-lookup"><span data-stu-id="094ea-136">You can further customize some, all, or none of the email properties from the template when you create and launch the campaign.</span></span>

- <span data-ttu-id="094ea-137">**Créer un modèle d’e-mail réutilisable** : après la création et l’enregistrement du modèle de courrier, vous pouvez le réutiliser pour de prochaines campagnes de harponnage.</span><span class="sxs-lookup"><span data-stu-id="094ea-137">**Create a reusable email template**: After you create and save the email template, you can use it again in future spear phishing campaigns.</span></span> <span data-ttu-id="094ea-138">Vous pouvez personnaliser certaines, toutes ou aucune des propriétés de courrier à partir du modèle lorsque vous créez et lancez la campagne.</span><span class="sxs-lookup"><span data-stu-id="094ea-138">You can further customize some, all, or none of the email properties from the template when you create and launch the campaign.</span></span>

- <span data-ttu-id="094ea-139">**Créer le message électronique dans l’Assistant** : vous pouvez directement créer le message électronique dans l’Assistant lors de la création et du lancement de la campagne de harponnage.</span><span class="sxs-lookup"><span data-stu-id="094ea-139">**Create the email message in the wizard**: You can create the email message directly in the wizard as you create and launch the spear phishing campaign.</span></span>

#### <a name="step-1-optional-create-a-custom-email-template"></a><span data-ttu-id="094ea-140">Étape 1 (facultatif) : création d’un modèle d’e-mail personnalisé</span><span class="sxs-lookup"><span data-stu-id="094ea-140">Step 1 (Optional): Create a custom email template</span></span>

<span data-ttu-id="094ea-141">Si vous allez utiliser l’un des modèles intégrés ou créer le message directement dans l’Assistant, vous pouvez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="094ea-141">If you're going to use one of the built-in templates or create the email message directly in the wizard, you can skip this step.</span></span>

1. <span data-ttu-id="094ea-142">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Simulateur d’attaques**.</span><span class="sxs-lookup"><span data-stu-id="094ea-142">In the Security & Compliance Center, go to **Threat management** \> **Attack simulator**.</span></span>

2. <span data-ttu-id="094ea-143">Sur la page **Simulation d’attaques**, dans les sections **Harponnage (recueil des informations d’identification)** ou **Harponnage (pièce jointe)**, cliquez sur **Détails de l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="094ea-143">On the **Simulate attacks** page, in either the **Spear Phishing (Credentials Harvest)** or **Spear Phishing (Attachment)** sections, click **Attack Details**.</span></span>

   <span data-ttu-id="094ea-144">Peu importe l’emplacement où vous créez le modèle.</span><span class="sxs-lookup"><span data-stu-id="094ea-144">It doesn't matter where you create the template.</span></span> <span data-ttu-id="094ea-145">Les options disponibles dans le modèle sont identiques pour les deux types d’attaques par hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="094ea-145">The available options in the template are the same for both types of phishing attacks.</span></span>

3. <span data-ttu-id="094ea-146">Dans la page des **Détails de l’attaque** qui s’ouvre, dans la section **Modèles d’hameçonnage** de la zone **Créer des modèles**, cliquez sur **Nouveau modèle**.</span><span class="sxs-lookup"><span data-stu-id="094ea-146">In the **Attack details** page that opens, in the **Phishing Templates** section, in the **Create Templates** area, click **New Template**.</span></span>

4. <span data-ttu-id="094ea-147">L’Assistant **Configurer le modèle d’hameçonnage** démarre dans un nouveau menu volant.</span><span class="sxs-lookup"><span data-stu-id="094ea-147">The **Configure Phishing Template** wizard starts in a new flyout.</span></span> <span data-ttu-id="094ea-148">À l’étape **Démarrer**, entrez un nom d’affichage unique pour le modèle, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="094ea-148">In the **Start** step, enter a unique display name for the template, and then click **Next**.</span></span>

5. <span data-ttu-id="094ea-149">À l’étape **Configurer les détails du courrier**, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="094ea-149">In the **Configure email details** step, configure the following settings:</span></span>

   - <span data-ttu-id="094ea-150">**De (nom)**  : le nom d’affichage utilisé en tant qu’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="094ea-150">**From (Name)**: The display name that's used for the message sender.</span></span>

   - <span data-ttu-id="094ea-151">**De (adresse de courrier)**  : l’adresse de courrier de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="094ea-151">**From (Email)**: The sender's email address.</span></span>

   - <span data-ttu-id="094ea-152">**URL du serveur de connexion d’hameçonnage** : cliquez sur la liste déroulante, puis sélectionnez l’une des URL disponibles dans la liste.</span><span class="sxs-lookup"><span data-stu-id="094ea-152">**Phishing Login Server URL**: Click the drop down and select one of the available URLs from the list.</span></span> <span data-ttu-id="094ea-153">Elle représente l’URL sur laquelle les utilisateurs sont tentés de cliquer.</span><span class="sxs-lookup"><span data-stu-id="094ea-153">This is the URL that users will be tempted to click.</span></span> <span data-ttu-id="094ea-154">Les choix possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="094ea-154">The choices are:</span></span>

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
     >
     > - <span data-ttu-id="094ea-155">Toutes les URL sont intentionnellement HTTP et non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="094ea-155">All of the URLs are intentionally http, not https.</span></span>
     >
     > - <span data-ttu-id="094ea-156">Un service de réputation d’URL peut identifier une ou plusieurs de ces URL comme étant non sécurisées.</span><span class="sxs-lookup"><span data-stu-id="094ea-156">A URL reputation service might identify one or more of these URLs as unsafe.</span></span> <span data-ttu-id="094ea-157">Vérifiez la disponibilité de l’URL dans vos navigateurs web pris en charge avant d’utiliser l’URL dans une campagne d’hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="094ea-157">Check the availability of the URL in your supported web browsers before you use the URL in a phishing campaign.</span></span>

   - <span data-ttu-id="094ea-158">**URL de la page de destination personnalisée** : entrez une page de destination facultative vers laquelle les utilisateurs sont dirigés s’ils cliquent sur le lien d’hameçonnage et entrent leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="094ea-158">**Custom Landing Page URL**: Enter an optional landing page where users are taken if they click the phishing link and enter their credentials.</span></span> <span data-ttu-id="094ea-159">Ce lien remplace la page de destination par défaut.</span><span class="sxs-lookup"><span data-stu-id="094ea-159">This link replaces the default landing page.</span></span> <span data-ttu-id="094ea-160">Par exemple, si vous avez une formation interne de sensibilisation, vous pouvez spécifier cette URL ici.</span><span class="sxs-lookup"><span data-stu-id="094ea-160">For example, if you have internal awareness training, you can specify that URL here.</span></span>

   - <span data-ttu-id="094ea-161">**Catégorie** : ce paramètre n’est à ce jour pas utilisé (ce que vous entrez n’est pas pris en compte).</span><span class="sxs-lookup"><span data-stu-id="094ea-161">**Category**: Currently, this setting isn't used (anything you enter is ignored).</span></span>

   - <span data-ttu-id="094ea-162">**Objet** : le champ **Objet** du message électronique.</span><span class="sxs-lookup"><span data-stu-id="094ea-162">**Subject**: The **Subject** field of the email message.</span></span>

   <span data-ttu-id="094ea-163">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="094ea-163">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="094ea-164">À l’étape **Composer un message**, créez le corps du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="094ea-164">In the **Compose email** step, create the message body of the email message.</span></span> <span data-ttu-id="094ea-165">Vous pouvez utiliser l’onglet **Courrier** (éditeur HTML enrichi) ou l’onglet **Source** (code HTML brut).</span><span class="sxs-lookup"><span data-stu-id="094ea-165">You can use the **Email** tab (a rich HTML editor) or the **Source** tab (raw HTML code).</span></span>

   <span data-ttu-id="094ea-166">La mise en forme HTML peut être simple ou complexe, en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="094ea-166">The HTML formatting can be as simple or complex as you need it to be.</span></span> <span data-ttu-id="094ea-167">Vous pouvez insérer des images et du texte pour améliorer la crédibilité du message dans le client de courrier du destinataire.</span><span class="sxs-lookup"><span data-stu-id="094ea-167">You can insert images and text to enhance the believability of the message in the recipient's email client.</span></span>

   - <span data-ttu-id="094ea-168">`${username}` insère le nom du destinataire.</span><span class="sxs-lookup"><span data-stu-id="094ea-168">`${username}` inserts the recipient's name.</span></span>

   - <span data-ttu-id="094ea-169">`${loginserverurl}` insère l’**URL du serveur de connexion d’hameçonnage** de l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="094ea-169">`${loginserverurl}` inserts the **Phishing Login Server URL** value from the previous step.</span></span>

   <span data-ttu-id="094ea-170">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="094ea-170">When you're finished, click **Next**.</span></span>

7. <span data-ttu-id="094ea-171">À l’étape **Confirmer**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="094ea-171">In the **Confirm** step, click **Finish**.</span></span>

#### <a name="step-2-create-and-launch-the-spear-phishing-campaign"></a><span data-ttu-id="094ea-172">Étape 2 : création et lancement d’une campagne de harponnage</span><span class="sxs-lookup"><span data-stu-id="094ea-172">Step 2: Create and launch the spear phishing campaign</span></span>

1. <span data-ttu-id="094ea-173">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Simulateur d’attaques**.</span><span class="sxs-lookup"><span data-stu-id="094ea-173">In the Security & Compliance Center, go to **Threat management** \> **Attack simulator**.</span></span>

2. <span data-ttu-id="094ea-174">Dans la page **Simulation d’attaques**, effectuez l’une des sélections suivantes en fonction du type de campagne que vous voulez créer :</span><span class="sxs-lookup"><span data-stu-id="094ea-174">On the **Simulate attacks** page, make one of the following selections based on the type of campaign you want to create:</span></span>

   - <span data-ttu-id="094ea-175">Dans la section **Harponnage (recueil des informations d’identification)**, cliquez sur **Lancer l’attaque** ou sur **Détails de l’attaque** \> **Lancer l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="094ea-175">In the **Spear Phishing (Credentials Harvest)** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

   - <span data-ttu-id="094ea-176">Dans la section **Harponnage (pièce jointe)**, cliquez sur **Lancer l’attaque** ou sur **Détails de l’attaque** \> **Lancer l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="094ea-176">In the **Spear Phishing (Attachment)** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

3. <span data-ttu-id="094ea-177">L’Assistant **Configurer l’attaque par hameçonnage** démarre dans un nouveau menu volant.</span><span class="sxs-lookup"><span data-stu-id="094ea-177">The **Configure Phishing Attack** wizard starts in a new flyout.</span></span> <span data-ttu-id="094ea-178">À l’étape **Démarrer**, effectuez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="094ea-178">In the **Start** step, do one of the following steps:</span></span>

   - <span data-ttu-id="094ea-179">Dans la zone **Nom**, entrez un nom d’affichage unique pour la campagne.</span><span class="sxs-lookup"><span data-stu-id="094ea-179">In the **Name** box, enter a unique display name for the campaign.</span></span> <span data-ttu-id="094ea-180">Ne pas cliquer sur **Utiliser le modèle**, car vous allez plus tard créer le message électronique dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="094ea-180">Don't click **Use Template**, because you'll create the email message later in the wizard.</span></span>

   - <span data-ttu-id="094ea-181">Cliquez sur **Utiliser le modèle**, puis sélectionnez un modèle de courrier prédéfini ou personnalisé.</span><span class="sxs-lookup"><span data-stu-id="094ea-181">Click **Use Template** and select a built-in or custom email template.</span></span> <span data-ttu-id="094ea-182">Après avoir sélectionné le modèle, la boîte de dialogue **Nom** est automatiquement remplie en fonction du modèle, mais il vous est possible de modifier le nom.</span><span class="sxs-lookup"><span data-stu-id="094ea-182">After you select the template, the **Name** box is automatically filled based on the template, but you can change the name.</span></span>

   ![Page de démarrage du hameçonnage](../../media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)

   <span data-ttu-id="094ea-184">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="094ea-184">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="094ea-185">À l’étape **Destinataires cible**, effectuez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="094ea-185">In the **Target recipients** step, do one of the following steps:</span></span>

   - <span data-ttu-id="094ea-186">Cliquez sur le **Carnet d'adresses** pour sélectionner les destinataires (utilisateurs ou groupes) pour la campagne.</span><span class="sxs-lookup"><span data-stu-id="094ea-186">Click **Address Book** to select the recipients (users or groups) for the campaign.</span></span> <span data-ttu-id="094ea-187">Chaque destinataire ciblé doit avoir une boîte aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="094ea-187">Each targeted recipient must have an Exchange Online mailbox.</span></span> <span data-ttu-id="094ea-188">Si vous cliquez sur **Filtrer** et **Appliquer** sans entrer de critères de recherche, tous les destinataires sont renvoyés et ajoutés à la campagne.</span><span class="sxs-lookup"><span data-stu-id="094ea-188">If you click **Filter** and **Apply** without entering a search criteria, all recipients are returned and added to the campaign.</span></span>

   - <span data-ttu-id="094ea-189">Cliquez sur **Importer**, puis sur **Importation d’un fichier** pour importer un fichier de valeurs séparées par des virgules (CSV) ou d’adresses e-mail séparées par une ligne.</span><span class="sxs-lookup"><span data-stu-id="094ea-189">Click **Import** then **File Import** to import a comma-separated value (CSV) or line-separated file of email addresses.</span></span> <span data-ttu-id="094ea-190">Chaque ligne doit contenir l’adresse e-mail du destinataire.</span><span class="sxs-lookup"><span data-stu-id="094ea-190">Each line must contain the recipient's email address.</span></span>

   <span data-ttu-id="094ea-191">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="094ea-191">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="094ea-192">À l’étape **Configurer les détails du courrier**, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="094ea-192">In the **Configure email details** step, configure the following settings:</span></span>

   <span data-ttu-id="094ea-193">Si vous avez sélectionné un modèle au cours de l’étape **Démarrer**, la plupart de ces valeurs sont déjà configurées, mais vous pouvez les modifier.</span><span class="sxs-lookup"><span data-stu-id="094ea-193">If you selected a template in the **Start** step, most of these values are already configured, but you can change them.</span></span>

   - <span data-ttu-id="094ea-194">**De (nom)**  : le nom d’affichage utilisé en tant qu’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="094ea-194">**From (Name)**: The display name that's used for the message sender.</span></span>

   - <span data-ttu-id="094ea-195">**De (adresse de courrier)**  : l’adresse de courrier de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="094ea-195">**From (Email)**: The sender's email address.</span></span> <span data-ttu-id="094ea-196">Vous pouvez entrer une adresse de messagerie véritable ou fictive à partir du domaine de courrier de votre organisation ou vous pouvez saisir une adresse fausse ou réelle de courrier externe.</span><span class="sxs-lookup"><span data-stu-id="094ea-196">You can enter a real or fake email address from your organization's email domain, or you can enter a real or fake external email address.</span></span> <span data-ttu-id="094ea-197">Une adresse de messagerie d’expéditeur valide de votre organisation prend en réalité la forme du client de courrier du destinataire.</span><span class="sxs-lookup"><span data-stu-id="094ea-197">A valid sender email address from your organization will actually resolve in the recipient's email client.</span></span>

   - <span data-ttu-id="094ea-198">**URL du serveur de connexion d’hameçonnage** : cliquez sur la liste déroulante, puis sélectionnez l’une des URL disponibles dans la liste.</span><span class="sxs-lookup"><span data-stu-id="094ea-198">**Phishing Login Server URL**: Click the drop down and select one of the available URLs from the list.</span></span> <span data-ttu-id="094ea-199">Elle représente l’URL sur laquelle les utilisateurs sont tentés de cliquer.</span><span class="sxs-lookup"><span data-stu-id="094ea-199">This is the URL that users will be tempted to click.</span></span> <span data-ttu-id="094ea-200">Les choix possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="094ea-200">The choices are:</span></span>

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
     >
     > - <span data-ttu-id="094ea-201">Toutes les URL sont intentionnellement HTTP et non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="094ea-201">All of the URLs are intentionally http, not https.</span></span>
     >
     > - <span data-ttu-id="094ea-202">Un service de réputation d’URL peut identifier une ou plusieurs de ces URL comme étant non sécurisées.</span><span class="sxs-lookup"><span data-stu-id="094ea-202">A URL reputation service might identify one or more of these URLs as unsafe.</span></span> <span data-ttu-id="094ea-203">Vérifiez la disponibilité de l’URL dans vos navigateurs web pris en charge avant d’utiliser l’URL dans une campagne d’hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="094ea-203">Check the availability of the URL in your supported web browsers before you use the URL in a phishing campaign.</span></span>
     >
     > - <span data-ttu-id="094ea-204">Vous devez sélectionner une URL.</span><span class="sxs-lookup"><span data-stu-id="094ea-204">You are required to select a URL.</span></span> <span data-ttu-id="094ea-205">Pour les campagnes d’**Harponnage (pièce jointe)**, vous pouvez supprimer le lien du corps du message à l’étape suivante (sinon, le message contient un lien **et** une pièce jointe).</span><span class="sxs-lookup"><span data-stu-id="094ea-205">For **Spear Phishing (Attachment)** campaigns, you can remove the link from the body of the message in the next step (otherwise, the message will contain both a link **and** an attachment).</span></span>

   - <span data-ttu-id="094ea-206">**Type de pièce jointe** : ce paramètre n’est disponible que pour les campagnes de **Harponnage (pièce jointe)**.</span><span class="sxs-lookup"><span data-stu-id="094ea-206">**Attachment Type**: This setting is only available in **Spear Phishing (Attachment)** campaigns.</span></span> <span data-ttu-id="094ea-207">Cliquez sur la liste déroulante, puis sélectionnez **.DOCX** ou **.PDF** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="094ea-207">Click the drop down and select **.DOCX** or **.PDF** from the list.</span></span>

   - <span data-ttu-id="094ea-208">**Nom de pièce jointe** : ce paramètre n’est disponible que pour les campagnes d’**Harponnage (pièce jointe)**.</span><span class="sxs-lookup"><span data-stu-id="094ea-208">**Attachment Name**: This setting is only available in **Spear Phishing (Attachment)** campaigns.</span></span> <span data-ttu-id="094ea-209">Entrez un nom de fichier pour la pièce jointe .docx ou .pdf.</span><span class="sxs-lookup"><span data-stu-id="094ea-209">Enter a filename for the .docx or .pdf attachment.</span></span>

   - <span data-ttu-id="094ea-210">**URL de la page de destination personnalisée** : entrez une page de destination facultative vers laquelle les utilisateurs sont dirigés s’ils cliquent sur le lien d’hameçonnage et entrent leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="094ea-210">**Custom Landing Page URL**: Enter an optional landing page where users are taken if they click the phishing link and enter their credentials.</span></span> <span data-ttu-id="094ea-211">Ce lien remplace la page de destination par défaut.</span><span class="sxs-lookup"><span data-stu-id="094ea-211">This link replaces the default landing page.</span></span> <span data-ttu-id="094ea-212">Par exemple, si vous avez une formation interne de sensibilisation, vous pouvez spécifier cette URL ici.</span><span class="sxs-lookup"><span data-stu-id="094ea-212">For example, if you have internal awareness training, you can specify that URL here.</span></span>

   - <span data-ttu-id="094ea-213">**Objet** : le champ **Objet** du message électronique.</span><span class="sxs-lookup"><span data-stu-id="094ea-213">**Subject**: The **Subject** field of the email message.</span></span>

   <span data-ttu-id="094ea-214">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="094ea-214">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="094ea-215">À l’étape **Composer un message**, créez le corps du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="094ea-215">In the **Compose email** step, create the message body of the email message.</span></span> <span data-ttu-id="094ea-216">Si vous avez sélectionné un modèle au cours de l’étape **Démarrer**, le corps du message est déjà configuré, mais vous pouvez le modifier.</span><span class="sxs-lookup"><span data-stu-id="094ea-216">If you selected a template in the **Start** step, the message body is already configured, but you can customize it.</span></span> <span data-ttu-id="094ea-217">Vous pouvez utiliser l’onglet **Courrier** (éditeur HTML enrichi) ou l’onglet **Source** (code HTML brut).</span><span class="sxs-lookup"><span data-stu-id="094ea-217">You can use the **Email** tab (a rich HTML editor) or the **Source** tab (raw HTML code).</span></span>

   <span data-ttu-id="094ea-218">La mise en forme HTML peut être simple ou complexe, en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="094ea-218">The HTML formatting can be as simple or complex as you need it to be.</span></span> <span data-ttu-id="094ea-219">Vous pouvez insérer des images et du texte pour améliorer la crédibilité du message dans le client de courrier du destinataire.</span><span class="sxs-lookup"><span data-stu-id="094ea-219">You can insert images and text to enhance the believability of the message in the recipient's email client.</span></span>

   - <span data-ttu-id="094ea-220">`${username}` insère le nom du destinataire.</span><span class="sxs-lookup"><span data-stu-id="094ea-220">`${username}` inserts the recipient's name.</span></span>

   - <span data-ttu-id="094ea-221">`${loginserverurl}` insère la valeur de l’**URL du serveur de connexion d’hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="094ea-221">`${loginserverurl}` inserts the **Phishing Login Server URL** value.</span></span>

   <span data-ttu-id="094ea-222">Pour les campagnes d’**Harponnage (pièce jointe)**, il est recommandé de supprimer le lien du corps du message (sinon, le message contient un lien **et** une pièce jointe et les clics sur un lien ne sont pas suivis dans une campagne de pièce jointe).</span><span class="sxs-lookup"><span data-stu-id="094ea-222">For **Spear Phishing (Attachment)** campaigns, you should remove the link from the body of the message (otherwise, the message will contain both a link **and** an attachment, and link clicks aren't tracked in an attachment campaign).</span></span>

   ![Composer un message](../../media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)

   <span data-ttu-id="094ea-224">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="094ea-224">When you're finished, click **Next**.</span></span>

7. <span data-ttu-id="094ea-225">À l’étape **Confirmer**, cliquez sur **Terminer** pour lancer la campagne.</span><span class="sxs-lookup"><span data-stu-id="094ea-225">In the **Confirm** step, click **Finish** to launch the campaign.</span></span> <span data-ttu-id="094ea-226">Le message d’hameçonnage est remis aux destinataires ciblés.</span><span class="sxs-lookup"><span data-stu-id="094ea-226">The phishing message is delivered to the targeted recipients.</span></span>

## <a name="password-attack-campaigns"></a><span data-ttu-id="094ea-227">Campagnes d’attaques de mot de passe</span><span class="sxs-lookup"><span data-stu-id="094ea-227">Password attack campaigns</span></span>

<span data-ttu-id="094ea-228">Une *attaque de mot de passe* tente de deviner les mots de passe des comptes d’utilisateurs au sein d’une organisation, généralement une fois que l’attaquant a identifié un ou plusieurs comptes d’utilisateurs valides.</span><span class="sxs-lookup"><span data-stu-id="094ea-228">A *password attack* tries to guess passwords for user accounts in an organization, typically after the attacker has identified one or more valid user accounts.</span></span>

<span data-ttu-id="094ea-229">Dans le Simulateur d’attaques, deux types différents de campagnes d’attaque de mot de passe sont à votre disposition pour tester la complexité des mots de passe des utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="094ea-229">In Attack Simulator, two different types of password attack campaigns are available for you to test the complexity of your users' passwords:</span></span>

- <span data-ttu-id="094ea-230">**Mot de passe par force brute (attaque par dictionnaire)**  : une attaque par *force brute* ou *dictionnaire* utilise un grand fichier dictionnaire pour les mots de passe d’un compte utilisateur, avec l’espoir que l’un d’entre eux va réussir (de nombreux mots de passe pour un seul compte).</span><span class="sxs-lookup"><span data-stu-id="094ea-230">**Brute force password (dictionary attack)**: A *brute force* or *dictionary* attack uses a large dictionary file of passwords on a user account with the hope that one of them will work (many passwords against one account).</span></span> <span data-ttu-id="094ea-231">Un mot de passe incorrect permet de dissuader les attaques de mot de passe par force brute.</span><span class="sxs-lookup"><span data-stu-id="094ea-231">Incorrect password lock-outs help deter brute force password attacks.</span></span>

  <span data-ttu-id="094ea-232">Pour l’attaque par dictionnaire, vous pouvez spécifier un ou plusieurs mots de passe à tenter (entrés manuellement ou dans un fichier téléchargé), et vous pouvez spécifier un ou plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="094ea-232">For the dictionary attack, you can specify one or many passwords to try (manually entered or in an uploaded file), and you can specify one or many users.</span></span>

- <span data-ttu-id="094ea-233">L’**Attaque par pulvérisation de mots de passe** : une *pulvérisation de mots de passe* utilise le même mot de passe soigneusement étudié contre une liste de comptes d’utilisateurs (un mot de passe pour plusieurs comptes).</span><span class="sxs-lookup"><span data-stu-id="094ea-233">**Password spray attack**: A *password spray* attack uses the same carefully considered password against a list of user accounts (one password against many accounts).</span></span> <span data-ttu-id="094ea-234">Les attaques par pulvérisation de mots de passe sont plus difficiles à détecter que les attaques de mots de passe par force brute (la probabilité de réussite augmente lorsqu’un attaquant essaie un mot de passe sur des dizaines ou des centaines de comptes sans risquer de déclencher le verrouillage du mot de passe incorrect de l’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="094ea-234">Password spray attacks are harder to detect than brute force password attacks (the probability of success increases when an attacker tries one password across dozens or hundreds of accounts without the risk of tripping the user's incorrect password lock-out).</span></span>

  <span data-ttu-id="094ea-235">Pour l’attaque par pulvérisation de mots de passe, vous ne pouvez spécifier qu’un seul mot de passe et vous pouvez préciser un ou plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="094ea-235">For the password spray attack, you can only specify one password to try, and you can specify one or many users.</span></span>

> [!NOTE]
> <span data-ttu-id="094ea-236">Les attaques par mot de passe dans le Simulateur d’attaques transmettent les demandes d’authentification de base par nom d’utilisateur et mot de passe à un point de terminaison. Elles fonctionnent ainsi avec d’autres méthodes d’authentification (AD FS, synchronisation du hachage de mot de passe, directe, PingFederate, etc.).</span><span class="sxs-lookup"><span data-stu-id="094ea-236">The password attacks in Attack Simulator pass username and password Basic auth requests to an endpoint, so they also work with other authentication methods (AD FS, password hash sync, pass-through, PingFederate, etc.).</span></span> <span data-ttu-id="094ea-237">Pour les utilisateurs qui ont activé l’authentification multifacteur, même si l’attaque de mot de passe essaie son propre mot de passe, la tentative s’enregistre toujours en tant qu’échec (en d’autres termes, les utilisateurs de l’authentification multifacteur n’apparaissent jamais dans le nombre de **Tentatives réussies** de la campagne).</span><span class="sxs-lookup"><span data-stu-id="094ea-237">For users that have MFA enabled, even if the password attack tries their actual password, the attempt will always register as a failure (in other words, MFA users will never appear in the **Successful attempts** count of the campaign).</span></span> <span data-ttu-id="094ea-238">Il s'agit du résultat attendu.</span><span class="sxs-lookup"><span data-stu-id="094ea-238">This is the expected result.</span></span> <span data-ttu-id="094ea-239">L’authentification multifacteur est la méthode principale pour permettre de vous protéger contre des attaques par mot de passe.</span><span class="sxs-lookup"><span data-stu-id="094ea-239">MFA is a primary method to help protect against password attacks.</span></span>

### <a name="create-and-launch-a-password-attack-campaign"></a><span data-ttu-id="094ea-240">Création et lancement d’une campagne d’attaque par mot de passe</span><span class="sxs-lookup"><span data-stu-id="094ea-240">Create and launch a password attack campaign</span></span>

1. <span data-ttu-id="094ea-241">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Simulateur d’attaques**.</span><span class="sxs-lookup"><span data-stu-id="094ea-241">In the Security & Compliance Center, go to **Threat management** \> **Attack simulator**.</span></span>

2. <span data-ttu-id="094ea-242">Dans la page **Simulation d’attaques**, effectuez l’une des sélections suivantes en fonction du type de campagne que vous voulez créer :</span><span class="sxs-lookup"><span data-stu-id="094ea-242">On the **Simulate attacks** page, make one of the following selections based on the type of campaign you want to create:</span></span>

   - <span data-ttu-id="094ea-243">Dans la section **Mot de passe par force brute (attaque par dictionnaire)**, cliquez sur **Lancer l’attaque** ou sur **Détails de l’attaque** \> **Lancer l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="094ea-243">In the **Brute Force Password (Dictionary Attack)** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

   - <span data-ttu-id="094ea-244">Dans la section **Attaque par pulvérisation de mots de passe**, cliquez sur **Lancer l’attaque** ou sur **Détails de l’attaque** \> **Lancer l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="094ea-244">in the **Password spray attack** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

3. <span data-ttu-id="094ea-245">L’Assistant **Configurer l’attaque de mot de passe** démarre dans un nouveau menu volant.</span><span class="sxs-lookup"><span data-stu-id="094ea-245">The **Configure Password Attack** wizard starts in a new flyout.</span></span> <span data-ttu-id="094ea-246">À l’étape **Démarrer**, entrez un nom d’affichage unique pour la campagne, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="094ea-246">In the **Start** step, enter a unique display name for the campaign, and then click **Next**.</span></span>

4. <span data-ttu-id="094ea-247">À l’étape **Utilisateurs cible**, effectuez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="094ea-247">In the **Target users** step, do one of the following steps:</span></span>

   - <span data-ttu-id="094ea-248">Cliquez sur le **Carnet d'adresses** pour sélectionner les destinataires (utilisateurs ou groupes) pour la campagne.</span><span class="sxs-lookup"><span data-stu-id="094ea-248">Click **Address Book** to select the recipients (users or groups) for the campaign.</span></span> <span data-ttu-id="094ea-249">Chaque destinataire ciblé doit avoir une boîte aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="094ea-249">Each targeted recipient must have an Exchange Online mailbox.</span></span> <span data-ttu-id="094ea-250">Si vous cliquez sur **Filtrer** et **Appliquer** sans entrer de critères de recherche, tous les destinataires sont renvoyés et ajoutés à la campagne.</span><span class="sxs-lookup"><span data-stu-id="094ea-250">If you click **Filter** and **Apply** without entering a search criteria, all recipients are returned and added to the campaign.</span></span>

   - <span data-ttu-id="094ea-251">Cliquez sur **Importer**, puis sur **Importation d’un fichier** pour importer un fichier de valeurs séparées par des virgules (CSV) ou d’adresses e-mail séparées par une ligne.</span><span class="sxs-lookup"><span data-stu-id="094ea-251">Click **Import** then **File Import** to import a comma-separated value (CSV) or line-separated file of email addresses.</span></span> <span data-ttu-id="094ea-252">Chaque ligne doit contenir l’adresse e-mail du destinataire.</span><span class="sxs-lookup"><span data-stu-id="094ea-252">Each line must contain the recipient's email address.</span></span>

   <span data-ttu-id="094ea-253">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="094ea-253">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="094ea-254">À l’étape **Choix des paramètres de l’attaque**, sélectionnez ce que vous voulez faire en fonction du type de campagne :</span><span class="sxs-lookup"><span data-stu-id="094ea-254">In the **Choose attack settings** step, choose what to do based on the campaign type:</span></span>

   - <span data-ttu-id="094ea-255">**Mot de passe par force brute (attaque par dictionnaire)**  : effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="094ea-255">**Brute Force Password (Dictionary Attack)**: Do either of the following steps:</span></span>

     - <span data-ttu-id="094ea-256">**Entrez les mots de passe manuellement** : dans la boîte de dialogue **Appuyez sur Entrée pour ajouter un mot de passe**, tapez un mot de passe, puis appuyez sur ENTRÉE.</span><span class="sxs-lookup"><span data-stu-id="094ea-256">**Enter passwords manually**: In the **Press enter to add a password** box, type a password and then press ENTER.</span></span> <span data-ttu-id="094ea-257">Répétez cette étape autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="094ea-257">Repeat this step as many times as necessary.</span></span>

     - <span data-ttu-id="094ea-258">**Charger des mots de passe à partir d’un fichier dictionnaire**: cliquez sur **Télécharger** pour importer un fichier texte existant qui contient un mot de passe sur chaque ligne et une dernière ligne vide.</span><span class="sxs-lookup"><span data-stu-id="094ea-258">**Upload passwords from a dictionary file**: Click **Upload** to import an existing text file that contains one password on each line and a blank last line.</span></span> <span data-ttu-id="094ea-259">La taille du fichier texte doit être inférieure ou égale à 10 Mo et ne peut pas contenir plus de 30 000 mots de passe.</span><span class="sxs-lookup"><span data-stu-id="094ea-259">The text file must be 10 MB or less in size, and can't contain more than 30000 passwords.</span></span>

   - <span data-ttu-id="094ea-260">**Attaque par pulvérisation par mots de passe** : entrez un mot de passe dans la zone de dialogue **Le ou les mots de passe à utiliser dans le cadre de l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="094ea-260">**Password spray attack**: In **The password(s) to use in the attack** box, enter one password.</span></span>

   <span data-ttu-id="094ea-261">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="094ea-261">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="094ea-262">À l’étape **Confirmer**, cliquez sur **Terminer** pour lancer la campagne.</span><span class="sxs-lookup"><span data-stu-id="094ea-262">In the **Confirm** step, click **Finish** to launch the campaign.</span></span> <span data-ttu-id="094ea-263">Les mots de passe que vous avez spécifiés ont été essayés pour les utilisateurs que vous avez précisés.</span><span class="sxs-lookup"><span data-stu-id="094ea-263">The passwords you specified are tried on users you specified.</span></span>

## <a name="view-campaign-results"></a><span data-ttu-id="094ea-264">Afficher les résultats de la campagne</span><span class="sxs-lookup"><span data-stu-id="094ea-264">View campaign results</span></span>

<span data-ttu-id="094ea-265">Après avoir lancé une campagne, vous pouvez consulter l’avancement et les résultats sur la page principale **Simulation d’attaques**.</span><span class="sxs-lookup"><span data-stu-id="094ea-265">After you launch a campaign, you can check the progress and results on the main **Simulate attacks** page.</span></span>

<span data-ttu-id="094ea-266">Les campagnes actives affichent une barre de statut, une valeur de pourcentage terminée et un nombre « (utilisateurs terminés) sur (total des utilisateurs) ».</span><span class="sxs-lookup"><span data-stu-id="094ea-266">Active campaigns will show a status bar, a completed percentage value and "(completed users) of (total users)" count.</span></span> <span data-ttu-id="094ea-267">Le fait de cliquer sur le bouton **Actualiser** permet de mettre à jour l’avancement de toutes les campagnes actives.</span><span class="sxs-lookup"><span data-stu-id="094ea-267">Clicking the **Refresh** button will update the progress of any active campaigns.</span></span> <span data-ttu-id="094ea-268">Vous pouvez également cliquer sur **Terminer** pour arrêter une campagne active.</span><span class="sxs-lookup"><span data-stu-id="094ea-268">You can also click **Terminate** to stop an active campaign.</span></span>

<span data-ttu-id="094ea-269">Une fois la campagne terminée, le statut devient **Attaque achevée**.</span><span class="sxs-lookup"><span data-stu-id="094ea-269">When the campaign is finished, the status changes to **Attack completed**.</span></span> <span data-ttu-id="094ea-270">Vous pouvez afficher les résultats de la campagne en effectuant l’une des actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="094ea-270">You can view the results of the campaign by doing either of the following actions:</span></span>

- <span data-ttu-id="094ea-271">Dans la page principale **Simulation d’attaques**, cliquez sur **Afficher le rapport** sous le nom de la campagne.</span><span class="sxs-lookup"><span data-stu-id="094ea-271">On the main **Simulate attacks** page, click **View Report** under the name of the campaign.</span></span>

- <span data-ttu-id="094ea-272">Dans la page principale **Simulation d’attaques**, cliquez sur les **Détails de l’attaque** dans la section correspondant au type d’attaque.</span><span class="sxs-lookup"><span data-stu-id="094ea-272">On the main **Simulate attacks** page, click **Attack Details** in the section for the type of attack.</span></span> <span data-ttu-id="094ea-273">Dans la page **Détails de l’attaque** qui s’ouvre, sélectionnez la campagne dans la section **Historique des attaques**.</span><span class="sxs-lookup"><span data-stu-id="094ea-273">On the **Attack details** page that opens, select the campaign in the **Attack History** section.</span></span>

<span data-ttu-id="094ea-274">L’une des actions précédentes vous dirige vers une page intitulée **Détails de l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="094ea-274">Either of the previous actions will take you to a page named **Attack details**.</span></span> <span data-ttu-id="094ea-275">Les informations disponibles dans cette page pour chaque type de campagne sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="094ea-275">The information that's available on this page for each type of campaign is described in the following sections.</span></span>

### <a name="spear-phishing-credentials-harvest-campaign-results"></a><span data-ttu-id="094ea-276">Résultats de campagne de harponnage (recueil des informations d’identification)</span><span class="sxs-lookup"><span data-stu-id="094ea-276">Spear Phishing (Credentials Harvest) campaign results</span></span>

<span data-ttu-id="094ea-277">Les informations suivantes sont disponibles sur la page des **Détails de l’attaque** pour chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="094ea-277">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="094ea-278">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="094ea-278">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="094ea-279">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="094ea-279">**Total users targeted**</span></span>

- <span data-ttu-id="094ea-280">**Tentatives réussies** : le nombre d’utilisateurs qui ont cliqué sur le lien **et** entré leurs informations d’identification (*toute* valeur de nom d’utilisateur et de mot de passe).</span><span class="sxs-lookup"><span data-stu-id="094ea-280">**Successful attempts**: The number of users who clicked the link **and** entered their credentials (*any* username and password value).</span></span>

- <span data-ttu-id="094ea-281">**Taux de réussite globale** : un pourcentage calculé par **Tentatives réussies** / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="094ea-281">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>

- <span data-ttu-id="094ea-282">**Le plus rapide – Clic** : le temps qu’il a fallu au premier utilisateur pour cliquer sur le lien après le lancement de votre campagne.</span><span class="sxs-lookup"><span data-stu-id="094ea-282">**Fastest Click**: How long it took the first user to click the link after you launched the campaign.</span></span>

- <span data-ttu-id="094ea-283">**Moyenne – Clic** : le temps total qu’il a fallu à tous les utilisateurs pour cliquer sur le lien, divisé par le nombre d’utilisateurs qui ont cliqué sur le lien.</span><span class="sxs-lookup"><span data-stu-id="094ea-283">**Average Click**: The sum of how long it took everyone to click the link divided by the number of users who clicked the link.</span></span>

- <span data-ttu-id="094ea-284">**Taux de réussite – Clic** : un pourcentage calculé par le (nombre d’utilisateurs qui ont cliqué sur le lien) / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="094ea-284">**Click Success Rate**: A percentage that's calculated by (number of users who clicked the link) / **Total users targeted**.</span></span>

- <span data-ttu-id="094ea-285">**Le plus rapide – Informations d’identification** : le temps qu’il a fallu au premier utilisateur pour entrer ses informations d’identification après le lancement de votre campagne.</span><span class="sxs-lookup"><span data-stu-id="094ea-285">**Fastest Credentials**: How long it took the first user to enter their credentials after you launched the campaign.</span></span>

- <span data-ttu-id="094ea-286">**Moyenne – Informations d’identification** : le temps total qu’il a fallu à tous les utilisateurs pour entrer leurs informations d’identification divisé par le nombre d’utilisateurs qui ont entré leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="094ea-286">**Average Credentials**: The sum of how long it took everyone to enter their credentials divided by the number of users who entered their credentials.</span></span>

- <span data-ttu-id="094ea-287">**Taux de réussite – Informations d’identification** : un pourcentage calculé par le (nombre d’utilisateurs qui ont entré leurs informations d’identification) / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="094ea-287">**Credential Success Rate**: A percentage that's calculated by (number of users who entered their credentials) / **Total users targeted**.</span></span>

- <span data-ttu-id="094ea-288">Graphique à barres affichant le **Lien sur lequel un clic a été effectué** et le nombre d’**Informations d’identification fournies** par jour.</span><span class="sxs-lookup"><span data-stu-id="094ea-288">A bar graph that shows the **Link clicked** and **Credential supplied** numbers per day.</span></span>

- <span data-ttu-id="094ea-289">Graphique circulaire affichant les pourcentages **Lien sur lequel un clic a été effectué**, **Informations d’identification fournies**et **Aucun** pour la campagne.</span><span class="sxs-lookup"><span data-stu-id="094ea-289">A circle graph that shows the **Link clicked**, **Credential supplied**, and **None** percentages for the campaign.</span></span>

- <span data-ttu-id="094ea-290">La section **Utilisateurs compromis** répertorie des informations sur les utilisateurs qui ont cliqué sur le lien :</span><span class="sxs-lookup"><span data-stu-id="094ea-290">The **Compromised Users** section lists the details of the users who clicked the link:</span></span>

  - <span data-ttu-id="094ea-291">L’adresse de messagerie de l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="094ea-291">The user's email address</span></span>

  - <span data-ttu-id="094ea-292">Date/heure à laquelle il a cliqué sur le lien.</span><span class="sxs-lookup"><span data-stu-id="094ea-292">The date/time when they clicked the link.</span></span>

  - <span data-ttu-id="094ea-293">L’adresse IP du client.</span><span class="sxs-lookup"><span data-stu-id="094ea-293">The client IP address.</span></span>

  - <span data-ttu-id="094ea-294">Détails sur la version de Windows et le navigateur web de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="094ea-294">Details about the user's version of Windows and web browser.</span></span>

  <span data-ttu-id="094ea-295">Vous pouvez cliquer sur **Exporter** pour exporter les résultats dans un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="094ea-295">You can click **Export** to export the results to a CSV file.</span></span>

### <a name="spear-phishing-attachment-campaign-results"></a><span data-ttu-id="094ea-296">Résultats de la campagne de harponnage (pièce jointe)</span><span class="sxs-lookup"><span data-stu-id="094ea-296">Spear Phishing (Attachment) campaign results</span></span>

<span data-ttu-id="094ea-297">Les informations suivantes sont disponibles sur la page des **Détails de l’attaque** pour chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="094ea-297">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="094ea-298">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="094ea-298">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="094ea-299">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="094ea-299">**Total users targeted**</span></span>

- <span data-ttu-id="094ea-300">**Tentatives réussies** : nombre d’utilisateurs qui ont ouvert ou téléchargé et ouvert la pièce jointe (l’aperçu ne compte pas).</span><span class="sxs-lookup"><span data-stu-id="094ea-300">**Successful attempts**: The number of users who opened or downloaded and opened the attachment (preview doesn't count).</span></span>

- <span data-ttu-id="094ea-301">**Taux de réussite globale** : un pourcentage calculé par **Tentatives réussies** / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="094ea-301">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>

- <span data-ttu-id="094ea-302">**Délai d’ouverture des pièces jointes le plus rapide** : le temps qu’il a fallu au premier utilisateur pour ouvrir la pièce jointe après le lancement de votre campagne.</span><span class="sxs-lookup"><span data-stu-id="094ea-302">**Fastest attachment open time**: How long it took the first user to open the attachment after you launched the campaign.</span></span>

- <span data-ttu-id="094ea-303">**Délai moyen d’ouverture des pièces jointes** : le temps total qu’il a fallu à tous les utilisateurs pour ouvrir la pièce jointe divisé par le nombre de personnes qui ont ouvert la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="094ea-303">**Average attachment open time**: The sum of how long it took everyone to open the attachment divided by the number of users who opened the attachment.</span></span>

- <span data-ttu-id="094ea-304">**Taux d’ouverture réussie des pièces jointes ** : un pourcentage calculé par le (nombre d’utilisateurs qui ont ouvert la pièce jointe) / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="094ea-304">**Attachment open success rate**: A percentage that's calculated by (number of users who opened the attachment) / **Total users targeted**.</span></span>

### <a name="brute-force-password-dictionary-attack-campaign-results"></a><span data-ttu-id="094ea-305">Résultats de la campagne de mot de passe par force brute (attaque par dictionnaire)</span><span class="sxs-lookup"><span data-stu-id="094ea-305">Brute Force Password (Dictionary Attack) campaign results</span></span>

<span data-ttu-id="094ea-306">Les informations suivantes sont disponibles sur la page des **Détails de l’attaque** pour chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="094ea-306">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="094ea-307">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="094ea-307">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="094ea-308">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="094ea-308">**Total users targeted**</span></span>

- <span data-ttu-id="094ea-309">**Tentatives réussies** : nombre d’utilisateurs qui se sont avérées utiliser l’un des mots de passe spécifiés.</span><span class="sxs-lookup"><span data-stu-id="094ea-309">**Successful attempts**: The number of users who were found to be using one of the specified passwords.</span></span>

- <span data-ttu-id="094ea-310">**Taux de réussite globale** : un pourcentage calculé par **Tentatives réussies** / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="094ea-310">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>

- <span data-ttu-id="094ea-311">La section **Utilisateurs compromis** répertorie les adresses de courrier des utilisateurs concernés.</span><span class="sxs-lookup"><span data-stu-id="094ea-311">The **Compromised Users** section lists the email addresses of the affected users.</span></span> <span data-ttu-id="094ea-312">Vous pouvez cliquer sur **Exporter** pour exporter les résultats dans un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="094ea-312">You can click **Export** to export the results to a CSV file.</span></span>

### <a name="password-spray-attack-campaign-results"></a><span data-ttu-id="094ea-313">Résultats de la campagne d’attaque par pulvérisation par mots de passe</span><span class="sxs-lookup"><span data-stu-id="094ea-313">Password spray attack campaign results</span></span>

<span data-ttu-id="094ea-314">Les informations suivantes sont disponibles sur la page des **Détails de l’attaque** pour chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="094ea-314">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="094ea-315">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="094ea-315">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="094ea-316">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="094ea-316">**Total users targeted**</span></span>

- <span data-ttu-id="094ea-317">**Tentatives réussies** : nombre d’utilisateurs qui se sont avérées utiliser le mot de passe spécifié.</span><span class="sxs-lookup"><span data-stu-id="094ea-317">**Successful attempts**: The number of users who were found to be using the specified password.</span></span>

- <span data-ttu-id="094ea-318">**Taux de réussite globale** : un pourcentage calculé par **Tentatives réussies** / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="094ea-318">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>
