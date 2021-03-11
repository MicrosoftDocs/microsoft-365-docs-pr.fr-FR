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
description: Les administrateurs peuvent apprendre à utiliser le Simulateur d’attaques pour exécuter des attaques par hameçonnage simulé et par mot de passe dans leurs organisations Microsoft 365 E5 ou Microsoft Defender pour Office 365 Plan 2.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 7c88a5df6fae61e1ffe70214ad4a73deef4b380e
ms.sourcegitcommit: 6e4ddf35aaf747599f476f9988bcef02cacce1b6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/11/2021
ms.locfileid: "50717610"
---
# <a name="attack-simulator-in-microsoft-defender-for-office-365"></a><span data-ttu-id="53036-103">Simulateur d’attaques dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="53036-103">Attack Simulator in Microsoft Defender for Office 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="53036-104">**S’applique** [à Microsoft Defender pour Office 365 plan 2](office-365-atp.md)</span><span class="sxs-lookup"><span data-stu-id="53036-104">**Applies to** [Microsoft Defender for Office 365 plan 2](office-365-atp.md)</span></span>

<span data-ttu-id="53036-105">Si votre organisation dispose de Microsoft Defender pour Office [](office-365-ti.md)365 Plan 2, qui inclut des fonctionnalités d’investigation et de réponse aux menaces, vous pouvez utiliser le Simulateur d’attaques dans le Centre de sécurité & conformité pour exécuter des scénarios d’attaque réalistes dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="53036-105">If your organization has Microsoft Defender for Office 365 Plan 2, which includes [Threat Investigation and Response capabilities](office-365-ti.md), you can use Attack Simulator in the Security & Compliance Center to run realistic attack scenarios in your organization.</span></span> <span data-ttu-id="53036-106">Ces attaques simulées peuvent vous aider à identifier et à trouver des utilisateurs vulnérables avant qu’une attaque réelle n’impacte votre ligne de bas de page.</span><span class="sxs-lookup"><span data-stu-id="53036-106">These simulated attacks can help you identify and find vulnerable users before a real attack impacts your bottom line.</span></span> <span data-ttu-id="53036-107">Pour en savoir plus, lisez cet article.</span><span class="sxs-lookup"><span data-stu-id="53036-107">Read this article to learn more.</span></span>

