---
title: Affecter des autorisations pour les enquêtes sur les données (aperçu)
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Cet article explique comment configurer les autorisations nécessaires pour utiliser l’outil des enquêtes de données dans Microsoft 365.
ms.openlocfilehash: 47a7923d38cfa0ea3bad6c4c266f580f8104c429
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43637756"
---
# <a name="assign-permissions-for-data-investigations-preview"></a><span data-ttu-id="b6d12-103">Affecter des autorisations pour les enquêtes sur les données (aperçu)</span><span class="sxs-lookup"><span data-stu-id="b6d12-103">Assign permissions for Data Investigations (Preview)</span></span>

<span data-ttu-id="b6d12-104">Pour accéder à une enquête sur les données dans le centre de conformité Office 365 ou Microsoft 365, vous devez être membre du groupe de rôles Data investigation.</span><span class="sxs-lookup"><span data-stu-id="b6d12-104">To access a data investigation in the Office 365 or Microsoft 365 compliance center, you need be a member of the Data Investigator role group.</span></span> <span data-ttu-id="b6d12-105">Pour ajouter des membres à un groupe de rôles, vous devez être membre du groupe de rôles gestion de l’organisation ou disposer du rôle de gestion des rôles dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="b6d12-105">To add members to a role group, you must be a member of the Organization Management role group or assigned the Role Management role in the Security & Compliance Center.</span></span> <span data-ttu-id="b6d12-106">Une fois qu’un utilisateur est membre du groupe de rôles Data investigation, il peut créer, consulter et mener des enquêtes dans les enquêtes de données dont vous êtes membre.</span><span class="sxs-lookup"><span data-stu-id="b6d12-106">After a user becomes a member of the Data Investigator role group, they can create, access, and conduct investigations in the data investigations that you are a member of.</span></span>

<span data-ttu-id="b6d12-107">Pour attribuer des autorisations d’investigation de données :</span><span class="sxs-lookup"><span data-stu-id="b6d12-107">To assign data investigations permissions:</span></span>

1. <span data-ttu-id="b6d12-108">Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide des informations d’identification d’un compte d’administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b6d12-108">Go to [https://protection.office.com](https://protection.office.com) and sign in using the credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="b6d12-109">Dans le centre de sécurité & conformité, cliquez sur **autorisations**.</span><span class="sxs-lookup"><span data-stu-id="b6d12-109">In the Security & Compliance Center, click **Permissions**.</span></span>

3. <span data-ttu-id="b6d12-110">Cliquez sur le groupe de rôles **Data investigation** , puis en regard de **membres** sur la page de menu volant, cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="b6d12-110">Click the **Data Investigator** role group, and then next to **Members** on the flyout page, click **Edit**.</span></span>

4. <span data-ttu-id="b6d12-111">Cliquez sur **choisir les membres** , puis sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b6d12-111">Click **Choose members** and then click **Add**.</span></span> <span data-ttu-id="b6d12-112">Sélectionnez les utilisateurs que vous souhaitez ajouter en tant qu’utilisateurs de données, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b6d12-112">Select the users that you want to add as data investigators, and then click **Add**.</span></span>

5. <span data-ttu-id="b6d12-113">Une fois que vous avez ajouté tous les utilisateurs, cliquez sur **Terminer** , puis sur **Enregistrer** pour enregistrer les modifications apportées au groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="b6d12-113">After you've added all the users, click **Done** and then click **Save** to save the changes to the role group.</span></span>

> [!NOTE]
> <span data-ttu-id="b6d12-114">Le rôle de gestion de l’accès aux données affecté au groupe de rôles Data investigation fournit les autorisations nécessaires pour accéder à l’outil d’investigation de données dans le centre de conformité Office 365 ou Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b6d12-114">The Data Investigation Management role that is assigned to the Data Investigator role group provides the necessary permissions to access the Data Investigations tool in the Office 365 or Microsoft 365 compliance center.</span></span> <span data-ttu-id="b6d12-115">Par défaut, ce rôle n’est pas attribué au groupe de rôles gestion de l’organisation, ce qui signifie que les administrateurs globaux de votre organisation ne pourront peut-être pas accéder à l’outil d’examen des données par défaut.</span><span class="sxs-lookup"><span data-stu-id="b6d12-115">By default, this role is not assigned to the Organization Management role group, which means that global admins in your organization may not be able to access the Data Investigations tool by default.</span></span> <span data-ttu-id="b6d12-116">Pour résoudre ce problème, vous pouvez ajouter des administrateurs globaux au groupe de rôles Data investigation ou ajouter le rôle de gestion de l’enquête sur les données au groupe de rôles gestion de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="b6d12-116">To fix this, you can add global admins to the Data Investigator role group or add the Data Investigation Management role to the Organization Management role group.</span></span> <span data-ttu-id="b6d12-117">Une troisième option consiste à créer un groupe de rôles personnalisé et à attribuer le rôle de gestion de l’examen des données (et d’autres rôles), puis à ajouter les membres appropriés.</span><span class="sxs-lookup"><span data-stu-id="b6d12-117">A third option would be to create a custom role group and assign the Data Investigation Management role (and other roles) and then add appropriate members.</span></span> <span data-ttu-id="b6d12-118">Pour plus d’informations sur les groupes de rôles et les rôles, consultez [la rubrique autorisations dans le centre de sécurité & conformité](https://docs.microsoft.com/microsoft-365/security/office-365-security/permissions-in-the-security-and-compliance-center).</span><span class="sxs-lookup"><span data-stu-id="b6d12-118">For more information about role groups and roles, see [Permissions in the Security & Compliance Center](https://docs.microsoft.com/microsoft-365/security/office-365-security/permissions-in-the-security-and-compliance-center).</span></span>
