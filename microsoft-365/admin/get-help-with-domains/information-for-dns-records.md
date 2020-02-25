---
title: Recueillez les informations nécessaires pour créer des enregistrements DNS Office 365
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
- Adm_O365_Setup
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
ms.assetid: 77f90d4a-dc7f-4f09-8972-c1b03ea85a67
description: 'Découvrez comment trouver les valeurs/informations dont vous avez besoin pour créer des enregistrements DNS pour Office 365. '
ms.custom: okr_smb
ms.openlocfilehash: 7b995aedc21305367e4a6621781e138d0d60efd1
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42252917"
---
# <a name="gather-the-information-you-need-to-create-office-365-dns-records"></a><span data-ttu-id="c2751-103">Recueillez les informations nécessaires pour créer des enregistrements DNS Office 365</span><span class="sxs-lookup"><span data-stu-id="c2751-103">Gather the information you need to create Office 365 DNS records</span></span>

 <span data-ttu-id="c2751-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="c2751-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
### <a name="step-1-find-the-txt-record-value-and-verify"></a><span data-ttu-id="c2751-105">Étape 1 : Rechercher la valeur de l’enregistrement TXT et vérifier</span><span class="sxs-lookup"><span data-stu-id="c2751-105">Step 1: Find the TXT record value and verify</span></span>

1. <span data-ttu-id="c2751-106">Dans le centre d’administration Microsoft 365, accédez à la page <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">domaines</a> **d’installation** \> .</span><span class="sxs-lookup"><span data-stu-id="c2751-106">In the Microsoft 365 admin center, go to the **Setup** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
    <span data-ttu-id="c2751-107">Si vous utilisez Office 365 Germany, accédez à la page de ces <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">domaines</a> .</span><span class="sxs-lookup"><span data-stu-id="c2751-107">If you're using Office 365 Germany, go to this <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">Domains</a> page.</span></span> 
    
    <span data-ttu-id="c2751-108">Si vous utilisez Office 365 géré par 21Vianet, accédez à la page de ce <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">domaine</a> .</span><span class="sxs-lookup"><span data-stu-id="c2751-108">If you're using Office 365 operated by 21Vianet, go to this <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="c2751-109">Sur la page **domaines** , sélectionnez votre domaine, puis **Démarrer le programme d’installation**.</span><span class="sxs-lookup"><span data-stu-id="c2751-109">On the **Domains** page, select your domain, then select **Start setup**.</span></span> <span data-ttu-id="c2751-110">Revenez à l'Assistant de configuration de domaines pour afficher la valeur spécifique que vous devez ajouter.</span><span class="sxs-lookup"><span data-stu-id="c2751-110">You'll go back to the domains setup wizard to see the specific value you need to add.</span></span>
    
3. <span data-ttu-id="c2751-111">Sur la page **vérifier le domaine** , sélectionnez **Ajouter un enregistrement txt**à la place, puis sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c2751-111">On the **Verify domain** page, select **Add a TXT record instead**, then select **Next**.</span></span>
    
4. <span data-ttu-id="c2751-112">Copiez la **valeur txt** affichée.</span><span class="sxs-lookup"><span data-stu-id="c2751-112">Copy the **TXT value** shown.</span></span> <span data-ttu-id="c2751-113">Il se présente comme ceci : **MS = msXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="c2751-113">It looks like this: **MS=msXXXXXXXX**.</span></span> 
    
5. <span data-ttu-id="c2751-114">Accédez à [créer des enregistrements DNS auprès d’un fournisseur d’hébergement DNS](create-dns-records-at-any-dns-hosting-provider.md)et sélectionnez votre hôte DNS dans la liste des bureaux d’enregistrement pour voir les instructions pas à pas.</span><span class="sxs-lookup"><span data-stu-id="c2751-114">Go to [Create DNS records at any DNS hosting provider](create-dns-records-at-any-dns-hosting-provider.md), and select your DNS host from the list of registrars to see the step-by-step instructions.</span></span>
    
