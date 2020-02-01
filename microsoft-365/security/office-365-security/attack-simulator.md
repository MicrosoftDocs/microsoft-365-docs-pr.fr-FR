---
title: Simulateur d’attaques dans Office 365
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
description: En tant qu’administrateur général Office 365, vous pouvez utiliser un simulateur d’attaque pour exécuter des scénarios d’attaque réaliste dans votre organisation. Cela peut vous aider à identifier et à trouver des utilisateurs vulnérables avant qu’une attaque réelle ne touche votre entreprise.
ms.openlocfilehash: 0bdb4a0ffac139f45d842025238d3780f41d594c
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41599821"
---
# <a name="attack-simulator-in-office-365"></a><span data-ttu-id="528e2-104">Simulateur d’attaques dans Office 365</span><span class="sxs-lookup"><span data-stu-id="528e2-104">Attack Simulator in Office 365</span></span>

<span data-ttu-id="528e2-105">**Résumé** Si vous êtes un administrateur général Office 365 ou un administrateur de sécurité et que votre organisation a Office 365 Advanced Threat Protection Plan 2, qui inclut des [fonctionnalités d’enquête et de réponse aux menaces](office-365-ti.md), vous pouvez utiliser un simulateur d’attaque pour exécuter des scénarios d’attaque réaliste dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="528e2-105">**Summary** If you are an Office 365 global administrator or a security administrator and your organization has Office 365 Advanced Threat Protection Plan 2, which includes [Threat Investigation and Response capabilities](office-365-ti.md), you can use Attack Simulator to run realistic attack scenarios in your organization.</span></span> <span data-ttu-id="528e2-106">Cela peut vous aider à identifier les utilisateurs vulnérables avant qu’une véritable attaque n’ait un impact sur votre chiffre d’affaires.</span><span class="sxs-lookup"><span data-stu-id="528e2-106">This can help you identify and find vulnerable users before a real attack impacts your bottom line.</span></span> <span data-ttu-id="528e2-107">Lisez cet article pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="528e2-107">Read this article to learn more.</span></span>

## <a name="the-attacks"></a><span data-ttu-id="528e2-108">Les attaques</span><span class="sxs-lookup"><span data-stu-id="528e2-108">The Attacks</span></span>

<span data-ttu-id="528e2-109">Trois types de simulations d’attaques sont actuellement disponibles :</span><span class="sxs-lookup"><span data-stu-id="528e2-109">Three kinds of attack simulations are currently available:</span></span>

