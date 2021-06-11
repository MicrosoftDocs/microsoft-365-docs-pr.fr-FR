---
title: Protéger les dossiers importants contre les ransomware contre le chiffrement de vos fichiers avec accès contrôlé aux dossiers
description: Les fichiers des dossiers par défaut peuvent être protégés contre les changements par des applications malveillantes. Empêcher les ransomware de chiffrer vos fichiers.
keywords: accès contrôlé aux dossiers, windows 10, windows defender, ransomware, protéger, fichiers, dossiers
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
audience: ITPro
ms.date: 06/10/2021
ms.reviewer: v-maave
manager: dansimp
ms.custom: asr
ms.technology: mde
ms.topic: how-to
ms.openlocfilehash: c60620d2a589c8473764b810d1fcb0e24f674451
ms.sourcegitcommit: 33d19853a38dfa4e6ed21b313976643670a14581
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "52904055"
---
# <a name="protect-important-folders-with-controlled-folder-access"></a><span data-ttu-id="32d59-105">Protéger les dossiers importants avec un accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="32d59-105">Protect important folders with controlled folder access</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="32d59-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="32d59-106">**Applies to:**</span></span>
- [<span data-ttu-id="32d59-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="32d59-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="32d59-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="32d59-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="32d59-109">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="32d59-109">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="32d59-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="32d59-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)

## <a name="what-is-controlled-folder-access"></a><span data-ttu-id="32d59-111">Qu’est-ce que l’accès contrôlé aux dossiers ?</span><span class="sxs-lookup"><span data-stu-id="32d59-111">What is controlled folder access?</span></span>

<span data-ttu-id="32d59-112">L’accès contrôlé aux dossiers permet de protéger vos données précieuses contre les applications malveillantes et les menaces, telles que les ransomware.</span><span class="sxs-lookup"><span data-stu-id="32d59-112">Controlled folder access helps protect your valuable data from malicious apps and threats, such as ransomware.</span></span> <span data-ttu-id="32d59-113">L’accès contrôlé aux dossiers protège vos données en vérifiant les applications par rapport à une liste d’applications connues et fiables.</span><span class="sxs-lookup"><span data-stu-id="32d59-113">Controlled folder access protects your data by checking apps against a list of known, trusted apps.</span></span> <span data-ttu-id="32d59-114">Pris en charge sur les clients Windows Server 2019 et Windows 10, l’accès contrôlé aux dossiers peut être désactivé à l’aide de Sécurité Windows App, Microsoft Endpoint Configuration Manager ou Intune (pour les appareils gérés).</span><span class="sxs-lookup"><span data-stu-id="32d59-114">Supported on Windows Server 2019 and Windows 10 clients, controlled folder access can be turned on using the Windows Security App, Microsoft Endpoint Configuration Manager, or Intune (for managed devices).</span></span> 

> [!NOTE]
> <span data-ttu-id="32d59-115">Les moteurs de script ne sont pas fiables et vous ne pouvez pas leur autoriser l’accès aux dossiers protégés contrôlés.</span><span class="sxs-lookup"><span data-stu-id="32d59-115">Scripting engines are not trusted and you cannot allow them access to controlled protected folders.</span></span>  <span data-ttu-id="32d59-116">Par exemple, PowerShell n’est pas approuvé par l’accès contrôlé aux [dossiers,](/microsoft-365/security/defender-endpoint/indicator-certificates)même si vous l’autorisez avec des indicateurs de certificat et de fichier.</span><span class="sxs-lookup"><span data-stu-id="32d59-116">For example, PowerShell is not trusted by controlled folder access, even if you allow with [certificate and file indicators](/microsoft-365/security/defender-endpoint/indicator-certificates).</span></span> 

