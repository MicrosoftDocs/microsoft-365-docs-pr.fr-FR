---
title: Analyser les utilisateurs dans le Centre de sécurité Microsoft 365
description: Analyser les utilisateurs dans le Centre de sécurité Microsoft 365
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
ms.openlocfilehash: 1fb5a4eee41384ef1afc9b46e5bf538344718fe9
ms.sourcegitcommit: 4076b43a4b661de029f6307ddc1a989ab3108edb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "51939729"
---
# <a name="analyze-users-in-microsoft-365-security-center"></a><span data-ttu-id="75fd2-104">Analyser les utilisateurs dans le Centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="75fd2-104">Analyze users in Microsoft 365 security center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="75fd2-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="75fd2-105">**Applies to:**</span></span>

- <span data-ttu-id="75fd2-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="75fd2-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="75fd2-107">Une partie de votre analyse des incidents peut inclure des comptes d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="75fd2-107">Part of your incident analysis can include user accounts.</span></span> <span data-ttu-id="75fd2-108">Commencez par **l'onglet Utilisateurs** pour un incident à partir d'incidents **& alertes >** incident *>* **utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="75fd2-108">Start with the **Users** tab for an incident from **Incidents & alerts >** *incident* **> Users**.</span></span> 

:::image type="content" source="../../media/investigate-incidents/incident-users.png" alt-text="Exemple de page Utilisateurs pour un incident":::

<span data-ttu-id="75fd2-110">Pour obtenir un résumé rapide d'un compte d'utilisateur pour l'incident, cochez la coche en regard du nom du compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="75fd2-110">To get a quick summary of a user account for the incident, select the check mark next to the user account name.</span></span> <span data-ttu-id="75fd2-111">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="75fd2-111">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-users/incidents-ss-user-pane.png" alt-text="Exemple de volet récapitulatif du compte d'utilisateur pour un incident dans le Centre de sécurité Microsoft 365":::

<span data-ttu-id="75fd2-113">À partir de là, vous pouvez sélectionner La page d'accès à **l'utilisateur** pour voir les détails d'un compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="75fd2-113">From here, you can select **Go to user page** to see the details of a user account.</span></span> <span data-ttu-id="75fd2-114">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="75fd2-114">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-users/incidents-ss-user-details.png" alt-text="Exemple de page de compte d'utilisateur pour un incident dans le Centre de sécurité Microsoft 365":::

<span data-ttu-id="75fd2-116">Vous pouvez également voir cette page en sélectionnant le nom du compte d'utilisateur dans la liste de la page **Utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="75fd2-116">You can also see this page by selecting the name of the user account from the list on the **Users** page.</span></span>

<span data-ttu-id="75fd2-117">La page utilisateur du Centre de sécurité Microsoft 365 combine les informations de Microsoft Defender pour le point de terminaison, Microsoft Defender pour l'identité et Microsoft Cloud App Security (en fonction des licences que vous avez).</span><span class="sxs-lookup"><span data-stu-id="75fd2-117">The Microsoft 365 security center user page combines information from Microsoft Defender for Endpoint, Microsoft Defender for Identity, and Microsoft Cloud App Security (depending on what licenses you have).</span></span> 

<span data-ttu-id="75fd2-118">Cette page affiche des informations spécifiques au risque de sécurité d'un compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="75fd2-118">This page shows information specific to the security risk of a user account.</span></span> <span data-ttu-id="75fd2-119">Cela inclut un score qui permet d'évaluer les risques et les événements et alertes récents qui ont contribué au risque global de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="75fd2-119">This includes a score that helps assess risk and recent events and alerts that contributed to the overall risk of the user.</span></span>

<span data-ttu-id="75fd2-120">À partir de cette page, vous pouvez faire les actions supplémentaires suivantes :</span><span class="sxs-lookup"><span data-stu-id="75fd2-120">From this page, you can do these additional actions:</span></span> 

- <span data-ttu-id="75fd2-121">Marquer le compte d'utilisateur comme compromis</span><span class="sxs-lookup"><span data-stu-id="75fd2-121">Mark the user account as compromised</span></span>
- <span data-ttu-id="75fd2-122">Exiger que l'utilisateur se connecte à nouveau</span><span class="sxs-lookup"><span data-stu-id="75fd2-122">Require the user to sign in again</span></span>
- <span data-ttu-id="75fd2-123">Suspendre le compte d'utilisateur</span><span class="sxs-lookup"><span data-stu-id="75fd2-123">Suspend the user account</span></span>
- <span data-ttu-id="75fd2-124">Voir les paramètres du compte d'utilisateur Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="75fd2-124">See the Azure Active Directory (Azure AD) user account settings</span></span>
- <span data-ttu-id="75fd2-125">Afficher les fichiers du compte d'utilisateur</span><span class="sxs-lookup"><span data-stu-id="75fd2-125">View the files owned by the user account</span></span>
- <span data-ttu-id="75fd2-126">Afficher les fichiers partagés avec cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="75fd2-126">View files shared with this user.</span></span> 

<span data-ttu-id="75fd2-127">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="75fd2-127">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-users/incidents-ss-user-details-actions.png" alt-text="Exemple d'actions sur un compte d'utilisateur pour un incident dans le Centre de sécurité Microsoft 365":::


<!--
You can access this page from multiple areas in the Microsoft 365 security center. You can access this page from a specific incident in the **Users** tab. Some alerts might include users as a specific affected asset. You can also search for users.  

Learn more about how to investigate users and potential risk [in this Cloud App Security tutorial](/cloud-app-security/tutorial-ueba#:~:text=To%20identify%20who%20your%20riskiest,user%20page%20to%20investigate%20them).

--> 

## <a name="related-topics"></a><span data-ttu-id="75fd2-129">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="75fd2-129">Related topics</span></span>

- [<span data-ttu-id="75fd2-130">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="75fd2-130">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="75fd2-131">Hiérarchiser les incidents</span><span class="sxs-lookup"><span data-stu-id="75fd2-131">Prioritize incidents</span></span>](incident-queue.md)
- [<span data-ttu-id="75fd2-132">Gérer les incidents</span><span class="sxs-lookup"><span data-stu-id="75fd2-132">Manage incidents</span></span>](manage-incidents.md)