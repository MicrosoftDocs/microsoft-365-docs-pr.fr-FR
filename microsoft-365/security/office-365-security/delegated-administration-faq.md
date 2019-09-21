---
title: FAQ sur l'administration déléguée
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 8/28/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: d6a87ce8-2c22-433a-b430-5eab14f6afdc
description: Cette rubrique contient des questions fréquemment posées et la réponse à ces questions pour les partenaires et les revendeurs Microsoft qui veulent effectuer des tâches d'administration Office 365 déléguée, y compris la capacité à gérer Exchange Online Protection (EOP) pour d'autres locataires (entreprises).
ms.openlocfilehash: 8fcc409c9a5705ad824f7f74b3370afa07e650e3
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37080138"
---
# <a name="delegated-administration-faq"></a><span data-ttu-id="57aa6-103">FAQ sur l’administration déléguée</span><span class="sxs-lookup"><span data-stu-id="57aa6-103">Delegated administration FAQ</span></span>

<span data-ttu-id="57aa6-104">Cette rubrique contient des questions fréquemment posées et la réponse à ces questions pour les partenaires et les revendeurs Microsoft qui veulent effectuer des tâches d'administration Office 365 déléguée, y compris la capacité à gérer Exchange Online Protection (EOP) pour d'autres locataires (entreprises).</span><span class="sxs-lookup"><span data-stu-id="57aa6-104">This topic provides frequently asked questions and answers for Microsoft partners and resellers who want to perform delegated Office 365 administration tasks, including the ability to manage Exchange Online Protection (EOP) for other tenants (companies).</span></span>
  
 <span data-ttu-id="57aa6-105">**Q. Je suis revendeur et je dois gérer les locataires de mon client. Comment cela fonctionne-t-il ?**</span><span class="sxs-lookup"><span data-stu-id="57aa6-105">**Q. I'm a reseller and I need to manage my customer's tenants; how does this work?**</span></span>
  
<span data-ttu-id="57aa6-106">A.</span><span class="sxs-lookup"><span data-stu-id="57aa6-106">A.</span></span> <span data-ttu-id="57aa6-107">Si vous êtes un partenaire ou un revendeur Microsoft et que vous êtes inscrit en tant que conseiller Microsoft, vous pouvez demander l’autorisation d’administrer son client au sein du centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="57aa6-107">If you are a Microsoft partner or reseller, and you've signed up to be a Microsoft advisor, you can request permission to administer their tenant within the admin center.</span></span> <span data-ttu-id="57aa6-108">C'est ce qu'on appelle l'administration déléguée.</span><span class="sxs-lookup"><span data-stu-id="57aa6-108">This is known as delegated administration, and it allows you to manage their Office 365 tenant (including EOP settings) as if you were an administrator within their organization.</span></span> <span data-ttu-id="57aa6-109">Elle vous permet de gérer son locataire Office 365 (notamment les paramètres EOP) comme si vous étiez administrateur au sein de son organisation Les étapes permettant d'effectuer une administration déléguée sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="57aa6-109">The steps for performing delegated administration are as follows:</span></span>
  
