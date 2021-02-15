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
description: 'Découvrez les valeurs/informations dont vous avez besoin pour créer des enregistrements DNS pour Microsoft 365. '
ms.openlocfilehash: 45994139b11a2fd5a03b2e979dd6af334bc1f00b
ms.sourcegitcommit: eac5d9f759f290d3c51cafaf335a1a1c43ded927
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "50126370"
---
# <a name="gather-the-information-you-need-to-create-dns-records"></a><span data-ttu-id="0b08f-103">Collecter les informations dont vous avez besoin pour créer des enregistrements DNS</span><span class="sxs-lookup"><span data-stu-id="0b08f-103">Gather the information you need to create DNS records</span></span>

 <span data-ttu-id="0b08f-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="0b08f-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span> 
  
### <a name="step-1-find-the-txt-record-value-and-verify"></a><span data-ttu-id="0b08f-105">Étape 1 : rechercher la valeur de l’enregistrement TXT et vérifier</span><span class="sxs-lookup"><span data-stu-id="0b08f-105">Step 1: Find the TXT record value and verify</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="0b08f-106">Dans le Centre d’administration Microsoft 365, allez à la page  \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines d’installation.</a></span><span class="sxs-lookup"><span data-stu-id="0b08f-106">In the Microsoft 365 admin center, go to the **Setup** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="0b08f-107">Dans le centre d’administration, allez à la page  > <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">Domaines d’installation.</a></span><span class="sxs-lookup"><span data-stu-id="0b08f-107">In the admin center, go to the **Setup** > <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">Domains</a> page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="0b08f-108">Dans le centre d’administration, allez à la page  > <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">Domaines d’installation.</a></span><span class="sxs-lookup"><span data-stu-id="0b08f-108">In the admin center, go to the **Setup** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">Domains</a> page.</span></span>

::: moniker-end
    
2. <span data-ttu-id="0b08f-109">Dans la page **Domaines,** sélectionnez votre domaine, puis sélectionnez **Démarrer la configuration.**</span><span class="sxs-lookup"><span data-stu-id="0b08f-109">On the **Domains** page, select your domain, then select **Start setup**.</span></span> <span data-ttu-id="0b08f-110">Revenez à l'Assistant de configuration de domaines pour afficher la valeur spécifique que vous devez ajouter.</span><span class="sxs-lookup"><span data-stu-id="0b08f-110">You'll go back to the domains setup wizard to see the specific value you need to add.</span></span>
    
3. <span data-ttu-id="0b08f-111">Dans la page **Vérifier le domaine,** **sélectionnez Ajouter un enregistrement TXT** à la place, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0b08f-111">On the **Verify domain** page, select **Add a TXT record instead**, then select **Next**.</span></span>
    
4. <span data-ttu-id="0b08f-112">Copiez **la valeur TXT** affichée.</span><span class="sxs-lookup"><span data-stu-id="0b08f-112">Copy the **TXT value** shown.</span></span> <span data-ttu-id="0b08f-113">Il se ressemble à ceci : **MS=msXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="0b08f-113">It looks like this: **MS=msXXXXXXXX**.</span></span> 
    
5. <span data-ttu-id="0b08f-114">Go to [Create DNS records at any DNS hosting provider](create-dns-records-at-any-dns-hosting-provider.md), and select your DNS host from the list of registrars to see the step-by-step instructions.</span><span class="sxs-lookup"><span data-stu-id="0b08f-114">Go to [Create DNS records at any DNS hosting provider](create-dns-records-at-any-dns-hosting-provider.md), and select your DNS host from the list of registrars to see the step-by-step instructions.</span></span>
    
6. <span data-ttu-id="0b08f-115">Suivez les étapes de création de l’enregistrement TXT (ou enregistrement MX) sur votre hôte DNS, puis vérifiez à nouveau le domaine dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0b08f-115">Follow the steps for creating the TXT record (or MX record) at your DNS host, then verify the domain back in Microsoft 365.</span></span>

7. <span data-ttu-id="0b08f-116">Supprimez l’enregistrement TXT (ou enregistrement MX) de votre hôte DNS une fois que le domaine est vérifié dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0b08f-116">Remove the TXT record (or MX record) from your DNS host once the domain is verified in Microsoft 365.</span></span>
    
### <a name="step-2-find-the-mx-record-value-for-email-and-more"></a><span data-ttu-id="0b08f-117">Étape 2 : Rechercher la valeur d’enregistrement MX pour le courrier électronique et bien plus encore</span><span class="sxs-lookup"><span data-stu-id="0b08f-117">Step 2: Find the MX record value for email and more</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="0b08f-118">Dans le Centre d’administration Microsoft 365, allez à la page  \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines d’installation.</a></span><span class="sxs-lookup"><span data-stu-id="0b08f-118">In the Microsoft 365 admin center, go to the **Setup** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

::: moniker-end
    
::: moniker range="o365-germany"

1. <span data-ttu-id="0b08f-119">Dans le centre d’administration, allez à la page  > <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">Domaines d’installation.</a></span><span class="sxs-lookup"><span data-stu-id="0b08f-119">In the admin center, go to the **Setup** > <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">Domains</a> page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="0b08f-120">Dans le centre d’administration, allez à la page  > <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">Domaines d’installation.</a></span><span class="sxs-lookup"><span data-stu-id="0b08f-120">In the admin center, go to the **Setup** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">Domains</a> page.</span></span>

::: moniker-end
    
2. <span data-ttu-id="0b08f-121">Dans la page **Domaines**, sélectionnez votre domaine.</span><span class="sxs-lookup"><span data-stu-id="0b08f-121">On the **Domains** page, select your domain.</span></span> 
    
3. <span data-ttu-id="0b08f-122">Les enregistrements DNS à ajouter se trouvent sous **Paramètres DNS requis**.</span><span class="sxs-lookup"><span data-stu-id="0b08f-122">Under **Required DNS settings**, you'll see the DNS records to add.</span></span>
    
    <span data-ttu-id="0b08f-123">Il est recommandé de conserver ces informations disponibles tandis que vous apportez des modifications à votre hôte DNS, pour que vous puissiez copier et coller les valeurs.</span><span class="sxs-lookup"><span data-stu-id="0b08f-123">You'll want to keep this information available while you make changes at your DNS host, so you can copy and paste the values.</span></span>
    
    <span data-ttu-id="0b08f-124">Les groupes d'enregistrements DNS figurant dans cette page dépendent des choix disponibles sous **Intention de domaine**.</span><span class="sxs-lookup"><span data-stu-id="0b08f-124">The groups of DNS records that are listed on the page depend on your choices listed under **Domain purpose**.</span></span>
    
4. <span data-ttu-id="0b08f-125">Go to [Create DNS records at any DNS hosting provider,](create-dns-records-at-any-dns-hosting-provider.md)and then select your DNS host from the list of registrars to see step-by-step instructions for adding records at that DNS host’s website.</span><span class="sxs-lookup"><span data-stu-id="0b08f-125">Go to [Create DNS records at any DNS hosting provider](create-dns-records-at-any-dns-hosting-provider.md), and then select your DNS host from the list of registrars to see step-by-step instructions for adding records at that DNS host's website.</span></span>
    
5. <span data-ttu-id="0b08f-126">Suivez la procédure de création des enregistrements auprès de votre hôte DNS.</span><span class="sxs-lookup"><span data-stu-id="0b08f-126">Follow the steps for creating the records at your DNS host.</span></span>
