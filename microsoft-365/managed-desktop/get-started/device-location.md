---
title: Service de localisation Windows 10
description: Comment faire pour que les services de localisation Windows sont allumés pour vos appareils
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
f1.keywords:
- NOCSH
ms.author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
manager: laurawi
ms.topic: article
audience: Admin
ms.openlocfilehash: 210356dd21b36efbb27d8faa4f8616145584159c
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50929500"
---
# <a name="windows-10-location-service"></a><span data-ttu-id="53b1a-104">Service de localisation Windows 10</span><span class="sxs-lookup"><span data-stu-id="53b1a-104">Windows 10 location service</span></span>

<span data-ttu-id="53b1a-105">Les appareils du Bureau géré Microsoft sont enregistrés à l’aide de Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="53b1a-105">Devices in Microsoft Managed Desktop are registered by using Windows Autopilot.</span></span> <span data-ttu-id="53b1a-106">Ce processus nous permet de les gérer avec Azure Active Directory et Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="53b1a-106">This process lets us manage them with Azure Active Directory and Microsoft Intune.</span></span> <span data-ttu-id="53b1a-107">Par défaut, le service d’emplacement De Windows 10 est désactivé lorsqu’un appareil est activé pour la première fois, sauf si cette fonctionnalité est activée dans les paramètres de confidentialité pendant l'« expérience d’out-of-box ».</span><span class="sxs-lookup"><span data-stu-id="53b1a-107">By default, the Windows 10 location service is disabled when a device is turned on for the first time unless this feature is enabled in the Privacy settings during the "out of box experience."</span></span> <span data-ttu-id="53b1a-108">Ces paramètres sont masqués lors de l’inscription Autopilot dans bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="53b1a-108">These settings are hidden during Autopilot enrollment in Microsoft Managed Desktop.</span></span> <span data-ttu-id="53b1a-109">Pour plus d’informations sur la façon dont Autopilot est installé, voir l’expérience de première expérience avec Autopilot et la page État de [l’inscription.](esp-first-run.md)</span><span class="sxs-lookup"><span data-stu-id="53b1a-109">For more information about how Autopilot is set up, see [First-run experience with Autopilot and the Enrollment Status Page](esp-first-run.md).</span></span>

<span data-ttu-id="53b1a-110">Pour cette raison, les appareils bureau géré Microsoft ne peuvent pas obtenir leur emplacement d’appareil, ce qui limite les fonctionnalités de plusieurs fonctionnalités Windows, telles que les fuseaux horaires.</span><span class="sxs-lookup"><span data-stu-id="53b1a-110">For this reason, Microsoft Managed Desktop devices can't obtain their device location, which limits the functionality of several Windows features, such as time zones.</span></span> <span data-ttu-id="53b1a-111">Pour plus d’informations sur le service d’emplacement Windows 10, voir [Service d’emplacement windows 10 et confidentialité.](https://support.microsoft.com/windows/windows-10-location-service-and-privacy-3a8eee0a-5b0b-dc07-eede-2a5ca1c49088)</span><span class="sxs-lookup"><span data-stu-id="53b1a-111">For more information about the Windows 10 location service, see [Windows 10 location service and privacy](https://support.microsoft.com/windows/windows-10-location-service-and-privacy-3a8eee0a-5b0b-dc07-eede-2a5ca1c49088).</span></span>

<span data-ttu-id="53b1a-112">Vous n’avez pas besoin d’utiliser le service de localisation pour participer au Bureau géré Microsoft, mais l’expérience utilisateur sera limitée.</span><span class="sxs-lookup"><span data-stu-id="53b1a-112">You don't have to use the location service in order to participate in Microsoft Managed Desktop, but the user experience will be restricted.</span></span> <span data-ttu-id="53b1a-113">Par exemple, les appareils ne seront pas en mesure de déterminer automatiquement le fuseau horaire dans le cas où vos utilisateurs travaillent dans un autre fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="53b1a-113">For example, devices won't be able to automatically determine the time zone they're in when your users work in a different time zone.</span></span>

## <a name="enable-the-location-service"></a><span data-ttu-id="53b1a-114">Activer le service de localisation</span><span class="sxs-lookup"><span data-stu-id="53b1a-114">Enable the location service</span></span>

<span data-ttu-id="53b1a-115">Vous pouvez choisir d’utiliser le service de localisation lorsque vous inscrivez des appareils dans le service Bureau géré Microsoft ou vous pouvez activer ou désactiver le service après l’inscription.</span><span class="sxs-lookup"><span data-stu-id="53b1a-115">You can either opt in to using the location service when you enroll devices into the Microsoft Managed Desktop service or you can turn the service on or off after enrollment.</span></span>

