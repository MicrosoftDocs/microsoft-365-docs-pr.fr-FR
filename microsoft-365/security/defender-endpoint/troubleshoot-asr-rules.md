---
title: Signaler et résoudre les problèmes de Règles asr de Microsoft Defender pour les points de terminaison
description: Cette rubrique décrit comment signaler et dépanner les règles de résolution des problèmes de Microsoft Defender pour endpoint ASR
keywords: Règles de réduction de la surface d’attaque, asr, hips, système de prévention des intrusions hôtes, règles de protection, anti-attaque, attaque, prévention des infections, microsoft defender pour le point de terminaison
search.product: eADQiWindows 10XVcnh
ms.pagetype: security
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: Normal
audience: ITPro
author: lovina-saldanha
ms.author: v-lsaldanha
ms.reviewer: ''
manager: dansimp
ms.custom: asr
ms.topic: article
ms.technology: mde
ms.openlocfilehash: c043e97d6c02e4f41d000e9ce8cfea4a0950252a
ms.sourcegitcommit: ff20f5b4e3268c7c98a84fb1cbe7db7151596b6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "52246144"
---
# <a name="report-and-troubleshoot-microsoft-defender-for-atp-asr-rules"></a><span data-ttu-id="29da9-104">Signaler et résoudre les problèmes de Microsoft Defender pour les règles DE LAR ATP</span><span class="sxs-lookup"><span data-stu-id="29da9-104">Report and troubleshoot Microsoft Defender for ATP ASR Rules</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="29da9-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="29da9-105">**Applies to:**</span></span>

