---
title: Utiliser Microsoft Teams classes avec tableau noir
ms.author: v-cichur
author: cichur
manager: serdars
ms.reviewer: sovaish
audience: admin
ms.topic: article
ms.service: o365-administration
f1.keywords:
- CSH
ms.collection: M365-modern-desktop
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
description: Intégrer Microsoft Teams classes de gestion dans votre système Learning gestion des données
ms.openlocfilehash: 3c574184c48ae064d425ed98dbc391b8f5bcf7e0
ms.sourcegitcommit: a4c93a4c7d7db08fe3b032b58d5c7dbbb9476e90
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2021
ms.locfileid: "53256959"
---
# <a name="use-microsoft-teams-classes-with-blackboard"></a><span data-ttu-id="f0ab5-103">Utiliser Microsoft Teams classes avec tableau noir</span><span class="sxs-lookup"><span data-stu-id="f0ab5-103">Use Microsoft Teams classes with Blackboard</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f0ab5-104">Certaines informations ont trait à un produit préalablement publié, qui peut être modifié de manière significative avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-104">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f0ab5-105">Microsoft n’offre aucune garantie, explicite ou implicite, concernant les informations fournies ici.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="f0ab5-106">Microsoft Teams classes est une application Learning Tools Interoperability (LTI) qui permet aux enseignants et aux étudiants de naviguer facilement entre leur système de gestion Learning (LMS) et leur Teams.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-106">Microsoft Teams classes is a Learning Tools Interoperability (LTI) app that helps educators and students easily navigate between their Learning Management System (LMS) and Teams.</span></span> <span data-ttu-id="f0ab5-107">Les utilisateurs peuvent accéder à leurs équipes de cours associées à leur cours directement à partir de leur LMS.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-107">Users can access their class teams associated with their course directly from within their LMS.</span></span>

## <a name="approve-the-app-in-the-microsoft-azure-tenant"></a><span data-ttu-id="f0ab5-108">Approuver l’application dans le Microsoft Azure client</span><span class="sxs-lookup"><span data-stu-id="f0ab5-108">Approve the app in the Microsoft Azure tenant</span></span>

<span data-ttu-id="f0ab5-109">Les tâches suivantes sont effectuées par l’administrateur Microsoft Office 365 et l’administrateur Blackboard Learn Ultra.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-109">The following tasks are completed by the Microsoft Office 365 admin and the Blackboard Learn Ultra admin.</span></span>

<span data-ttu-id="f0ab5-110">Avant de gérer l’intégration dans Blackboard Learn Ultra, l’administrateur Microsoft Office 365 doit approuver le **Teams MSFT** pour l’application Learn Ultra Azure pour le client Microsoft Azure de l’établissement.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-110">Before managing the integration within Blackboard Learn Ultra, the Microsoft Office 365 admin must approve the Blackboard **MSFT Teams for Learn Ultra Azure** app for the institution’s Microsoft Azure tenant.</span></span>

1. <span data-ttu-id="f0ab5-111">Recherchez votre ID de locataire Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-111">Find your Microsoft Tenant ID.</span></span> <span data-ttu-id="f0ab5-112">Découvrez [comment trouver le client.](/azure/active-directory/fundamentals/active-directory-how-to-find-tenant)</span><span class="sxs-lookup"><span data-stu-id="f0ab5-112">See [how to find the tenant](/azure/active-directory/fundamentals/active-directory-how-to-find-tenant).</span></span>

2. <span data-ttu-id="f0ab5-113">Redirigez le point de terminaison de consentement de l’administrateur de la plateforme d’identités Microsoft en fonction de l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="f0ab5-113">Redirect the Microsoft Identity Platform Admin Consent Endpoint according to the following example:</span></span>

   `https://login.microsoftonline.com/{tenant}/adminconsent?client_id=2d94989f-457a-47c1-a637-e75acdb11568`

   > [!NOTE]
   > <span data-ttu-id="f0ab5-114">Remplacez {tenant} par l’ID de client Microsoft de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-114">Replace {tenant} with your organization’s Microsoft tenant ID.</span></span>

## <a name="register-the-integration-apps"></a><span data-ttu-id="f0ab5-115">Inscrire les applications d’intégration</span><span class="sxs-lookup"><span data-stu-id="f0ab5-115">Register the integration apps</span></span>

<span data-ttu-id="f0ab5-116">En tant qu’administrateur Blackboard Learn Ultra, vous devez inscrire 2 applications d’intégration LTI 1.3 dans votre environnement de test :</span><span class="sxs-lookup"><span data-stu-id="f0ab5-116">As a Blackboard Learn Ultra admin, you'll need to register 2 LTI 1.3 integration apps within your Test environment:</span></span>

- <span data-ttu-id="f0ab5-117">Intégration de la classe Blackboard Learn Teams prise en charge de la synchronisation des listes de classes</span><span class="sxs-lookup"><span data-stu-id="f0ab5-117">The Blackboard Learn Class Teams integration to support the roster sync</span></span>

