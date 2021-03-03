---
title: Simulateur d’attaques dans Microsoft Defender pour Office 365
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: how-to
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à utiliser le Simulateur d’attaques pour exécuter des attaques par hameçonnage et par mot de passe simulés dans leurs organisations Microsoft 365 E5 ou Microsoft Defender pour Office 365 Plan 2.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 85b376701ffa0c567fd66aa629371e9f69b354e9
ms.sourcegitcommit: 070724118be25cd83418d2a56863da95582dae65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "50407470"
---
# <a name="attack-simulator-in-microsoft-defender-for-office-365"></a><span data-ttu-id="8112a-103">Simulateur d’attaques dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="8112a-103">Attack Simulator in Microsoft Defender for Office 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="8112a-104">**S’applique** [à Microsoft Defender pour Office 365 plan 2](office-365-atp.md)</span><span class="sxs-lookup"><span data-stu-id="8112a-104">**Applies to** [Microsoft Defender for Office 365 plan 2](office-365-atp.md)</span></span>

<span data-ttu-id="8112a-105">Si votre organisation dispose de Microsoft Defender pour Office [](office-365-ti.md)365 Plan 2, qui inclut des fonctionnalités d’investigation et de réponse aux menaces, vous pouvez utiliser le Simulateur d’attaques dans le Centre de sécurité & conformité pour exécuter des scénarios d’attaque réalistes dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8112a-105">If your organization has Microsoft Defender for Office 365 Plan 2, which includes [Threat Investigation and Response capabilities](office-365-ti.md), you can use Attack Simulator in the Security & Compliance Center to run realistic attack scenarios in your organization.</span></span> <span data-ttu-id="8112a-106">Ces attaques simulées peuvent vous aider à identifier et à trouver des utilisateurs vulnérables avant qu’une attaque réelle n’impacte votre ligne de bas de page.</span><span class="sxs-lookup"><span data-stu-id="8112a-106">These simulated attacks can help you identify and find vulnerable users before a real attack impacts your bottom line.</span></span> <span data-ttu-id="8112a-107">Pour en savoir plus, lisez cet article.</span><span class="sxs-lookup"><span data-stu-id="8112a-107">Read this article to learn more.</span></span>

> [!NOTE]
> <span data-ttu-id="8112a-108">L’expérience du Simulateur d’attaques v1 a été basculée en mode lecture seule et remplacée par une formation au simulateur d’attaques décrite dans La formation à la [simulation d’attaques.](attack-simulation-training-get-started.md)</span><span class="sxs-lookup"><span data-stu-id="8112a-108">Attack Simulator v1 experience has been switched to read-only mode and replaced by Attack simulator training that's described in [Get started using Attack simulation training](attack-simulation-training-get-started.md).</span></span>
> <span data-ttu-id="8112a-109">La possibilité de lancer de nouvelles simulations à partir de ce site a été désactivée.</span><span class="sxs-lookup"><span data-stu-id="8112a-109">The ability to launch new simulations from this site has been disabled.</span></span> <span data-ttu-id="8112a-110">Toutefois, vous pouvez toujours accéder aux rapports pour les simulations qui s’exécutent pendant une période de 90 jours à partir du 24 janvier 2021.</span><span class="sxs-lookup"><span data-stu-id="8112a-110">However, you can still access reports for simulations run for a period of 90 days from January 24, 2021.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="8112a-111">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="8112a-111">What do you need to know before you begin?</span></span>

- <span data-ttu-id="8112a-112">Pour ouvrir le Centre de conformité et sécurité, consultez <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="8112a-112">To open the Security & Compliance Center, go to <https://protection.office.com/>.</span></span> <span data-ttu-id="8112a-113">Le Simulateur d’attaques est disponible dans **Gestion des menaces** \> **Simulateur d’attaques**.</span><span class="sxs-lookup"><span data-stu-id="8112a-113">Attack simulator is available at **Threat management** \> **Attack simulator**.</span></span> <span data-ttu-id="8112a-114">Go go directly to attack simulator, open <https://protection.office.com/attacksimulator> .</span><span class="sxs-lookup"><span data-stu-id="8112a-114">Go go directly to attack simulator, open <https://protection.office.com/attacksimulator>.</span></span>

