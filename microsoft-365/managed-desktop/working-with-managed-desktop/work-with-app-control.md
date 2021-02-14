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
ms.openlocfilehash: 0b76a14a30caeb75cfdcb8acc5715fe6710e0625
ms.sourcegitcommit: abf63669daf12993ad3353e4b578f41c8910b20f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2020
ms.locfileid: "47289458"
---
# <a name="work-with-app-control"></a><span data-ttu-id="4d1bd-103">Utiliser le contrôle d’application</span><span class="sxs-lookup"><span data-stu-id="4d1bd-103">Work with app control</span></span>

<span data-ttu-id="4d1bd-104">Une fois que le contrôle d’application a été déployé dans votre environnement, vous et les opérations Bureau géré Microsoft avez des responsabilités en cours.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-104">Once app control has been deployed in your environment, both you and Microsoft Managed Desktop Operations have ongoing responsibilities.</span></span> <span data-ttu-id="4d1bd-105">Par exemple, vous pouvez ajouter une nouvelle application dans l’environnement ou ajouter (ou supprimer) un signataire approuvé.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-105">For example, you might want to add a new app in the environment or add (or remove) a trusted signer.</span></span> <span data-ttu-id="4d1bd-106">Pour améliorer la sécurité, toutes les applications doivent être signées par code avant de les publier pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-106">To improve security, all apps should be code-signed before you release them to users.</span></span> <span data-ttu-id="4d1bd-107">Les détails de l’éditeur d’une application incluent des informations sur le signataire.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-107">An app's publisher details includes information about the signer.</span></span>


## <a name="add-a-new-app"></a><span data-ttu-id="4d1bd-108">Ajout d’une nouvelle application</span><span class="sxs-lookup"><span data-stu-id="4d1bd-108">Add a new app</span></span>

<span data-ttu-id="4d1bd-109">Pour ajouter une nouvelle application, suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4d1bd-109">To add a new app, follow these steps:</span></span>

