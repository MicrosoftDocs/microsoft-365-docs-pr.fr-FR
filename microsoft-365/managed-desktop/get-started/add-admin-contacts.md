---
title: Ajouter et vérifier des contacts d’administrateur dans le portail d’administration
description: Dites-nous qui contacter pour chaque zone de focus.
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.author: jaimeo
manager: laurawi
ms.topic: article
ms.openlocfilehash: d8a5775d90f592aa5f64dd5f379fb37278032d87
ms.sourcegitcommit: 126d22d8abd190beb7101f14bd357005e4c729f0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/30/2020
ms.locfileid: "46529802"
---
# <a name="add-and-verify-admin-contacts-in-the-admin-portal"></a><span data-ttu-id="566c3-104">Ajouter et vérifier des contacts d’administrateur dans le portail d’administration</span><span class="sxs-lookup"><span data-stu-id="566c3-104">Add and verify admin contacts in the Admin portal</span></span>

<span data-ttu-id="566c3-105">Le service de bureau géré Microsoft communique de plusieurs façons avec les clients.</span><span class="sxs-lookup"><span data-stu-id="566c3-105">There are several ways that Microsoft Managed Desktop service communicates with customers.</span></span> <span data-ttu-id="566c3-106">Pour simplifier la communication et vérifier que nous vérifions les personnes appropriées, vous devez fournir un ensemble de contacts d’administration.</span><span class="sxs-lookup"><span data-stu-id="566c3-106">To streamline communication and ensure we’re checking with the right people, you need to provide a set of admin contacts.</span></span> <span data-ttu-id="566c3-107">Les opérations informatiques de bureau gérées par Microsoft contacteront ces personnes pour résoudre les problèmes de résolution des problèmes pour votre client.</span><span class="sxs-lookup"><span data-stu-id="566c3-107">Microsoft Managed Desktop IT Operations will contact these people for assistance troubleshooting issues for your tenant.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="566c3-108">Vous avez peut-être déjà ajouté ces contacts dans le portail d’administration.</span><span class="sxs-lookup"><span data-stu-id="566c3-108">You might have already added these contacts in the Admin portal.</span></span> <span data-ttu-id="566c3-109">Si c’est le cas, prenez le temps de vérifier que la liste des contacts est exacte, car Microsoft Managed Desktop **doit** être en mesure de les joindre en cas d’incident grave.</span><span class="sxs-lookup"><span data-stu-id="566c3-109">If so, take a moment now to double-check that the contact list is accurate, since Microsoft Managed Desktop **must** be able to reach them if a severe incident occurs.</span></span>

## <a name="azure-active-directory-access-for-microsoft-managed-desktop-admin-portal"></a><span data-ttu-id="566c3-110">Accès Azure Active Directory pour le portail d’administration de bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="566c3-110">Azure Active Directory access for Microsoft Managed Desktop Admin portal</span></span>

<span data-ttu-id="566c3-111">Le portail d’administration de bureau géré Microsoft exige que les utilisateurs qui accèdent au portail disposent de l’un de ces rôles Azure Active Directory (AD) :</span><span class="sxs-lookup"><span data-stu-id="566c3-111">Microsoft Managed Desktop Admin portal requires that people accessing the portal have one of these Azure Active Directory (AD) roles:</span></span>
- <span data-ttu-id="566c3-112">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="566c3-112">Global Administrator</span></span>
- <span data-ttu-id="566c3-113">Administrateur du service Intune</span><span class="sxs-lookup"><span data-stu-id="566c3-113">Intune Service Administrator</span></span>
- <span data-ttu-id="566c3-114">Lecteur général</span><span class="sxs-lookup"><span data-stu-id="566c3-114">Global Reader</span></span>
- <span data-ttu-id="566c3-115">Administrateur de support de service</span><span class="sxs-lookup"><span data-stu-id="566c3-115">Service Support Administrator</span></span>

