---
title: Informations de base de l’Explorateur de menaces et des détections en temps réel dans Microsoft Defender Office 365
f1.keywords:
- NOCSH
ms.author: dansimp
author: MSFTTracyp
manager: dansimp
audience: ITPro
ms.topic: article
ms.date: 05/05/2021
localization_priority: Normal
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
description: Utilisez les détections de l’Explorateur ou en temps réel pour examiner les menaces et y répondre efficacement.
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 4d0a9ba7ee40c8ad97df745a20d6b5b3314bb3d8
ms.sourcegitcommit: cd55fe6abe25b1e4f5fbe8295d3a99aebd97ce66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53083187"
---
# <a name="explorer-and-real-time-detections-basics"></a><span data-ttu-id="e0a55-103">Informations de base sur les détections en temps réel et de l’Explorateur</span><span class="sxs-lookup"><span data-stu-id="e0a55-103">Explorer and Real-time detections basics</span></span>

<span data-ttu-id="e0a55-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="e0a55-104">**Applies to**</span></span>
- [<span data-ttu-id="e0a55-105">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="e0a55-105">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="e0a55-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e0a55-106">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="e0a55-107">Contenu de cet article :</span><span class="sxs-lookup"><span data-stu-id="e0a55-107">In this article:</span></span>

- [<span data-ttu-id="e0a55-108">Différences entre les détections de l’Explorateur et en temps réel</span><span class="sxs-lookup"><span data-stu-id="e0a55-108">Differences between Explorer and Real-time detections</span></span>](#differences-between-explorer-and-real-time-detections)
- [<span data-ttu-id="e0a55-109">Licences et autorisations requises</span><span class="sxs-lookup"><span data-stu-id="e0a55-109">Required licenses and permissions</span></span>](#required-licenses-and-permissions)

> [!NOTE]
> <span data-ttu-id="e0a55-110">Cela fait partie d’une série de **3 articles** sur l’Explorateur (également connu sous le nom d’Explorateur de **menaces),** la sécurité du courrier électronique et les bases de détection en temps réel et de l’Explorateur **(telles** que les différences entre les outils et les autorisations nécessaires pour les utiliser).</span><span class="sxs-lookup"><span data-stu-id="e0a55-110">This is part of a **3-article series** on **Explorer (also known as Threat Explorer)**, **email security**, and **Explorer and Real-time detections basics** (such as differences between the tools, and permissions needed to operate them).</span></span> <span data-ttu-id="e0a55-111">Les deux autres articles de cette série sont le recherche de menaces dans [l’Explorateur](threat-hunting-in-threat-explorer.md) et la [sécurité de messagerie avec l’Explorateur.](email-security-in-microsoft-defender.md)</span><span class="sxs-lookup"><span data-stu-id="e0a55-111">The other two articles in this series are [Threat hunting in Explorer](threat-hunting-in-threat-explorer.md) and [Email security with Explorer](email-security-in-microsoft-defender.md).</span></span>

<span data-ttu-id="e0a55-112">Cet article explique la différence entre l’Explorateur et les rapports de détections en temps réel, ainsi que les licences et autorisations requises.</span><span class="sxs-lookup"><span data-stu-id="e0a55-112">This article explains the difference between Explorer and real-time detections reporting, and the licenses and permissions that are required.</span></span>

<span data-ttu-id="e0a55-113">Si votre organisation dispose de [Microsoft Defender](defender-for-office-365.md)pour Office 365 et que vous disposez des [autorisations,](#required-licenses-and-permissions)vous pouvez utiliser l’Explorateur **(également** appelé Explorateur de menaces) ou les détections en temps réel pour détecter et corriger les **menaces.**</span><span class="sxs-lookup"><span data-stu-id="e0a55-113">If your organization has [Microsoft Defender for Office 365](defender-for-office-365.md), and you have the [permissions](#required-licenses-and-permissions), you can use **Explorer** (also known as **Threat Explorer**) or **Real-time detections** to detect and remediate threats.</span></span>

<span data-ttu-id="e0a55-114">Dans le portail Microsoft 365 Defender ( ), go <https://security.microsoft.com> to **Email & collaboration,** and then choose **Explorer** _or_ **Real-time detections**.</span><span class="sxs-lookup"><span data-stu-id="e0a55-114">In the Microsoft 365 Defender portal (<https://security.microsoft.com>), go to **Email & collaboration**, and then choose **Explorer** _or_ **Real-time detections**.</span></span>

<span data-ttu-id="e0a55-115">Avec ces outils, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="e0a55-115">With these tools, you can:</span></span>

- <span data-ttu-id="e0a55-116">Consultez les programmes malveillants détectés Microsoft 365 fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e0a55-116">See malware detected by Microsoft 365 security features.</span></span>
- <span data-ttu-id="e0a55-117">Afficher l’URL de hameçonnage et cliquer sur les données de verdict.</span><span class="sxs-lookup"><span data-stu-id="e0a55-117">View phishing URL and click verdict data.</span></span>
- <span data-ttu-id="e0a55-118">Démarrez un processus d’examen et de réponse automatisé à partir d’un affichage dans l’Explorateur.</span><span class="sxs-lookup"><span data-stu-id="e0a55-118">Start an automated investigation and response process from a view in Explorer.</span></span>
- <span data-ttu-id="e0a55-119">Examinez les e-mails malveillants, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="e0a55-119">Investigate malicious email, and more.</span></span>

<span data-ttu-id="e0a55-120">Pour plus d’informations, voir [Sécurité du courrier électronique avec l’Explorateur.](email-security-in-microsoft-defender.md)</span><span class="sxs-lookup"><span data-stu-id="e0a55-120">For more information, see [Email security with Explorer](email-security-in-microsoft-defender.md).</span></span>

## <a name="differences-between-explorer-and-real-time-detections"></a><span data-ttu-id="e0a55-121">Différences entre les détections de l’Explorateur et en temps réel</span><span class="sxs-lookup"><span data-stu-id="e0a55-121">Differences between Explorer and Real-time detections</span></span>

- <span data-ttu-id="e0a55-122">*Les détections en temps réel* sont un outil de rapports disponible dans Defender pour Office 365 Plan 1.</span><span class="sxs-lookup"><span data-stu-id="e0a55-122">*Real-time detections* is a reporting tool available in Defender for Office 365 Plan 1.</span></span> <span data-ttu-id="e0a55-123">*L’Explorateur de* menaces est un outil de recherche et de correction des menaces disponible dans Defender Office 365 Plan 2.</span><span class="sxs-lookup"><span data-stu-id="e0a55-123">*Threat Explorer* is a threat hunting and remediation tool available in Defender for Office 365 Plan 2.</span></span>
- <span data-ttu-id="e0a55-124">Le rapport de détections en temps réel vous permet d’afficher les détections en temps réel.</span><span class="sxs-lookup"><span data-stu-id="e0a55-124">The Real-time detections report allows you to view detections in real time.</span></span> <span data-ttu-id="e0a55-125">L’Explorateur de menaces le fait également, mais fournit des détails supplémentaires pour une attaque donnée, comme la mise en surbrillance des campagnes d’attaque, et offre aux équipes des opérations de sécurité la possibilité de corriger les menaces (notamment le déclenchement d’une enquête automatisée et d’une enquête sur les [réponses).](automated-investigation-response-office.md)</span><span class="sxs-lookup"><span data-stu-id="e0a55-125">Threat Explorer does this as well, but it provides additional details for a given attack, such as highlighting attack campaigns, and gives security operations teams the ability to remediate threats (including triggering an [Automated Investigation and Response investigation](automated-investigation-response-office.md)).</span></span>
- <span data-ttu-id="e0a55-126">Un *affichage de courrier tout* est disponible dans l’Explorateur de menaces, mais n’est pas inclus dans le rapport de détections en temps réel.</span><span class="sxs-lookup"><span data-stu-id="e0a55-126">An *All email* view is available in Threat Explorer, but not included in the Real-time detections report.</span></span>
- <span data-ttu-id="e0a55-127">Des fonctionnalités de filtrage enrichies et des actions de correction sont incluses dans l’Explorateur de menaces.</span><span class="sxs-lookup"><span data-stu-id="e0a55-127">Rich filtering capabilities and remediation actions are included in Threat Explorer.</span></span> <span data-ttu-id="e0a55-128">Pour plus d’informations, voir Microsoft Defender pour la description Office 365 service : disponibilité des fonctionnalités dans [Defender pour Office 365 plans.](/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#feature-availability-across-advanced-threat-protection-atp-plans)</span><span class="sxs-lookup"><span data-stu-id="e0a55-128">For more information, see [Microsoft Defender for Office 365 Service Description: Feature availability across Defender for Office 365 plans](/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#feature-availability-across-advanced-threat-protection-atp-plans).</span></span>

## <a name="required-licenses-and-permissions"></a><span data-ttu-id="e0a55-129">Licences et autorisations requises</span><span class="sxs-lookup"><span data-stu-id="e0a55-129">Required licenses and permissions</span></span>

<span data-ttu-id="e0a55-130">Vous devez avoir [Microsoft Defender](defender-for-office-365.md) pour Office 365 utiliser l’explorateur ou les détections en temps réel :</span><span class="sxs-lookup"><span data-stu-id="e0a55-130">You must have [Microsoft Defender for Office 365](defender-for-office-365.md) to use either of Explorer or Real-time detections:</span></span>

- <span data-ttu-id="e0a55-131">Explorer est inclus uniquement dans Defender pour Office 365 Plan 2.</span><span class="sxs-lookup"><span data-stu-id="e0a55-131">Explorer is only included in Defender for Office 365 Plan 2.</span></span>
- <span data-ttu-id="e0a55-132">Le rapport détections en temps réel est inclus dans Defender pour Office 365 Plan 1.</span><span class="sxs-lookup"><span data-stu-id="e0a55-132">The Real-time detections report is included in Defender for Office 365 Plan 1.</span></span>

<span data-ttu-id="e0a55-133">Les équipes des opérations de sécurité doivent attribuer des licences à tous les utilisateurs qui doivent être protégés par Defender pour Office 365 et sachent que les détections d’Explorateur et en temps réel montrent les données de détection pour les utilisateurs sous licence.</span><span class="sxs-lookup"><span data-stu-id="e0a55-133">Security Operations teams need to assign licenses for all users who should be protected by Defender for Office 365 and be aware that Explorer and Real-time detections show detection data for licensed users.</span></span>

<span data-ttu-id="e0a55-134">Pour afficher et utiliser *les* détections de l’Explorateur ou en temps réel, vous avez besoin des autorisations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e0a55-134">To view and use Explorer *or* Real-time detections, you need the following permissions:</span></span>

- <span data-ttu-id="e0a55-135">Dans Defender pour Office 365 :</span><span class="sxs-lookup"><span data-stu-id="e0a55-135">In Defender for Office 365:</span></span>
  - <span data-ttu-id="e0a55-136">Gestion de l’organisation</span><span class="sxs-lookup"><span data-stu-id="e0a55-136">Organization Management</span></span>
  - <span data-ttu-id="e0a55-137">Administrateur de sécurité (peut être affecté dans le centre d’administration Azure Active Directory de sécurité ( <https://aad.portal.azure.com> )</span><span class="sxs-lookup"><span data-stu-id="e0a55-137">Security Administrator (this can be assigned in the Azure Active Directory admin center (<https://aad.portal.azure.com>)</span></span>
  - <span data-ttu-id="e0a55-138">Lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="e0a55-138">Security Reader</span></span>
- <span data-ttu-id="e0a55-139">Dans Exchange Online :</span><span class="sxs-lookup"><span data-stu-id="e0a55-139">In Exchange Online:</span></span>
  - <span data-ttu-id="e0a55-140">Gestion de l’organisation</span><span class="sxs-lookup"><span data-stu-id="e0a55-140">Organization Management</span></span>
  - <span data-ttu-id="e0a55-141">Afficher uniquement la gestion de l’organisation</span><span class="sxs-lookup"><span data-stu-id="e0a55-141">View-Only Organization Management</span></span>
  - <span data-ttu-id="e0a55-142">Afficher uniquement les destinataires</span><span class="sxs-lookup"><span data-stu-id="e0a55-142">View-Only Recipients</span></span>
  - <span data-ttu-id="e0a55-143">Gestion de la conformité</span><span class="sxs-lookup"><span data-stu-id="e0a55-143">Compliance Management</span></span>

<span data-ttu-id="e0a55-144">Pour en savoir plus sur les rôles et les autorisations, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="e0a55-144">To learn more about roles and permissions, see the following articles:</span></span>

- [<span data-ttu-id="e0a55-145">Autorisations dans le Portail Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e0a55-145">Permissions in the Microsoft 365 Defender portal</span></span>](permissions-microsoft-365-security-center.md)
- [<span data-ttu-id="e0a55-146">Autorisations dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="e0a55-146">Permissions in Exchange Online</span></span>](/e/exchange/permissions-exo/permissions-exo)

## <a name="more-information"></a><span data-ttu-id="e0a55-147">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e0a55-147">More information</span></span>

- [<span data-ttu-id="e0a55-148">L’Explorateur de menaces collecte les détails des e-mails sur la page d’entité de messagerie</span><span class="sxs-lookup"><span data-stu-id="e0a55-148">Threat Explorer collect email details on the email entity page</span></span>](mdo-email-entity-page.md)
- [<span data-ttu-id="e0a55-149">Rechercher et d’examiner l’e-mail malveillant qui a été distribué</span><span class="sxs-lookup"><span data-stu-id="e0a55-149">Find and investigate malicious email that was delivered</span></span>](investigate-malicious-email-that-was-delivered.md)
- [<span data-ttu-id="e0a55-150">Afficher les fichiers malveillants détectés dans SharePoint Online, OneDrive et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="e0a55-150">View malicious files detected in SharePoint Online, OneDrive, and Microsoft Teams</span></span>](mdo-for-spo-odb-and-teams.md)
- [<span data-ttu-id="e0a55-151">Rapport sur l’état de la protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="e0a55-151">Threat protection status report</span></span>](view-email-security-reports.md#threat-protection-status-report)
- [<span data-ttu-id="e0a55-152">Examen et réponses automatisés dans Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="e0a55-152">Automated investigation and response in Microsoft Threat Protection</span></span>](automated-investigation-response-office.md)