- <span data-ttu-id="f0ab5-118">Application LTI Microsoft Teams l’équipe de la classe</span><span class="sxs-lookup"><span data-stu-id="f0ab5-118">The Microsoft Teams class team LTI app</span></span>

1. <span data-ttu-id="f0ab5-119">Notez les ID de client LTI suivants pour les deux applications :</span><span class="sxs-lookup"><span data-stu-id="f0ab5-119">Make a note of the following LTI Client IDs for both Apps:</span></span>

    - <span data-ttu-id="f0ab5-120">Tableau noir - f1561daa-1b21-4693-ba90-6c55f1a0eb41</span><span class="sxs-lookup"><span data-stu-id="f0ab5-120">Blackboard - f1561daa-1b21-4693-ba90-6c55f1a0eb41</span></span>

    - <span data-ttu-id="f0ab5-121">Microsoft - 027328b7-c2e3-4c9e-aaa1-07802dae6c89</span><span class="sxs-lookup"><span data-stu-id="f0ab5-121">Microsoft - 027328b7-c2e3-4c9e-aaa1-07802dae6c89</span></span>

2. <span data-ttu-id="f0ab5-122">Accédez au Panneau d’administration et, sous **Intégrations,** recherchez les fournisseurs d’outils LTI.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-122">Access the Admin Panel, and under **Integrations**, locate the LTI Tool Providers.</span></span>

   ![Il s’agit de la boîte de dialogue Fournisseur d’outils LTI qui affiche la liste des fournisseurs](../media/lti-media/lti-tool-providers.png)

3. <span data-ttu-id="f0ab5-124">Sélectionnez **Inscrire LTI1.3/Outil Advantage.**</span><span class="sxs-lookup"><span data-stu-id="f0ab5-124">Select **Register LTI1.3/Advantage Tool**.</span></span>

4. <span data-ttu-id="f0ab5-125">Entrez le premier des ID clients fournis (tableau noir ou Microsoft), puis sélectionnez **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="f0ab5-125">Enter the first of the Client IDs provided (either Blackboard or Microsoft), and select **Submit**.</span></span>

5. <span data-ttu-id="f0ab5-126">Examinez les paramètres pré-remplis et assurez-vous que l’état de l’outil est marqué comme approuvé.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-126">Review the pre-populated settings and ensure that the tool status is marked as approved.</span></span>

6. <span data-ttu-id="f0ab5-127">Faites défiler jusqu’au bas, puis sélectionnez **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="f0ab5-127">Scroll to the bottom, and then select **Submit**.</span></span>

7. <span data-ttu-id="f0ab5-128">Répétez les étapes précédentes pour inscrire la deuxième application LTI dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-128">Repeat the previous steps to register the second of the LTI apps within your environment.</span></span>

## <a name="set-up-the-rest-application-and-cross-origin-resource-sharing"></a><span data-ttu-id="f0ab5-129">Configurer l’application REST et le partage de ressources d’origine croisée</span><span class="sxs-lookup"><span data-stu-id="f0ab5-129">Set up the REST Application and Cross Origin Resource Sharing</span></span>

<span data-ttu-id="f0ab5-130">L’administrateur Blackboard Learn Ultra devra également configurer l’application REST et la configuration du partage de ressources d’origine croisée.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-130">The Blackboard Learn Ultra admin will also need to configure the REST Application and the Cross Origin Resource Sharing configuration.</span></span>

<span data-ttu-id="f0ab5-131">Complétez les procédures suivantes pour configurer l’application REST</span><span class="sxs-lookup"><span data-stu-id="f0ab5-131">Complete the following to set up the REST Application</span></span>

1. <span data-ttu-id="f0ab5-132">Accédez aux outils d’administration Learn, puis sélectionnez **Intégrations d’API REST dans** la section **Intégrations.**</span><span class="sxs-lookup"><span data-stu-id="f0ab5-132">Access the Learn Administration Tools, and then select **REST API Integrations** from the **Integrations** section.</span></span>

2. <span data-ttu-id="f0ab5-133">Sélectionnez **Créer des intégrations** et entrez le même ID d’application/client que celui que vous avez entré pour l’outil Blackboard Learn Class Teams Integration LTI.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-133">Select **Create integrations** and enter the same Application/Client ID that you entered for the Blackboard Learn Class Teams Integration LTI tool.</span></span>

3. <span data-ttu-id="f0ab5-134">Entrez l’utilisateur Learn (il peut s’y trouver à votre propre nom d’utilisateur d’administrateur Learn) ou **sélectionnez Parcourir** pour le localiser.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-134">Enter the Learn User (this could be your own learn admin username), or select **Browse** to locate.</span></span>