<span data-ttu-id="566c3-116">L’administrateur général doit être celui pour inscrire votre organisation dans le bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="566c3-116">The Global Administrator must be the one to enroll your organization in Microsoft Managed Desktop.</span></span> <span data-ttu-id="566c3-117">Les cinq rôles ont le même accès dans le portail d’administration pour lancer et afficher les tâches.</span><span class="sxs-lookup"><span data-stu-id="566c3-117">All five roles have the same access within the Admin portal to initiate and view tasks.</span></span> <span data-ttu-id="566c3-118">Pour plus d’informations sur l’affectation de ces rôles dans Azure AD, reportez-vous à la rubrique [Administrator Role Permissions in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="566c3-118">For more information on assigning these roles in Azure AD, see [Administrator role permissions in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles).</span></span> 

## <a name="admin-contact-areas-of-focus"></a><span data-ttu-id="566c3-119">Zones de contact de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="566c3-119">Admin contact areas of focus</span></span>

<span data-ttu-id="566c3-120">Les contacts d’administration doivent être la personne ou le groupe le mieux adapté pour répondre aux questions et prendre des décisions pour différentes zones de focus.</span><span class="sxs-lookup"><span data-stu-id="566c3-120">Admin contacts should be the best person or group that can answer questions and make decisions for different areas of focus.</span></span> <span data-ttu-id="566c3-121">**Les opérations de bureau géré Microsoft contacteront ces contacts d’administration pour les questions portant sur les demandes de support déposées par le client.**</span><span class="sxs-lookup"><span data-stu-id="566c3-121">**Microsoft Managed Desktop Operations will contact these Admin contacts for questions involving support requests filed by the customer.**</span></span> <span data-ttu-id="566c3-122">Ces contacts d’administration recevront des notifications pour les mises à jour des demandes de support et les nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="566c3-122">These Admin contacts will receive notifications for support request updates and new messages.</span></span> <span data-ttu-id="566c3-123">Ces domaines sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="566c3-123">These areas include:</span></span>

<span data-ttu-id="566c3-124">Zone de focus</span><span class="sxs-lookup"><span data-stu-id="566c3-124">Area of focus</span></span> | <span data-ttu-id="566c3-125">Pour obtenir des questions sur</span><span class="sxs-lookup"><span data-stu-id="566c3-125">For questions about</span></span>
--- | ---
<span data-ttu-id="566c3-126">Empaquetage d’applications</span><span class="sxs-lookup"><span data-stu-id="566c3-126">App packaging</span></span> | <span data-ttu-id="566c3-127">Résolution des problèmes d’empaquetage d’applications</span><span class="sxs-lookup"><span data-stu-id="566c3-127">Troubleshooting app packaging</span></span>
<span data-ttu-id="566c3-128">Appareils</span><span class="sxs-lookup"><span data-stu-id="566c3-128">Devices</span></span> | <span data-ttu-id="566c3-129">Intégrité de l’appareil, résolution des problèmes avec les appareils de bureau gérés Microsoft</span><span class="sxs-lookup"><span data-stu-id="566c3-129">Device health, troubleshooting with Microsoft Managed Desktop devices</span></span>
<span data-ttu-id="566c3-130">Sécurité</span><span class="sxs-lookup"><span data-stu-id="566c3-130">Security</span></span> | <span data-ttu-id="566c3-131">Résolution des problèmes de sécurité avec les appareils de bureau gérés Microsoft</span><span class="sxs-lookup"><span data-stu-id="566c3-131">Troubleshooting security issues with Microsoft Managed Desktop devices</span></span>
<span data-ttu-id="566c3-132">Support technique informatique</span><span class="sxs-lookup"><span data-stu-id="566c3-132">IT help desk</span></span> | <span data-ttu-id="566c3-133">dans les cas où notre équipe de support technique effectue des tickets d’utilisateur final en dehors des zones de support de bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="566c3-133">in cases where our Support staff hands over end-user tickets outside of Microsoft Managed Desktop support areas</span></span> 
<span data-ttu-id="566c3-134">Autre</span><span class="sxs-lookup"><span data-stu-id="566c3-134">Other</span></span> | <span data-ttu-id="566c3-135">Pour les problèmes non couverts par d’autres domaines</span><span class="sxs-lookup"><span data-stu-id="566c3-135">For issues not covered by other areas</span></span>

<span data-ttu-id="566c3-136">**Les personnes que vous choisissez pour ces contacts doivent disposer des connaissances et des pouvoirs nécessaires pour prendre des décisions concernant votre environnement de bureau géré Microsoft.**</span><span class="sxs-lookup"><span data-stu-id="566c3-136">**Whoever you choose for these contacts needs to have the knowledge and authority to make decisions for your Microsoft Managed Desktop environment.**</span></span> <span data-ttu-id="566c3-137">Lorsque vous intégrez votre environnement de bureau géré Microsoft, vous êtes invité à ajouter des contacts pour votre service d’assistance et sécurité locaux.</span><span class="sxs-lookup"><span data-stu-id="566c3-137">When you onboard your Microsoft Managed Desktop environment, you’re prompted to add contacts for your local Helpdesk and Security.</span></span> 

<span data-ttu-id="566c3-138">Les contacts d’administration sont requis lorsque vous [envoyez une demande de support](../service-description/support.md).</span><span class="sxs-lookup"><span data-stu-id="566c3-138">Admin contacts are required when you [submit a Support request](../service-description/support.md).</span></span> <span data-ttu-id="566c3-139">Vous devez disposer d’un contact administrateur pour la zone de sélection de la demande de support.</span><span class="sxs-lookup"><span data-stu-id="566c3-139">You’ll need to have an admin contact for the focus area of the Support request.</span></span> 

<span data-ttu-id="566c3-140">**Pour ajouter des contacts d’administration**</span><span class="sxs-lookup"><span data-stu-id="566c3-140">**To add admin contacts**</span></span>

1.  <span data-ttu-id="566c3-141">Connectez-vous au [portail d’administration de bureau géré Microsoft](https://aka.ms/mwaasportal).</span><span class="sxs-lookup"><span data-stu-id="566c3-141">Sign in to [Microsoft Managed Desktop admin portal](https://aka.ms/mwaasportal).</span></span> 

2.  <span data-ttu-id="566c3-142">Sous **support**, sélectionnez **contacts d’administration**.</span><span class="sxs-lookup"><span data-stu-id="566c3-142">Under **Support**, select **Admin contacts**.</span></span> 

    ![Menu support, contacts administrateur dans la partie supérieure sélectionnée](../../media/admincontacts.png)

3. <span data-ttu-id="566c3-144">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="566c3-144">Select **Add**.</span></span>

    ![Portail d’administration, bouton Ajouter, à gauche de l’option Exporter et actualiser](../../media/adminadd.png)

4.  <span data-ttu-id="566c3-146">Sélectionnez une **zone de** sélection, puis entrez les informations du contact.</span><span class="sxs-lookup"><span data-stu-id="566c3-146">Select an **Area of focus** and enter the info for the contact.</span></span> 

    ![Liste des domaines ciblés, tels que les autres, les applications et la sécurité](../../media/areaoffocus.png)

5. <span data-ttu-id="566c3-148">Répétez l’opération pour chaque zone de focus.</span><span class="sxs-lookup"><span data-stu-id="566c3-148">Repeat for each area of focus.</span></span> 

## <a name="steps-to-get-started-with-microsoft-managed-desktop"></a><span data-ttu-id="566c3-149">Étapes de prise en main de Microsoft Managed Desktop</span><span class="sxs-lookup"><span data-stu-id="566c3-149">Steps to get started with Microsoft Managed Desktop</span></span>

1. <span data-ttu-id="566c3-150">Ajouter et vérifier des contacts d’administration dans le portail d’administration (cette rubrique)</span><span class="sxs-lookup"><span data-stu-id="566c3-150">Add and verify admin contacts in the Admin portal (this topic)</span></span>
2. [<span data-ttu-id="566c3-151">Ajuster l’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="566c3-151">Adjust conditional access</span></span>](conditional-access.md)
3. [<span data-ttu-id="566c3-152">Affecter des licences</span><span class="sxs-lookup"><span data-stu-id="566c3-152">Assign licenses</span></span>](assign-licenses.md)
4. [<span data-ttu-id="566c3-153">Installer l’application Portail d’entreprise Intune sur les appareils</span><span class="sxs-lookup"><span data-stu-id="566c3-153">Install Intune Company Portal on on devices</span></span>](company-portal.md)
5. [<span data-ttu-id="566c3-154">Activer Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="566c3-154">Enable Enterprise State Roaming</span></span>](enterprise-state-roaming.md)
6. [<span data-ttu-id="566c3-155">Configurer les appareils Bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="566c3-155">Set up Microsoft Managed Desktop devices</span></span>](set-up-devices.md)
7. [<span data-ttu-id="566c3-156">Préparer vos utilisateurs à l’utilisation les appareils</span><span class="sxs-lookup"><span data-stu-id="566c3-156">Get your users ready to use devices</span></span>](get-started-devices.md)
8. [<span data-ttu-id="566c3-157">Déployer les applications sur les appareils</span><span class="sxs-lookup"><span data-stu-id="566c3-157">Deploy apps to devices</span></span>](deploy-apps.md)
