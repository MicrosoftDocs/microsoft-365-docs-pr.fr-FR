---
title: Intégration d’Azure à Microsoft 365
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Ent_O365
- M365-identity-device-management
f1.keywords:
- CSH
ms.custom:
- Adm_O365
- seo-marvel-apr2020
search.appverid:
- MET150
- MOE150
- MED150
- BCS160
ms.assetid: a5efce5d-9c9c-4190-b61b-fd273c1d425f
description: Intégrez Microsoft 365 à Azure AD si vous souhaitez synchroniser le mot de passe ou l' sign-on unique avec votre environnement local.
ms.openlocfilehash: f977969634401d59d7598136f9323cb0e37f9ece
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50905331"
---
# <a name="azure-integration-with-microsoft-365"></a><span data-ttu-id="4b36b-103">Intégration d’Azure à Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4b36b-103">Azure integration with Microsoft 365</span></span>

<span data-ttu-id="4b36b-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="4b36b-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="4b36b-105">Microsoft 365 utilise Azure Active Directory (Azure AD) pour gérer les identités des utilisateurs en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="4b36b-105">Microsoft 365 uses Azure Active Directory (Azure AD) to manage user identities behind the scenes.</span></span> <span data-ttu-id="4b36b-106">Votre abonnement Microsoft 365 inclut un abonnement Azure AD gratuit qui vous permet d’intégrer vos services de domaine Active Directory (AD DS) locaux pour synchroniser les comptes d’utilisateurs et les mots de passe ou configurer l' sign-on unique.</span><span class="sxs-lookup"><span data-stu-id="4b36b-106">Your Microsoft 365 subscription includes a free Azure AD subscription so that you can integrate your on-premises Active Directory Domain Services (AD DS) to synchronize user accounts and passwords or set up single sign-on.</span></span> <span data-ttu-id="4b36b-107">Vous pouvez également acheter des fonctionnalités avancées pour mieux gérer vos comptes.</span><span class="sxs-lookup"><span data-stu-id="4b36b-107">You can also purchase advanced features to better manage your accounts.</span></span>
  
<span data-ttu-id="4b36b-108">Azure AD offre également d’autres fonctionnalités, telles que la gestion des applications intégrées, que vous pouvez utiliser pour étendre et personnaliser vos abonnements Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4b36b-108">Azure AD also offers other functionality, like managing integrated apps, that you can use to extend and customize your Microsoft 365 subscriptions.</span></span>
  