4. <span data-ttu-id="f0ab5-135">Sélectionnez **Oui** pour **l’accès des utilisateurs finux.**</span><span class="sxs-lookup"><span data-stu-id="f0ab5-135">Select **Yes** for **End User Access**.</span></span>

5. <span data-ttu-id="f0ab5-136">Sélectionnez **Oui** **pour être autorisé à agir en tant qu’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="f0ab5-136">Select **Yes** for **Authorized to Act as User**</span></span>

6. <span data-ttu-id="f0ab5-137">Sélectionnez **Envoyer** une fois terminé.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-137">Select **Submit** once complete.</span></span>

## <a name="set-up-cross-origin-resource-sharing"></a><span data-ttu-id="f0ab5-138">Configurer le partage de ressources d’origine croisée</span><span class="sxs-lookup"><span data-stu-id="f0ab5-138">Set up Cross-Origin Resource Sharing</span></span>

1. <span data-ttu-id="f0ab5-139">Accédez aux outils d’administration Learn et sélectionnez **Partage** de ressources d’origine croisée dans la section **Intégrations.**</span><span class="sxs-lookup"><span data-stu-id="f0ab5-139">Access the Learn Administration Tools, and select **Cross-Origin Resource Sharing** from the **Integrations** section.</span></span>

2. <span data-ttu-id="f0ab5-140">Sélectionnez **Créer une configuration.**</span><span class="sxs-lookup"><span data-stu-id="f0ab5-140">Select **Create Configuration**.</span></span>

3. <span data-ttu-id="f0ab5-141">Entrez `https://bb-ms-teams-ultra-ext.api.blackboard.com` l’origine.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-141">Enter `https://bb-ms-teams-ultra-ext.api.blackboard.com` in the origin.</span></span>

4. <span data-ttu-id="f0ab5-142">Ajoutez le mot **Autorisation** dans les **en-têtes autorisés.**</span><span class="sxs-lookup"><span data-stu-id="f0ab5-142">Add the word **Authorization** in the **Allowed Headers**.</span></span>

5. <span data-ttu-id="f0ab5-143">Définir **Disponible** sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-143">Set **Available** to **Yes**.</span></span>

6. <span data-ttu-id="f0ab5-144">Sélectionnez **Envoyer** une fois terminé.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-144">Select **Submit** once complete.</span></span>

## <a name="enable-class-teams-in-blackboard-learn"></a><span data-ttu-id="f0ab5-145">Activer l’Teams classe dans Blackboard Learn</span><span class="sxs-lookup"><span data-stu-id="f0ab5-145">Enable Class Teams in Blackboard Learn</span></span>

<span data-ttu-id="f0ab5-146">Une fois que vous avez activé les outils LTI, l’étape suivante consiste à configurer l’intégration de microsoft Class Teams à partir de votre propre client Microsoft Office 365 client.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-146">Once you've enabled the LTI tools, your next step will be to set up the Microsoft Class Teams integration from your own Microsoft Office 365 tenant.</span></span> <span data-ttu-id="f0ab5-147">Pour ce faire, vous pouvez suivre ces étapes en tant qu’administrateur Blackboard Learn Ultra.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-147">You can do this by following these steps as the Blackboard Learn Ultra admin.</span></span>

1. <span data-ttu-id="f0ab5-148">In **Learn Admin** Tools and  >  **Utilities,** select Microsoft Teams Integration **Admin**.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-148">In **Learn Admin** > **Tools and Utilities**, select **Microsoft Teams Integration Admin**.</span></span>

   ![boîte de dialogue outils et utilitaires avec une liste des outils disponibles](../media/lti-media/tools-utilities.png)

2. <span data-ttu-id="f0ab5-150">Activez la case à cocher **Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="f0ab5-150">Select the checkbox for **Enable Microsoft Teams**.</span></span>

3. <span data-ttu-id="f0ab5-151">Entrez votre ID de client comme indiqué dans la section sous Microsoft O365 Admin</span><span class="sxs-lookup"><span data-stu-id="f0ab5-151">Enter your tenant ID as referenced in the section under Microsoft O365 Admin</span></span>

 > [!NOTE]
 > <span data-ttu-id="f0ab5-152">Vous ne pourrez pas enregistrer les paramètres tant que l’application n’aura pas été approuvée par l’administrateur O365. Voir [Approuver l’application dans Microsoft Azure client.](#approve-the-app-in-the-microsoft-azure-tenant)</span><span class="sxs-lookup"><span data-stu-id="f0ab5-152">You won't be able to save the settings until the app has been approved by the O365 admin. See [Approve the app in Microsoft Azure tenant](#approve-the-app-in-the-microsoft-azure-tenant).</span></span>

4. <span data-ttu-id="f0ab5-153">Lorsque l’administrateur général O365 a approuvé le tableau noir Teams application dans votre client Microsoft, sélectionnez **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="f0ab5-153">When the global O365 admin has approved the Blackboard Teams application in your Microsoft Tenant, select **Submit**.</span></span>
