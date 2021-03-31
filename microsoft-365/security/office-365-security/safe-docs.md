---
title: Documents sécurisés dans Microsoft Defender pour Office 365
ms.author: chrisda
author: chrisda
manager: dansimp
ms.reviewer: kshi
ms.date: ''
audience: ITPro
ms.topic: how-to
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ''
ms.collection:
- M365-security-compliance
description: Découvrez la sécurité des documents sécurisés dans Microsoft 365 E5 ou Microsoft 365 E5 Security.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 78ae99158e30046923d24897e7ab9b45adff31d0
ms.sourcegitcommit: 39609c4d8c432c8e7d7a31cb35c8020e5207385b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/30/2021
ms.locfileid: "51445395"
---
# <a name="safe-documents-in-microsoft-365-e5"></a><span data-ttu-id="4d004-103">Documents sécurisés dans Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="4d004-103">Safe Documents in Microsoft 365 E5</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="4d004-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="4d004-104">**Applies to**</span></span>
- [<span data-ttu-id="4d004-105">Microsoft Defender pour Office 365 Plan 2</span><span class="sxs-lookup"><span data-stu-id="4d004-105">Microsoft Defender for Office 365 plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="4d004-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="4d004-106">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="4d004-107">La fonctionnalité Documents sécurisés dans Microsoft 365 E5 ou Microsoft 365 E5 Security utilise Microsoft [](https://support.microsoft.com/office/d6f09ac7-e6b9-4495-8e43-2bbcdbcb6653) [Defender pour](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) le point de terminaison pour analyser les documents et les fichiers ouverts en affichage protégé ou Application Guard [pour Office.](https://support.microsoft.com/topic/9e0fb9c2-ffad-43bf-8ba3-78f785fdba46)</span><span class="sxs-lookup"><span data-stu-id="4d004-107">Safe Documents is a feature in Microsoft 365 E5 or Microsoft 365 E5 Security that uses [Microsoft Defender for Endpoint](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) to scan documents and files that are opened in [Protected View](https://support.microsoft.com/office/d6f09ac7-e6b9-4495-8e43-2bbcdbcb6653) or [Application Guard for Office](https://support.microsoft.com/topic/9e0fb9c2-ffad-43bf-8ba3-78f785fdba46).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="4d004-108">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="4d004-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="4d004-109">Les documents sécurisés sont disponibles uniquement pour les utilisateurs titulaires de licences De sécurité *Microsoft 365 E5* ou *Microsoft 365 E5.*</span><span class="sxs-lookup"><span data-stu-id="4d004-109">Safe Documents is available only to users with *Microsoft 365 E5* or *Microsoft 365 E5 Security* licenses.</span></span> <span data-ttu-id="4d004-110">Ces licences ne sont pas incluses dans les plans Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="4d004-110">These licenses are not included in Microsoft Defender for Office 365 plans.</span></span>

- <span data-ttu-id="4d004-111">La sécurité des documents est prise en charge dans Microsoft 365 Apps for enterprise (anciennement Office 365 ProPlus) version 2004 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4d004-111">Safe Documents is supported in Microsoft 365 Apps for enterprise (formerly known as Office 365 ProPlus) version 2004 or later.</span></span>

- <span data-ttu-id="4d004-112">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com>.</span><span class="sxs-lookup"><span data-stu-id="4d004-112">You open the Security & Compliance Center at <https://protection.office.com>.</span></span> <span data-ttu-id="4d004-113">Pour aller directement à la page Pièces **jointes sécurisées ATP,** ouvrez <https://protection.office.com/safeattachmentv2> .</span><span class="sxs-lookup"><span data-stu-id="4d004-113">To go directly to the **ATP Safe Attachments** page, open <https://protection.office.com/safeattachmentv2>.</span></span>

- <span data-ttu-id="4d004-114">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="4d004-114">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="4d004-115">Des autorisations doivent vous avoir été attribuées dans **Exchange Online** pour que vous puissiez effectuer les procédures décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="4d004-115">You need to be assigned permissions in **Exchange Online** before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="4d004-116">Pour configurer les paramètres des documents sécurisés,  vous devez être membre des groupes de rôles Gestion de l’organisation ou **Administrateur de** la sécurité.</span><span class="sxs-lookup"><span data-stu-id="4d004-116">To configure Safe Documents settings, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="4d004-117">Pour accéder en lecture seule aux paramètres des documents  sécurisés,  vous devez être membre des groupes de rôles Lecteur global ou Lecteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="4d004-117">For read-only access to Safe Documents settings, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="4d004-118">Pour plus d'informations, voir [Permissions en échange en ligne](/exchange/permissions-exo/permissions-exo).</span><span class="sxs-lookup"><span data-stu-id="4d004-118">For more information, see [Permissions in Exchange Online](/exchange/permissions-exo/permissions-exo).</span></span>

  > [!NOTE]
  >
  > - <span data-ttu-id="4d004-119">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4d004-119">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="4d004-120">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d004-120">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  >
  > - <span data-ttu-id="4d004-121">Le groupe de rôles **Gestion de l’organisation en affichage seul** dans [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) permet également d’accéder en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="4d004-121">The **View-Only Organization Management** role group in [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

### <a name="how-does-microsoft-handle-your-data"></a><span data-ttu-id="4d004-122">Comment Microsoft gère-t-il vos données ?</span><span class="sxs-lookup"><span data-stu-id="4d004-122">How does Microsoft handle your data?</span></span>

<span data-ttu-id="4d004-123">Pour vous protéger, les documents sécurisés envoient des fichiers au cloud [Microsoft Defender for Endpoint](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) pour analyse.</span><span class="sxs-lookup"><span data-stu-id="4d004-123">To keep you protected, Safe Documents sends files to the [Microsoft Defender for Endpoint](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) cloud for analysis.</span></span> <span data-ttu-id="4d004-124">Pour plus d’informations sur la façon dont Microsoft Defender pour le point de terminaison gère vos données, voir : Microsoft Defender pour le stockage et la confidentialité des données de [point de terminaison.](/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy)</span><span class="sxs-lookup"><span data-stu-id="4d004-124">Details on how Microsoft Defender for Endpoint handles your data can be found here: [Microsoft Defender for Endpoint data storage and privacy](/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy).</span></span>

<span data-ttu-id="4d004-125">Les fichiers envoyés par des documents sécurisés ne sont pas conservés dans Defender au-delà du temps nécessaire à l’analyse (généralement, moins de 24 heures).</span><span class="sxs-lookup"><span data-stu-id="4d004-125">Files sent by Safe Documents are not retained in Defender beyond the time needed for analysis (typically, less than 24 hours).</span></span>

## <a name="use-the-security--compliance-center-to-configure-safe-documents"></a><span data-ttu-id="4d004-126">Utiliser le Centre de sécurité & conformité pour configurer des documents sécurisés</span><span class="sxs-lookup"><span data-stu-id="4d004-126">Use the Security & Compliance Center to configure Safe Documents</span></span>

1. <span data-ttu-id="4d004-127">Dans le Centre de sécurité &  conformité, allez dans Stratégie de gestion des menaces - Pièces jointes sécurisées , puis cliquez sur \>  \>  **Paramètres globaux.**</span><span class="sxs-lookup"><span data-stu-id="4d004-127">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**, and then click **Global settings**.</span></span>

2. <span data-ttu-id="4d004-128">Dans le **volant des paramètres globaux** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="4d004-128">In the **Global settings** fly out that appears, configure the following settings:</span></span>

   - <span data-ttu-id="4d004-129">**Activer les documents sécurisés pour les clients Office**: déplacez le basculement vers la droite pour activer la fonctionnalité : ![ activer. ](../../media/scc-toggle-on.png)</span><span class="sxs-lookup"><span data-stu-id="4d004-129">**Turn on Safe Documents for Office clients**: Move the toggle to the right to turn on the feature: ![Toggle on](../../media/scc-toggle-on.png).</span></span>

   - <span data-ttu-id="4d004-130">Autoriser les utilisateurs à cliquer dans le affichage protégé même si les **documents sécurisés identifient** le fichier comme malveillant : nous vous recommandons de laisser cette option désactivée (laissez le bouton bascule vers la gauche : ![ basculez vers la ](../../media/scc-toggle-off.png) gauche).</span><span class="sxs-lookup"><span data-stu-id="4d004-130">**Allow people to click through Protected View even if Safe Documents identifies the file as malicious**: We recommend that you leave this option turned off (leave the toggle to the left: ![Toggle off](../../media/scc-toggle-off.png)).</span></span>

   <span data-ttu-id="4d004-131">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4d004-131">When you're finished, click **Save**.</span></span>

   ![Paramètres des documents sécurisés après la sélection des paramètres globaux dans la page Pièces jointes sécurisées.](../../media/safe-docs.png)

### <a name="use-exchange-online-powershell-to-configure-safe-documents"></a><span data-ttu-id="4d004-133">Utiliser Exchange Online PowerShell pour configurer des documents sécurisés</span><span class="sxs-lookup"><span data-stu-id="4d004-133">Use Exchange Online PowerShell to configure Safe Documents</span></span>

<span data-ttu-id="4d004-134">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="4d004-134">Use the following syntax:</span></span>

```powershell
Set-AtpPolicyForO365 -EnableSafeDocs <$true | $false> -AllowSafeDocsOpen <$true | $false>
```

- <span data-ttu-id="4d004-135">Le _paramètre EnableSafeDocs_ active ou désactive les documents sécurisés pour l’ensemble de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="4d004-135">The _EnableSafeDocs_ parameter enables or disables Safe Documents for the entire organization.</span></span>
- <span data-ttu-id="4d004-136">Le _paramètre AllowSafeDocsOpen_ permet ou empêche les utilisateurs de quitter le affichage protégé (c’est-à-dire, l’ouverture du document) si le document a été identifié comme malveillant.</span><span class="sxs-lookup"><span data-stu-id="4d004-136">The _AllowSafeDocsOpen_ parameter allows or prevents users from leaving Protected View (that is, opening the document) if the document has been identified as malicious.</span></span>

<span data-ttu-id="4d004-137">Cet exemple active les documents sécurisés pour l’ensemble de l’organisation et empêche les utilisateurs d’ouvrir des documents qui ont été identifiés comme malveillants en affichage protégé.</span><span class="sxs-lookup"><span data-stu-id="4d004-137">This example enables Safe Documents for the entire organization, and prevents users from opening documents that have been identified as malicious from Protected View.</span></span>

```powershell
Set-AtpPolicyForO365 -EnableSafeDocs $true -AllowSafeDocsOpen $false
```

<span data-ttu-id="4d004-138">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-AtpPolicyForO365](/powershell/module/exchange/set-atppolicyforo365).</span><span class="sxs-lookup"><span data-stu-id="4d004-138">For detailed syntax and parameter information, see [Set-AtpPolicyForO365](/powershell/module/exchange/set-atppolicyforo365).</span></span>

### <a name="onboard-to-the-microsoft-defender-for-endpoint-service-to-enable-auditing-capabilities"></a><span data-ttu-id="4d004-139">Intégration au service Microsoft Defender for Endpoint pour activer les fonctionnalités d’audit</span><span class="sxs-lookup"><span data-stu-id="4d004-139">Onboard to the Microsoft Defender for Endpoint Service to enable auditing capabilities</span></span>

<span data-ttu-id="4d004-140">Pour déployer Microsoft Defender pour endpoint, vous devez passer par les différentes phases de déploiement.</span><span class="sxs-lookup"><span data-stu-id="4d004-140">To deploy Microsoft Defender for Endpoint, you need to go through the various phases of deployment.</span></span> <span data-ttu-id="4d004-141">Après l’intégration, vous pouvez configurer les fonctionnalités d’audit dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="4d004-141">After onboarding, you can configure auditing capabilities in the Security & Compliance Center.</span></span>

<span data-ttu-id="4d004-142">Pour plus d’informations, [voir Intégrer au service Microsoft Defender for Endpoint.](/microsoft-365/security/defender-endpoint/onboarding)</span><span class="sxs-lookup"><span data-stu-id="4d004-142">To learn more, see [Onboard to the Microsoft Defender for Endpoint service](/microsoft-365/security/defender-endpoint/onboarding).</span></span> <span data-ttu-id="4d004-143">Si vous avez besoin d’aide supplémentaire, reportez-vous à La résolution des problèmes d’intégration de Microsoft Defender pour les points [de terminaison.](/microsoft-365/security/defender-endpoint/troubleshoot-onboarding)</span><span class="sxs-lookup"><span data-stu-id="4d004-143">If you need additional help, please refer to [Troubleshoot Microsoft Defender for Endpoint onboarding issues](/microsoft-365/security/defender-endpoint/troubleshoot-onboarding).</span></span>

### <a name="how-do-i-know-this-worked"></a><span data-ttu-id="4d004-144">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="4d004-144">How do I know this worked?</span></span>

<span data-ttu-id="4d004-145">Pour vérifier que vous avez activé et configuré les documents sécurisés, faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4d004-145">To verify that you've enabled and configured Safe Documents, do any of the following steps:</span></span>

- <span data-ttu-id="4d004-146">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments,** click Global **settings**, and verify the Turn on Safe Documents for Office **clients** and Allow people to click **through Protected View even if Safe Documents identifies the file as malicious** settings.</span><span class="sxs-lookup"><span data-stu-id="4d004-146">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**, click **Global settings**, and verify the **Turn on Safe Documents for Office clients** and **Allow people to click through Protected View even if Safe Documents identifies the file as malicious** settings.</span></span>

- <span data-ttu-id="4d004-147">Exécutez la commande suivante dans Exchange Online PowerShell et vérifiez les valeurs des propriétés :</span><span class="sxs-lookup"><span data-stu-id="4d004-147">Run the following command in Exchange Online PowerShell and verify the property values:</span></span>

  ```powershell
  Get-AtpPolicyForO365 | Format-List *SafeDocs*
  ```

- <span data-ttu-id="4d004-148">Les fichiers suivants sont disponibles pour tester la protection des documents sécurisés.</span><span class="sxs-lookup"><span data-stu-id="4d004-148">The following files are available to test Safe Documents protection.</span></span> <span data-ttu-id="4d004-149">Ces documents sont similaires au fichier EICAR.TXT pour tester les solutions antivirus et anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="4d004-149">These documents are similar to the EICAR.TXT file for testing anti-malware and anti-virus solutions.</span></span> <span data-ttu-id="4d004-150">Les fichiers ne sont pas dangereux, mais ils déclenchent la protection des documents sécurisés.</span><span class="sxs-lookup"><span data-stu-id="4d004-150">The files are not harmful, but they will trigger Safe Documents protection.</span></span>

  - [<span data-ttu-id="4d004-151">SafeDocsDemo.docx</span><span class="sxs-lookup"><span data-stu-id="4d004-151">SafeDocsDemo.docx</span></span>](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/downloads/SafeDocsDemo.docx)
  - [<span data-ttu-id="4d004-152">SafeDocsDemo.pptx</span><span class="sxs-lookup"><span data-stu-id="4d004-152">SafeDocsDemo.pptx</span></span>](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/downloads/SafeDocsDemo.pptx)
  - [<span data-ttu-id="4d004-153">SafeDocsDemo.xlsx</span><span class="sxs-lookup"><span data-stu-id="4d004-153">SafeDocsDemo.xlsx</span></span>](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/downloads/SafeDocsDemo.xlsx)