<span data-ttu-id="4b36b-109">Vous pouvez utiliser les conseillers de déploiement Azure AD pour une configuration guidée dans le Centre d’administration Microsoft 365 (vous devez être inscrit à Microsoft 365) :</span><span class="sxs-lookup"><span data-stu-id="4b36b-109">You can use the Azure AD deployment advisors for a guided setup and configuration experience in the Microsoft 365 admin center (you must be signed in to Microsoft 365):</span></span>

 - [<span data-ttu-id="4b36b-110">Conseiller Azure AD Connect</span><span class="sxs-lookup"><span data-stu-id="4b36b-110">Azure AD Connect advisor</span></span>](https://aka.ms/aadconnectpwsync)
 - [<span data-ttu-id="4b36b-111">Conseiller de déploiement AD FS</span><span class="sxs-lookup"><span data-stu-id="4b36b-111">AD FS deployment advisor</span></span>](https://aka.ms/adfsguidance)
 - [<span data-ttu-id="4b36b-112">Guide de configuration d’Azure AD</span><span class="sxs-lookup"><span data-stu-id="4b36b-112">Azure AD setup guide</span></span>](https://aka.ms/aadpguidance)
  
## <a name="azure-ad-editions-and-microsoft-365-identity-management"></a><span data-ttu-id="4b36b-113">Éditions Azure AD et gestion des identités Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4b36b-113">Azure AD editions and Microsoft 365 identity management</span></span>

<span data-ttu-id="4b36b-114">Si vous avez un abonnement payant à Microsoft 365, vous avez également un abonnement Azure AD gratuit.</span><span class="sxs-lookup"><span data-stu-id="4b36b-114">If you have a paid subscription to Microsoft 365, you also have a free Azure AD subscription.</span></span> <span data-ttu-id="4b36b-115">Vous pouvez utiliser Azure AD pour créer et gérer des comptes d’utilisateur et de groupe.</span><span class="sxs-lookup"><span data-stu-id="4b36b-115">You can use Azure AD to create and manage user and group accounts.</span></span> <span data-ttu-id="4b36b-116">Pour activer cet abonnement, vous devez effectuer une inscription à une seule fois.</span><span class="sxs-lookup"><span data-stu-id="4b36b-116">To activate this subscription, you have to complete a one-time registration.</span></span> <span data-ttu-id="4b36b-117">Ensuite, vous pouvez accéder à Azure AD à partir de votre Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4b36b-117">Afterward, you can access Azure AD from your Microsoft 365 admin center.</span></span> 

<span data-ttu-id="4b36b-118">Pour obtenir des instructions pour inscrire votre abonnement Azure AD gratuit, consultez votre abonnement [Azure AD gratuit.](../compliance/use-your-free-azure-ad-subscription-in-office-365.md)</span><span class="sxs-lookup"><span data-stu-id="4b36b-118">For instructions to register your free Azure AD subscription, see [use your free Azure AD subscription](../compliance/use-your-free-azure-ad-subscription-in-office-365.md).</span></span> <span data-ttu-id="4b36b-119">N’allez pas directement à azure.microsoft.com pour vous inscrire ou vous vous retrouverez avec un abonnement d’essai ou payant à Microsoft Azure distinct de votre abonnement Azure AD gratuit avec Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4b36b-119">Don't go directly to azure.microsoft.com to sign up or you'll end up with a trial or paid subscription to Microsoft Azure that is separate from your free Azure AD subscription with Microsoft 365.</span></span> 
  
<span data-ttu-id="4b36b-120">Avec l’abonnement gratuit, vous pouvez synchroniser avec les annuaires locaux, configurer l' sign-on unique et synchroniser avec de nombreux logiciels en tant qu’applications de service, tels que Salesforce, DropBox et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="4b36b-120">With the free subscription you can synchronize with on-premises directories, set up single sign-on, and synchronize with many software as service applications, such as Salesforce, DropBox, and many more.</span></span>
  
<span data-ttu-id="4b36b-121">Si vous souhaitez améliorer les fonctionnalités AD DS, la synchronisation bi-directionnelle et d’autres fonctionnalités de gestion, vous pouvez mettre à niveau votre abonnement gratuit vers un abonnement premium payant.</span><span class="sxs-lookup"><span data-stu-id="4b36b-121">If you want enhanced AD DS functionality, bi-directional synchronization, and other management capabilities, you can upgrade your free subscription to a paid premium subscription.</span></span> <span data-ttu-id="4b36b-122">Pour plus d’informations, [consultez les éditions Azure Active Directory.](https://azure.microsoft.com/pricing/details/active-directory/)</span><span class="sxs-lookup"><span data-stu-id="4b36b-122">For the details, see [Azure Active Directory editions](https://azure.microsoft.com/pricing/details/active-directory/).</span></span>
  
<span data-ttu-id="4b36b-123">Pour plus d’informations sur Microsoft 365 et Azure AD, voir modèles d’identité [Microsoft 365.](about-microsoft-365-identity.md)</span><span class="sxs-lookup"><span data-stu-id="4b36b-123">For more information about Microsoft 365 and Azure AD, see [Microsoft 365 identity models](about-microsoft-365-identity.md).</span></span>
  
## <a name="extend-the-capabilities-of-your-microsoft-365-tenant"></a><span data-ttu-id="4b36b-124">Étendre les fonctionnalités de votre client Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4b36b-124">Extend the capabilities of your Microsoft 365 tenant</span></span>

|<span data-ttu-id="4b36b-125">**Fonctionnalité**</span><span class="sxs-lookup"><span data-stu-id="4b36b-125">**Feature**</span></span>|<span data-ttu-id="4b36b-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="4b36b-126">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4b36b-127">Applications intégrées</span><span class="sxs-lookup"><span data-stu-id="4b36b-127">Integrated apps</span></span>  <br/> |<span data-ttu-id="4b36b-128">Vous pouvez accorder à des applications individuelles l’accès à vos données Microsoft 365, telles que la messagerie, les calendriers, les contacts, les utilisateurs, les groupes, les fichiers et les dossiers.</span><span class="sxs-lookup"><span data-stu-id="4b36b-128">You can grant individual apps access to your Microsoft 365 data, such as mail, calendars, contacts, users, groups, files, and folders.</span></span> <span data-ttu-id="4b36b-129">Vous pouvez également autoriser ces applications au niveau de l’administrateur global et les mettre à la disposition de l’ensemble de votre entreprise en les enregistrant dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="4b36b-129">You can also authorize these apps at global admin level and make them available to your entire company by registering the apps in Azure AD.</span></span> <span data-ttu-id="4b36b-130">Pour plus d’informations, voir [Applications intégrées et Azure AD pour les administrateurs Microsoft 365.](integrated-apps-and-azure-ads.md)</span><span class="sxs-lookup"><span data-stu-id="4b36b-130">Formore information, see [Integrated Apps and Azure AD for Microsoft 365 administrators](integrated-apps-and-azure-ads.md).</span></span>  <br/> <span data-ttu-id="4b36b-131">Voir aussi [1 000 000 000](/azure/active-directory/manage-apps/what-is-single-sign-on).</span><span class="sxs-lookup"><span data-stu-id="4b36b-131">Also see [Single sign-on](/azure/active-directory/manage-apps/what-is-single-sign-on).</span></span>  <br/> |
|<span data-ttu-id="4b36b-132">PowerApps</span><span class="sxs-lookup"><span data-stu-id="4b36b-132">PowerApps</span></span>  <br/> | <span data-ttu-id="4b36b-133">Les applications d’alimentation sont des applications axées sur les appareils mobiles qui peuvent se connecter à vos sources de données existantes, telles que des listes SharePoint et d’autres applications de données.</span><span class="sxs-lookup"><span data-stu-id="4b36b-133">Power apps are focused apps for mobile devices that can connect to your existing data sources like SharePoint lists and other data apps.</span></span> <span data-ttu-id="4b36b-134">Pour [plus d’informations,](https://support.office.com/article/9338b2d2-67ac-4b81-8e67-97da27e5e9ab) voir Créer un PowerApp pour une liste dans SharePoint Online et la page [PowerApps.](https://powerapps.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="4b36b-134">See [Create a PowerApp for a list in SharePoint Online](https://support.office.com/article/9338b2d2-67ac-4b81-8e67-97da27e5e9ab) and the [PowerApps page](https://powerapps.microsoft.com/) for details.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4b36b-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b36b-135">See also</span></span>

[<span data-ttu-id="4b36b-136">Vue d’ensemble de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="4b36b-136">Microsoft 365 Enterprise overview</span></span>](microsoft-365-overview.md)