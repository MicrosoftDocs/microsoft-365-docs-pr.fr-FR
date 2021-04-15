---
title: Activer la fonctionnalité d'analyse périodique limitée de l'Antivirus Microsoft Defender
description: L'analyse périodique limitée vous permet d'utiliser l'Antivirus Microsoft Defender en plus de vos autres fournisseurs antivirus installés.
keywords: lps, limité, périodique, analyse, analyse, compatibilité, tiers, autre antivirus, désactiver
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 09/03/2018
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: 82c4bc1feec1556dc864558a843ed5e911c3ef3d
ms.sourcegitcommit: 7a339c9f7039825d131b39481ddf54c57b021b11
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "51764482"
---
# <a name="use-limited-periodic-scanning-in-microsoft-defender-antivirus"></a><span data-ttu-id="0e8ee-104">Utiliser une analyse périodique limitée dans l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="0e8ee-104">Use limited periodic scanning in Microsoft Defender Antivirus</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="0e8ee-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="0e8ee-105">**Applies to:**</span></span>

- [<span data-ttu-id="0e8ee-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="0e8ee-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="0e8ee-107">L'analyse périodique limitée est un type spécial de détection et de correction des menaces qui peut être activé lorsque vous avez installé un autre produit antivirus sur un appareil Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0e8ee-107">Limited periodic scanning is a special type of threat detection and remediation that can be enabled when you have installed another antivirus product on a Windows 10 device.</span></span>

<span data-ttu-id="0e8ee-108">Il ne peut être activé que dans certaines situations.</span><span class="sxs-lookup"><span data-stu-id="0e8ee-108">It can only be enabled in certain situations.</span></span> <span data-ttu-id="0e8ee-109">Pour plus d'informations sur l'analyse périodique limitée et le fonctionnement de l'Antivirus Microsoft Defender avec d'autres produits antivirus, voir Compatibilité de [l'Antivirus Microsoft Defender.](microsoft-defender-antivirus-compatibility.md)</span><span class="sxs-lookup"><span data-stu-id="0e8ee-109">For more information about limited periodic scanning and how Microsoft Defender Antivirus works with other antivirus products, see [Microsoft Defender Antivirus compatibility](microsoft-defender-antivirus-compatibility.md).</span></span>

<span data-ttu-id="0e8ee-110">**Microsoft ne recommande pas l'utilisation de cette fonctionnalité dans les environnements d'entreprise. Il s'agit d'une fonctionnalité principalement destinée aux consommateurs.**</span><span class="sxs-lookup"><span data-stu-id="0e8ee-110">**Microsoft does not recommend using this feature in enterprise environments. This is a feature primarily intended for consumers.**</span></span> <span data-ttu-id="0e8ee-111">Cette fonctionnalité utilise uniquement un sous-ensemble limité des fonctionnalités de l'Antivirus Microsoft Defender pour détecter les programmes malveillants et ne peut pas détecter la plupart des programmes malveillants et des logiciels potentiellement indésirables.</span><span class="sxs-lookup"><span data-stu-id="0e8ee-111">This feature only uses a limited subset of the Microsoft Defender Antivirus capabilities to detect malware, and will not be able to detect most malware and potentially unwanted software.</span></span> <span data-ttu-id="0e8ee-112">En outre, les fonctionnalités de gestion et de rapport seront limitées.</span><span class="sxs-lookup"><span data-stu-id="0e8ee-112">Also, management and reporting capabilities will be limited.</span></span> <span data-ttu-id="0e8ee-113">Microsoft recommande aux entreprises de choisir leur solution antivirus principale et de l'utiliser exclusivement.</span><span class="sxs-lookup"><span data-stu-id="0e8ee-113">Microsoft recommends enterprises choose their primary antivirus solution and use it exclusively.</span></span>

## <a name="how-to-enable-limited-periodic-scanning"></a><span data-ttu-id="0e8ee-114">Comment activer l'analyse périodique limitée</span><span class="sxs-lookup"><span data-stu-id="0e8ee-114">How to enable limited periodic scanning</span></span>

<span data-ttu-id="0e8ee-115">Par défaut, l'Antivirus Microsoft Defender s'active sur un appareil Windows 10 si aucun autre produit antivirus n'est installé, ou si l'autre produit est périmé, expiré ou ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="0e8ee-115">By default, Microsoft Defender Antivirus will enable itself on a Windows 10 device if there is no other antivirus product installed, or if the other product is out-of-date, expired, or not working correctly.</span></span>

<span data-ttu-id="0e8ee-116">Si l'Antivirus Microsoft Defender est activé, les options habituelles s'affichent pour le configurer sur cet appareil :</span><span class="sxs-lookup"><span data-stu-id="0e8ee-116">If Microsoft Defender Antivirus is enabled, the usual options will appear to configure it on that device:</span></span>

![Application sécurité Windows affichant les options de Microsoft Defender AV, y compris les options d'analyse, les paramètres et les options de mise à jour](images/vtp-wdav.png)

<span data-ttu-id="0e8ee-118">Si un autre produit antivirus est installé et fonctionne correctement, l'Antivirus Microsoft Defender se désactive lui-même.</span><span class="sxs-lookup"><span data-stu-id="0e8ee-118">If another antivirus product is installed and working correctly, Microsoft Defender Antivirus will disable itself.</span></span> <span data-ttu-id="0e8ee-119">L'application Sécurité Windows modifie la section Protection contre les virus **&** contre les menaces pour afficher l'état du produit antivirus et fournit un lien vers les options de configuration du produit.</span><span class="sxs-lookup"><span data-stu-id="0e8ee-119">The Windows Security app will change the **Virus & threat protection** section to show status about the AV product, and provide a link to the product's configuration options.</span></span>

<span data-ttu-id="0e8ee-120">Sous les produits antivirus tiers, un nouveau lien s'affiche en tant qu'options de **l'Antivirus Microsoft Defender.**</span><span class="sxs-lookup"><span data-stu-id="0e8ee-120">Underneath any third party AV products, a new link will appear as **Microsoft Defender Antivirus options**.</span></span> <span data-ttu-id="0e8ee-121">Cliquez sur ce lien pour afficher le bouton bascule qui permet une analyse périodique limitée.</span><span class="sxs-lookup"><span data-stu-id="0e8ee-121">Clicking this link will expand to show the toggle that enables limited periodic scanning.</span></span> <span data-ttu-id="0e8ee-122">Notez que l'option périodique limitée est un basculement permettant d'activer ou de désactiver l'analyse périodique.</span><span class="sxs-lookup"><span data-stu-id="0e8ee-122">Note that the limited periodic option is a toggle to enable or disable periodic scanning.</span></span> 

<span data-ttu-id="0e8ee-123">Le fait de faire glisser le commutateur sur **On** affiche les options standard de l'Antivirus Microsoft Defender sous le produit antivirus tiers.</span><span class="sxs-lookup"><span data-stu-id="0e8ee-123">Sliding the switch to **On** will show the standard Microsoft Defender AV options underneath the third party AV product.</span></span> <span data-ttu-id="0e8ee-124">L'option d'analyse périodique limitée s'affiche en bas de la page.</span><span class="sxs-lookup"><span data-stu-id="0e8ee-124">The limited periodic scanning option will appear at the bottom of the page.</span></span>

## <a name="related-articles"></a><span data-ttu-id="0e8ee-125">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="0e8ee-125">Related articles</span></span>

- [<span data-ttu-id="0e8ee-126">Configurer la protection comportementale, heuristique et en temps réel</span><span class="sxs-lookup"><span data-stu-id="0e8ee-126">Configure behavioral, heuristic, and real-time protection</span></span>](configure-protection-features-microsoft-defender-antivirus.md)
- [<span data-ttu-id="0e8ee-127">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="0e8ee-127">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)