- [<span data-ttu-id="29da9-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="29da9-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="29da9-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="29da9-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="29da9-108">Le centre Microsoft 365 de sécurité est la nouvelle interface de surveillance et de gestion de la sécurité au sein de vos identités, données, appareils, applications et infrastructure Microsoft.</span><span class="sxs-lookup"><span data-stu-id="29da9-108">The Microsoft 365 security center is the new interface for monitoring and managing security across your Microsoft identities, data, devices, apps, and infrastructure.</span></span> <span data-ttu-id="29da9-109">Vous pouvez ici consulter facilement l’état de la sécurité de votre organisation, agir pour configurer les appareils, les utilisateurs et les applications ainsi que recevoir des alertes relatives aux activités suspectes.</span><span class="sxs-lookup"><span data-stu-id="29da9-109">Here you can easily view the security health of your organization, act to configure devices, users, and apps, and get alerts for suspicious activity.</span></span> <span data-ttu-id="29da9-110">Le Centre de sécurité Microsoft 365 est destiné aux administrateurs de la sécurité et aux équipes d’exploitation de la sécurité pour améliorer la gestion et la protection de leur organisation.</span><span class="sxs-lookup"><span data-stu-id="29da9-110">The Microsoft 365 security center is intended for security admins and security operations teams to better manage and protect their organization.</span></span> <span data-ttu-id="29da9-111">Visitez le centre Microsoft 365 sécurité sur https://security.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="29da9-111">Visit the Microsoft 365 security center at https://security.microsoft.com.</span></span>
<span data-ttu-id="29da9-112">Dans Microsoft 365 de sécurité, nous vous proposons un coup d’œil complet sur la configuration et les événements actuels des règles asr dans votre patrimoine.</span><span class="sxs-lookup"><span data-stu-id="29da9-112">In Microsoft 365 security center, we offer you a complete look at the current ASR rules configuration and events in your estate.</span></span> <span data-ttu-id="29da9-113">Notez que vos appareils doivent être intégrés au service Microsoft Defender for Endpoint pour que ces rapports soient remplis.</span><span class="sxs-lookup"><span data-stu-id="29da9-113">Note that your devices must be onboarded into the Microsoft Defender for Endpoint service for these reports to be populated.</span></span>
<span data-ttu-id="29da9-114">Voici une capture d’écran du centre de sécurité Microsoft 365 (sous **Réduction** de la surface d’attaque des appareils  >    >  **de rapports).**</span><span class="sxs-lookup"><span data-stu-id="29da9-114">Here's a screenshot from the Microsoft 365 security center (under **Reports** > **Devices** > **Attack surface reduction**).</span></span> <span data-ttu-id="29da9-115">Au niveau de l’appareil, **sélectionnez Configuration** dans le volet Règles de réduction de **la surface d’attaque.**</span><span class="sxs-lookup"><span data-stu-id="29da9-115">At the device level, select **Configuration** from the **Attack surface reduction rules** pane.</span></span> <span data-ttu-id="29da9-116">L’écran suivant s’affiche, dans lequel vous pouvez sélectionner un appareil spécifique et vérifier sa configuration de règle asr individuelle.</span><span class="sxs-lookup"><span data-stu-id="29da9-116">The following screen is displayed, where you can select a specific device and check its individual ASR rule configuration.</span></span>

:::image type="content" source="images/asrrulesnew.png" alt-text="Écran règles de la asr":::

## <a name="microsoft-defender-for-endpoint--advanced-hunting"></a><span data-ttu-id="29da9-118">Microsoft Defender pour le point de terminaison : recherche avancée</span><span class="sxs-lookup"><span data-stu-id="29da9-118">Microsoft Defender for Endpoint – Advanced hunting</span></span>

<span data-ttu-id="29da9-119">L’une des fonctionnalités les plus puissantes de Microsoft Defender pour point de terminaison est le recherche avancée.</span><span class="sxs-lookup"><span data-stu-id="29da9-119">One of the most powerful features of Microsoft Defender for Endpoint is advanced hunting.</span></span> <span data-ttu-id="29da9-120">Si vous ne connaissez pas le hunting avancé, recherchez de manière proactive les menaces [avec le chasse avancée.](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="29da9-120">If you're unfamiliar with advanced hunting, refer [proactively hunt for threats with advanced hunting](advanced-hunting-overview.md).</span></span>

<span data-ttu-id="29da9-121">Le repérage avancé est un outil de repérage de menaces basé sur une requête (Kusto Query Language) qui vous permet d’explorer jusqu’à 30 jours des données capturées (brutes) que le point de terminaison MDE détection et réponse (PEPT) collecte à partir de tous vos ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="29da9-121">Advanced hunting is a query-based (Kusto Query Language) threat-hunting tool that lets you explore up to 30 days of the captured (raw) data, that MDE Endpoint Detection and Response (EDR) collects from all your machines.</span></span> <span data-ttu-id="29da9-122">Grâce à la recherche avancée, vous pouvez inspecter de manière proactive les événements pour rechercher des indicateurs et des entités intéressants.</span><span class="sxs-lookup"><span data-stu-id="29da9-122">Through advanced hunting, you can proactively inspect events to locate interesting indicators and entities.</span></span> <span data-ttu-id="29da9-123">L’accès flexible aux données permet un recherche sans contraintes pour les menaces connues et potentielles.</span><span class="sxs-lookup"><span data-stu-id="29da9-123">The flexible access to data helps unconstrained hunting for both known and potential threats.</span></span>

<span data-ttu-id="29da9-124">Grâce à la recherche avancée, il est possible d’extraire des informations sur les règles de la asr, de créer des rapports et d’obtenir des informations détaillées sur le contexte d’un événement d’audit ou de blocage de règle asr donné.</span><span class="sxs-lookup"><span data-stu-id="29da9-124">Through advanced hunting, it's possible to extract ASR rules information, create reports, and get in-depth information on the context of a given ASR rule audit or block event.</span></span>

<span data-ttu-id="29da9-125">Les événements de règles ASR peuvent être interrogés à partir de la table DeviceEvents de la section de recherche avancée du Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="29da9-125">ASR rules events are available to be queried from the DeviceEvents table in the advanced hunting section of the Microsoft Defender Security Center.</span></span> <span data-ttu-id="29da9-126">Par exemple, une requête simple, telle que celle ci-dessous, peut signaler tous les événements qui ont des règles ASR en tant que source de données, au cours des 30 derniers jours, et les synthétisera par le nombre ActionType, qu’il s’agit dans ce cas du nom de code réel de la règle asr.</span><span class="sxs-lookup"><span data-stu-id="29da9-126">For example, a simple query such as the one below can report all the events that have ASR rules as data source, for the last 30 days, and will summarize them by the ActionType count, that in this case it will be the actual codename of the ASR rule.</span></span>

:::image type="content" source="images/adv-hunt-querynew.png" alt-text="Requête de recherche avancée":::

:::image type="content" source="images/adv-hunt-sc-2new.png" alt-text="écran de recherche avancée":::

<span data-ttu-id="29da9-129">Avec le repérage avancé, vous pouvez mettre en forme les requêtes à votre convenance, afin de voir ce qui se passe, que vous vouliez identifier un pointage sur un ordinateur individuel ou que vous vouliez extraire des informations de l’ensemble de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="29da9-129">With advanced hunting you can shape the queries to your liking, so that you can see what is happening, regardless of whether you want to pinpoint something on an individual machine, or you want to extract insights from your entire environment.</span></span>

## <a name="microsoft-defender-for-endpoint-machine-timeline"></a><span data-ttu-id="29da9-130">Chronologie de l’ordinateur Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="29da9-130">Microsoft Defender for Endpoint machine timeline</span></span>

<span data-ttu-id="29da9-131">Une alternative à la recherche avancée, mais avec une étendue plus étroite, est la chronologie de l’ordinateur Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="29da9-131">An alternative to advanced hunting, but with a narrower scope, is the Microsoft Defender for Endpoint machine timeline.</span></span> <span data-ttu-id="29da9-132">Vous pouvez afficher tous les événements collectés d’un appareil, au cours des six derniers mois, dans la Centre de sécurité Microsoft Defender, en allant dans la liste Ordinateurs, sélectionnez un ordinateur donné, puis cliquez sur l’onglet Chronologie.</span><span class="sxs-lookup"><span data-stu-id="29da9-132">You can view all the collected events of a device, for the past six months, in the Microsoft Defender Security Center, by going to the Machines list, select a given machine, and then click on the Timeline tab.</span></span>

<span data-ttu-id="29da9-133">Voici une capture d’écran de l’affichage Chronologie de ces événements sur un point de terminaison donné.</span><span class="sxs-lookup"><span data-stu-id="29da9-133">Pictured below is a screenshot of the Timeline view of these events on a given endpoint.</span></span>  <span data-ttu-id="29da9-134">À partir de cet affichage, vous pouvez filtrer la liste des événements en fonction de n’importe quel groupe d’événements le long du volet droit.</span><span class="sxs-lookup"><span data-stu-id="29da9-134">From this view, you can filter the events list based on any of the Event Groups along the right-side pane.</span></span> <span data-ttu-id="29da9-135">Vous pouvez également activer ou désactiver les événements marqués et verbose lors de l’affichage des alertes et du défilement dans la chronologie historique.</span><span class="sxs-lookup"><span data-stu-id="29da9-135">You can also enable or disable Flagged and Verbose events while viewing alerts and scrolling through the historical timeline.</span></span>

:::image type="content" source="images/mic-sec-def-timelinenew.png" alt-text="Chronologie du centre de sécurité microsoft Defender":::

## <a name="how-to-troubleshoot-asr-rules"></a><span data-ttu-id="29da9-137">Comment résoudre les problèmes de règles de la asr ?</span><span class="sxs-lookup"><span data-stu-id="29da9-137">How to troubleshoot ASR rules?</span></span>

<span data-ttu-id="29da9-138">La première et la plus immédiate consiste à vérifier localement, sur un appareil Windows, les règles asr sont activées (et leur configuration) à l’aide des cmdlets PowerShell.</span><span class="sxs-lookup"><span data-stu-id="29da9-138">The first and most immediate way is to check locally, on a Windows device, which ASR rules are enabled (and their configuration) is by using the PowerShell cmdlets.</span></span>

<span data-ttu-id="29da9-139">Voici quelques autres sources d’informations que vous Windows, pour résoudre les problèmes d’impact et de fonctionnement des règles asr.</span><span class="sxs-lookup"><span data-stu-id="29da9-139">Here are a few other sources of information that Windows offers, to troubleshoot ASR rules’ impact and operation.</span></span>

### <a name="querying-which-rules-are-active"></a><span data-ttu-id="29da9-140">Interrogation des règles actives</span><span class="sxs-lookup"><span data-stu-id="29da9-140">Querying which rules are active</span></span>
<span data-ttu-id="29da9-141">L’une des façons les plus simples de déterminer si les règles de la astérence sont déjà activées , par le biais d’une cmdlet PowerShell, Get-MpPreference.</span><span class="sxs-lookup"><span data-stu-id="29da9-141">One of the easiest ways to determine if ASR rules are already enabled—and, is through a PowerShell cmdlet, Get-MpPreference.</span></span>
<span data-ttu-id="29da9-142">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="29da9-142">Here's an example:</span></span>

:::image type="content" source="images/getmpreferencescriptnew.png" alt-text="obtenir un script mppreference":::

<span data-ttu-id="29da9-144">Plusieurs règles de asr sont actives, avec différentes actions configurées.</span><span class="sxs-lookup"><span data-stu-id="29da9-144">There are multiple ASR rules active, with different configured actions.</span></span>

<span data-ttu-id="29da9-145">Pour développer les informations ci-dessus sur les règles de la asr, vous pouvez utiliser les propriétés **AttackSurfaceReductionRules_Ids** et/ou **AttackSurfaceReductionRules_Actions**.</span><span class="sxs-lookup"><span data-stu-id="29da9-145">To expand the above information on ASR rules, you can use the properties **AttackSurfaceReductionRules_Ids** and/or **AttackSurfaceReductionRules_Actions**.</span></span>

<span data-ttu-id="29da9-146">Exemple :</span><span class="sxs-lookup"><span data-stu-id="29da9-146">Example:</span></span>

<span data-ttu-id="29da9-147">*Get-MPPreference, | Select-Object -ExpandProperty\*\*AttackSurfaceReductionRules_Ids*</span><span class="sxs-lookup"><span data-stu-id="29da9-147">*Get-MPPreference | Select-Object -ExpandProperty\*\*AttackSurfaceReductionRules_Ids*</span></span>

:::image type="content" source="images/getmpref-examplenew.png" alt-text="obtenir un exemple de mpreference":::

<span data-ttu-id="29da9-149">L’exemple ci-dessus montre tous les ID pour les règles de asr qui ont un paramètre différent de 0 (non configuré).</span><span class="sxs-lookup"><span data-stu-id="29da9-149">The above shows all the IDs for ASR rules that have a setting different from 0 (Not Configured).</span></span>

<span data-ttu-id="29da9-150">L’étape suivante consiste ensuite à lister les actions réelles (Bloquer ou Auditer) avec qui chaque règle est configurée.</span><span class="sxs-lookup"><span data-stu-id="29da9-150">The next step is then to list the actual actions (Block or Audit) that each rule is configured with.</span></span> 

<span data-ttu-id="29da9-151">*Get-MPPreference, | Select-Object -ExpandProperty\*\*AttackSurfaceReductionRules_Actions*</span><span class="sxs-lookup"><span data-stu-id="29da9-151">*Get-MPPreference | Select-Object -ExpandProperty\*\*AttackSurfaceReductionRules_Actions*</span></span>

:::image type="content" source="images/getmpref-example2new.png" alt-text="get mppreference example2":::

### <a name="querying-blocking-and-auditing-events"></a><span data-ttu-id="29da9-153">Interrogation des événements de blocage et d’audit</span><span class="sxs-lookup"><span data-stu-id="29da9-153">Querying blocking and auditing events</span></span>
<span data-ttu-id="29da9-154">Les événements de règle asr peuvent être vus dans Windows Defender journal.</span><span class="sxs-lookup"><span data-stu-id="29da9-154">ASR rule events can be viewed within the Windows Defender log.</span></span>

<span data-ttu-id="29da9-155">Pour y accéder, ouvrez Windows’observateur d’événements et accédez aux journaux des **applications** et des services  >  **microsoft**  >  **Windows**  >  **Windows Defender**  >  **opérationnels.**</span><span class="sxs-lookup"><span data-stu-id="29da9-155">To access it, open Windows Event Viewer, and browse to **Applications and Services Logs** > **Microsoft** > **Windows** > **Windows Defender** > **Operational**.</span></span>

:::image type="content" source="images/eventviewerscrnew.png" alt-text="scr observateur d’événements":::

## <a name="microsoft-defender-malware-protection-logs"></a><span data-ttu-id="29da9-157">Journaux de protection contre les programmes malveillants Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="29da9-157">Microsoft Defender Malware Protection Logs</span></span>
<span data-ttu-id="29da9-158">Vous pouvez également afficher les événements de règle via Antivirus Microsoft Defender’outil en ligne de commande dédié, appelé , qui peut être utilisé pour gérer et configurer, et automatiser les tâches si `*mpcmdrun.exe*` nécessaire.</span><span class="sxs-lookup"><span data-stu-id="29da9-158">You can also view rule events through the Microsoft Defender Antivirus dedicated command-line tool, called `*mpcmdrun.exe*`, that can be used to manage and configure, and automate tasks if needed.</span></span>

<span data-ttu-id="29da9-159">Vous pouvez trouver cet utilitaire dans *%ProgramFiles%\Windows Defender\MpCmdRun.exe*.</span><span class="sxs-lookup"><span data-stu-id="29da9-159">You can find this utility in *%ProgramFiles%\Windows Defender\MpCmdRun.exe*.</span></span> <span data-ttu-id="29da9-160">Vous devez l’exécuter à partir d’une invite de commandes avec élévation de privilèges (autrement dit, exécuter en tant qu’administrateur).</span><span class="sxs-lookup"><span data-stu-id="29da9-160">You must run it from an elevated command prompt (that is, run as Admin).</span></span>

<span data-ttu-id="29da9-161">Pour générer les informations de support, *tapezMpCmdRun.exe -getfiles*.</span><span class="sxs-lookup"><span data-stu-id="29da9-161">To generate the support information, type *MpCmdRun.exe -getfiles*.</span></span> <span data-ttu-id="29da9-162">Après un certain temps, plusieurs journaux seront empaquetés dans une archive (MpSupportFiles.cab) et disponibles dans *C:\ProgramData\Microsoft\Windows Defender\Support*.</span><span class="sxs-lookup"><span data-stu-id="29da9-162">After a while, several logs will be packaged into an archive (MpSupportFiles.cab) and made available in *C:\ProgramData\Microsoft\Windows Defender\Support*.</span></span>

:::image type="content" source="images/malware-prot-logsnew.png" alt-text="journaux de protection contre les programmes malveillants":::

<span data-ttu-id="29da9-164">Extrayez cette archive et de nombreux fichiers seront disponibles à des fins de dépannage.</span><span class="sxs-lookup"><span data-stu-id="29da9-164">Extract that archive and you'll have many files available for troubleshooting purposes.</span></span>

<span data-ttu-id="29da9-165">Les fichiers les plus pertinents sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="29da9-165">The most relevant files are as follows:</span></span>

- <span data-ttu-id="29da9-166">**MPOperationalEvents.txt** - Ce fichier contient le même niveau d’informations que celui de l’Observateur d’événements Windows Defender journal opérationnel de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="29da9-166">**MPOperationalEvents.txt** - This file contains same level of information found in Event Viewer for Windows Defender’s Operational log.</span></span>
- <span data-ttu-id="29da9-167">**MPRegistry.txt** : dans ce fichier, vous pouvez analyser toutes les configurations Windows Defender jour, à partir du moment où les journaux de support ont été capturés.</span><span class="sxs-lookup"><span data-stu-id="29da9-167">**MPRegistry.txt** – In this file you will can analyze all the current Windows Defender configurations, from the moment the support logs were captured.</span></span>
- <span data-ttu-id="29da9-168">**MPLog.txt** : ce journal contient des informations plus détaillées sur toutes les actions/opérations du Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="29da9-168">**MPLog.txt** – This log contains more verbose information about all the actions/operations of the Windows Defender.</span></span>
