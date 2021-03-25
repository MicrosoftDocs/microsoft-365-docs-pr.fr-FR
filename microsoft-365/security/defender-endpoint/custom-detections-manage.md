---
title: Afficher et gérer des règles de détection personnalisées dans Microsoft Defender ATP
ms.reviewer: ''
description: Découvrez comment afficher et gérer des règles de détection personnalisées
keywords: détections personnalisées, afficher, gérer, alertes, modifier, exécuter à la demande, règles de détection, repérage avancé, recherche, requête, actions de réponse, mdatp, microsoft defender atp
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: lomayor
author: lomayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: f6a7fc4d4141b19f9c5129eea9b89943d07695b2
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51165776"
---
# <a name="view-and-manage-custom-detection-rules"></a><span data-ttu-id="ca99a-104">Afficher et gérer des règles de détection personnalisées</span><span class="sxs-lookup"><span data-stu-id="ca99a-104">View and manage custom detection rules</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="ca99a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ca99a-105">**Applies to:**</span></span>
- [<span data-ttu-id="ca99a-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ca99a-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="ca99a-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ca99a-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="ca99a-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="ca99a-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="ca99a-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="ca99a-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)

<span data-ttu-id="ca99a-110">Gérez vos règles de [détection personnalisées](custom-detection-rules.md) existantes pour vous assurer qu’elles trouvent efficacement les menaces et prennent des mesures.</span><span class="sxs-lookup"><span data-stu-id="ca99a-110">Manage your existing [custom detection rules](custom-detection-rules.md) to ensure they are effectively finding threats and taking actions.</span></span> <span data-ttu-id="ca99a-111">Découvrez comment afficher la liste des règles, vérifier leurs précédentes séries et passer en revue les alertes qu’elles ont déclenchées.</span><span class="sxs-lookup"><span data-stu-id="ca99a-111">Explore how to view the list of rules, check their previous runs, and review the alerts they have triggered.</span></span> <span data-ttu-id="ca99a-112">Vous pouvez également exécuter une règle à la demande et la modifier.</span><span class="sxs-lookup"><span data-stu-id="ca99a-112">You can also run a rule on demand and modify it.</span></span>

## <a name="required-permissions"></a><span data-ttu-id="ca99a-113">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="ca99a-113">Required permissions</span></span>