- <span data-ttu-id="8112a-115">Pour plus d’informations sur la disponibilité du Simulateur d’attaques dans différents abonnements Microsoft 365, voir la description du service Microsoft Defender pour [Office 365.](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)</span><span class="sxs-lookup"><span data-stu-id="8112a-115">For more information about the availability of Attack Simulator across different Microsoft 365 subscriptions, see [Microsoft Defender for Office 365 service description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>

- <span data-ttu-id="8112a-116">Vous devez être membre des groupes de rôles **Management de l’organisation** ou **Administrateur de sécurité**.</span><span class="sxs-lookup"><span data-stu-id="8112a-116">You need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span> <span data-ttu-id="8112a-117">Pour des informations supplémentaires sur les groupes de rôles dans le Centre de sécurité et conformité, voir [Autorisations dans le Centre de sécurité et conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="8112a-117">For more information about role groups in the Security & Compliance Center, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="8112a-118">Votre compte doit être configuré pour l’authentification multifacteur (MFA) afin que vous puissiez créer et gérer des campagnes dans le Simulateur d’attaques.</span><span class="sxs-lookup"><span data-stu-id="8112a-118">Your account needs to be configured for multi-factor authentication (MFA) to create and manage campaigns in Attack Simulator.</span></span> <span data-ttu-id="8112a-119">Pour consulter des instructions, voir [Configurer Multi-factor Authentification (MFA)](../../admin/security-and-compliance/set-up-multi-factor-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="8112a-119">For instructions, see [Set up multi-factor authentication](../../admin/security-and-compliance/set-up-multi-factor-authentication.md).</span></span>

- <span data-ttu-id="8112a-120">Le Simulateur d’attaques fonctionne uniquement sur les boîtes aux lettres en nuage.</span><span class="sxs-lookup"><span data-stu-id="8112a-120">Attack Simulator only works on cloud-based mailboxes.</span></span>

- <span data-ttu-id="8112a-121">Les campagnes d’hameçonnage collectent et traitent des événements sur une durée de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="8112a-121">Phishing campaigns will collect and process events for 30 days.</span></span> <span data-ttu-id="8112a-122">L’historique des données de la campagne est disponible pendant un maximum de 90 jours après le lancement de la campagne.</span><span class="sxs-lookup"><span data-stu-id="8112a-122">Historical campaign data will be available for up to 90 days after you launch the campaign.</span></span>

- <span data-ttu-id="8112a-123">Les données associées à la simulation d’attaque et à la formation sont stockées avec d’autres données client pour les services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8112a-123">Attack simulation and training related data is stored with other customer data for Microsoft 365 services.</span></span> <span data-ttu-id="8112a-124">Pour plus d’informations, voir emplacements de données [Microsoft 365.](/microsoft-365/enterprise/o365-data-locations)</span><span class="sxs-lookup"><span data-stu-id="8112a-124">For more information see [Microsoft 365 data locations](/microsoft-365/enterprise/o365-data-locations).</span></span>

- <span data-ttu-id="8112a-125">Il n’existe pas d’applet de commande PowerShell correspondante pour le Simulateur d’attaques.</span><span class="sxs-lookup"><span data-stu-id="8112a-125">There are no corresponding PowerShell cmdlets for Attack Simulator.</span></span>

## <a name="spear-phishing-campaigns"></a><span data-ttu-id="8112a-126">Campagnes de Harponnage</span><span class="sxs-lookup"><span data-stu-id="8112a-126">Spear phishing campaigns</span></span>

<span data-ttu-id="8112a-127">Le *Hameçonnage* est un terme générique qui décrit les attaques par courrier électronique tentant d’accéder à des informations sensibles par le biais de messages qui paraissent provenir d’expéditeurs légitimes ou approuvés.</span><span class="sxs-lookup"><span data-stu-id="8112a-127">*Phishing* is a generic term for email attacks that try to steal sensitive information in messages that appear to be from legitimate or trusted senders.</span></span> <span data-ttu-id="8112a-128">*Le harponnage* est une attaque ciblée par hameçonnage qui utilise du contenu ciblé et personnalisé spécifiquement adapté aux destinataires ciblés (généralement, après la reconnaissance des destinataires par l’attaquant).</span><span class="sxs-lookup"><span data-stu-id="8112a-128">*Spear phishing* is a targeted phishing attack that uses focused and customized content that's specifically tailored to the targeted recipients (typically, after reconnaissance on the recipients by the attacker).</span></span>

<span data-ttu-id="8112a-129">Dans le Simulateur d’attaques, deux types différents de campagnes de harponnage sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="8112a-129">In Attack Simulator, two different types of spear phishing campaigns are available:</span></span>

- <span data-ttu-id="8112a-130">**Harponnage (données d’identification)**: l’attaque tente de convaincre les destinataires de cliquer sur une URL dans le message.</span><span class="sxs-lookup"><span data-stu-id="8112a-130">**Spear phishing (credentials harvest)**: The attack tries to convince the recipients to click a URL in the message.</span></span> <span data-ttu-id="8112a-131">S’ils cliquent sur le lien, ils sont invités à entrer leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="8112a-131">If they click the link, they're asked to enter their credentials.</span></span> <span data-ttu-id="8112a-132">Si c’est le cas, ils sont conduits à l’un des emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="8112a-132">If they do, they're taken to one of the following locations:</span></span>

  - <span data-ttu-id="8112a-133">Page par défaut qui explique qu’il s’agit d’un simple test et donne des conseils pour reconnaître les messages d’hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="8112a-133">A default page that explains that this was a just a test, and gives tips for recognizing phishing messages.</span></span>

    ![Ce que l’utilisateur voit s’il clique sur le lien de hameçonnage, puis entre ses informations d’identification](../../media/attack-simulator-phishing-result.png)

  - <span data-ttu-id="8112a-135">Une page personnalisée (URL) que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="8112a-135">A custom page (URL) that you specify.</span></span>

- <span data-ttu-id="8112a-136">**Harponnage (pièce jointe)**  : l’attaque tente de convaincre le destinataire d’ouvrir une pièce jointe .docx ou .pdf contenue dans le message.</span><span class="sxs-lookup"><span data-stu-id="8112a-136">**Spear phishing (attachment)**: The attack tries to convince the recipients to open a .docx or .pdf attachment in the message.</span></span> <span data-ttu-id="8112a-137">La pièce jointe contient le même contenu à partir du lien de hameçonnage par défaut, mais la première phrase commence par « , vous voyez ce message comme un message électronique récent que vous avez \<Display Name\> ouvert... ».</span><span class="sxs-lookup"><span data-stu-id="8112a-137">The attachment contains the same content from the default phishing link, but the first sentence starts with "\<Display Name\>, you are seeing this message as a recent email message you opened...".</span></span>

> [!NOTE]
> <span data-ttu-id="8112a-138">Les campagnes de harponnage dans le Simulateur d’attaques n’arrivent pas à expiration pour le moment.</span><span class="sxs-lookup"><span data-stu-id="8112a-138">Currently, spear phishing campaigns in Attack Simulator don't expire.</span></span>

### <a name="create-a-spear-phishing-campaign"></a><span data-ttu-id="8112a-139">Création d’une campagne de harponnage</span><span class="sxs-lookup"><span data-stu-id="8112a-139">Create a spear phishing campaign</span></span>

<span data-ttu-id="8112a-140">L’apparence du message électronique envoyé aux destinataires ciblés est un élément important dans toute campagne de harponnage.</span><span class="sxs-lookup"><span data-stu-id="8112a-140">An important part of any spear phishing campaign is the look and feel of the email message that's sent to the targeted recipients.</span></span> <span data-ttu-id="8112a-141">Pour créer et configurer le courrier électronique, vous disposez des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="8112a-141">To create and configure the email message, you have these options:</span></span>

- <span data-ttu-id="8112a-142">**Utiliser un modèle d’e-mail intégré** : deux modèles prédéfinis sont disponibles : **Concours avec de nombreux prix à remporter** et **Mise à jour des données de paie**.</span><span class="sxs-lookup"><span data-stu-id="8112a-142">**Use a built-in email template**: Two built-in templates are available: **Prize Giveaway** and **Payroll Update**.</span></span> <span data-ttu-id="8112a-143">Vous pouvez personnaliser certaines, toutes ou aucune des propriétés de courrier à partir du modèle lorsque vous créez et lancez la campagne.</span><span class="sxs-lookup"><span data-stu-id="8112a-143">You can further customize some, all, or none of the email properties from the template when you create and launch the campaign.</span></span>

- <span data-ttu-id="8112a-144">**Créer un modèle d’e-mail réutilisable** : après la création et l’enregistrement du modèle de courrier, vous pouvez le réutiliser pour de prochaines campagnes de harponnage.</span><span class="sxs-lookup"><span data-stu-id="8112a-144">**Create a reusable email template**: After you create and save the email template, you can use it again in future spear phishing campaigns.</span></span> <span data-ttu-id="8112a-145">Vous pouvez personnaliser certaines, toutes ou aucune des propriétés de courrier à partir du modèle lorsque vous créez et lancez la campagne.</span><span class="sxs-lookup"><span data-stu-id="8112a-145">You can further customize some, all, or none of the email properties from the template when you create and launch the campaign.</span></span>

- <span data-ttu-id="8112a-146">**Créer le message électronique dans l’Assistant** : vous pouvez directement créer le message électronique dans l’Assistant lors de la création et du lancement de la campagne de harponnage.</span><span class="sxs-lookup"><span data-stu-id="8112a-146">**Create the email message in the wizard**: You can create the email message directly in the wizard as you create and launch the spear phishing campaign.</span></span>

#### <a name="step-1-optional-create-a-custom-email-template"></a><span data-ttu-id="8112a-147">Étape 1 (facultatif) : création d’un modèle d’e-mail personnalisé</span><span class="sxs-lookup"><span data-stu-id="8112a-147">Step 1 (Optional): Create a custom email template</span></span>

<span data-ttu-id="8112a-148">Si vous allez utiliser l’un des modèles intégrés ou créer le message directement dans l’Assistant, vous pouvez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="8112a-148">If you're going to use one of the built-in templates or create the email message directly in the wizard, you can skip this step.</span></span>

1. <span data-ttu-id="8112a-149">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Simulateur d’attaques**.</span><span class="sxs-lookup"><span data-stu-id="8112a-149">In the Security & Compliance Center, go to **Threat management** \> **Attack simulator**.</span></span>

2. <span data-ttu-id="8112a-150">Sur la page **Simulation d’attaques**, dans les sections **Harponnage (recueil des informations d’identification)** ou **Harponnage (pièce jointe)**, cliquez sur **Détails de l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="8112a-150">On the **Simulate attacks** page, in either the **Spear Phishing (Credentials Harvest)** or **Spear Phishing (Attachment)** sections, click **Attack Details**.</span></span>

   <span data-ttu-id="8112a-151">Peu importe l’emplacement où vous créez le modèle.</span><span class="sxs-lookup"><span data-stu-id="8112a-151">It doesn't matter where you create the template.</span></span> <span data-ttu-id="8112a-152">Les options disponibles dans le modèle sont identiques pour les deux types d’attaques par hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="8112a-152">The available options in the template are the same for both types of phishing attacks.</span></span>

3. <span data-ttu-id="8112a-153">Dans la page des **Détails de l’attaque** qui s’ouvre, dans la section **Modèles d’hameçonnage** de la zone **Créer des modèles**, cliquez sur **Nouveau modèle**.</span><span class="sxs-lookup"><span data-stu-id="8112a-153">In the **Attack details** page that opens, in the **Phishing Templates** section, in the **Create Templates** area, click **New Template**.</span></span>

4. <span data-ttu-id="8112a-154">L’Assistant **Configurer le modèle d’hameçonnage** démarre dans un nouveau menu volant.</span><span class="sxs-lookup"><span data-stu-id="8112a-154">The **Configure Phishing Template** wizard starts in a new flyout.</span></span> <span data-ttu-id="8112a-155">À l’étape **Démarrer**, entrez un nom d’affichage unique pour le modèle, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="8112a-155">In the **Start** step, enter a unique display name for the template, and then click **Next**.</span></span>

5. <span data-ttu-id="8112a-156">À l’étape **Configurer les détails du courrier**, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8112a-156">In the **Configure email details** step, configure the following settings:</span></span>

   - <span data-ttu-id="8112a-157">**De (nom)**  : le nom d’affichage utilisé en tant qu’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="8112a-157">**From (Name)**: The display name that's used for the message sender.</span></span>

   - <span data-ttu-id="8112a-158">**De (adresse de courrier)**  : l’adresse de courrier de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="8112a-158">**From (Email)**: The sender's email address.</span></span>

   - <span data-ttu-id="8112a-159">**URL du serveur de connexion d’hameçonnage** : cliquez sur la liste déroulante, puis sélectionnez l’une des URL disponibles dans la liste.</span><span class="sxs-lookup"><span data-stu-id="8112a-159">**Phishing Login Server URL**: Click the drop down and select one of the available URLs from the list.</span></span> <span data-ttu-id="8112a-160">Elle représente l’URL sur laquelle les utilisateurs sont tentés de cliquer.</span><span class="sxs-lookup"><span data-stu-id="8112a-160">This is the URL that users will be tempted to click.</span></span> <span data-ttu-id="8112a-161">Les choix possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="8112a-161">The choices are:</span></span>

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
     > <span data-ttu-id="8112a-162">Un service de réputation d’URL peut identifier une ou plusieurs de ces URL comme étant non sécurisées.</span><span class="sxs-lookup"><span data-stu-id="8112a-162">A URL reputation service might identify one or more of these URLs as unsafe.</span></span> <span data-ttu-id="8112a-163">Vérifiez la disponibilité de l’URL dans vos navigateurs web pris en charge avant d’utiliser l’URL dans une campagne d’hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="8112a-163">Check the availability of the URL in your supported web browsers before you use the URL in a phishing campaign.</span></span>

   - <span data-ttu-id="8112a-164">**URL de la page de destination personnalisée** : entrez une page de destination facultative vers laquelle les utilisateurs sont dirigés s’ils cliquent sur le lien d’hameçonnage et entrent leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="8112a-164">**Custom Landing Page URL**: Enter an optional landing page where users are taken if they click the phishing link and enter their credentials.</span></span> <span data-ttu-id="8112a-165">Ce lien remplace la page de destination par défaut.</span><span class="sxs-lookup"><span data-stu-id="8112a-165">This link replaces the default landing page.</span></span> <span data-ttu-id="8112a-166">Par exemple, si vous avez une formation interne de sensibilisation, vous pouvez spécifier cette URL ici.</span><span class="sxs-lookup"><span data-stu-id="8112a-166">For example, if you have internal awareness training, you can specify that URL here.</span></span>

   - <span data-ttu-id="8112a-167">**Catégorie** : ce paramètre n’est à ce jour pas utilisé (ce que vous entrez n’est pas pris en compte).</span><span class="sxs-lookup"><span data-stu-id="8112a-167">**Category**: Currently, this setting isn't used (anything you enter is ignored).</span></span>

   - <span data-ttu-id="8112a-168">**Objet** : le champ **Objet** du message électronique.</span><span class="sxs-lookup"><span data-stu-id="8112a-168">**Subject**: The **Subject** field of the email message.</span></span>

   <span data-ttu-id="8112a-169">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="8112a-169">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="8112a-170">À l’étape **Composer un message**, créez le corps du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="8112a-170">In the **Compose email** step, create the message body of the email message.</span></span> <span data-ttu-id="8112a-171">Vous pouvez utiliser l’onglet **Courrier** (éditeur HTML enrichi) ou l’onglet **Source** (code HTML brut).</span><span class="sxs-lookup"><span data-stu-id="8112a-171">You can use the **Email** tab (a rich HTML editor) or the **Source** tab (raw HTML code).</span></span>

   <span data-ttu-id="8112a-172">La mise en forme HTML peut être simple ou complexe, en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="8112a-172">The HTML formatting can be as simple or complex as you need it to be.</span></span> <span data-ttu-id="8112a-173">Vous pouvez insérer des images et du texte pour améliorer la crédibilité du message dans le client de courrier du destinataire.</span><span class="sxs-lookup"><span data-stu-id="8112a-173">You can insert images and text to enhance the believability of the message in the recipient's email client.</span></span>

   - <span data-ttu-id="8112a-174">`${username}` insère le nom du destinataire.</span><span class="sxs-lookup"><span data-stu-id="8112a-174">`${username}` inserts the recipient's name.</span></span>

   - <span data-ttu-id="8112a-175">`${loginserverurl}` insère l’**URL du serveur de connexion d’hameçonnage** de l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="8112a-175">`${loginserverurl}` inserts the **Phishing Login Server URL** value from the previous step.</span></span>

   <span data-ttu-id="8112a-176">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="8112a-176">When you're finished, click **Next**.</span></span>

7. <span data-ttu-id="8112a-177">À l’étape **Confirmer**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="8112a-177">In the **Confirm** step, click **Finish**.</span></span>

#### <a name="step-2-create-and-launch-the-spear-phishing-campaign"></a><span data-ttu-id="8112a-178">Étape 2 : création et lancement d’une campagne de harponnage</span><span class="sxs-lookup"><span data-stu-id="8112a-178">Step 2: Create and launch the spear phishing campaign</span></span>

1. <span data-ttu-id="8112a-179">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Simulateur d’attaques**.</span><span class="sxs-lookup"><span data-stu-id="8112a-179">In the Security & Compliance Center, go to **Threat management** \> **Attack simulator**.</span></span>

2. <span data-ttu-id="8112a-180">Dans la page **Simulation d’attaques**, effectuez l’une des sélections suivantes en fonction du type de campagne que vous voulez créer :</span><span class="sxs-lookup"><span data-stu-id="8112a-180">On the **Simulate attacks** page, make one of the following selections based on the type of campaign you want to create:</span></span>

   - <span data-ttu-id="8112a-181">Dans la section **Harponnage (recueil des informations d’identification)**, cliquez sur **Lancer l’attaque** ou sur **Détails de l’attaque** \> **Lancer l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="8112a-181">In the **Spear Phishing (Credentials Harvest)** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

   - <span data-ttu-id="8112a-182">Dans la section **Harponnage (pièce jointe)**, cliquez sur **Lancer l’attaque** ou sur **Détails de l’attaque** \> **Lancer l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="8112a-182">In the **Spear Phishing (Attachment)** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

3. <span data-ttu-id="8112a-183">L’Assistant **Configurer l’attaque par hameçonnage** démarre dans un nouveau menu volant.</span><span class="sxs-lookup"><span data-stu-id="8112a-183">The **Configure Phishing Attack** wizard starts in a new flyout.</span></span> <span data-ttu-id="8112a-184">À l’étape **Démarrer**, effectuez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8112a-184">In the **Start** step, do one of the following steps:</span></span>

   - <span data-ttu-id="8112a-185">Dans la zone **Nom**, entrez un nom d’affichage unique pour la campagne.</span><span class="sxs-lookup"><span data-stu-id="8112a-185">In the **Name** box, enter a unique display name for the campaign.</span></span> <span data-ttu-id="8112a-186">Ne pas cliquer sur **Utiliser le modèle**, car vous allez plus tard créer le message électronique dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="8112a-186">Don't click **Use Template**, because you'll create the email message later in the wizard.</span></span>

   - <span data-ttu-id="8112a-187">Cliquez sur **Utiliser le modèle**, puis sélectionnez un modèle de courrier prédéfini ou personnalisé.</span><span class="sxs-lookup"><span data-stu-id="8112a-187">Click **Use Template** and select a built-in or custom email template.</span></span> <span data-ttu-id="8112a-188">Après avoir sélectionné le modèle, la boîte de dialogue **Nom** est automatiquement remplie en fonction du modèle, mais il vous est possible de modifier le nom.</span><span class="sxs-lookup"><span data-stu-id="8112a-188">After you select the template, the **Name** box is automatically filled based on the template, but you can change the name.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="8112a-189">![Page de démarrage du hameçonnage](../../media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)</span><span class="sxs-lookup"><span data-stu-id="8112a-189">![Phishing Start Page](../../media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)</span></span>

   <span data-ttu-id="8112a-190">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="8112a-190">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="8112a-191">À l’étape **Destinataires cible**, effectuez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8112a-191">In the **Target recipients** step, do one of the following steps:</span></span>

   - <span data-ttu-id="8112a-192">Cliquez sur le **Carnet d'adresses** pour sélectionner les destinataires (utilisateurs ou groupes) pour la campagne.</span><span class="sxs-lookup"><span data-stu-id="8112a-192">Click **Address Book** to select the recipients (users or groups) for the campaign.</span></span> <span data-ttu-id="8112a-193">Chaque destinataire ciblé doit avoir une boîte aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="8112a-193">Each targeted recipient must have an Exchange Online mailbox.</span></span> <span data-ttu-id="8112a-194">Si vous cliquez sur **Filtrer** et **Appliquer** sans entrer de critères de recherche, tous les destinataires sont renvoyés et ajoutés à la campagne.</span><span class="sxs-lookup"><span data-stu-id="8112a-194">If you click **Filter** and **Apply** without entering a search criteria, all recipients are returned and added to the campaign.</span></span>

   - <span data-ttu-id="8112a-195">Cliquez sur **Importer**, puis sur **Importation d’un fichier** pour importer un fichier de valeurs séparées par des virgules (CSV) ou d’adresses e-mail séparées par une ligne.</span><span class="sxs-lookup"><span data-stu-id="8112a-195">Click **Import** then **File Import** to import a comma-separated value (CSV) or line-separated file of email addresses.</span></span> <span data-ttu-id="8112a-196">Chaque ligne doit contenir l’adresse e-mail du destinataire.</span><span class="sxs-lookup"><span data-stu-id="8112a-196">Each line must contain the recipient's email address.</span></span>

   <span data-ttu-id="8112a-197">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="8112a-197">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="8112a-198">À l’étape **Configurer les détails du courrier**, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8112a-198">In the **Configure email details** step, configure the following settings:</span></span>

   <span data-ttu-id="8112a-199">Si vous avez sélectionné un modèle au cours de l’étape **Démarrer**, la plupart de ces valeurs sont déjà configurées, mais vous pouvez les modifier.</span><span class="sxs-lookup"><span data-stu-id="8112a-199">If you selected a template in the **Start** step, most of these values are already configured, but you can change them.</span></span>

   - <span data-ttu-id="8112a-200">**De (nom)**  : le nom d’affichage utilisé en tant qu’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="8112a-200">**From (Name)**: The display name that's used for the message sender.</span></span>

   - <span data-ttu-id="8112a-201">**De (adresse de courrier)**  : l’adresse de courrier de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="8112a-201">**From (Email)**: The sender's email address.</span></span> <span data-ttu-id="8112a-202">Vous pouvez entrer une adresse de messagerie véritable ou fictive à partir du domaine de courrier de votre organisation ou vous pouvez saisir une adresse fausse ou réelle de courrier externe.</span><span class="sxs-lookup"><span data-stu-id="8112a-202">You can enter a real or fake email address from your organization's email domain, or you can enter a real or fake external email address.</span></span> <span data-ttu-id="8112a-203">Une adresse de messagerie d’expéditeur valide de votre organisation prend en réalité la forme du client de courrier du destinataire.</span><span class="sxs-lookup"><span data-stu-id="8112a-203">A valid sender email address from your organization will actually resolve in the recipient's email client.</span></span>

   - <span data-ttu-id="8112a-204">**URL du serveur de connexion d’hameçonnage** : cliquez sur la liste déroulante, puis sélectionnez l’une des URL disponibles dans la liste.</span><span class="sxs-lookup"><span data-stu-id="8112a-204">**Phishing Login Server URL**: Click the drop down and select one of the available URLs from the list.</span></span> <span data-ttu-id="8112a-205">Elle représente l’URL sur laquelle les utilisateurs sont tentés de cliquer.</span><span class="sxs-lookup"><span data-stu-id="8112a-205">This is the URL that users will be tempted to click.</span></span> <span data-ttu-id="8112a-206">Les choix possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="8112a-206">The choices are:</span></span>

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
     > - <span data-ttu-id="8112a-207">Toutes les URL sont intentionnellement HTTP et non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="8112a-207">All of the URLs are intentionally http, not https.</span></span>
     >
     > - <span data-ttu-id="8112a-208">Un service de réputation d’URL peut identifier une ou plusieurs de ces URL comme étant non sécurisées.</span><span class="sxs-lookup"><span data-stu-id="8112a-208">A URL reputation service might identify one or more of these URLs as unsafe.</span></span> <span data-ttu-id="8112a-209">Vérifiez la disponibilité de l’URL dans vos navigateurs web pris en charge avant d’utiliser l’URL dans une campagne d’hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="8112a-209">Check the availability of the URL in your supported web browsers before you use the URL in a phishing campaign.</span></span>
     >
     > - <span data-ttu-id="8112a-210">Vous devez sélectionner une URL.</span><span class="sxs-lookup"><span data-stu-id="8112a-210">You are required to select a URL.</span></span> <span data-ttu-id="8112a-211">Pour les campagnes d’**Harponnage (pièce jointe)**, vous pouvez supprimer le lien du corps du message à l’étape suivante (sinon, le message contient un lien **et** une pièce jointe).</span><span class="sxs-lookup"><span data-stu-id="8112a-211">For **Spear Phishing (Attachment)** campaigns, you can remove the link from the body of the message in the next step (otherwise, the message will contain both a link **and** an attachment).</span></span>

   - <span data-ttu-id="8112a-212">**Type de pièce jointe** : ce paramètre n’est disponible que pour les campagnes de **Harponnage (pièce jointe)**.</span><span class="sxs-lookup"><span data-stu-id="8112a-212">**Attachment Type**: This setting is only available in **Spear Phishing (Attachment)** campaigns.</span></span> <span data-ttu-id="8112a-213">Cliquez sur la liste déroulante, puis sélectionnez **.DOCX** ou **.PDF** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="8112a-213">Click the drop down and select **.DOCX** or **.PDF** from the list.</span></span>

   - <span data-ttu-id="8112a-214">**Nom de pièce jointe** : ce paramètre n’est disponible que pour les campagnes d’**Harponnage (pièce jointe)**.</span><span class="sxs-lookup"><span data-stu-id="8112a-214">**Attachment Name**: This setting is only available in **Spear Phishing (Attachment)** campaigns.</span></span> <span data-ttu-id="8112a-215">Entrez un nom de fichier pour la pièce jointe .docx ou .pdf.</span><span class="sxs-lookup"><span data-stu-id="8112a-215">Enter a filename for the .docx or .pdf attachment.</span></span>

   - <span data-ttu-id="8112a-216">**URL de la page de destination personnalisée** : entrez une page de destination facultative vers laquelle les utilisateurs sont dirigés s’ils cliquent sur le lien d’hameçonnage et entrent leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="8112a-216">**Custom Landing Page URL**: Enter an optional landing page where users are taken if they click the phishing link and enter their credentials.</span></span> <span data-ttu-id="8112a-217">Ce lien remplace la page de destination par défaut.</span><span class="sxs-lookup"><span data-stu-id="8112a-217">This link replaces the default landing page.</span></span> <span data-ttu-id="8112a-218">Par exemple, si vous avez une formation interne de sensibilisation, vous pouvez spécifier cette URL ici.</span><span class="sxs-lookup"><span data-stu-id="8112a-218">For example, if you have internal awareness training, you can specify that URL here.</span></span>

   - <span data-ttu-id="8112a-219">**Objet** : le champ **Objet** du message électronique.</span><span class="sxs-lookup"><span data-stu-id="8112a-219">**Subject**: The **Subject** field of the email message.</span></span>

   <span data-ttu-id="8112a-220">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="8112a-220">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="8112a-221">À l’étape **Composer un message**, créez le corps du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="8112a-221">In the **Compose email** step, create the message body of the email message.</span></span> <span data-ttu-id="8112a-222">Si vous avez sélectionné un modèle au cours de l’étape **Démarrer**, le corps du message est déjà configuré, mais vous pouvez le modifier.</span><span class="sxs-lookup"><span data-stu-id="8112a-222">If you selected a template in the **Start** step, the message body is already configured, but you can customize it.</span></span> <span data-ttu-id="8112a-223">Vous pouvez utiliser l’onglet **Courrier** (éditeur HTML enrichi) ou l’onglet **Source** (code HTML brut).</span><span class="sxs-lookup"><span data-stu-id="8112a-223">You can use the **Email** tab (a rich HTML editor) or the **Source** tab (raw HTML code).</span></span>

   <span data-ttu-id="8112a-224">La mise en forme HTML peut être simple ou complexe, en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="8112a-224">The HTML formatting can be as simple or complex as you need it to be.</span></span> <span data-ttu-id="8112a-225">Vous pouvez insérer des images et du texte pour améliorer la crédibilité du message dans le client de courrier du destinataire.</span><span class="sxs-lookup"><span data-stu-id="8112a-225">You can insert images and text to enhance the believability of the message in the recipient's email client.</span></span>

   - <span data-ttu-id="8112a-226">`${username}` insère le nom du destinataire.</span><span class="sxs-lookup"><span data-stu-id="8112a-226">`${username}` inserts the recipient's name.</span></span>

   - <span data-ttu-id="8112a-227">`${loginserverurl}` insère la valeur de l’**URL du serveur de connexion d’hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="8112a-227">`${loginserverurl}` inserts the **Phishing Login Server URL** value.</span></span>

   <span data-ttu-id="8112a-228">Pour les campagnes d’**Harponnage (pièce jointe)**, il est recommandé de supprimer le lien du corps du message (sinon, le message contient un lien **et** une pièce jointe et les clics sur un lien ne sont pas suivis dans une campagne de pièce jointe).</span><span class="sxs-lookup"><span data-stu-id="8112a-228">For **Spear Phishing (Attachment)** campaigns, you should remove the link from the body of the message (otherwise, the message will contain both a link **and** an attachment, and link clicks aren't tracked in an attachment campaign).</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="8112a-229">![Composer un message](../../media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)</span><span class="sxs-lookup"><span data-stu-id="8112a-229">![Compose Email Body](../../media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)</span></span>

   <span data-ttu-id="8112a-230">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="8112a-230">When you're finished, click **Next**.</span></span>

7. <span data-ttu-id="8112a-231">À l’étape **Confirmer**, cliquez sur **Terminer** pour lancer la campagne.</span><span class="sxs-lookup"><span data-stu-id="8112a-231">In the **Confirm** step, click **Finish** to launch the campaign.</span></span> <span data-ttu-id="8112a-232">Le message d’hameçonnage est remis aux destinataires ciblés.</span><span class="sxs-lookup"><span data-stu-id="8112a-232">The phishing message is delivered to the targeted recipients.</span></span>

## <a name="password-attack-campaigns"></a><span data-ttu-id="8112a-233">Campagnes d’attaques de mot de passe</span><span class="sxs-lookup"><span data-stu-id="8112a-233">Password attack campaigns</span></span>

<span data-ttu-id="8112a-234">Une *attaque de mot de passe* tente de deviner les mots de passe des comptes d’utilisateurs au sein d’une organisation, généralement une fois que l’attaquant a identifié un ou plusieurs comptes d’utilisateurs valides.</span><span class="sxs-lookup"><span data-stu-id="8112a-234">A *password attack* tries to guess passwords for user accounts in an organization, typically after the attacker has identified one or more valid user accounts.</span></span>

<span data-ttu-id="8112a-235">Dans le Simulateur d’attaques, deux types différents de campagnes d’attaque de mot de passe sont à votre disposition pour tester la complexité des mots de passe des utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="8112a-235">In Attack Simulator, two different types of password attack campaigns are available for you to test the complexity of your users' passwords:</span></span>

- <span data-ttu-id="8112a-236">**Mot de passe par force brute (attaque par dictionnaire)**  : une attaque par *force brute* ou *dictionnaire* utilise un grand fichier dictionnaire pour les mots de passe d’un compte utilisateur, avec l’espoir que l’un d’entre eux va réussir (de nombreux mots de passe pour un seul compte).</span><span class="sxs-lookup"><span data-stu-id="8112a-236">**Brute force password (dictionary attack)**: A *brute force* or *dictionary* attack uses a large dictionary file of passwords on a user account with the hope that one of them will work (many passwords against one account).</span></span> <span data-ttu-id="8112a-237">Un mot de passe incorrect permet de dissuader les attaques de mot de passe par force brute.</span><span class="sxs-lookup"><span data-stu-id="8112a-237">Incorrect password lock-outs help deter brute force password attacks.</span></span>

  <span data-ttu-id="8112a-238">Pour l’attaque par dictionnaire, vous pouvez spécifier un ou plusieurs mots de passe à tenter (entrés manuellement ou dans un fichier téléchargé), et vous pouvez spécifier un ou plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8112a-238">For the dictionary attack, you can specify one or many passwords to try (manually entered or in an uploaded file), and you can specify one or many users.</span></span>

- <span data-ttu-id="8112a-239">L’**Attaque par pulvérisation de mots de passe** : une *pulvérisation de mots de passe* utilise le même mot de passe soigneusement étudié contre une liste de comptes d’utilisateurs (un mot de passe pour plusieurs comptes).</span><span class="sxs-lookup"><span data-stu-id="8112a-239">**Password spray attack**: A *password spray* attack uses the same carefully considered password against a list of user accounts (one password against many accounts).</span></span> <span data-ttu-id="8112a-240">Les attaques par pulvérisation de mots de passe sont plus difficiles à détecter que les attaques de mots de passe par force brute (la probabilité de réussite augmente lorsqu’un attaquant essaie un mot de passe sur des dizaines ou des centaines de comptes sans risquer de déclencher le verrouillage du mot de passe incorrect de l’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="8112a-240">Password spray attacks are harder to detect than brute force password attacks (the probability of success increases when an attacker tries one password across dozens or hundreds of accounts without the risk of tripping the user's incorrect password lock-out).</span></span>

  <span data-ttu-id="8112a-241">Pour l’attaque par pulvérisation de mots de passe, vous ne pouvez spécifier qu’un seul mot de passe et vous pouvez préciser un ou plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8112a-241">For the password spray attack, you can only specify one password to try, and you can specify one or many users.</span></span>

> [!NOTE]
> <span data-ttu-id="8112a-242">Les attaques par mot de passe dans le Simulateur d’attaques transmettent les demandes d’authentification de base par nom d’utilisateur et mot de passe à un point de terminaison. Elles fonctionnent ainsi avec d’autres méthodes d’authentification (AD FS, synchronisation du hachage de mot de passe, directe, PingFederate, etc.).</span><span class="sxs-lookup"><span data-stu-id="8112a-242">The password attacks in Attack Simulator pass username and password Basic auth requests to an endpoint, so they also work with other authentication methods (AD FS, password hash sync, pass-through, PingFederate, etc.).</span></span> <span data-ttu-id="8112a-243">Pour les utilisateurs qui ont activé l’authentification multifacteur, même si l’attaque de mot de passe essaie son propre mot de passe, la tentative s’enregistre toujours en tant qu’échec (en d’autres termes, les utilisateurs de l’authentification multifacteur n’apparaissent jamais dans le nombre de **Tentatives réussies** de la campagne).</span><span class="sxs-lookup"><span data-stu-id="8112a-243">For users that have MFA enabled, even if the password attack tries their actual password, the attempt will always register as a failure (in other words, MFA users will never appear in the **Successful attempts** count of the campaign).</span></span> <span data-ttu-id="8112a-244">Il s'agit du résultat attendu.</span><span class="sxs-lookup"><span data-stu-id="8112a-244">This is the expected result.</span></span> <span data-ttu-id="8112a-245">L’authentification multifacteur est la méthode principale pour permettre de vous protéger contre des attaques par mot de passe.</span><span class="sxs-lookup"><span data-stu-id="8112a-245">MFA is a primary method to help protect against password attacks.</span></span>

### <a name="create-and-launch-a-password-attack-campaign"></a><span data-ttu-id="8112a-246">Création et lancement d’une campagne d’attaque par mot de passe</span><span class="sxs-lookup"><span data-stu-id="8112a-246">Create and launch a password attack campaign</span></span>

1. <span data-ttu-id="8112a-247">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Simulateur d’attaques**.</span><span class="sxs-lookup"><span data-stu-id="8112a-247">In the Security & Compliance Center, go to **Threat management** \> **Attack simulator**.</span></span>

2. <span data-ttu-id="8112a-248">Dans la page **Simulation d’attaques**, effectuez l’une des sélections suivantes en fonction du type de campagne que vous voulez créer :</span><span class="sxs-lookup"><span data-stu-id="8112a-248">On the **Simulate attacks** page, make one of the following selections based on the type of campaign you want to create:</span></span>

   - <span data-ttu-id="8112a-249">Dans la section **Mot de passe par force brute (attaque par dictionnaire)**, cliquez sur **Lancer l’attaque** ou sur **Détails de l’attaque** \> **Lancer l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="8112a-249">In the **Brute Force Password (Dictionary Attack)** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

   - <span data-ttu-id="8112a-250">Dans la section **Attaque par pulvérisation de mots de passe**, cliquez sur **Lancer l’attaque** ou sur **Détails de l’attaque** \> **Lancer l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="8112a-250">in the **Password spray attack** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

3. <span data-ttu-id="8112a-251">L’Assistant **Configurer l’attaque de mot de passe** démarre dans un nouveau menu volant.</span><span class="sxs-lookup"><span data-stu-id="8112a-251">The **Configure Password Attack** wizard starts in a new flyout.</span></span> <span data-ttu-id="8112a-252">À l’étape **Démarrer**, entrez un nom d’affichage unique pour la campagne, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="8112a-252">In the **Start** step, enter a unique display name for the campaign, and then click **Next**.</span></span>

4. <span data-ttu-id="8112a-253">À l’étape **Utilisateurs cible**, effectuez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8112a-253">In the **Target users** step, do one of the following steps:</span></span>

   - <span data-ttu-id="8112a-254">Cliquez sur le **Carnet d'adresses** pour sélectionner les destinataires (utilisateurs ou groupes) pour la campagne.</span><span class="sxs-lookup"><span data-stu-id="8112a-254">Click **Address Book** to select the recipients (users or groups) for the campaign.</span></span> <span data-ttu-id="8112a-255">Chaque destinataire ciblé doit avoir une boîte aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="8112a-255">Each targeted recipient must have an Exchange Online mailbox.</span></span> <span data-ttu-id="8112a-256">Si vous cliquez sur **Filtrer** et **Appliquer** sans entrer de critères de recherche, tous les destinataires sont renvoyés et ajoutés à la campagne.</span><span class="sxs-lookup"><span data-stu-id="8112a-256">If you click **Filter** and **Apply** without entering a search criteria, all recipients are returned and added to the campaign.</span></span>

   - <span data-ttu-id="8112a-257">Cliquez sur **Importer**, puis sur **Importation d’un fichier** pour importer un fichier de valeurs séparées par des virgules (CSV) ou d’adresses e-mail séparées par une ligne.</span><span class="sxs-lookup"><span data-stu-id="8112a-257">Click **Import** then **File Import** to import a comma-separated value (CSV) or line-separated file of email addresses.</span></span> <span data-ttu-id="8112a-258">Chaque ligne doit contenir l’adresse e-mail du destinataire.</span><span class="sxs-lookup"><span data-stu-id="8112a-258">Each line must contain the recipient's email address.</span></span>

   <span data-ttu-id="8112a-259">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="8112a-259">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="8112a-260">À l’étape **Choix des paramètres de l’attaque**, sélectionnez ce que vous voulez faire en fonction du type de campagne :</span><span class="sxs-lookup"><span data-stu-id="8112a-260">In the **Choose attack settings** step, choose what to do based on the campaign type:</span></span>

   - <span data-ttu-id="8112a-261">**Mot de passe par force brute (attaque par dictionnaire)**  : effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="8112a-261">**Brute Force Password (Dictionary Attack)**: Do either of the following steps:</span></span>

     - <span data-ttu-id="8112a-262">**Entrez les mots de passe manuellement** : dans la boîte de dialogue **Appuyez sur Entrée pour ajouter un mot de passe**, tapez un mot de passe, puis appuyez sur ENTRÉE.</span><span class="sxs-lookup"><span data-stu-id="8112a-262">**Enter passwords manually**: In the **Press enter to add a password** box, type a password and then press ENTER.</span></span> <span data-ttu-id="8112a-263">Répétez cette étape autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8112a-263">Repeat this step as many times as necessary.</span></span>

     - <span data-ttu-id="8112a-264">**Charger des mots de passe à partir d’un fichier dictionnaire**: cliquez sur **Télécharger** pour importer un fichier texte existant qui contient un mot de passe sur chaque ligne et une dernière ligne vide.</span><span class="sxs-lookup"><span data-stu-id="8112a-264">**Upload passwords from a dictionary file**: Click **Upload** to import an existing text file that contains one password on each line and a blank last line.</span></span> <span data-ttu-id="8112a-265">La taille du fichier texte doit être inférieure ou égale à 10 Mo et ne peut pas contenir plus de 30 000 mots de passe.</span><span class="sxs-lookup"><span data-stu-id="8112a-265">The text file must be 10 MB or less in size, and can't contain more than 30000 passwords.</span></span>

   - <span data-ttu-id="8112a-266">**Attaque par pulvérisation par mots de passe** : entrez un mot de passe dans la zone de dialogue **Le ou les mots de passe à utiliser dans le cadre de l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="8112a-266">**Password spray attack**: In **The password(s) to use in the attack** box, enter one password.</span></span>

   <span data-ttu-id="8112a-267">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="8112a-267">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="8112a-268">À l’étape **Confirmer**, cliquez sur **Terminer** pour lancer la campagne.</span><span class="sxs-lookup"><span data-stu-id="8112a-268">In the **Confirm** step, click **Finish** to launch the campaign.</span></span> <span data-ttu-id="8112a-269">Les mots de passe que vous avez spécifiés ont été essayés pour les utilisateurs que vous avez précisés.</span><span class="sxs-lookup"><span data-stu-id="8112a-269">The passwords you specified are tried on users you specified.</span></span>

## <a name="view-campaign-results"></a><span data-ttu-id="8112a-270">Afficher les résultats de la campagne</span><span class="sxs-lookup"><span data-stu-id="8112a-270">View campaign results</span></span>

<span data-ttu-id="8112a-271">Après avoir lancé une campagne, vous pouvez consulter l’avancement et les résultats sur la page principale **Simulation d’attaques**.</span><span class="sxs-lookup"><span data-stu-id="8112a-271">After you launch a campaign, you can check the progress and results on the main **Simulate attacks** page.</span></span>

<span data-ttu-id="8112a-272">Les campagnes actives affichent une barre de statut, une valeur de pourcentage terminée et un nombre « (utilisateurs terminés) sur (total des utilisateurs) ».</span><span class="sxs-lookup"><span data-stu-id="8112a-272">Active campaigns will show a status bar, a completed percentage value and "(completed users) of (total users)" count.</span></span> <span data-ttu-id="8112a-273">Le fait de cliquer sur le bouton **Actualiser** permet de mettre à jour l’avancement de toutes les campagnes actives.</span><span class="sxs-lookup"><span data-stu-id="8112a-273">Clicking the **Refresh** button will update the progress of any active campaigns.</span></span> <span data-ttu-id="8112a-274">Vous pouvez également cliquer sur **Terminer** pour arrêter une campagne active.</span><span class="sxs-lookup"><span data-stu-id="8112a-274">You can also click **Terminate** to stop an active campaign.</span></span>

<span data-ttu-id="8112a-275">Une fois la campagne terminée, le statut devient **Attaque achevée**.</span><span class="sxs-lookup"><span data-stu-id="8112a-275">When the campaign is finished, the status changes to **Attack completed**.</span></span> <span data-ttu-id="8112a-276">Vous pouvez afficher les résultats de la campagne en effectuant l’une des actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="8112a-276">You can view the results of the campaign by doing either of the following actions:</span></span>

- <span data-ttu-id="8112a-277">Dans la page principale **Simulation d’attaques**, cliquez sur **Afficher le rapport** sous le nom de la campagne.</span><span class="sxs-lookup"><span data-stu-id="8112a-277">On the main **Simulate attacks** page, click **View Report** under the name of the campaign.</span></span>

- <span data-ttu-id="8112a-278">Dans la page principale **Simulation d’attaques**, cliquez sur les **Détails de l’attaque** dans la section correspondant au type d’attaque.</span><span class="sxs-lookup"><span data-stu-id="8112a-278">On the main **Simulate attacks** page, click **Attack Details** in the section for the type of attack.</span></span> <span data-ttu-id="8112a-279">Dans la page **Détails de l’attaque** qui s’ouvre, sélectionnez la campagne dans la section **Historique des attaques**.</span><span class="sxs-lookup"><span data-stu-id="8112a-279">On the **Attack details** page that opens, select the campaign in the **Attack History** section.</span></span>

<span data-ttu-id="8112a-280">L’une des actions précédentes vous dirige vers une page intitulée **Détails de l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="8112a-280">Either of the previous actions will take you to a page named **Attack details**.</span></span> <span data-ttu-id="8112a-281">Les informations disponibles dans cette page pour chaque type de campagne sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="8112a-281">The information that's available on this page for each type of campaign is described in the following sections.</span></span>

### <a name="spear-phishing-credentials-harvest-campaign-results"></a><span data-ttu-id="8112a-282">Résultats de campagne de harponnage (recueil des informations d’identification)</span><span class="sxs-lookup"><span data-stu-id="8112a-282">Spear Phishing (Credentials Harvest) campaign results</span></span>

<span data-ttu-id="8112a-283">Les informations suivantes sont disponibles sur la page des **Détails de l’attaque** pour chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="8112a-283">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="8112a-284">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="8112a-284">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="8112a-285">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="8112a-285">**Total users targeted**</span></span>

- <span data-ttu-id="8112a-286">**Tentatives réussies** : le nombre d’utilisateurs qui ont cliqué sur le lien **et** entré leurs informations d’identification (*toute* valeur de nom d’utilisateur et de mot de passe).</span><span class="sxs-lookup"><span data-stu-id="8112a-286">**Successful attempts**: The number of users who clicked the link **and** entered their credentials (*any* username and password value).</span></span>

- <span data-ttu-id="8112a-287">**Taux de réussite globale** : un pourcentage calculé par **Tentatives réussies** / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="8112a-287">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>

- <span data-ttu-id="8112a-288">**Le plus rapide – Clic** : le temps qu’il a fallu au premier utilisateur pour cliquer sur le lien après le lancement de votre campagne.</span><span class="sxs-lookup"><span data-stu-id="8112a-288">**Fastest Click**: How long it took the first user to click the link after you launched the campaign.</span></span>

- <span data-ttu-id="8112a-289">**Moyenne – Clic** : le temps total qu’il a fallu à tous les utilisateurs pour cliquer sur le lien, divisé par le nombre d’utilisateurs qui ont cliqué sur le lien.</span><span class="sxs-lookup"><span data-stu-id="8112a-289">**Average Click**: The sum of how long it took everyone to click the link divided by the number of users who clicked the link.</span></span>

- <span data-ttu-id="8112a-290">**Taux de réussite – Clic** : un pourcentage calculé par le (nombre d’utilisateurs qui ont cliqué sur le lien) / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="8112a-290">**Click Success Rate**: A percentage that's calculated by (number of users who clicked the link) / **Total users targeted**.</span></span>

- <span data-ttu-id="8112a-291">**Le plus rapide – Informations d’identification** : le temps qu’il a fallu au premier utilisateur pour entrer ses informations d’identification après le lancement de votre campagne.</span><span class="sxs-lookup"><span data-stu-id="8112a-291">**Fastest Credentials**: How long it took the first user to enter their credentials after you launched the campaign.</span></span>

- <span data-ttu-id="8112a-292">**Moyenne – Informations d’identification** : le temps total qu’il a fallu à tous les utilisateurs pour entrer leurs informations d’identification divisé par le nombre d’utilisateurs qui ont entré leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="8112a-292">**Average Credentials**: The sum of how long it took everyone to enter their credentials divided by the number of users who entered their credentials.</span></span>

- <span data-ttu-id="8112a-293">**Taux de réussite – Informations d’identification** : un pourcentage calculé par le (nombre d’utilisateurs qui ont entré leurs informations d’identification) / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="8112a-293">**Credential Success Rate**: A percentage that's calculated by (number of users who entered their credentials) / **Total users targeted**.</span></span>

- <span data-ttu-id="8112a-294">Graphique à barres affichant le **Lien sur lequel un clic a été effectué** et le nombre d’**Informations d’identification fournies** par jour.</span><span class="sxs-lookup"><span data-stu-id="8112a-294">A bar graph that shows the **Link clicked** and **Credential supplied** numbers per day.</span></span>

- <span data-ttu-id="8112a-295">Graphique circulaire affichant les pourcentages **Lien sur lequel un clic a été effectué**, **Informations d’identification fournies** et **Aucun** pour la campagne.</span><span class="sxs-lookup"><span data-stu-id="8112a-295">A circle graph that shows the **Link clicked**, **Credential supplied**, and **None** percentages for the campaign.</span></span>

- <span data-ttu-id="8112a-296">La section **Utilisateurs compromis** répertorie des informations sur les utilisateurs qui ont cliqué sur le lien :</span><span class="sxs-lookup"><span data-stu-id="8112a-296">The **Compromised Users** section lists the details of the users who clicked the link:</span></span>

  - <span data-ttu-id="8112a-297">L’adresse de messagerie de l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="8112a-297">The user's email address</span></span>

  - <span data-ttu-id="8112a-298">Date/heure à laquelle il a cliqué sur le lien.</span><span class="sxs-lookup"><span data-stu-id="8112a-298">The date/time when they clicked the link.</span></span>

  - <span data-ttu-id="8112a-299">L’adresse IP du client.</span><span class="sxs-lookup"><span data-stu-id="8112a-299">The client IP address.</span></span>

  - <span data-ttu-id="8112a-300">Détails sur la version de Windows et le navigateur web de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8112a-300">Details about the user's version of Windows and web browser.</span></span>

  <span data-ttu-id="8112a-301">Vous pouvez cliquer sur **Exporter** pour exporter les résultats dans un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="8112a-301">You can click **Export** to export the results to a CSV file.</span></span>

### <a name="spear-phishing-attachment-campaign-results"></a><span data-ttu-id="8112a-302">Résultats de la campagne de harponnage (pièce jointe)</span><span class="sxs-lookup"><span data-stu-id="8112a-302">Spear Phishing (Attachment) campaign results</span></span>

<span data-ttu-id="8112a-303">Les informations suivantes sont disponibles sur la page des **Détails de l’attaque** pour chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="8112a-303">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="8112a-304">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="8112a-304">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="8112a-305">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="8112a-305">**Total users targeted**</span></span>

- <span data-ttu-id="8112a-306">**Tentatives réussies** : nombre d’utilisateurs qui ont ouvert ou téléchargé et ouvert la pièce jointe (l’aperçu ne compte pas).</span><span class="sxs-lookup"><span data-stu-id="8112a-306">**Successful attempts**: The number of users who opened or downloaded and opened the attachment (preview doesn't count).</span></span>

- <span data-ttu-id="8112a-307">**Taux de réussite globale** : un pourcentage calculé par **Tentatives réussies** / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="8112a-307">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>

- <span data-ttu-id="8112a-308">**Délai d’ouverture des pièces jointes le plus rapide** : le temps qu’il a fallu au premier utilisateur pour ouvrir la pièce jointe après le lancement de votre campagne.</span><span class="sxs-lookup"><span data-stu-id="8112a-308">**Fastest attachment open time**: How long it took the first user to open the attachment after you launched the campaign.</span></span>

- <span data-ttu-id="8112a-309">**Délai moyen d’ouverture des pièces jointes** : le temps total qu’il a fallu à tous les utilisateurs pour ouvrir la pièce jointe divisé par le nombre de personnes qui ont ouvert la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="8112a-309">**Average attachment open time**: The sum of how long it took everyone to open the attachment divided by the number of users who opened the attachment.</span></span>

- <span data-ttu-id="8112a-310">**Taux d’ouverture réussie des pièces jointes** : un pourcentage calculé par le (nombre d’utilisateurs qui ont ouvert la pièce jointe) / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="8112a-310">**Attachment open success rate**: A percentage that's calculated by (number of users who opened the attachment) / **Total users targeted**.</span></span>

### <a name="brute-force-password-dictionary-attack-campaign-results"></a><span data-ttu-id="8112a-311">Résultats de la campagne de mot de passe par force brute (attaque par dictionnaire)</span><span class="sxs-lookup"><span data-stu-id="8112a-311">Brute Force Password (Dictionary Attack) campaign results</span></span>

<span data-ttu-id="8112a-312">Les informations suivantes sont disponibles sur la page des **Détails de l’attaque** pour chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="8112a-312">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="8112a-313">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="8112a-313">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="8112a-314">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="8112a-314">**Total users targeted**</span></span>

- <span data-ttu-id="8112a-315">**Tentatives réussies** : nombre d’utilisateurs qui se sont avérées utiliser l’un des mots de passe spécifiés.</span><span class="sxs-lookup"><span data-stu-id="8112a-315">**Successful attempts**: The number of users who were found to be using one of the specified passwords.</span></span>

- <span data-ttu-id="8112a-316">**Taux de réussite globale** : un pourcentage calculé par **Tentatives réussies** / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="8112a-316">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>

- <span data-ttu-id="8112a-317">La section **Utilisateurs compromis** répertorie les adresses de courrier des utilisateurs concernés.</span><span class="sxs-lookup"><span data-stu-id="8112a-317">The **Compromised Users** section lists the email addresses of the affected users.</span></span> <span data-ttu-id="8112a-318">Vous pouvez cliquer sur **Exporter** pour exporter les résultats dans un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="8112a-318">You can click **Export** to export the results to a CSV file.</span></span>

### <a name="password-spray-attack-campaign-results"></a><span data-ttu-id="8112a-319">Résultats de la campagne d’attaque par pulvérisation par mots de passe</span><span class="sxs-lookup"><span data-stu-id="8112a-319">Password spray attack campaign results</span></span>

<span data-ttu-id="8112a-320">Les informations suivantes sont disponibles sur la page des **Détails de l’attaque** pour chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="8112a-320">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="8112a-321">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="8112a-321">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="8112a-322">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="8112a-322">**Total users targeted**</span></span>

- <span data-ttu-id="8112a-323">**Tentatives réussies** : nombre d’utilisateurs qui se sont avérées utiliser le mot de passe spécifié.</span><span class="sxs-lookup"><span data-stu-id="8112a-323">**Successful attempts**: The number of users who were found to be using the specified password.</span></span>

- <span data-ttu-id="8112a-324">**Taux de réussite globale** : un pourcentage calculé par **Tentatives réussies** / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="8112a-324">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>