6. <span data-ttu-id="c2751-115">Suivez les étapes permettant de créer l'enregistrement TXT (ou l'enregistrement MX) auprès de votre hôte DNS, puis vérifiez le domaine dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="c2751-115">Follow the steps for creating the TXT record (or MX record) at your DNS host, then verify the domain back in Office 365.</span></span>

7. <span data-ttu-id="c2751-116">Supprimez l’enregistrement TXT (ou l’enregistrement MX) de votre hôte DNS une fois le domaine vérifié dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="c2751-116">Remove the TXT record (or MX record) from your DNS host once the domain is verified in Office 365.</span></span>
    
### <a name="step-2-find-the-mx-record-value-for-email-and-more"></a><span data-ttu-id="c2751-117">Étape 2 : trouver la valeur de l’enregistrement MX pour la messagerie électronique et plus</span><span class="sxs-lookup"><span data-stu-id="c2751-117">Step 2: Find the MX record value for email and more</span></span>

1. <span data-ttu-id="c2751-118">Dans le centre d’administration Microsoft 365, accédez à la page <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">domaines</a> **d’installation** \> .</span><span class="sxs-lookup"><span data-stu-id="c2751-118">In the Microsoft 365 admin center, go to the **Setup** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
    <span data-ttu-id="c2751-119">Si vous utilisez Office 365 Germany, accédez à la page de ces <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">domaines</a> .</span><span class="sxs-lookup"><span data-stu-id="c2751-119">If you're using Office 365 Germany, go to this <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">Domains</a> page.</span></span> 
    
    <span data-ttu-id="c2751-120">Si vous utilisez Office 365 géré par 21Vianet, accédez à la page de ce <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">domaine</a> .</span><span class="sxs-lookup"><span data-stu-id="c2751-120">If you're using Office 365 operated by 21Vianet, go to this <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="c2751-121">Dans la page **Domaines**, sélectionnez votre domaine.</span><span class="sxs-lookup"><span data-stu-id="c2751-121">On the **Domains** page, select your domain.</span></span> 
    
3. <span data-ttu-id="c2751-122">Les enregistrements DNS à ajouter se trouvent sous **Paramètres DNS requis**.</span><span class="sxs-lookup"><span data-stu-id="c2751-122">Under **Required DNS settings**, you'll see the DNS records to add.</span></span>
    
    <span data-ttu-id="c2751-123">Il est recommandé de conserver ces informations disponibles tandis que vous apportez des modifications à votre hôte DNS, pour que vous puissiez copier et coller les valeurs.</span><span class="sxs-lookup"><span data-stu-id="c2751-123">You'll want to keep this information available while you make changes at your DNS host, so you can copy and paste the values.</span></span>
    
    <span data-ttu-id="c2751-124">Les groupes d'enregistrements DNS figurant dans cette page dépendent des choix disponibles sous **Intention de domaine**.</span><span class="sxs-lookup"><span data-stu-id="c2751-124">The groups of DNS records that are listed on the page depend on your choices listed under **Domain purpose**.</span></span>
    
4. <span data-ttu-id="c2751-125">Accédez à [créer des enregistrements DNS auprès d’un fournisseur d’hébergement DNS](create-dns-records-at-any-dns-hosting-provider.md), puis sélectionnez votre hôte DNS dans la liste des bureaux d’enregistrement pour voir les instructions pas à pas pour ajouter des enregistrements sur le site Web de l’hôte DNS.</span><span class="sxs-lookup"><span data-stu-id="c2751-125">Go to [Create DNS records at any DNS hosting provider](create-dns-records-at-any-dns-hosting-provider.md), and then select your DNS host from the list of registrars to see step-by-step instructions for adding records at that DNS host's website.</span></span>
    
5. <span data-ttu-id="c2751-126">Suivez la procédure de création des enregistrements auprès de votre hôte DNS.</span><span class="sxs-lookup"><span data-stu-id="c2751-126">Follow the steps for creating the records at your DNS host.</span></span>