### <a name="opt-in-during-enrollment"></a><span data-ttu-id="53b1a-116">S’inscrire lors de l’inscription</span><span class="sxs-lookup"><span data-stu-id="53b1a-116">Opt in during enrollment</span></span>

<span data-ttu-id="53b1a-117">Le service Bureau géré Microsoft peut activer le service de localisation.</span><span class="sxs-lookup"><span data-stu-id="53b1a-117">You can have the Microsoft Managed Desktop service enable the location service.</span></span> <span data-ttu-id="53b1a-118">Au cours de la séquence d’inscription, vous serez invité à choisir si vous souhaitez activer le service d’emplacement Windows 10 sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="53b1a-118">During the enrollment sequence, you'll be asked to select whether you want to allow the Windows 10 location service to be enabled on devices.</span></span>

### <a name="control-the-location-service-after-enrollment"></a><span data-ttu-id="53b1a-119">Contrôler le service d’emplacement après l’inscription</span><span class="sxs-lookup"><span data-stu-id="53b1a-119">Control the location service after enrollment</span></span>

<span data-ttu-id="53b1a-120">Vous pouvez que le service d’emplacement soit allumé (ou désactivé) à tout moment en envoyant une demande de [support](../working-with-managed-desktop/admin-support.md) via le portail [d’administration.](access-admin-portal.md)</span><span class="sxs-lookup"><span data-stu-id="53b1a-120">You can have the location service turned on (or off) at any time by submitting a [support request](../working-with-managed-desktop/admin-support.md) through the [Admin portal](access-admin-portal.md).</span></span>

## <a name="how-microsoft-managed-desktop-configures-the-windows-10-location-service"></a><span data-ttu-id="53b1a-121">Comment Bureau géré Microsoft configure le service d’emplacement Windows 10</span><span class="sxs-lookup"><span data-stu-id="53b1a-121">How Microsoft Managed Desktop configures the Windows 10 location service</span></span>

<span data-ttu-id="53b1a-122">Si vous optez pour l’utilisation du service d’emplacement, nous utilisons les paramètres minimaux nécessaires sans affecter la confidentialité des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="53b1a-122">If you opt in to using the location service, we use the minimum settings necessary without affecting users' privacy.</span></span> <span data-ttu-id="53b1a-123">Pour plus d’informations, voir le service d’emplacement et la confidentialité [de Windows 10.](https://support.microsoft.com/windows/windows-10-location-service-and-privacy-3a8eee0a-5b0b-dc07-eede-2a5ca1c49088)</span><span class="sxs-lookup"><span data-stu-id="53b1a-123">For more information, see [Windows 10 location service and privacy](https://support.microsoft.com/windows/windows-10-location-service-and-privacy-3a8eee0a-5b0b-dc07-eede-2a5ca1c49088).</span></span>

<span data-ttu-id="53b1a-124">Bureau géré Microsoft active le paramètre de confidentialité **Emplacement** dans les **paramètres Windows** pour autoriser l’accès **à l’emplacement sur cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="53b1a-124">Microsoft Managed Desktop enables the **Location privacy** setting in **Windows settings** to **Allow access to location on this device**.</span></span> <span data-ttu-id="53b1a-125">L’interface utilisateur ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="53b1a-125">The user interface looks like this:</span></span>

 :::image type="content" source="../../media/MMD-location-services-UI.png" alt-text="Paramètres d’emplacement dans les paramètres Windows":::

> [!NOTE]
> <span data-ttu-id="53b1a-127">Si vous optez pour l’utilisation du service de localisation, cela s’applique uniquement au système d’exploitation Windows lui-même.</span><span class="sxs-lookup"><span data-stu-id="53b1a-127">If you opt in to using the location service, this applies only to the Windows operating system itself.</span></span> <span data-ttu-id="53b1a-128">Les applications ne sont pas autorisées à utiliser les services de localisation.</span><span class="sxs-lookup"><span data-stu-id="53b1a-128">Apps are not allowed to use location services.</span></span> <span data-ttu-id="53b1a-129">Chaque utilisateur peut choisir d’autoriser ou non les applications à accéder à leur emplacement.</span><span class="sxs-lookup"><span data-stu-id="53b1a-129">Each user can choose whether to allow apps to access their location.</span></span>