1. <span data-ttu-id="57aa6-110">Inscrivez-vous pour devenir [partenaire Microsoft Office 365](https://aka.ms/cloudbenefits).</span><span class="sxs-lookup"><span data-stu-id="57aa6-110">Sign up to be a [Microsoft Office 365 Advisor](https://aka.ms/cloudbenefits).</span></span>

2. <span data-ttu-id="57aa6-p102">Inscrivez-vous à l'administration déléguée Office 365. Avant que vous puissiez administrer le compte d'un client, celui-ci doit vous fournir les autorisations d'administrateur délégué. Pour obtenir leur approbation, vous devez d'abord [leur envoyer une offre d'administration déléguée](https://go.microsoft.com/fwlink/?LinkId=396829). (Vous pouvez également proposer l'administration déléguée à votre client ultérieurement.)</span><span class="sxs-lookup"><span data-stu-id="57aa6-p102">Sign up for Office 365 delegated administration. Before you can start administering a customer's account, they must authorize you as a delegated administrator. To obtain their approval, you first [send them an offer for delegated administration](https://go.microsoft.com/fwlink/?LinkId=396829). (You can also offer delegated administration to your customer at a later time.)</span></span>

3. <span data-ttu-id="57aa6-115">Créez le compte d’administrateur délégué en suivant les étapes décrites dans [Ajouter ou supprimer un administrateur délégué](https://go.microsoft.com/fwlink/?LinkId=396831).</span><span class="sxs-lookup"><span data-stu-id="57aa6-115">Create the delegated admin account using the steps in [Add or delete a delegated admin](https://go.microsoft.com/fwlink/?LinkId=396831).</span></span>

<span data-ttu-id="57aa6-116">Consultez l'article [Partenaires : développez votre activité et gérez votre compte Office 365](https://go.microsoft.com/fwlink/?LinkId=301485) pour plus d'informations sur la configuration d'une administration déléguée Office 365.</span><span class="sxs-lookup"><span data-stu-id="57aa6-116">Visit [Partners: Build your business and administer your Office 365 partner account](https://go.microsoft.com/fwlink/?LinkId=301485) for more information about how to set up Office 365 delegated administration.</span></span>
  
 <span data-ttu-id="57aa6-117">**Q. Je suis un client, pas un revendeur, comment puis-je configurer un administrateur délégué pour mes sous-locataires ?**</span><span class="sxs-lookup"><span data-stu-id="57aa6-117">**Q. I'm a customer, not a reseller, how can set up delegated administrator for my sub-tenants?**</span></span>
  
<span data-ttu-id="57aa6-p103">R. Pour le moment, l'administration déléguée est uniquement disponible pour les revendeurs et les partenaires. Cependant, nous avons fourni un exemple de script Windows PowerShell qui vous aidera à appliquer des stratégies à vos sous-locataires (entreprises). Pour plus d'informations, voir [Exemple de script pour l'application de paramètres EOP à plusieurs locataires](sample-script-for-applying-eop-settings-to-multiple-tenants.md).</span><span class="sxs-lookup"><span data-stu-id="57aa6-p103">A. Delegated administration is only available for resellers and partners at this time. However, we've provided a sample Windows PowerShell script that will help you apply policies to your sub-tenants (companies). For more information, see [Sample script for applying EOP settings to multiple tenants](sample-script-for-applying-eop-settings-to-multiple-tenants.md).</span></span>
  
 <span data-ttu-id="57aa6-122">**Q. Puis-je empêcher mon administration de sous-locataires de modifier ma stratégie ?**</span><span class="sxs-lookup"><span data-stu-id="57aa6-122">**Q. Can I prevent my sub-tenant admin from modifying my policy?**</span></span>
  
<span data-ttu-id="57aa6-p104">R. Office 365 ne dispose actuellement pas de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="57aa6-p104">A. Office 365 does not currently have this capability.</span></span>
  
 <span data-ttu-id="57aa6-125">**Q. Puis-je disposer de la création de rapports consolidés dans l'ensemble de mes sous-locataires ?**</span><span class="sxs-lookup"><span data-stu-id="57aa6-125">**Q. Can I get consolidated reporting across all of my sub-tenants?**</span></span>
  
<span data-ttu-id="57aa6-126">R.</span><span class="sxs-lookup"><span data-stu-id="57aa6-126">A.</span></span> <span data-ttu-id="57aa6-127">La création de rapports consolidés dans les sociétés que vous gérez n’est pas disponible pour les rapports du centre d’administration 365 de Microsoft pour le moment.</span><span class="sxs-lookup"><span data-stu-id="57aa6-127">Consolidated reporting across the companies you manage is not available for the Microsoft 365 admin center reports at this time.</span></span> <span data-ttu-id="57aa6-128">Toutefois, vous pouvez le faire à l’aide de Windows PowerShell à distance ou du [service Web de création de rapports Office 365](https://go.microsoft.com/fwlink/?LinkId=279926).</span><span class="sxs-lookup"><span data-stu-id="57aa6-128">However, you can do this by using remote Windows PowerShell or the [Office 365 Reporting web service](https://go.microsoft.com/fwlink/?LinkId=279926).</span></span>

