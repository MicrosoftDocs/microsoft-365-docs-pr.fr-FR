---
title: Redirection des comptes de Microsoft Defender pour le point de terminaison vers le Centre de sécurité Microsoft 365
description: Comment rediriger les comptes et les sessions du point de terminaison Defender vers le Centre de sécurité Microsoft 365.
keywords: Centre de sécurité Microsoft 365, Mise en place du Centre de sécurité Microsoft 365, redirection du Centre de sécurité
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
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: 626bc9950512438bfa43e6500adf72940ddcbfec
ms.sourcegitcommit: 3d48e198e706f22ac903b346cadda06b2368dd1e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/11/2021
ms.locfileid: "50727564"
---
# <a name="redirecting-accounts-from-microsoft-defender-for-endpoint-to-the-microsoft-365-security-center"></a><span data-ttu-id="a1917-104">Redirection des comptes de Microsoft Defender pour le point de terminaison vers le Centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a1917-104">Redirecting accounts from Microsoft Defender for Endpoint to the Microsoft 365 security center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

[!INCLUDE [Prerelease](../includes/prerelease.md)]

<span data-ttu-id="a1917-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a1917-105">**Applies to:**</span></span>
- <span data-ttu-id="a1917-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a1917-106">Microsoft 365 Defender</span></span>
- <span data-ttu-id="a1917-107">Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="a1917-107">Defender for Endpoint</span></span>

<span data-ttu-id="a1917-108">Dans l’alignement de l’approche multi-domaines de Microsoft en matière de protection contre les menaces avec LA DÉTECTION SIEM et la détection et réponse étendues (XDR), nous avons renommé Microsoft Defender – Protection avancée contre les menaces microsoft defender en Microsoft Defender pour point de terminaison et l’avons unifié en un portail intégré unique : le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a1917-108">In alignment with Microsoft’s cross-domain approach to threat protection with SIEM and Extended detection and response (XDR), we’ve rebranded Microsoft Defender Advanced Threat Protection as Microsoft Defender for Endpoint and unified it into a single integrated portal - the Microsoft 365 security center.</span></span>

