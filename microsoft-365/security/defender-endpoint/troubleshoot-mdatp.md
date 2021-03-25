---
title: Résoudre les problèmes de service Microsoft Defender pour les points de terminaison
description: Trouvez des solutions et contourner les problèmes connus, tels que les erreurs de serveur lors de la tentative d’accès au service.
keywords: résoudre les problèmes de Microsoft Defender pour le point de terminaison, résoudre les problèmes de Windows ATP, erreur du serveur, accès refusé, informations d’identification non valides, aucune donnée, portail de tableau de bord, autoriser, observateur d’événements
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: troubleshooting
ms.technology: mde
ms.openlocfilehash: bd211a56ee9ed6aa871c8d55149247a4755bc863
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51064865"
---
# <a name="troubleshoot-service-issues"></a><span data-ttu-id="e7725-104">Résoudre les problèmes de service</span><span class="sxs-lookup"><span data-stu-id="e7725-104">Troubleshoot service issues</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="e7725-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e7725-105">**Applies to:**</span></span>
- [<span data-ttu-id="e7725-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e7725-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="e7725-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e7725-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="e7725-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="e7725-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="e7725-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="e7725-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-pullalerts-abovefoldlink) 


<span data-ttu-id="e7725-110">Cette section traite des problèmes qui peuvent survenir lorsque vous utilisez le service Microsoft Defender - Menace avancée.</span><span class="sxs-lookup"><span data-stu-id="e7725-110">This section addresses issues that might arise as you use the Microsoft Defender Advanced Threat service.</span></span>

## <a name="server-error---access-is-denied-due-to-invalid-credentials"></a><span data-ttu-id="e7725-111">Erreur de serveur : l’accès est refusé en raison d’informations d’identification non valides</span><span class="sxs-lookup"><span data-stu-id="e7725-111">Server error - Access is denied due to invalid credentials</span></span>
<span data-ttu-id="e7725-112">Si vous rencontrez une erreur de serveur lors de la tentative d’accès au service, vous devez modifier les paramètres de cookie de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="e7725-112">If you encounter a server error when trying to access the service, you’ll need to change your browser cookie settings.</span></span>
<span data-ttu-id="e7725-113">Configurez votre navigateur pour autoriser les cookies.</span><span class="sxs-lookup"><span data-stu-id="e7725-113">Configure your browser to allow cookies.</span></span>

## <a name="elements-or-data-missing-on-the-portal"></a><span data-ttu-id="e7725-114">Éléments ou données manquants sur le portail</span><span class="sxs-lookup"><span data-stu-id="e7725-114">Elements or data missing on the portal</span></span>
<span data-ttu-id="e7725-115">Si certains éléments ou données d’interface utilisateur sont manquants dans le Centre de sécurité Microsoft Defender, il est possible que les paramètres proxy le bloquent.</span><span class="sxs-lookup"><span data-stu-id="e7725-115">If some UI elements or data is missing on Microsoft Defender Security Center it’s possible that proxy settings are blocking it.</span></span>

<span data-ttu-id="e7725-116">Assurez-vous `*.securitycenter.windows.com` qu’elle est incluse dans la liste d’accès proxy.</span><span class="sxs-lookup"><span data-stu-id="e7725-116">Make sure that `*.securitycenter.windows.com` is included the proxy allow list.</span></span>


> [!NOTE]
> <span data-ttu-id="e7725-117">Vous devez utiliser le protocole HTTPS lors de l’ajout des points de terminaison suivants.</span><span class="sxs-lookup"><span data-stu-id="e7725-117">You must use the HTTPS protocol when adding the following endpoints.</span></span>

## <a name="microsoft-defender-for-endpoint-service-shows-event-or-error-logs-in-the-event-viewer"></a><span data-ttu-id="e7725-118">Le service Microsoft Defender for Endpoint affiche les journaux des événements ou des erreurs dans l’Observateur d’événements</span><span class="sxs-lookup"><span data-stu-id="e7725-118">Microsoft Defender for Endpoint service shows event or error logs in the Event Viewer</span></span>

<span data-ttu-id="e7725-119">Consultez la rubrique [Examiner les événements](event-error-codes.md) et les erreurs à l’aide de l’Observateur d’événements pour obtenir la liste des ID d’événement signalés par le service Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="e7725-119">See the topic [Review events and errors using Event Viewer](event-error-codes.md) for a list of event IDs that are reported by the Microsoft Defender for Endpoint service.</span></span> <span data-ttu-id="e7725-120">Cette rubrique contient également les étapes de résolution des erreurs d’événement.</span><span class="sxs-lookup"><span data-stu-id="e7725-120">The topic also contains troubleshooting steps for event errors.</span></span>

## <a name="microsoft-defender-for-endpoint-service-fails-to-start-after-a-reboot-and-shows-error-577"></a><span data-ttu-id="e7725-121">Le service Microsoft Defender for Endpoint ne parvient pas à démarrer après un redémarrage et affiche l’erreur 577</span><span class="sxs-lookup"><span data-stu-id="e7725-121">Microsoft Defender for Endpoint service fails to start after a reboot and shows error 577</span></span>

<span data-ttu-id="e7725-122">Si l’intégration des appareils se termine correctement, mais que Microsoft Defender pour le point de terminaison ne démarre pas après un redémarrage et affiche l’erreur 577, vérifiez que Windows Defender n’est pas désactivé par une stratégie.</span><span class="sxs-lookup"><span data-stu-id="e7725-122">If onboarding devices successfully completes but Microsoft Defender for Endpoint does not start after a reboot and shows error 577, check that Windows Defender is not disabled by a policy.</span></span>