<span data-ttu-id="ca99a-114">Pour créer ou gérer des détections personnalisées, [votre rôle](user-roles.md#create-roles-and-assign-the-role-to-an-azure-active-directory-group) doit avoir l’autorisation gérer les **paramètres de** sécurité.</span><span class="sxs-lookup"><span data-stu-id="ca99a-114">To create or manage custom detections, [your role](user-roles.md#create-roles-and-assign-the-role-to-an-azure-active-directory-group) needs to have the **manage security settings** permission.</span></span>

## <a name="view-existing-rules"></a><span data-ttu-id="ca99a-115">Afficher les règles existantes</span><span class="sxs-lookup"><span data-stu-id="ca99a-115">View existing rules</span></span>

<span data-ttu-id="ca99a-116">Pour afficher toutes les règles de détection personnalisées **existantes,** accédez à Paramètres  >  **Détections personnalisées.**</span><span class="sxs-lookup"><span data-stu-id="ca99a-116">To view all existing custom detection rules, navigate to **Settings** > **Custom detections**.</span></span> <span data-ttu-id="ca99a-117">La page répertorie toutes les règles avec les informations d’exécuter suivantes :</span><span class="sxs-lookup"><span data-stu-id="ca99a-117">The page lists all the rules with the following run information:</span></span>

- <span data-ttu-id="ca99a-118">**Dernière série**: lorsqu’une règle a été exécuté pour la dernière fois pour vérifier les correspondances de requête et générer des alertes</span><span class="sxs-lookup"><span data-stu-id="ca99a-118">**Last run**—when a rule was last run to check for query matches and generate alerts</span></span>
- <span data-ttu-id="ca99a-119">**État de la dernière fois**: si une règle s’est correctement exécuté</span><span class="sxs-lookup"><span data-stu-id="ca99a-119">**Last run status**—whether a rule ran successfully</span></span>
- <span data-ttu-id="ca99a-120">**Next run**—the next scheduled run</span><span class="sxs-lookup"><span data-stu-id="ca99a-120">**Next run**—the next scheduled run</span></span>
- <span data-ttu-id="ca99a-121">**État**: si une règle a été allumée ou désactivée</span><span class="sxs-lookup"><span data-stu-id="ca99a-121">**Status**—whether a rule has been turned on or off</span></span>

## <a name="view-rule-details-modify-rule-and-run-rule"></a><span data-ttu-id="ca99a-122">Afficher les détails de la règle, modifier la règle et exécuter la règle</span><span class="sxs-lookup"><span data-stu-id="ca99a-122">View rule details, modify rule, and run rule</span></span>

<span data-ttu-id="ca99a-123">Pour afficher des informations complètes sur une règle de détection personnalisée, sélectionnez le nom de la règle dans la liste des règles dans **paramètres**  >  **détections personnalisées**.</span><span class="sxs-lookup"><span data-stu-id="ca99a-123">To view comprehensive information about a custom detection rule, select the name of rule from the list of rules in **Settings** > **Custom detections**.</span></span> <span data-ttu-id="ca99a-124">Une page sur la règle sélectionnée affiche les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="ca99a-124">A page about the selected rule displays the following information:</span></span>

- <span data-ttu-id="ca99a-125">Informations générales sur la règle, y compris les détails de l’alerte, l’état d’exécuter et l’étendue</span><span class="sxs-lookup"><span data-stu-id="ca99a-125">General information about the rule, including the details of the alert, run status, and scope</span></span>
- <span data-ttu-id="ca99a-126">Liste des alertes déclenchées</span><span class="sxs-lookup"><span data-stu-id="ca99a-126">List of triggered alerts</span></span>
- <span data-ttu-id="ca99a-127">Liste des actions déclenchées</span><span class="sxs-lookup"><span data-stu-id="ca99a-127">List of triggered actions</span></span>

<span data-ttu-id="ca99a-128">![Page règle de détection personnalisée](images/atp-custom-detection-rule-details.png)</span><span class="sxs-lookup"><span data-stu-id="ca99a-128">![Custom detection rule page](images/atp-custom-detection-rule-details.png)</span></span><br>
<span data-ttu-id="ca99a-129">*Page règle de détection personnalisée*</span><span class="sxs-lookup"><span data-stu-id="ca99a-129">*Custom detection rule page*</span></span>

<span data-ttu-id="ca99a-130">Vous pouvez également prendre les mesures suivantes sur la règle à partir de cette page :</span><span class="sxs-lookup"><span data-stu-id="ca99a-130">You can also take the following actions on the rule from this page:</span></span>

- <span data-ttu-id="ca99a-131">**Exécutez** la règle immédiatement.</span><span class="sxs-lookup"><span data-stu-id="ca99a-131">**Run**—run the rule immediately.</span></span> <span data-ttu-id="ca99a-132">Cette action réinitialise également l’intervalle pour la prochaine suite.</span><span class="sxs-lookup"><span data-stu-id="ca99a-132">This action also resets the interval for the next run.</span></span>
- <span data-ttu-id="ca99a-133">**Modifier**— modifier la règle sans modifier la requête</span><span class="sxs-lookup"><span data-stu-id="ca99a-133">**Edit**—modify the rule without changing the query</span></span>
- <span data-ttu-id="ca99a-134">**Modifier la requête —** modifier la requête dans le recherche avancée</span><span class="sxs-lookup"><span data-stu-id="ca99a-134">**Modify query**—edit the query in advanced hunting</span></span>
- <span data-ttu-id="ca99a-135">**Activer**  /  **Désactiver :** activer la règle ou l’arrêter d’être en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="ca99a-135">**Turn on** / **Turn off**—enable the rule or stop it from running</span></span>
- <span data-ttu-id="ca99a-136">**Supprimer**: désactiver la règle et la supprimer</span><span class="sxs-lookup"><span data-stu-id="ca99a-136">**Delete**—turn off the rule and remove it</span></span>

>[!TIP]
><span data-ttu-id="ca99a-137">Pour afficher rapidement des informations et agir sur un élément d’un tableau, utilisez la colonne de sélection [&#10003;] à gauche du tableau.</span><span class="sxs-lookup"><span data-stu-id="ca99a-137">To quickly view information and take action on an item in a table, use the selection column [&#10003;] at the left of the table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca99a-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca99a-138">Related topics</span></span>
- [<span data-ttu-id="ca99a-139">Vue d’ensemble des détections personnalisées</span><span class="sxs-lookup"><span data-stu-id="ca99a-139">Custom detections overview</span></span>](overview-custom-detections.md)
- [<span data-ttu-id="ca99a-140">Créer des règles de détection</span><span class="sxs-lookup"><span data-stu-id="ca99a-140">Create detection rules</span></span>](custom-detection-rules.md)
- [<span data-ttu-id="ca99a-141">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="ca99a-141">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="ca99a-142">Afficher et organiser les alertes</span><span class="sxs-lookup"><span data-stu-id="ca99a-142">View and organize alerts</span></span>](alerts-queue.md)
