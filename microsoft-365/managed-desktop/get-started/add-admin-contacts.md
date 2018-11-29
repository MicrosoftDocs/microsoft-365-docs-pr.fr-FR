---
title: Ajouter des contacts d’administration dans le portail d’administration d’ordinateur de bureau Microsoft
description: Indiquez les personnes à contacter pour chaque zone de focus.
keywords: Service Microsoft de bureau, Microsoft 365, documentation
ms.service: m365-md
author: jdeckerms
ms.localizationpriority: normal
ms.date: 09/24/2018
ms.openlocfilehash: 65dd8709c469826e2696015c13823c58eb10e342
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867018"
---
# <a name="add-admin-contacts-in-microsoft-managed-desktop-admin-portal"></a><span data-ttu-id="72baa-104">Ajouter des contacts d’administration dans le portail d’administration de bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="72baa-104">Add Admin contacts in Microsoft Managed Desktop Admin portal</span></span>

<span data-ttu-id="72baa-p101">Il existe plusieurs manières de service de l’ordinateur de bureau Microsoft communique avec les clients. Pour simplifier la communication et garantir que nous vérifions avec les contacts meilleures, vous devez fournir un ensemble de contacts d’administration. Les opérations informatiques de bureau géré Microsoft contacte ces personnes pour obtenir une assistance de résolution des problèmes pour votre client.</span><span class="sxs-lookup"><span data-stu-id="72baa-p101">There are several ways that Microsoft Managed Desktop service communicates with customers. To streamline communication and ensure we’re checking with the best contacts, you need to provide a set of admin contacts. Microsoft Managed Desktop IT Operations will contact these people for assistance troubleshooting issues for your tenant.</span></span> 

## <a name="azure-active-directory-access-for-microsoft-managed-desktop-admin-portal"></a><span data-ttu-id="72baa-108">Accès à Active Directory pour le portail d’administration de bureau géré Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="72baa-108">Azure Active Directory access for Microsoft Managed Desktop Admin portal</span></span>

<span data-ttu-id="72baa-109">Portail d’administration de bureau géré Microsoft nécessite que personnes l’accès au portail un de ces rôles d’Azure Active Directory (AD) :</span><span class="sxs-lookup"><span data-stu-id="72baa-109">Microsoft Managed Desktop Admin portal requires that people accessing the portal have one of these Azure Active Directory (AD) roles:</span></span>
- <span data-ttu-id="72baa-110">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="72baa-110">Global Administrator</span></span>
- <span data-ttu-id="72baa-111">Administrateur de Service Intune</span><span class="sxs-lookup"><span data-stu-id="72baa-111">Intune Service Administrator</span></span>
- <span data-ttu-id="72baa-112">Administrateur de facturation</span><span class="sxs-lookup"><span data-stu-id="72baa-112">Billing Administrator</span></span>
- <span data-ttu-id="72baa-113">Administrateur de service prise en charge</span><span class="sxs-lookup"><span data-stu-id="72baa-113">Service Support Administrator</span></span>

