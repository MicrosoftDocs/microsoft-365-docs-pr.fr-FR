---
title: Enquêter sur les utilisateurs dans Microsoft 365 Defender
description: Enquêter sur les utilisateurs pour un incident dans le centre Microsoft 365 sécurité de la ville.
keywords: sécurité, malware, Microsoft 365, M365, centre de sécurité, moniteur, rapport, identités, données, appareils, applications, incident, analyse, réponse
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
ms.openlocfilehash: 72eb111da2f342b78aa6161c7334a7252314b4a5
ms.sourcegitcommit: 0936f075a1205b8f8a71a7dd7761a2e2ce6167b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52572800"
---
# <a name="investigate-users-in-microsoft-365-defender"></a><span data-ttu-id="e9596-104">Enquêter sur les utilisateurs dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e9596-104">Investigate users in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="e9596-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e9596-105">**Applies to:**</span></span>

- <span data-ttu-id="e9596-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e9596-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="e9596-107">Une partie de votre enquête sur les incidents peut inclure des comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e9596-107">Part of your incident investigation can include user accounts.</span></span> <span data-ttu-id="e9596-108">Commencez par **l’onglet** Utilisateurs pour un incident provenant **d’incidents & alertes** *>'incident* **> utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="e9596-108">Start with the **Users** tab for an incident from **Incidents & alerts >** *incident* **> Users**.</span></span> 

:::image type="content" source="../../media/investigate-incidents/incident-users.png" alt-text="Exemple d’une page utilisateurs pour un incident":::

<span data-ttu-id="e9596-110">Pour obtenir un résumé rapide d’un compte utilisateur pour l’incident, sélectionnez la marque de contrôle à côté du nom du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e9596-110">To get a quick summary of a user account for the incident, select the check mark next to the user account name.</span></span> <span data-ttu-id="e9596-111">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="e9596-111">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-users/incidents-ss-user-pane.png" alt-text="Exemple du volet résumé du compte utilisateur pour un incident dans le centre de sécurité Microsoft 365'utilisateur":::

> [!NOTE]
> <span data-ttu-id="e9596-113">La page Utilisateur affiche Azure Active Directory organisation (Azure AD) ainsi que des groupes, vous aidant à comprendre les groupes et les autorisations associés à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e9596-113">The User page shows Azure Active Directory (Azure AD) organization as well as groups, helping you understand the groups and permissions associated with a user.</span></span>

<span data-ttu-id="e9596-114">Dans cette page de survol, vous pouvez consulter les informations sur les menaces des utilisateurs, y compris les incidents actuels, les alertes actives et le niveau de risque, ainsi que l’exposition des utilisateurs, les comptes, les appareils et plus encore.</span><span class="sxs-lookup"><span data-stu-id="e9596-114">In this fly-out page, you can review user threat information, including any current incidents, active alerts, and risk level as well as user exposure, accounts, devices, and more.</span></span>

<span data-ttu-id="e9596-115">En outre, vous pouvez prendre des mesures directement dans le centre de sécurité Microsoft 365 pour s’adresser à un utilisateur compromis, confirmant que l’utilisateur est compromis ou l’obligeant à se connecter à nouveau.</span><span class="sxs-lookup"><span data-stu-id="e9596-115">In addition, you can take action directly in the Microsoft 365 security center to address a compromised user, confirming the user is compromised or requiring them to sign in again.</span></span>

<span data-ttu-id="e9596-116">De là, vous pouvez sélectionner Go **to user page pour voir** les détails d’un compte utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e9596-116">From here, you can select **Go to user page** to see the details of a user account.</span></span> <span data-ttu-id="e9596-117">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="e9596-117">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-users/incidents-ss-user-details.png" alt-text="Exemple de page de compte utilisateur pour un incident dans le centre Microsoft 365 sécurité":::

<span data-ttu-id="e9596-119">Vous pouvez également voir cette page en sélectionnant le nom du compte utilisateur à partir de la liste sur la page **Utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="e9596-119">You can also see this page by selecting the name of the user account from the list on the **Users** page.</span></span>

