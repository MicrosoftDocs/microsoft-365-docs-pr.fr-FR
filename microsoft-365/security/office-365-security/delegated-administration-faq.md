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
ms.openlocfilehash: 4e2548ebe52926e00269615a436662183ec5bd2a
ms.sourcegitcommit: 5710ce729c55d95b8b452d99ffb7ea92b5cb254a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2019
ms.locfileid: "39970750"
---
# <a name="delegated-administration-faq"></a><span data-ttu-id="8bf68-103">FAQ sur l’administration déléguée</span><span class="sxs-lookup"><span data-stu-id="8bf68-103">Delegated administration FAQ</span></span>

<span data-ttu-id="8bf68-104">Cette rubrique contient des questions fréquemment posées et la réponse à ces questions pour les partenaires et les revendeurs Microsoft qui veulent effectuer des tâches d'administration Office 365 déléguée, y compris la capacité à gérer Exchange Online Protection (EOP) pour d'autres locataires (entreprises).</span><span class="sxs-lookup"><span data-stu-id="8bf68-104">This topic provides frequently asked questions and answers for Microsoft partners and resellers who want to perform delegated Office 365 administration tasks, including the ability to manage Exchange Online Protection (EOP) for other tenants (companies).</span></span>

<span data-ttu-id="8bf68-105">**Q. Je suis revendeur et je dois gérer les locataires de mon client. Comment cela fonctionne-t-il ?**</span><span class="sxs-lookup"><span data-stu-id="8bf68-105">**Q. I'm a reseller and I need to manage my customer's tenants; how does this work?**</span></span>

<span data-ttu-id="8bf68-106">A.</span><span class="sxs-lookup"><span data-stu-id="8bf68-106">A.</span></span> <span data-ttu-id="8bf68-107">Si vous êtes un partenaire ou un revendeur Microsoft et que vous êtes inscrit en tant que conseiller Microsoft, vous pouvez demander l’autorisation d’administrer son client au sein du centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="8bf68-107">If you are a Microsoft partner or reseller, and you've signed up to be a Microsoft advisor, you can request permission to administer their tenant within the admin center.</span></span> <span data-ttu-id="8bf68-108">C'est ce qu'on appelle l'administration déléguée.</span><span class="sxs-lookup"><span data-stu-id="8bf68-108">This is known as delegated administration, and it allows you to manage their Office 365 tenant (including EOP settings) as if you were an administrator within their organization.</span></span> <span data-ttu-id="8bf68-109">Elle vous permet de gérer son locataire Office 365 (notamment les paramètres EOP) comme si vous étiez administrateur au sein de son organisation Les étapes permettant d'effectuer une administration déléguée sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8bf68-109">The steps for performing delegated administration are as follows:</span></span>

