---
title: Examiner les utilisateurs dans Microsoft 365 Defender
description: Examinez les utilisateurs pour un incident dans le centre Microsoft 365 de sécurité.
keywords: sécurité, programmes malveillants, Microsoft 365, M365, centre de sécurité, surveiller, signaler, identités, données, appareils, applications, incident, analyser, réponse
ms.prod: m365-security
ms.mktglfcycl: deploy
localization_priority: Normal
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: dansimp
ms.date: ''
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
search.appverid: met150
ms.custom: seo-marvel-jun2020
ms.technology: m365d
ms.openlocfilehash: 7084b9370a0dd83265b37ff1d152e2164fe32813
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52539130"
---
# <a name="investigate-users-in-microsoft-365-defender"></a><span data-ttu-id="afee7-104">Examiner les utilisateurs dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="afee7-104">Investigate users in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="afee7-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="afee7-105">**Applies to:**</span></span>

- <span data-ttu-id="afee7-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="afee7-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="afee7-107">Une partie de votre enquête sur les incidents peut inclure des comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="afee7-107">Part of your incident investigation can include user accounts.</span></span> <span data-ttu-id="afee7-108">Commencez par **l’onglet Utilisateurs** pour un incident à partir d’incidents **& alertes >** incident *>* **utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="afee7-108">Start with the **Users** tab for an incident from **Incidents & alerts >** *incident* **> Users**.</span></span> 

:::image type="content" source="../../media/investigate-incidents/incident-users.png" alt-text="Exemple de page Utilisateurs pour un incident":::

<span data-ttu-id="afee7-110">Pour obtenir un résumé rapide d’un compte d’utilisateur pour l’incident, cochez la coche en regard du nom du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="afee7-110">To get a quick summary of a user account for the incident, select the check mark next to the user account name.</span></span> <span data-ttu-id="afee7-111">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="afee7-111">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-users/incidents-ss-user-pane.png" alt-text="Exemple de volet récapitulatif du compte d’utilisateur pour un incident dans le centre Microsoft 365 de sécurité":::

> [!NOTE]
> <span data-ttu-id="afee7-113">La page Utilisateur affiche Azure Active Directory organisation (AD), ainsi que des groupes, pour vous aider à comprendre les groupes et les autorisations associés à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="afee7-113">The User page shows Azure Active Directory (AD) organization as well as groups, helping you understand the groups and permissions associated with a user.</span></span>

<span data-ttu-id="afee7-114">Dans cette page volante, vous pouvez passer en revue les informations sur les menaces des utilisateurs, notamment les incidents actuels, les alertes actives et le niveau de risque, ainsi que l’exposition des utilisateurs, les comptes, les appareils, etc.</span><span class="sxs-lookup"><span data-stu-id="afee7-114">In this fly-out page, you can review user threat information, including any current incidents, active alerts, and risk level as well as user exposure, accounts, devices, and more.</span></span>

<span data-ttu-id="afee7-115">En outre, vous pouvez agir directement dans le Centre de sécurité Microsoft 365 pour traiter un utilisateur compromis, en confirmant que l’utilisateur est compromis ou en exigeant qu’il se connecte à nouveau.</span><span class="sxs-lookup"><span data-stu-id="afee7-115">In addition, you can take action directly in the Microsoft 365 security center to address a compromised user, confirming the user is compromised or requiring them to sign in again.</span></span>

<span data-ttu-id="afee7-116">À partir de là, vous pouvez sélectionner La page d’accès à **l’utilisateur** pour voir les détails d’un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="afee7-116">From here, you can select **Go to user page** to see the details of a user account.</span></span> <span data-ttu-id="afee7-117">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="afee7-117">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-users/incidents-ss-user-details.png" alt-text="Exemple de page de compte d’utilisateur pour un incident dans le centre Microsoft 365 sécurité":::

