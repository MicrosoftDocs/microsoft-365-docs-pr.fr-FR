---
title: Redirection des comptes de Microsoft Defender Office 365 vers le nouveau centre Microsoft 365 sécurité
description: Comment rediriger de Defender vers Office 365 centre de sécurité Microsoft 365 de sécurité.
keywords: Microsoft 365 de sécurité, mise en Microsoft 365 centre de sécurité, redirection du centre de sécurité
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: 40d86f9f3a4896bbe788f0a9894a7e08efe3a690
ms.sourcegitcommit: 58d74ff60303a879e35d112f10f79724ba41188f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "52301727"
---
# <a name="redirecting-accounts-from-microsoft-defender-for-office-365-to-the-microsoft-365-security-center"></a><span data-ttu-id="d604d-104">Redirection des comptes de Microsoft Defender Office 365 vers le centre Microsoft 365 de sécurité microsoft</span><span class="sxs-lookup"><span data-stu-id="d604d-104">Redirecting accounts from Microsoft Defender for Office 365 to the Microsoft 365 security center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="d604d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d604d-105">**Applies to:**</span></span>

- <span data-ttu-id="d604d-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d604d-106">Microsoft 365 Defender</span></span>
- <span data-ttu-id="d604d-107">Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="d604d-107">Defender for Office 365</span></span>

