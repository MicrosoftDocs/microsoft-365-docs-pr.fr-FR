---
title: Collecter les informations dont vous avez besoin pour créer des enregistrements DNS
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
- Adm_O365_Setup
ms.custom:
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
ms.assetid: 77f90d4a-dc7f-4f09-8972-c1b03ea85a67
description: Collectez les valeurs/informations dont vous avez besoin pour créer des enregistrements DNS afin de connecter votre domaine à Microsoft 365 abonnement.
ms.openlocfilehash: e65d53269f5fb8625b12c4eb22f78516818045be
ms.sourcegitcommit: 17f0aada83627d9defa0acf4db03a2d58e46842f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52635725"
---
# <a name="gather-the-information-you-need-to-create-dns-records"></a><span data-ttu-id="aa055-103">Collecter les informations dont vous avez besoin pour créer des enregistrements DNS</span><span class="sxs-lookup"><span data-stu-id="aa055-103">Gather the information you need to create DNS records</span></span>

 <span data-ttu-id="aa055-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="aa055-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span> 
  
### <a name="step-1-find-the-txt-record-value-and-verify"></a><span data-ttu-id="aa055-105">Étape 1 : rechercher la valeur de l’enregistrement TXT et vérifier</span><span class="sxs-lookup"><span data-stu-id="aa055-105">Step 1: Find the TXT record value and verify</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="aa055-106">Dans le Microsoft 365 d’administration,  allez à la page \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines d’installation.</a></span><span class="sxs-lookup"><span data-stu-id="aa055-106">In the Microsoft 365 admin center, go to the **Setup** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="aa055-107">Dans le centre d’administration, allez à la page  > <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">Domaines d’installation.</a></span><span class="sxs-lookup"><span data-stu-id="aa055-107">In the admin center, go to the **Setup** > <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">Domains</a> page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="aa055-108">Dans le centre d’administration, allez à la page  > <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">Domaines d’installation.</a></span><span class="sxs-lookup"><span data-stu-id="aa055-108">In the admin center, go to the **Setup** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">Domains</a> page.</span></span>

::: moniker-end
    
2. <span data-ttu-id="aa055-109">Dans la page **Domaines,** sélectionnez votre domaine, puis sélectionnez **Démarrer la configuration.**</span><span class="sxs-lookup"><span data-stu-id="aa055-109">On the **Domains** page, select your domain, then select **Start setup**.</span></span> <span data-ttu-id="aa055-110">Revenez à l'Assistant de configuration de domaines pour afficher la valeur spécifique que vous devez ajouter.</span><span class="sxs-lookup"><span data-stu-id="aa055-110">You'll go back to the domains setup wizard to see the specific value you need to add.</span></span>
    
3. <span data-ttu-id="aa055-111">Dans la page **Vérifier le domaine,** **sélectionnez Ajouter un enregistrement TXT** à la place, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="aa055-111">On the **Verify domain** page, select **Add a TXT record instead**, then select **Next**.</span></span>
    
4. <span data-ttu-id="aa055-112">Copiez **la valeur TXT** affichée.</span><span class="sxs-lookup"><span data-stu-id="aa055-112">Copy the **TXT value** shown.</span></span> <span data-ttu-id="aa055-113">Il se ressemble à ceci : **MS=msXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="aa055-113">It looks like this: **MS=msXXXXXXXX**.</span></span> 
    
5. <span data-ttu-id="aa055-114">Go to [Create DNS records at any DNS hosting provider](create-dns-records-at-any-dns-hosting-provider.md), and select your DNS host from the list of registrars to see the step-by-step instructions.</span><span class="sxs-lookup"><span data-stu-id="aa055-114">Go to [Create DNS records at any DNS hosting provider](create-dns-records-at-any-dns-hosting-provider.md), and select your DNS host from the list of registrars to see the step-by-step instructions.</span></span>
    
6. <span data-ttu-id="aa055-115">Suivez les étapes de création de l’enregistrement TXT (ou enregistrement MX) sur votre hôte DNS, puis vérifiez de nouveau le domaine dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="aa055-115">Follow the steps for creating the TXT record (or MX record) at your DNS host, then verify the domain back in Microsoft 365.</span></span>

