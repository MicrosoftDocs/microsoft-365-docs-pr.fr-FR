---
title: Redirection des comptes de Microsoft Defender pour Office 365 vers le nouveau Centre de sécurité Microsoft 365
description: Comment rediriger de Defender pour Office 365 vers le Centre de sécurité Microsoft 365.
keywords: Centre de sécurité Microsoft 365, Mise en place du Centre de sécurité Microsoft 365, redirection du centre de sécurité
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
ms.openlocfilehash: ce8c178b4c46a00b83833f008080b776f4dc7e60
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51064641"
---
# <a name="redirecting-accounts-from-microsoft-defender-for-office-365-to-the-microsoft-365-security-center"></a><span data-ttu-id="b163e-104">Redirection des comptes de Microsoft Defender pour Office 365 vers le Centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b163e-104">Redirecting accounts from Microsoft Defender for Office 365 to the Microsoft 365 security center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="b163e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b163e-105">**Applies to:**</span></span>

- <span data-ttu-id="b163e-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b163e-106">Microsoft 365 Defender</span></span>
- <span data-ttu-id="b163e-107">Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="b163e-107">Defender for Office 365</span></span>

<span data-ttu-id="b163e-108">Cet article explique comment router les comptes vers le Centre de sécurité Microsoft 365 en activant la redirection automatique de l’ancien Centre de sécurité et conformité Microsoft (protection.office.com ou securitycenter.microsoft.com) vers le Centre de sécurité Microsoft 365 (security.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="b163e-108">This article explains how to route accounts to the Microsoft 365 security center by enabling automatic redirection from the former Microsoft Security and Compliance Center (protection.office.com or securitycenter.microsoft.com), to the Microsoft 365 security center (security.microsoft.com).</span></span>

>[!NOTE]
> <span data-ttu-id="b163e-109">La fonctionnalité de redirection de portail est disponible uniquement pour les clients Office 365 E5 et Microsoft Defender pour Office P2.</span><span class="sxs-lookup"><span data-stu-id="b163e-109">Portal redirection capability is available for Office 365 E5 and Microsoft Defender for Office P2 customers only</span></span>

## <a name="what-to-expect"></a><span data-ttu-id="b163e-110">À quoi s’attendre</span><span class="sxs-lookup"><span data-stu-id="b163e-110">What to expect</span></span>
<span data-ttu-id="b163e-111">Une fois la redirection automatique activée et active, les utilisateurs accédant aux fonctionnalités liées à la sécurité dans Office 365 Security and Compliance (protection.office.com) sont automatiquement acheminés vers le Centre de sécurité Microsoft 365 ( https://security.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="b163e-111">Once automatic redirection is enabled and active, users accessing the security-related capabilities in  Office 365 Security and Compliance (protection.office.com), will be automatically routed to the Microsoft 365 security center (https://security.microsoft.com).</span></span>  

<span data-ttu-id="b163e-112">En savoir plus sur ce qui a changé : Microsoft Defender pour Office 365 dans le Centre de sécurité [Microsoft 365.](microsoft-365-security-center-mdo.md)</span><span class="sxs-lookup"><span data-stu-id="b163e-112">Learn more about what’s changed: [Microsoft Defender for Office 365 in the Microsoft 365 security center](microsoft-365-security-center-mdo.md).</span></span>

<span data-ttu-id="b163e-113">Lorsque la redirection automatique est désactivée, les utilisateurs sont acheminés vers le Centre de sécurité Microsoft 365 lorsqu’ils utilisent les fonctionnalités de sécurité du Centre de sécurité et conformité Office 365.</span><span class="sxs-lookup"><span data-stu-id="b163e-113">With automatic redirection turned on, users will be routed to Microsoft 365 security center when they use security capabilities in the Office 365 Security and Compliance Center.</span></span>

<span data-ttu-id="b163e-114">Il s’agit notamment des fonctionnalités de la section Gestion des menaces, du tableau de bord et des rapports de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="b163e-114">These include capabilities in the Threat Management section and the Threat Management dashboard and reports.</span></span> <span data-ttu-id="b163e-115">Les éléments du Centre de sécurité et conformité Office 365 qui ne sont pas liés à la sécurité ne sont pas redirigés vers le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b163e-115">Items in the Office 365 Security and Compliance Center that are not related to security are not redirected to the Microsoft 365 security center.</span></span>

<span data-ttu-id="b163e-116">Les éléments liés à la conformité se trouvent dans le Centre de conformité Microsoft 365, et les éléments liés au flux de messagerie se trouvent dans le Centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="b163e-116">Compliance-related items can be found in the Microsoft 365 compliance center, and mail-flow related items can be found in the Exchange admin center.</span></span>

<span data-ttu-id="b163e-117">Toutes les autres fonctionnalités, que ce soit liées à la conformité ou aux fonctionnalités qui servent les deux ne sont pas affectées par la redirection.</span><span class="sxs-lookup"><span data-stu-id="b163e-117">All other capabilities, whether compliance-related or capabilities that serve both are not affected by redirection.</span></span> <span data-ttu-id="b163e-118">Les alertes de sécurité Office 365 apparaissent dans le Centre de sécurité Microsoft 365 et le Centre de sécurité et conformité Office 365, sans redirection.</span><span class="sxs-lookup"><span data-stu-id="b163e-118">Office 365 security alerts appear in both the Microsoft 365 security center and the Office 365 Security and Compliance center, without redirection.</span></span>  

### <a name="set-up-portal-redirection"></a><span data-ttu-id="b163e-119">Configurer la redirection du portail</span><span class="sxs-lookup"><span data-stu-id="b163e-119">Set up portal redirection</span></span>
<span data-ttu-id="b163e-120">Pour démarrer le routage des comptes vers le Centre de sécurité Microsoft 365, security.microsoft.com :</span><span class="sxs-lookup"><span data-stu-id="b163e-120">To start routing accounts to the Microsoft 365 security center at security.microsoft.com:</span></span>

1. <span data-ttu-id="b163e-121">Assurez-vous que vous êtes un administrateur général ou que vous avez des autorisations d’administrateur de sécurité dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b163e-121">Make sure you’re a global administrator or have security administrator permissions in Azure Active directory.</span></span>
2. <span data-ttu-id="b163e-122">[Connectez-vous](https://security.microsoft.com/) au Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b163e-122">[Sign in](https://security.microsoft.com/) to the Microsoft 365 security center.</span></span>
3. <span data-ttu-id="b163e-123">Accédez à **Paramètres**  >  **E-mail &**  >  **redirection du portail de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="b163e-123">Navigate to **Settings** > **Email & collaboration** > **Portal redirection**.</span></span>  
4. <span data-ttu-id="b163e-124">Basculez le paramètre de redirection automatique sur **Sur**.</span><span class="sxs-lookup"><span data-stu-id="b163e-124">Toggle the Automatic redirection setting to **On**.</span></span>
5. <span data-ttu-id="b163e-125">Cliquez **sur Activer** pour appliquer la redirection automatique vers le portail du Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b163e-125">Click **Enable** to apply automatic redirection to the Microsoft 365 security center portal.</span></span>

> [!NOTE]
> <span data-ttu-id="b163e-126">Une fois la redirection activée, les comptes dans les sessions actives pendant que ce paramètre est appliqué ne sont pas éjectés de leur session et sont acheminés uniquement vers le Centre de sécurité Microsoft 365 après avoir mis fin à leur session active et se sont de nouveau ré-signés.</span><span class="sxs-lookup"><span data-stu-id="b163e-126">After redirection is enabled, accounts in active sessions while this setting is applied will not be ejected from their session and will only be routed to the Microsoft 365 security center after ending their current session and signing back in again.</span></span>

## <a name="can-i-go-back-to-using-the-former-portal"></a><span data-ttu-id="b163e-127">Puis-je revenir à l’ancien portail ?</span><span class="sxs-lookup"><span data-stu-id="b163e-127">Can I go back to using the former portal?</span></span>
<span data-ttu-id="b163e-128">Si quelque chose ne fonctionne pas pour vous ou s’il y a quelque chose que vous ne parvenez pas à effectuer via le portail du Centre de sécurité Microsoft 365, nous souhaitons en savoir plus à ce sujet à l’aide de l’option de commentaires du portail.</span><span class="sxs-lookup"><span data-stu-id="b163e-128">If something isn’t working for you or if there’s anything you’re unable to complete through the Microsoft 365 security center portal, we want to hear about it using the portal feedback option.</span></span> <span data-ttu-id="b163e-129">Si vous avez rencontré des problèmes de redirection, nous vous encourageons à contacter votre pm directement via la prévisualisation privée ou faites-le nous savoir via le formulaire d’envoi de commentaires.</span><span class="sxs-lookup"><span data-stu-id="b163e-129">If you’ve encountered any issues with redirection, we encourage you to reach out to your PM buddy directly through private preview or let us know via the Give feedback submission form.</span></span>

<span data-ttu-id="b163e-130">Pour revenir à l’ancien portail :</span><span class="sxs-lookup"><span data-stu-id="b163e-130">To revert to the former portal:</span></span>

1. <span data-ttu-id="b163e-131">[Connectez-vous](https://security.microsoft.com/) au Centre de sécurité Microsoft 365 en tant qu’administrateur général ou en utilisant et en utilisant des comptes avec des autorisations d’administrateur de sécurité dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b163e-131">[Sign in](https://security.microsoft.com/) to the Microsoft 365 security center as a global administrator or using and account with security administrator permissions in Azure Active directory.</span></span>

2. <span data-ttu-id="b163e-132">Accédez **à La redirection** du portail général  >  **des points de**  >    >  **terminaison des paramètres.**</span><span class="sxs-lookup"><span data-stu-id="b163e-132">Navigate to **Settings** > **Endpoints** > **General** > **Portal redirection**.</span></span>  

3. <span data-ttu-id="b163e-133">Désaffectez le paramètre de redirection **automatique.**</span><span class="sxs-lookup"><span data-stu-id="b163e-133">Toggle the Automatic redirection setting to **Off**.</span></span>

4. <span data-ttu-id="b163e-134">Cliquez **sur Désactiver le** partage & commentaires lorsque vous y avez été invité.</span><span class="sxs-lookup"><span data-stu-id="b163e-134">Click **Disable** & share feedback when prompted.</span></span>

<span data-ttu-id="b163e-135">Ce paramètre peut être à nouveau activé à tout moment.</span><span class="sxs-lookup"><span data-stu-id="b163e-135">This setting can be enabled again at any time.</span></span>

<span data-ttu-id="b163e-136">Une fois désactivés, les comptes ne seront plus acheminés vers security.microsoft.com, et vous aurez à nouveau accès à l’ancien portail ( securitycenter.windows.com ou securitycenter.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="b163e-136">Once disabled, accounts will no longer be routed to security.microsoft.com, and you will once again have access to the former portal - securitycenter.windows.com or securitycenter.microsoft.com.</span></span>

## <a name="related-information"></a><span data-ttu-id="b163e-137">Informations connexes</span><span class="sxs-lookup"><span data-stu-id="b163e-137">Related information</span></span>
- [<span data-ttu-id="b163e-138">Vue d’ensemble du Centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b163e-138">Microsoft 365 security center overview</span></span>](overview-security-center.md)
- [<span data-ttu-id="b163e-139">Microsoft Defender pour le point de terminaison dans le Centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b163e-139">Microsoft Defender for Endpoint in the Microsoft 365 security center</span></span>](microsoft-365-security-center-mde.md)
- [<span data-ttu-id="b163e-140">Microsoft fournit un SIEM et XDR unifiés pour moderniser les opérations de sécurité</span><span class="sxs-lookup"><span data-stu-id="b163e-140">Microsoft delivers unified SIEM and XDR to modernize security operations</span></span>](https://www.microsoft.com/security/blog/?p=91813) 
- [<span data-ttu-id="b163e-141">Infographie XDR et SIEM</span><span class="sxs-lookup"><span data-stu-id="b163e-141">XDR versus SIEM infographic</span></span>](https://afrait.com/blog/xdr-versus-siem/) 
- [<span data-ttu-id="b163e-142">Le nouveau defender</span><span class="sxs-lookup"><span data-stu-id="b163e-142">The New Defender</span></span>](https://afrait.com/blog/the-new-defender/) 
- [<span data-ttu-id="b163e-143">À propos de Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b163e-143">About Microsoft 365 Defender</span></span>](https://www.microsoft.com/microsoft-365/security/microsoft-365-defender) 
- [<span data-ttu-id="b163e-144">Portails de sécurité Microsoft et centres d’administration</span><span class="sxs-lookup"><span data-stu-id="b163e-144">Microsoft security portals and admin centers</span></span>](portals.md)