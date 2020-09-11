---
title: Gérer Microsoft 365 avec Windows PowerShell pour les partenaires DAP
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Ent_O365
- M365-subscription-management
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
ms.assetid: be497751-596f-431d-b256-0a89d36a47ce
description: La manière dont les partenaires de syndication et de fournisseur de solutions Cloud peuvent utiliser Windows PowerShell pour gérer les locataires de clients Microsoft 365.
ms.openlocfilehash: a7b2fbb5423e3b923e17aa2d9c488e7dd085be35
ms.sourcegitcommit: aeb94601a81db3ead8610c2f36cff30eb9fe10e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "47429877"
---
# <a name="how-to-manage-microsoft-365-with-windows-powershell-for-delegated-access-permissions-partners"></a><span data-ttu-id="24136-103">Comment gérer Microsoft 365 avec Windows PowerShell pour les partenaires avec autorisations d’accès délégué</span><span class="sxs-lookup"><span data-stu-id="24136-103">How to manage Microsoft 365 with Windows PowerShell for Delegated Access Permissions partners</span></span>

<span data-ttu-id="24136-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="24136-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="24136-105">Les partenaires avec autorisation d'accès délégué sont les partenaires de syndication et fournisseurs de solutions cloud.</span><span class="sxs-lookup"><span data-stu-id="24136-105">Delegated Access Permission (DAP) partners are Syndication and Cloud Solution Providers (CSP) Partners.</span></span> <span data-ttu-id="24136-106">De nombreux sont les fournisseurs de réseau ou de télécommunications.</span><span class="sxs-lookup"><span data-stu-id="24136-106">Many are network or telecom providers.</span></span> <span data-ttu-id="24136-107">Ils regroupent les abonnements Microsoft 365 dans leurs offres de service.</span><span class="sxs-lookup"><span data-stu-id="24136-107">They bundle Microsoft 365 subscriptions into their service offerings.</span></span> <span data-ttu-id="24136-108">Lors de la vente d’un abonnement Microsoft 365, les autorisations d’administration pour le compte de (administrateur) sont automatiquement accordées aux locations du client afin qu’ils puissent administrer et rendre compte de ces locations.</span><span class="sxs-lookup"><span data-stu-id="24136-108">When they sell a Microsoft 365 subscription, they're automatically granted Administer On Behalf Of (AOBO) permissions to the customer's tenancies so they can administer and report on those tenancies.</span></span> <span data-ttu-id="24136-109">Ces tâches sont difficiles à effectuer dans le centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="24136-109">These tasks are difficult to do in the Microsoft 365 admin center.</span></span> <span data-ttu-id="24136-110">Il est beaucoup plus facile d’utiliser PowerShell pour Microsoft 365 pour effectuer des tâches administratives telles que :</span><span class="sxs-lookup"><span data-stu-id="24136-110">It's much easier to use PowerShell for Microsoft 365 to do administrative tasks such as:</span></span>
- <span data-ttu-id="24136-111">Répertorier tous les clients **TenantIds** et leurs domaines</span><span class="sxs-lookup"><span data-stu-id="24136-111">List all the customer **TenantIds** and their domains</span></span> 
- <span data-ttu-id="24136-112">Identifier tous les utilisateurs d’un client et les licences qui leur ont été attribuées</span><span class="sxs-lookup"><span data-stu-id="24136-112">Identify all users in a customer tenancy and their assigned licenses</span></span>
> [!NOTE]
> <span data-ttu-id="24136-113">Certaines tâches d’administration peuvent uniquement être effectuées dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="24136-113">Some administrative tasks can only be done in PowerShell.</span></span>

<span data-ttu-id="24136-114">Les articles suivants montrent comment les partenaires de syndication et CSP utilisent PowerShell pour administrer leurs clients :</span><span class="sxs-lookup"><span data-stu-id="24136-114">The following articles show how Syndication and CSP partners use PowerShell to administer their customer tenancies:</span></span>
  
- [<span data-ttu-id="24136-115">Gérer les clients Microsoft 365 avec Windows PowerShell pour les partenaires avec autorisations d’accès délégué</span><span class="sxs-lookup"><span data-stu-id="24136-115">Manage Microsoft 365 tenants with Windows PowerShell for Delegated Access Permissions (DAP) partners</span></span>](manage-microsoft-365-tenants-with-windows-powershell-for-delegated-access-permissio.md)
    
- [<span data-ttu-id="24136-116">Ajout d'un domaine à la location d'un client avec Windows PowerShell pour les partenaires avec autorisation d'accès délégué</span><span class="sxs-lookup"><span data-stu-id="24136-116">Add a domain to a client tenancy with Windows PowerShell for Delegated Access Permission (DAP) partners</span></span>](add-a-domain-to-a-client-tenancy-with-windows-powershell-for-delegated-access-pe.md)
    
- [<span data-ttu-id="24136-117">Connexion à Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="24136-117">Connect to Exchange Online PowerShell</span></span>](connect-to-exchange-online-tenants-with-remote-windows-powershell-for-delegated.md)
    
- [<span data-ttu-id="24136-118">Récupération des données des rapports du locataire d'un client avec Windows PowerShell pour les partenaires avec autorisation d'accès délégué</span><span class="sxs-lookup"><span data-stu-id="24136-118">Retrieve customer tenant reporting data with Windows PowerShell for Delegated Access Permissions (DAP) partners</span></span>](retrieve-customer-tenant-reporting-data-with-windows-powershell-for-delegated-ac.md)
   