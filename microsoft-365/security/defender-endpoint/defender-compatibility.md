---
title: Compatibilité de l'Antivirus Microsoft Defender avec Defender pour le point de terminaison
description: Découvrez comment Windows Defender fonctionne avec Microsoft Defender pour Endpoint et comment il fonctionne lorsqu'un client anti-programme malveillant tiers est utilisé.
keywords: compatibilité de windows defender, defender, Microsoft Defender pour le point de terminaison, defender pour le point de terminaison, antivirus, mde
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
ms.topic: conceptual
ms.date: 04/24/2018
ms.technology: mde
ms.openlocfilehash: a8dca4a80385fabcdc64a5584474214d05be4a6c
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51935376"
---
# <a name="microsoft-defender-antivirus-compatibility-with-microsoft-defender-for-endpoint"></a><span data-ttu-id="5d752-104">Compatibilité de l'Antivirus Microsoft Defender avec Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="5d752-104">Microsoft Defender Antivirus compatibility with Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="5d752-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="5d752-105">**Applies to:**</span></span>
- [<span data-ttu-id="5d752-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="5d752-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="5d752-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="5d752-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


><span data-ttu-id="5d752-108">Vous souhaitez faire l'expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="5d752-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="5d752-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="5d752-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-defendercompat-abovefoldlink)

<span data-ttu-id="5d752-110">L'agent Microsoft Defender pour endpoint dépend de l'Antivirus Microsoft Defender pour certaines fonctionnalités telles que l'analyse de fichiers.</span><span class="sxs-lookup"><span data-stu-id="5d752-110">The Microsoft Defender for Endpoint agent depends on Microsoft Defender Antivirus for some capabilities such as file scanning.</span></span>

>[!IMPORTANT]
><span data-ttu-id="5d752-111">Defender pour le point de terminaison ne respecte pas les paramètres d'exclusions de l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="5d752-111">Defender for Endpoint does not adhere to the Microsoft Defender Antivirus Exclusions settings.</span></span> 

<span data-ttu-id="5d752-112">Vous devez configurer les mises à jour d'intelligence de sécurité sur les appareils Defender for Endpoint, que l'Antivirus Microsoft Defender soit ou non le logiciel anti-programme malveillant actif.</span><span class="sxs-lookup"><span data-stu-id="5d752-112">You must configure Security intelligence updates on the Defender for Endpoint devices whether Microsoft Defender Antivirus is the active antimalware or not.</span></span> <span data-ttu-id="5d752-113">Pour plus d'informations, voir Gérer les mises à [jour de l'Antivirus Microsoft Defender et appliquer les lignes de base.](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/manage-updates-baselines-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="5d752-113">For more information, see [Manage Microsoft Defender Antivirus updates and apply baselines](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/manage-updates-baselines-microsoft-defender-antivirus.md).</span></span>

<span data-ttu-id="5d752-114">Si un appareil intégré est protégé par un client tiers anti-programme malveillant, l'Antivirus Microsoft Defender sur ce point de terminaison passe en mode passif.</span><span class="sxs-lookup"><span data-stu-id="5d752-114">If an onboarded device is protected by a third-party antimalware client, Microsoft Defender Antivirus on that endpoint will enter into passive mode.</span></span>

<span data-ttu-id="5d752-115">L'Antivirus Microsoft Defender continue de recevoir des mises à jour et le processus *mspeng.exe* est répertorié comme un service en cours d'exécution, mais il n'effectue pas d'analyses et ne remplace pas le client anti-programme malveillant tiers en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="5d752-115">Microsoft Defender Antivirus will continue to receive updates, and the *mspeng.exe* process will be listed as a running a service, but it will not perform scans and will not replace the running third-party antimalware client.</span></span>

<span data-ttu-id="5d752-116">L'interface antivirus Microsoft Defender sera désactivée et les utilisateurs de l'appareil ne pourront pas utiliser l'Antivirus Microsoft Defender pour effectuer des analyses à la demande ou configurer la plupart des options.</span><span class="sxs-lookup"><span data-stu-id="5d752-116">The Microsoft Defender Antivirus interface will be disabled, and users on the device will not be able to use Microsoft Defender Antivirus to perform on-demand scans or configure most options.</span></span>

<span data-ttu-id="5d752-117">Pour plus d'informations, consultez la rubrique sur la compatibilité entre [l'Antivirus Microsoft Defender](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/microsoft-defender-antivirus-compatibility)et Defender pour endpoint.</span><span class="sxs-lookup"><span data-stu-id="5d752-117">For more information, see the [Microsoft Defender Antivirus and Defender for Endpoint compatibility topic](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/microsoft-defender-antivirus-compatibility).</span></span>