<span data-ttu-id="a1917-109">Ce guide explique comment router les comptes vers le Centre de sécurité Microsoft 365 en activant la redirection automatique de l’ancien portail Microsoft Defender pour points de terminaison (securitycenter.windows.com ou securitycenter.microsoft.com) vers le portail du Centre de sécurité Microsoft 365 (security.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="a1917-109">This guide explains how to route accounts to the Microsoft 365 security center by enabling automatic redirection from the former Microsoft Defender for Endpoint portal (securitycenter.windows.com or securitycenter.microsoft.com), to the Microsoft 365 security center portal (security.microsoft.com).</span></span>

> [!NOTE]
> <span data-ttu-id="a1917-110">Microsoft Defender pour le point de terminaison dans le Centre de sécurité Microsoft 365 prend en charge l’octroi de l’accès aux fournisseurs de services de sécurité [gérés (MSSP)](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/grant-mssp-access) de la même façon que l’accès est accordé dans le Centre de sécurité [Microsoft Defender.](https://docs.microsoft.com/microsoft-365/security/mtp/mssp-access)</span><span class="sxs-lookup"><span data-stu-id="a1917-110">Microsoft Defender for Endpoint in the Microsoft 365 security center supports [granting access to managed security service providers (MSSPs)](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/grant-mssp-access) in the same that way access is [granted in the Microsoft Defender security center](https://docs.microsoft.com/microsoft-365/security/mtp/mssp-access).</span></span>

## <a name="what-to-expect"></a><span data-ttu-id="a1917-111">À quoi s’attendre</span><span class="sxs-lookup"><span data-stu-id="a1917-111">What to expect</span></span>
<span data-ttu-id="a1917-112">Une fois la redirection automatique activée, les comptes accédant à l’ancien portail Microsoft Defender for Endpoint sur securitycenter.windows.com ou securitycenter.microsoft.com sont automatiquement acheminés vers le portail du Centre de sécurité Microsoft 365 sur security.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="a1917-112">Once automatic redirection is enabled, accounts accessing the former Microsoft Defender for Endpoint portal at securitycenter.windows.com or securitycenter.microsoft.com, will be automatically routed to the Microsoft 365 security center portal at security.microsoft.com.</span></span>
 
<span data-ttu-id="a1917-113">En savoir plus sur ce qui a changé : Microsoft Defender pour point de terminaison dans le Centre de sécurité [Microsoft 365.](microsoft-365-security-center-mde.md)</span><span class="sxs-lookup"><span data-stu-id="a1917-113">Learn more about what’s changed: [Microsoft Defender for Endpoint in the Microsoft 365 security center](microsoft-365-security-center-mde.md).</span></span>

<span data-ttu-id="a1917-114">Cela inclut la redirection pour l’accès direct à l’ancien portail via le navigateur, y compris les liens pointant vers l’ancien portail securitycenter.windows.com, tels que les liens dans les notifications par courrier électronique et les liens renvoyés par les appels d’API SIEM.</span><span class="sxs-lookup"><span data-stu-id="a1917-114">This includes redirection for direct access to the former portal via browser, including links pointing towards the former securitycenter.windows.com portal - such as links in email notifications, and links returned by SIEM API calls.</span></span>  

 <span data-ttu-id="a1917-115">Les liens externes provenant de notifications par courrier électronique ou d’API SIEM contiennent actuellement des liens vers les deux portails.</span><span class="sxs-lookup"><span data-stu-id="a1917-115">External links from email notifications or SIEM APIs currently contain links to both portals.</span></span> <span data-ttu-id="a1917-116">Une fois la redirection activée, les deux liens pointent vers le Centre de sécurité Microsoft 365 jusqu’à ce que l’ancien lien soit finalement supprimé.</span><span class="sxs-lookup"><span data-stu-id="a1917-116">Once redirection is enabled, both links will point to the Microsoft 365 security center until the old link is eventually removed.</span></span> <span data-ttu-id="a1917-117">Nous vous encourageons à adopter le nouveau lien pointant vers le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a1917-117">We encourage you to adopt the new link pointing to the Microsoft 365 security center.</span></span>

<span data-ttu-id="a1917-118">Pour plus d’informations sur les liens et le routage, voir le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a1917-118">Refer to the table below for more on links and routing.</span></span>
## <a name="siem-api-routing"></a><span data-ttu-id="a1917-119">Routage de l’API SIEM</span><span class="sxs-lookup"><span data-stu-id="a1917-119">SIEM API routing</span></span>

|<span data-ttu-id="a1917-120">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="a1917-120">**Property**</span></span>  |<span data-ttu-id="a1917-121">**Destination lorsque la redirection est off**</span><span class="sxs-lookup"><span data-stu-id="a1917-121">**Destination when redirection is OFF**</span></span>  |<span data-ttu-id="a1917-122">**Destination lorsque la redirection est SUR**</span><span class="sxs-lookup"><span data-stu-id="a1917-122">**Destination when redirection is ON**</span></span> | 
|---------|---------|---------|
| <span data-ttu-id="a1917-123">LinkToWDATP</span><span class="sxs-lookup"><span data-stu-id="a1917-123">LinkToWDATP</span></span> | <span data-ttu-id="a1917-124">Page d’alerte dans securitycenter.windows.com</span><span class="sxs-lookup"><span data-stu-id="a1917-124">Alert page in securitycenter.windows.com</span></span> | <span data-ttu-id="a1917-125">Page d’alerte dans security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a1917-125">Alert page in security.microsoft.com</span></span>  |
| <span data-ttu-id="a1917-126">IncidentLinkToWDATP</span><span class="sxs-lookup"><span data-stu-id="a1917-126">IncidentLinkToWDATP</span></span> | <span data-ttu-id="a1917-127">Page Incident dans securitycenter.windows.com</span><span class="sxs-lookup"><span data-stu-id="a1917-127">Incident page in securitycenter.windows.com</span></span>  | <span data-ttu-id="a1917-128">Page Incident dans security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a1917-128">Incident page in security.microsoft.com</span></span>  |
| <span data-ttu-id="a1917-129">LinkToMTP</span><span class="sxs-lookup"><span data-stu-id="a1917-129">LinkToMTP</span></span> | <span data-ttu-id="a1917-130">Page d’alerte dans security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a1917-130">Alert page in security.microsoft.com</span></span> | <span data-ttu-id="a1917-131">Page d’alerte dans security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a1917-131">Alert page in security.microsoft.com</span></span>  |
| <span data-ttu-id="a1917-132">IncidentLinkToMTP</span><span class="sxs-lookup"><span data-stu-id="a1917-132">IncidentLinkToMTP</span></span> | <span data-ttu-id="a1917-133">Page Incident dans security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a1917-133">Incident page in security.microsoft.com</span></span>  | <span data-ttu-id="a1917-134">Page Incident dans security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a1917-134">Incident page in security.microsoft.com</span></span>  

## <a name="email-alert-notifications"></a><span data-ttu-id="a1917-135">Notifications d’alerte par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="a1917-135">Email alert notifications</span></span>

|<span data-ttu-id="a1917-136">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="a1917-136">**Property**</span></span>  |<span data-ttu-id="a1917-137">**Destination lorsque la redirection est off**</span><span class="sxs-lookup"><span data-stu-id="a1917-137">**Destination when redirection is OFF**</span></span>  |<span data-ttu-id="a1917-138">**Destination lorsque la redirection est SUR**</span><span class="sxs-lookup"><span data-stu-id="a1917-138">**Destination when redirection is ON**</span></span> |
|---------|---------|---------|
| <span data-ttu-id="a1917-139">Page d’alerte</span><span class="sxs-lookup"><span data-stu-id="a1917-139">Alert page</span></span>  | <span data-ttu-id="a1917-140">Page d’alerte dans securitycenter.windows.com</span><span class="sxs-lookup"><span data-stu-id="a1917-140">Alert page in securitycenter.windows.com</span></span>  | <span data-ttu-id="a1917-141">Page d’alerte dans security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a1917-141">Alert page in security.microsoft.com</span></span>  |
| <span data-ttu-id="a1917-142">Page Incident</span><span class="sxs-lookup"><span data-stu-id="a1917-142">Incident page</span></span>  |<span data-ttu-id="a1917-143">Page Incident dans securitycenter.windows.com</span><span class="sxs-lookup"><span data-stu-id="a1917-143">Incident page in securitycenter.windows.com</span></span>  | <span data-ttu-id="a1917-144">Page Incident dans security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a1917-144">Incident page in security.microsoft.com</span></span>  
| <span data-ttu-id="a1917-145">Page d’alerte dans le portail du centre de sécurité</span><span class="sxs-lookup"><span data-stu-id="a1917-145">Alert page in security center portal</span></span> | <span data-ttu-id="a1917-146">Page d’alerte dans security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a1917-146">Alert page in security.microsoft.com</span></span> | <span data-ttu-id="a1917-147">Page d’alerte dans security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a1917-147">Alert page in security.microsoft.com</span></span> | 
| <span data-ttu-id="a1917-148">Page Incident dans le portail centre de sécurité</span><span class="sxs-lookup"><span data-stu-id="a1917-148">Incident page in security center portal</span></span> | <span data-ttu-id="a1917-149">Page Incident dans security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a1917-149">Incident page in security.microsoft.com</span></span>  | <span data-ttu-id="a1917-150">Page Incident dans security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a1917-150">Incident page in security.microsoft.com</span></span>  |

## <a name="when-does-this-take-effect"></a><span data-ttu-id="a1917-151">Quand cela prend-il effet ?</span><span class="sxs-lookup"><span data-stu-id="a1917-151">When does this take effect?</span></span> 
<span data-ttu-id="a1917-152">Une fois activée, cette mise à jour peut prendre effet presque immédiatement pour certains comptes.</span><span class="sxs-lookup"><span data-stu-id="a1917-152">Once enabled, this update might take effect almost immediately for some accounts.</span></span> <span data-ttu-id="a1917-153">Toutefois, la propagation de la redirection vers chaque compte de votre organisation peut prendre plus de temps.</span><span class="sxs-lookup"><span data-stu-id="a1917-153">But the redirection might take longer to propagate to every account in your organization.</span></span> <span data-ttu-id="a1917-154">Les comptes dans les sessions actives pendant que ce paramètre est appliqué ne seront pas éjectés de leur session et seront acheminés uniquement vers le Centre de sécurité Microsoft 365 après avoir mis fin à leur session en cours et en se dénouant à nouveau.</span><span class="sxs-lookup"><span data-stu-id="a1917-154">Accounts in active sessions while this setting is applied will not be ejected from their session and will only be routed to the Microsoft 365 security center after ending their current session and signing back in again.</span></span>  

### <a name="set-up-portal-redirection"></a><span data-ttu-id="a1917-155">Configurer la redirection du portail</span><span class="sxs-lookup"><span data-stu-id="a1917-155">Set up portal redirection</span></span>
<span data-ttu-id="a1917-156">Pour démarrer le routage des comptes vers le Centre de sécurité Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="a1917-156">To start routing accounts to the Microsoft 365 security center:</span></span>
1. <span data-ttu-id="a1917-157">Assurez-vous que vous êtes un administrateur général ou que vous avez des autorisations d’administrateur de sécurité dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="a1917-157">Make sure you’re a global administrator or have security administrator permissions in Azure Active directory</span></span> 

2. <span data-ttu-id="a1917-158">[Connectez-vous](https://security.microsoft.com/) au Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a1917-158">[Sign in](https://security.microsoft.com/) to the Microsoft 365 security center.</span></span>

3. <span data-ttu-id="a1917-159">Accédez **à La redirection** du portail général des points de  >  **terminaison**  >    >   des paramètres [ou cliquez ici.](https://security.microsoft.com/preferences2/portal_redirection)</span><span class="sxs-lookup"><span data-stu-id="a1917-159">Navigate to **Settings** > **Endpoints** > **General** > **Portal redirection** or [click here](https://security.microsoft.com/preferences2/portal_redirection).</span></span>  

4. <span data-ttu-id="a1917-160">Basculez le paramètre de redirection automatique sur **Le**.</span><span class="sxs-lookup"><span data-stu-id="a1917-160">Toggle the Automatic redirection setting to **On**.</span></span>

5. <span data-ttu-id="a1917-161">Cliquez **sur Activer** pour appliquer la redirection automatique vers le portail du Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a1917-161">Click **Enable** to apply automatic redirection to the Microsoft 365 security center portal.</span></span>

>[!IMPORTANT]
><span data-ttu-id="a1917-162">L’activation de ce paramètre ne met pas fin aux sessions utilisateur actives.</span><span class="sxs-lookup"><span data-stu-id="a1917-162">Enabling this setting will not terminate active user sessions.</span></span> <span data-ttu-id="a1917-163">Les comptes qui sont dans une session active pendant que ce paramètre est appliqué sont dirigés uniquement vers le Centre de sécurité Microsoft 365 après avoir mis fin à leur session active et se sont à nouveau signés.</span><span class="sxs-lookup"><span data-stu-id="a1917-163">Accounts who are in an active session while this setting is applied will only be directed to the Microsoft 365 security center after ending their current session and signing in again.</span></span>

>[!NOTE]
><span data-ttu-id="a1917-164">Vous devez être administrateur général ou avoir des autorisations d’administrateur de sécurité dans Azure Active Directory pour activer ou désactiver ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="a1917-164">You must be a global administrator or have security administrator permissions in Azure Active Directory to enable or disable this setting.</span></span>  

## <a name="can-i-go-back-to-using-the-former-portal"></a><span data-ttu-id="a1917-165">Puis-je revenir à l’ancien portail ?</span><span class="sxs-lookup"><span data-stu-id="a1917-165">Can I go back to using the former portal?</span></span>
<span data-ttu-id="a1917-166">Si quelque chose ne fonctionne pas pour vous ou s’il y a quelque chose que vous ne pouvez pas effectuer via le portail du Centre de sécurité Microsoft 365, nous souhaitons en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="a1917-166">If something isn’t working for you or if there’s anything you’re unable to complete through the Microsoft 365 security center portal, we want to hear about it.</span></span> <span data-ttu-id="a1917-167">Si vous avez rencontré des problèmes avec la redirection, nous vous encourageons à nous le faire savoir à l’aide du formulaire d’envoi de commentaires.</span><span class="sxs-lookup"><span data-stu-id="a1917-167">If you’ve encountered any issues with redirection, we encourage you to let us know by using the Give feedback submission form.</span></span>

<span data-ttu-id="a1917-168">Pour revenir à l’ancien portail Microsoft Defender pour points de terminaison :</span><span class="sxs-lookup"><span data-stu-id="a1917-168">To revert to the former Microsoft Defender for Endpoint portal:</span></span>

1. <span data-ttu-id="a1917-169">[Connectez-vous](https://security.microsoft.com/) au Centre de sécurité Microsoft 365 en tant qu’administrateur général ou en utilisant et en utilisant des comptes avec des autorisations d’administrateur de sécurité dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a1917-169">[Sign in](https://security.microsoft.com/) to the Microsoft 365 security center as a global administrator or using and account with security administrator permissions in Azure Active directory.</span></span>

2. <span data-ttu-id="a1917-170">Accédez **à La redirection** du portail général des points de terminaison des  >  **paramètres** ou  >    >   [ouvrez la page ici.](https://security.microsoft.com/preferences2/portal_redirection)</span><span class="sxs-lookup"><span data-stu-id="a1917-170">Navigate to **Settings** > **Endpoints** > **General** > **Portal redirection** or [open the page here](https://security.microsoft.com/preferences2/portal_redirection).</span></span>  

3. <span data-ttu-id="a1917-171">Désaffectez le paramètre de redirection **automatique.**</span><span class="sxs-lookup"><span data-stu-id="a1917-171">Toggle the Automatic redirection setting to **Off**.</span></span>

4. <span data-ttu-id="a1917-172">Cliquez **sur Désactiver le** partage & commentaires lorsque vous y avez été invité.</span><span class="sxs-lookup"><span data-stu-id="a1917-172">Click **Disable** & share feedback when prompted.</span></span>

<span data-ttu-id="a1917-173">Ce paramètre peut être à nouveau activé à tout moment.</span><span class="sxs-lookup"><span data-stu-id="a1917-173">This setting can be enabled again at any time.</span></span> 

<span data-ttu-id="a1917-174">Une fois désactivés, les comptes ne seront plus acheminés vers security.microsoft.com, et vous aurez à nouveau accès à l’ancien portail : securitycenter.windows.com ou securitycenter.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="a1917-174">Once disabled, accounts will no longer be routed to security.microsoft.com, and you will once again have access to the former portal - securitycenter.windows.com or securitycenter.microsoft.com.</span></span> 

## <a name="related-information"></a><span data-ttu-id="a1917-175">Informations connexes</span><span class="sxs-lookup"><span data-stu-id="a1917-175">Related information</span></span>
- [<span data-ttu-id="a1917-176">Vue d’ensemble du Centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a1917-176">Microsoft 365 security center overview</span></span>](overview-security-center.md)
- [<span data-ttu-id="a1917-177">Microsoft Defender pour point de terminaison dans le Centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a1917-177">Microsoft Defender for Endpoint in the Microsoft 365 security center</span></span>](microsoft-365-security-center-mde.md)
- [<span data-ttu-id="a1917-178">Microsoft fournit un SIEM et XDR unifiés pour moderniser les opérations de sécurité</span><span class="sxs-lookup"><span data-stu-id="a1917-178">Microsoft delivers unified SIEM and XDR to modernize security operations</span></span>](https://www.microsoft.com/security/blog/?p=91813) 
- [<span data-ttu-id="a1917-179">Infographie XDR et SIEM</span><span class="sxs-lookup"><span data-stu-id="a1917-179">XDR versus SIEM infographic</span></span>](https://afrait.com/blog/xdr-versus-siem/) 
- [<span data-ttu-id="a1917-180">Nouveau defender</span><span class="sxs-lookup"><span data-stu-id="a1917-180">The New Defender</span></span>](https://afrait.com/blog/the-new-defender/) 
- [<span data-ttu-id="a1917-181">À propos de Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a1917-181">About Microsoft 365 Defender</span></span>](https://www.microsoft.com/microsoft-365/security/microsoft-365-defender) 
- [<span data-ttu-id="a1917-182">Portails de sécurité Microsoft et centres d’administration</span><span class="sxs-lookup"><span data-stu-id="a1917-182">Microsoft security portals and admin centers</span></span>](portals.md)
