---
title: Exemple d’attaque par e-mail de hameçonnage
description: Analyse pas à pas d’une attaque par hameçonnage.
keywords: incidents, alertes, enquêter, corrélation, attaque, machines, appareils, utilisateurs, identités, identité, boîte de réception, e-mail, 365, microsoft, m365
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.technology: m365d
ms.openlocfilehash: 41a2c73ce5e1c3060d88572f4fa7afe63e193f46
ms.sourcegitcommit: de5fce90de22ba588e75e1a1d2e87e03b9e25ec7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "52299987"
---
# <a name="example-of-a-phishing-email-attack"></a><span data-ttu-id="a47ab-104">Exemple d’attaque par e-mail de hameçonnage</span><span class="sxs-lookup"><span data-stu-id="a47ab-104">Example of a phishing email attack</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="a47ab-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a47ab-105">**Applies to:**</span></span>
- <span data-ttu-id="a47ab-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a47ab-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="a47ab-107">Microsoft 365 Defender peut vous aider à détecter les pièces jointes malveillantes remis par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="a47ab-107">Microsoft 365 Defender can help detect malicious attachments delivered via email.</span></span> <span data-ttu-id="a47ab-108">Dans la mesure où le Centre de sécurité et conformité [Office 365](https://protection.office.com/) s’intègre à Microsoft 365 Defender, les analystes de sécurité peuvent avoir une visibilité sur les menaces provenant de Office 365, par exemple par le biais de pièces jointes de courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="a47ab-108">Since the [Office 365 Security and Compliance Center](https://protection.office.com/) integrates with Microsoft 365 Defender, security analysts can have visibility on threats coming in from Office 365, such as through email attachments.</span></span>

<span data-ttu-id="a47ab-109">Par exemple, un analyste a été affecté à un incident à plusieurs étapes.</span><span class="sxs-lookup"><span data-stu-id="a47ab-109">For example, an analyst was assigned a multi-stage incident.</span></span>
 
:::image type="content" source="../../media/first-incident-path-phishing/first-incident-phishing-incident.png" alt-text="Exemple d’incident en plusieurs étapes"::: 

<span data-ttu-id="a47ab-111">Dans **l’onglet Alertes** de l’incident, les alertes de Defender Office 365 et Microsoft Cloud App Security sont affichées.</span><span class="sxs-lookup"><span data-stu-id="a47ab-111">In the **Alerts** tab of the incident, alerts from Defender for Office 365 and Microsoft Cloud App Security are displayed.</span></span> <span data-ttu-id="a47ab-112">L’analyste peut descendre dans defender pour Office 365 alertes en sélectionnant les alertes de messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="a47ab-112">The analyst can drill down into the Defender for Office 365 alerts by selecting the email messages alerts.</span></span> <span data-ttu-id="a47ab-113">Les détails de l’alerte s’affichent dans le volet latéral.</span><span class="sxs-lookup"><span data-stu-id="a47ab-113">The details of the alert are displayed on the side pane.</span></span>

:::image type="content" source="../../media/first-incident-path-phishing/first-incident-phishing-alerts.png" alt-text="Exemple d’alerte par courrier électronique":::
 
<span data-ttu-id="a47ab-115">En faisant défiler vers le bas, plus d’informations s’affichent, montrant les fichiers malveillants et l’utilisateur qui ont été touchés.</span><span class="sxs-lookup"><span data-stu-id="a47ab-115">By scrolling down further, more information is displayed, showing the malicious files and user that was impacted.</span></span>

:::image type="content" source="../../media/first-incident-path-phishing/first-incident-phishing-impact.png" alt-text="Exemple d’impact sur les utilisateurs et les fichiers d’une alerte par courrier électronique":::
  
<span data-ttu-id="a47ab-117">La sélection **de la page** Ouvrir une alerte vous permet d’obtenir l’alerte spécifique dans laquelle différentes informations peuvent être vues plus en détail en sélectionnant le lien.</span><span class="sxs-lookup"><span data-stu-id="a47ab-117">Selecting **Open alert page** takes you to the specific alert where various information can be viewed in greater detail by selecting the link.</span></span> <span data-ttu-id="a47ab-118">Le message électronique réel peut être vu en sélectionnant Afficher les messages dans **l’Explorateur** en bas du panneau.</span><span class="sxs-lookup"><span data-stu-id="a47ab-118">The actual email message can be viewed by selecting **View messages in Explorer** toward the bottom of the panel.</span></span>
 
:::image type="content" source="../../media/first-incident-path-phishing/first-incident-phishing-event-explorer.png" alt-text="Exemple de détails d’une alerte"::: 

<span data-ttu-id="a47ab-120">L’analyste se trouve alors sur la page Gestion des menaces dans laquelle l’objet, le destinataire, l’expéditeur et d’autres informations du courrier électronique sont affichés.</span><span class="sxs-lookup"><span data-stu-id="a47ab-120">This takes the analyst to the Threat Management page where the email Subject, Recipient, Sender, and other information are displayed.</span></span> <span data-ttu-id="a47ab-121">**ZaP** sous **Actions spéciales indique** à l’analyste que la fonctionnalité de purge automatique heure zéro a été implémentée.</span><span class="sxs-lookup"><span data-stu-id="a47ab-121">**ZAP** under **Special Actions** tells the analyst that the Zero-hour auto purge feature was implemented.</span></span> <span data-ttu-id="a47ab-122">ZAP détecte et supprime automatiquement les messages malveillants et de courrier indésirable des boîtes aux lettres au sein de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="a47ab-122">ZAP automatically detects and removes malicious and spam messages from mailboxes across the organization.</span></span> <span data-ttu-id="a47ab-123">Pour plus d’informations, voir [la purge automatique heure zéro (ZAP) dans Exchange Online](../office-365-security/zero-hour-auto-purge.md).</span><span class="sxs-lookup"><span data-stu-id="a47ab-123">For more information, see [Zero-hour auto purge (ZAP) in Exchange Online](../office-365-security/zero-hour-auto-purge.md).</span></span>

<span data-ttu-id="a47ab-124">D’autres actions peuvent être prises sur des messages spécifiques en sélectionnant **Actions.**</span><span class="sxs-lookup"><span data-stu-id="a47ab-124">Other actions can be taken on specific messages by selecting **Actions**.</span></span> 
 
:::image type="content" source="../../media/first-incident-path-phishing/first-incident-phishing-actions.png" alt-text="Exemple d’autres actions peuvent être prises sur les messages électroniques"::: 

## <a name="next-step"></a><span data-ttu-id="a47ab-126">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="a47ab-126">Next step</span></span>

<span data-ttu-id="a47ab-127">Consultez le chemin [d’accès à l’examen des attaques](first-incident-path-identity.md) basée sur l’identité.</span><span class="sxs-lookup"><span data-stu-id="a47ab-127">See the [identity-based attack](first-incident-path-identity.md) investigation path.</span></span>

## <a name="see-also"></a><span data-ttu-id="a47ab-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a47ab-128">See also</span></span>

- [<span data-ttu-id="a47ab-129">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="a47ab-129">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="a47ab-130">Enquêter sur des incidents</span><span class="sxs-lookup"><span data-stu-id="a47ab-130">Investigate incidents</span></span>](investigate-incidents.md)
- [<span data-ttu-id="a47ab-131">Gérer les incidents</span><span class="sxs-lookup"><span data-stu-id="a47ab-131">Manage incidents</span></span>](manage-incidents.md)