<span data-ttu-id="e9596-120">La page utilisateur Microsoft 365 centre de sécurité combine les informations de Microsoft Defender pour Endpoint, Microsoft Defender for Identity et Microsoft Cloud App Security (selon les licences que vous avez).</span><span class="sxs-lookup"><span data-stu-id="e9596-120">The Microsoft 365 security center user page combines information from Microsoft Defender for Endpoint, Microsoft Defender for Identity, and Microsoft Cloud App Security (depending on what licenses you have).</span></span> 

<span data-ttu-id="e9596-121">Cette page affiche des informations spécifiques au risque de sécurité d’un compte utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e9596-121">This page shows information specific to the security risk of a user account.</span></span> <span data-ttu-id="e9596-122">Cela inclut un score qui permet d’évaluer les risques et les événements récents et les alertes qui ont contribué au risque global de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e9596-122">This includes a score that helps assess risk and recent events and alerts that contributed to the overall risk of the user.</span></span>

<span data-ttu-id="e9596-123">À partir de cette page, vous pouvez faire ces actions supplémentaires :</span><span class="sxs-lookup"><span data-stu-id="e9596-123">From this page, you can do these additional actions:</span></span> 

- <span data-ttu-id="e9596-124">Marquer le compte utilisateur comme compromis</span><span class="sxs-lookup"><span data-stu-id="e9596-124">Mark the user account as compromised</span></span>
- <span data-ttu-id="e9596-125">Exiger de l’utilisateur qu’il se connecte à nouveau</span><span class="sxs-lookup"><span data-stu-id="e9596-125">Require the user to sign in again</span></span>
- <span data-ttu-id="e9596-126">Suspendre le compte utilisateur</span><span class="sxs-lookup"><span data-stu-id="e9596-126">Suspend the user account</span></span>
- <span data-ttu-id="e9596-127">Voir les paramètres Azure Active Directory compte utilisateur (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="e9596-127">See the Azure Active Directory (Azure AD) user account settings</span></span>
- <span data-ttu-id="e9596-128">Voir les fichiers appartenant au compte utilisateur</span><span class="sxs-lookup"><span data-stu-id="e9596-128">View the files owned by the user account</span></span>
- <span data-ttu-id="e9596-129">Consultez les fichiers partagés avec cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e9596-129">View files shared with this user.</span></span> 

<span data-ttu-id="e9596-130">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="e9596-130">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-users/incidents-ss-user-details-actions.png" alt-text="Exemple des actions sur un compte utilisateur pour un incident dans le centre Microsoft 365 sécurité":::


<!--
You can access this page from multiple areas in the Microsoft 365 security center. You can access this page from a specific incident in the **Users** tab. Some alerts might include users as a specific affected asset. You can also search for users.  

Learn more about how to investigate users and potential risk [in this Cloud App Security tutorial](/cloud-app-security/tutorial-ueba#:~:text=To%20identify%20who%20your%20riskiest,user%20page%20to%20investigate%20them).

--> 

## <a name="next-steps"></a><span data-ttu-id="e9596-132">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="e9596-132">Next steps</span></span>

<span data-ttu-id="e9596-133">Au besoin pour les incidents en cours, poursuivez votre [enquête](investigate-incidents.md).</span><span class="sxs-lookup"><span data-stu-id="e9596-133">As needed for in-process incidents, continue your [investigation](investigate-incidents.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e9596-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9596-134">See also</span></span>

- [<span data-ttu-id="e9596-135">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="e9596-135">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="e9596-136">Hiérarchiser les incidents</span><span class="sxs-lookup"><span data-stu-id="e9596-136">Prioritize incidents</span></span>](incident-queue.md)
- [<span data-ttu-id="e9596-137">Gérer les incidents</span><span class="sxs-lookup"><span data-stu-id="e9596-137">Manage incidents</span></span>](manage-incidents.md)