<span data-ttu-id="e7725-123">Pour plus d’informations, [voir s’assurer que l’Antivirus Microsoft Defender n’est pas désactivé par la stratégie.](troubleshoot-onboarding.md#ensure-that-microsoft-defender-antivirus-is-not-disabled-by-a-policy)</span><span class="sxs-lookup"><span data-stu-id="e7725-123">For more information, see [Ensure that Microsoft Defender Antivirus is not disabled by policy](troubleshoot-onboarding.md#ensure-that-microsoft-defender-antivirus-is-not-disabled-by-a-policy).</span></span>

## <a name="known-issues-with-regional-formats"></a><span data-ttu-id="e7725-124">Problèmes connus avec les formats régionaux</span><span class="sxs-lookup"><span data-stu-id="e7725-124">Known issues with regional formats</span></span>

<span data-ttu-id="e7725-125">**Formats de date et d’heure**</span><span class="sxs-lookup"><span data-stu-id="e7725-125">**Date and time formats**</span></span><br>
<span data-ttu-id="e7725-126">Il existe des problèmes connus avec les formats d’heure et de date.</span><span class="sxs-lookup"><span data-stu-id="e7725-126">There are some known issues with the time and date formats.</span></span> 

<span data-ttu-id="e7725-127">Les formats de date suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="e7725-127">The following date formats are supported:</span></span>
- <span data-ttu-id="e7725-128">MM/j j/aaie</span><span class="sxs-lookup"><span data-stu-id="e7725-128">MM/dd/yyyy</span></span>
- <span data-ttu-id="e7725-129">dd/MM/yyyy</span><span class="sxs-lookup"><span data-stu-id="e7725-129">dd/MM/yyyy</span></span>

<span data-ttu-id="e7725-130">Les formats de date et d’heure suivants ne sont actuellement pas pris en charge :</span><span class="sxs-lookup"><span data-stu-id="e7725-130">The following date and time formats are currently not supported:</span></span>
- <span data-ttu-id="e7725-131">Date au format aaa/MM/j j/j/j j</span><span class="sxs-lookup"><span data-stu-id="e7725-131">Date format yyyy/MM/dd</span></span>
- <span data-ttu-id="e7725-132">Format de date j/MM/aa</span><span class="sxs-lookup"><span data-stu-id="e7725-132">Date format dd/MM/yy</span></span>
- <span data-ttu-id="e7725-133">Format de date avec aa.</span><span class="sxs-lookup"><span data-stu-id="e7725-133">Date format with yy.</span></span> <span data-ttu-id="e7725-134">Affiche uniquement yyyy.</span><span class="sxs-lookup"><span data-stu-id="e7725-134">Will only show yyyy.</span></span>
- <span data-ttu-id="e7725-135">Le format d’heure HH:mm:ss n’est pas pris en charge (le format 12 heures AM/PM n’est pas pris en charge).</span><span class="sxs-lookup"><span data-stu-id="e7725-135">Time format HH:mm:ss is not supported (the 12 hour AM/PM format is not supported).</span></span> <span data-ttu-id="e7725-136">Seul le format 24 heures est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e7725-136">Only the 24-hour format is supported.</span></span>

<span data-ttu-id="e7725-137">**Utilisation de virgule pour indiquer un millier**</span><span class="sxs-lookup"><span data-stu-id="e7725-137">**Use of comma to indicate thousand**</span></span><br>
<span data-ttu-id="e7725-138">La prise en charge de l’utilisation de la virgule comme séparateur dans les nombres n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e7725-138">Support of use of comma as a separator in numbers are not supported.</span></span> <span data-ttu-id="e7725-139">Les régions où un nombre est séparé par une virgule pour indiquer un millier ne voient que l’utilisation d’un point comme séparateur.</span><span class="sxs-lookup"><span data-stu-id="e7725-139">Regions where a number is separated with a comma to indicate a thousand, will only see the use of a dot as a separator.</span></span> <span data-ttu-id="e7725-140">Par exemple, 15 500 000 sont affichés en tant que 15,5 000.</span><span class="sxs-lookup"><span data-stu-id="e7725-140">For example, 15,5K is displayed as 15.5K.</span></span>

><span data-ttu-id="e7725-141">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="e7725-141">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="e7725-142">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="e7725-142">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-troubleshoot-belowfoldlink)

## <a name="microsoft-defender-for-endpoint-tenant-was-automatically-created-in-europe"></a><span data-ttu-id="e7725-143">Le client Microsoft Defender pour point de terminaison a été créé automatiquement en Europe</span><span class="sxs-lookup"><span data-stu-id="e7725-143">Microsoft Defender for Endpoint tenant was automatically created in Europe</span></span>
<span data-ttu-id="e7725-144">Lorsque vous utilisez le Centre de sécurité Azure pour surveiller les serveurs, un client Microsoft Defender pour point de terminaison est créé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="e7725-144">When you use Azure Security Center to monitor servers, a Microsoft Defender for Endpoint tenant is automatically created.</span></span> <span data-ttu-id="e7725-145">Les données de Microsoft Defender pour point de terminaison sont stockées en Europe par défaut.</span><span class="sxs-lookup"><span data-stu-id="e7725-145">The Microsoft Defender for Endpoint data is stored in Europe by default.</span></span>





## <a name="related-topics"></a><span data-ttu-id="e7725-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7725-146">Related topics</span></span>
- [<span data-ttu-id="e7725-147">Résoudre les problèmes d’intégration de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="e7725-147">Troubleshoot Microsoft Defender for Endpoint onboarding issues</span></span>](troubleshoot-onboarding.md)
- [<span data-ttu-id="e7725-148">Passer en revue les événements et les erreurs à l’aide de l’Observateur d’événements</span><span class="sxs-lookup"><span data-stu-id="e7725-148">Review events and errors using Event Viewer</span></span>](event-error-codes.md)