- [<span data-ttu-id="528e2-110">Attaque par harponnage du nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="528e2-110">Display name spear-phishing attack</span></span>](#display-name-spear-phishing-attack)

- [<span data-ttu-id="528e2-111">Attaque par pulvérisation de mot de passe</span><span class="sxs-lookup"><span data-stu-id="528e2-111">Password-spray attack</span></span>](#password-spray-attack)

- [<span data-ttu-id="528e2-112">Attaque de mot de passe par force brute</span><span class="sxs-lookup"><span data-stu-id="528e2-112">Brute-force password attack</span></span>](#brute-force-password-attack)

<span data-ttu-id="528e2-113">Pour qu’une attaque réussisse, assurez-vous que le compte que vous utilisez pour exécuter des attaques simulées utilise l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="528e2-113">For an attack to be successfully launched, make sure that the account you are using to run simulated attacks is using multi-factor authentication.</span></span> <span data-ttu-id="528e2-114">En outre, vous devez être un administrateur général Office 365 ou un administrateur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="528e2-114">In addition, you must be an Office 365 global administrator or a security administrator.</span></span> <span data-ttu-id="528e2-115">(Pour en savoir plus sur les rôles et les autorisations, consultez [la rubrique autorisations dans le centre de conformité des & de sécurité Office 365](permissions-in-the-security-and-compliance-center.md).)</span><span class="sxs-lookup"><span data-stu-id="528e2-115">(To learn more about roles and permissions, see [Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).)</span></span>

<span data-ttu-id="528e2-116">Pour accéder à un simulateur d’attaque &amp; , dans le centre de sécurité conformité, sélectionnez **Threat Management** \> **Attack Simulator**.</span><span class="sxs-lookup"><span data-stu-id="528e2-116">To access Attack Simulator, in the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="528e2-117">Avant de commencer...</span><span class="sxs-lookup"><span data-stu-id="528e2-117">Before you begin...</span></span>

<span data-ttu-id="528e2-118">Assurez-vous que vous et votre organisation remplissez les conditions requises suivantes pour le simulateur d’attaque :</span><span class="sxs-lookup"><span data-stu-id="528e2-118">Make sure that you and your organization meet the following requirements for Attack Simulator:</span></span>

- <span data-ttu-id="528e2-119">Le courrier électronique de votre organisation est hébergé dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="528e2-119">Your organization's email is hosted in Exchange Online.</span></span> <span data-ttu-id="528e2-120">(Le simulateur d’attaque n’est pas disponible pour les serveurs de messagerie locaux.)</span><span class="sxs-lookup"><span data-stu-id="528e2-120">(Attack Simulator is not available for on-premises email servers.)</span></span>

- <span data-ttu-id="528e2-121">Vous êtes un administrateur général Office 365 ou un administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="528e2-121">You are an Office 365 global administrator or security administrator</span></span>

- <span data-ttu-id="528e2-122">L' [authentification multifacteur/l’accès conditionnel](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication) est activé, pour au moins le compte administrateur général Office 365 et les administrateurs de sécurité qui utiliseront un simulateur d’attaque.</span><span class="sxs-lookup"><span data-stu-id="528e2-122">[Multi-factor authentication/Conditional Access](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication) is turned on, for at least the Office 365 global administrator account and security administrators who will be using Attack Simulator.</span></span> <span data-ttu-id="528e2-123">(Idéalement, l’accès à plusieurs facteurs/accès conditionnel est activé pour tous les utilisateurs de votre organisation.)</span><span class="sxs-lookup"><span data-stu-id="528e2-123">(Ideally, multi-factor authentication/conditional access is turned on for all users in your organization.)</span></span>

- <span data-ttu-id="528e2-124">Votre organisation dispose d' [Office 365 Advanced Threat Protection Plan 2](office-365-atp.md), avec un simulateur d’attaque &amp; visible dans le centre de sécurité conformité (allez sur **Threat Management** \> **Attack Simulator**)</span><span class="sxs-lookup"><span data-stu-id="528e2-124">Your organization has [Office 365 Advanced Threat Protection Plan 2](office-365-atp.md), with Attack Simulator visible in the Security &amp; Compliance Center (go to **Threat management** \> **Attack simulator**)</span></span>

    ![Gestion des menaces-simulateur d’attaque](../media/ThreatMgmt-AttackSimulator.png)

## <a name="display-name-spear-phishing-attack"></a><span data-ttu-id="528e2-126">Attaque par harponnage du nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="528e2-126">Display name spear-phishing attack</span></span>

<span data-ttu-id="528e2-127">Le hameçonnage est un terme générique pour une suite d’attaques classées comme une attaque de style d’ingénierie sociale.</span><span class="sxs-lookup"><span data-stu-id="528e2-127">Phishing is a generic term for a broad suite of attacks classed as a social engineering style attack.</span></span> <span data-ttu-id="528e2-128">Cette attaque est axée sur le Spear Phishing, une attaque plus ciblée, dirigée par un groupe spécifique de personnes ou une organisation.</span><span class="sxs-lookup"><span data-stu-id="528e2-128">This attack is focused on spear phishing, a more targeted attack that is aimed at a specific group of individuals or an organization.</span></span> <span data-ttu-id="528e2-129">En règle générale, une attaque personnalisée avec une reconnaissance a été effectuée et utilise un nom complet qui générera une approbation dans le destinataire, comme un message électronique qui semble provenir d’un cadre de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="528e2-129">Typically, a customized attack with some reconnaissance performed and using a display name that will generate trust in the recipient, such as an email message that looks like it came from an executive within your organization.</span></span>

<span data-ttu-id="528e2-130">Cette attaque est axée sur la possibilité de manipuler le nom d’affichage et l’adresse source du message.</span><span class="sxs-lookup"><span data-stu-id="528e2-130">This attack focuses on letting you manipulate who the message appears to have originated from by changing the display name and source address.</span></span> <span data-ttu-id="528e2-131">Lorsque les attaques de Spear Phishing sont réussies, cyberattackers accéder aux informations d’identification des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="528e2-131">When spear-phishing attacks are successful, cyberattackers gain access to users' credentials.</span></span>

### <a name="to-simulate-a-spear-phishing-attack"></a><span data-ttu-id="528e2-132">Pour simuler une attaque par hameçonnage (Spear Phishing)</span><span class="sxs-lookup"><span data-stu-id="528e2-132">To simulate a spear-phishing attack</span></span>

![Composer le corps du message électronique](../media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)

<span data-ttu-id="528e2-134">Vous pouvez concevoir l’éditeur HTML enrichi directement dans le champ de **corps du message** lui-même ou utiliser la source HTML.</span><span class="sxs-lookup"><span data-stu-id="528e2-134">You can craft the rich HTML editor directly in the **Email body** field itself or work with HTML source.</span></span>

1. <span data-ttu-id="528e2-135">Dans le [Centre &amp; de sécurité conformité](https://protection.office.com), sélectionnez **Threat Management** \> **Attack Simulator**.</span><span class="sxs-lookup"><span data-stu-id="528e2-135">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>

2. <span data-ttu-id="528e2-136">Spécifiez un nom de campagne significatif pour l’attaque ou sélectionnez un modèle.</span><span class="sxs-lookup"><span data-stu-id="528e2-136">Specify a meaningful campaign name for the attack or select a template.</span></span>

   ![Page de démarrage du hameçonnage](../media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)

3. <span data-ttu-id="528e2-138">Spécifiez les destinataires cibles.</span><span class="sxs-lookup"><span data-stu-id="528e2-138">Specify the target recipients.</span></span> <span data-ttu-id="528e2-139">Il peut s’agir d’individus ou de groupes au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="528e2-139">This can be individuals or groups in your organization.</span></span> <span data-ttu-id="528e2-140">Chaque destinataire ciblé doit disposer d’une boîte aux lettres Exchange Online pour que l’attaque aboutisse.</span><span class="sxs-lookup"><span data-stu-id="528e2-140">Each targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>

   ![Sélection de destinataires](../media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)

4. <span data-ttu-id="528e2-142">Configurez les détails du courrier électronique de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="528e2-142">Configure the Phishing email details.</span></span>

   ![Configurer les détails du courrier électronique](../media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)

   <span data-ttu-id="528e2-144">La mise en forme HTML peut être aussi complexe ou basique que les besoins de votre campagne.</span><span class="sxs-lookup"><span data-stu-id="528e2-144">The HTML formatting can be as complex or basic as your campaign needs.</span></span> <span data-ttu-id="528e2-145">Comme le format du message est HTML, vous pouvez insérer des images et du texte pour améliorer la convivialité.</span><span class="sxs-lookup"><span data-stu-id="528e2-145">As the email format is HTML, you can insert images and text to enhance believability.</span></span> <span data-ttu-id="528e2-146">Vous avez le contrôle sur ce à quoi ressemblera le message reçu dans le client de messagerie de réception.</span><span class="sxs-lookup"><span data-stu-id="528e2-146">You have control on what the received message will look like in the receiving email client.</span></span>

5. <span data-ttu-id="528e2-147">Spécifiez le texte du champ **de (nom)** .</span><span class="sxs-lookup"><span data-stu-id="528e2-147">Specify text for the **From (Name)** field.</span></span> <span data-ttu-id="528e2-148">Il s’agit du champ qui indique le **nom d’affichage** dans le client de messagerie de réception.</span><span class="sxs-lookup"><span data-stu-id="528e2-148">This is the field that shows in the **Display Name** in the receiving email client.</span></span>

6. <span data-ttu-id="528e2-149">Spécifiez le texte ou le champ **de** .</span><span class="sxs-lookup"><span data-stu-id="528e2-149">Specify text or the **From** field.</span></span> <span data-ttu-id="528e2-150">Il s’agit du champ qui indique comme adresse de messagerie de l’expéditeur dans le client de messagerie de réception.</span><span class="sxs-lookup"><span data-stu-id="528e2-150">This is the field that shows as the email address of the sender in the receiving email client.</span></span>

   <span data-ttu-id="528e2-151">Vous pouvez entrer un espace de noms de messagerie existant dans votre organisation (en procédant ainsi à la résolution de l’adresse de messagerie dans le client de réception, ce qui facilite un modèle d’approbation très élevée) ou vous pouvez entrer une adresse de messagerie externe.</span><span class="sxs-lookup"><span data-stu-id="528e2-151">You can enter an existing email namespace within your organization (doing this will make the email address actually resolve in the receiving client, facilitating a very high trust model), or you can enter an external email address.</span></span> <span data-ttu-id="528e2-152">L’adresse de messagerie que vous spécifiez n’a pas besoin d’exister réellement, mais elle doit suivre le format d’une adresse SMTP valide, telle `user@domainname.extension`que.</span><span class="sxs-lookup"><span data-stu-id="528e2-152">The email address that you specify does not have to actually exist, but it does need to follow the format of a valid SMTP address, such as `user@domainname.extension`.</span></span>

7. <span data-ttu-id="528e2-153">À l’aide du sélecteur de liste déroulante, sélectionnez une URL de serveur de connexion d’hameçonnage reflétant le type de contenu que vous aurez au sein de votre attaque.</span><span class="sxs-lookup"><span data-stu-id="528e2-153">Using the drop-down selector, select a Phishing Login server URL that reflects the type of content you will have within your attack.</span></span> <span data-ttu-id="528e2-154">Plusieurs URL à thèmes vous sont proposées, telles que livraison de documents, technique, paie, etc. Il s’agit en fait de l’URL sur laquelle les utilisateurs ciblés sont invités à cliquer.</span><span class="sxs-lookup"><span data-stu-id="528e2-154">Several themed URLs are provided for you to choose from, such as document delivery, technical, payroll etc. This is effectively the URL that targeted users are asked to click.</span></span>

8. <span data-ttu-id="528e2-155">Spécifiez une URL de page d’accueil personnalisée.</span><span class="sxs-lookup"><span data-stu-id="528e2-155">Specify a custom landing page URL.</span></span> <span data-ttu-id="528e2-156">Cette opération permet de rediriger les utilisateurs vers une URL que vous spécifiez à la fin d’une attaque réussie.</span><span class="sxs-lookup"><span data-stu-id="528e2-156">Using this will redirect users to a URL you specify at the end of a successful attack.</span></span> <span data-ttu-id="528e2-157">Si vous avez une formation interne à la sensibilisation, par exemple, vous pouvez spécifier cela ici.</span><span class="sxs-lookup"><span data-stu-id="528e2-157">If you have internal awareness training, for example, you can specify that here.</span></span>

9. <span data-ttu-id="528e2-158">Spécifiez le texte du champ **Subject** .</span><span class="sxs-lookup"><span data-stu-id="528e2-158">Specify text for the **Subject** field.</span></span> <span data-ttu-id="528e2-159">Il s’agit du champ qui indique le **nom** de l’objet dans le client de messagerie de réception.</span><span class="sxs-lookup"><span data-stu-id="528e2-159">This is the field that shows as the **Subject Name** in the receiving email client.</span></span>

10. <span data-ttu-id="528e2-160">Composez le **corps du message électronique** que la cible recevra.</span><span class="sxs-lookup"><span data-stu-id="528e2-160">Compose the **Email body** that the target will receive.</span></span>

    <span data-ttu-id="528e2-161">`${username}`insère le nom des cibles dans le corps du message électronique.</span><span class="sxs-lookup"><span data-stu-id="528e2-161">`${username}` inserts the targets name into the Email body.</span></span>

    <span data-ttu-id="528e2-162">`${loginserverurl}`insère l’URL sur laquelle les utilisateurs cibles doivent cliquer</span><span class="sxs-lookup"><span data-stu-id="528e2-162">`${loginserverurl}` inserts the URL we want target users to click</span></span>

11. <span data-ttu-id="528e2-163">Choisissez **suivant,** puis **Terminer** pour lancer l’attaque.</span><span class="sxs-lookup"><span data-stu-id="528e2-163">Choose **Next,** then **Finish** to launch the attack.</span></span> <span data-ttu-id="528e2-164">Le message électronique de Spear Phishing est remis aux boîtes aux lettres de vos destinataires cibles.</span><span class="sxs-lookup"><span data-stu-id="528e2-164">The spear phishing email message is delivered to your target recipients' mailboxes.</span></span>

## <a name="password-spray-attack"></a><span data-ttu-id="528e2-165">Attaque par pulvérisation de mot de passe</span><span class="sxs-lookup"><span data-stu-id="528e2-165">Password-spray attack</span></span>

<span data-ttu-id="528e2-166">Une attaque par pulvérisation de mot de passe contre une organisation est généralement utilisée après qu’un acteur incorrect a réussi à acquérir une liste d’utilisateurs valides du client.</span><span class="sxs-lookup"><span data-stu-id="528e2-166">A password spray attack against an organization is typically used after a bad actor has successfully acquired a list of valid users from the tenant.</span></span> <span data-ttu-id="528e2-167">L’acteur incorrect connaît les mots de passe courants que les personnes utilisent.</span><span class="sxs-lookup"><span data-stu-id="528e2-167">The bad actor knows about common passwords that people use.</span></span> <span data-ttu-id="528e2-168">Il s’agit d’une attaque très utilisée, car il s’agit d’une attaque bon marché à exécuter et plus difficile à détecter que les approches en force.</span><span class="sxs-lookup"><span data-stu-id="528e2-168">This is a widely used attack, as it is a cheap attack to run, and harder to detect than brute force approaches.</span></span>

<span data-ttu-id="528e2-169">Cette attaque est axée sur la possibilité de spécifier un mot de passe commun pour un grand nombre d’utilisateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="528e2-169">This attack focuses on letting you specify a common password against a large target base of users.</span></span>

### <a name="to-simulate-a-password-spray-attack"></a><span data-ttu-id="528e2-170">Pour simuler une attaque par pulvérisation de mot de passe</span><span class="sxs-lookup"><span data-stu-id="528e2-170">To simulate a password-spray attack</span></span>

1. <span data-ttu-id="528e2-171">Dans le [Centre &amp; de sécurité conformité](https://protection.office.com), sélectionnez **Threat Management** \> **Attack Simulator**.</span><span class="sxs-lookup"><span data-stu-id="528e2-171">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>

2. <span data-ttu-id="528e2-172">Spécifiez un nom de campagne significatif pour l’attaque.</span><span class="sxs-lookup"><span data-stu-id="528e2-172">Specify a meaningful campaign name for the attack.</span></span>

3. <span data-ttu-id="528e2-173">Spécifiez les destinataires cibles.</span><span class="sxs-lookup"><span data-stu-id="528e2-173">Specify the target recipients.</span></span> <span data-ttu-id="528e2-174">Il peut s’agir d’individus ou de groupes au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="528e2-174">This can be individuals or groups in your organization.</span></span> <span data-ttu-id="528e2-175">Un destinataire ciblé doit disposer d’une boîte aux lettres Exchange Online pour que l’attaque réussisse.</span><span class="sxs-lookup"><span data-stu-id="528e2-175">A targeted recipient must have an Exchange Online mailbox in order for the attack to be successful.</span></span>

4. <span data-ttu-id="528e2-176">Spécifiez un mot de passe à utiliser pour l’attaque.</span><span class="sxs-lookup"><span data-stu-id="528e2-176">Specify a password to use for the attack.</span></span> <span data-ttu-id="528e2-177">Par exemple, vous pouvez essayer un mot de passe courant et `Summer2019`pertinent.</span><span class="sxs-lookup"><span data-stu-id="528e2-177">For example, one common, relevant password you could try is `Summer2019`.</span></span> <span data-ttu-id="528e2-178">Un autre peut `Fall2019`être ou `Password1`.</span><span class="sxs-lookup"><span data-stu-id="528e2-178">Another might be `Fall2019`, or `Password1`.</span></span>

5. <span data-ttu-id="528e2-179">Cliquez sur **Terminer** pour lancer l’attaque.</span><span class="sxs-lookup"><span data-stu-id="528e2-179">Choose **Finish** to launch the attack.</span></span>

## <a name="brute-force-password-attack"></a><span data-ttu-id="528e2-180">Attaque de mot de passe par force brute</span><span class="sxs-lookup"><span data-stu-id="528e2-180">Brute-force password attack</span></span>

<span data-ttu-id="528e2-181">Une attaque de mot de passe en force contre une organisation est généralement utilisée après qu’un acteur incorrect a réussi à acquérir une liste d’utilisateurs clés auprès du client.</span><span class="sxs-lookup"><span data-stu-id="528e2-181">A brute-force password attack against an organization is typically used after a bad actor has successfully acquired a list of key users from the tenant.</span></span> <span data-ttu-id="528e2-182">Cette attaque consiste à essayer un ensemble de mots de passe sur le compte d’un seul utilisateur.</span><span class="sxs-lookup"><span data-stu-id="528e2-182">This attack focuses on trying a set of passwords on a single user's account.</span></span>

### <a name="to-simulate-a-brute-force-password-attack"></a><span data-ttu-id="528e2-183">Pour simuler une attaque de mot de passe en force brute</span><span class="sxs-lookup"><span data-stu-id="528e2-183">To simulate a brute-force password attack</span></span>

1. <span data-ttu-id="528e2-184">Dans le [Centre &amp; de sécurité conformité](https://protection.office.com), sélectionnez **Threat Management** \> **Attack Simulator**.</span><span class="sxs-lookup"><span data-stu-id="528e2-184">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>

2. <span data-ttu-id="528e2-185">Spécifiez un nom de campagne significatif pour l’attaque.</span><span class="sxs-lookup"><span data-stu-id="528e2-185">Specify a meaningful campaign name for the attack.</span></span>

3. <span data-ttu-id="528e2-186">Spécifiez le destinataire cible.</span><span class="sxs-lookup"><span data-stu-id="528e2-186">Specify the target recipient.</span></span> <span data-ttu-id="528e2-187">Un destinataire ciblé doit disposer d’une boîte aux lettres Exchange Online pour que l’attaque réussisse.</span><span class="sxs-lookup"><span data-stu-id="528e2-187">A targeted recipient must have an Exchange Online mailbox in order for the attack to be successful.</span></span>

4. <span data-ttu-id="528e2-188">Spécifiez un ensemble de mots de passe à utiliser pour l’attaque.</span><span class="sxs-lookup"><span data-stu-id="528e2-188">Specify a set of passwords to use for the attack.</span></span> <span data-ttu-id="528e2-189">Pour ce faire, vous pouvez utiliser un fichier texte (. txt) pour votre liste de mots de passe.</span><span class="sxs-lookup"><span data-stu-id="528e2-189">To do this, you can use a text (.txt) file for your list of passwords.</span></span> <span data-ttu-id="528e2-190">Le fichier texte ne peut pas dépasser 10 Mo dans la taille du fichier.</span><span class="sxs-lookup"><span data-stu-id="528e2-190">The text file cannot exceed 10 MB in file size.</span></span> <span data-ttu-id="528e2-191">Utilisez un mot de passe par ligne et assurez-vous d’inclure un retour à la ligne après le dernier mot de passe de votre liste.</span><span class="sxs-lookup"><span data-stu-id="528e2-191">Use one password per line, and make sure to include a hard return after the last password in your list.</span></span>

5. <span data-ttu-id="528e2-192">Cliquez sur **Terminer** pour lancer l’attaque.</span><span class="sxs-lookup"><span data-stu-id="528e2-192">Choose **Finish** to launch the attack.</span></span>

## <a name="new-features-in-attack-simulator"></a><span data-ttu-id="528e2-193">Nouvelles fonctionnalités dans un simulateur d’attaque</span><span class="sxs-lookup"><span data-stu-id="528e2-193">New features in Attack Simulator</span></span>

<span data-ttu-id="528e2-194">De nouvelles fonctionnalités ont récemment été ajoutées au simulateur d’attaques.</span><span class="sxs-lookup"><span data-stu-id="528e2-194">New features have recently been added to Attack Simulator.</span></span> <span data-ttu-id="528e2-195">Cela inclut ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="528e2-195">These include:</span></span>

- <span data-ttu-id="528e2-196">Fonctionnalités de création de rapports avancées.</span><span class="sxs-lookup"><span data-stu-id="528e2-196">Advanced reporting capabilities.</span></span> <span data-ttu-id="528e2-197">La possibilité d’afficher des données telles que le temps le plus rapide (ou le plus lent) pour ouvrir un message électronique de simulation d’attaque, le temps le plus rapide (ou le plus lent) de cliquer sur un lien dans le message, ainsi que davantage de visualisations.</span><span class="sxs-lookup"><span data-stu-id="528e2-197">The ability to see data such as the fastest (or slowest) time to open an attack simulation email message, the fastest (or slowest) time to click a link in the message, and more visualizations.</span></span>

- <span data-ttu-id="528e2-198">Éditeur de modèles de courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="528e2-198">Email template editor.</span></span> <span data-ttu-id="528e2-199">La possibilité de créer un modèle de courrier électronique personnalisé réutilisable que vous pouvez utiliser pour les simulations d’attaque ultérieures.</span><span class="sxs-lookup"><span data-stu-id="528e2-199">The ability to create a custom, reusable email template's that you can use for future attack simulations.</span></span>

- <span data-ttu-id="528e2-200">Importation de destinataires CSV.</span><span class="sxs-lookup"><span data-stu-id="528e2-200">CSV Recipient Import.</span></span> <span data-ttu-id="528e2-201">La possibilité d’utiliser un fichier. csv pour importer votre liste de destinataires cible au lieu d’utiliser le sélecteur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="528e2-201">The ability to use a .csv file to import your target recipient list instead of using the address book picker.</span></span>

<span data-ttu-id="528e2-202">De nouvelles fonctionnalités sont bientôt disponibles pour les simulateurs d’attaques.</span><span class="sxs-lookup"><span data-stu-id="528e2-202">More new features are coming soon to Attack Simulator.</span></span> <span data-ttu-id="528e2-203">Cela inclut ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="528e2-203">These include:</span></span>

- <span data-ttu-id="528e2-204">Simulation d’hameçonnage de la charge utile des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="528e2-204">Attachment payload phishing simulation.</span></span> <span data-ttu-id="528e2-205">Possibilité d’utiliser une pièce jointe comme charge utile pour la simulation de hameçonnage à la place d’une URL.</span><span class="sxs-lookup"><span data-stu-id="528e2-205">The ability to use an attachment as the payload for phishing simulation in place of a URL.</span></span>

<span data-ttu-id="528e2-206">Consultez la feuille de [route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap) pour découvrir les éléments en cours de développement, le déploiement et les fonctionnalités déjà lancées.</span><span class="sxs-lookup"><span data-stu-id="528e2-206">Visit the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap) to see what's in development, what's rolling out, and what's already launched.</span></span>

## <a name="see-also"></a><span data-ttu-id="528e2-207">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="528e2-207">See also</span></span>

[<span data-ttu-id="528e2-208">Description du service Office 365 - Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="528e2-208">Office 365 Advanced Threat Protection Service Description</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)

[<span data-ttu-id="528e2-209">Protection avancée contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="528e2-209">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