<span data-ttu-id="32d59-117">L’accès contrôlé aux dossiers fonctionne mieux avec [Microsoft Defender pour point](microsoft-defender-endpoint.md)de terminaison, qui vous fournit des rapports détaillés sur les événements et les blocs d’accès contrôlé aux dossiers dans le cadre des scénarios d’investigation d’alerte [habituels.](investigate-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="32d59-117">Controlled folder access works best with [Microsoft Defender for Endpoint](microsoft-defender-endpoint.md), which gives you detailed reporting into controlled folder access events and blocks as part of the usual [alert investigation scenarios](investigate-alerts.md).</span></span>

> [!TIP]
> <span data-ttu-id="32d59-118">Les blocs d’accès contrôlé aux dossiers ne génèrent pas d’alertes dans la file [d’attente des alertes.](alerts-queue.md)</span><span class="sxs-lookup"><span data-stu-id="32d59-118">Controlled folder access blocks don't generate alerts in the [Alerts queue](alerts-queue.md).</span></span> <span data-ttu-id="32d59-119">Toutefois, vous pouvez afficher des informations [](investigate-machines.md)sur les blocs d’accès contrôlés aux dossiers dans l’affichage chronologie de l’appareil, lors de l’utilisation d’un repérage avancé [ou](advanced-hunting-overview.md)avec des règles de [détection personnalisées.](custom-detection-rules.md)</span><span class="sxs-lookup"><span data-stu-id="32d59-119">However, you can view information about controlled folder access blocks in the [device timeline view](investigate-machines.md), while using [advanced hunting](advanced-hunting-overview.md), or with [custom detection rules](custom-detection-rules.md).</span></span>

## <a name="how-does-controlled-folder-access-work"></a><span data-ttu-id="32d59-120">Comment fonctionne l’accès contrôlé aux dossiers ?</span><span class="sxs-lookup"><span data-stu-id="32d59-120">How does controlled folder access work?</span></span>

<span data-ttu-id="32d59-121">L’accès contrôlé aux dossiers fonctionne uniquement en permettant aux applications de confiance d’accéder aux dossiers protégés.</span><span class="sxs-lookup"><span data-stu-id="32d59-121">Controlled folder access works by only allowing trusted apps to access protected folders.</span></span> <span data-ttu-id="32d59-122">Les dossiers protégés sont spécifiés lorsque l’accès contrôlé aux dossiers est configuré.</span><span class="sxs-lookup"><span data-stu-id="32d59-122">Protected folders are specified when controlled folder access is configured.</span></span> <span data-ttu-id="32d59-123">En règle générale, les dossiers couramment utilisés, tels que ceux utilisés pour les documents, les images, les téléchargements, etc., sont inclus dans la liste des dossiers contrôlés.</span><span class="sxs-lookup"><span data-stu-id="32d59-123">Typically, commonly used folders, such as those used for documents, pictures, downloads, and so on, are included in the list of controlled folders.</span></span> 

<span data-ttu-id="32d59-124">L’accès contrôlé aux dossiers fonctionne avec une liste d’applications de confiance.</span><span class="sxs-lookup"><span data-stu-id="32d59-124">Controlled folder access works with a list of trusted apps.</span></span> <span data-ttu-id="32d59-125">Les applications incluses dans la liste des logiciels de confiance fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="32d59-125">Apps that are included in the list of trusted software work as expected.</span></span> <span data-ttu-id="32d59-126">Les applications qui ne sont pas incluses dans la liste sont empêchées d’apporter des modifications aux fichiers à l’intérieur de dossiers protégés.</span><span class="sxs-lookup"><span data-stu-id="32d59-126">Apps that are not included in the list are prevented from making any changes to files inside protected folders.</span></span> 

<span data-ttu-id="32d59-127">Les applications sont ajoutées à la liste en fonction de leur prévalence et de leur réputation.</span><span class="sxs-lookup"><span data-stu-id="32d59-127">Apps are added to the list based upon their prevalence and reputation.</span></span> <span data-ttu-id="32d59-128">Les applications qui sont très répandues dans toute votre organisation et qui n’ont jamais affiché de comportement considéré comme malveillant sont considérées comme fiables.</span><span class="sxs-lookup"><span data-stu-id="32d59-128">Apps that are highly prevalent throughout your organization and that have never displayed any behavior deemed malicious are considered trustworthy.</span></span> <span data-ttu-id="32d59-129">Ces applications sont ajoutées automatiquement à la liste.</span><span class="sxs-lookup"><span data-stu-id="32d59-129">Those apps are added to the list automatically.</span></span>

<span data-ttu-id="32d59-130">Les applications peuvent également être ajoutées manuellement à la liste de confiance à l’aide de Configuration Manager ou d’Intune.</span><span class="sxs-lookup"><span data-stu-id="32d59-130">Apps can also be added manually to the trusted list by using Configuration Manager or Intune.</span></span> <span data-ttu-id="32d59-131">Des actions supplémentaires, telles que l’ajout d’un [indicateur de fichier](respond-file-alerts.md#add-indicator-to-block-or-allow-a-file) pour une application, peuvent être effectuées à partir de la console du centre de sécurité.</span><span class="sxs-lookup"><span data-stu-id="32d59-131">Additional actions, such as [adding a file indicator](respond-file-alerts.md#add-indicator-to-block-or-allow-a-file) for an app, can be performed from the Security Center Console.</span></span>

## <a name="why-controlled-folder-access-is-important"></a><span data-ttu-id="32d59-132">Pourquoi l’accès contrôlé aux dossiers est-il important ?</span><span class="sxs-lookup"><span data-stu-id="32d59-132">Why controlled folder access is important</span></span>

<span data-ttu-id="32d59-133">L’accès contrôlé aux dossiers est particulièrement utile pour protéger vos documents et informations contre les [ransomware.](https://www.microsoft.com/wdsi/threats/ransomware)</span><span class="sxs-lookup"><span data-stu-id="32d59-133">Controlled folder access is especially useful in helping to protect your documents and information from [ransomware](https://www.microsoft.com/wdsi/threats/ransomware).</span></span> <span data-ttu-id="32d59-134">Dans le cas d’une attaque par ransomware, vos fichiers peuvent être chiffrés et maintenus en maison d’amis.</span><span class="sxs-lookup"><span data-stu-id="32d59-134">In a ransomware attack, your files can get encrypted and held hostage.</span></span> <span data-ttu-id="32d59-135">Une fois l’accès contrôlé aux dossiers en place, une notification s’affiche sur l’ordinateur sur lequel une application a tenté d’apporter des modifications à un fichier dans un dossier protégé.</span><span class="sxs-lookup"><span data-stu-id="32d59-135">With controlled folder access in place, a notification appears on the computer where an app attempted to make changes to a file in a protected folder.</span></span> <span data-ttu-id="32d59-136">Vous pouvez [personnaliser la notification avec](customize-attack-surface-reduction.md#customize-the-notification) les détails et les coordonnées de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="32d59-136">You can [customize the notification](customize-attack-surface-reduction.md#customize-the-notification) with your company details and contact information.</span></span> <span data-ttu-id="32d59-137">Vous pouvez également activer les règles individuellement pour personnaliser les techniques que la fonctionnalité surveille.</span><span class="sxs-lookup"><span data-stu-id="32d59-137">You can also enable the rules individually to customize what techniques the feature monitors.</span></span>

<span data-ttu-id="32d59-138">Les [dossiers protégés incluent les dossiers](#review-controlled-folder-access-events-in-windows-event-viewer) système courants (y compris les secteurs de démarrage) et vous pouvez [ajouter d’autres dossiers.](customize-controlled-folders.md#protect-additional-folders)</span><span class="sxs-lookup"><span data-stu-id="32d59-138">The [protected folders](#review-controlled-folder-access-events-in-windows-event-viewer) include common system folders (including boot sectors), and you can [add more folders](customize-controlled-folders.md#protect-additional-folders).</span></span> <span data-ttu-id="32d59-139">Vous pouvez également [autoriser les applications](customize-controlled-folders.md#allow-specific-apps-to-make-changes-to-controlled-folders) à leur donner accès aux dossiers protégés.</span><span class="sxs-lookup"><span data-stu-id="32d59-139">You can also [allow apps](customize-controlled-folders.md#allow-specific-apps-to-make-changes-to-controlled-folders) to give them access to the protected folders.</span></span>

<span data-ttu-id="32d59-140">Vous pouvez utiliser le [mode audit pour](audit-windows-defender.md) évaluer l’impact de l’accès contrôlé aux dossiers sur votre organisation s’il était activé.</span><span class="sxs-lookup"><span data-stu-id="32d59-140">You can use [audit mode](audit-windows-defender.md) to evaluate how controlled folder access would impact your organization if it were enabled.</span></span> <span data-ttu-id="32d59-141">Vous pouvez également visiter le site web Windows Defender test au [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) pour vérifier que la fonctionnalité fonctionne et voir comment elle fonctionne.</span><span class="sxs-lookup"><span data-stu-id="32d59-141">You can also visit the Windows Defender Test ground website at [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) to confirm the feature is working and see how it works.</span></span>

<span data-ttu-id="32d59-142">L’accès contrôlé aux dossiers est pris en charge sur les versions suivantes Windows :</span><span class="sxs-lookup"><span data-stu-id="32d59-142">Controlled folder access is supported on the following versions of Windows:</span></span>
- <span data-ttu-id="32d59-143">[Windows 10, version 1709 et](/windows/whats-new/whats-new-windows-10-version-1709) ultérieures</span><span class="sxs-lookup"><span data-stu-id="32d59-143">[Windows 10, version 1709](/windows/whats-new/whats-new-windows-10-version-1709) and later</span></span>
- [<span data-ttu-id="32d59-144">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="32d59-144">Windows Server 2019</span></span>](/windows-server/get-started-19/whats-new-19)

## <a name="windows-system-folders-are-protected-by-default"></a><span data-ttu-id="32d59-145">Windows dossiers système sont protégés par défaut</span><span class="sxs-lookup"><span data-stu-id="32d59-145">Windows system folders are protected by default</span></span>

<span data-ttu-id="32d59-146">Windows système sont protégés par défaut, ainsi que plusieurs autres dossiers :</span><span class="sxs-lookup"><span data-stu-id="32d59-146">Windows system folders are protected by default, along with several other folders:</span></span> 

- `c:\Users\<username>\Documents`
- `c:\Users\Public\Documents`
- `c:\Users\<username>\Pictures`
- `c:\Users\Public\Pictures`
- `c:\Users\Public\Videos`
- `c:\Users\<username>\Videos`
- `c:\Users\<username>\Music`
- `c:\Users\Public\Music`
- `c:\Users\<username>\Favorites`

> [!NOTE]
> <span data-ttu-id="32d59-147">Vous pouvez configurer des dossiers supplémentaires comme étant protégés, mais vous ne pouvez pas supprimer les Windows système qui sont protégés par défaut.</span><span class="sxs-lookup"><span data-stu-id="32d59-147">You can configure additional folders as protected, but you cannot remove the Windows system folders that are protected by default.</span></span>

## <a name="requirements-for-controlled-folder-access"></a><span data-ttu-id="32d59-148">Conditions requises pour l’accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="32d59-148">Requirements for controlled folder access</span></span>

<span data-ttu-id="32d59-149">L’accès contrôlé aux dossiers [nécessite l’activation Antivirus Microsoft Defender protection en temps réel.](/windows/security/threat-protection/microsoft-defender-antivirus/configure-real-time-protection-microsoft-defender-antivirus)</span><span class="sxs-lookup"><span data-stu-id="32d59-149">Controlled folder access requires enabling [Microsoft Defender Antivirus real-time protection](/windows/security/threat-protection/microsoft-defender-antivirus/configure-real-time-protection-microsoft-defender-antivirus).</span></span>

## <a name="review-controlled-folder-access-events-in-the-microsoft-365-defender-portal"></a><span data-ttu-id="32d59-150">Passer en revue les événements d’accès contrôlé aux dossiers dans le portail Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="32d59-150">Review controlled folder access events in the Microsoft 365 Defender portal</span></span>

<span data-ttu-id="32d59-151">Defender for Endpoint fournit des rapports détaillés sur les événements et les blocages dans le cadre de ses [scénarios](investigate-alerts.md) d’investigation d’alerte dans le portail Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="32d59-151">Defender for Endpoint provides detailed reporting into events and blocks as part of its [alert investigation scenarios](investigate-alerts.md) in the Microsoft 365 Defender portal.</span></span> <span data-ttu-id="32d59-152">(Voir [Microsoft Defender pour le point de terminaison dans Microsoft 365 Defender.)](../defender/microsoft-365-security-center-mde.md)</span><span class="sxs-lookup"><span data-stu-id="32d59-152">(See [Microsoft Defender for Endpoint in Microsoft 365 Defender](../defender/microsoft-365-security-center-mde.md).)</span></span>

<span data-ttu-id="32d59-153">Vous pouvez interroger Microsoft Defender pour obtenir des données de point de terminaison à l’aide du [recherche avancée.](/microsoft-365/security/defender-endpoint/advanced-hunting-windows-defender-advanced-threat-protection)</span><span class="sxs-lookup"><span data-stu-id="32d59-153">You can query Microsoft Defender for Endpoint data by using [Advanced hunting](/microsoft-365/security/defender-endpoint/advanced-hunting-windows-defender-advanced-threat-protection).</span></span> <span data-ttu-id="32d59-154">Si vous utilisez le [mode audit,](audit-windows-defender.md)vous pouvez utiliser la recherche avancée pour voir comment les paramètres d’accès contrôlé aux dossiers auraient une incidence sur votre environnement s’ils étaient activés. [](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="32d59-154">If you're using [audit mode](audit-windows-defender.md), you can use [advanced hunting](advanced-hunting-overview.md) to see how controlled folder access settings would affect your environment if they were enabled.</span></span>

<span data-ttu-id="32d59-155">Exemples de requête :</span><span class="sxs-lookup"><span data-stu-id="32d59-155">Example query:</span></span>

```PowerShell
DeviceEvents
| where ActionType in ('ControlledFolderAccessViolationAudited','ControlledFolderAccessViolationBlocked')
```

## <a name="review-controlled-folder-access-events-in-windows-event-viewer"></a><span data-ttu-id="32d59-156">Passer en revue les événements d’accès contrôlé aux dossiers dans Windows’observateur d’événements</span><span class="sxs-lookup"><span data-stu-id="32d59-156">Review controlled folder access events in Windows Event Viewer</span></span>

<span data-ttu-id="32d59-157">Vous pouvez consulter le journal Windows événements pour voir les événements créés lorsque l’accès contrôlé aux dossiers bloque (ou audite) une application :</span><span class="sxs-lookup"><span data-stu-id="32d59-157">You can review the Windows event log to see events that are created when controlled folder access blocks (or audits) an app:</span></span>

1. <span data-ttu-id="32d59-158">Téléchargez le [package d’évaluation](https://aka.ms/mp7z2w) et *extrayez* le fichiercfa-events.xmlun emplacement facilement accessible sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="32d59-158">Download the [Evaluation Package](https://aka.ms/mp7z2w) and extract the file *cfa-events.xml* to an easily accessible location on the device.</span></span>
2. <span data-ttu-id="32d59-159">Tapez **Observateur d’événements** dans le menu Démarrer pour ouvrir l Windows’observateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="32d59-159">Type **Event viewer** in the Start menu to open the Windows Event Viewer.</span></span>
3. <span data-ttu-id="32d59-160">Dans le panneau gauche, sous **Actions,** **sélectionnez Importer un affichage personnalisé...**.</span><span class="sxs-lookup"><span data-stu-id="32d59-160">On the left panel, under **Actions**, select **Import custom view...**.</span></span>
4. <span data-ttu-id="32d59-161">Accédez à l’endroit où *vous avezcfa-events.xml* et sélectionnez-le.</span><span class="sxs-lookup"><span data-stu-id="32d59-161">Navigate to where you extracted *cfa-events.xml* and select it.</span></span> <span data-ttu-id="32d59-162">Vous pouvez également [copier le XML directement.](event-views.md)</span><span class="sxs-lookup"><span data-stu-id="32d59-162">Alternatively, [copy the XML directly](event-views.md).</span></span>
5. <span data-ttu-id="32d59-163">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="32d59-163">Select **OK**.</span></span>

<span data-ttu-id="32d59-164">Le tableau suivant indique les événements liés à l’accès contrôlé aux dossiers :</span><span class="sxs-lookup"><span data-stu-id="32d59-164">The following table shows events related to controlled folder access:</span></span>

|<span data-ttu-id="32d59-165">ID de l'événement</span><span class="sxs-lookup"><span data-stu-id="32d59-165">Event ID</span></span> | <span data-ttu-id="32d59-166">Description</span><span class="sxs-lookup"><span data-stu-id="32d59-166">Description</span></span> |
|:---|:---|
|<span data-ttu-id="32d59-167">5007</span><span class="sxs-lookup"><span data-stu-id="32d59-167">5007</span></span> | <span data-ttu-id="32d59-168">Événement lorsque les paramètres sont modifiés</span><span class="sxs-lookup"><span data-stu-id="32d59-168">Event when settings are changed</span></span> |
|<span data-ttu-id="32d59-169">1124</span><span class="sxs-lookup"><span data-stu-id="32d59-169">1124</span></span> | <span data-ttu-id="32d59-170">Événement d’accès contrôlé aux dossiers audité</span><span class="sxs-lookup"><span data-stu-id="32d59-170">Audited controlled folder access event</span></span> | 
|<span data-ttu-id="32d59-171">1123</span><span class="sxs-lookup"><span data-stu-id="32d59-171">1123</span></span> | <span data-ttu-id="32d59-172">Événement d’accès contrôlé aux dossiers bloqué</span><span class="sxs-lookup"><span data-stu-id="32d59-172">Blocked controlled folder access event</span></span> |

## <a name="view-or-change-the-list-of-protected-folders"></a><span data-ttu-id="32d59-173">Afficher ou modifier la liste des dossiers protégés</span><span class="sxs-lookup"><span data-stu-id="32d59-173">View or change the list of protected folders</span></span>

<span data-ttu-id="32d59-174">Vous pouvez utiliser l’application Sécurité Windows pour afficher la liste des dossiers protégés par un accès contrôlé aux dossiers.</span><span class="sxs-lookup"><span data-stu-id="32d59-174">You can use the Windows Security app to view the list of folders that are protected by controlled folder access.</span></span> 

1. <span data-ttu-id="32d59-175">Sur votre Windows 10, ouvrez l’application Sécurité Windows’application.</span><span class="sxs-lookup"><span data-stu-id="32d59-175">On your Windows 10 device, open the Windows Security app.</span></span>
2. <span data-ttu-id="32d59-176">Sélectionnez **Protection contre les virus et les menaces**.</span><span class="sxs-lookup"><span data-stu-id="32d59-176">Select **Virus & threat protection**.</span></span>
3. <span data-ttu-id="32d59-177">Sous Protection **contre les ransomware,** **sélectionnez Gérer la protection contre les ransomware.**</span><span class="sxs-lookup"><span data-stu-id="32d59-177">Under **Ransomware protection**, select **Manage ransomware protection**.</span></span>
4. <span data-ttu-id="32d59-178">Si l’accès contrôlé aux dossiers est désactivé, vous devez l’activer.</span><span class="sxs-lookup"><span data-stu-id="32d59-178">If controlled folder access is turned off, you'll need to turn it on.</span></span> <span data-ttu-id="32d59-179">Sélectionnez **les dossiers protégés.**</span><span class="sxs-lookup"><span data-stu-id="32d59-179">Select **protected folders**.</span></span>
5. <span data-ttu-id="32d59-180">Effectuez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="32d59-180">Do one of the following steps:</span></span>
   - <span data-ttu-id="32d59-181">Pour ajouter un dossier, **sélectionnez + Ajouter un dossier protégé.**</span><span class="sxs-lookup"><span data-stu-id="32d59-181">To add a folder, select **+ Add a protected folder**.</span></span>
   - <span data-ttu-id="32d59-182">Pour supprimer un dossier, sélectionnez-le, puis sélectionnez **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="32d59-182">To remove a folder, select it, and then select **Remove**.</span></span> 

> [!NOTE]
> <span data-ttu-id="32d59-183">[Windows dossiers système](#windows-system-folders-are-protected-by-default) sont protégés par défaut et vous ne pouvez pas les supprimer de la liste.</span><span class="sxs-lookup"><span data-stu-id="32d59-183">[Windows system folders](#windows-system-folders-are-protected-by-default) are protected by default, and you cannot remove them from the list.</span></span>


