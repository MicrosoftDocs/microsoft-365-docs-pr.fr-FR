---
title: Simulateur d’attaque dans la protection avancée contre les menaces
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
description: En tant qu’administrateur général, vous pouvez utiliser un simulateur d’attaque pour exécuter des scénarios d’attaque réaliste dans votre organisation. Cela peut vous aider à identifier et à trouver des utilisateurs vulnérables avant qu’une attaque réelle ne touche votre entreprise.
ms.openlocfilehash: cac09ed48a46531ea2246f9c3ef798649dc73196
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43638571"
---
# <a name="attack-simulator-in-atp"></a><span data-ttu-id="c6c3b-104">Simulateur d’attaque dans la protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="c6c3b-104">Attack Simulator in ATP</span></span>

<span data-ttu-id="c6c3b-105">**Résumé** Si vous êtes un administrateur général ou un administrateur de la sécurité et que votre organisation a Office 365 Advanced Threat Protection Plan 2, qui inclut des [fonctionnalités d’enquête et de réponse aux menaces](office-365-ti.md), vous pouvez utiliser un simulateur d’attaque pour exécuter des scénarios d’attaque réaliste dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-105">**Summary** If you are a global administrator or a security administrator and your organization has Office 365 Advanced Threat Protection Plan 2, which includes [Threat Investigation and Response capabilities](office-365-ti.md), you can use Attack Simulator to run realistic attack scenarios in your organization.</span></span> <span data-ttu-id="c6c3b-106">Cela peut vous aider à identifier les utilisateurs vulnérables avant qu’une véritable attaque n’ait un impact sur votre chiffre d’affaires.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-106">This can help you identify and find vulnerable users before a real attack impacts your bottom line.</span></span> <span data-ttu-id="c6c3b-107">Lisez cet article pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-107">Read this article to learn more.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="c6c3b-108">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="c6c3b-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="c6c3b-109">Pour ouvrir le centre de sécurité & conformité, accédez <https://protection.office.com/>à.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-109">To open the Security & Compliance Center, go to <https://protection.office.com/>.</span></span> <span data-ttu-id="c6c3b-110">Le simulateur d’attaque est disponible dans le **simulateur d’attaques** **Threat Management** \> .</span><span class="sxs-lookup"><span data-stu-id="c6c3b-110">Attack simulator is available at **Threat management** \> **Attack simulator**.</span></span>

  ![Gestion des menaces-simulateur d’attaque](../../media/ThreatMgmt-AttackSimulator.png)

