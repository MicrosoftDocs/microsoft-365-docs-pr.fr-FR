---
title: Utiliser le contrôle d’application
description: ''
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.author: jaimeo
manager: laurawi
audience: ITpro
ms.topic: article
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.openlocfilehash: 31cc897fe28f557a65cba9c99e5dcecbf7c2b0e5
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50917639"
---
# <a name="work-with-app-control"></a><span data-ttu-id="a76ef-103">Utiliser le contrôle d’application</span><span class="sxs-lookup"><span data-stu-id="a76ef-103">Work with app control</span></span>

<span data-ttu-id="a76ef-104">Une fois que le contrôle d’application a été déployé dans votre environnement, vous et Bureau géré Microsoft opérations ont des responsabilités en cours.</span><span class="sxs-lookup"><span data-stu-id="a76ef-104">Once app control has been deployed in your environment, both you and Microsoft Managed Desktop Operations have ongoing responsibilities.</span></span> <span data-ttu-id="a76ef-105">Par exemple, vous pouvez ajouter une nouvelle application dans l’environnement ou ajouter (ou supprimer) un signataire approuvé.</span><span class="sxs-lookup"><span data-stu-id="a76ef-105">For example, you might want to add a new app in the environment or add (or remove) a trusted signer.</span></span> <span data-ttu-id="a76ef-106">Pour améliorer la sécurité, toutes les applications doivent être signées par code avant de les publier pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a76ef-106">To improve security, all apps should be code-signed before you release them to users.</span></span> <span data-ttu-id="a76ef-107">Les détails de l’éditeur d’une application incluent des informations sur le signataire.</span><span class="sxs-lookup"><span data-stu-id="a76ef-107">An app's publisher details includes information about the signer.</span></span>


## <a name="add-a-new-app"></a><span data-ttu-id="a76ef-108">Ajout d’une nouvelle application</span><span class="sxs-lookup"><span data-stu-id="a76ef-108">Add a new app</span></span>

<span data-ttu-id="a76ef-109">Pour ajouter une nouvelle application, suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a76ef-109">To add a new app, follow these steps:</span></span>

1. <span data-ttu-id="a76ef-110">Ajoutez l’application [à Microsoft Intune](/mem/intune/apps/apps-win32-app-management).</span><span class="sxs-lookup"><span data-stu-id="a76ef-110">Add the app to [Microsoft Intune](/mem/intune/apps/apps-win32-app-management).</span></span>
2. <span data-ttu-id="a76ef-111">Déployez l’application sur n’importe quel appareil de l’anneau Test.</span><span class="sxs-lookup"><span data-stu-id="a76ef-111">Deploy the app to any device in the Test ring.</span></span> 
3. <span data-ttu-id="a76ef-112">Testez votre application en fonction de vos processus d’entreprise standard.</span><span class="sxs-lookup"><span data-stu-id="a76ef-112">Test your app according to your standard business processes.</span></span> 
4. <span data-ttu-id="a76ef-113">Consultez l’Observateur d’événements sous Journaux des applications et des **services\Microsoft\Windows\AppLocker**, à la recherche d’événements **8003** ou **8006.**</span><span class="sxs-lookup"><span data-stu-id="a76ef-113">Check Event Viewer under **Application and Services Logs\Microsoft\Windows\AppLocker**, looking for any **8003** or **8006** events.</span></span> <span data-ttu-id="a76ef-114">Ces événements indiquent que l’application sera bloquée.</span><span class="sxs-lookup"><span data-stu-id="a76ef-114">These events indicate that the app would be blocked.</span></span> <span data-ttu-id="a76ef-115">Pour plus d’informations sur tous les événements App Locker et leurs significations, voir Utilisation de l’Observateur d’événements [avec AppLocker.](/windows/security/threat-protection/windows-defender-application-control/applocker/using-event-viewer-with-applocker)</span><span class="sxs-lookup"><span data-stu-id="a76ef-115">For more information about all App Locker events and their meanings, see [Using Event Viewer with AppLocker](/windows/security/threat-protection/windows-defender-application-control/applocker/using-event-viewer-with-applocker).</span></span>
5. <span data-ttu-id="a76ef-116">Si vous trouvez l’un de ces événements, ouvrez une demande de signataire avec Bureau géré Microsoft Operations.</span><span class="sxs-lookup"><span data-stu-id="a76ef-116">If you find any of these events, open a signer request with Microsoft Managed Desktop Operations.</span></span>

