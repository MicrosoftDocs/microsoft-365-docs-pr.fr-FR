---
title: Gérer comment et où Antivirus Microsoft Defender reçoit les mises à jour
description: Gérez l’ordre de retour de la façon dont Antivirus Microsoft Defender reçoit les mises à jour de protection.
keywords: mises à jour, lignes de base de sécurité, protection, ordre de base, ADL, MMPC, UNC, chemin d’accès au fichier, partage, wsus
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.reviewer: pahuijbr
manager: dansimp
ms.custom: nextgen
ms.technology: mde
ms.topic: article
ms.openlocfilehash: 52fe64b096b24dfc52a97fb664e408c5aeb701f4
ms.sourcegitcommit: 686f192e1a650ec805fe8e908b46ca51771ed41f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52624208"
---
# <a name="manage-the-sources-for-microsoft-defender-antivirus-protection-updates"></a><span data-ttu-id="f71d2-104">Gérer les sources des mises à jour de la protection antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="f71d2-104">Manage the sources for Microsoft Defender Antivirus protection updates</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="f71d2-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f71d2-105">**Applies to:**</span></span>

- [<span data-ttu-id="f71d2-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f71d2-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=22154037)

<a id="protection-updates"></a>
<!-- this has been used as anchor in VDI content -->

<span data-ttu-id="f71d2-107">Il est essentiel de maintenir la protection antivirus à jour.</span><span class="sxs-lookup"><span data-stu-id="f71d2-107">Keeping your antivirus protection up to date is critical.</span></span> <span data-ttu-id="f71d2-108">Il existe deux composants pour la gestion des mises à jour de protection Antivirus Microsoft Defender :</span><span class="sxs-lookup"><span data-stu-id="f71d2-108">There are two components to managing protection updates for Microsoft Defender Antivirus:</span></span> 
- <span data-ttu-id="f71d2-109">*l’endroit* à partir de laquelle les mises à jour sont téléchargées ; et</span><span class="sxs-lookup"><span data-stu-id="f71d2-109">*Where* the updates are downloaded from; and</span></span> 
- <span data-ttu-id="f71d2-110">*Lorsque les* mises à jour sont téléchargées et appliquées.</span><span class="sxs-lookup"><span data-stu-id="f71d2-110">*When* updates are downloaded and applied.</span></span> 

<span data-ttu-id="f71d2-111">Cet article explique comment spécifier l’endroit où les mises à jour doivent être téléchargées (c’est également ce qu’on appelle l’ordre de retour).</span><span class="sxs-lookup"><span data-stu-id="f71d2-111">This article describes how to specify from where updates should be downloaded (this is also known as the fallback order).</span></span> <span data-ttu-id="f71d2-112">Voir [Gérer Antivirus Microsoft Defender](manage-updates-baselines-microsoft-defender-antivirus.md) mises à jour et appliquer les lignes de base pour une vue d’ensemble sur le fonctionnement des mises à jour et la configuration d’autres aspects des mises à jour (par exemple, la planification des mises à jour).</span><span class="sxs-lookup"><span data-stu-id="f71d2-112">See [Manage Microsoft Defender Antivirus updates and apply baselines](manage-updates-baselines-microsoft-defender-antivirus.md) topic for an overview on how updates work, and how to configure other aspects of updates (such as scheduling updates).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f71d2-113">Antivirus Microsoft Defender Les mises à jour des informations de sécurité sont mises à jour via Windows Update et, à compter du lundi 21 octobre 2019, toutes les mises à jour de l’intelligence de sécurité seront signées exclusivement par SHA-2.</span><span class="sxs-lookup"><span data-stu-id="f71d2-113">Microsoft Defender Antivirus Security intelligence updates are delivered through Windows Update and starting Monday, October 21, 2019, all security intelligence updates will be SHA-2 signed exclusively.</span></span> <span data-ttu-id="f71d2-114">Vos appareils doivent être mis à jour pour prendre en charge SHA-2 afin de mettre à jour vos informations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f71d2-114">Your devices must be updated to support SHA-2 in order to update your security intelligence.</span></span> <span data-ttu-id="f71d2-115">Pour plus d’informations, voir [2019 SHA-2 Code Signing Support requirement for Windows and WSUS](https://support.microsoft.com/help/4472027/2019-sha-2-code-signing-support-requirement-for-windows-and-wsus).</span><span class="sxs-lookup"><span data-stu-id="f71d2-115">To learn more, see [2019 SHA-2 Code Signing Support requirement for Windows and WSUS](https://support.microsoft.com/help/4472027/2019-sha-2-code-signing-support-requirement-for-windows-and-wsus).</span></span>  


<a id="fallback-order"></a>

## <a name="fallback-order"></a><span data-ttu-id="f71d2-116">Ordre de retour</span><span class="sxs-lookup"><span data-stu-id="f71d2-116">Fallback order</span></span>

<span data-ttu-id="f71d2-117">En règle générale, vous configurez les points de terminaison pour télécharger individuellement les mises à jour à partir d’une source principale suivie d’autres sources par ordre de priorité, en fonction de la configuration de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="f71d2-117">Typically, you configure endpoints to individually download updates from a primary source followed by other sources in order of priority, based on your network configuration.</span></span> <span data-ttu-id="f71d2-118">Les mises à jour sont obtenues à partir de sources dans l’ordre que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="f71d2-118">Updates are obtained from sources in the order you specify.</span></span> <span data-ttu-id="f71d2-119">Si une source n’est pas disponible, la source suivante de la liste est utilisée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="f71d2-119">If a source is not available, the next source in the list is used immediately.</span></span>

<span data-ttu-id="f71d2-120">Lorsque des mises à jour sont publiées, une logique est appliquée pour réduire la taille de la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="f71d2-120">When updates are published, some logic is applied to minimize the size of the update.</span></span> <span data-ttu-id="f71d2-121">Dans la plupart des cas, seules les différences entre la dernière mise à jour et la mise à jour actuellement installée (appelée delta) sur l’appareil sont téléchargées et appliquées.</span><span class="sxs-lookup"><span data-stu-id="f71d2-121">In most cases, only the differences between the latest update and the update that is currently installed (this is referred to as the delta) on the device is downloaded and applied.</span></span> <span data-ttu-id="f71d2-122">Toutefois, la taille du delta dépend de deux facteurs principaux :</span><span class="sxs-lookup"><span data-stu-id="f71d2-122">However, the size of the delta depends on two main factors:</span></span>
- <span data-ttu-id="f71d2-123">L’âge de la dernière mise à jour sur l’appareil ; et</span><span class="sxs-lookup"><span data-stu-id="f71d2-123">The age of the last update on the device; and</span></span> 
- <span data-ttu-id="f71d2-124">Source utilisée pour télécharger et appliquer les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="f71d2-124">The source used to download and apply updates.</span></span> 

<span data-ttu-id="f71d2-125">Plus les mises à jour sur un point de terminaison sont anciennes, plus le téléchargement est volumineux.</span><span class="sxs-lookup"><span data-stu-id="f71d2-125">The older the updates on an endpoint, the larger the download will be.</span></span> <span data-ttu-id="f71d2-126">Toutefois, vous devez également prendre en compte la fréquence de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="f71d2-126">However, you must also consider download frequency as well.</span></span> <span data-ttu-id="f71d2-127">Une planification des mises à jour plus fréquente peut entraîner une utilisation plus fréquente du réseau, tandis qu’une planification moins fréquente peut entraîner des tailles de fichiers plus importantes par téléchargement.</span><span class="sxs-lookup"><span data-stu-id="f71d2-127">A more frequent update schedule can result in more network usage, whereas a less-frequent schedule can result in larger file sizes per download.</span></span> 

<span data-ttu-id="f71d2-128">Il existe cinq emplacements où vous pouvez spécifier l’emplacement où un point de terminaison doit obtenir des mises à jour :</span><span class="sxs-lookup"><span data-stu-id="f71d2-128">There are five locations where you can specify where an endpoint should obtain updates:</span></span> 

- [<span data-ttu-id="f71d2-129">Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="f71d2-129">Microsoft Update</span></span>](https://support.microsoft.com/help/12373/windows-update-faq)
- [<span data-ttu-id="f71d2-130">Windows Service de mise à jour du serveur</span><span class="sxs-lookup"><span data-stu-id="f71d2-130">Windows Server Update Service</span></span>](/windows-server/administration/windows-server-update-services/get-started/windows-server-update-services-wsus)
- [<span data-ttu-id="f71d2-131">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f71d2-131">Microsoft Endpoint Configuration Manager</span></span>](/configmgr/core/servers/manage/updates)
- [<span data-ttu-id="f71d2-132">Partage de fichiers réseau</span><span class="sxs-lookup"><span data-stu-id="f71d2-132">Network file share</span></span>](#unc-share)
- <span data-ttu-id="f71d2-133">Mises à jour de l’intelligence de la sécurité pour Antivirus Microsoft Defender et autres logiciels anti-programme malveillant [Microsoft](https://www.microsoft.com/en-us/wdsi/defenderupdates) (votre stratégie et votre Registre peuvent être répertoriés en tant qu’intelligence de sécurité CENTRE DE PROTECTION MICROSOFT CONTRE LES PROGRAMMES MALVEILLANTS (MMPC), son ancien nom).)</span><span class="sxs-lookup"><span data-stu-id="f71d2-133">[Security intelligence updates for Microsoft Defender Antivirus and other Microsoft antimalware](https://www.microsoft.com/en-us/wdsi/defenderupdates) (Your policy and registry might have this listed as Microsoft Malware Protection Center (MMPC) security intelligence, its former name.)</span></span>

<span data-ttu-id="f71d2-134">Pour garantir le meilleur niveau de protection, Microsoft Update permet des mises à jour rapides, ce qui signifie des téléchargements plus petits sur une base fréquente.</span><span class="sxs-lookup"><span data-stu-id="f71d2-134">To ensure the best level of protection, Microsoft Update allows for rapid releases, which means smaller downloads on a frequent basis.</span></span> <span data-ttu-id="f71d2-135">Les sources Windows de mise à jour du service de mise à jour du serveur, de Microsoft Endpoint Configuration Manager et de l’intelligence de sécurité Microsoft offrent des mises à jour moins fréquentes.</span><span class="sxs-lookup"><span data-stu-id="f71d2-135">The Windows Server Update Service, Microsoft Endpoint Configuration Manager, and Microsoft security intelligence updates sources deliver less frequent updates.</span></span> <span data-ttu-id="f71d2-136">Par conséquent, le delta peut être plus grand, ce qui entraîne des téléchargements plus importants.</span><span class="sxs-lookup"><span data-stu-id="f71d2-136">Thus, the delta can be larger, resulting in larger downloads.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="f71d2-137">Si vous avez définie les mises à jour de [la page](https://www.microsoft.com/security/portal/definitions/adl.aspx) d’aide à la sécurité Microsoft comme source de récupération après le service de mise à jour du serveur Windows ou Microsoft Update, les mises à jour sont téléchargées uniquement à partir des mises à jour de l’intelligence de sécurité lorsque la mise à jour actuelle est considérée comme étant hors date.</span><span class="sxs-lookup"><span data-stu-id="f71d2-137">If you have set [Microsoft Security intelligence page](https://www.microsoft.com/security/portal/definitions/adl.aspx) updates as a fallback source after Windows Server Update Service or Microsoft Update, updates are only downloaded from security intelligence updates when the current update is considered out-of-date.</span></span> <span data-ttu-id="f71d2-138">(Par défaut, cela fait sept jours consécutifs que vous ne pouvez pas appliquer les mises à jour à partir du service de mise à jour du serveur Windows ou des services Microsoft Update).</span><span class="sxs-lookup"><span data-stu-id="f71d2-138">(By default, this is seven consecutive days of not being able to apply updates from the Windows Server Update Service or Microsoft Update services).</span></span>
> <span data-ttu-id="f71d2-139">Toutefois, vous pouvez définir le nombre de jours avant que la protection ne soit signalée comme [étant hors date.](/windows/threat-protection/microsoft-defender-antivirus/manage-outdated-endpoints-microsoft-defender-antivirus#set-the-number-of-days-before-protection-is-reported-as-out-of-date)</span><span class="sxs-lookup"><span data-stu-id="f71d2-139">You can, however, [set the number of days before protection is reported as out-of-date](/windows/threat-protection/microsoft-defender-antivirus/manage-outdated-endpoints-microsoft-defender-antivirus#set-the-number-of-days-before-protection-is-reported-as-out-of-date).</span></span><p>
> <span data-ttu-id="f71d2-140">À compter du lundi 21 octobre 2019, les mises à jour des informations de sécurité seront exclusivement signées SHA-2.</span><span class="sxs-lookup"><span data-stu-id="f71d2-140">Starting Monday, October 21, 2019, security intelligence updates will be SHA-2 signed exclusively.</span></span> <span data-ttu-id="f71d2-141">Les appareils doivent être mis à jour pour prendre en charge SHA-2 afin d’obtenir les dernières mises à jour de l’intelligence de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f71d2-141">Devices must be updated to support SHA-2 in order to get the latest security intelligence updates.</span></span> <span data-ttu-id="f71d2-142">Pour plus d’informations, voir [2019 SHA-2 Code Signing Support requirement for Windows and WSUS](https://support.microsoft.com/help/4472027/2019-sha-2-code-signing-support-requirement-for-windows-and-wsus).</span><span class="sxs-lookup"><span data-stu-id="f71d2-142">To learn more, see [2019 SHA-2 Code Signing Support requirement for Windows and WSUS](https://support.microsoft.com/help/4472027/2019-sha-2-code-signing-support-requirement-for-windows-and-wsus).</span></span>

<span data-ttu-id="f71d2-143">Chaque source présente des scénarios classiques qui dépendent de la façon dont votre réseau est configuré, en plus de la fréquence de publication des mises à jour, comme décrit dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="f71d2-143">Each source has typical scenarios that depend on how your network is configured, in addition to how often they publish updates, as described in the following table:</span></span>

|<span data-ttu-id="f71d2-144">Emplacement</span><span class="sxs-lookup"><span data-stu-id="f71d2-144">Location</span></span> | <span data-ttu-id="f71d2-145">Exemple de scénario</span><span class="sxs-lookup"><span data-stu-id="f71d2-145">Sample scenario</span></span> |
|---|---|
|<span data-ttu-id="f71d2-146">Windows Service de mise à jour du serveur</span><span class="sxs-lookup"><span data-stu-id="f71d2-146">Windows Server Update Service</span></span> | <span data-ttu-id="f71d2-147">Vous utilisez Windows Server Update Service pour gérer les mises à jour de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="f71d2-147">You are using Windows Server Update Service to manage updates for your network.</span></span>|
|<span data-ttu-id="f71d2-148">Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="f71d2-148">Microsoft Update</span></span> | <span data-ttu-id="f71d2-149">Vous souhaitez que vos points de terminaison se connectent directement à Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="f71d2-149">You want your endpoints to connect directly to Microsoft Update.</span></span> <span data-ttu-id="f71d2-150">Cela peut être utile pour les points de terminaison qui se connectent de manière irrégulière à votre réseau d’entreprise, ou si vous n’utilisez pas Windows Server Update Service pour gérer vos mises à jour.</span><span class="sxs-lookup"><span data-stu-id="f71d2-150">This can be useful for endpoints that irregularly connect to your enterprise network, or if you do not use Windows Server Update Service to manage your updates.</span></span>|
|<span data-ttu-id="f71d2-151">Partage de fichiers</span><span class="sxs-lookup"><span data-stu-id="f71d2-151">File share</span></span> | <span data-ttu-id="f71d2-152">Vous avez des appareils non connectés à Internet (tels que des VM).</span><span class="sxs-lookup"><span data-stu-id="f71d2-152">You have non-Internet-connected devices (such as VMs).</span></span> <span data-ttu-id="f71d2-153">Vous pouvez utiliser votre hôte de vm connecté à Internet pour télécharger les mises à jour sur un partage réseau, à partir duquel les VM peuvent obtenir les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="f71d2-153">You can use your Internet-connected VM host to download the updates to a network share, from which the VMs can obtain the updates.</span></span> <span data-ttu-id="f71d2-154">Consultez le [guide de déploiement VDI](deployment-vdi-microsoft-defender-antivirus.md) pour savoir comment les partages de fichiers peuvent être utilisés dans les environnements d’infrastructure de bureau virtuel (VDI).</span><span class="sxs-lookup"><span data-stu-id="f71d2-154">See the [VDI deployment guide](deployment-vdi-microsoft-defender-antivirus.md) for how file shares can be used in virtual desktop infrastructure (VDI) environments.</span></span>|
|<span data-ttu-id="f71d2-155">Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="f71d2-155">Microsoft Endpoint Manager</span></span> | <span data-ttu-id="f71d2-156">Vous utilisez Microsoft Endpoint Manager pour mettre à jour vos points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="f71d2-156">You are using Microsoft Endpoint Manager to update your endpoints.</span></span>|
|<span data-ttu-id="f71d2-157">Mises à jour des informations de sécurité pour Antivirus Microsoft Defender logiciel anti-programme malveillant Microsoft (anciennement appelé MMPC)</span><span class="sxs-lookup"><span data-stu-id="f71d2-157">Security intelligence updates for Microsoft Defender Antivirus and other Microsoft antimalware (formerly referred to as MMPC)</span></span> |<span data-ttu-id="f71d2-158">[Assurez-vous que vos appareils sont mis à jour pour prendre en charge SHA-2.](https://support.microsoft.com/help/4472027/2019-sha-2-code-signing-support-requirement-for-windows-and-wsus)</span><span class="sxs-lookup"><span data-stu-id="f71d2-158">[Make sure your devices are updated to support SHA-2](https://support.microsoft.com/help/4472027/2019-sha-2-code-signing-support-requirement-for-windows-and-wsus).</span></span> <span data-ttu-id="f71d2-159">Antivirus Microsoft Defender Les mises à jour de l’intelligence de sécurité sont Windows Update et, à compter du lundi 21 octobre 2019, les mises à jour de l’intelligence de sécurité seront signées exclusivement par SHA-2.</span><span class="sxs-lookup"><span data-stu-id="f71d2-159">Microsoft Defender Antivirus Security intelligence updates are delivered through Windows Update, and starting Monday October 21, 2019 security intelligence updates will be SHA-2 signed exclusively.</span></span> <br/><span data-ttu-id="f71d2-160">Téléchargez les dernières mises à jour de protection en raison d’une infection récente ou pour mettre en service une image de base forte pour le [déploiement VDI.](deployment-vdi-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="f71d2-160">Download the latest protection updates because of a recent infection or to help provision a strong, base image for [VDI deployment](deployment-vdi-microsoft-defender-antivirus.md).</span></span> <span data-ttu-id="f71d2-161">Cette option doit généralement être utilisée uniquement comme source de retour final, et non comme source principale.</span><span class="sxs-lookup"><span data-stu-id="f71d2-161">This option should generally be used only as a final fallback source, and not the primary source.</span></span> <span data-ttu-id="f71d2-162">Elle sera utilisée uniquement si les mises à jour ne peuvent pas être téléchargées depuis Windows Server Update Service ou Microsoft Update pour un [nombre de jours spécifié.](/windows/threat-protection/microsoft-defender-antivirus/manage-outdated-endpoints-microsoft-defender-antivirus#set-the-number-of-days-before-protection-is-reported-as-out-of-date)</span><span class="sxs-lookup"><span data-stu-id="f71d2-162">It will only be used if updates cannot be downloaded from Windows Server Update Service or Microsoft Update for [a specified number of days](/windows/threat-protection/microsoft-defender-antivirus/manage-outdated-endpoints-microsoft-defender-antivirus#set-the-number-of-days-before-protection-is-reported-as-out-of-date).</span></span>|

<span data-ttu-id="f71d2-163">Vous pouvez gérer l’ordre dans lequel les sources de mise à jour sont utilisées avec la stratégie de groupe, Microsoft Endpoint Configuration Manager, les cmdlets PowerShell et WMI.</span><span class="sxs-lookup"><span data-stu-id="f71d2-163">You can manage the order in which update sources are used with Group Policy, Microsoft Endpoint Configuration Manager, PowerShell cmdlets, and WMI.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f71d2-164">Si vous définissez Windows Server Update Service comme emplacement de téléchargement, vous devez approuver les mises à jour, quel que soit l’outil de gestion que vous utilisez pour spécifier l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="f71d2-164">If you set Windows Server Update Service as a download location, you must approve the updates, regardless of the management tool you use to specify the location.</span></span> <span data-ttu-id="f71d2-165">Vous pouvez configurer une règle d’approbation automatique avec Windows Server Update Service, ce qui peut être utile lorsque les mises à jour arrivent au moins une fois par jour.</span><span class="sxs-lookup"><span data-stu-id="f71d2-165">You can set up an automatic approval rule with Windows Server Update Service, which might be useful as updates arrive at least once a day.</span></span> <span data-ttu-id="f71d2-166">Pour plus d’informations, voir synchroniser les mises à jour de la protection des points de terminaison dans Windows service de mise [à jour du serveur.](/configmgr/protect/deploy-use/endpoint-definitions-wsus#to-synchronize-endpoint-protection-definition-updates-in-standalone-wsus)</span><span class="sxs-lookup"><span data-stu-id="f71d2-166">To learn more, see [synchronize endpoint protection updates in standalone Windows Server Update Service](/configmgr/protect/deploy-use/endpoint-definitions-wsus#to-synchronize-endpoint-protection-definition-updates-in-standalone-wsus).</span></span>

<span data-ttu-id="f71d2-167">Les procédures de cet article décrivent d’abord comment définir  la commande, puis comment configurer l’option de partage de fichiers si vous l’avez activée.</span><span class="sxs-lookup"><span data-stu-id="f71d2-167">The procedures in this article first describe how to set the order, and then how to set up the **File share** option if you have enabled it.</span></span>

## <a name="use-group-policy-to-manage-the-update-location"></a><span data-ttu-id="f71d2-168">Utiliser une stratégie de groupe pour gérer l’emplacement de mise à jour</span><span class="sxs-lookup"><span data-stu-id="f71d2-168">Use Group Policy to manage the update location</span></span>

1. <span data-ttu-id="f71d2-169">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l’objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="f71d2-169">On your Group Policy management machine, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and click **Edit**.</span></span>

2. <span data-ttu-id="f71d2-170">Dans **l’Éditeur de gestion des stratégies de** groupe, allez à **Configuration ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="f71d2-170">In the **Group Policy Management Editor** go to **Computer configuration**.</span></span>

3. <span data-ttu-id="f71d2-171">Cliquez **sur Stratégies** **puis Modèles d’administration.**</span><span class="sxs-lookup"><span data-stu-id="f71d2-171">Click **Policies** then **Administrative templates**.</span></span>

4. <span data-ttu-id="f71d2-172">Développez l’arborescence **Windows composants > Windows Defender > mises** à jour des signatures et configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f71d2-172">Expand the tree to **Windows components > Windows Defender > Signature updates** and configure the following settings:</span></span>

   1.  <span data-ttu-id="f71d2-173">Double-cliquez sur **le paramètre Définir l’ordre** des sources de téléchargement des mises à jour d’informations de sécurité et définissez l’option sur **Activé.**</span><span class="sxs-lookup"><span data-stu-id="f71d2-173">Double-click the **Define the order of sources for downloading security intelligence updates** setting and set the option to **Enabled**.</span></span>

   2.  <span data-ttu-id="f71d2-174">Entrez l’ordre des sources, séparés par un seul canal, par exemple : `InternalDefinitionUpdateServer|MicrosoftUpdateServer|MMPC` , comme illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="f71d2-174">Enter the order of sources, separated by a single pipe, for example: `InternalDefinitionUpdateServer|MicrosoftUpdateServer|MMPC`, as shown in the following screenshot.</span></span>

   ![Capture d’écran du paramètre de stratégie de groupe répertoriant l’ordre des sources](images/defender/wdav-order-update-sources.png)

   3. <span data-ttu-id="f71d2-176">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="f71d2-176">Click **OK**.</span></span> <span data-ttu-id="f71d2-177">Cela définira l’ordre des sources de mise à jour de la protection.</span><span class="sxs-lookup"><span data-stu-id="f71d2-177">This will set the order of protection update sources.</span></span>

   4. <span data-ttu-id="f71d2-178">Double-cliquez sur le paramètre Définir les **partages de fichiers** pour télécharger les mises à jour de l’intelligence de sécurité et définissez l’option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="f71d2-178">Double-click the **Define file shares for downloading security intelligence updates** setting and set the option to **Enabled**.</span></span>

   5. <span data-ttu-id="f71d2-179">Entrez la source du partage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="f71d2-179">Enter the file share source.</span></span> <span data-ttu-id="f71d2-180">Si vous avez plusieurs sources, entrez chaque source dans l’ordre où elles doivent être utilisées, séparées par un seul canal.</span><span class="sxs-lookup"><span data-stu-id="f71d2-180">If you have multiple sources, enter each source in the order they should be used, separated by a single pipe.</span></span> <span data-ttu-id="f71d2-181">Utilisez [la notation UNC standard](/openspecs/windows_protocols/ms-dtyp/62e862f4-2a51-452e-8eeb-dc4ff5ee33cc) pour le chemin d’accès, par exemple : `\\host-name1\share-name\object-name|\\host-name2\share-name\object-name` .</span><span class="sxs-lookup"><span data-stu-id="f71d2-181">Use [standard UNC notation](/openspecs/windows_protocols/ms-dtyp/62e862f4-2a51-452e-8eeb-dc4ff5ee33cc) for denoting the path, for example: `\\host-name1\share-name\object-name|\\host-name2\share-name\object-name`.</span></span>  <span data-ttu-id="f71d2-182">Si vous n’entrez aucun chemin d’accès, cette source est ignorée lorsque l’VM télécharge les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="f71d2-182">If you do not enter any paths, then this source will be skipped when the VM downloads updates.</span></span>

   6. <span data-ttu-id="f71d2-183">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="f71d2-183">Click **OK**.</span></span> <span data-ttu-id="f71d2-184">Cela définit l’ordre des partages de fichiers lorsque cette source est référencé dans le paramètre de stratégie de groupe Définir l’ordre des **sources...**</span><span class="sxs-lookup"><span data-stu-id="f71d2-184">This will set the order of file shares when that source is referenced in the **Define the order of sources...** group policy setting.</span></span>

> [!NOTE]
> <span data-ttu-id="f71d2-185">Pour Windows 10, versions 1703 jusqu’à 1809 inclus, le chemin d’accès de stratégie est **Windows Components > Antivirus Microsoft Defender > Signature Updates** For Windows 10, version 1903, le chemin d’accès de stratégie est **Windows Components > Antivirus Microsoft Defender > Security Intelligence Updates**</span><span class="sxs-lookup"><span data-stu-id="f71d2-185">For Windows 10, versions 1703 up to and including 1809, the policy path is **Windows Components > Microsoft Defender Antivirus > Signature Updates** For Windows 10, version 1903, the policy path is **Windows Components > Microsoft Defender Antivirus > Security Intelligence Updates**</span></span>

## <a name="use-configuration-manager-to-manage-the-update-location"></a><span data-ttu-id="f71d2-186">Utiliser Configuration Manager pour gérer l’emplacement de mise à jour</span><span class="sxs-lookup"><span data-stu-id="f71d2-186">Use Configuration Manager to manage the update location</span></span>

<span data-ttu-id="f71d2-187">Pour [plus d’informations](/configmgr/protect/deploy-use/endpoint-definition-updates) sur la configuration Microsoft Endpoint Manager (branche actuelle), voir Configurer les mises à jour de l’intelligence de sécurité pour Endpoint Protection données.</span><span class="sxs-lookup"><span data-stu-id="f71d2-187">See [Configure Security intelligence Updates for Endpoint Protection](/configmgr/protect/deploy-use/endpoint-definition-updates) for details on configuring Microsoft Endpoint Manager (current branch).</span></span>


## <a name="use-powershell-cmdlets-to-manage-the-update-location"></a><span data-ttu-id="f71d2-188">Utiliser les cmdlets PowerShell pour gérer l’emplacement de mise à jour</span><span class="sxs-lookup"><span data-stu-id="f71d2-188">Use PowerShell cmdlets to manage the update location</span></span>

<span data-ttu-id="f71d2-189">Utilisez les cmdlets PowerShell suivantes pour définir l’ordre de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="f71d2-189">Use the following PowerShell cmdlets to set the update order.</span></span>

```PowerShell
Set-MpPreference -SignatureFallbackOrder {LOCATION|LOCATION|LOCATION|LOCATION}
Set-MpPreference -SignatureDefinitionUpdateFileSharesSource {\\UNC SHARE PATH|\\UNC SHARE PATH}
```
<span data-ttu-id="f71d2-190">Pour plus d’informations, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="f71d2-190">See the following articles for more information:</span></span>
- [<span data-ttu-id="f71d2-191">Set-MpPreference -SignatureFallbackOrder</span><span class="sxs-lookup"><span data-stu-id="f71d2-191">Set-MpPreference -SignatureFallbackOrder</span></span>](/powershell/module/defender/set-mppreference)
- [<span data-ttu-id="f71d2-192">Set-MpPreference -SignatureDefinitionUpdateFileSharesSource</span><span class="sxs-lookup"><span data-stu-id="f71d2-192">Set-MpPreference -SignatureDefinitionUpdateFileSharesSource</span></span>](/powershell/module/defender/set-mppreference#-signaturedefinitionupdatefilesharessources)
- [<span data-ttu-id="f71d2-193">Utiliser les cmdlets PowerShell pour configurer et exécuter des Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="f71d2-193">Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus</span></span>](use-powershell-cmdlets-microsoft-defender-antivirus.md)
- [<span data-ttu-id="f71d2-194">Cmdlets Defender</span><span class="sxs-lookup"><span data-stu-id="f71d2-194">Defender cmdlets</span></span>](/powershell/module/defender/index)

## <a name="use-windows-management-instruction-wmi-to-manage-the-update-location"></a><span data-ttu-id="f71d2-195">Utiliser Windows Management Instruction (WMI) pour gérer l’emplacement de mise à jour</span><span class="sxs-lookup"><span data-stu-id="f71d2-195">Use Windows Management Instruction (WMI) to manage the update location</span></span>

<span data-ttu-id="f71d2-196">Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) pour les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="f71d2-196">Use the [**Set** method of the **MSFT_MpPreference**](/previous-versions/windows/desktop/legacy/dn455323(v=vs.85)) class for the following properties:</span></span>

```WMI
SignatureFallbackOrder
SignatureDefinitionUpdateFileSharesSource
```

<span data-ttu-id="f71d2-197">Pour plus d’informations, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="f71d2-197">See the following articles for more information:</span></span>
- [<span data-ttu-id="f71d2-198">Windows Defender API WMIv2</span><span class="sxs-lookup"><span data-stu-id="f71d2-198">Windows Defender WMIv2 APIs</span></span>](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)

## <a name="use-mobile-device-management-mdm-to-manage-the-update-location"></a><span data-ttu-id="f71d2-199">Utiliser la gestion des périphériques mobiles (MDM) pour gérer l’emplacement de mise à jour</span><span class="sxs-lookup"><span data-stu-id="f71d2-199">Use Mobile Device Management (MDM) to manage the update location</span></span>

<span data-ttu-id="f71d2-200">Voir [Policy CSP - Defender/SignatureUpdateFallbackOrder](/windows/client-management/mdm/policy-csp-defender#defender-signatureupdatefallbackorder) pour plus d’informations sur la configuration de mdm.</span><span class="sxs-lookup"><span data-stu-id="f71d2-200">See [Policy CSP - Defender/SignatureUpdateFallbackOrder](/windows/client-management/mdm/policy-csp-defender#defender-signatureupdatefallbackorder) for details on configuring MDM.</span></span>

## <a name="what-if-were-using-a-third-party-vendor"></a><span data-ttu-id="f71d2-201">Que se passe-t-il si nous utilisons un fournisseur tiers ?</span><span class="sxs-lookup"><span data-stu-id="f71d2-201">What if we're using a third-party vendor?</span></span>

<span data-ttu-id="f71d2-202">Cet article explique comment configurer et gérer les mises à jour pour Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="f71d2-202">This article describes how to configure and manage updates for Microsoft Defender Antivirus.</span></span> <span data-ttu-id="f71d2-203">Toutefois, les fournisseurs tiers peuvent être utilisés pour effectuer ces tâches.</span><span class="sxs-lookup"><span data-stu-id="f71d2-203">However, third-party vendors can be used to perform these tasks.</span></span> 

<span data-ttu-id="f71d2-204">Par exemple, supposons que Contoso a embauché Fabrikam pour gérer sa solution de sécurité, qui inclut Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="f71d2-204">For example, suppose that Contoso has hired Fabrikam to manage their security solution, which includes Microsoft Defender Antivirus.</span></span> <span data-ttu-id="f71d2-205">Fabrikam utilise généralement [Windows Management Instrumentation,](./use-wmi-microsoft-defender-antivirus.md)des [cmdlets PowerShell](./use-powershell-cmdlets-microsoft-defender-antivirus.md)ou [Windows](./command-line-arguments-microsoft-defender-antivirus.md) ligne de commande pour déployer des correctifs et des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="f71d2-205">Fabrikam typically uses [Windows Management Instrumentation](./use-wmi-microsoft-defender-antivirus.md), [PowerShell cmdlets](./use-powershell-cmdlets-microsoft-defender-antivirus.md), or [Windows command-line](./command-line-arguments-microsoft-defender-antivirus.md) to deploy patches and updates.</span></span> 

> [!NOTE]
> <span data-ttu-id="f71d2-206">Microsoft ne teste pas les solutions tierces pour la gestion des Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="f71d2-206">Microsoft does not test third-party solutions for managing Microsoft Defender Antivirus.</span></span>

<a id="unc-share"></a>
## <a name="create-a-unc-share-for-security-intelligence-updates"></a><span data-ttu-id="f71d2-207">Créer un partage UNC pour les mises à jour d’informations de sécurité</span><span class="sxs-lookup"><span data-stu-id="f71d2-207">Create a UNC share for security intelligence updates</span></span>

<span data-ttu-id="f71d2-208">Configurer un partage de fichiers réseau (lecteur UNC/mappé) pour télécharger les mises à jour d’informations de sécurité à partir du site MMPC à l’aide d’une tâche programmée.</span><span class="sxs-lookup"><span data-stu-id="f71d2-208">Set up a network file share (UNC/mapped drive) to download security intelligence updates from the MMPC site by using a scheduled task.</span></span>

1. <span data-ttu-id="f71d2-209">Sur le système sur lequel vous souhaitez mettre en service le partage et télécharger les mises à jour, créez un dossier dans lequel vous enregistrerez le script.</span><span class="sxs-lookup"><span data-stu-id="f71d2-209">On the system on which you want to provision the share and download the updates, create a folder to which you will save the script.</span></span>
    ```DOS
    Start, CMD (Run as admin)
    MD C:\Tool\PS-Scripts\
    ```

2. <span data-ttu-id="f71d2-210">Créez le dossier dans lequel vous allez enregistrer les mises à jour de signature.</span><span class="sxs-lookup"><span data-stu-id="f71d2-210">Create the folder to which you will save the signature updates.</span></span>
    ```DOS
    MD C:\Temp\TempSigs\x64
    MD C:\Temp\TempSigs\x86
    ```

3. <span data-ttu-id="f71d2-211">Téléchargez le script PowerShell à [partir www.powershellgallery.com/packages/SignatureDownloadCustomTask/1.4](https://www.powershellgallery.com/packages/SignatureDownloadCustomTask/1.4).</span><span class="sxs-lookup"><span data-stu-id="f71d2-211">Download the PowerShell script from [www.powershellgallery.com/packages/SignatureDownloadCustomTask/1.4](https://www.powershellgallery.com/packages/SignatureDownloadCustomTask/1.4).</span></span>

4. <span data-ttu-id="f71d2-212">Cliquez **sur Téléchargement manuel.**</span><span class="sxs-lookup"><span data-stu-id="f71d2-212">Click **Manual Download**.</span></span>

5. <span data-ttu-id="f71d2-213">Cliquez **sur Télécharger le fichier nupkg brut.**</span><span class="sxs-lookup"><span data-stu-id="f71d2-213">Click **Download the raw nupkg file**.</span></span>

6. <span data-ttu-id="f71d2-214">Extrayons le fichier.</span><span class="sxs-lookup"><span data-stu-id="f71d2-214">Extract the file.</span></span>

7. <span data-ttu-id="f71d2-215">Copiez le fichier SignatureDownloadCustomTask.ps1 dans le dossier que vous avez précédemment créé, C:\Tool\PS-Scripts\ .</span><span class="sxs-lookup"><span data-stu-id="f71d2-215">Copy the file SignatureDownloadCustomTask.ps1 to the folder you previously created, C:\Tool\PS-Scripts\ .</span></span>

8. <span data-ttu-id="f71d2-216">Utilisez la ligne de commande pour configurer la tâche programmée.</span><span class="sxs-lookup"><span data-stu-id="f71d2-216">Use the command line to set up the scheduled task.</span></span>
    > [!NOTE]
    > <span data-ttu-id="f71d2-217">Il existe deux types de mises à jour : complète et delta.</span><span class="sxs-lookup"><span data-stu-id="f71d2-217">There are two types of updates: full and delta.</span></span>
   - <span data-ttu-id="f71d2-218">Pour le delta x64 :</span><span class="sxs-lookup"><span data-stu-id="f71d2-218">For x64 delta:</span></span>

       ```DOS
       Powershell (Run as admin)
    
       C:\Tool\PS-Scripts\
    
       ".\SignatureDownloadCustomTask.ps1 -action create -arch x64 -isDelta $true -destDir C:\Temp\TempSigs\x64 -scriptPath C:\Tool\PS-Scripts\SignatureDownloadCustomTask.ps1 -daysInterval 1"
       ```

   - <span data-ttu-id="f71d2-219">Pour x64 complet :</span><span class="sxs-lookup"><span data-stu-id="f71d2-219">For x64 full:</span></span>

       ```DOS
       Powershell (Run as admin)
    
       C:\Tool\PS-Scripts\
    
       ".\SignatureDownloadCustomTask.ps1 -action create -arch x64 -isDelta $false -destDir C:\Temp\TempSigs\x64 -scriptPath C:\Tool\PS-Scripts\SignatureDownloadCustomTask.ps1 -daysInterval 1"
       ```

   - <span data-ttu-id="f71d2-220">Pour le delta x86 :</span><span class="sxs-lookup"><span data-stu-id="f71d2-220">For x86 delta:</span></span>

       ```DOS
       Powershell (Run as admin)
    
       C:\Tool\PS-Scripts\
    
       ".\SignatureDownloadCustomTask.ps1 -action create -arch x86 -isDelta $true -destDir C:\Temp\TempSigs\x86 -scriptPath C:\Tool\PS-Scripts\SignatureDownloadCustomTask.ps1 -daysInterval 1"
       ```

   - <span data-ttu-id="f71d2-221">Pour x86 complet :</span><span class="sxs-lookup"><span data-stu-id="f71d2-221">For x86 full:</span></span>

       ```DOS
       Powershell (Run as admin)
    
       C:\Tool\PS-Scripts\
    
       ".\SignatureDownloadCustomTask.ps1 -action create -arch x86 -isDelta $false -destDir C:\Temp\TempSigs\x86 -scriptPath C:\Tool\PS-Scripts\SignatureDownloadCustomTask.ps1 -daysInterval 1"
       ```

    > [!NOTE]
    > <span data-ttu-id="f71d2-222">Lorsque les tâches programmées sont créées, vous pouvez les trouver dans le Programmeur des tâches sous Microsoft\Windows\Windows Defender</span><span class="sxs-lookup"><span data-stu-id="f71d2-222">When the scheduled tasks are created, you can find these in the Task Scheduler under Microsoft\Windows\Windows Defender</span></span>
9. <span data-ttu-id="f71d2-223">Exécutez chaque tâche manuellement et vérifiez que vous avez des données (mpam-d.exe, mpam-fe.exe et nis_full.exe) dans les dossiers suivants (vous avez peut-être choisi différents emplacements) :</span><span class="sxs-lookup"><span data-stu-id="f71d2-223">Run each task manually and verify that you have data (mpam-d.exe, mpam-fe.exe, and nis_full.exe) in the following folders (you might have chosen different locations):</span></span>

   - <span data-ttu-id="f71d2-224">C:\Temp\TempSigs\x86</span><span class="sxs-lookup"><span data-stu-id="f71d2-224">C:\Temp\TempSigs\x86</span></span>
   - <span data-ttu-id="f71d2-225">C:\Temp\TempSigs\x64</span><span class="sxs-lookup"><span data-stu-id="f71d2-225">C:\Temp\TempSigs\x64</span></span>

   <span data-ttu-id="f71d2-226">Si la tâche programmée échoue, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f71d2-226">If the scheduled task fails, run the following commands:</span></span>

    ```DOS
    C:\windows\system32\windowspowershell\v1.0\powershell.exe -NoProfile -executionpolicy allsigned -command "&\"C:\Tool\PS-Scripts\SignatureDownloadCustomTask.ps1\" -action run -arch x64 -isDelta $False -destDir C:\Temp\TempSigs\x64"
    
    C:\windows\system32\windowspowershell\v1.0\powershell.exe -NoProfile -executionpolicy allsigned -command "&\"C:\Tool\PS-Scripts\SignatureDownloadCustomTask.ps1\" -action run -arch x64 -isDelta $True -destDir C:\Temp\TempSigs\x64"
    
    C:\windows\system32\windowspowershell\v1.0\powershell.exe -NoProfile -executionpolicy allsigned -command "&\"C:\Tool\PS-Scripts\SignatureDownloadCustomTask.ps1\" -action run -arch x86 -isDelta $False -destDir C:\Temp\TempSigs\x86"
    
    C:\windows\system32\windowspowershell\v1.0\powershell.exe -NoProfile -executionpolicy allsigned -command "&\"C:\Tool\PS-Scripts\SignatureDownloadCustomTask.ps1\" -action run -arch x86 -isDelta $True -destDir C:\Temp\TempSigs\x86"
    ```
    > [!NOTE]
    > <span data-ttu-id="f71d2-227">Des problèmes peuvent également être dus à la stratégie d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f71d2-227">Issues could also be due to execution policy.</span></span>
    
10. <span data-ttu-id="f71d2-228">Créez un partage pointant vers C:\Temp\TempSigs (par exemple, \\ serveur\mises à jour).</span><span class="sxs-lookup"><span data-stu-id="f71d2-228">Create a share pointing to C:\Temp\TempSigs (e.g. \\server\updates).</span></span>
    > [!NOTE]
    > <span data-ttu-id="f71d2-229">Au minimum, les utilisateurs authentifiés doivent avoir accès en lecture.</span><span class="sxs-lookup"><span data-stu-id="f71d2-229">At a minimum, authenticated users must have "Read" access.</span></span>
11. <span data-ttu-id="f71d2-230">Définissez l’emplacement du partage dans la stratégie sur le partage.</span><span class="sxs-lookup"><span data-stu-id="f71d2-230">Set the share location in the policy to the share.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f71d2-231">N’ajoutez pas le dossier x64 (ou x86) dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="f71d2-231">Do not add the x64 (or x86) folder in the path.</span></span> <span data-ttu-id="f71d2-232">Le processus mpcmdrun.exe l’ajoute automatiquement.</span><span class="sxs-lookup"><span data-stu-id="f71d2-232">The mpcmdrun.exe process adds it automatically.</span></span>

## <a name="related-articles"></a><span data-ttu-id="f71d2-233">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="f71d2-233">Related articles</span></span>

- [<span data-ttu-id="f71d2-234">Déployer Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="f71d2-234">Deploy Microsoft Defender Antivirus</span></span>](deploy-manage-report-microsoft-defender-antivirus.md)
- [<span data-ttu-id="f71d2-235">Gérer les mises Antivirus Microsoft Defender jour et appliquer les lignes de base</span><span class="sxs-lookup"><span data-stu-id="f71d2-235">Manage Microsoft Defender Antivirus updates and apply baselines</span></span>](manage-updates-baselines-microsoft-defender-antivirus.md)
- [<span data-ttu-id="f71d2-236">Gérer les mises à jour des points de terminaison qui ne sont plus à jour</span><span class="sxs-lookup"><span data-stu-id="f71d2-236">Manage updates for endpoints that are out of date</span></span>](manage-outdated-endpoints-microsoft-defender-antivirus.md)
- [<span data-ttu-id="f71d2-237">Gérer les mises à jour forcées en fonction des événements</span><span class="sxs-lookup"><span data-stu-id="f71d2-237">Manage event-based forced updates</span></span>](manage-event-based-updates-microsoft-defender-antivirus.md)
- [<span data-ttu-id="f71d2-238">Gérer les mises à jour pour les appareils mobiles et les VM</span><span class="sxs-lookup"><span data-stu-id="f71d2-238">Manage updates for mobile devices and VMs</span></span>](manage-updates-mobile-devices-vms-microsoft-defender-antivirus.md)
- [<span data-ttu-id="f71d2-239">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="f71d2-239">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)
