---
title: Ajouter et vérifier des contacts d’administrateur dans le portail d’administration
description: Indiquez-nous qui contacter pour chaque domaine de travail.
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.author: jaimeo
manager: laurawi
ms.topic: article
ms.openlocfilehash: 65d7647e9000152d2eeb8d6bf36e8d45a0d4fa90
ms.sourcegitcommit: 34c06715e036255faa75c66ebf95c12a85f8ef42
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "52984699"
---
# <a name="add-and-verify-admin-contacts-in-the-admin-portal"></a><span data-ttu-id="2ade7-104">Ajouter et vérifier des contacts d’administrateur dans le portail d’administration</span><span class="sxs-lookup"><span data-stu-id="2ade7-104">Add and verify admin contacts in the Admin portal</span></span>

<span data-ttu-id="2ade7-105">Il existe plusieurs façons Bureau géré Microsoft service communique avec les clients.</span><span class="sxs-lookup"><span data-stu-id="2ade7-105">There are several ways that Microsoft Managed Desktop service communicates with customers.</span></span> <span data-ttu-id="2ade7-106">Pour simplifier la communication et nous assurer que nous vérifions avec les bonnes personnes, vous devez fournir un ensemble de contacts d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="2ade7-106">To streamline communication and ensure we’re checking with the right people, you need to provide a set of admin contacts.</span></span> <span data-ttu-id="2ade7-107">Bureau géré Microsoft Les opérations IT contacteront ces personnes pour obtenir de l’aide pour résoudre les problèmes de votre client.</span><span class="sxs-lookup"><span data-stu-id="2ade7-107">Microsoft Managed Desktop IT Operations will contact these people for assistance troubleshooting issues for your tenant.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2ade7-108">Vous avez peut-être déjà ajouté ces contacts dans le portail d’administration.</span><span class="sxs-lookup"><span data-stu-id="2ade7-108">You might have already added these contacts in the Admin portal.</span></span> <span data-ttu-id="2ade7-109">Si c’est le cas, prenez le temps de vérifier que  la liste des contacts est exacte, car Bureau géré Microsoft être en mesure de les joindre en cas d’incident grave.</span><span class="sxs-lookup"><span data-stu-id="2ade7-109">If so, take a moment now to double-check that the contact list is accurate, since Microsoft Managed Desktop **must** be able to reach them if a severe incident occurs.</span></span>

## <a name="azure-active-directory-access-for-microsoft-managed-desktop-admin-portal"></a><span data-ttu-id="2ade7-110">Azure Active Directory’accès au Bureau géré Microsoft d’administration</span><span class="sxs-lookup"><span data-stu-id="2ade7-110">Azure Active Directory access for Microsoft Managed Desktop Admin portal</span></span>

<span data-ttu-id="2ade7-111">Bureau géré Microsoft Le portail d’administration exige que les personnes accédant au portail ont l’un des rôles Azure Active Directory (AD) ci-après :</span><span class="sxs-lookup"><span data-stu-id="2ade7-111">Microsoft Managed Desktop Admin portal requires that people accessing the portal have one of these Azure Active Directory (AD) roles:</span></span>
- <span data-ttu-id="2ade7-112">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="2ade7-112">Global Administrator</span></span>
- <span data-ttu-id="2ade7-113">Administrateur de service Intune</span><span class="sxs-lookup"><span data-stu-id="2ade7-113">Intune Service Administrator</span></span>
- <span data-ttu-id="2ade7-114">Lecteur général</span><span class="sxs-lookup"><span data-stu-id="2ade7-114">Global Reader</span></span>
- <span data-ttu-id="2ade7-115">Administrateur du support technique</span><span class="sxs-lookup"><span data-stu-id="2ade7-115">Service Support Administrator</span></span>

<span data-ttu-id="2ade7-116">L’administrateur général doit être celui qui inscrit votre organisation dans Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2ade7-116">The Global Administrator must be the one to enroll your organization in Microsoft Managed Desktop.</span></span> <span data-ttu-id="2ade7-117">Les cinq rôles ont le même accès au sein du portail d’administration pour lancer et afficher les tâches.</span><span class="sxs-lookup"><span data-stu-id="2ade7-117">All five roles have the same access within the Admin portal to initiate and view tasks.</span></span> <span data-ttu-id="2ade7-118">Pour plus d’informations sur l’attribution de ces rôles dans Azure AD, voir [autorisations](/azure/active-directory/users-groups-roles/directory-assign-admin-roles)de rôle d’administrateur dans Azure Active Directory .</span><span class="sxs-lookup"><span data-stu-id="2ade7-118">For more information on assigning these roles in Azure AD, see [Administrator role permissions in Azure Active Directory](/azure/active-directory/users-groups-roles/directory-assign-admin-roles).</span></span> 

