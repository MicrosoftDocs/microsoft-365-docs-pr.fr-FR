---
title: Résoudre les problèmes d’intégration et les messages d’erreur
description: Résoudre les problèmes d’intégration et le message d’erreur lors de la configuration de Microsoft Defender pour le point de terminaison.
keywords: résolution des problèmes, dépannage, Azure Active Directory, intégration, message d’erreur, messages d’erreur, microsoft defender pour le point de terminaison
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
ms.openlocfilehash: 63981d985140858cbbda54a10dc94b30f28131e5
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51064854"
---
# <a name="troubleshoot-subscription-and-portal-access-issues"></a><span data-ttu-id="1f3b2-104">Résoudre les problèmes d’abonnement et d’accès au portail</span><span class="sxs-lookup"><span data-stu-id="1f3b2-104">Troubleshoot subscription and portal access issues</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="1f3b2-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="1f3b2-105">**Applies to:**</span></span>
- [<span data-ttu-id="1f3b2-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1f3b2-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="1f3b2-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1f3b2-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="1f3b2-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="1f3b2-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="1f3b2-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="1f3b2-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-troublshootonboarding-abovefoldlink)

<span data-ttu-id="1f3b2-110">Cette page fournit des étapes détaillées pour résoudre les problèmes qui peuvent se produire lors de la configuration de votre service Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="1f3b2-110">This page provides detailed steps to troubleshoot issues that might occur when setting up your Microsoft Defender for Endpoint service.</span></span>

<span data-ttu-id="1f3b2-111">Si vous recevez un message d’erreur, le Centre de sécurité Microsoft Defender fournit une explication détaillée du problème et des liens pertinents sont fournis.</span><span class="sxs-lookup"><span data-stu-id="1f3b2-111">If you receive an error message, Microsoft Defender Security Center will provide a detailed explanation on what the issue is and relevant links will be supplied.</span></span>

## <a name="no-subscriptions-found"></a><span data-ttu-id="1f3b2-112">Aucun abonnement trouvé</span><span class="sxs-lookup"><span data-stu-id="1f3b2-112">No subscriptions found</span></span>

<span data-ttu-id="1f3b2-113">Si, lors de l’accès au Centre de sécurité Microsoft Defender, vous obtenez un **message** aucun abonnement trouvé, cela signifie que l’Azure Active Directory (Azure AD) utilisé pour se connecter à l’utilisateur sur le portail n’a pas de licence Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1f3b2-113">If while accessing Microsoft Defender Security Center you get a **No subscriptions found** message, it means the Azure Active Directory (Azure AD) used to log in the user to the portal, does not have a Microsoft Defender for Endpoint license.</span></span>

<span data-ttu-id="1f3b2-114">Raisons potentielles :</span><span class="sxs-lookup"><span data-stu-id="1f3b2-114">Potential reasons:</span></span>
- <span data-ttu-id="1f3b2-115">Les licences Windows E5 et Office E5 sont distinctes.</span><span class="sxs-lookup"><span data-stu-id="1f3b2-115">The Windows E5 and Office E5 licenses are separate licenses.</span></span>
- <span data-ttu-id="1f3b2-116">La licence a été achetée, mais elle n’a pas été mise en service pour cette instance Azure AD.</span><span class="sxs-lookup"><span data-stu-id="1f3b2-116">The license was purchased but not provisioned to this Azure AD instance.</span></span>
    - <span data-ttu-id="1f3b2-117">Il peut s’agit d’un problème de mise en service de licence.</span><span class="sxs-lookup"><span data-stu-id="1f3b2-117">It could be a license provisioning issue.</span></span>
    - <span data-ttu-id="1f3b2-118">Il se peut que vous avez mis en service par inadvertance la licence sur un microsoft Azure AD différent de celui utilisé pour l’authentification dans le service.</span><span class="sxs-lookup"><span data-stu-id="1f3b2-118">It could be you inadvertently provisioned the license to a different Microsoft Azure AD than the one used for authentication into the service.</span></span>