## <a name="add-or-remove-a-trusted-signer"></a><span data-ttu-id="a76ef-117">Ajouter (ou supprimer) un signataire approuvé</span><span class="sxs-lookup"><span data-stu-id="a76ef-117">Add (or remove) a trusted signer</span></span>

<span data-ttu-id="a76ef-118">Lorsque vous ouvrez une demande de signataire, vous devez d’abord fournir des détails importants sur l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="a76ef-118">When you open a signer request, you'll need to provide some important publisher details first.</span></span> <span data-ttu-id="a76ef-119">Ensuite, suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a76ef-119">Then follow these steps:</span></span>

1. <span data-ttu-id="a76ef-120">[Rassemblez les détails de l’éditeur.](#gather-publisher-details)</span><span class="sxs-lookup"><span data-stu-id="a76ef-120">[Gather publisher details](#gather-publisher-details).</span></span>
2. <span data-ttu-id="a76ef-121">Ouvrez un ticket avec Bureau géré Microsoft Operations pour demander la règle du signataire et inclure les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="a76ef-121">Open a ticket with Microsoft Managed Desktop Operations to request the signer rule and include following details:</span></span>  
    - <span data-ttu-id="a76ef-122">Nom de l’application</span><span class="sxs-lookup"><span data-stu-id="a76ef-122">Application name</span></span> 
    - <span data-ttu-id="a76ef-123">Version de l’application</span><span class="sxs-lookup"><span data-stu-id="a76ef-123">Application version</span></span> 
    - <span data-ttu-id="a76ef-124">Description</span><span class="sxs-lookup"><span data-stu-id="a76ef-124">Description</span></span> 
    - <span data-ttu-id="a76ef-125">Type de modification (« ajouter » ou « supprimer »)</span><span class="sxs-lookup"><span data-stu-id="a76ef-125">Change type ("add" or "remove")</span></span>  
    - <span data-ttu-id="a76ef-126">Publisher détails détaillés (par exemple : « O= <publisher name> ,L= <location> ,S=State,C=Country »)</span><span class="sxs-lookup"><span data-stu-id="a76ef-126">Publisher details (for example: “O=<publisher name>,L=<location>,S=State,C=Country”)</span></span> 

> [!NOTE]
> <span data-ttu-id="a76ef-127">Pour supprimer l’confiance pour une application, suivez les mêmes étapes, mais définissez **le type de modification** à *supprimer.*</span><span class="sxs-lookup"><span data-stu-id="a76ef-127">To remove trust for an app, follow the same steps, but set **Change type** to *remove*.</span></span>

<span data-ttu-id="a76ef-128">Les opérations déploieront progressivement des stratégies dans des groupes de déploiement en suivant cette planification :</span><span class="sxs-lookup"><span data-stu-id="a76ef-128">Operations will progressively deploy policies to deployment groups following this schedule:</span></span>


|<span data-ttu-id="a76ef-129">Groupe de déploiement</span><span class="sxs-lookup"><span data-stu-id="a76ef-129">Deployment group</span></span>  |<span data-ttu-id="a76ef-130">Type de stratégie</span><span class="sxs-lookup"><span data-stu-id="a76ef-130">Policy type</span></span>  |<span data-ttu-id="a76ef-131">Calendrier</span><span class="sxs-lookup"><span data-stu-id="a76ef-131">Timing</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="a76ef-132">Tester</span><span class="sxs-lookup"><span data-stu-id="a76ef-132">Test</span></span>     |  <span data-ttu-id="a76ef-133">Audit</span><span class="sxs-lookup"><span data-stu-id="a76ef-133">Audit</span></span>       |  <span data-ttu-id="a76ef-134">Jour 0</span><span class="sxs-lookup"><span data-stu-id="a76ef-134">Day 0</span></span>       |
|<span data-ttu-id="a76ef-135">Premier</span><span class="sxs-lookup"><span data-stu-id="a76ef-135">First</span></span>     | <span data-ttu-id="a76ef-136">Enforced</span><span class="sxs-lookup"><span data-stu-id="a76ef-136">Enforced</span></span>        | <span data-ttu-id="a76ef-137">Jour 1</span><span class="sxs-lookup"><span data-stu-id="a76ef-137">Day 1</span></span>        |
|<span data-ttu-id="a76ef-138">Rapide</span><span class="sxs-lookup"><span data-stu-id="a76ef-138">Fast</span></span>     | <span data-ttu-id="a76ef-139">Enforced</span><span class="sxs-lookup"><span data-stu-id="a76ef-139">Enforced</span></span>        |  <span data-ttu-id="a76ef-140">Jour 2</span><span class="sxs-lookup"><span data-stu-id="a76ef-140">Day 2</span></span>       |
|<span data-ttu-id="a76ef-141">Larges</span><span class="sxs-lookup"><span data-stu-id="a76ef-141">Broad</span></span>     | <span data-ttu-id="a76ef-142">Enforced</span><span class="sxs-lookup"><span data-stu-id="a76ef-142">Enforced</span></span>        |  <span data-ttu-id="a76ef-143">Jour 3</span><span class="sxs-lookup"><span data-stu-id="a76ef-143">Day 3</span></span>       |


<span data-ttu-id="a76ef-144">Vous pouvez suspendre ou revenir en arrière le déploiement à tout moment pendant le déploiement.</span><span class="sxs-lookup"><span data-stu-id="a76ef-144">You can pause or roll back the deployment at any time during the rollout.</span></span> <span data-ttu-id="a76ef-145">Pour ce faire, ouvrez une autre demande de service avec Operations.</span><span class="sxs-lookup"><span data-stu-id="a76ef-145">To do this, open another service request with Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="a76ef-146">Si vous suspendez la publication d’une règle de signataire, cette règle doit être soit mise à jour, soit terminée avant qu’un autre déploiement puisse démarrer.</span><span class="sxs-lookup"><span data-stu-id="a76ef-146">If you pause the release of a signer rule, that rule must be either rolled back or completed before another rollout can start.</span></span>

## <a name="gather-publisher-details"></a><span data-ttu-id="a76ef-147">Collecter les détails de l’éditeur</span><span class="sxs-lookup"><span data-stu-id="a76ef-147">Gather publisher details</span></span>

<span data-ttu-id="a76ef-148">Pour accéder aux données d’éditeur d’une application, suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a76ef-148">To access the publisher data for an app, follow these steps:</span></span>

1. <span data-ttu-id="a76ef-149">Recherchez un Bureau géré Microsoft de test sur l’anneau test sur la stratégie du mode Audit appliquée.</span><span class="sxs-lookup"><span data-stu-id="a76ef-149">Find a Microsoft Managed Desktop device in the Test ring that has an Audit Mode policy applied.</span></span> 
2. <span data-ttu-id="a76ef-150">Essayez d’installer l’application sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a76ef-150">Attempt to install the app on the device.</span></span>
3. <span data-ttu-id="a76ef-151">Ouvrez l’Observateur d’événements sur cet appareil.</span><span class="sxs-lookup"><span data-stu-id="a76ef-151">Open Event Viewer on that device.</span></span> 
4. <span data-ttu-id="a76ef-152">Dans l’Observateur d’événements, accédez à Journaux des applications et des **services\Microsoft\Windows,** puis sélectionnez **AppLocker.**</span><span class="sxs-lookup"><span data-stu-id="a76ef-152">In Event Viewer, navigate to **Application and Services Logs\Microsoft\Windows**, and then select **AppLocker**.</span></span> 
5. <span data-ttu-id="a76ef-153">Recherchez **un événement 8003** ou **8006,** puis copiez les informations de l’événement :</span><span class="sxs-lookup"><span data-stu-id="a76ef-153">Find any **8003** or **8006** event, and then copy information from the event:</span></span> 
    - <span data-ttu-id="a76ef-154">Nom de l’application</span><span class="sxs-lookup"><span data-stu-id="a76ef-154">Application name</span></span> 
    - <span data-ttu-id="a76ef-155">Version de l’application</span><span class="sxs-lookup"><span data-stu-id="a76ef-155">Application version</span></span> 
    - <span data-ttu-id="a76ef-156">Description</span><span class="sxs-lookup"><span data-stu-id="a76ef-156">Description</span></span> 
    - <span data-ttu-id="a76ef-157">Publisher détails détaillés (par exemple : « O= <publisher name> , L= <location> , S=State, C=Country »)</span><span class="sxs-lookup"><span data-stu-id="a76ef-157">Publisher details (for example: “O=<publisher name>, L=<location>, S=State, C=Country”)</span></span>