## <a name="admin-contact-areas-of-focus"></a><span data-ttu-id="2ade7-119">Domaines de contact de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="2ade7-119">Admin contact areas of focus</span></span>

<span data-ttu-id="2ade7-120">Les contacts d’administrateur doivent être la meilleure personne ou le meilleur groupe qui puisse répondre aux questions et prendre des décisions pour différents domaines de travail.</span><span class="sxs-lookup"><span data-stu-id="2ade7-120">Admin contacts should be the best person or group that can answer questions and make decisions for different areas of focus.</span></span> <span data-ttu-id="2ade7-121">**Bureau géré Microsoft Les opérations contactent ces contacts d’administrateur pour les questions concernant les demandes de support déposées par le client.**</span><span class="sxs-lookup"><span data-stu-id="2ade7-121">**Microsoft Managed Desktop Operations will contact these Admin contacts for questions involving support requests filed by the customer.**</span></span> <span data-ttu-id="2ade7-122">Ces contacts d’administrateur recevront des notifications pour les mises à jour de demande de support et les nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="2ade7-122">These Admin contacts will receive notifications for support request updates and new messages.</span></span> <span data-ttu-id="2ade7-123">Ces domaines sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="2ade7-123">These areas include:</span></span>

<span data-ttu-id="2ade7-124">Zone de mise au point</span><span class="sxs-lookup"><span data-stu-id="2ade7-124">Area of focus</span></span> | <span data-ttu-id="2ade7-125">Pour des questions sur</span><span class="sxs-lookup"><span data-stu-id="2ade7-125">For questions about</span></span>
--- | ---
<span data-ttu-id="2ade7-126">Empaquetage d’application</span><span class="sxs-lookup"><span data-stu-id="2ade7-126">App packaging</span></span> | <span data-ttu-id="2ade7-127">Résolution des problèmes d’empaquetage d’application</span><span class="sxs-lookup"><span data-stu-id="2ade7-127">Troubleshooting app packaging</span></span>
<span data-ttu-id="2ade7-128">Appareils</span><span class="sxs-lookup"><span data-stu-id="2ade7-128">Devices</span></span> | <span data-ttu-id="2ade7-129">État de l’appareil, résolution des problèmes Bureau géré Microsoft appareils</span><span class="sxs-lookup"><span data-stu-id="2ade7-129">Device health, troubleshooting with Microsoft Managed Desktop devices</span></span>
<span data-ttu-id="2ade7-130">Sécurité</span><span class="sxs-lookup"><span data-stu-id="2ade7-130">Security</span></span> | <span data-ttu-id="2ade7-131">Résolution des problèmes de sécurité avec Bureau géré Microsoft appareils</span><span class="sxs-lookup"><span data-stu-id="2ade7-131">Troubleshooting security issues with Microsoft Managed Desktop devices</span></span>
<span data-ttu-id="2ade7-132">Service d’aide à l’information</span><span class="sxs-lookup"><span data-stu-id="2ade7-132">IT help desk</span></span> | <span data-ttu-id="2ade7-133">dans les cas où le personnel de support technique remet des tickets d’utilisateur en dehors des Bureau géré Microsoft de support</span><span class="sxs-lookup"><span data-stu-id="2ade7-133">in cases where our Support staff hands over user tickets outside of Microsoft Managed Desktop support areas</span></span> 
<span data-ttu-id="2ade7-134">Autre</span><span class="sxs-lookup"><span data-stu-id="2ade7-134">Other</span></span> | <span data-ttu-id="2ade7-135">Pour les problèmes non couverts par d’autres domaines</span><span class="sxs-lookup"><span data-stu-id="2ade7-135">For issues not covered by other areas</span></span>

<span data-ttu-id="2ade7-136">**Toute personne que vous choisissez pour ces contacts doit avoir les connaissances et l’autorité nécessaires pour prendre des décisions pour Bureau géré Microsoft environnement.**</span><span class="sxs-lookup"><span data-stu-id="2ade7-136">**Whoever you choose for these contacts needs to have the knowledge and authority to make decisions for your Microsoft Managed Desktop environment.**</span></span> <span data-ttu-id="2ade7-137">Lorsque vous intégrerez votre environnement Bureau géré Microsoft, vous êtes invité à ajouter des contacts pour votre aide et sécurité locales.</span><span class="sxs-lookup"><span data-stu-id="2ade7-137">When you onboard your Microsoft Managed Desktop environment, you’re prompted to add contacts for your local Helpdesk and Security.</span></span> 