> [!NOTE]
>
> <span data-ttu-id="53036-108">Le Simulateur d’attaques, comme décrit dans cet article, est désormais en lecture seule et a été remplacé par une formation à la **simulation** d’attaque dans le nœud de collaboration e-mail **&** dans le Centre de sécurité [Microsoft 365.](https://security.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="53036-108">Attack Simulator as described in this article is now read-only and has been replaced by **Attack simulation training** in the **Email & collaboration** node in the [Microsoft 365 security center](https://security.microsoft.com).</span></span> <span data-ttu-id="53036-109">Pour plus d’informations, voir [Get started using Attack simulation training](attack-simulation-training-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="53036-109">For more information, see [Get started using Attack simulation training](attack-simulation-training-get-started.md).</span></span>
>
> <span data-ttu-id="53036-110">La possibilité de lancer de nouvelles simulations à partir de cette version du Simulateur d’attaques a été désactivée.</span><span class="sxs-lookup"><span data-stu-id="53036-110">The ability to launch new simulations from this version of Attack Simulator has been disabled.</span></span> <span data-ttu-id="53036-111">Toutefois, vous pouvez toujours accéder aux rapports pendant 90 jours à partir du 24 janvier 2021.</span><span class="sxs-lookup"><span data-stu-id="53036-111">However, you can still access reports for up to 90 days from January 24, 2021.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="53036-112">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="53036-112">What do you need to know before you begin?</span></span>

- <span data-ttu-id="53036-113">Pour ouvrir le Centre de conformité et sécurité, consultez <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="53036-113">To open the Security & Compliance Center, go to <https://protection.office.com/>.</span></span> <span data-ttu-id="53036-114">Le Simulateur d’attaques est disponible dans **Gestion des menaces** \> **Simulateur d’attaques**.</span><span class="sxs-lookup"><span data-stu-id="53036-114">Attack simulator is available at **Threat management** \> **Attack simulator**.</span></span> <span data-ttu-id="53036-115">Go go directly to attack simulator, open <https://protection.office.com/attacksimulator> .</span><span class="sxs-lookup"><span data-stu-id="53036-115">Go go directly to attack simulator, open <https://protection.office.com/attacksimulator>.</span></span>

- <span data-ttu-id="53036-116">Pour plus d’informations sur la disponibilité du Simulateur d’attaques dans différents abonnements Microsoft 365, voir la description du service Microsoft Defender pour [Office 365.](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)</span><span class="sxs-lookup"><span data-stu-id="53036-116">For more information about the availability of Attack Simulator across different Microsoft 365 subscriptions, see [Microsoft Defender for Office 365 service description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>

- <span data-ttu-id="53036-117">Vous devez être membre des groupes de rôles **Management de l’organisation** ou **Administrateur de sécurité**.</span><span class="sxs-lookup"><span data-stu-id="53036-117">You need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span> <span data-ttu-id="53036-118">Pour des informations supplémentaires sur les groupes de rôles dans le Centre de sécurité et conformité, voir [Autorisations dans le Centre de sécurité et conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="53036-118">For more information about role groups in the Security & Compliance Center, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="53036-119">Votre compte doit être configuré pour l’authentification multifacteur (MFA) afin que vous puissiez créer et gérer des campagnes dans le Simulateur d’attaques.</span><span class="sxs-lookup"><span data-stu-id="53036-119">Your account needs to be configured for multi-factor authentication (MFA) to create and manage campaigns in Attack Simulator.</span></span> <span data-ttu-id="53036-120">Pour consulter des instructions, voir [Configurer Multi-factor Authentification (MFA)](../../admin/security-and-compliance/set-up-multi-factor-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="53036-120">For instructions, see [Set up multi-factor authentication](../../admin/security-and-compliance/set-up-multi-factor-authentication.md).</span></span>

- <span data-ttu-id="53036-121">Le Simulateur d’attaques fonctionne uniquement sur les boîtes aux lettres en nuage.</span><span class="sxs-lookup"><span data-stu-id="53036-121">Attack Simulator only works on cloud-based mailboxes.</span></span>

- <span data-ttu-id="53036-122">Les campagnes d’hameçonnage collectent et traitent des événements sur une durée de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="53036-122">Phishing campaigns will collect and process events for 30 days.</span></span> <span data-ttu-id="53036-123">L’historique des données de la campagne est disponible pendant un maximum de 90 jours après le lancement de la campagne.</span><span class="sxs-lookup"><span data-stu-id="53036-123">Historical campaign data will be available for up to 90 days after you launch the campaign.</span></span>

- <span data-ttu-id="53036-124">Les données associées à la simulation d’attaque et à la formation sont stockées avec d’autres données client pour les services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="53036-124">Attack simulation and training related data is stored with other customer data for Microsoft 365 services.</span></span> <span data-ttu-id="53036-125">Pour plus d’informations, voir emplacements de données [Microsoft 365.](/microsoft-365/enterprise/o365-data-locations)</span><span class="sxs-lookup"><span data-stu-id="53036-125">For more information see [Microsoft 365 data locations](/microsoft-365/enterprise/o365-data-locations).</span></span>

- <span data-ttu-id="53036-126">Il n’existe pas d’applet de commande PowerShell correspondante pour le Simulateur d’attaques.</span><span class="sxs-lookup"><span data-stu-id="53036-126">There are no corresponding PowerShell cmdlets for Attack Simulator.</span></span>

## <a name="spear-phishing-campaigns"></a><span data-ttu-id="53036-127">Campagnes de Harponnage</span><span class="sxs-lookup"><span data-stu-id="53036-127">Spear phishing campaigns</span></span>

<span data-ttu-id="53036-128">Le *Hameçonnage* est un terme générique qui décrit les attaques par courrier électronique tentant d’accéder à des informations sensibles par le biais de messages qui paraissent provenir d’expéditeurs légitimes ou approuvés.</span><span class="sxs-lookup"><span data-stu-id="53036-128">*Phishing* is a generic term for email attacks that try to steal sensitive information in messages that appear to be from legitimate or trusted senders.</span></span> <span data-ttu-id="53036-129">*Le harponnage* est une attaque ciblée par hameçonnage qui utilise du contenu ciblé et personnalisé spécifiquement adapté aux destinataires ciblés (généralement, après la reconnaissance des destinataires par l’attaquant).</span><span class="sxs-lookup"><span data-stu-id="53036-129">*Spear phishing* is a targeted phishing attack that uses focused and customized content that's specifically tailored to the targeted recipients (typically, after reconnaissance on the recipients by the attacker).</span></span>

<span data-ttu-id="53036-130">Dans le Simulateur d’attaques, deux types différents de campagnes de harponnage sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="53036-130">In Attack Simulator, two different types of spear phishing campaigns are available:</span></span>

- <span data-ttu-id="53036-131">**Harponnage (données d’identification)**: l’attaque tente de convaincre les destinataires de cliquer sur une URL dans le message.</span><span class="sxs-lookup"><span data-stu-id="53036-131">**Spear phishing (credentials harvest)**: The attack tries to convince the recipients to click a URL in the message.</span></span> <span data-ttu-id="53036-132">S’ils cliquent sur le lien, ils sont invités à entrer leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="53036-132">If they click the link, they're asked to enter their credentials.</span></span> <span data-ttu-id="53036-133">Si c’est le cas, ils sont conduits à l’un des emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="53036-133">If they do, they're taken to one of the following locations:</span></span>

  - <span data-ttu-id="53036-134">Page par défaut qui explique qu’il s’agit d’un simple test et donne des conseils pour reconnaître les messages d’hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="53036-134">A default page that explains that this was a just a test, and gives tips for recognizing phishing messages.</span></span>

    ![Ce que l’utilisateur voit s’il clique sur le lien de hameçonnage, puis entre ses informations d’identification](../../media/attack-simulator-phishing-result.png)

  - <span data-ttu-id="53036-136">Une page personnalisée (URL) que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="53036-136">A custom page (URL) that you specify.</span></span>

- <span data-ttu-id="53036-137">**Harponnage (pièce jointe)**  : l’attaque tente de convaincre le destinataire d’ouvrir une pièce jointe .docx ou .pdf contenue dans le message.</span><span class="sxs-lookup"><span data-stu-id="53036-137">**Spear phishing (attachment)**: The attack tries to convince the recipients to open a .docx or .pdf attachment in the message.</span></span> <span data-ttu-id="53036-138">La pièce jointe contient le même contenu à partir du lien de hameçonnage par défaut, mais la première phrase commence par « , vous voyez ce message comme un message électronique récent que vous avez \<Display Name\> ouvert... ».</span><span class="sxs-lookup"><span data-stu-id="53036-138">The attachment contains the same content from the default phishing link, but the first sentence starts with "\<Display Name\>, you are seeing this message as a recent email message you opened...".</span></span>

> [!NOTE]
> <span data-ttu-id="53036-139">Les campagnes de harponnage dans le Simulateur d’attaques n’arrivent pas à expiration pour le moment.</span><span class="sxs-lookup"><span data-stu-id="53036-139">Currently, spear phishing campaigns in Attack Simulator don't expire.</span></span>

### <a name="create-a-spear-phishing-campaign"></a><span data-ttu-id="53036-140">Création d’une campagne de harponnage</span><span class="sxs-lookup"><span data-stu-id="53036-140">Create a spear phishing campaign</span></span>

<span data-ttu-id="53036-141">L’apparence du message électronique envoyé aux destinataires ciblés est un élément important dans toute campagne de harponnage.</span><span class="sxs-lookup"><span data-stu-id="53036-141">An important part of any spear phishing campaign is the look and feel of the email message that's sent to the targeted recipients.</span></span> <span data-ttu-id="53036-142">Pour créer et configurer le courrier électronique, vous disposez des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="53036-142">To create and configure the email message, you have these options:</span></span>

- <span data-ttu-id="53036-143">**Utiliser un modèle d’e-mail intégré** : deux modèles prédéfinis sont disponibles : **Concours avec de nombreux prix à remporter** et **Mise à jour des données de paie**.</span><span class="sxs-lookup"><span data-stu-id="53036-143">**Use a built-in email template**: Two built-in templates are available: **Prize Giveaway** and **Payroll Update**.</span></span> <span data-ttu-id="53036-144">Vous pouvez personnaliser certaines, toutes ou aucune des propriétés de courrier à partir du modèle lorsque vous créez et lancez la campagne.</span><span class="sxs-lookup"><span data-stu-id="53036-144">You can further customize some, all, or none of the email properties from the template when you create and launch the campaign.</span></span>

- <span data-ttu-id="53036-145">**Créer un modèle d’e-mail réutilisable** : après la création et l’enregistrement du modèle de courrier, vous pouvez le réutiliser pour de prochaines campagnes de harponnage.</span><span class="sxs-lookup"><span data-stu-id="53036-145">**Create a reusable email template**: After you create and save the email template, you can use it again in future spear phishing campaigns.</span></span> <span data-ttu-id="53036-146">Vous pouvez personnaliser certaines, toutes ou aucune des propriétés de courrier à partir du modèle lorsque vous créez et lancez la campagne.</span><span class="sxs-lookup"><span data-stu-id="53036-146">You can further customize some, all, or none of the email properties from the template when you create and launch the campaign.</span></span>

- <span data-ttu-id="53036-147">**Créer le message électronique dans l’Assistant** : vous pouvez directement créer le message électronique dans l’Assistant lors de la création et du lancement de la campagne de harponnage.</span><span class="sxs-lookup"><span data-stu-id="53036-147">**Create the email message in the wizard**: You can create the email message directly in the wizard as you create and launch the spear phishing campaign.</span></span>

#### <a name="step-1-optional-create-a-custom-email-template"></a><span data-ttu-id="53036-148">Étape 1 (facultatif) : création d’un modèle d’e-mail personnalisé</span><span class="sxs-lookup"><span data-stu-id="53036-148">Step 1 (Optional): Create a custom email template</span></span>

<span data-ttu-id="53036-149">Si vous allez utiliser l’un des modèles intégrés ou créer le message directement dans l’Assistant, vous pouvez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="53036-149">If you're going to use one of the built-in templates or create the email message directly in the wizard, you can skip this step.</span></span>

1. <span data-ttu-id="53036-150">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Simulateur d’attaques**.</span><span class="sxs-lookup"><span data-stu-id="53036-150">In the Security & Compliance Center, go to **Threat management** \> **Attack simulator**.</span></span>

2. <span data-ttu-id="53036-151">Sur la page **Simulation d’attaques**, dans les sections **Harponnage (recueil des informations d’identification)** ou **Harponnage (pièce jointe)**, cliquez sur **Détails de l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="53036-151">On the **Simulate attacks** page, in either the **Spear Phishing (Credentials Harvest)** or **Spear Phishing (Attachment)** sections, click **Attack Details**.</span></span>

   <span data-ttu-id="53036-152">Peu importe l’emplacement où vous créez le modèle.</span><span class="sxs-lookup"><span data-stu-id="53036-152">It doesn't matter where you create the template.</span></span> <span data-ttu-id="53036-153">Les options disponibles dans le modèle sont identiques pour les deux types d’attaques par hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="53036-153">The available options in the template are the same for both types of phishing attacks.</span></span>

3. <span data-ttu-id="53036-154">Dans la page des **Détails de l’attaque** qui s’ouvre, dans la section **Modèles d’hameçonnage** de la zone **Créer des modèles**, cliquez sur **Nouveau modèle**.</span><span class="sxs-lookup"><span data-stu-id="53036-154">In the **Attack details** page that opens, in the **Phishing Templates** section, in the **Create Templates** area, click **New Template**.</span></span>

4. <span data-ttu-id="53036-155">L’Assistant **Configurer le modèle d’hameçonnage** démarre dans un nouveau menu volant.</span><span class="sxs-lookup"><span data-stu-id="53036-155">The **Configure Phishing Template** wizard starts in a new flyout.</span></span> <span data-ttu-id="53036-156">À l’étape **Démarrer**, entrez un nom d’affichage unique pour le modèle, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="53036-156">In the **Start** step, enter a unique display name for the template, and then click **Next**.</span></span>

5. <span data-ttu-id="53036-157">À l’étape **Configurer les détails du courrier**, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="53036-157">In the **Configure email details** step, configure the following settings:</span></span>

   - <span data-ttu-id="53036-158">**De (nom)**  : le nom d’affichage utilisé en tant qu’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="53036-158">**From (Name)**: The display name that's used for the message sender.</span></span>

   - <span data-ttu-id="53036-159">**De (adresse de courrier)**  : l’adresse de courrier de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="53036-159">**From (Email)**: The sender's email address.</span></span>

   - <span data-ttu-id="53036-160">**URL du serveur de connexion d’hameçonnage** : cliquez sur la liste déroulante, puis sélectionnez l’une des URL disponibles dans la liste.</span><span class="sxs-lookup"><span data-stu-id="53036-160">**Phishing Login Server URL**: Click the drop down and select one of the available URLs from the list.</span></span> <span data-ttu-id="53036-161">Elle représente l’URL sur laquelle les utilisateurs sont tentés de cliquer.</span><span class="sxs-lookup"><span data-stu-id="53036-161">This is the URL that users will be tempted to click.</span></span> <span data-ttu-id="53036-162">Les choix possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="53036-162">The choices are:</span></span>

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
     > <span data-ttu-id="53036-163">Un service de réputation d’URL peut identifier une ou plusieurs de ces URL comme étant non sécurisées.</span><span class="sxs-lookup"><span data-stu-id="53036-163">A URL reputation service might identify one or more of these URLs as unsafe.</span></span> <span data-ttu-id="53036-164">Vérifiez la disponibilité de l’URL dans vos navigateurs web pris en charge avant d’utiliser l’URL dans une campagne d’hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="53036-164">Check the availability of the URL in your supported web browsers before you use the URL in a phishing campaign.</span></span>

   - <span data-ttu-id="53036-165">**URL de la page de destination personnalisée** : entrez une page de destination facultative vers laquelle les utilisateurs sont dirigés s’ils cliquent sur le lien d’hameçonnage et entrent leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="53036-165">**Custom Landing Page URL**: Enter an optional landing page where users are taken if they click the phishing link and enter their credentials.</span></span> <span data-ttu-id="53036-166">Ce lien remplace la page de destination par défaut.</span><span class="sxs-lookup"><span data-stu-id="53036-166">This link replaces the default landing page.</span></span> <span data-ttu-id="53036-167">Par exemple, si vous avez une formation interne de sensibilisation, vous pouvez spécifier cette URL ici.</span><span class="sxs-lookup"><span data-stu-id="53036-167">For example, if you have internal awareness training, you can specify that URL here.</span></span>

   - <span data-ttu-id="53036-168">**Catégorie** : ce paramètre n’est à ce jour pas utilisé (ce que vous entrez n’est pas pris en compte).</span><span class="sxs-lookup"><span data-stu-id="53036-168">**Category**: Currently, this setting isn't used (anything you enter is ignored).</span></span>

   - <span data-ttu-id="53036-169">**Objet** : le champ **Objet** du message électronique.</span><span class="sxs-lookup"><span data-stu-id="53036-169">**Subject**: The **Subject** field of the email message.</span></span>

   <span data-ttu-id="53036-170">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="53036-170">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="53036-171">À l’étape **Composer un message**, créez le corps du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="53036-171">In the **Compose email** step, create the message body of the email message.</span></span> <span data-ttu-id="53036-172">Vous pouvez utiliser l’onglet **Courrier** (éditeur HTML enrichi) ou l’onglet **Source** (code HTML brut).</span><span class="sxs-lookup"><span data-stu-id="53036-172">You can use the **Email** tab (a rich HTML editor) or the **Source** tab (raw HTML code).</span></span>

   <span data-ttu-id="53036-173">La mise en forme HTML peut être simple ou complexe, en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="53036-173">The HTML formatting can be as simple or complex as you need it to be.</span></span> <span data-ttu-id="53036-174">Vous pouvez insérer des images et du texte pour améliorer la crédibilité du message dans le client de courrier du destinataire.</span><span class="sxs-lookup"><span data-stu-id="53036-174">You can insert images and text to enhance the believability of the message in the recipient's email client.</span></span>

   - <span data-ttu-id="53036-175">`${username}` insère le nom du destinataire.</span><span class="sxs-lookup"><span data-stu-id="53036-175">`${username}` inserts the recipient's name.</span></span>

   - <span data-ttu-id="53036-176">`${loginserverurl}` insère l’**URL du serveur de connexion d’hameçonnage** de l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="53036-176">`${loginserverurl}` inserts the **Phishing Login Server URL** value from the previous step.</span></span>

   <span data-ttu-id="53036-177">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="53036-177">When you're finished, click **Next**.</span></span>

7. <span data-ttu-id="53036-178">À l’étape **Confirmer**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="53036-178">In the **Confirm** step, click **Finish**.</span></span>

#### <a name="step-2-create-and-launch-the-spear-phishing-campaign"></a><span data-ttu-id="53036-179">Étape 2 : création et lancement d’une campagne de harponnage</span><span class="sxs-lookup"><span data-stu-id="53036-179">Step 2: Create and launch the spear phishing campaign</span></span>

1. <span data-ttu-id="53036-180">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Simulateur d’attaques**.</span><span class="sxs-lookup"><span data-stu-id="53036-180">In the Security & Compliance Center, go to **Threat management** \> **Attack simulator**.</span></span>

2. <span data-ttu-id="53036-181">Dans la page **Simulation d’attaques**, effectuez l’une des sélections suivantes en fonction du type de campagne que vous voulez créer :</span><span class="sxs-lookup"><span data-stu-id="53036-181">On the **Simulate attacks** page, make one of the following selections based on the type of campaign you want to create:</span></span>

   - <span data-ttu-id="53036-182">Dans la section **Harponnage (recueil des informations d’identification)**, cliquez sur **Lancer l’attaque** ou sur **Détails de l’attaque** \> **Lancer l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="53036-182">In the **Spear Phishing (Credentials Harvest)** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

   - <span data-ttu-id="53036-183">Dans la section **Harponnage (pièce jointe)**, cliquez sur **Lancer l’attaque** ou sur **Détails de l’attaque** \> **Lancer l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="53036-183">In the **Spear Phishing (Attachment)** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

3. <span data-ttu-id="53036-184">L’Assistant **Configurer l’attaque par hameçonnage** démarre dans un nouveau menu volant.</span><span class="sxs-lookup"><span data-stu-id="53036-184">The **Configure Phishing Attack** wizard starts in a new flyout.</span></span> <span data-ttu-id="53036-185">À l’étape **Démarrer**, effectuez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="53036-185">In the **Start** step, do one of the following steps:</span></span>

   - <span data-ttu-id="53036-186">Dans la zone **Nom**, entrez un nom d’affichage unique pour la campagne.</span><span class="sxs-lookup"><span data-stu-id="53036-186">In the **Name** box, enter a unique display name for the campaign.</span></span> <span data-ttu-id="53036-187">Ne pas cliquer sur **Utiliser le modèle**, car vous allez plus tard créer le message électronique dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="53036-187">Don't click **Use Template**, because you'll create the email message later in the wizard.</span></span>

   - <span data-ttu-id="53036-188">Cliquez sur **Utiliser le modèle**, puis sélectionnez un modèle de courrier prédéfini ou personnalisé.</span><span class="sxs-lookup"><span data-stu-id="53036-188">Click **Use Template** and select a built-in or custom email template.</span></span> <span data-ttu-id="53036-189">Après avoir sélectionné le modèle, la boîte de dialogue **Nom** est automatiquement remplie en fonction du modèle, mais il vous est possible de modifier le nom.</span><span class="sxs-lookup"><span data-stu-id="53036-189">After you select the template, the **Name** box is automatically filled based on the template, but you can change the name.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="53036-190">![Page de démarrage du hameçonnage](../../media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)</span><span class="sxs-lookup"><span data-stu-id="53036-190">![Phishing Start Page](../../media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)</span></span>

   <span data-ttu-id="53036-191">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="53036-191">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="53036-192">À l’étape **Destinataires cible**, effectuez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="53036-192">In the **Target recipients** step, do one of the following steps:</span></span>

   - <span data-ttu-id="53036-193">Cliquez sur le **Carnet d'adresses** pour sélectionner les destinataires (utilisateurs ou groupes) pour la campagne.</span><span class="sxs-lookup"><span data-stu-id="53036-193">Click **Address Book** to select the recipients (users or groups) for the campaign.</span></span> <span data-ttu-id="53036-194">Chaque destinataire ciblé doit avoir une boîte aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="53036-194">Each targeted recipient must have an Exchange Online mailbox.</span></span> <span data-ttu-id="53036-195">Si vous cliquez sur **Filtrer** et **Appliquer** sans entrer de critères de recherche, tous les destinataires sont renvoyés et ajoutés à la campagne.</span><span class="sxs-lookup"><span data-stu-id="53036-195">If you click **Filter** and **Apply** without entering a search criteria, all recipients are returned and added to the campaign.</span></span>

   - <span data-ttu-id="53036-196">Cliquez sur **Importer**, puis sur **Importation d’un fichier** pour importer un fichier de valeurs séparées par des virgules (CSV) ou d’adresses e-mail séparées par une ligne.</span><span class="sxs-lookup"><span data-stu-id="53036-196">Click **Import** then **File Import** to import a comma-separated value (CSV) or line-separated file of email addresses.</span></span> <span data-ttu-id="53036-197">Chaque ligne doit contenir l’adresse e-mail du destinataire.</span><span class="sxs-lookup"><span data-stu-id="53036-197">Each line must contain the recipient's email address.</span></span>

   <span data-ttu-id="53036-198">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="53036-198">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="53036-199">À l’étape **Configurer les détails du courrier**, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="53036-199">In the **Configure email details** step, configure the following settings:</span></span>

   <span data-ttu-id="53036-200">Si vous avez sélectionné un modèle au cours de l’étape **Démarrer**, la plupart de ces valeurs sont déjà configurées, mais vous pouvez les modifier.</span><span class="sxs-lookup"><span data-stu-id="53036-200">If you selected a template in the **Start** step, most of these values are already configured, but you can change them.</span></span>

   - <span data-ttu-id="53036-201">**De (nom)**  : le nom d’affichage utilisé en tant qu’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="53036-201">**From (Name)**: The display name that's used for the message sender.</span></span>

   - <span data-ttu-id="53036-202">**De (adresse de courrier)**  : l’adresse de courrier de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="53036-202">**From (Email)**: The sender's email address.</span></span> <span data-ttu-id="53036-203">Vous pouvez entrer une adresse de messagerie véritable ou fictive à partir du domaine de courrier de votre organisation ou vous pouvez saisir une adresse fausse ou réelle de courrier externe.</span><span class="sxs-lookup"><span data-stu-id="53036-203">You can enter a real or fake email address from your organization's email domain, or you can enter a real or fake external email address.</span></span> <span data-ttu-id="53036-204">Une adresse de messagerie d’expéditeur valide de votre organisation prend en réalité la forme du client de courrier du destinataire.</span><span class="sxs-lookup"><span data-stu-id="53036-204">A valid sender email address from your organization will actually resolve in the recipient's email client.</span></span>

   - <span data-ttu-id="53036-205">**URL du serveur de connexion d’hameçonnage** : cliquez sur la liste déroulante, puis sélectionnez l’une des URL disponibles dans la liste.</span><span class="sxs-lookup"><span data-stu-id="53036-205">**Phishing Login Server URL**: Click the drop down and select one of the available URLs from the list.</span></span> <span data-ttu-id="53036-206">Elle représente l’URL sur laquelle les utilisateurs sont tentés de cliquer.</span><span class="sxs-lookup"><span data-stu-id="53036-206">This is the URL that users will be tempted to click.</span></span> <span data-ttu-id="53036-207">Les choix possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="53036-207">The choices are:</span></span>

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
     > - <span data-ttu-id="53036-208">Toutes les URL sont intentionnellement HTTP et non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="53036-208">All of the URLs are intentionally http, not https.</span></span>
     >
     > - <span data-ttu-id="53036-209">Un service de réputation d’URL peut identifier une ou plusieurs de ces URL comme étant non sécurisées.</span><span class="sxs-lookup"><span data-stu-id="53036-209">A URL reputation service might identify one or more of these URLs as unsafe.</span></span> <span data-ttu-id="53036-210">Vérifiez la disponibilité de l’URL dans vos navigateurs web pris en charge avant d’utiliser l’URL dans une campagne d’hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="53036-210">Check the availability of the URL in your supported web browsers before you use the URL in a phishing campaign.</span></span>
     >
     > - <span data-ttu-id="53036-211">Vous devez sélectionner une URL.</span><span class="sxs-lookup"><span data-stu-id="53036-211">You are required to select a URL.</span></span> <span data-ttu-id="53036-212">Pour les campagnes d’**Harponnage (pièce jointe)**, vous pouvez supprimer le lien du corps du message à l’étape suivante (sinon, le message contient un lien **et** une pièce jointe).</span><span class="sxs-lookup"><span data-stu-id="53036-212">For **Spear Phishing (Attachment)** campaigns, you can remove the link from the body of the message in the next step (otherwise, the message will contain both a link **and** an attachment).</span></span>

   - <span data-ttu-id="53036-213">**Type de pièce jointe** : ce paramètre n’est disponible que pour les campagnes de **Harponnage (pièce jointe)**.</span><span class="sxs-lookup"><span data-stu-id="53036-213">**Attachment Type**: This setting is only available in **Spear Phishing (Attachment)** campaigns.</span></span> <span data-ttu-id="53036-214">Cliquez sur la liste déroulante, puis sélectionnez **.DOCX** ou **.PDF** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="53036-214">Click the drop down and select **.DOCX** or **.PDF** from the list.</span></span>

   - <span data-ttu-id="53036-215">**Nom de pièce jointe** : ce paramètre n’est disponible que pour les campagnes d’**Harponnage (pièce jointe)**.</span><span class="sxs-lookup"><span data-stu-id="53036-215">**Attachment Name**: This setting is only available in **Spear Phishing (Attachment)** campaigns.</span></span> <span data-ttu-id="53036-216">Entrez un nom de fichier pour la pièce jointe .docx ou .pdf.</span><span class="sxs-lookup"><span data-stu-id="53036-216">Enter a filename for the .docx or .pdf attachment.</span></span>

   - <span data-ttu-id="53036-217">**URL de la page de destination personnalisée** : entrez une page de destination facultative vers laquelle les utilisateurs sont dirigés s’ils cliquent sur le lien d’hameçonnage et entrent leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="53036-217">**Custom Landing Page URL**: Enter an optional landing page where users are taken if they click the phishing link and enter their credentials.</span></span> <span data-ttu-id="53036-218">Ce lien remplace la page de destination par défaut.</span><span class="sxs-lookup"><span data-stu-id="53036-218">This link replaces the default landing page.</span></span> <span data-ttu-id="53036-219">Par exemple, si vous avez une formation interne de sensibilisation, vous pouvez spécifier cette URL ici.</span><span class="sxs-lookup"><span data-stu-id="53036-219">For example, if you have internal awareness training, you can specify that URL here.</span></span>

   - <span data-ttu-id="53036-220">**Objet** : le champ **Objet** du message électronique.</span><span class="sxs-lookup"><span data-stu-id="53036-220">**Subject**: The **Subject** field of the email message.</span></span>

   <span data-ttu-id="53036-221">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="53036-221">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="53036-222">À l’étape **Composer un message**, créez le corps du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="53036-222">In the **Compose email** step, create the message body of the email message.</span></span> <span data-ttu-id="53036-223">Si vous avez sélectionné un modèle au cours de l’étape **Démarrer**, le corps du message est déjà configuré, mais vous pouvez le modifier.</span><span class="sxs-lookup"><span data-stu-id="53036-223">If you selected a template in the **Start** step, the message body is already configured, but you can customize it.</span></span> <span data-ttu-id="53036-224">Vous pouvez utiliser l’onglet **Courrier** (éditeur HTML enrichi) ou l’onglet **Source** (code HTML brut).</span><span class="sxs-lookup"><span data-stu-id="53036-224">You can use the **Email** tab (a rich HTML editor) or the **Source** tab (raw HTML code).</span></span>

   <span data-ttu-id="53036-225">La mise en forme HTML peut être simple ou complexe, en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="53036-225">The HTML formatting can be as simple or complex as you need it to be.</span></span> <span data-ttu-id="53036-226">Vous pouvez insérer des images et du texte pour améliorer la crédibilité du message dans le client de courrier du destinataire.</span><span class="sxs-lookup"><span data-stu-id="53036-226">You can insert images and text to enhance the believability of the message in the recipient's email client.</span></span>

   - <span data-ttu-id="53036-227">`${username}` insère le nom du destinataire.</span><span class="sxs-lookup"><span data-stu-id="53036-227">`${username}` inserts the recipient's name.</span></span>

   - <span data-ttu-id="53036-228">`${loginserverurl}` insère la valeur de l’**URL du serveur de connexion d’hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="53036-228">`${loginserverurl}` inserts the **Phishing Login Server URL** value.</span></span>

   <span data-ttu-id="53036-229">Pour les campagnes d’**Harponnage (pièce jointe)**, il est recommandé de supprimer le lien du corps du message (sinon, le message contient un lien **et** une pièce jointe et les clics sur un lien ne sont pas suivis dans une campagne de pièce jointe).</span><span class="sxs-lookup"><span data-stu-id="53036-229">For **Spear Phishing (Attachment)** campaigns, you should remove the link from the body of the message (otherwise, the message will contain both a link **and** an attachment, and link clicks aren't tracked in an attachment campaign).</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="53036-230">![Composer un message](../../media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)</span><span class="sxs-lookup"><span data-stu-id="53036-230">![Compose Email Body](../../media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)</span></span>

   <span data-ttu-id="53036-231">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="53036-231">When you're finished, click **Next**.</span></span>

7. <span data-ttu-id="53036-232">À l’étape **Confirmer**, cliquez sur **Terminer** pour lancer la campagne.</span><span class="sxs-lookup"><span data-stu-id="53036-232">In the **Confirm** step, click **Finish** to launch the campaign.</span></span> <span data-ttu-id="53036-233">Le message d’hameçonnage est remis aux destinataires ciblés.</span><span class="sxs-lookup"><span data-stu-id="53036-233">The phishing message is delivered to the targeted recipients.</span></span>

## <a name="password-attack-campaigns"></a><span data-ttu-id="53036-234">Campagnes d’attaques de mot de passe</span><span class="sxs-lookup"><span data-stu-id="53036-234">Password attack campaigns</span></span>

<span data-ttu-id="53036-235">Une *attaque de mot de passe* tente de deviner les mots de passe des comptes d’utilisateurs au sein d’une organisation, généralement une fois que l’attaquant a identifié un ou plusieurs comptes d’utilisateurs valides.</span><span class="sxs-lookup"><span data-stu-id="53036-235">A *password attack* tries to guess passwords for user accounts in an organization, typically after the attacker has identified one or more valid user accounts.</span></span>

<span data-ttu-id="53036-236">Dans le Simulateur d’attaques, deux types différents de campagnes d’attaque de mot de passe sont à votre disposition pour tester la complexité des mots de passe des utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="53036-236">In Attack Simulator, two different types of password attack campaigns are available for you to test the complexity of your users' passwords:</span></span>

- <span data-ttu-id="53036-237">**Mot de passe par force brute (attaque par dictionnaire)**  : une attaque par *force brute* ou *dictionnaire* utilise un grand fichier dictionnaire pour les mots de passe d’un compte utilisateur, avec l’espoir que l’un d’entre eux va réussir (de nombreux mots de passe pour un seul compte).</span><span class="sxs-lookup"><span data-stu-id="53036-237">**Brute force password (dictionary attack)**: A *brute force* or *dictionary* attack uses a large dictionary file of passwords on a user account with the hope that one of them will work (many passwords against one account).</span></span> <span data-ttu-id="53036-238">Un mot de passe incorrect permet de dissuader les attaques de mot de passe par force brute.</span><span class="sxs-lookup"><span data-stu-id="53036-238">Incorrect password lock-outs help deter brute force password attacks.</span></span>

  <span data-ttu-id="53036-239">Pour l’attaque par dictionnaire, vous pouvez spécifier un ou plusieurs mots de passe à tenter (entrés manuellement ou dans un fichier téléchargé), et vous pouvez spécifier un ou plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="53036-239">For the dictionary attack, you can specify one or many passwords to try (manually entered or in an uploaded file), and you can specify one or many users.</span></span>

- <span data-ttu-id="53036-240">L’**Attaque par pulvérisation de mots de passe** : une *pulvérisation de mots de passe* utilise le même mot de passe soigneusement étudié contre une liste de comptes d’utilisateurs (un mot de passe pour plusieurs comptes).</span><span class="sxs-lookup"><span data-stu-id="53036-240">**Password spray attack**: A *password spray* attack uses the same carefully considered password against a list of user accounts (one password against many accounts).</span></span> <span data-ttu-id="53036-241">Les attaques par pulvérisation de mots de passe sont plus difficiles à détecter que les attaques de mots de passe par force brute (la probabilité de réussite augmente lorsqu’un attaquant essaie un mot de passe sur des dizaines ou des centaines de comptes sans risquer de déclencher le verrouillage du mot de passe incorrect de l’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="53036-241">Password spray attacks are harder to detect than brute force password attacks (the probability of success increases when an attacker tries one password across dozens or hundreds of accounts without the risk of tripping the user's incorrect password lock-out).</span></span>

  <span data-ttu-id="53036-242">Pour l’attaque par pulvérisation de mots de passe, vous ne pouvez spécifier qu’un seul mot de passe et vous pouvez préciser un ou plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="53036-242">For the password spray attack, you can only specify one password to try, and you can specify one or many users.</span></span>

> [!NOTE]
> <span data-ttu-id="53036-243">Les attaques par mot de passe dans le Simulateur d’attaques transmettent les demandes d’authentification de base par nom d’utilisateur et mot de passe à un point de terminaison. Elles fonctionnent ainsi avec d’autres méthodes d’authentification (AD FS, synchronisation du hachage de mot de passe, directe, PingFederate, etc.).</span><span class="sxs-lookup"><span data-stu-id="53036-243">The password attacks in Attack Simulator pass username and password Basic auth requests to an endpoint, so they also work with other authentication methods (AD FS, password hash sync, pass-through, PingFederate, etc.).</span></span> <span data-ttu-id="53036-244">Pour les utilisateurs qui ont activé l’authentification multifacteur, même si l’attaque de mot de passe essaie son propre mot de passe, la tentative s’enregistre toujours en tant qu’échec (en d’autres termes, les utilisateurs de l’authentification multifacteur n’apparaissent jamais dans le nombre de **Tentatives réussies** de la campagne).</span><span class="sxs-lookup"><span data-stu-id="53036-244">For users that have MFA enabled, even if the password attack tries their actual password, the attempt will always register as a failure (in other words, MFA users will never appear in the **Successful attempts** count of the campaign).</span></span> <span data-ttu-id="53036-245">Il s'agit du résultat attendu.</span><span class="sxs-lookup"><span data-stu-id="53036-245">This is the expected result.</span></span> <span data-ttu-id="53036-246">L’authentification multifacteur est la méthode principale pour permettre de vous protéger contre des attaques par mot de passe.</span><span class="sxs-lookup"><span data-stu-id="53036-246">MFA is a primary method to help protect against password attacks.</span></span>

### <a name="create-and-launch-a-password-attack-campaign"></a><span data-ttu-id="53036-247">Création et lancement d’une campagne d’attaque par mot de passe</span><span class="sxs-lookup"><span data-stu-id="53036-247">Create and launch a password attack campaign</span></span>

1. <span data-ttu-id="53036-248">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Simulateur d’attaques**.</span><span class="sxs-lookup"><span data-stu-id="53036-248">In the Security & Compliance Center, go to **Threat management** \> **Attack simulator**.</span></span>

2. <span data-ttu-id="53036-249">Dans la page **Simulation d’attaques**, effectuez l’une des sélections suivantes en fonction du type de campagne que vous voulez créer :</span><span class="sxs-lookup"><span data-stu-id="53036-249">On the **Simulate attacks** page, make one of the following selections based on the type of campaign you want to create:</span></span>

   - <span data-ttu-id="53036-250">Dans la section **Mot de passe par force brute (attaque par dictionnaire)**, cliquez sur **Lancer l’attaque** ou sur **Détails de l’attaque** \> **Lancer l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="53036-250">In the **Brute Force Password (Dictionary Attack)** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

   - <span data-ttu-id="53036-251">Dans la section **Attaque par pulvérisation de mots de passe**, cliquez sur **Lancer l’attaque** ou sur **Détails de l’attaque** \> **Lancer l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="53036-251">in the **Password spray attack** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

3. <span data-ttu-id="53036-252">L’Assistant **Configurer l’attaque de mot de passe** démarre dans un nouveau menu volant.</span><span class="sxs-lookup"><span data-stu-id="53036-252">The **Configure Password Attack** wizard starts in a new flyout.</span></span> <span data-ttu-id="53036-253">À l’étape **Démarrer**, entrez un nom d’affichage unique pour la campagne, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="53036-253">In the **Start** step, enter a unique display name for the campaign, and then click **Next**.</span></span>

4. <span data-ttu-id="53036-254">À l’étape **Utilisateurs cible**, effectuez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="53036-254">In the **Target users** step, do one of the following steps:</span></span>

   - <span data-ttu-id="53036-255">Cliquez sur le **Carnet d'adresses** pour sélectionner les destinataires (utilisateurs ou groupes) pour la campagne.</span><span class="sxs-lookup"><span data-stu-id="53036-255">Click **Address Book** to select the recipients (users or groups) for the campaign.</span></span> <span data-ttu-id="53036-256">Chaque destinataire ciblé doit avoir une boîte aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="53036-256">Each targeted recipient must have an Exchange Online mailbox.</span></span> <span data-ttu-id="53036-257">Si vous cliquez sur **Filtrer** et **Appliquer** sans entrer de critères de recherche, tous les destinataires sont renvoyés et ajoutés à la campagne.</span><span class="sxs-lookup"><span data-stu-id="53036-257">If you click **Filter** and **Apply** without entering a search criteria, all recipients are returned and added to the campaign.</span></span>

   - <span data-ttu-id="53036-258">Cliquez sur **Importer**, puis sur **Importation d’un fichier** pour importer un fichier de valeurs séparées par des virgules (CSV) ou d’adresses e-mail séparées par une ligne.</span><span class="sxs-lookup"><span data-stu-id="53036-258">Click **Import** then **File Import** to import a comma-separated value (CSV) or line-separated file of email addresses.</span></span> <span data-ttu-id="53036-259">Chaque ligne doit contenir l’adresse e-mail du destinataire.</span><span class="sxs-lookup"><span data-stu-id="53036-259">Each line must contain the recipient's email address.</span></span>

   <span data-ttu-id="53036-260">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="53036-260">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="53036-261">À l’étape **Choix des paramètres de l’attaque**, sélectionnez ce que vous voulez faire en fonction du type de campagne :</span><span class="sxs-lookup"><span data-stu-id="53036-261">In the **Choose attack settings** step, choose what to do based on the campaign type:</span></span>

   - <span data-ttu-id="53036-262">**Mot de passe par force brute (attaque par dictionnaire)**  : effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="53036-262">**Brute Force Password (Dictionary Attack)**: Do either of the following steps:</span></span>

     - <span data-ttu-id="53036-263">**Entrez les mots de passe manuellement** : dans la boîte de dialogue **Appuyez sur Entrée pour ajouter un mot de passe**, tapez un mot de passe, puis appuyez sur ENTRÉE.</span><span class="sxs-lookup"><span data-stu-id="53036-263">**Enter passwords manually**: In the **Press enter to add a password** box, type a password and then press ENTER.</span></span> <span data-ttu-id="53036-264">Répétez cette étape autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="53036-264">Repeat this step as many times as necessary.</span></span>

     - <span data-ttu-id="53036-265">**Charger des mots de passe à partir d’un fichier dictionnaire**: cliquez sur **Télécharger** pour importer un fichier texte existant qui contient un mot de passe sur chaque ligne et une dernière ligne vide.</span><span class="sxs-lookup"><span data-stu-id="53036-265">**Upload passwords from a dictionary file**: Click **Upload** to import an existing text file that contains one password on each line and a blank last line.</span></span> <span data-ttu-id="53036-266">La taille du fichier texte doit être inférieure ou égale à 10 Mo et ne peut pas contenir plus de 30 000 mots de passe.</span><span class="sxs-lookup"><span data-stu-id="53036-266">The text file must be 10 MB or less in size, and can't contain more than 30000 passwords.</span></span>

   - <span data-ttu-id="53036-267">**Attaque par pulvérisation par mots de passe** : entrez un mot de passe dans la zone de dialogue **Le ou les mots de passe à utiliser dans le cadre de l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="53036-267">**Password spray attack**: In **The password(s) to use in the attack** box, enter one password.</span></span>

   <span data-ttu-id="53036-268">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="53036-268">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="53036-269">À l’étape **Confirmer**, cliquez sur **Terminer** pour lancer la campagne.</span><span class="sxs-lookup"><span data-stu-id="53036-269">In the **Confirm** step, click **Finish** to launch the campaign.</span></span> <span data-ttu-id="53036-270">Les mots de passe que vous avez spécifiés ont été essayés pour les utilisateurs que vous avez précisés.</span><span class="sxs-lookup"><span data-stu-id="53036-270">The passwords you specified are tried on users you specified.</span></span>

## <a name="view-campaign-results"></a><span data-ttu-id="53036-271">Afficher les résultats de la campagne</span><span class="sxs-lookup"><span data-stu-id="53036-271">View campaign results</span></span>

<span data-ttu-id="53036-272">Après avoir lancé une campagne, vous pouvez consulter l’avancement et les résultats sur la page principale **Simulation d’attaques**.</span><span class="sxs-lookup"><span data-stu-id="53036-272">After you launch a campaign, you can check the progress and results on the main **Simulate attacks** page.</span></span>

<span data-ttu-id="53036-273">Les campagnes actives affichent une barre de statut, une valeur de pourcentage terminée et un nombre « (utilisateurs terminés) sur (total des utilisateurs) ».</span><span class="sxs-lookup"><span data-stu-id="53036-273">Active campaigns will show a status bar, a completed percentage value and "(completed users) of (total users)" count.</span></span> <span data-ttu-id="53036-274">Le fait de cliquer sur le bouton **Actualiser** permet de mettre à jour l’avancement de toutes les campagnes actives.</span><span class="sxs-lookup"><span data-stu-id="53036-274">Clicking the **Refresh** button will update the progress of any active campaigns.</span></span> <span data-ttu-id="53036-275">Vous pouvez également cliquer sur **Terminer** pour arrêter une campagne active.</span><span class="sxs-lookup"><span data-stu-id="53036-275">You can also click **Terminate** to stop an active campaign.</span></span>

<span data-ttu-id="53036-276">Une fois la campagne terminée, le statut devient **Attaque achevée**.</span><span class="sxs-lookup"><span data-stu-id="53036-276">When the campaign is finished, the status changes to **Attack completed**.</span></span> <span data-ttu-id="53036-277">Vous pouvez afficher les résultats de la campagne en effectuant l’une des actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="53036-277">You can view the results of the campaign by doing either of the following actions:</span></span>

- <span data-ttu-id="53036-278">Dans la page principale **Simulation d’attaques**, cliquez sur **Afficher le rapport** sous le nom de la campagne.</span><span class="sxs-lookup"><span data-stu-id="53036-278">On the main **Simulate attacks** page, click **View Report** under the name of the campaign.</span></span>

- <span data-ttu-id="53036-279">Dans la page principale **Simulation d’attaques**, cliquez sur les **Détails de l’attaque** dans la section correspondant au type d’attaque.</span><span class="sxs-lookup"><span data-stu-id="53036-279">On the main **Simulate attacks** page, click **Attack Details** in the section for the type of attack.</span></span> <span data-ttu-id="53036-280">Dans la page **Détails de l’attaque** qui s’ouvre, sélectionnez la campagne dans la section **Historique des attaques**.</span><span class="sxs-lookup"><span data-stu-id="53036-280">On the **Attack details** page that opens, select the campaign in the **Attack History** section.</span></span>

<span data-ttu-id="53036-281">L’une des actions précédentes vous dirige vers une page intitulée **Détails de l’attaque**.</span><span class="sxs-lookup"><span data-stu-id="53036-281">Either of the previous actions will take you to a page named **Attack details**.</span></span> <span data-ttu-id="53036-282">Les informations disponibles dans cette page pour chaque type de campagne sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="53036-282">The information that's available on this page for each type of campaign is described in the following sections.</span></span>

### <a name="spear-phishing-credentials-harvest-campaign-results"></a><span data-ttu-id="53036-283">Résultats de campagne de harponnage (recueil des informations d’identification)</span><span class="sxs-lookup"><span data-stu-id="53036-283">Spear Phishing (Credentials Harvest) campaign results</span></span>

<span data-ttu-id="53036-284">Les informations suivantes sont disponibles sur la page des **Détails de l’attaque** pour chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="53036-284">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="53036-285">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="53036-285">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="53036-286">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="53036-286">**Total users targeted**</span></span>

- <span data-ttu-id="53036-287">**Tentatives réussies** : le nombre d’utilisateurs qui ont cliqué sur le lien **et** entré leurs informations d’identification (*toute* valeur de nom d’utilisateur et de mot de passe).</span><span class="sxs-lookup"><span data-stu-id="53036-287">**Successful attempts**: The number of users who clicked the link **and** entered their credentials (*any* username and password value).</span></span>

- <span data-ttu-id="53036-288">**Taux de réussite globale** : un pourcentage calculé par **Tentatives réussies** / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="53036-288">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>

- <span data-ttu-id="53036-289">**Le plus rapide – Clic** : le temps qu’il a fallu au premier utilisateur pour cliquer sur le lien après le lancement de votre campagne.</span><span class="sxs-lookup"><span data-stu-id="53036-289">**Fastest Click**: How long it took the first user to click the link after you launched the campaign.</span></span>

- <span data-ttu-id="53036-290">**Moyenne – Clic** : le temps total qu’il a fallu à tous les utilisateurs pour cliquer sur le lien, divisé par le nombre d’utilisateurs qui ont cliqué sur le lien.</span><span class="sxs-lookup"><span data-stu-id="53036-290">**Average Click**: The sum of how long it took everyone to click the link divided by the number of users who clicked the link.</span></span>

- <span data-ttu-id="53036-291">**Taux de réussite – Clic** : un pourcentage calculé par le (nombre d’utilisateurs qui ont cliqué sur le lien) / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="53036-291">**Click Success Rate**: A percentage that's calculated by (number of users who clicked the link) / **Total users targeted**.</span></span>

- <span data-ttu-id="53036-292">**Le plus rapide – Informations d’identification** : le temps qu’il a fallu au premier utilisateur pour entrer ses informations d’identification après le lancement de votre campagne.</span><span class="sxs-lookup"><span data-stu-id="53036-292">**Fastest Credentials**: How long it took the first user to enter their credentials after you launched the campaign.</span></span>

- <span data-ttu-id="53036-293">**Moyenne – Informations d’identification** : le temps total qu’il a fallu à tous les utilisateurs pour entrer leurs informations d’identification divisé par le nombre d’utilisateurs qui ont entré leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="53036-293">**Average Credentials**: The sum of how long it took everyone to enter their credentials divided by the number of users who entered their credentials.</span></span>

- <span data-ttu-id="53036-294">**Taux de réussite – Informations d’identification** : un pourcentage calculé par le (nombre d’utilisateurs qui ont entré leurs informations d’identification) / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="53036-294">**Credential Success Rate**: A percentage that's calculated by (number of users who entered their credentials) / **Total users targeted**.</span></span>

- <span data-ttu-id="53036-295">Graphique à barres affichant le **Lien sur lequel un clic a été effectué** et le nombre d’**Informations d’identification fournies** par jour.</span><span class="sxs-lookup"><span data-stu-id="53036-295">A bar graph that shows the **Link clicked** and **Credential supplied** numbers per day.</span></span>

- <span data-ttu-id="53036-296">Graphique circulaire affichant les pourcentages **Lien sur lequel un clic a été effectué**, **Informations d’identification fournies** et **Aucun** pour la campagne.</span><span class="sxs-lookup"><span data-stu-id="53036-296">A circle graph that shows the **Link clicked**, **Credential supplied**, and **None** percentages for the campaign.</span></span>

- <span data-ttu-id="53036-297">La section **Utilisateurs compromis** répertorie des informations sur les utilisateurs qui ont cliqué sur le lien :</span><span class="sxs-lookup"><span data-stu-id="53036-297">The **Compromised Users** section lists the details of the users who clicked the link:</span></span>

  - <span data-ttu-id="53036-298">L’adresse de messagerie de l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="53036-298">The user's email address</span></span>

  - <span data-ttu-id="53036-299">Date/heure à laquelle il a cliqué sur le lien.</span><span class="sxs-lookup"><span data-stu-id="53036-299">The date/time when they clicked the link.</span></span>

  - <span data-ttu-id="53036-300">L’adresse IP du client.</span><span class="sxs-lookup"><span data-stu-id="53036-300">The client IP address.</span></span>

  - <span data-ttu-id="53036-301">Détails sur la version de Windows et le navigateur web de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="53036-301">Details about the user's version of Windows and web browser.</span></span>

  <span data-ttu-id="53036-302">Vous pouvez cliquer sur **Exporter** pour exporter les résultats dans un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="53036-302">You can click **Export** to export the results to a CSV file.</span></span>

### <a name="spear-phishing-attachment-campaign-results"></a><span data-ttu-id="53036-303">Résultats de la campagne de harponnage (pièce jointe)</span><span class="sxs-lookup"><span data-stu-id="53036-303">Spear Phishing (Attachment) campaign results</span></span>

<span data-ttu-id="53036-304">Les informations suivantes sont disponibles sur la page des **Détails de l’attaque** pour chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="53036-304">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="53036-305">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="53036-305">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="53036-306">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="53036-306">**Total users targeted**</span></span>

- <span data-ttu-id="53036-307">**Tentatives réussies** : nombre d’utilisateurs qui ont ouvert ou téléchargé et ouvert la pièce jointe (l’aperçu ne compte pas).</span><span class="sxs-lookup"><span data-stu-id="53036-307">**Successful attempts**: The number of users who opened or downloaded and opened the attachment (preview doesn't count).</span></span>

- <span data-ttu-id="53036-308">**Taux de réussite globale** : un pourcentage calculé par **Tentatives réussies** / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="53036-308">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>

- <span data-ttu-id="53036-309">**Délai d’ouverture des pièces jointes le plus rapide** : le temps qu’il a fallu au premier utilisateur pour ouvrir la pièce jointe après le lancement de votre campagne.</span><span class="sxs-lookup"><span data-stu-id="53036-309">**Fastest attachment open time**: How long it took the first user to open the attachment after you launched the campaign.</span></span>

- <span data-ttu-id="53036-310">**Délai moyen d’ouverture des pièces jointes** : le temps total qu’il a fallu à tous les utilisateurs pour ouvrir la pièce jointe divisé par le nombre de personnes qui ont ouvert la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="53036-310">**Average attachment open time**: The sum of how long it took everyone to open the attachment divided by the number of users who opened the attachment.</span></span>

- <span data-ttu-id="53036-311">**Taux d’ouverture réussie des pièces jointes** : un pourcentage calculé par le (nombre d’utilisateurs qui ont ouvert la pièce jointe) / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="53036-311">**Attachment open success rate**: A percentage that's calculated by (number of users who opened the attachment) / **Total users targeted**.</span></span>

### <a name="brute-force-password-dictionary-attack-campaign-results"></a><span data-ttu-id="53036-312">Résultats de la campagne de mot de passe par force brute (attaque par dictionnaire)</span><span class="sxs-lookup"><span data-stu-id="53036-312">Brute Force Password (Dictionary Attack) campaign results</span></span>

<span data-ttu-id="53036-313">Les informations suivantes sont disponibles sur la page des **Détails de l’attaque** pour chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="53036-313">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="53036-314">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="53036-314">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="53036-315">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="53036-315">**Total users targeted**</span></span>

- <span data-ttu-id="53036-316">**Tentatives réussies** : nombre d’utilisateurs qui se sont avérées utiliser l’un des mots de passe spécifiés.</span><span class="sxs-lookup"><span data-stu-id="53036-316">**Successful attempts**: The number of users who were found to be using one of the specified passwords.</span></span>

- <span data-ttu-id="53036-317">**Taux de réussite globale** : un pourcentage calculé par **Tentatives réussies** / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="53036-317">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>

- <span data-ttu-id="53036-318">La section **Utilisateurs compromis** répertorie les adresses de courrier des utilisateurs concernés.</span><span class="sxs-lookup"><span data-stu-id="53036-318">The **Compromised Users** section lists the email addresses of the affected users.</span></span> <span data-ttu-id="53036-319">Vous pouvez cliquer sur **Exporter** pour exporter les résultats dans un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="53036-319">You can click **Export** to export the results to a CSV file.</span></span>

### <a name="password-spray-attack-campaign-results"></a><span data-ttu-id="53036-320">Résultats de la campagne d’attaque par pulvérisation par mots de passe</span><span class="sxs-lookup"><span data-stu-id="53036-320">Password spray attack campaign results</span></span>

<span data-ttu-id="53036-321">Les informations suivantes sont disponibles sur la page des **Détails de l’attaque** pour chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="53036-321">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="53036-322">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="53036-322">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="53036-323">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="53036-323">**Total users targeted**</span></span>

- <span data-ttu-id="53036-324">**Tentatives réussies** : nombre d’utilisateurs qui se sont avérées utiliser le mot de passe spécifié.</span><span class="sxs-lookup"><span data-stu-id="53036-324">**Successful attempts**: The number of users who were found to be using the specified password.</span></span>

- <span data-ttu-id="53036-325">**Taux de réussite globale** : un pourcentage calculé par **Tentatives réussies** / **Nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="53036-325">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>