<span data-ttu-id="1f3b2-119">Dans les deux cas, vous devez contacter le support Microsoft à l’aide du support [général de Microsoft Defender pour](https://support.microsoft.com/getsupport?wf=0&tenant=ClassicCommercial&oaspworkflow=start_1.0.0.0&locale=en-us&supportregion=en-us&pesid=16055&ccsid=636419533611396913) les points de terminaison ou du support de licence en [volume.](https://www.microsoft.com/licensing/servicecenter/Help/Contact.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f3b2-119">For both cases, you should contact Microsoft support at [General Microsoft Defender for Endpoint Support](https://support.microsoft.com/getsupport?wf=0&tenant=ClassicCommercial&oaspworkflow=start_1.0.0.0&locale=en-us&supportregion=en-us&pesid=16055&ccsid=636419533611396913) or [Volume license support](https://www.microsoft.com/licensing/servicecenter/Help/Contact.aspx).</span></span>

![Image d’aucun abonnement trouvé](images/atp-no-subscriptions-found.png)

## <a name="your-subscription-has-expired"></a><span data-ttu-id="1f3b2-121">Votre abonnement a expiré</span><span class="sxs-lookup"><span data-stu-id="1f3b2-121">Your subscription has expired</span></span>

<span data-ttu-id="1f3b2-122">Si, lors de l’accès au Centre de sécurité Microsoft Defender, vous obtenez un **message** votre abonnement a expiré, votre abonnement de service en ligne a expiré.</span><span class="sxs-lookup"><span data-stu-id="1f3b2-122">If while accessing Microsoft Defender Security Center you get a **Your subscription has expired** message, your online service subscription has expired.</span></span> <span data-ttu-id="1f3b2-123">L’abonnement Microsoft Defender pour les points de terminaison, comme tout autre abonnement de service en ligne, a une date d’expiration.</span><span class="sxs-lookup"><span data-stu-id="1f3b2-123">Microsoft Defender for Endpoint subscription, like any other online service subscription, has an expiration date.</span></span> 

<span data-ttu-id="1f3b2-124">Vous pouvez choisir de renouveler ou de prolonger la licence à tout moment.</span><span class="sxs-lookup"><span data-stu-id="1f3b2-124">You can choose to renew or extend the license at any point in time.</span></span> <span data-ttu-id="1f3b2-125">Lorsque vous accédez au portail après la date d’expiration, un **message** votre abonnement a expiré se présente avec une option pour télécharger le package de la sortie de l’appareil, si vous choisissez de ne pas renouveler la licence.</span><span class="sxs-lookup"><span data-stu-id="1f3b2-125">When accessing the portal after the expiration date a **Your subscription has expired** message will be presented with an option to download the device offboarding package, should you choose to not renew the license.</span></span>

> [!NOTE]
> <span data-ttu-id="1f3b2-126">Pour des raisons de sécurité, le package utilisé pour la sortie des appareils expirera 30 jours après la date de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="1f3b2-126">For security reasons, the package used to Offboard devices will expire 30 days after the date it was downloaded.</span></span> <span data-ttu-id="1f3b2-127">Les packages de offboarding expirés envoyés à un appareil seront rejetés.</span><span class="sxs-lookup"><span data-stu-id="1f3b2-127">Expired offboarding packages sent to a device will be rejected.</span></span> <span data-ttu-id="1f3b2-128">Lorsque vous téléchargez un package de déclassage, vous êtes informé de la date d’expiration des packages et il est également inclus dans le nom du package.</span><span class="sxs-lookup"><span data-stu-id="1f3b2-128">When downloading an offboarding package you will be notified of the packages expiry date and it will also be included in the package name.</span></span>

![Image de l’abonnement expiré](images/atp-subscription-expired.png)

## <a name="you-are-not-authorized-to-access-the-portal"></a><span data-ttu-id="1f3b2-130">Vous n’êtes pas autorisé à accéder au portail</span><span class="sxs-lookup"><span data-stu-id="1f3b2-130">You are not authorized to access the portal</span></span>

<span data-ttu-id="1f3b2-131">Si vous recevez une demande Vous n’êtes pas autorisé à accéder au **portail,** sachez que Microsoft Defender pour le point de terminaison est un produit de surveillance de la sécurité, d’examen des incidents et de réponse. En tant que tel, l’accès à celui-ci est restreint et contrôlé par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1f3b2-131">If you receive a **You are not authorized to access the portal**, be aware that Microsoft Defender for Endpoint is a security monitoring, incident investigation and response product, and as such, access to it is restricted and controlled by the user.</span></span>
<span data-ttu-id="1f3b2-132">Pour plus d’informations, voir [**Attribuer un accès utilisateur au portail.**](https://docs.microsoft.com/windows/threat-protection/windows-defender-atp/assign-portal-access-windows-defender-advanced-threat-protection)</span><span class="sxs-lookup"><span data-stu-id="1f3b2-132">For more information, see, [**Assign user access to the portal**](https://docs.microsoft.com/windows/threat-protection/windows-defender-atp/assign-portal-access-windows-defender-advanced-threat-protection).</span></span>

![Image d’un portail non autorisé à accéder](images/atp-not-authorized-to-access-portal.png)

## <a name="data-currently-isnt-available-on-some-sections-of-the-portal"></a><span data-ttu-id="1f3b2-134">Les données ne sont actuellement pas disponibles sur certaines sections du portail</span><span class="sxs-lookup"><span data-stu-id="1f3b2-134">Data currently isn't available on some sections of the portal</span></span>
<span data-ttu-id="1f3b2-135">Si le tableau de bord du portail et d’autres sections indiquent un message d’erreur tel que « Les données ne sont actuellement pas disponibles » :</span><span class="sxs-lookup"><span data-stu-id="1f3b2-135">If the portal dashboard and other sections show an error message such as "Data currently isn't available":</span></span>

![Image des données actuellement non disponible](images/atp-data-not-available.png)

<span data-ttu-id="1f3b2-137">Vous devez autoriser le sous-domaine et tous ses `securitycenter.windows.com` sous-domaine.</span><span class="sxs-lookup"><span data-stu-id="1f3b2-137">You'll need to allow the `securitycenter.windows.com` and all subdomains under it.</span></span> <span data-ttu-id="1f3b2-138">Par exemple, `*.securitycenter.windows.com`.</span><span class="sxs-lookup"><span data-stu-id="1f3b2-138">For example, `*.securitycenter.windows.com`.</span></span>


## <a name="portal-communication-issues"></a><span data-ttu-id="1f3b2-139">Problèmes de communication du portail</span><span class="sxs-lookup"><span data-stu-id="1f3b2-139">Portal communication issues</span></span>
<span data-ttu-id="1f3b2-140">Si vous rencontrez des problèmes d’accès au portail, de données manquantes ou d’accès restreint à certaines parties du portail, vous devez vérifier que les URL suivantes sont autorisées et ouvertes pour la communication.</span><span class="sxs-lookup"><span data-stu-id="1f3b2-140">If you encounter issues with accessing the portal, missing data, or restricted access to portions of the portal, you'll need to verify that the following URLs are allowed and open for communication.</span></span>

- `*.blob.core.windows.net`
- `crl.microsoft.com`
- `https://*.microsoftonline-p.com`
- `https://*.securitycenter.windows.com` 
- `https://automatediracs-eus-prd.securitycenter.windows.com`
- `https://login.microsoftonline.com`
- `https://login.windows.net`
- `https://onboardingpackagescusprd.blob.core.windows.net`
- `https://secure.aadcdn.microsoftonline-p.com` 
- `https://securitycenter.windows.com` 
- `https://static2.sharepointonline.com` 



