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
ms.openlocfilehash: 7ab7b5731d121106d930868b03330d4ac7befd77
ms.sourcegitcommit: de5fce90de22ba588e75e1a1d2e87e03b9e25ec7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "52300154"
---
# <a name="threat-explorer-and-real-time-detections-basics"></a><span data-ttu-id="c8597-103">Informations de base de l’explorateur de menaces et détections en temps réel</span><span class="sxs-lookup"><span data-stu-id="c8597-103">Threat Explorer and Real-time detections basics</span></span>

<span data-ttu-id="c8597-104">Contenu de cet article :</span><span class="sxs-lookup"><span data-stu-id="c8597-104">In this article:</span></span>

- [<span data-ttu-id="c8597-105">Différences entre l’Explorateur de menaces et les détections en temps réel</span><span class="sxs-lookup"><span data-stu-id="c8597-105">Differences between Threat Explorer and Real-time detections</span></span>](#differences-between-threat-explorer-and-real-time-detections)<br/>
- [<span data-ttu-id="c8597-106">Licences et autorisations requises</span><span class="sxs-lookup"><span data-stu-id="c8597-106">Required licenses and permissions</span></span>](#required-licenses-and-permissions)

> [!NOTE]
> <span data-ttu-id="c8597-107">Cela fait partie d’une série de **3** articles sur l’Explorateur de menaces **,** la sécurité du courrier électronique et les bases de détection **en** temps réel et de l’Explorateur (telles que les différences entre les outils et les autorisations nécessaires pour les utiliser).</span><span class="sxs-lookup"><span data-stu-id="c8597-107">This is part of a **3-article series** on **Threat Explorer (Explorer)**, **email security**, and **Explorer and Real-time detections basics** (such as differences between the tools, and permissions needed to operate them).</span></span> <span data-ttu-id="c8597-108">Les deux autres articles de cette série sont le recherche de menaces dans [l’Explorateur](threat-hunting-in-threat-explorer.md) de menaces et la sécurité du [courrier électronique avec l’Explorateur de menaces.](email-security-in-microsoft-defender.md)</span><span class="sxs-lookup"><span data-stu-id="c8597-108">The other two articles in this series are [Threat hunting in Threat Explorer](threat-hunting-in-threat-explorer.md) and [Email security with Threat Explorer](email-security-in-microsoft-defender.md).</span></span>

<span data-ttu-id="c8597-109">Cet article explique la différence entre les rapports sur l’exploration des menaces et les détections en temps réel, ainsi que les licences et autorisations requises.</span><span class="sxs-lookup"><span data-stu-id="c8597-109">This article explains the difference between threat exploration and real-time detections reporting, and the licenses and permissions that are required.</span></span>

<span data-ttu-id="c8597-110">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="c8597-110">**Applies to**</span></span>
- [<span data-ttu-id="c8597-111">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="c8597-111">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="c8597-112">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="c8597-112">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="c8597-113">Si votre organisation dispose de [Microsoft Defender](defender-for-office-365.md)pour Office 365 et que vous disposez des [autorisations,](#required-licenses-and-permissions)vous pouvez utiliser l’Explorateur de menaces **(appelé** **Explorateur)** ou les détections en temps réel pour détecter et corriger les **menaces.**</span><span class="sxs-lookup"><span data-stu-id="c8597-113">If your organization has [Microsoft Defender for Office 365](defender-for-office-365.md), and you have the [permissions](#required-licenses-and-permissions), you can use **Threat Explorer** (called **Explorer**) or **Real-time detections** to detect and remediate threats.</span></span>

<span data-ttu-id="c8597-114">Dans le Centre de sécurité &  **conformité,** sélectionnez Gestion des menaces, puis sélectionnez **Explorer**  ou **Détections en temps réel.**</span><span class="sxs-lookup"><span data-stu-id="c8597-114">In the **Security & Compliance Center**, go to **Threat management**, and then choose **Explorer** _or_ **Real-time detections**.</span></span>

<br>

****

|<span data-ttu-id="c8597-115">Avec Microsoft Defender pour Office 365 Plan 2, vous pouvez voir :</span><span class="sxs-lookup"><span data-stu-id="c8597-115">With Microsoft Defender for Office 365 Plan 2, you see:</span></span>|<span data-ttu-id="c8597-116">Avec Microsoft Defender pour Office 365 Plan 1, vous pouvez voir :</span><span class="sxs-lookup"><span data-stu-id="c8597-116">With Microsoft Defender for Office 365 Plan 1, you see:</span></span>|
|---|---|
|![Explorateur de menaces](../../media/threatmgmt-explorer.png)|![Détections en temps réel](../../media/threatmgmt-realtimedetections.png)|
|

<span data-ttu-id="c8597-119">Avec ces outils, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="c8597-119">With these tools, you can:</span></span>

- <span data-ttu-id="c8597-120">Consultez les programmes malveillants détectés Microsoft 365 fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c8597-120">See malware detected by Microsoft 365 security features.</span></span>
- <span data-ttu-id="c8597-121">Afficher l’URL de hameçonnage et cliquer sur les données de verdict.</span><span class="sxs-lookup"><span data-stu-id="c8597-121">View phishing URL and click verdict data.</span></span>
- <span data-ttu-id="c8597-122">Démarrez un processus d’examen et de réponse automatisé à partir d’un affichage dans l’Explorateur.</span><span class="sxs-lookup"><span data-stu-id="c8597-122">Start an automated investigation and response process from a view in Explorer.</span></span>
- <span data-ttu-id="c8597-123">Examinez les e-mails malveillants, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="c8597-123">Investigate malicious email, and more.</span></span>

<span data-ttu-id="c8597-124">Pour plus d’informations, [voir Sécurité du courrier électronique avec l’Explorateur de menaces.](email-security-in-microsoft-defender.md)</span><span class="sxs-lookup"><span data-stu-id="c8597-124">For more information, see [Email security with Threat Explorer](email-security-in-microsoft-defender.md).</span></span>

## <a name="differences-between-threat-explorer-and-real-time-detections"></a><span data-ttu-id="c8597-125">Différences entre l’Explorateur de menaces et les détections en temps réel</span><span class="sxs-lookup"><span data-stu-id="c8597-125">Differences between Threat Explorer and Real-time detections</span></span>

- <span data-ttu-id="c8597-126">*Les détections en temps réel* sont un outil de rapports disponible dans Defender pour Office 365 Plan 1.</span><span class="sxs-lookup"><span data-stu-id="c8597-126">*Real-time detections* is a reporting tool available in Defender for Office 365 Plan 1.</span></span> <span data-ttu-id="c8597-127">*L’Explorateur de* menaces est un outil de recherche et de correction des menaces disponible dans Defender Office 365 Plan 2.</span><span class="sxs-lookup"><span data-stu-id="c8597-127">*Threat Explorer* is a threat hunting and remediation tool available in Defender for Office 365 Plan 2.</span></span>
- <span data-ttu-id="c8597-128">Le rapport de détections en temps réel vous permet d’afficher les détections en temps réel.</span><span class="sxs-lookup"><span data-stu-id="c8597-128">The Real-time detections report allows you to view detections in real time.</span></span> <span data-ttu-id="c8597-129">L’Explorateur de menaces le fait également, mais fournit des détails supplémentaires pour une attaque donnée, comme la mise en surbrillance des campagnes d’attaque, et donne aux équipes des opérations de sécurité la possibilité de corriger les menaces (notamment le déclenchement d’une enquête automatisée et d’une enquête sur les [réponses).](automated-investigation-response-office.md)</span><span class="sxs-lookup"><span data-stu-id="c8597-129">Threat Explorer does this as well, but it provides additional details for a given attack, such as highlighting attack campaigns, and gives security operations teams the ability to remediate threats (including triggering an [Automated Investigation and Response investigation](automated-investigation-response-office.md)).</span></span>
- <span data-ttu-id="c8597-130">Un *affichage de courrier tout* est disponible dans l’Explorateur de menaces, mais n’est pas inclus dans le rapport de détections en temps réel.</span><span class="sxs-lookup"><span data-stu-id="c8597-130">An *All email* view is available in Threat Explorer, but not included in the Real-time detections report.</span></span>
- <span data-ttu-id="c8597-131">Des fonctionnalités de filtrage enrichies et des actions de correction sont incluses dans l’Explorateur de menaces.</span><span class="sxs-lookup"><span data-stu-id="c8597-131">Rich filtering capabilities and remediation actions are included in Threat Explorer.</span></span> <span data-ttu-id="c8597-132">Pour plus d’informations, voir Microsoft Defender pour la description Office 365 service : disponibilité des fonctionnalités dans [Defender pour Office 365 plans.](/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#feature-availability-across-advanced-threat-protection-atp-plans)</span><span class="sxs-lookup"><span data-stu-id="c8597-132">For more information, see [Microsoft Defender for Office 365 Service Description: Feature availability across Defender for Office 365 plans](/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#feature-availability-across-advanced-threat-protection-atp-plans).</span></span>

## <a name="required-licenses-and-permissions"></a><span data-ttu-id="c8597-133">Licences et autorisations requises</span><span class="sxs-lookup"><span data-stu-id="c8597-133">Required licenses and permissions</span></span>

<span data-ttu-id="c8597-134">Vous devez avoir [Microsoft Defender](defender-for-office-365.md) pour Office 365 utiliser l’explorateur ou les détections en temps réel :</span><span class="sxs-lookup"><span data-stu-id="c8597-134">You must have [Microsoft Defender for Office 365](defender-for-office-365.md) to use either of Explorer or Real-time detections:</span></span>

- <span data-ttu-id="c8597-135">Mais Explorer est inclus uniquement dans Defender pour Office 365 Plan 2.</span><span class="sxs-lookup"><span data-stu-id="c8597-135">But Explorer is only included in Defender for Office 365 Plan 2.</span></span>
- <span data-ttu-id="c8597-136">Le rapport détections en temps réel est inclus dans Defender pour Office 365 Plan 1.</span><span class="sxs-lookup"><span data-stu-id="c8597-136">The Real-time detections report is included in Defender for Office 365 Plan 1.</span></span>

<span data-ttu-id="c8597-137">Les équipes des opérations de sécurité doivent attribuer des licences à tous les utilisateurs qui doivent être protégés par Defender pour Office 365 et sachent que les détections d’Explorateur et en temps réel montrent les données de détection pour les utilisateurs sous licence.</span><span class="sxs-lookup"><span data-stu-id="c8597-137">Security Operations teams need to assign licenses for all users who should be protected by Defender for Office 365 and be aware that Explorer and Real-time detections show detection data for licensed users.</span></span>

<span data-ttu-id="c8597-138">Pour afficher et utiliser les *détections* de l’Explorateur ou en temps réel, vous devez avoir les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8597-138">To view and use Explorer *or* Real-time detections, you must have the following:</span></span>

- <span data-ttu-id="c8597-139">Pour le Centre de sécurité & conformité :</span><span class="sxs-lookup"><span data-stu-id="c8597-139">For the Security & Compliance Center:</span></span>

  - <span data-ttu-id="c8597-140">Gestion de l’organisation</span><span class="sxs-lookup"><span data-stu-id="c8597-140">Organization Management</span></span>
  - <span data-ttu-id="c8597-141">Administrateur de sécurité (peut être affecté dans le centre d’administration Azure Active Directory de sécurité ( <https://aad.portal.azure.com> )</span><span class="sxs-lookup"><span data-stu-id="c8597-141">Security Administrator (this can be assigned in the Azure Active Directory admin center (<https://aad.portal.azure.com>)</span></span>
  - <span data-ttu-id="c8597-142">Lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="c8597-142">Security Reader</span></span>

- <span data-ttu-id="c8597-143">Pour Exchange Online :</span><span class="sxs-lookup"><span data-stu-id="c8597-143">For Exchange Online:</span></span>

  - <span data-ttu-id="c8597-144">Gestion de l’organisation</span><span class="sxs-lookup"><span data-stu-id="c8597-144">Organization Management</span></span>
  - <span data-ttu-id="c8597-145">Afficher uniquement la gestion de l’organisation</span><span class="sxs-lookup"><span data-stu-id="c8597-145">View-Only Organization Management</span></span>
  - <span data-ttu-id="c8597-146">Afficher uniquement les destinataires</span><span class="sxs-lookup"><span data-stu-id="c8597-146">View-Only Recipients</span></span>
  - <span data-ttu-id="c8597-147">Gestion de la conformité</span><span class="sxs-lookup"><span data-stu-id="c8597-147">Compliance Management</span></span>

<span data-ttu-id="c8597-148">Pour en savoir plus sur les rôles et les autorisations, consultez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8597-148">To learn more about roles and permissions, see the following resources:</span></span>

- [<span data-ttu-id="c8597-149">Autorisations dans le centre de conformité et de sécurité</span><span class="sxs-lookup"><span data-stu-id="c8597-149">Permissions in the Security & Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
- [<span data-ttu-id="c8597-150">Autorisations des fonctionnalités dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="c8597-150">Feature permissions in Exchange Online</span></span>](/exchange/permissions-exo/feature-permissions)
- [<span data-ttu-id="c8597-151">Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="c8597-151">Exchange Online PowerShell</span></span>](/powershell/exchange/exchange-online-powershell)

## <a name="more-information"></a><span data-ttu-id="c8597-152">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="c8597-152">More information</span></span>
- [<span data-ttu-id="c8597-153">L’Explorateur de menaces collecte les détails des e-mails sur la page d’entité de messagerie</span><span class="sxs-lookup"><span data-stu-id="c8597-153">Threat Explorer collect email details on the email entity page</span></span>](mdo-email-entity-page.md)
- [<span data-ttu-id="c8597-154">Rechercher et d’examiner l’e-mail malveillant qui a été distribué</span><span class="sxs-lookup"><span data-stu-id="c8597-154">Find and investigate malicious email that was delivered</span></span>](investigate-malicious-email-that-was-delivered.md)
- [<span data-ttu-id="c8597-155">Afficher les fichiers malveillants détectés dans SharePoint Online, OneDrive et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="c8597-155">View malicious files detected in SharePoint Online, OneDrive, and Microsoft Teams</span></span>](mdo-for-spo-odb-and-teams.md)
- [<span data-ttu-id="c8597-156">Rapport sur l’état de la protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="c8597-156">Threat protection status report</span></span>](view-email-security-reports.md#threat-protection-status-report)
- [<span data-ttu-id="c8597-157">Examen et réponses automatisés dans Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="c8597-157">Automated investigation and response in Microsoft Threat Protection</span></span>](automated-investigation-response-office.md)