1. <span data-ttu-id="8bf68-110">Inscrivez-vous pour devenir [partenaire Microsoft Office 365](https://aka.ms/cloudbenefits).</span><span class="sxs-lookup"><span data-stu-id="8bf68-110">Sign up to be a [Microsoft Office 365 Advisor](https://aka.ms/cloudbenefits).</span></span>

2. <span data-ttu-id="8bf68-p102">Inscrivez-vous à l'administration déléguée Office 365. Avant que vous puissiez administrer le compte d'un client, celui-ci doit vous fournir les autorisations d'administrateur délégué. Pour obtenir leur approbation, vous devez d'abord [leur envoyer une offre d'administration déléguée](https://support.office.com/article/26530dc0-ebba-415b-86b1-b55bc06b073e). (Vous pouvez également proposer l'administration déléguée à votre client ultérieurement.)</span><span class="sxs-lookup"><span data-stu-id="8bf68-p102">Sign up for Office 365 delegated administration. Before you can start administering a customer's account, they must authorize you as a delegated administrator. To obtain their approval, you first [send them an offer for delegated administration](https://support.office.com/article/26530dc0-ebba-415b-86b1-b55bc06b073e). (You can also offer delegated administration to your customer at a later time.)</span></span>

3. <span data-ttu-id="8bf68-115">Créez le compte d’administrateur délégué en suivant les étapes décrites dans [Ajouter, modifier ou supprimer un partenaire conseiller d’abonnement](https://docs.microsoft.com/office365/admin/misc/add-partner).</span><span class="sxs-lookup"><span data-stu-id="8bf68-115">Create the delegated admin account using the steps in [Add, change, or delete a subscription advisor partner](https://docs.microsoft.com/office365/admin/misc/add-partner).</span></span>

<span data-ttu-id="8bf68-116">Visitez les [partenaires : développez votre entreprise et administrez votre abonnement partenaire office 365](https://support.office.com/article/30dd1681-47e0-4cbc-abfe-a222cd111319) pour plus d’informations sur la configuration de l’administration déléguée Office 365.</span><span class="sxs-lookup"><span data-stu-id="8bf68-116">Visit [Partners: Build your business and administer your Office 365 partner subscription](https://support.office.com/article/30dd1681-47e0-4cbc-abfe-a222cd111319) for more information about how to set up Office 365 delegated administration.</span></span>

<span data-ttu-id="8bf68-117">**Q. Je suis un client, pas un revendeur, comment puis-je configurer un administrateur délégué pour mes sous-locataires ?**</span><span class="sxs-lookup"><span data-stu-id="8bf68-117">**Q. I'm a customer, not a reseller, how can set up delegated administrator for my sub-tenants?**</span></span>

<span data-ttu-id="8bf68-p103">R. Pour le moment, l'administration déléguée est uniquement disponible pour les revendeurs et les partenaires. Cependant, nous avons fourni un exemple de script Windows PowerShell qui vous aidera à appliquer des stratégies à vos sous-locataires (entreprises). Pour plus d'informations, voir [Exemple de script pour l'application de paramètres EOP à plusieurs locataires](sample-script-for-applying-eop-settings-to-multiple-tenants.md).</span><span class="sxs-lookup"><span data-stu-id="8bf68-p103">A. Delegated administration is only available for resellers and partners at this time. However, we've provided a sample Windows PowerShell script that will help you apply policies to your sub-tenants (companies). For more information, see [Sample script for applying EOP settings to multiple tenants](sample-script-for-applying-eop-settings-to-multiple-tenants.md).</span></span>

<span data-ttu-id="8bf68-122">**Q. Puis-je empêcher mon administration de sous-locataires de modifier ma stratégie ?**</span><span class="sxs-lookup"><span data-stu-id="8bf68-122">**Q. Can I prevent my sub-tenant admin from modifying my policy?**</span></span>

<span data-ttu-id="8bf68-p104">R. Office 365 ne dispose actuellement pas de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="8bf68-p104">A. Office 365 does not currently have this capability.</span></span>

<span data-ttu-id="8bf68-125">**Q. Puis-je disposer de la création de rapports consolidés dans l'ensemble de mes sous-locataires ?**</span><span class="sxs-lookup"><span data-stu-id="8bf68-125">**Q. Can I get consolidated reporting across all of my sub-tenants?**</span></span>

<span data-ttu-id="8bf68-126">R.</span><span class="sxs-lookup"><span data-stu-id="8bf68-126">A.</span></span> <span data-ttu-id="8bf68-127">La création de rapports consolidés dans les sociétés que vous gérez n’est pas disponible pour les rapports du centre d’administration 365 de Microsoft pour le moment.</span><span class="sxs-lookup"><span data-stu-id="8bf68-127">Consolidated reporting across the companies you manage is not available for the Microsoft 365 admin center reports at this time.</span></span> <span data-ttu-id="8bf68-128">Toutefois, vous pouvez le faire à l’aide de [Microsoft Graph](https://docs.microsoft.com/graph/overview).</span><span class="sxs-lookup"><span data-stu-id="8bf68-128">However, you can do this by using [Microsoft Graph](https://docs.microsoft.com/graph/overview).</span></span>
