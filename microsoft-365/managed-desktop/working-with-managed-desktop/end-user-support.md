---
title: Obtenir la prise en charge des utilisateurs pour Microsoft Manged Desktop
description: Comment les utilisateurs peuvent obtenir de l’aide sur le service et les appareils
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.author: jaimeo
manager: laurawi
ms.topic: article
ms.openlocfilehash: 2eea02b0a891f65ccd7e4e993ca719b0f3aa1b8b
ms.sourcegitcommit: f7fbf45af64c5c0727fd5eaab309d20ad097a483
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "53362605"
---
# <a name="getting-help-for-users"></a><span data-ttu-id="a8946-104">Obtenir de l’aide pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="a8946-104">Getting help for users</span></span>

<span data-ttu-id="a8946-105">Si vous avez atteint le [](../service-description/user-support.md) point dans le flux de travail où vous devez demander l’accès ou l’escalade d’appareil élevé à Microsoft, suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a8946-105">If you've reached the point in the [workflow](../service-description/user-support.md) where you need to request elevated device access or escalation to Microsoft, follow these steps:</span></span>
 
>[!NOTE]
><span data-ttu-id="a8946-106">Ces options de prise en charge ne sont pas disponibles pour les appareils du groupe Test.</span><span class="sxs-lookup"><span data-stu-id="a8946-106">These support options are not available for devices in the Test group.</span></span>

## <a name="elevation-requests"></a><span data-ttu-id="a8946-107">Demandes d’élévation</span><span class="sxs-lookup"><span data-stu-id="a8946-107">Elevation requests</span></span>

<span data-ttu-id="a8946-108">Avant de demander un accès élevé à un appareil, il est préférable de passer en revue les actions les mieux adaptées.</span><span class="sxs-lookup"><span data-stu-id="a8946-108">Before you request elevated access to a device, it's best to review which actions are best suited.</span></span>

- <span data-ttu-id="a8946-109">**Ce processus** est généralement destiné à des actions qui seraient effectuées régulièrement lors de la résolution des problèmes liés Microsoft Manged Desktop appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="a8946-109">**Typical actions** are what this process is intended for and would be performed routinely while troubleshooting problems with Microsoft Managed Desktop devices.</span></span> <span data-ttu-id="a8946-110">Les exemples incluent :</span><span class="sxs-lookup"><span data-stu-id="a8946-110">Examples include:</span></span>
    - <span data-ttu-id="a8946-111">Élévation des niveaux des dépannages du système intégrés, de l’invite de commandes ou des Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a8946-111">Elevating built-in system troubleshooters, the command prompt, or Windows PowerShell</span></span>
    - <span data-ttu-id="a8946-112">Résolution des problèmes des applications métier</span><span class="sxs-lookup"><span data-stu-id="a8946-112">Troubleshooting line-of-business applications</span></span>
    - <span data-ttu-id="a8946-113">Utilisation d’une solution de contournement pour corriger quelque chose qui doit fonctionner par conception (par exemple, l’activation de BitLocker ou le temps système non mis à jour)</span><span class="sxs-lookup"><span data-stu-id="a8946-113">Using a workaround to correct something that should function by design (such as BitLocker activation or system time not updating)</span></span>
    - <span data-ttu-id="a8946-114">Élévation de la fonction Gestionnaire de périphériques pour faire des opérations telles que les pilotes de mise à jour, désinstaller un appareil ou analyser les nouvelles modifications</span><span class="sxs-lookup"><span data-stu-id="a8946-114">Elevating Device Manager to do things like update drivers, uninstall a device, or scan for new changes</span></span>

- <span data-ttu-id="a8946-115">**Les actions qui ne sont pas recommandées sont** les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a8946-115">**Actions that aren't recommended** include the following:</span></span>
    - <span data-ttu-id="a8946-116">Installation de logiciels ou de navigateurs</span><span class="sxs-lookup"><span data-stu-id="a8946-116">Installing software or browsers</span></span>
    - <span data-ttu-id="a8946-117">Installation de pilotes en dehors des paramètres Windows, y compris ceux des périphériques</span><span class="sxs-lookup"><span data-stu-id="a8946-117">Installing drivers outside of Windows settings, including those for peripherals</span></span>
    - <span data-ttu-id="a8946-118">Installation de .msi ou de .exe fichiers</span><span class="sxs-lookup"><span data-stu-id="a8946-118">Installing .msi or .exe files</span></span>
    - <span data-ttu-id="a8946-119">Installation de Windows fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="a8946-119">Installing Windows features</span></span>