1. <span data-ttu-id="4d1bd-110">Ajoutez l’application [à Microsoft Intune.](https://docs.microsoft.com/mem/intune/apps/apps-win32-app-management)</span><span class="sxs-lookup"><span data-stu-id="4d1bd-110">Add the app to [Microsoft Intune](https://docs.microsoft.com/mem/intune/apps/apps-win32-app-management).</span></span>
2. <span data-ttu-id="4d1bd-111">Déployez l’application sur n’importe quel appareil de l’anneau Test.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-111">Deploy the app to any device in the Test ring.</span></span> 
3. <span data-ttu-id="4d1bd-112">Testez votre application en fonction de vos processus d’entreprise standard.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-112">Test your app according to your standard business processes.</span></span> 
4. <span data-ttu-id="4d1bd-113">Vérifiez l’Observateur d’événements sous Journaux des applications et des **services\Microsoft\Windows\AppLocker**, en cherchant les **événements 8003** ou **8006.**</span><span class="sxs-lookup"><span data-stu-id="4d1bd-113">Check Event Viewer under **Application and Services Logs\Microsoft\Windows\AppLocker**, looking for any **8003** or **8006** events.</span></span> <span data-ttu-id="4d1bd-114">Ces événements indiquent que l’application sera bloquée.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-114">These events indicate that the app would be blocked.</span></span> <span data-ttu-id="4d1bd-115">Pour plus d’informations sur tous les événements App Locker et leurs significations, voir Utilisation de l’Observateur d’événements [avec AppLocker.](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-application-control/applocker/using-event-viewer-with-applocker)</span><span class="sxs-lookup"><span data-stu-id="4d1bd-115">For more information about all App Locker events and their meanings, see [Using Event Viewer with AppLocker](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-application-control/applocker/using-event-viewer-with-applocker).</span></span>
5. <span data-ttu-id="4d1bd-116">Si vous trouvez l’un de ces événements, ouvrez une demande de signataire avec les opérations de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-116">If you find any of these events, open a signer request with Microsoft Managed Desktop Operations.</span></span>

## <a name="add-or-remove-a-trusted-signer"></a><span data-ttu-id="4d1bd-117">Ajouter (ou supprimer) un signataire approuvé</span><span class="sxs-lookup"><span data-stu-id="4d1bd-117">Add (or remove) a trusted signer</span></span>

<span data-ttu-id="4d1bd-118">Lorsque vous ouvrez une demande de signataire, vous devez d’abord fournir des détails importants sur l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-118">When you open a signer request, you'll need to provide some important publisher details first.</span></span> <span data-ttu-id="4d1bd-119">Ensuite, suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4d1bd-119">Then follow these steps:</span></span>

1. <span data-ttu-id="4d1bd-120">[Rassemblez les détails de l’éditeur.](#gather-publisher-details)</span><span class="sxs-lookup"><span data-stu-id="4d1bd-120">[Gather publisher details](#gather-publisher-details).</span></span>
2. <span data-ttu-id="4d1bd-121">Ouvrez un ticket avec microsoft Managed Desktop Operations pour demander la règle du signataire et inclure les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="4d1bd-121">Open a ticket with Microsoft Managed Desktop Operations to request the signer rule and include following details:</span></span>  
    - <span data-ttu-id="4d1bd-122">Nom de l’application</span><span class="sxs-lookup"><span data-stu-id="4d1bd-122">Application name</span></span> 
    - <span data-ttu-id="4d1bd-123">Version de l’application</span><span class="sxs-lookup"><span data-stu-id="4d1bd-123">Application version</span></span> 
    - <span data-ttu-id="4d1bd-124">Description</span><span class="sxs-lookup"><span data-stu-id="4d1bd-124">Description</span></span> 
    - <span data-ttu-id="4d1bd-125">Type de modification (« ajouter » ou « supprimer »)</span><span class="sxs-lookup"><span data-stu-id="4d1bd-125">Change type ("add" or "remove")</span></span>  
    - <span data-ttu-id="4d1bd-126">Détails de l’éditeur (par exemple : « O= <publisher name> ,L= <location> ,S=State,C=Country »)</span><span class="sxs-lookup"><span data-stu-id="4d1bd-126">Publisher details (for example: “O=<publisher name>,L=<location>,S=State,C=Country”)</span></span> 

> [!NOTE]
> <span data-ttu-id="4d1bd-127">Pour supprimer l’confiance d’une application, suivez les mêmes étapes, mais définissez **le type de modification** à *supprimer.*</span><span class="sxs-lookup"><span data-stu-id="4d1bd-127">To remove trust for an app, follow the same steps, but set **Change type** to *remove*.</span></span>

<span data-ttu-id="4d1bd-128">Les opérations déploieront progressivement des stratégies dans des groupes de déploiement en suivant cette planification :</span><span class="sxs-lookup"><span data-stu-id="4d1bd-128">Operations will progressively deploy policies to deployment groups following this schedule:</span></span>


|<span data-ttu-id="4d1bd-129">Groupe de déploiement</span><span class="sxs-lookup"><span data-stu-id="4d1bd-129">Deployment group</span></span>  |<span data-ttu-id="4d1bd-130">Type de stratégie</span><span class="sxs-lookup"><span data-stu-id="4d1bd-130">Policy type</span></span>  |<span data-ttu-id="4d1bd-131">Calendrier</span><span class="sxs-lookup"><span data-stu-id="4d1bd-131">Timing</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="4d1bd-132">Tester</span><span class="sxs-lookup"><span data-stu-id="4d1bd-132">Test</span></span>     |  <span data-ttu-id="4d1bd-133">Audit</span><span class="sxs-lookup"><span data-stu-id="4d1bd-133">Audit</span></span>       |  <span data-ttu-id="4d1bd-134">Jour 0</span><span class="sxs-lookup"><span data-stu-id="4d1bd-134">Day 0</span></span>       |
|<span data-ttu-id="4d1bd-135">Premier</span><span class="sxs-lookup"><span data-stu-id="4d1bd-135">First</span></span>     | <span data-ttu-id="4d1bd-136">Enforced</span><span class="sxs-lookup"><span data-stu-id="4d1bd-136">Enforced</span></span>        | <span data-ttu-id="4d1bd-137">Jour 1</span><span class="sxs-lookup"><span data-stu-id="4d1bd-137">Day 1</span></span>        |
|<span data-ttu-id="4d1bd-138">Rapide</span><span class="sxs-lookup"><span data-stu-id="4d1bd-138">Fast</span></span>     | <span data-ttu-id="4d1bd-139">Enforced</span><span class="sxs-lookup"><span data-stu-id="4d1bd-139">Enforced</span></span>        |  <span data-ttu-id="4d1bd-140">Jour 2</span><span class="sxs-lookup"><span data-stu-id="4d1bd-140">Day 2</span></span>       |
|<span data-ttu-id="4d1bd-141">Larges</span><span class="sxs-lookup"><span data-stu-id="4d1bd-141">Broad</span></span>     | <span data-ttu-id="4d1bd-142">Enforced</span><span class="sxs-lookup"><span data-stu-id="4d1bd-142">Enforced</span></span>        |  <span data-ttu-id="4d1bd-143">Jour 3</span><span class="sxs-lookup"><span data-stu-id="4d1bd-143">Day 3</span></span>       |


<span data-ttu-id="4d1bd-144">Vous pouvez suspendre ou revenir en arrière le déploiement à tout moment pendant le déploiement.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-144">You can pause or roll back the deployment at any time during the rollout.</span></span> <span data-ttu-id="4d1bd-145">Pour ce faire, ouvrez une autre demande de service avec Operations.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-145">To do this, open another service request with Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="4d1bd-146">Si vous suspendez la publication d’une règle de signataire, cette règle doit être soit mise à jour, soit terminée avant qu’un autre déploiement puisse démarrer.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-146">If you pause the release of a signer rule, that rule must be either rolled back or completed before another rollout can start.</span></span>

## <a name="gather-publisher-details"></a><span data-ttu-id="4d1bd-147">Collecter les détails de l’éditeur</span><span class="sxs-lookup"><span data-stu-id="4d1bd-147">Gather publisher details</span></span>

<span data-ttu-id="4d1bd-148">Pour accéder aux données d’éditeur d’une application, suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4d1bd-148">To access the publisher data for an app, follow these steps:</span></span>

1. <span data-ttu-id="4d1bd-149">Recherchez un appareil bureau géré Microsoft dans l’anneau Test sur la stratégie de mode Audit appliquée.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-149">Find a Microsoft Managed Desktop device in the Test ring that has an Audit Mode policy applied.</span></span> 
2. <span data-ttu-id="4d1bd-150">Essayez d’installer l’application sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-150">Attempt to install the app on the device.</span></span>
3. <span data-ttu-id="4d1bd-151">Ouvrez l’Observateur d’événements sur cet appareil.</span><span class="sxs-lookup"><span data-stu-id="4d1bd-151">Open Event Viewer on that device.</span></span> 
4. <span data-ttu-id="4d1bd-152">Dans l’Observateur d’événements, accédez à Journaux des applications et **des services\Microsoft\Windows,** puis sélectionnez **AppLocker.**</span><span class="sxs-lookup"><span data-stu-id="4d1bd-152">In Event Viewer, navigate to **Application and Services Logs\Microsoft\Windows**, and then select **AppLocker**.</span></span> 
5. <span data-ttu-id="4d1bd-153">Recherchez **un événement 8003** ou **8006,** puis copiez les informations de l’événement :</span><span class="sxs-lookup"><span data-stu-id="4d1bd-153">Find any **8003** or **8006** event, and then copy information from the event:</span></span> 
    - <span data-ttu-id="4d1bd-154">Nom de l’application</span><span class="sxs-lookup"><span data-stu-id="4d1bd-154">Application name</span></span> 
    - <span data-ttu-id="4d1bd-155">Version de l’application</span><span class="sxs-lookup"><span data-stu-id="4d1bd-155">Application version</span></span> 
    - <span data-ttu-id="4d1bd-156">Description</span><span class="sxs-lookup"><span data-stu-id="4d1bd-156">Description</span></span> 
    - <span data-ttu-id="4d1bd-157">Détails de l’éditeur (par exemple : « O= <publisher name> , L= <location> , S=State, C=Country »)</span><span class="sxs-lookup"><span data-stu-id="4d1bd-157">Publisher details (for example: “O=<publisher name>, L=<location>, S=State, C=Country”)</span></span> 