7. <span data-ttu-id="aa055-116">Supprimez l’enregistrement TXT (ou enregistrement MX) de votre hôte DNS une fois que le domaine est vérifié Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="aa055-116">Remove the TXT record (or MX record) from your DNS host once the domain is verified in Microsoft 365.</span></span>
    
### <a name="step-2-find-the-mx-record-value-for-email-and-more"></a><span data-ttu-id="aa055-117">Étape 2 : Rechercher la valeur d’enregistrement MX pour le courrier électronique et bien plus encore</span><span class="sxs-lookup"><span data-stu-id="aa055-117">Step 2: Find the MX record value for email and more</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="aa055-118">Dans le Microsoft 365 d’administration,  allez à la page \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines d’installation.</a></span><span class="sxs-lookup"><span data-stu-id="aa055-118">In the Microsoft 365 admin center, go to the **Setup** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

::: moniker-end
    
::: moniker range="o365-germany"

1. <span data-ttu-id="aa055-119">Dans le centre d’administration, allez à la page  > <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">Domaines d’installation.</a></span><span class="sxs-lookup"><span data-stu-id="aa055-119">In the admin center, go to the **Setup** > <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">Domains</a> page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="aa055-120">Dans le centre d’administration, allez à la page  > <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">Domaines d’installation.</a></span><span class="sxs-lookup"><span data-stu-id="aa055-120">In the admin center, go to the **Setup** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">Domains</a> page.</span></span>

::: moniker-end
    
2. <span data-ttu-id="aa055-121">Dans la page **Domaines**, sélectionnez votre domaine.</span><span class="sxs-lookup"><span data-stu-id="aa055-121">On the **Domains** page, select your domain.</span></span> 
    
3. <span data-ttu-id="aa055-122">Les enregistrements DNS à ajouter se trouvent sous **Paramètres DNS requis**.</span><span class="sxs-lookup"><span data-stu-id="aa055-122">Under **Required DNS settings**, you'll see the DNS records to add.</span></span>
    
    <span data-ttu-id="aa055-123">Il est recommandé de conserver ces informations disponibles tandis que vous apportez des modifications à votre hôte DNS, pour que vous puissiez copier et coller les valeurs.</span><span class="sxs-lookup"><span data-stu-id="aa055-123">You'll want to keep this information available while you make changes at your DNS host, so you can copy and paste the values.</span></span>
    
    <span data-ttu-id="aa055-124">Les groupes d'enregistrements DNS figurant dans cette page dépendent des choix disponibles sous **Intention de domaine**.</span><span class="sxs-lookup"><span data-stu-id="aa055-124">The groups of DNS records that are listed on the page depend on your choices listed under **Domain purpose**.</span></span>
    
4. <span data-ttu-id="aa055-125">Go to [Create DNS records at any DNS hosting provider,](create-dns-records-at-any-dns-hosting-provider.md)and then select your DNS host from the list of registrars to see step-by-step instructions for adding records at that DNS host’s website.</span><span class="sxs-lookup"><span data-stu-id="aa055-125">Go to [Create DNS records at any DNS hosting provider](create-dns-records-at-any-dns-hosting-provider.md), and then select your DNS host from the list of registrars to see step-by-step instructions for adding records at that DNS host's website.</span></span>
    
5. <span data-ttu-id="aa055-126">Suivez la procédure de création des enregistrements auprès de votre hôte DNS.</span><span class="sxs-lookup"><span data-stu-id="aa055-126">Follow the steps for creating the records at your DNS host.</span></span>

## <a name="related-content"></a><span data-ttu-id="aa055-127">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="aa055-127">Related content</span></span>

<span data-ttu-id="aa055-128">[FAQ sur les domaines](../setup/domains-faq.yml) (article)</span><span class="sxs-lookup"><span data-stu-id="aa055-128">[Domains FAQ](../setup/domains-faq.yml) (article)</span></span>\
<span data-ttu-id="aa055-129">[Rechercher et corriger les problèmes, y compris de messagerie, après avoir ajouté votre domaine ou des enregistrements DNS](find-and-fix-issues.md) (article)</span><span class="sxs-lookup"><span data-stu-id="aa055-129">[Find and fix issues after adding your domain or DNS records](find-and-fix-issues.md) (article)</span></span>\
<span data-ttu-id="aa055-130">[Gérer des domaines](index.yml) (page de lien)</span><span class="sxs-lookup"><span data-stu-id="aa055-130">[Manage domains](index.yml) (link page)</span></span>