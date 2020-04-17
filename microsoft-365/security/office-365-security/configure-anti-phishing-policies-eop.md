---
title: Configurer la stratégie anti-hameçonnage par défaut dans EOP
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: article
ms.date: ''
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à modifier les paramètres de détection d’usurpation d’identité disponibles dans la stratégie anti-hameçonnage par défaut dans les organisations Office 365 avec des boîtes aux lettres Exchange Online.
ms.openlocfilehash: 1a8527a55796910e79fbf70b824de828ca48591b
ms.sourcegitcommit: db8702cf578b02c6fd6a2670c177b456efae4748
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2020
ms.locfileid: "43537532"
---
# <a name="configure-the-default-anti-phishing-policy-in-eop"></a><span data-ttu-id="cd978-103">Configurer la stratégie anti-hameçonnage par défaut dans EOP</span><span class="sxs-lookup"><span data-stu-id="cd978-103">Configure the default anti-phishing policy in EOP</span></span>

<span data-ttu-id="cd978-104">Les organisations Office 365 avec des boîtes aux lettres Exchange Online et les organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online ont une stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="cd978-104">Office 365 organizations with Exchange Online mailboxes and standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes have a default anti-phishing policy.</span></span> <span data-ttu-id="cd978-105">Cette stratégie contient un nombre limité de fonctionnalités d’usurpation d’identité qui sont activées par défaut.</span><span class="sxs-lookup"><span data-stu-id="cd978-105">This policy contains a limited number of anti-spoofing features that are enabled by default.</span></span> <span data-ttu-id="cd978-106">Pour plus d’informations, reportez-vous à la rubrique [usurpation des paramètres dans les stratégies anti-hameçonnage](set-up-anti-phishing-policies.md#spoof-settings).</span><span class="sxs-lookup"><span data-stu-id="cd978-106">For more information, see [Spoof settings in anti-phishing policies](set-up-anti-phishing-policies.md#spoof-settings).</span></span>

<span data-ttu-id="cd978-107">Les organisations Office 365 avec des boîtes aux lettres Exchange Online peuvent modifier la stratégie anti-hameçonnage par défaut dans le centre de sécurité & de sécurité Office 365 ou dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cd978-107">Office 365 organizations with Exchange Online mailboxes can modify the default anti-phishing policy in the Office 365 Security & Compliance Center or in Exchange Online PowerShell.</span></span> <span data-ttu-id="cd978-108">Les organisations EOP autonomes sans boîte aux lettres Exchange Online ne peuvent pas modifier leur stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="cd978-108">Standalone EOP organizations without Exchange Online mailboxes can't modify their default anti-phishing policy.</span></span>

<span data-ttu-id="cd978-109">Pour plus d’informations sur la création et la modification des stratégies anti-hameçonnage plus avancées disponibles dans Office 365 Advanced Threat Protection, consultez la rubrique [configure ATP anti-phishing Policies in office 365](configure-atp-anti-phishing-policies.md).</span><span class="sxs-lookup"><span data-stu-id="cd978-109">For information about creating and modifying the more advanced ATP anti-phishing policies that are available in Office 365 Advanced Threat Protection, see [Configure ATP anti-phishing policies in Office 365](configure-atp-anti-phishing-policies.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="cd978-110">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="cd978-110">What do you need to know before you begin?</span></span>

- <span data-ttu-id="cd978-111">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="cd978-111">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="cd978-112">Pour accéder directement à la page **anti-hameçonnage** , utilisez <https://protection.office.com/antiphishing>.</span><span class="sxs-lookup"><span data-stu-id="cd978-112">To go directly to the **Anti-phishing** page, use <https://protection.office.com/antiphishing>.</span></span>

- <span data-ttu-id="cd978-113">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="cd978-113">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="cd978-114">Des autorisations doivent vous être attribuées avant de pouvoir exécuter ces procédures.</span><span class="sxs-lookup"><span data-stu-id="cd978-114">You need to be assigned permissions before you can perform these procedures.</span></span> <span data-ttu-id="cd978-115">Pour ajouter, modifier et supprimer des stratégies de détection d’hameçonnage, vous devez être membre des groupes de rôles de gestion de l' **organisation** ou d' **administrateur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="cd978-115">To add, modify, and delete anti-phishing policies, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span> <span data-ttu-id="cd978-116">Pour un accès en lecture seule aux stratégies de détection d’hameçonnage, vous devez être membre du groupe de rôles **lecteur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="cd978-116">For read-only access to anti-phishing policies, you need to be a member of the **Security Reader** role group.</span></span> <span data-ttu-id="cd978-117">Pour plus d’informations sur les groupes de rôles dans le Centre de sécurité et conformité, voir [Autorisations dans le Centre de sécurité et conformité Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="cd978-117">For more information about role groups in the Security & Compliance Center, see [Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="cd978-118">Pour connaître les paramètres recommandés pour la stratégie anti-hameçonnage par défaut, consultez les paramètres de la [stratégie anti-hameçonnage par défaut EOP](recommended-settings-for-eop-and-office365-atp.md#eop-default-anti-phishing-policy-settings).</span><span class="sxs-lookup"><span data-stu-id="cd978-118">For our recommended settings for the default anti-phishing policy, see [EOP default anti-phishing policy settings](recommended-settings-for-eop-and-office365-atp.md#eop-default-anti-phishing-policy-settings).</span></span>

- <span data-ttu-id="cd978-119">Autorisez jusqu’à 30 minutes pour l’application de la stratégie mise à jour.</span><span class="sxs-lookup"><span data-stu-id="cd978-119">Allow up to 30 minutes for the updated policy to be applied.</span></span>

- <span data-ttu-id="cd978-120">Pour plus d’informations sur l’endroit où les stratégies de détection d’hameçonnage sont appliquées dans le pipeline de filtrage, consultez la rubrique [Order and Precedence of Mail Protection in Office 365](how-policies-and-protections-are-combined.md).</span><span class="sxs-lookup"><span data-stu-id="cd978-120">For information about where anti-phishing policies are applied in the filtering pipeline, see [Order and precedence of email protection in Office 365](how-policies-and-protections-are-combined.md).</span></span>

### <a name="use-the-security--compliance-center-to-modify-the-default-anti-phishing-policy"></a><span data-ttu-id="cd978-121">Utiliser le centre de sécurité & conformité pour modifier la stratégie anti-hameçonnage par défaut</span><span class="sxs-lookup"><span data-stu-id="cd978-121">Use the Security & Compliance Center to modify the default anti-phishing policy</span></span>

<span data-ttu-id="cd978-122">La stratégie anti-hameçonnage par défaut est nommée Office antiphishing par défaut et n’apparaît pas dans la liste des stratégies.</span><span class="sxs-lookup"><span data-stu-id="cd978-122">The default anti-phishing policy is named Office365 AntiPhish Default, and it doesn't appear in the list of policies.</span></span> <span data-ttu-id="cd978-123">Pour modifier la stratégie anti-hameçonnage par défaut, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="cd978-123">To modify the default anti-phishing policy, do the following steps:</span></span>

1. <span data-ttu-id="cd978-124">Dans le centre de sécurité & conformité, accédez à **protection anti-hameçonnage**de la **stratégie** \> de **gestion** \> des menaces.</span><span class="sxs-lookup"><span data-stu-id="cd978-124">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-phishing**.</span></span>

2. <span data-ttu-id="cd978-125">Sur la page **anti-hameçonnage** , cliquez sur **stratégie par défaut**.</span><span class="sxs-lookup"><span data-stu-id="cd978-125">On the **Anti-phishing** page, click **Default policy**.</span></span>

3. <span data-ttu-id="cd978-126">La page **modifier votre stratégie d’anti-hameçonnage Office 365 par défaut** apparaît.</span><span class="sxs-lookup"><span data-stu-id="cd978-126">The **Edit your policy Office365 AntiPhish Default** page appears.</span></span> <span data-ttu-id="cd978-127">Dans la section **usurpation** , cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="cd978-127">In the **Spoof** section, click **Edit**.</span></span>

   <span data-ttu-id="cd978-128">Notez que ces paramètres sont identiques aux paramètres d’usurpation d’identité disponibles dans les stratégies anti-hameçonnage ATP.</span><span class="sxs-lookup"><span data-stu-id="cd978-128">Note that these settings are identical to the spoof settings that are available in ATP anti-phishing policies.</span></span>

   - <span data-ttu-id="cd978-129">**Usurpation des paramètres de filtrage**: la valeur par défaut est **activée**, et nous vous recommandons de la laisser activée.</span><span class="sxs-lookup"><span data-stu-id="cd978-129">**Spoofing filter settings**: The default value is **On**, and we recommend that you leave it on.</span></span> <span data-ttu-id="cd978-130">Pour le désactiver, faites glisser le bouton de bascule sur **désactivé**.</span><span class="sxs-lookup"><span data-stu-id="cd978-130">To turn it off, slide the toggle to **Off**.</span></span> <span data-ttu-id="cd978-131">Pour plus d’informations, consultez la rubrique [configure usurpation Intelligence in Office 365](learn-about-spoof-intelligence.md).</span><span class="sxs-lookup"><span data-stu-id="cd978-131">For more information, see [Configure spoof intelligence in Office 365](learn-about-spoof-intelligence.md).</span></span>

     > [!NOTE]
     > <span data-ttu-id="cd978-132">Vous n’avez pas besoin de désactiver la protection contre l’usurpation d’identité si votre enregistrement MX ne pointe pas vers Office 365 ; vous activez le filtrage amélioré pour les connecteurs à la place.</span><span class="sxs-lookup"><span data-stu-id="cd978-132">You don't need to disable anti-spoofing protection if your MX record doesn't point to Office 365; you enable Enhanced Filtering for Connectors instead.</span></span> <span data-ttu-id="cd978-133">Pour obtenir des instructions, voir [Enhanced Filtering for Connectors in Exchange Online](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors).</span><span class="sxs-lookup"><span data-stu-id="cd978-133">For instructions, see [Enhanced Filtering for Connectors in Exchange Online](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors).</span></span>

   - <span data-ttu-id="cd978-134">**Activer la fonctionnalité d’expéditeur non authentifié**: ajoute un point d’interrogation à la photo de l’expéditeur si le message ne parvient pas à vérifier l’authentification de messagerie.</span><span class="sxs-lookup"><span data-stu-id="cd978-134">**Enable Unauthenticated Sender feature**: Adds a question mark to the sender's photo if the message fails email authentication checks.</span></span> <span data-ttu-id="cd978-135">Pour plus d’informations, reportez-vous à la rubrique [usurpation des paramètres dans les stratégies anti-hameçonnage](set-up-anti-phishing-policies.md#spoof-settings).</span><span class="sxs-lookup"><span data-stu-id="cd978-135">For more information, see [Spoof settings in anti-phishing policies](set-up-anti-phishing-policies.md#spoof-settings).</span></span> <span data-ttu-id="cd978-136">La valeur par défaut est **Activée**.</span><span class="sxs-lookup"><span data-stu-id="cd978-136">The default value is **On**.</span></span> <span data-ttu-id="cd978-137">Pour le désactiver, faites glisser le bouton de bascule sur **désactivé**.</span><span class="sxs-lookup"><span data-stu-id="cd978-137">To turn it off, slide the toggle to **Off**.</span></span>

   - <span data-ttu-id="cd978-138">**Actions**: spécifiez l’action à effectuer sur les messages qui échouent à l’aide d’usurpation d’identité :</span><span class="sxs-lookup"><span data-stu-id="cd978-138">**Actions**: Specify the action to take on messages that fail spoof intelligence:</span></span>

     <span data-ttu-id="cd978-139">**Si un message électronique est envoyé par un utilisateur qui n’est pas autorisé à usurper votre domaine**:</span><span class="sxs-lookup"><span data-stu-id="cd978-139">**If email is sent by someone who's not allowed to spoof your domain**:</span></span>

     - <span data-ttu-id="cd978-140">**Déplacer le message vers les dossiers de courrier indésirable des destinataires** (il s’agit de la valeur par défaut.)</span><span class="sxs-lookup"><span data-stu-id="cd978-140">**Move message to the recipients' Junk Email folders** (This is the default value.)</span></span>
     - <span data-ttu-id="cd978-141">**Mettre en quarantaine le message**</span><span class="sxs-lookup"><span data-stu-id="cd978-141">**Quarantine the message**</span></span>

   - <span data-ttu-id="cd978-142">**Vérifiez vos paramètres**: au lieu de cliquer sur chaque étape individuelle, les paramètres sont affichés dans un résumé.</span><span class="sxs-lookup"><span data-stu-id="cd978-142">**Review your settings**: Instead of clicking on each individual step, the settings are displayed in a summary.</span></span>

     - <span data-ttu-id="cd978-143">Vous pouvez cliquer sur **modifier** dans chaque section pour revenir à la page appropriée.</span><span class="sxs-lookup"><span data-stu-id="cd978-143">You can click **Edit** in each section to jump back to the relevant page.</span></span>
     - <span data-ttu-id="cd978-144">Vous pouvez activer ou **Désactiver** les paramètres suivants **directement sur cette** page :</span><span class="sxs-lookup"><span data-stu-id="cd978-144">You can toggle the following settings **On** or **Off** directly on this page:</span></span>

       - <span data-ttu-id="cd978-145">**Activer la protection contre l’usurpation d’identité**</span><span class="sxs-lookup"><span data-stu-id="cd978-145">**Enable antispoofing protection**</span></span>
       - <span data-ttu-id="cd978-146">**Activer la fonctionnalité d’expéditeur non authentifié**</span><span class="sxs-lookup"><span data-stu-id="cd978-146">**Enable Unauthenticated Sender feature**</span></span>

   <span data-ttu-id="cd978-147">Lorsque vous avez terminé, cliquez sur **Enregistrer** sur une page.</span><span class="sxs-lookup"><span data-stu-id="cd978-147">When you're finished, click **Save** on any page.</span></span>

4. <span data-ttu-id="cd978-148">Sur la page **modifier votre stratégie par défaut pour les antiphishing Office 365** , vérifiez vos paramètres, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="cd978-148">Back on the **Edit your policy Office365 AntiPhish Default** page, review your settings and then click **Close**.</span></span>

## <a name="use-the-security--compliance-center-to-view-the-default-anti-phishing-policy"></a><span data-ttu-id="cd978-149">Utiliser le centre de sécurité & conformité pour afficher la stratégie anti-hameçonnage par défaut</span><span class="sxs-lookup"><span data-stu-id="cd978-149">Use the Security & Compliance Center to view the default anti-phishing policy</span></span>

1. <span data-ttu-id="cd978-150">Dans le centre de sécurité & conformité, puis accédez à **Policy** \> **protection contre les** **menaces** \> pour le hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="cd978-150">In the Security & Compliance Center, and go to **Threat management** \> **Policy** \> **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="cd978-151">Cliquez sur **stratégie par défaut** pour afficher la stratégie anti-hameçonnage par défaut.</span><span class="sxs-lookup"><span data-stu-id="cd978-151">Click **Default policy** to view the default anti-phishing policy.</span></span>

## <a name="use-exchange-online-powershell-to-configure-the-default-anti-phishing-policy"></a><span data-ttu-id="cd978-152">Utiliser Exchange Online PowerShell pour configurer la stratégie anti-hameçonnage par défaut</span><span class="sxs-lookup"><span data-stu-id="cd978-152">Use Exchange Online PowerShell to configure the default anti-phishing policy</span></span>

### <a name="use-powershell-to-view-the-default-anti-phish-policy"></a><span data-ttu-id="cd978-153">Utiliser PowerShell pour afficher la stratégie anti-hameçonnage par défaut</span><span class="sxs-lookup"><span data-stu-id="cd978-153">Use PowerShell to view the default anti-phish policy</span></span>

<span data-ttu-id="cd978-154">Pour afficher la stratégie anti-hameçonnage par défaut, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="cd978-154">To view the default anti-phish policy, run the following command:</span></span>

```PowerShell
Get-AntiPhishPolicy -Identity "Office365 AntiPhish Default"
```

<span data-ttu-id="cd978-155">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-antiphishpolicy permet](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Get-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="cd978-155">For detailed syntax and parameter information, see [Get-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Get-AntiPhishPolicy).</span></span>

### <a name="use-powershell-to-modify-the-default-anti-phish-policy"></a><span data-ttu-id="cd978-156">Utiliser PowerShell pour modifier la stratégie anti-hameçonnage par défaut</span><span class="sxs-lookup"><span data-stu-id="cd978-156">Use PowerShell to modify the default anti-phish policy</span></span>

<span data-ttu-id="cd978-157">Pour modifier la stratégie anti-hameçonnage par défaut, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="cd978-157">To modify the default anti-phish policy, use the following syntax:</span></span>

```powershell
Set-AntiPhishPolicy -Identity "Office365 AntiPhish Default" [-AuthenticationFailAction <MoveToJmf | Quarantine>] [-EnableAntispoofEnforcement <$true | $false>] [-EnableUnauthenticatedSender <$true | $false>]
```

<span data-ttu-id="cd978-158">Cet exemple modifie l’action pour les messages usurpés dont l’authentification échoue lors de la mise en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="cd978-158">This example changes the action for spoofed messages that fail authentication checks to quarantine.</span></span>

```powershell
Set-AntiPhishPolicy -Identity "Office365 AntiPhish Default" -AuthenticationFailAction Quarantine
```

<span data-ttu-id="cd978-159">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-antiphishpolicy permet](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Set-AntiPhishPolicy).</span><span class="sxs-lookup"><span data-stu-id="cd978-159">For detailed syntax and parameter information, see [Set-AntiPhishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Set-AntiPhishPolicy).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="cd978-160">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="cd978-160">How do you know these procedures worked?</span></span>

<span data-ttu-id="cd978-161">Pour vérifier que vous avez bien configuré la stratégie anti-hameçonnage par défaut, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="cd978-161">To verify that you've successfully configured the default anti-phishing policy, do any of the following steps:</span></span>

- <span data-ttu-id="cd978-162">Dans le centre de sécurité & conformité, accédez à **stratégie** \> de **gestion** \> **des menaces-hameçonnage** \> , cliquez sur **stratégie par défaut** et affichez les détails dans le menu volant.</span><span class="sxs-lookup"><span data-stu-id="cd978-162">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Anti-phishing** \> click **Default policy** and view the details in the flyout.</span></span>

- <span data-ttu-id="cd978-163">Dans Exchange Online PowerShell, exécutez la commande suivante et vérifiez les paramètres :</span><span class="sxs-lookup"><span data-stu-id="cd978-163">In Exchange Online PowerShell, run the following command and verify the settings:</span></span>

  ```PowerShell
  Get-AntiPhishPolicy -Identity "Office365 AntiPhish Default"
  ```