- <span data-ttu-id="c6c3b-112">Pour plus d’informations sur la disponibilité d’un simulateur d’attaque sur différents abonnements Microsoft 365, consultez la rubrique [Description du service protection avancée contre les menaces d’Office 365](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="c6c3b-112">For more information about the availability of Attack Simulator across different Microsoft 365 subscriptions, see [Office 365 Advanced Threat Protection service description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>

- <span data-ttu-id="c6c3b-113">Vous devez être membre des groupes de rôles **gestion** de l’organisation ou **administrateur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="c6c3b-113">You need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span> <span data-ttu-id="c6c3b-114">Pour plus d’informations sur les groupes de rôles dans le centre de sécurité & conformité, consultez [la rubrique autorisations dans le centre de sécurité & conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="c6c3b-114">For more information about role groups in the Security & Compliance Center, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="c6c3b-115">Votre compte doit être configuré pour l’authentification multifacteur (MFA) pour créer et gérer des campagnes dans un simulateur d’attaque.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-115">Your account needs to be configured for multi-factor authentication (MFA) to create and manage campaigns in Attack Simulator.</span></span> <span data-ttu-id="c6c3b-116">Pour obtenir des instructions, consultez la rubrique [set up Multi-Factor Authentication](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication).</span><span class="sxs-lookup"><span data-stu-id="c6c3b-116">For instructions, see [Set up multi-factor authentication](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication).</span></span>

<span data-ttu-id="c6c3b-117">Pour qu’une attaque réussisse, assurez-vous que le compte que vous utilisez pour exécuter des attaques simulées utilise l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-117">For an attack to be successfully launched, make sure that the account you are using to run simulated attacks is using multi-factor authentication.</span></span> <span data-ttu-id="c6c3b-118">En outre, vous devez être administrateur général ou administrateur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-118">In addition, you must be a global administrator or a security administrator.</span></span> <span data-ttu-id="c6c3b-119">(Pour en savoir plus sur les rôles et les autorisations, consultez [la rubrique autorisations dans le centre de sécurité & conformité](permissions-in-the-security-and-compliance-center.md)).</span><span class="sxs-lookup"><span data-stu-id="c6c3b-119">(To learn more about roles and permissions, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).)</span></span>

- <span data-ttu-id="c6c3b-120">Les campagnes de hameçonnage recueillent et traitent les événements pendant 30 jours.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-120">Phishing campaigns will collect and process events for 30 days.</span></span> <span data-ttu-id="c6c3b-121">Les données de la campagne historique seront disponibles pendant 90 jours après le lancement de la campagne.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-121">Historical campaign data will be available for up to 90 days after you launch the campaign.</span></span>

- <span data-ttu-id="c6c3b-122">Il n’existe pas d’applet de commande PowerShell correspondante pour un simulateur d’attaque.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-122">There are no corresponding PowerShell cmdlets for Attack Simulator.</span></span>

## <a name="spear-phishing-campaigns"></a><span data-ttu-id="c6c3b-123">Campagnes de phishing pour le Spear</span><span class="sxs-lookup"><span data-stu-id="c6c3b-123">Spear phishing campaigns</span></span>

<span data-ttu-id="c6c3b-124">Le *hameçonnage* est un terme générique pour les attaques par courrier électronique qui tentent de voler des informations sensibles dans les messages semblant provenir d’expéditeurs légitimes ou approuvés.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-124">*Phishing* is a generic term for email attacks that try to steal sensitive information in messages that appear to be from legitimate or trusted senders.</span></span> <span data-ttu-id="c6c3b-125">Le *Spear Phishing* est une attaque de hameçonnage ciblée qui utilise un contenu très ciblé et personnalisé qui est spécifiquement adapté aux destinataires ciblés (en général, après la reconnaissance des destinataires par l’agresseur).</span><span class="sxs-lookup"><span data-stu-id="c6c3b-125">*Spear phishing* is a targeted phishing attack that uses very focused and customized content that's specifically tailored to the targeted recipients (typically, after reconnaissance on the recipients by the attacker).</span></span>

- <span data-ttu-id="c6c3b-126">Vous êtes un administrateur général ou un administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="c6c3b-126">You are a global administrator or security administrator</span></span>

<span data-ttu-id="c6c3b-127">Dans un simulateur d’attaque, deux types différents de campagnes de Spear Phishing sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="c6c3b-127">In Attack Simulator, two different types of spear phishing campaigns are available:</span></span>

- <span data-ttu-id="c6c3b-128">L' [authentification multifacteur/l’accès conditionnel](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication) est activé, pour au moins le compte administrateur général et les administrateurs de sécurité qui utiliseront un simulateur d’attaque.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-128">[Multi-factor authentication/Conditional Access](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication) is turned on, for at least the global administrator account and security administrators who will be using Attack Simulator.</span></span> <span data-ttu-id="c6c3b-129">(Idéalement, l’accès à plusieurs facteurs/accès conditionnel est activé pour tous les utilisateurs de votre organisation.)</span><span class="sxs-lookup"><span data-stu-id="c6c3b-129">(Ideally, multi-factor authentication/conditional access is turned on for all users in your organization.)</span></span>

  - <span data-ttu-id="c6c3b-130">Page par défaut qui explique qu’il s’agissait d’un simple test et fournit des conseils pour la reconnaissance des messages de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-130">A default page that explains this was a just a test, and gives tips for recognizing phishing messages.</span></span>

    ![Ce que les utilisateurs voient s’ils cliquent sur le lien d’hameçonnage et entrent leurs informations d’identification](../../media/attack-simulator-phishing-result.png)

  - <span data-ttu-id="c6c3b-132">Une page personnalisée (URL) que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-132">A custom page (URL) that you specify.</span></span>

- <span data-ttu-id="c6c3b-133">**Spear Phishing (pièce jointe)**: l’attaque tente de convaincre les destinataires d’ouvrir une pièce jointe. docx ou. pdf dans le message.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-133">**Spear phishing (attachment)**: The attack tries to convince the recipients to open a .docx or .pdf attachment in the message.</span></span> <span data-ttu-id="c6c3b-134">La pièce jointe contient le même contenu que le lien de hameçonnage par défaut, mais la première phrase\<commence par\>« nom complet, vous voyez ce message en tant que message électronique récent que vous avez ouvert... ».</span><span class="sxs-lookup"><span data-stu-id="c6c3b-134">The attachment contains the same content from the default phishing link, but the first sentence starts with "\<Display Name\>, you are seeing this message as a recent email message you opened...".</span></span>

> [!NOTE]
> <span data-ttu-id="c6c3b-135">Actuellement, les campagnes de phishing de Spear dans un simulateur d’attaque n’expirent pas.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-135">Currently, spear phishing campaigns in Attack Simulator don't expire.</span></span>

### <a name="create-a-spear-phishing-campaign"></a><span data-ttu-id="c6c3b-136">Créer une campagne de phishing pour le Spear</span><span class="sxs-lookup"><span data-stu-id="c6c3b-136">Create a spear phishing campaign</span></span>

<span data-ttu-id="c6c3b-137">Une partie importante de toute campagne de hameçonnage est l’apparence du message électronique envoyé aux destinataires ciblés.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-137">An important part of any spear phishing campaign is the look and feel of the email message that's sent to the targeted recipients.</span></span> <span data-ttu-id="c6c3b-138">Pour créer et configurer le message électronique, vous disposez des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="c6c3b-138">To create and configure the email message, you have these options:</span></span>

- <span data-ttu-id="c6c3b-139">**Utilisez un modèle de courrier intégré**: les deux modèles prédéfinis sont disponibles : **prix des cadeaux** et **mise à jour**de la paie.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-139">**Use a built-in email template**: Two built-in templates are available: **Prize Giveaway** and **Payroll Update**.</span></span> <span data-ttu-id="c6c3b-140">Vous pouvez personnaliser davantage certaines, toutes ou aucune des propriétés de messagerie à partir du modèle lors de la création et du lancement de la campagne.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-140">You can further customize some, all, or none of the email properties from the template when you create and launch the campaign.</span></span>

- <span data-ttu-id="c6c3b-141">**Créer un modèle de courrier réutilisable**: après avoir créé et enregistré le modèle de courrier, vous pouvez le réutiliser dans les futures campagnes de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-141">**Create a reusable email template**: After you create and save the email template, you can use it again in future spear phishing campaigns.</span></span> <span data-ttu-id="c6c3b-142">Vous pouvez personnaliser davantage certaines, toutes ou aucune des propriétés de messagerie à partir du modèle lors de la création et du lancement de la campagne.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-142">You can further customize some, all, or none of the email properties from the template when you create and launch the campaign.</span></span>

- <span data-ttu-id="c6c3b-143">**Créer le message électronique dans l’Assistant**: vous pouvez créer le message électronique directement dans l’Assistant lors de la création et du lancement de la campagne de hameçonnage du Spear.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-143">**Create the email message in the wizard**: You can create the email message directly in the wizard as you create and launch the spear phishing campaign.</span></span>

#### <a name="step-1-optional-create-a-custom-email-template"></a><span data-ttu-id="c6c3b-144">Étape 1 (facultatif) : créer un modèle de courrier électronique personnalisé</span><span class="sxs-lookup"><span data-stu-id="c6c3b-144">Step 1 (Optional): Create a custom email template</span></span>

<span data-ttu-id="c6c3b-145">Si vous envisagez d’utiliser l’un des modèles intégrés ou de créer le message électronique directement dans l’Assistant, vous pouvez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-145">If you're going to use one of the built-in templates or create the email message directly in the wizard, you can skip this step.</span></span>

1. <span data-ttu-id="c6c3b-146">Dans le centre de sécurité & conformité, accédez à **Threat Management** \> **Attack Simulator**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-146">In the Security & Compliance Center, go to **Threat management** \> **Attack simulator**.</span></span>

2. <span data-ttu-id="c6c3b-147">Sur la page **simuler les attaques** , dans les sections **Spear Phishing (Credentials Harvest)** ou **Spear Phishing (pièce jointe)** , cliquez sur informations sur les **attaques**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-147">On the **Simulate attacks** page, in either the **Spear Phishing (Credentials Harvest)** or **Spear Phishing (Attachment)** sections, click **Attack Details**.</span></span>

   <span data-ttu-id="c6c3b-148">La création du modèle n’a pas d’importance.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-148">It doesn't matter where you create the template.</span></span> <span data-ttu-id="c6c3b-149">Les options disponibles dans le modèle sont les mêmes pour les deux types d’attaques par hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-149">The available options in the template are the same for both types of phishing attacks.</span></span>

3. <span data-ttu-id="c6c3b-150">Dans la page **Détails** de l’attaque qui s’ouvre, dans la section **modèles d’hameçonnage** , dans la zone créer des **modèles** , cliquez sur **nouveau modèle**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-150">In the **Attack details** page that opens, in the **Phishing Templates** section, in the **Create Templates** area, click **New Template**.</span></span>

4. <span data-ttu-id="c6c3b-151">L’Assistant **configurer le modèle d’hameçonnage** démarre dans une nouvelle fenêtre mobile.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-151">The **Configure Phishing Template** wizard starts in a new flyout.</span></span> <span data-ttu-id="c6c3b-152">À l’étape de **démarrage** , entrez un nom complet unique pour le modèle, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-152">In the **Start** step, enter a unique display name for the template, and then click **Next**.</span></span>

5. <span data-ttu-id="c6c3b-153">Dans l’étape **configurer les détails du courrier** , configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="c6c3b-153">In the **Configure email details** step, configure the following settings:</span></span>

   - <span data-ttu-id="c6c3b-154">**From (Name)**: nom complet utilisé pour l’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-154">**From (Name)**: The display name that's used for the message sender.</span></span>

   - <span data-ttu-id="c6c3b-155">**De (courrier électronique)**: adresse de messagerie de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-155">**From (Email)**: The sender's email address.</span></span>

   - <span data-ttu-id="c6c3b-156">**URL du serveur de connexion d’hameçonnage**: cliquez sur le menu déroulant et sélectionnez l’une des URL disponibles dans la liste.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-156">**Phishing Login Server URL**: Click the drop down and select one of the available URLs from the list.</span></span> <span data-ttu-id="c6c3b-157">Il s’agit de l’URL sur laquelle les utilisateurs seront tentés de cliquer.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-157">This is the URL that users will be tempted to click.</span></span> <span data-ttu-id="c6c3b-158">Les possibilités suivantes s'offrent à vous :</span><span class="sxs-lookup"><span data-stu-id="c6c3b-158">The choices are:</span></span>

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
     > <ul><li><span data-ttu-id="c6c3b-159">Toutes les URL sont intentionnellement http, et non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-159">All of the URLs are intentionally http, not https.</span></span></li><li><span data-ttu-id="c6c3b-160">Un service de réputation d’URL peut identifier une ou plusieurs de ces URL comme non sécurisées.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-160">A URL reputation service might identify one or more of these URLs as unsafe.</span></span> <span data-ttu-id="c6c3b-161">Vérifiez la disponibilité de l’URL dans vos navigateurs Web pris en charge avant d’utiliser l’URL d’une campagne de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-161">Check the availability of the URL in your supported web browsers before you use the URL in a phishing campaign.</span></span></li></ul>

   - <span data-ttu-id="c6c3b-162">**URL de la page d’accueil personnalisée**: entrez une page d’accueil facultative où les utilisateurs sont pris s’ils cliquent sur le lien d’hameçonnage et entrez leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-162">**Custom Landing Page URL**: Enter an optional landing page where users are taken if they click the phishing link and enter their credentials.</span></span> <span data-ttu-id="c6c3b-163">Ce lien remplace la page d’accueil par défaut.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-163">This link replaces the default landing page.</span></span> <span data-ttu-id="c6c3b-164">Par exemple, si vous avez une formation interne à la sensibilisation, vous pouvez spécifier cette URL ici.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-164">For example, if you have internal awareness training, you can specify that URL here.</span></span>

   - <span data-ttu-id="c6c3b-165">**Catégorie**: actuellement, ce paramètre n’est pas utilisé (tout ce que vous entrez n’est pas pris en compte).</span><span class="sxs-lookup"><span data-stu-id="c6c3b-165">**Category**: Currently, this setting isn't used (anything you enter is ignored).</span></span>

   - <span data-ttu-id="c6c3b-166">**Subject**: champ **Subject** du message électronique.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-166">**Subject**: The **Subject** field of the email message.</span></span>

   <span data-ttu-id="c6c3b-167">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-167">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="c6c3b-168">Dans l’étape **composer un courrier électronique** , créez le corps du message électronique.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-168">In the **Compose email** step, create the message body of the email message.</span></span> <span data-ttu-id="c6c3b-169">Vous pouvez utiliser l’onglet **messagerie** (éditeur HTML enrichi) ou l’onglet **source** (code HTML brut).</span><span class="sxs-lookup"><span data-stu-id="c6c3b-169">You can use the **Email** tab (a rich HTML editor) or the **Source** tab (raw HTML code).</span></span>

   <span data-ttu-id="c6c3b-170">La mise en forme HTML peut être simple ou complexe, comme vous en avez besoin.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-170">The HTML formatting can be as simple or complex as you need it to be.</span></span> <span data-ttu-id="c6c3b-171">Vous pouvez insérer des images et du texte pour améliorer la convivialité du message dans le client de messagerie du destinataire.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-171">You can insert images and text to enhance the believability of the message in the recipient's email client.</span></span>

   - <span data-ttu-id="c6c3b-172">`${username}`insère le nom du destinataire.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-172">`${username}` inserts the recipient's name.</span></span>

   - <span data-ttu-id="c6c3b-173">`${loginserverurl}`insère la valeur de l' **URL du serveur de connexion de hameçonnage** à partir de l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-173">`${loginserverurl}` inserts the **Phishing Login Server URL** value from the previous step.</span></span>

   <span data-ttu-id="c6c3b-174">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-174">When you're finished, click **Next**.</span></span>

7. <span data-ttu-id="c6c3b-175">Dans l’étape **confirmer** , cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-175">In the **Confirm** step, click **Finish**.</span></span>

#### <a name="step-2-create-and-launch-the-spear-phishing-campaign"></a><span data-ttu-id="c6c3b-176">Étape 2 : créer et lancer la campagne de hameçonnage de la sonde</span><span class="sxs-lookup"><span data-stu-id="c6c3b-176">Step 2: Create and launch the spear phishing campaign</span></span>

1. <span data-ttu-id="c6c3b-177">Dans le centre de sécurité & conformité, accédez à **Threat Management** \> **Attack Simulator**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-177">In the Security & Compliance Center, go to **Threat management** \> **Attack simulator**.</span></span>

2. <span data-ttu-id="c6c3b-178">Sur la page **simuler des attaques** , effectuez l’une des sélections suivantes en fonction du type de campagne que vous souhaitez créer :</span><span class="sxs-lookup"><span data-stu-id="c6c3b-178">On the **Simulate attacks** page, make one of the following selections based on the type of campaign you want to create:</span></span>

   - <span data-ttu-id="c6c3b-179">Dans la section **Spear Phishing (informations d’identification)** , cliquez sur **lancer une attaque** ou **sur attaquer les** **Détails** \> de l’attaque.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-179">In the **Spear Phishing (Credentials Harvest)** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

   - <span data-ttu-id="c6c3b-180">Dans la **section Spear Phishing (pièce jointe)** , cliquez sur **lancer une attaque** ou \> sur attaques pour **lancer** **une attaque.**</span><span class="sxs-lookup"><span data-stu-id="c6c3b-180">In the **Spear Phishing (Attachment)** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

3. <span data-ttu-id="c6c3b-181">L’Assistant **configurer une attaque de hameçonnage** démarre dans une nouvelle fenêtre mobile.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-181">The **Configure Phishing Attack** wizard starts in a new flyout.</span></span> <span data-ttu-id="c6c3b-182">Dans l’étape de **démarrage** , effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c6c3b-182">In the **Start** step, do one of the following steps:</span></span>

   - <span data-ttu-id="c6c3b-183">Dans la zone **nom** , entrez un nom complet unique pour la campagne.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-183">In the **Name** box, enter a unique display name for the campaign.</span></span> <span data-ttu-id="c6c3b-184">Ne cliquez pas sur **utiliser le modèle**, car vous allez créer le message électronique plus tard dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-184">Don't click **Use Template**, because you'll create the email message later in the wizard.</span></span>

   - <span data-ttu-id="c6c3b-185">Cliquez sur **utiliser le modèle** et sélectionnez un modèle de courrier intégré ou personnalisé.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-185">Click **Use Template** and select a built-in or custom email template.</span></span> <span data-ttu-id="c6c3b-186">Une fois que vous avez sélectionné le modèle, la zone **nom** est automatiquement remplie en fonction du modèle, mais vous pouvez modifier le nom.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-186">After you select the template, the **Name** box is automatically filled based on the template, but you can change the name.</span></span>

   ![Page de démarrage du hameçonnage](../../media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)

   <span data-ttu-id="c6c3b-188">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-188">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="c6c3b-189">Dans l’étape **destinataires cibles** , effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c6c3b-189">In the **Target recipients** step, do one of the following steps:</span></span>

   - <span data-ttu-id="c6c3b-190">Cliquez sur **carnet d’adresses** pour sélectionner les destinataires (utilisateurs ou groupes) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-190">Click **Address Book** to select the recipients (users or groups) for the campaign.</span></span> <span data-ttu-id="c6c3b-191">Chaque destinataire ciblé doit disposer d’une boîte aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-191">Each targeted recipient must have an Exchange Online mailbox.</span></span> <span data-ttu-id="c6c3b-192">Si vous cliquez sur **Filtrer** et **appliquer** sans entrer de critère de recherche, tous les destinataires sont renvoyés et ajoutés à la campagne.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-192">If you click **Filter** and **Apply** without entering a search criteria, all recipients are returned and added to the campaign.</span></span>

   - <span data-ttu-id="c6c3b-193">Cliquez sur **Importer** , puis sur **importation de fichiers** pour importer un fichier de valeurs séparées par des virgules (CSV) ou séparé par une ligne d’adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-193">Click **Import** then **File Import** to import a comma-separated value (CSV) or line-separated file of email addresses.</span></span> <span data-ttu-id="c6c3b-194">Chaque ligne doit contenir l’adresse de messagerie du destinataire.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-194">Each line must contain the recipient's email address.</span></span>

   <span data-ttu-id="c6c3b-195">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-195">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="c6c3b-196">Dans l’étape **configurer les détails du courrier** , configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="c6c3b-196">In the **Configure email details** step, configure the following settings:</span></span>

   <span data-ttu-id="c6c3b-197">Si vous avez sélectionné un modèle dans l’étape de **démarrage** , la plupart de ces valeurs sont déjà configurées, mais vous pouvez les modifier.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-197">If you selected a template in the **Start** step, most of these values are already configured, but you can change them.</span></span>

   - <span data-ttu-id="c6c3b-198">**From (Name)**: nom complet utilisé pour l’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-198">**From (Name)**: The display name that's used for the message sender.</span></span>

   - <span data-ttu-id="c6c3b-199">**De (courrier électronique)**: adresse de messagerie de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-199">**From (Email)**: The sender's email address.</span></span> <span data-ttu-id="c6c3b-200">Vous pouvez entrer une adresse de messagerie réelle ou fictive à partir du domaine de messagerie de votre organisation, ou vous pouvez entrer une adresse de messagerie externe réelle ou fictive.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-200">You can enter a real or fake email address from your organization's email domain, or you can enter a real or fake external email address.</span></span> <span data-ttu-id="c6c3b-201">Une adresse de messagerie d’expéditeur valide de votre organisation est en fait résolue dans le client de messagerie du destinataire.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-201">A valid sender email address from your organization will actually resolve in the recipient's email client.</span></span>

   - <span data-ttu-id="c6c3b-202">**URL du serveur de connexion d’hameçonnage**: cliquez sur le menu déroulant et sélectionnez l’une des URL disponibles dans la liste.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-202">**Phishing Login Server URL**: Click the drop down and select one of the available URLs from the list.</span></span> <span data-ttu-id="c6c3b-203">Il s’agit de l’URL sur laquelle les utilisateurs seront tentés de cliquer.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-203">This is the URL that users will be tempted to click.</span></span> <span data-ttu-id="c6c3b-204">Les possibilités suivantes s'offrent à vous :</span><span class="sxs-lookup"><span data-stu-id="c6c3b-204">The choices are:</span></span>

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
     > <ul><li><span data-ttu-id="c6c3b-205">Toutes les URL sont intentionnellement http, et non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-205">All of the URLs are intentionally http, not https.</span></span></li><li><span data-ttu-id="c6c3b-206">Un service de réputation d’URL peut identifier une ou plusieurs de ces URL comme non sécurisées.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-206">A URL reputation service might identify one or more of these URLs as unsafe.</span></span> <span data-ttu-id="c6c3b-207">Vérifiez la disponibilité de l’URL dans vos navigateurs Web pris en charge avant d’utiliser l’URL d’une campagne de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-207">Check the availability of the URL in your supported web browsers before you use the URL in a phishing campaign.</span></span></li><li><span data-ttu-id="c6c3b-208">Vous devez sélectionner une URL.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-208">You are required to select a URL.</span></span> <span data-ttu-id="c6c3b-209">Pour les campagnes de <b>hameçonnage (de pièces jointes)</b> , vous pouvez supprimer le lien du corps du message à l’étape suivante (dans le cas contraire, le message contiendra un lien <b>et</b> une pièce jointe).</span><span class="sxs-lookup"><span data-stu-id="c6c3b-209">For <b>Spear Phishing (Attachment)</b> campaigns, you can remove the link from the body of the message in the next step (otherwise, the message will contain both a link <b>and</b> an attachment).</span></span></li></ul>

   - <span data-ttu-id="c6c3b-210">**Type de pièce jointe**: ce paramètre est disponible uniquement dans les campagnes de **hameçonnage (de pièces jointes)** .</span><span class="sxs-lookup"><span data-stu-id="c6c3b-210">**Attachment Type**: This setting is only available in **Spear Phishing (Attachment)** campaigns.</span></span> <span data-ttu-id="c6c3b-211">Cliquez sur le menu déroulant et sélectionnez **. DOCX** ou **. PDF** à partir de la liste.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-211">Click the drop down and select **.DOCX** or **.PDF** from the list.</span></span>

   - <span data-ttu-id="c6c3b-212">**Nom de la pièce jointe**: ce paramètre est disponible uniquement dans les campagnes de **hameçonnage (de pièces jointes)** .</span><span class="sxs-lookup"><span data-stu-id="c6c3b-212">**Attachment Name**: This setting is only available in **Spear Phishing (Attachment)** campaigns.</span></span> <span data-ttu-id="c6c3b-213">Entrez un nom de fichier pour la pièce jointe. docx ou. pdf.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-213">Enter a filename for the .docx or .pdf attachment.</span></span>

   - <span data-ttu-id="c6c3b-214">**URL de la page d’accueil personnalisée**: entrez une page d’accueil facultative où les utilisateurs sont pris s’ils cliquent sur le lien d’hameçonnage et entrez leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-214">**Custom Landing Page URL**: Enter an optional landing page where users are taken if they click the phishing link and enter their credentials.</span></span> <span data-ttu-id="c6c3b-215">Ce lien remplace la page d’accueil par défaut.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-215">This link replaces the default landing page.</span></span> <span data-ttu-id="c6c3b-216">Par exemple, si vous avez une formation interne à la sensibilisation, vous pouvez spécifier cette URL ici.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-216">For example, if you have internal awareness training, you can specify that URL here.</span></span>

   - <span data-ttu-id="c6c3b-217">**Subject**: champ **Subject** du message électronique.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-217">**Subject**: The **Subject** field of the email message.</span></span>

   <span data-ttu-id="c6c3b-218">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-218">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="c6c3b-219">Dans l’étape **composer un courrier électronique** , créez le corps du message électronique.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-219">In the **Compose email** step, create the message body of the email message.</span></span> <span data-ttu-id="c6c3b-220">Si vous avez sélectionné un modèle dans l’étape de **démarrage** , le corps du message est déjà configuré, mais vous pouvez le personnaliser.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-220">If you selected a template in the **Start** step, the message body is already configured, but you can customize it.</span></span> <span data-ttu-id="c6c3b-221">Vous pouvez utiliser l’onglet **messagerie** (éditeur HTML enrichi) ou l’onglet **source** (code HTML brut).</span><span class="sxs-lookup"><span data-stu-id="c6c3b-221">You can use the **Email** tab (a rich HTML editor) or the **Source** tab (raw HTML code).</span></span>

   <span data-ttu-id="c6c3b-222">La mise en forme HTML peut être simple ou complexe, comme vous en avez besoin.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-222">The HTML formatting can be as simple or complex as you need it to be.</span></span> <span data-ttu-id="c6c3b-223">Vous pouvez insérer des images et du texte pour améliorer la convivialité du message dans le client de messagerie du destinataire.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-223">You can insert images and text to enhance the believability of the message in the recipient's email client.</span></span>

   - <span data-ttu-id="c6c3b-224">`${username}`insère le nom du destinataire.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-224">`${username}` inserts the recipient's name.</span></span>

   - <span data-ttu-id="c6c3b-225">`${loginserverurl}`insère la valeur de l' **URL du serveur de connexion de hameçonnage** .</span><span class="sxs-lookup"><span data-stu-id="c6c3b-225">`${loginserverurl}` inserts the **Phishing Login Server URL** value.</span></span>

   <span data-ttu-id="c6c3b-226">Pour les campagnes de **hameçonnage (de pièces jointes)** , vous devez supprimer le lien du corps du message (dans le cas contraire, le message contient à la fois un lien **et** une pièce jointe, et les clics de liens ne sont pas suivis dans une campagne de pièces jointes).</span><span class="sxs-lookup"><span data-stu-id="c6c3b-226">For **Spear Phishing (Attachment)** campaigns, you should remove the link from the body of the message (otherwise, the message will contain both a link **and** an attachment, and link clicks aren't tracked in an attachment campaign).</span></span>

   ![Composer le corps du message électronique](../../media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)

   <span data-ttu-id="c6c3b-228">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-228">When you're finished, click **Next**.</span></span>

7. <span data-ttu-id="c6c3b-229">Dans l’étape **confirmer** , cliquez sur **Terminer** pour lancer la campagne.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-229">In the **Confirm** step, click **Finish** to launch the campaign.</span></span> <span data-ttu-id="c6c3b-230">Le message de hameçonnage est remis aux destinataires ciblés.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-230">The phishing message is delivered to the targeted recipients.</span></span>

## <a name="password-attack-campaigns"></a><span data-ttu-id="c6c3b-231">Campagnes d’attaque par mot de passe</span><span class="sxs-lookup"><span data-stu-id="c6c3b-231">Password attack campaigns</span></span>

<span data-ttu-id="c6c3b-232">Une *attaque par mot de passe* tente de deviner les mots de passe des comptes d’utilisateur d’une organisation, généralement après que l’agresseur a identifié un ou plusieurs comptes d’utilisateurs valides.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-232">A *password attack* tries to guess passwords for user accounts in an organization, typically after the attacker has identified one or more valid user accounts.</span></span>

<span data-ttu-id="c6c3b-233">Dans un simulateur d’attaque, deux types différents de campagnes d’attaque de mot de passe sont disponibles pour vous permettre de tester la complexité des mots de passe des utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="c6c3b-233">In Attack Simulator, two different types of password attack campaigns are available for you to test the complexity of your users' passwords:</span></span>

- <span data-ttu-id="c6c3b-234">**Mot de passe en force (attaque de dictionnaire)**: une attaque en *force ou une* attaque de *dictionnaire* utilise un fichier dictionnaire volumineux de mots de passe sur un compte d’utilisateur en espérant que l’un d’entre eux fonctionnera (de nombreux mots de passe par rapport à un compte).</span><span class="sxs-lookup"><span data-stu-id="c6c3b-234">**Brute force password (dictionary attack)**: A *brute force* or *dictionary* attack uses a large dictionary file of passwords on a user account with the hope that one of them will work (many passwords against one account).</span></span> <span data-ttu-id="c6c3b-235">Le verrouillage de mot de passe incorrect permet de dissuader les attaques de mot de passe en force.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-235">Incorrect password lock-outs help deter brute force password attacks.</span></span>

  <span data-ttu-id="c6c3b-236">Pour l’attaque de dictionnaire, vous pouvez spécifier un ou plusieurs mots de passe à essayer (entrés manuellement ou dans un fichier téléchargé) et vous pouvez spécifier un ou plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-236">For the dictionary attack, you can specify one or many passwords to try (manually entered or in an uploaded file), and you can specify one or many users.</span></span>

- <span data-ttu-id="c6c3b-237">**Attaque par pulvérisation de mot de passe**: une attaque par *pulvérisation de mot de passe* utilise le même mot de passe soigneusement considéré avec une liste de comptes d’utilisateurs (un mot de passe par rapport à de nombreux comptes).</span><span class="sxs-lookup"><span data-stu-id="c6c3b-237">**Password spray attack**: A *password spray* attack uses the same carefully considered password against a list of user accounts (one password against many accounts).</span></span> <span data-ttu-id="c6c3b-238">Les attaques par pulvérisation de mot de passe sont plus difficiles à détecter que les attaques de mot de passe en force (la probabilité de réussite augmente lorsqu’un agresseur tente un mot de passe entre des dizaines ou des centaines de comptes sans risque de faire passer le verrouillage incorrect du mot de passe de l’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="c6c3b-238">Password spray attacks are harder to detect than brute force password attacks (the probability of success increases when an attacker tries one password across dozens or hundreds of accounts without the risk of tripping the user's incorrect password lock-out).</span></span>

  <span data-ttu-id="c6c3b-239">Pour l’attaque par pulvérisation par mot de passe, vous ne pouvez spécifier qu’un seul mot de passe à essayer et vous pouvez spécifier un ou plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-239">For the password spray attack, you can only specify one password to try, and you can specify one or many users.</span></span>

> [!NOTE]
> <span data-ttu-id="c6c3b-240">Les attaques de mot de passe dans le simulateur de test du nom d’utilisateur et du mot de passe des demandes d’authentification de base à un point de terminaison fonctionnent également avec d’autres méthodes d’authentification (AD FS, synchronisation de hachage de mot de passe, direct, PingFederate, etc.).</span><span class="sxs-lookup"><span data-stu-id="c6c3b-240">The password attacks in Attack Simulator pass username and password Basic auth requests to an endpoint, so they also work with other authentication methods (AD FS, password hash sync, pass-through, PingFederate, etc.).</span></span> <span data-ttu-id="c6c3b-241">Pour les utilisateurs pour lesquels l’authentification multifacteur (MFA) est activée, même si l’attaque par mot de passe essaie son mot de passe réel, la tentative s’inscrit toujours comme un échec (en d’autres termes, les utilisateurs MFA n’apparaissent jamais dans le nombre de **tentatives réussies** de la campagne).</span><span class="sxs-lookup"><span data-stu-id="c6c3b-241">For users that have MFA enabled, even if the password attack tries their actual password, the attempt will always register as a failure (in other words, MFA users will never appear in the **Successful attempts** count of the campaign).</span></span> <span data-ttu-id="c6c3b-242">Il s’agit du résultat attendu.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-242">This is the expected result.</span></span> <span data-ttu-id="c6c3b-243">MFA est une méthode principale pour vous protéger contre les attaques par mot de passe.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-243">MFA is a primary method to help protect against password attacks.</span></span>

### <a name="create-and-launch-a-password-attack-campaign"></a><span data-ttu-id="c6c3b-244">Créer et lancer une campagne d’attaque par mot de passe</span><span class="sxs-lookup"><span data-stu-id="c6c3b-244">Create and launch a password attack campaign</span></span>

1. <span data-ttu-id="c6c3b-245">Dans le centre de sécurité & conformité, accédez à **Threat Management** \> **Attack Simulator**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-245">In the Security & Compliance Center, go to **Threat management** \> **Attack simulator**.</span></span>

2. <span data-ttu-id="c6c3b-246">Sur la page **simuler des attaques** , effectuez l’une des sélections suivantes en fonction du type de campagne que vous souhaitez créer :</span><span class="sxs-lookup"><span data-stu-id="c6c3b-246">On the **Simulate attacks** page, make one of the following selections based on the type of campaign you want to create:</span></span>

   - <span data-ttu-id="c6c3b-247">Dans la **section mot de passe en force (attaque de dictionnaire)** , cliquez sur **lancer une attaque** ou sur attaque des **Détails** \> de l' **attaque.**</span><span class="sxs-lookup"><span data-stu-id="c6c3b-247">In the **Brute Force Password (Dictionary Attack)** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

   - <span data-ttu-id="c6c3b-248">dans la section **attaque par pulvérisation par mot de passe** , cliquez sur lancer une **attaque** **ou sur** \> attaques pour **lancer**une attaque.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-248">in the **Password spray attack** section, click **Launch Attack** or click **Attack Details** \> **Launch Attack**.</span></span>

3. <span data-ttu-id="c6c3b-249">L’Assistant Configuration d’une **attaque de mot de passe** démarre dans une nouvelle fenêtre mobile.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-249">The **Configure Password Attack** wizard starts in a new flyout.</span></span> <span data-ttu-id="c6c3b-250">À l’étape de **démarrage** , entrez un nom complet unique pour la campagne, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-250">In the **Start** step, enter a unique display name for the campaign, and then click **Next**.</span></span>

4. <span data-ttu-id="c6c3b-251">Dans l’étape **utilisateurs cibles** , effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c6c3b-251">In the **Target users** step, do one of the following steps:</span></span>

   - <span data-ttu-id="c6c3b-252">Cliquez sur **carnet d’adresses** pour sélectionner les destinataires (utilisateurs ou groupes) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-252">Click **Address Book** to select the recipients (users or groups) for the campaign.</span></span> <span data-ttu-id="c6c3b-253">Chaque destinataire ciblé doit disposer d’une boîte aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-253">Each targeted recipient must have an Exchange Online mailbox.</span></span> <span data-ttu-id="c6c3b-254">Si vous cliquez sur **Filtrer** et **appliquer** sans entrer de critère de recherche, tous les destinataires sont renvoyés et ajoutés à la campagne.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-254">If you click **Filter** and **Apply** without entering a search criteria, all recipients are returned and added to the campaign.</span></span>

   - <span data-ttu-id="c6c3b-255">Cliquez sur **Importer** , puis sur **importation de fichiers** pour importer un fichier de valeurs séparées par des virgules (CSV) ou séparé par une ligne d’adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-255">Click **Import** then **File Import** to import a comma-separated value (CSV) or line-separated file of email addresses.</span></span> <span data-ttu-id="c6c3b-256">Chaque ligne doit contenir l’adresse de messagerie du destinataire.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-256">Each line must contain the recipient's email address.</span></span>

   <span data-ttu-id="c6c3b-257">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-257">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="c6c3b-258">Dans l’étape **choisir les paramètres d’attaque** , choisissez ce qu’il faut faire en fonction du type de campagne :</span><span class="sxs-lookup"><span data-stu-id="c6c3b-258">In the **Choose attack settings** step, choose what to do based on the campaign type:</span></span>

   - <span data-ttu-id="c6c3b-259">**Mot de passe en force (attaque de dictionnaire)**: effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c6c3b-259">**Brute Force Password (Dictionary Attack)**: Do either of the following steps:</span></span>

     - <span data-ttu-id="c6c3b-260">**Entrez les mots de passe manuellement**: dans la zone **Appuyez sur entrée pour ajouter un mot de passe** , tapez un mot de passe, puis appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-260">**Enter passwords manually**: In the **Press enter to add a password** box, type a password and then press ENTER.</span></span> <span data-ttu-id="c6c3b-261">Répétez cette étape autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-261">Repeat this step as many times as necessary.</span></span>

     - <span data-ttu-id="c6c3b-262">**Charger les mots de passe à partir d’un fichier de dictionnaire**: cliquez sur **Télécharger** pour importer un fichier texte existant qui contient un mot de passe sur chaque ligne et une dernière ligne vide.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-262">**Upload passwords from a dictionary file**: Click **Upload** to import an existing text file that contains one password on each line and a blank last line.</span></span> <span data-ttu-id="c6c3b-263">La taille du fichier texte doit être inférieure ou égale à 10 Mo et ne peut pas contenir plus de 30000 mots de passe.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-263">The text file must be 10 MB or less in size, and can't contain more than 30000 passwords.</span></span>

   - <span data-ttu-id="c6c3b-264">**Attaque par pulvérisation de mot de passe**: dans **le champ mot de passe à utiliser dans la zone attaque** , entrez un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-264">**Password spray attack**: In **The password(s) to use in the attack** box, enter one password.</span></span>

   <span data-ttu-id="c6c3b-265">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-265">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="c6c3b-266">Dans l’étape **confirmer** , cliquez sur **Terminer** pour lancer la campagne.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-266">In the **Confirm** step, click **Finish** to launch the campaign.</span></span> <span data-ttu-id="c6c3b-267">Les mots de passe que vous avez spécifiés sont testés sur les utilisateurs que vous avez spécifiés.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-267">The passwords you specified are tried on users you specified.</span></span>

## <a name="view-campaign-results"></a><span data-ttu-id="c6c3b-268">Afficher les résultats de la campagne</span><span class="sxs-lookup"><span data-stu-id="c6c3b-268">View campaign results</span></span>

<span data-ttu-id="c6c3b-269">Une fois que vous avez lancé une campagne, vous pouvez vérifier la progression et les résultats sur la page principale **attaques par simulation** .</span><span class="sxs-lookup"><span data-stu-id="c6c3b-269">After you launch a campaign, you can check the progress and results on the main **Simulate attacks** page.</span></span>

<span data-ttu-id="c6c3b-270">Les campagnes actives affichent une barre d’État, une valeur de pourcentage terminé et le nombre de (utilisateurs terminés) de (nombre total d’utilisateurs).</span><span class="sxs-lookup"><span data-stu-id="c6c3b-270">Active campaigns will show a status bar, a completed percentage value and "(completed users) of (total users)" count.</span></span> <span data-ttu-id="c6c3b-271">Cliquez sur le bouton **Actualiser** pour mettre à jour la progression de toutes les campagnes actives.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-271">Clicking the **Refresh** button will update the progress of any active campaigns.</span></span> <span data-ttu-id="c6c3b-272">Vous pouvez également cliquer sur **Terminer** pour arrêter une campagne active.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-272">You can also click **Terminate** to stop an active campaign.</span></span>

<span data-ttu-id="c6c3b-273">Une fois la campagne terminée, l’État devient **attaque terminée**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-273">When the campaign is finished, the status changes to **Attack completed**.</span></span> <span data-ttu-id="c6c3b-274">Vous pouvez afficher les résultats de la campagne en effectuant l’une des actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="c6c3b-274">You can view the results of the campaign by doing either of the following actions:</span></span>

- <span data-ttu-id="c6c3b-275">Sur la page principale **attaques de simulation** , cliquez sur Afficher le **rapport** sous le nom de la campagne.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-275">On the main **Simulate attacks** page, click **View Report** under the name of the campaign.</span></span>

- <span data-ttu-id="c6c3b-276">Sur la page principale **attaques de simulation** , cliquez sur informations sur les **attaques** dans la section correspondant au type d’attaque.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-276">On the main **Simulate attacks** page, click **Attack Details** in the section for the type of attack.</span></span> <span data-ttu-id="c6c3b-277">Sur la page Détails de l' **attaque** qui s’ouvre, sélectionnez la campagne dans la section **historique des attaques** .</span><span class="sxs-lookup"><span data-stu-id="c6c3b-277">On the **Attack details** page that opens, select the campaign in the **Attack History** section.</span></span>

<span data-ttu-id="c6c3b-278">L’une des actions précédentes vous permet d’accéder à une page intitulée **informations d’attaque**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-278">Either of the previous actions will take you to a page named **Attack details**.</span></span> <span data-ttu-id="c6c3b-279">Les informations qui sont disponibles sur cette page pour chaque type de campagne sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-279">The information that's available on this page for each type of campaign is described in the following sections.</span></span>

### <a name="spear-phishing-credentials-harvest-campaign-results"></a><span data-ttu-id="c6c3b-280">Résultats de la campagne de Spear Phishing (informations d’identification)</span><span class="sxs-lookup"><span data-stu-id="c6c3b-280">Spear Phishing (Credentials Harvest) campaign results</span></span>

<span data-ttu-id="c6c3b-281">Les informations suivantes sont disponibles dans la page Détails de l' **attaque** de chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="c6c3b-281">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="c6c3b-282">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-282">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="c6c3b-283">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="c6c3b-283">**Total users targeted**</span></span>

- <span data-ttu-id="c6c3b-284">**Tentatives réussies**: nombre d’utilisateurs ayant cliqué sur le lien **et** entré leurs informations d’identification (*n’importe quel* nom d’utilisateur et mot de passe).</span><span class="sxs-lookup"><span data-stu-id="c6c3b-284">**Successful attempts**: The number of users who clicked the link **and** entered their credentials (*any* username and password value).</span></span>

- <span data-ttu-id="c6c3b-285">**Taux de réussite global**: pourcentage calculé en / **nombre total d’utilisateurs ciblés**par des **tentatives réussies**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-285">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>

- <span data-ttu-id="c6c3b-286">Le **plus rapide**est de cliquer sur le lien après avoir lancé la campagne.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-286">**Fastest Click**: How long it took the first user to click the link after you launched the campaign.</span></span>

- <span data-ttu-id="c6c3b-287">**Moyenne : cliquez sur**le nombre de fois que tout le monde a pris le temps de cliquer sur le lien, divisé par le nombre d’utilisateurs ayant cliqué sur le lien.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-287">**Average Click**: The sum of how long it took everyone to click the link divided by the number of users who clicked the link.</span></span>

- <span data-ttu-id="c6c3b-288">**Cliquez sur taux de réussite**: pourcentage calculé par (nombre d’utilisateurs ayant cliqué sur le lien)/ **nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-288">**Click Success Rate**: A percentage that's calculated by (number of users who clicked the link) / **Total users targeted**.</span></span>

- <span data-ttu-id="c6c3b-289">**Informations d’identification les plus rapides**: combien de temps a duré le premier utilisateur pour entrer ses informations d’identification après avoir lancé la campagne.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-289">**Fastest Credentials**: How long it took the first user to enter their credentials after you launched the campaign.</span></span>

- <span data-ttu-id="c6c3b-290">**Moyenne des informations d’identification**: somme du temps nécessaire à l’utilisateur pour entrer ses informations d’identification divisée par le nombre d’utilisateurs qui ont entré leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-290">**Average Credentials**: The sum of how long it took everyone to enter their credentials divided by the number of users who entered their credentials.</span></span>

- <span data-ttu-id="c6c3b-291">**Taux de réussite des informations d’identification**: pourcentage calculé par (nombre d’utilisateurs qui ont entré leurs informations d’identification)/ **nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-291">**Credential Success Rate**: A percentage that's calculated by (number of users who entered their credentials) / **Total users targeted**.</span></span>

- <span data-ttu-id="c6c3b-292">Graphique à barres qui affiche le **lien sur lequel l’utilisateur a cliqué** et les numéros **d’identification fournis** par jour.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-292">A bar graph that shows the **Link clicked** and **Credential supplied** numbers per day.</span></span>

- <span data-ttu-id="c6c3b-293">Graphique circulaire qui affiche le **lien sur lequel l’utilisateur a cliqué**, les **informations d’identification fournies**et **aucun** pourcentage de la campagne.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-293">A circle graph that shows the **Link clicked**, **Credential supplied**, and **None** percentages for the campaign.</span></span>

- <span data-ttu-id="c6c3b-294">La section **utilisateurs compromis** répertorie les détails des utilisateurs qui ont cliqué sur le lien :</span><span class="sxs-lookup"><span data-stu-id="c6c3b-294">The **Compromised Users** section lists the details of the users who clicked the link:</span></span>

  - <span data-ttu-id="c6c3b-295">Adresse de messagerie de l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="c6c3b-295">The user's email address</span></span>

  - <span data-ttu-id="c6c3b-296">Date/heure à laquelle l’utilisateur a cliqué sur le lien.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-296">The date/time when they clicked the link.</span></span>

  - <span data-ttu-id="c6c3b-297">Adresse IP du client.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-297">The client IP address.</span></span>

  - <span data-ttu-id="c6c3b-298">Détails sur la version de l’utilisateur de Windows et du navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-298">Details about the user's version of Windows and web browser.</span></span>

  <span data-ttu-id="c6c3b-299">Vous pouvez cliquer sur **Exporter** pour exporter les résultats dans un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-299">You can click **Export** to export the results to a CSV file.</span></span>

### <a name="spear-phishing-attachment-campaign-results"></a><span data-ttu-id="c6c3b-300">Résultats de la campagne de hameçonnage (pièce jointe)</span><span class="sxs-lookup"><span data-stu-id="c6c3b-300">Spear Phishing (Attachment) campaign results</span></span>

<span data-ttu-id="c6c3b-301">Les informations suivantes sont disponibles dans la page Détails de l' **attaque** de chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="c6c3b-301">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="c6c3b-302">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-302">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="c6c3b-303">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="c6c3b-303">**Total users targeted**</span></span>

- <span data-ttu-id="c6c3b-304">**Tentatives réussies**: nombre d’utilisateurs qui ont ouvert ou téléchargé la pièce jointe et qui l’a ouverte (l’aperçu n’est pas compté).</span><span class="sxs-lookup"><span data-stu-id="c6c3b-304">**Successful attempts**: The number of users who opened or downloaded and opened the attachment (preview doesn't count).</span></span>

- <span data-ttu-id="c6c3b-305">**Taux de réussite global**: pourcentage calculé en / **nombre total d’utilisateurs ciblés**par des **tentatives réussies**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-305">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>

- <span data-ttu-id="c6c3b-306">**Durée maximale d’ouverture des pièces jointes**: durée de l’ouverture de la pièce jointe par le premier utilisateur après le lancement de la campagne.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-306">**Fastest attachment open time**: How long it took the first user to open the attachment after you launched the campaign.</span></span>

- <span data-ttu-id="c6c3b-307">**Durée moyenne d’ouverture des pièces jointes : durée**totale de l’ouverture de la pièce jointe, divisée par le nombre d’utilisateurs ayant ouvert la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-307">**Average attachment open time**: The sum of how long it took everyone to open the attachment divided by the number of users who opened the attachment.</span></span>

- <span data-ttu-id="c6c3b-308">**Taux de réussite d’ouverture des pièces jointes**: pourcentage calculé par (nombre d’utilisateurs ayant ouvert la pièce jointe)/ **nombre total d’utilisateurs ciblés**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-308">**Attachment open success rate**: A percentage that's calculated by (number of users who opened the attachment) / **Total users targeted**.</span></span>

### <a name="brute-force-password-dictionary-attack-campaign-results"></a><span data-ttu-id="c6c3b-309">Résultats de la campagne de mot de passe en force (attaque de dictionnaire)</span><span class="sxs-lookup"><span data-stu-id="c6c3b-309">Brute Force Password (Dictionary Attack) campaign results</span></span>

<span data-ttu-id="c6c3b-310">Les informations suivantes sont disponibles dans la page Détails de l' **attaque** de chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="c6c3b-310">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="c6c3b-311">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-311">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="c6c3b-312">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="c6c3b-312">**Total users targeted**</span></span>

- <span data-ttu-id="c6c3b-313">**Tentatives réussies**: nombre d’utilisateurs pour lesquels l’un des mots de passe spécifiés a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-313">**Successful attempts**: The number of users who were found to be using one of the specified passwords.</span></span>

- <span data-ttu-id="c6c3b-314">**Taux de réussite global**: pourcentage calculé en / **nombre total d’utilisateurs ciblés**par des **tentatives réussies**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-314">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>

- <span data-ttu-id="c6c3b-315">La section **utilisateurs compromis** répertorie les adresses de messagerie des utilisateurs concernés.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-315">The **Compromised Users** section lists the email addresses of the affected users.</span></span> <span data-ttu-id="c6c3b-316">Vous pouvez cliquer sur **Exporter** pour exporter les résultats dans un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-316">You can click **Export** to export the results to a CSV file.</span></span>

### <a name="password-spray-attack-campaign-results"></a><span data-ttu-id="c6c3b-317">Résultats de la campagne d’attaque par pulvérisation</span><span class="sxs-lookup"><span data-stu-id="c6c3b-317">Password spray attack campaign results</span></span>

<span data-ttu-id="c6c3b-318">Les informations suivantes sont disponibles dans la page Détails de l' **attaque** de chaque campagne :</span><span class="sxs-lookup"><span data-stu-id="c6c3b-318">The following information is available on the **Attack details** page for each campaign:</span></span>

- <span data-ttu-id="c6c3b-319">Durée (date/heure de début et date/heure de fin) de la campagne.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-319">The duration (start date/time and end date/time) of the campaign.</span></span>

- <span data-ttu-id="c6c3b-320">**Nombre total d’utilisateurs ciblés**</span><span class="sxs-lookup"><span data-stu-id="c6c3b-320">**Total users targeted**</span></span>

- <span data-ttu-id="c6c3b-321">**Tentatives réussies**: nombre d’utilisateurs qui ont été identifiés comme utilisant le mot de passe spécifié.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-321">**Successful attempts**: The number of users who were found to be using the specified password.</span></span>

- <span data-ttu-id="c6c3b-322">**Taux de réussite global**: pourcentage calculé en / **nombre total d’utilisateurs ciblés**par des **tentatives réussies**.</span><span class="sxs-lookup"><span data-stu-id="c6c3b-322">**Overall Success Rate**: A percentage that's calculated by **Successful attempts** / **Total users targeted**.</span></span>
