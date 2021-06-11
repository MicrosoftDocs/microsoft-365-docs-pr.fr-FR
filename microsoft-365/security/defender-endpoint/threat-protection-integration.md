---
title: Intégrer Microsoft Defender for Endpoint à d’autres solutions Microsoft
description: Découvrez comment Microsoft Defender pour endpoint s’intègre à d’autres solutions Microsoft, notamment Microsoft Defender pour l’identité et Azure Defender.
author: mjcaparas
ms.author: macapara
ms.prod: m365-security
keywords: microsoft 365 defender, accès conditionnel, office, Microsoft Defender pour le point de terminaison, microsoft defender pour l’identité, microsoft defender pour office, Azure Defender, microsoft cloud app security, azure sentinel
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 8973a78787345532055161507e2d30f75b3b2cf1
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52844969"
---
# <a name="microsoft-defender-for-endpoint-and-other-microsoft-solutions"></a><span data-ttu-id="a914d-104">Microsoft Defender pour le point de terminaison et d’autres solutions Microsoft</span><span class="sxs-lookup"><span data-stu-id="a914d-104">Microsoft Defender for Endpoint and other Microsoft solutions</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="a914d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a914d-105">**Applies to:**</span></span>
- [<span data-ttu-id="a914d-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="a914d-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="a914d-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a914d-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="a914d-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="a914d-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="a914d-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="a914d-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

## <a name="integrate-with-other-microsoft-solutions"></a><span data-ttu-id="a914d-110">Intégration à d’autres solutions Microsoft</span><span class="sxs-lookup"><span data-stu-id="a914d-110">Integrate with other Microsoft solutions</span></span>

<span data-ttu-id="a914d-111">Microsoft Defender pour le point de terminaison s’intègre directement à différentes solutions Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a914d-111">Microsoft Defender for Endpoint directly integrates with various Microsoft solutions.</span></span>

### <a name="azure-defender"></a><span data-ttu-id="a914d-112">Azure Defender</span><span class="sxs-lookup"><span data-stu-id="a914d-112">Azure Defender</span></span>
<span data-ttu-id="a914d-113">Microsoft Defender pour le point de terminaison fournit une solution de protection serveur complète, notamment des fonctionnalités protection évolutive des points de terminaison (PEPT) sur Windows serveurs.</span><span class="sxs-lookup"><span data-stu-id="a914d-113">Microsoft Defender for Endpoint provides a comprehensive server protection solution, including endpoint detection and response (EDR) capabilities on Windows Servers.</span></span>

### <a name="azure-sentinel"></a><span data-ttu-id="a914d-114">Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="a914d-114">Azure Sentinel</span></span>
<span data-ttu-id="a914d-115">Le connecteur Microsoft Defender pour point de terminaison vous permet de diffuser des alertes à partir de Microsoft Defender pour Endpoint dans Azure Sentinel.</span><span class="sxs-lookup"><span data-stu-id="a914d-115">The Microsoft Defender for Endpoint connector lets you stream alerts from Microsoft Defender for Endpoint into Azure Sentinel.</span></span> <span data-ttu-id="a914d-116">Cela vous permettra d’analyser plus en détail les événements de sécurité au sein de votre organisation et de créer des manuels pour obtenir une réponse efficace et immédiate.</span><span class="sxs-lookup"><span data-stu-id="a914d-116">This will enable you to more comprehensively analyze security events across your organization and build playbooks for effective and immediate response.</span></span>

### <a name="azure-information-protection"></a><span data-ttu-id="a914d-117">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="a914d-117">Azure Information Protection</span></span>
<span data-ttu-id="a914d-118">Nous avons récemment supprimé l’intégration Azure Information Protection, car nos fonctionnalités DLP de point de terminaison intègrent une solution de découverte et de protection améliorée pour les données sensibles stockées sur les appareils de point de terminaison, ce qui facilite la visibilité et l’intégration entre les solutions.</span><span class="sxs-lookup"><span data-stu-id="a914d-118">We recently deprecated the Azure Information Protection integration as our Endpoint DLP capabilities incorporate an improved discovery and protection solution for sensitive data stored on endpoint devices that facilitates greater visibility and integration between solutions.</span></span> <span data-ttu-id="a914d-119">Cela a été annoncé dans le [blog suivant.](https://techcommunity.microsoft.com/t5/microsoft-defender-for-endpoint/protecting-sensitive-information-on-devices/ba-p/2143555)</span><span class="sxs-lookup"><span data-stu-id="a914d-119">This was announced in the following [blog](https://techcommunity.microsoft.com/t5/microsoft-defender-for-endpoint/protecting-sensitive-information-on-devices/ba-p/2143555).</span></span> <span data-ttu-id="a914d-120">Nous recommandons aux clients de passer à l’utilisation du point de terminaison DLP.</span><span class="sxs-lookup"><span data-stu-id="a914d-120">We recommend that customers move to using Endpoint DLP.</span></span>

### <a name="conditional-access"></a><span data-ttu-id="a914d-121">Accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="a914d-121">Conditional Access</span></span>
<span data-ttu-id="a914d-122">Le score de risque de l’appareil dynamique de Microsoft Defender pour le point de terminaison est intégré à l’évaluation de l’accès conditionnel, garantissant que seuls les appareils sécurisés ont accès aux ressources.</span><span class="sxs-lookup"><span data-stu-id="a914d-122">Microsoft Defender for Endpoint's dynamic device risk score is integrated into the Conditional Access evaluation, ensuring that only secure devices have access to resources.</span></span> 

### <a name="microsoft-cloud-app-security"></a><span data-ttu-id="a914d-123">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="a914d-123">Microsoft Cloud App Security</span></span>
<span data-ttu-id="a914d-124">Microsoft Cloud App Security utilise les signaux de point de terminaison Microsoft Defender pour les points de terminaison pour permettre une visibilité directe de l’utilisation des applications cloud, y compris l’utilisation de services cloud non pris en compte (shadow IT) de tous les appareils surveillés par Microsoft Defender pour Endpoint.</span><span class="sxs-lookup"><span data-stu-id="a914d-124">Microsoft Cloud App Security leverages Microsoft Defender for Endpoint endpoint signals to allow direct visibility into cloud application usage including the use of unsupported cloud services (shadow IT) from all Microsoft Defender for Endpoint monitored devices.</span></span>

### <a name="microsoft-defender-for-identity"></a><span data-ttu-id="a914d-125">Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="a914d-125">Microsoft Defender for Identity</span></span>
<span data-ttu-id="a914d-126">Les activités suspectes sont des processus en cours d’exécution dans un contexte utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a914d-126">Suspicious activities are processes running under a user context.</span></span> <span data-ttu-id="a914d-127">L’intégration entre Microsoft Defender pour point de terminaison et Microsoft Defender pour l’identité offre la flexibilité nécessaire pour mener des enquêtes sur la cybersécurité entre les activités et les identités.</span><span class="sxs-lookup"><span data-stu-id="a914d-127">The integration between Microsoft Defender for Endpoint and Microsoft Defender for Identity provides the flexibility of conducting cyber security investigation across activities and identities.</span></span>

### <a name="microsoft-defender-for-office"></a><span data-ttu-id="a914d-128">Microsoft Defender pour Office</span><span class="sxs-lookup"><span data-stu-id="a914d-128">Microsoft Defender for Office</span></span>
<span data-ttu-id="a914d-129">[Defender for Office 365](/office365/securitycompliance/office-365-atp) permet de protéger votre organisation contre les programmes malveillants dans les messages électroniques ou les fichiers par le biais de liens sécurisés, de pièces jointes sécurisées, d’anti-hameçonnage avancé et de fonctionnalités d’intelligence contre l’usurpation d’adresses.</span><span class="sxs-lookup"><span data-stu-id="a914d-129">[Defender for Office 365](/office365/securitycompliance/office-365-atp) helps protect your organization from malware in email messages or files through Safe Links, Safe Attachments, advanced Anti-Phishing, and spoof intelligence capabilities.</span></span> <span data-ttu-id="a914d-130">L’intégration entre Microsoft Defender pour Office 365 et Microsoft Defender pour le point de terminaison permet aux analystes de sécurité de monter en amont pour examiner le point d’entrée d’une attaque.</span><span class="sxs-lookup"><span data-stu-id="a914d-130">The integration between Microsoft Defender for Office 365 and Microsoft Defender for Endpoint enables security analysts to go upstream to investigate the entry point of an attack.</span></span> <span data-ttu-id="a914d-131">Grâce au partage des renseignements sur les menaces, les attaques peuvent être contenues et bloquées.</span><span class="sxs-lookup"><span data-stu-id="a914d-131">Through threat intelligence sharing, attacks can be contained and blocked.</span></span> 

>[!NOTE]
> <span data-ttu-id="a914d-132">Defender pour Office 365 données de sécurité est affiché pour les événements des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="a914d-132">Defender for Office 365 data is displayed for events within the last 30 days.</span></span> <span data-ttu-id="a914d-133">Pour les alertes, defender pour Office 365 données s’affiche en fonction de la première activité.</span><span class="sxs-lookup"><span data-stu-id="a914d-133">For alerts, Defender for Office 365 data is displayed based on first activity time.</span></span> <span data-ttu-id="a914d-134">Ensuite, les données ne sont plus disponibles dans Defender pour les Office 365.</span><span class="sxs-lookup"><span data-stu-id="a914d-134">After that, the data is no longer available in Defender for Office 365.</span></span>

### <a name="skype-for-business"></a><span data-ttu-id="a914d-135">Skype Entreprise</span><span class="sxs-lookup"><span data-stu-id="a914d-135">Skype for Business</span></span>
<span data-ttu-id="a914d-136">L’intégration Skype Entreprise’analyse permet aux analystes de communiquer avec un utilisateur ou un propriétaire d’appareil potentiellement compromis par le biais d’un bouton simple à partir du portail.</span><span class="sxs-lookup"><span data-stu-id="a914d-136">The Skype for Business integration provides a way for analysts to communicate with a potentially compromised user or device owner through a simple button from the portal.</span></span>

## <a name="microsoft-365-defender"></a><span data-ttu-id="a914d-137">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a914d-137">Microsoft 365 Defender</span></span>
<span data-ttu-id="a914d-138">Avec Microsoft 365 Defender, Microsoft Defender pour point de terminaison et diverses solutions de sécurité Microsoft constituent une suite de défense d’entreprise unifiée avant et après la violation qui s’intègre en mode natif à travers le point de terminaison, l’identité, le courrier électronique et les applications pour détecter, empêcher, examiner et répondre automatiquement aux attaques sophistiquées.</span><span class="sxs-lookup"><span data-stu-id="a914d-138">With Microsoft 365 Defender, Microsoft Defender for Endpoint and various Microsoft security solutions form a unified pre- and post-breach enterprise defense suite that natively integrates across endpoint, identity, email, and applications to detect, prevent, investigate and automatically respond to sophisticated attacks.</span></span> 
 
[<span data-ttu-id="a914d-139">En savoir plus sur Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a914d-139">Learn more about Microsoft 365 Defender</span></span>](/microsoft-365/security/defender/microsoft-threat-protection)


## <a name="related-topics"></a><span data-ttu-id="a914d-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a914d-140">Related topics</span></span>
- [<span data-ttu-id="a914d-141">Configurer l’intégration et d’autres fonctionnalités avancées</span><span class="sxs-lookup"><span data-stu-id="a914d-141">Configure integration and other advanced features</span></span>](advanced-features.md)
- [<span data-ttu-id="a914d-142">Microsoft 365 Vue d’ensemble de Defender</span><span class="sxs-lookup"><span data-stu-id="a914d-142">Microsoft 365 Defender overview</span></span>](/microsoft-365/security/defender/microsoft-threat-protection)
- [<span data-ttu-id="a914d-143">Activer Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a914d-143">Turn on Microsoft 365 Defender</span></span>](/microsoft-365/security/defender/mtp-enable)
- [<span data-ttu-id="a914d-144">Protéger les utilisateurs, les données et les appareils avec l’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="a914d-144">Protect users, data, and devices with Conditional Access</span></span>](conditional-access.md)