<span data-ttu-id="afee7-119">Vous pouvez également voir cette page en sélectionnant le nom du compte d’utilisateur dans la liste de la page **Utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="afee7-119">You can also see this page by selecting the name of the user account from the list on the **Users** page.</span></span>

<span data-ttu-id="afee7-120">La page utilisateur du centre de sécurité Microsoft 365 combine les informations de Microsoft Defender pour endpoint, Microsoft Defender pour identité et Microsoft Cloud App Security (en fonction des licences dont vous avez la licence).</span><span class="sxs-lookup"><span data-stu-id="afee7-120">The Microsoft 365 security center user page combines information from Microsoft Defender for Endpoint, Microsoft Defender for Identity, and Microsoft Cloud App Security (depending on what licenses you have).</span></span> 

<span data-ttu-id="afee7-121">Cette page affiche des informations spécifiques au risque de sécurité d’un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="afee7-121">This page shows information specific to the security risk of a user account.</span></span> <span data-ttu-id="afee7-122">Cela inclut un score qui permet d’évaluer les risques et les événements et alertes récents qui ont contribué au risque global de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="afee7-122">This includes a score that helps assess risk and recent events and alerts that contributed to the overall risk of the user.</span></span>

<span data-ttu-id="afee7-123">À partir de cette page, vous pouvez faire les actions supplémentaires suivantes :</span><span class="sxs-lookup"><span data-stu-id="afee7-123">From this page, you can do these additional actions:</span></span> 

- <span data-ttu-id="afee7-124">Marquer le compte d’utilisateur comme compromis</span><span class="sxs-lookup"><span data-stu-id="afee7-124">Mark the user account as compromised</span></span>
- <span data-ttu-id="afee7-125">Exiger que l’utilisateur se connecte à nouveau</span><span class="sxs-lookup"><span data-stu-id="afee7-125">Require the user to sign in again</span></span>
- <span data-ttu-id="afee7-126">Suspendre le compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="afee7-126">Suspend the user account</span></span>
- <span data-ttu-id="afee7-127">Voir les Azure Active Directory de compte d’utilisateur (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="afee7-127">See the Azure Active Directory (Azure AD) user account settings</span></span>
- <span data-ttu-id="afee7-128">Afficher les fichiers du compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="afee7-128">View the files owned by the user account</span></span>
- <span data-ttu-id="afee7-129">Afficher les fichiers partagés avec cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="afee7-129">View files shared with this user.</span></span> 

<span data-ttu-id="afee7-130">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="afee7-130">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-users/incidents-ss-user-details-actions.png" alt-text="Exemple d’actions sur un compte d’utilisateur pour un incident dans le centre Microsoft 365 sécurité":::


<!--
You can access this page from multiple areas in the Microsoft 365 security center. You can access this page from a specific incident in the **Users** tab. Some alerts might include users as a specific affected asset. You can also search for users.  

Learn more about how to investigate users and potential risk [in this Cloud App Security tutorial](/cloud-app-security/tutorial-ueba#:~:text=To%20identify%20who%20your%20riskiest,user%20page%20to%20investigate%20them).

--> 

## <a name="next-steps"></a><span data-ttu-id="afee7-132">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="afee7-132">Next steps</span></span>

<span data-ttu-id="afee7-133">Si nécessaire pour les incidents in-process, poursuivez votre [enquête.](investigate-incidents.md)</span><span class="sxs-lookup"><span data-stu-id="afee7-133">As needed for in-process incidents, continue your [investigation](investigate-incidents.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="afee7-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="afee7-134">See also</span></span>

- [<span data-ttu-id="afee7-135">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="afee7-135">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="afee7-136">Hiérarchiser les incidents</span><span class="sxs-lookup"><span data-stu-id="afee7-136">Prioritize incidents</span></span>](incident-queue.md)
- [<span data-ttu-id="afee7-137">Gérer les incidents</span><span class="sxs-lookup"><span data-stu-id="afee7-137">Manage incidents</span></span>](manage-incidents.md)