<span data-ttu-id="2ade7-138">Les contacts d’administrateur sont requis lorsque vous [envoyez une demande de support.](../service-description/support.md)</span><span class="sxs-lookup"><span data-stu-id="2ade7-138">Admin contacts are required when you [submit a Support request](../service-description/support.md).</span></span> <span data-ttu-id="2ade7-139">Vous devez avoir un contact d’administrateur pour la zone de focus de la demande de support.</span><span class="sxs-lookup"><span data-stu-id="2ade7-139">You’ll need to have an admin contact for the focus area of the Support request.</span></span> 

<span data-ttu-id="2ade7-140">**Pour ajouter des contacts d’administrateur**</span><span class="sxs-lookup"><span data-stu-id="2ade7-140">**To add admin contacts**</span></span>

1.  <span data-ttu-id="2ade7-141">Connectez-vous [à Microsoft Endpoint Manager](https://endpoint.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="2ade7-141">Sign in to [Microsoft Endpoint Manager](https://endpoint.microsoft.com).</span></span> 

2.  <span data-ttu-id="2ade7-142">Sous **Administration du client,** recherchez la section **Bureau géré Microsoft** puis sélectionnez **Contacts d’administration.**</span><span class="sxs-lookup"><span data-stu-id="2ade7-142">Under **Tenant administration**, look for the **Microsoft Managed Desktop** section then select **Admin contacts**.</span></span> 

3. <span data-ttu-id="2ade7-143">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="2ade7-143">Select **Add**.</span></span>

4.  <span data-ttu-id="2ade7-144">Sélectionnez **une zone de focus** et entrez les informations du contact.</span><span class="sxs-lookup"><span data-stu-id="2ade7-144">Select an **Area of focus** and enter the info for the contact.</span></span> 

    ![liste des domaines de mise au point, tels que Autres, Applications et Sécurité](../../media/areaoffocus.png)

5. <span data-ttu-id="2ade7-146">Répétez l’étape pour chaque zone de mise au point.</span><span class="sxs-lookup"><span data-stu-id="2ade7-146">Repeat for each area of focus.</span></span> 

## <a name="steps-to-get-started-with-microsoft-managed-desktop"></a><span data-ttu-id="2ade7-147">Étapes de mise en Bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="2ade7-147">Steps to get started with Microsoft Managed Desktop</span></span>

1. <span data-ttu-id="2ade7-148">Ajouter et vérifier des contacts d’administrateur dans le portail d’administration (cette rubrique)</span><span class="sxs-lookup"><span data-stu-id="2ade7-148">Add and verify admin contacts in the Admin portal (this topic)</span></span>
2. [<span data-ttu-id="2ade7-149">Ajuster l’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="2ade7-149">Adjust conditional access</span></span>](conditional-access.md)
3. [<span data-ttu-id="2ade7-150">Affecter des licences</span><span class="sxs-lookup"><span data-stu-id="2ade7-150">Assign licenses</span></span>](assign-licenses.md)
4. [<span data-ttu-id="2ade7-151">Installer l’application Portail d’entreprise Intune sur les appareils</span><span class="sxs-lookup"><span data-stu-id="2ade7-151">Install Intune Company Portal on on devices</span></span>](company-portal.md)
5. [<span data-ttu-id="2ade7-152">Activer Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="2ade7-152">Enable Enterprise State Roaming</span></span>](enterprise-state-roaming.md)
6. [<span data-ttu-id="2ade7-153">Configurer les appareils Bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="2ade7-153">Set up Microsoft Managed Desktop devices</span></span>](set-up-devices.md)
7. [<span data-ttu-id="2ade7-154">Préparer vos utilisateurs à l’utilisation les appareils</span><span class="sxs-lookup"><span data-stu-id="2ade7-154">Get your users ready to use devices</span></span>](get-started-devices.md)
8. [<span data-ttu-id="2ade7-155">Déployer les applications sur les appareils</span><span class="sxs-lookup"><span data-stu-id="2ade7-155">Deploy apps to devices</span></span>](deploy-apps.md)