- <span data-ttu-id="a8946-120">**Les actions qui ne sont pas prises en charge sont** les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a8946-120">**Actions that aren't supported** include the following:</span></span>
    - <span data-ttu-id="a8946-121">Installation de logiciels ou de fonctionnalités en conflit avec Microsoft Manged Desktop de sécurité ou de gestion ou des opérations</span><span class="sxs-lookup"><span data-stu-id="a8946-121">Installing software or features that conflict with Microsoft Managed Desktop security or management capabilities or operations</span></span>
    - <span data-ttu-id="a8946-122">Désactivation d’une Windows requise pour les Microsoft Manged Desktop, telle que BitLocker</span><span class="sxs-lookup"><span data-stu-id="a8946-122">Disabling a Windows feature that is required for Microsoft Managed Desktop, such as BitLocker</span></span>
    - <span data-ttu-id="a8946-123">Modification des paramètres gérés par votre organisation</span><span class="sxs-lookup"><span data-stu-id="a8946-123">Modifying settings managed by your org</span></span>

### <a name="to-request-elevation"></a><span data-ttu-id="a8946-124">Pour demander une élévation</span><span class="sxs-lookup"><span data-stu-id="a8946-124">To request elevation</span></span>

1. <span data-ttu-id="a8946-125">Go to the portal at [https://aka.ms/mmdelevationrequest](https://aka.ms/mmdelevationrequest) and sign in with your Azure Active Directory credentials.</span><span class="sxs-lookup"><span data-stu-id="a8946-125">Go to the portal at [https://aka.ms/mmdelevationrequest](https://aka.ms/mmdelevationrequest) and sign in with your Azure Active Directory credentials.</span></span>
2. <span data-ttu-id="a8946-126">Sélectionnez **Nouvelle demande d’élévation.**</span><span class="sxs-lookup"><span data-stu-id="a8946-126">Select **New elevation request**.</span></span>
3. <span data-ttu-id="a8946-127">Fournissez les détails ci-après :</span><span class="sxs-lookup"><span data-stu-id="a8946-127">Provide these details:</span></span>
    - <span data-ttu-id="a8946-128">**ID de ticket de support** à partir de votre propre système de tickets de support.</span><span class="sxs-lookup"><span data-stu-id="a8946-128">**Support ticket ID** from your own support ticketing system.</span></span>
    - <span data-ttu-id="a8946-129">**Nom de l’appareil**: entrez le numéro de série de l’appareil, puis sélectionnez l’appareil dans le menu.</span><span class="sxs-lookup"><span data-stu-id="a8946-129">**Device name**: enter the device serial number and then select the device from the menu.</span></span>
    - <span data-ttu-id="a8946-130">**Catégorie**: sélectionnez la catégorie qui correspond le mieux à votre problème.</span><span class="sxs-lookup"><span data-stu-id="a8946-130">**Category**: Select the category that best fits your issue.</span></span> <span data-ttu-id="a8946-131">Si aucune option ne semble proche, sélectionnez **Autre** et fournissez plus d’informations dans les **champs** Titre et Plan **d’action.**</span><span class="sxs-lookup"><span data-stu-id="a8946-131">If no option seems close, then select **Other** and provide more info in the **Title** and **Plan of action** fields.</span></span> <span data-ttu-id="a8946-132">Il est préférable de sélectionner une catégorie si possible.</span><span class="sxs-lookup"><span data-stu-id="a8946-132">It's best to select a category if at all possible.</span></span>
    - <span data-ttu-id="a8946-133">**Sous-catégorie :** sélectionnez celle qui répond le mieux au problème.</span><span class="sxs-lookup"><span data-stu-id="a8946-133">**Subcategory**: Select the one that best fits the issue.</span></span> <span data-ttu-id="a8946-134">Si aucune option ne semble proche, sélectionnez **Autre** et fournissez une brève description dans **titre**.</span><span class="sxs-lookup"><span data-stu-id="a8946-134">If no option seems close, then select **Other** and provide a short description in **Title**.</span></span> <span data-ttu-id="a8946-135">Dans **le plan d’action,** fournissez les étapes de résolution des problèmes que vous prévoyez d’suivre une fois l’élévation accordée.</span><span class="sxs-lookup"><span data-stu-id="a8946-135">In **Plan of action**, provide the troubleshooting steps you plan to take once elevation is granted.</span></span>
4. <span data-ttu-id="a8946-136">Sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="a8946-136">Select **Submit**.</span></span>


## <a name="escalation-requests"></a><span data-ttu-id="a8946-137">Demandes d’escalade</span><span class="sxs-lookup"><span data-stu-id="a8946-137">Escalation requests</span></span>


<span data-ttu-id="a8946-138">Si vous devez faire [une escalade d’un](../service-description/user-support.md#escalation-portal) problème à Microsoft, suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a8946-138">If you need to [escalate](../service-description/user-support.md#escalation-portal) an issue to Microsoft, follow these steps:</span></span>

1. <span data-ttu-id="a8946-139">Go to the portal at [https://aka.ms/mmdelevationrequest](https://aka.ms/mmdelevationrequest) and sign in with your Azure Active Directory credentials.</span><span class="sxs-lookup"><span data-stu-id="a8946-139">Go to the portal at [https://aka.ms/mmdelevationrequest](https://aka.ms/mmdelevationrequest) and sign in with your Azure Active Directory credentials.</span></span>
2. <span data-ttu-id="a8946-140">Sélectionnez **Demandes d’escalade,** puis Nouvelle **demande d’escalade.**</span><span class="sxs-lookup"><span data-stu-id="a8946-140">Select **Escalation requests**, and then select **New escalation request**.</span></span>
3. <span data-ttu-id="a8946-141">Fournissez les détails ci-après :</span><span class="sxs-lookup"><span data-stu-id="a8946-141">Provide these details:</span></span>
    - <span data-ttu-id="a8946-142">**Catégorie**: sélectionnez la catégorie qui correspond le mieux à votre problème.</span><span class="sxs-lookup"><span data-stu-id="a8946-142">**Category**: Select the category that best fits your issue.</span></span>
    - <span data-ttu-id="a8946-143">**Titre**: fournissez une brève description.</span><span class="sxs-lookup"><span data-stu-id="a8946-143">**Title**: Provide a very brief description.</span></span>
    - <span data-ttu-id="a8946-144">**Description**: ajoutez tous les détails supplémentaires qui pourraient aider notre équipe à comprendre le problème.</span><span class="sxs-lookup"><span data-stu-id="a8946-144">**Description**: Add any additional details that could help our team understand the problem.</span></span> <span data-ttu-id="a8946-145">Si vous devez joindre des fichiers, vous pouvez le faire en revenir à la demande après l’avoir soumis.</span><span class="sxs-lookup"><span data-stu-id="a8946-145">If you need to attach files, you can do that by coming back to the request after you submit it.</span></span>
    - <span data-ttu-id="a8946-146">**Informations de contact principales**: fournissez des informations sur la façon de contacter la personne principale responsable de l’collaboration avec notre équipe.</span><span class="sxs-lookup"><span data-stu-id="a8946-146">**Primary contact information**: Provide info about how to contact the main person responsible for working with our team.</span></span>
4. <span data-ttu-id="a8946-147">Sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="a8946-147">Select **Submit**.</span></span>
5. <span data-ttu-id="a8946-148">Revenir sur le ticket dans le même portail pour interagir avec notre équipe.</span><span class="sxs-lookup"><span data-stu-id="a8946-148">Revisit the ticket in the same portal to interact with our team.</span></span>

> [!NOTE]
> <span data-ttu-id="a8946-149">Seuls les problèmes de gravité C peuvent être escalades via ce chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="a8946-149">Only Severity C issues can be escalated through this path.</span></span> <span data-ttu-id="a8946-150">Pour d’autres problèmes, contactez votre administrateur informatique pour déposer la demande via le portail d’administration.</span><span class="sxs-lookup"><span data-stu-id="a8946-150">For other issues, contact your IT admin to file the request through the Admin portal.</span></span>