<span data-ttu-id="72baa-114">Pour plus d’informations sur ces rôles et leur affectation dans Azure AD, voir [autorisations de rôle administrateur dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="72baa-114">For more information on these roles and assigning them in Azure AD, see [Administrator role permissions in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles).</span></span> 

## <a name="admin-contact-focus-areas"></a><span data-ttu-id="72baa-115">Domaines contact d’administration</span><span class="sxs-lookup"><span data-stu-id="72baa-115">Admin contact focus areas</span></span>

<span data-ttu-id="72baa-p102">Contacts d’administration doivent être la meilleure personne ou un groupe qui peut répondre aux questions et prendre des décisions de différents domaines. Ces domaines sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="72baa-p102">Admin contacts should be the best person or group that can answer questions and make decisions for different focus areas. These areas include:</span></span>

<span data-ttu-id="72baa-118">Zone de focus</span><span class="sxs-lookup"><span data-stu-id="72baa-118">Focus area</span></span> | <span data-ttu-id="72baa-119">Pour toute question concernant</span><span class="sxs-lookup"><span data-stu-id="72baa-119">For questions about</span></span>
--- | ---
<span data-ttu-id="72baa-120">Applications</span><span class="sxs-lookup"><span data-stu-id="72baa-120">Apps</span></span> | <span data-ttu-id="72baa-121">Résolution des problèmes d’empaquetage de l’application</span><span class="sxs-lookup"><span data-stu-id="72baa-121">Troubleshooting App Packaging</span></span>
<span data-ttu-id="72baa-122"> Appareils </span><span class="sxs-lookup"><span data-stu-id="72baa-122">Devices</span></span> | <span data-ttu-id="72baa-123">État de santé, résolution des problèmes avec les périphériques de bureau Microsoft</span><span class="sxs-lookup"><span data-stu-id="72baa-123">Device health, troubleshooting with Microsoft Managed Desktop devices</span></span>
<span data-ttu-id="72baa-124">Sécurité</span><span class="sxs-lookup"><span data-stu-id="72baa-124">Security</span></span> | <span data-ttu-id="72baa-125">Résolution des problèmes de sécurité avec des périphériques de bureau Microsoft</span><span class="sxs-lookup"><span data-stu-id="72baa-125">Troubleshooting security issues with Microsoft Managed Desktop devices</span></span>
<span data-ttu-id="72baa-126">Autre</span><span class="sxs-lookup"><span data-stu-id="72baa-126">Other</span></span> | <span data-ttu-id="72baa-127">Pour les problèmes non couverts par les autres domaines</span><span class="sxs-lookup"><span data-stu-id="72baa-127">For issues not covered by other areas</span></span>

<span data-ttu-id="72baa-p103">Toute personne que vous choisissez pour ces contacts doit disposer de la base de connaissances et l’autorité de prendre des décisions pour votre environnement de bureau Microsoft. Lorsque vous intégrée de Microsoft géré environnement de bureau, vous êtes invité à ajouter des contacts de votre support technique et de sécurité locale.</span><span class="sxs-lookup"><span data-stu-id="72baa-p103">Whoever you choose for these contacts needs to have the knowledge and authority to make decisions for your Microsoft Managed Desktop environment. When you onboard your Microsoft Managed Desktop environment, you’re prompted to add contacts for your local Helpdesk and Security.</span></span> 

<span data-ttu-id="72baa-p104">Contacts d’administration sont requis lorsque vous [soumettre une demande de prise en charge](../working-with-managed-desktop/support.md). Vous devez disposer d’un contact de l’administrateur de la zone de focus de la demande de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="72baa-p104">Admin contacts are required when you [submit a Support request](../working-with-managed-desktop/support.md). You’ll need to have an admin contact for the focus area of the Support request.</span></span> 

<span data-ttu-id="72baa-132">**Pour ajouter des contacts d’administration**</span><span class="sxs-lookup"><span data-stu-id="72baa-132">**To add admin contacts**</span></span>

1.  <span data-ttu-id="72baa-133">Connectez-vous au [portail d’administration d’ordinateur de bureau Microsoft](http://aka.ms/mwaasportal).</span><span class="sxs-lookup"><span data-stu-id="72baa-133">Sign in to [Microsoft Managed Desktop admin portal](http://aka.ms/mwaasportal).</span></span> 

2.  <span data-ttu-id="72baa-134">Sous **prise en charge**, sélectionnez **les contacts d’administration**.</span><span class="sxs-lookup"><span data-stu-id="72baa-134">Under **Support**, select **Admin contacts**.</span></span> 

    ![Menu de prise en charge, les contacts d’administration](images/admincontacts.png)

3. <span data-ttu-id="72baa-136">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="72baa-136">Select **Add**.</span></span>

    ![Bouton Ajouter un portail d’administration](images/adminadd.png)

4.  <span data-ttu-id="72baa-138">Sélectionnez une **zone du focus** , entrez les informations du contact.</span><span class="sxs-lookup"><span data-stu-id="72baa-138">Select an **Area of focus** and enter the info for the contact.</span></span> 

    ![la liste de domaines](images/areaoffocus.png)

5. <span data-ttu-id="72baa-140">Répétez pour chaque zone de focus.</span><span class="sxs-lookup"><span data-stu-id="72baa-140">Repeat for each area of focus.</span></span> 