<span data-ttu-id="d604d-108">Cet article explique comment router les comptes vers le centre de sécurité Microsoft 365 en activant la redirection automatique de l’ancien Centre de sécurité et conformité Microsoft (protection.office.com ou securitycenter.microsoft.com) vers le Centre de sécurité Microsoft 365 (security.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="d604d-108">This article explains how to route accounts to the Microsoft 365 security center by enabling automatic redirection from the former Microsoft Security and Compliance Center (protection.office.com or securitycenter.microsoft.com), to the Microsoft 365 security center (security.microsoft.com).</span></span>

## <a name="what-to-expect"></a><span data-ttu-id="d604d-109">À quoi s’attendre</span><span class="sxs-lookup"><span data-stu-id="d604d-109">What to expect</span></span>
<span data-ttu-id="d604d-110">Une fois la redirection automatique activée et active, les utilisateurs accédant aux fonctionnalités liées à la sécurité dans Office 365 Security and Compliance (protection.office.com) sont automatiquement acheminés vers le centre de sécurité Microsoft 365 ( https://security.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="d604d-110">Once automatic redirection is enabled and active, users accessing the security-related capabilities in  Office 365 Security and Compliance (protection.office.com), will be automatically routed to the Microsoft 365 security center (https://security.microsoft.com).</span></span>  

<span data-ttu-id="d604d-111">En savoir plus sur ce qui a changé [: Microsoft Defender pour Office 365 dans le centre Microsoft 365 de sécurité.](microsoft-365-security-center-mdo.md)</span><span class="sxs-lookup"><span data-stu-id="d604d-111">Learn more about what’s changed: [Microsoft Defender for Office 365 in the Microsoft 365 security center](microsoft-365-security-center-mdo.md).</span></span>

<span data-ttu-id="d604d-112">Lorsque la redirection automatique est désactivée, les utilisateurs sont acheminés vers le centre de sécurité Microsoft 365 lorsqu’ils utilisent les fonctionnalités de sécurité du Centre de sécurité et de conformité Office 365.</span><span class="sxs-lookup"><span data-stu-id="d604d-112">With automatic redirection turned on, users will be routed to Microsoft 365 security center when they use security capabilities in the Office 365 Security and Compliance Center.</span></span>

<span data-ttu-id="d604d-113">Il s’agit notamment des fonctionnalités de la section Gestion des menaces, du tableau de bord et des rapports de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="d604d-113">These include capabilities in the Threat Management section and the Threat Management dashboard and reports.</span></span> <span data-ttu-id="d604d-114">Les éléments du Centre Office 365 sécurité et conformité qui ne sont pas liés à la sécurité ne sont pas redirigés vers le centre Microsoft 365 sécurité.</span><span class="sxs-lookup"><span data-stu-id="d604d-114">Items in the Office 365 Security and Compliance Center that are not related to security are not redirected to the Microsoft 365 security center.</span></span>

<span data-ttu-id="d604d-115">Les éléments liés à la conformité se trouvent dans le centre Microsoft 365 conformité, et les éléments liés au flux de messagerie se trouvent dans le centre d Exchange’administration.</span><span class="sxs-lookup"><span data-stu-id="d604d-115">Compliance-related items can be found in the Microsoft 365 compliance center, and mail-flow related items can be found in the Exchange admin center.</span></span>

<span data-ttu-id="d604d-116">Toutes les autres fonctionnalités, que ce soit liées à la conformité ou aux fonctionnalités qui servent les deux ne sont pas affectées par la redirection.</span><span class="sxs-lookup"><span data-stu-id="d604d-116">All other capabilities, whether compliance-related or capabilities that serve both are not affected by redirection.</span></span> <span data-ttu-id="d604d-117">Office 365 alertes de sécurité s’affichent à la fois dans le centre de sécurité Microsoft 365 et dans le centre Office 365 sécurité et conformité, sans redirection.</span><span class="sxs-lookup"><span data-stu-id="d604d-117">Office 365 security alerts appear in both the Microsoft 365 security center and the Office 365 Security and Compliance center, without redirection.</span></span>  

### <a name="set-up-portal-redirection"></a><span data-ttu-id="d604d-118">Configurer la redirection du portail</span><span class="sxs-lookup"><span data-stu-id="d604d-118">Set up portal redirection</span></span>
<span data-ttu-id="d604d-119">Pour démarrer le routage des comptes vers le centre de sécurité Microsoft 365 à l’security.microsoft.com :</span><span class="sxs-lookup"><span data-stu-id="d604d-119">To start routing accounts to the Microsoft 365 security center at security.microsoft.com:</span></span>

1. <span data-ttu-id="d604d-120">Assurez-vous que vous êtes un administrateur général ou que vous avez des autorisations d’administrateur de sécurité dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d604d-120">Make sure you’re a global administrator or have security administrator permissions in Azure Active directory.</span></span>
2. <span data-ttu-id="d604d-121">[Connectez-vous](https://security.microsoft.com/) au centre Microsoft 365 sécurité.</span><span class="sxs-lookup"><span data-stu-id="d604d-121">[Sign in](https://security.microsoft.com/) to the Microsoft 365 security center.</span></span>
3. <span data-ttu-id="d604d-122">Accédez à **Paramètres**  >  **courrier électronique &**  >  **redirection du portail de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="d604d-122">Navigate to **Settings** > **Email & collaboration** > **Portal redirection**.</span></span>  
4. <span data-ttu-id="d604d-123">Basculez le paramètre de redirection automatique sur **Le**.</span><span class="sxs-lookup"><span data-stu-id="d604d-123">Toggle the Automatic redirection setting to **On**.</span></span>
5. <span data-ttu-id="d604d-124">Cliquez **sur Activer** pour appliquer la redirection automatique au portail Microsoft 365 centre de sécurité.</span><span class="sxs-lookup"><span data-stu-id="d604d-124">Click **Enable** to apply automatic redirection to the Microsoft 365 security center portal.</span></span>

> [!NOTE]
> <span data-ttu-id="d604d-125">Une fois la redirection activée, les comptes dans les sessions actives pendant que ce paramètre est appliqué ne sont pas éjectés de leur session et sont acheminés uniquement vers le centre de sécurité Microsoft 365 après avoir mis fin à leur session en cours et se sont de nouveau ré-signés.</span><span class="sxs-lookup"><span data-stu-id="d604d-125">After redirection is enabled, accounts in active sessions while this setting is applied will not be ejected from their session and will only be routed to the Microsoft 365 security center after ending their current session and signing back in again.</span></span>

## <a name="can-i-go-back-to-using-the-former-portal"></a><span data-ttu-id="d604d-126">Puis-je revenir à l’ancien portail ?</span><span class="sxs-lookup"><span data-stu-id="d604d-126">Can I go back to using the former portal?</span></span>
<span data-ttu-id="d604d-127">Si quelque chose ne fonctionne pas pour vous ou s’il y a quelque chose que vous ne pouvez pas effectuer via le portail du centre de sécurité Microsoft 365, nous souhaitons en savoir plus à ce sujet à l’aide de l’option de commentaires du portail.</span><span class="sxs-lookup"><span data-stu-id="d604d-127">If something isn’t working for you or if there’s anything you’re unable to complete through the Microsoft 365 security center portal, we want to hear about it using the portal feedback option.</span></span> <span data-ttu-id="d604d-128">Si vous avez rencontré des problèmes de redirection, nous vous encourageons à contacter votre pm directement via la prévisualisation privée ou faites-le nous savoir via le formulaire d’envoi de commentaires.</span><span class="sxs-lookup"><span data-stu-id="d604d-128">If you’ve encountered any issues with redirection, we encourage you to reach out to your PM buddy directly through private preview or let us know via the Give feedback submission form.</span></span>

<span data-ttu-id="d604d-129">Pour revenir à l’ancien portail :</span><span class="sxs-lookup"><span data-stu-id="d604d-129">To revert to the former portal:</span></span>

1. <span data-ttu-id="d604d-130">[Connectez-vous](https://security.microsoft.com/) au centre de sécurité Microsoft 365 en tant qu’administrateur général ou en utilisant et compte avec des autorisations d’administrateur de sécurité dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d604d-130">[Sign in](https://security.microsoft.com/) to the Microsoft 365 security center as a global administrator or using and account with security administrator permissions in Azure Active directory.</span></span>

2. <span data-ttu-id="d604d-131">Accédez à **Paramètres**  >  **redirection du** portail général des  >    >  **points de terminaison.**</span><span class="sxs-lookup"><span data-stu-id="d604d-131">Navigate to **Settings** > **Endpoints** > **General** > **Portal redirection**.</span></span>  

3. <span data-ttu-id="d604d-132">Basculez le paramètre de redirection automatique sur **Désintégation.**</span><span class="sxs-lookup"><span data-stu-id="d604d-132">Toggle the Automatic redirection setting to **Off**.</span></span>

4. <span data-ttu-id="d604d-133">Cliquez **sur Désactiver le** partage & commentaires lorsque vous y avez été invité.</span><span class="sxs-lookup"><span data-stu-id="d604d-133">Click **Disable** & share feedback when prompted.</span></span>

<span data-ttu-id="d604d-134">Ce paramètre peut être à nouveau activé à tout moment.</span><span class="sxs-lookup"><span data-stu-id="d604d-134">This setting can be enabled again at any time.</span></span>

<span data-ttu-id="d604d-135">Une fois désactivés, les comptes ne seront plus acheminés vers security.microsoft.com, et vous aurez à nouveau accès à l’ancien portail ( securitycenter.windows.com ou securitycenter.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="d604d-135">Once disabled, accounts will no longer be routed to security.microsoft.com, and you will once again have access to the former portal - securitycenter.windows.com or securitycenter.microsoft.com.</span></span>

## <a name="related-information"></a><span data-ttu-id="d604d-136">Informations connexes</span><span class="sxs-lookup"><span data-stu-id="d604d-136">Related information</span></span>
- [<span data-ttu-id="d604d-137">Vue d’ensemble du Centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="d604d-137">Microsoft 365 security center overview</span></span>](overview-security-center.md)
- [<span data-ttu-id="d604d-138">Microsoft Defender pour le point de terminaison dans le centre Microsoft 365 sécurité</span><span class="sxs-lookup"><span data-stu-id="d604d-138">Microsoft Defender for Endpoint in the Microsoft 365 security center</span></span>](microsoft-365-security-center-mde.md)
- [<span data-ttu-id="d604d-139">Microsoft fournit un SIEM et XDR unifiés pour moderniser les opérations de sécurité</span><span class="sxs-lookup"><span data-stu-id="d604d-139">Microsoft delivers unified SIEM and XDR to modernize security operations</span></span>](https://www.microsoft.com/security/blog/?p=91813) 
- [<span data-ttu-id="d604d-140">Infographie XDR et SIEM</span><span class="sxs-lookup"><span data-stu-id="d604d-140">XDR versus SIEM infographic</span></span>](https://afrait.com/blog/xdr-versus-siem/) 
- [<span data-ttu-id="d604d-141">Nouveau defender</span><span class="sxs-lookup"><span data-stu-id="d604d-141">The New Defender</span></span>](https://afrait.com/blog/the-new-defender/) 
- [<span data-ttu-id="d604d-142">À propos Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d604d-142">About Microsoft 365 Defender</span></span>](https://www.microsoft.com/microsoft-365/security/microsoft-365-defender) 
- [<span data-ttu-id="d604d-143">Portails de sécurité Microsoft et centres d’administration</span><span class="sxs-lookup"><span data-stu-id="d604d-143">Microsoft security portals and admin centers</span></span>](portals.md)
