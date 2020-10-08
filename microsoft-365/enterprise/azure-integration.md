---
title: Intégration Azure avec Microsoft 365
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
description: Intégrez Microsoft 365 à Azure AD si vous voulez une synchronisation de mot de passe ou une authentification unique avec votre environnement local.
ms.openlocfilehash: b1f20ebc692421ed6df0d6f7c31a4d80347133e3
ms.sourcegitcommit: 11d1044c6600b1f568b6dc8a53db9b07f2f0ad1c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/08/2020
ms.locfileid: "48384739"
---
# <a name="azure-integration-with-microsoft-365"></a><span data-ttu-id="28ce5-103">Intégration Azure avec Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="28ce5-103">Azure integration with Microsoft 365</span></span>

<span data-ttu-id="28ce5-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="28ce5-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="28ce5-105">Microsoft 365 utilise Azure Active Directory (Azure AD) pour gérer les identités des utilisateurs en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="28ce5-105">Microsoft 365 uses Azure Active Directory (Azure AD) to manage user identities behind the scenes.</span></span> <span data-ttu-id="28ce5-106">Votre abonnement Microsoft 365 inclut un abonnement Azure AD gratuit afin que vous puissiez intégrer vos services de domaine Active Directory (AD DS) locaux pour synchroniser les comptes d’utilisateurs et les mots de passe ou configurer l’authentification unique.</span><span class="sxs-lookup"><span data-stu-id="28ce5-106">Your Microsoft 365 subscription includes a free Azure AD subscription so that you can integrate your on-premises Active Directory Domain Services (AD DS) to synchronize user accounts and passwords or set up single sign-on.</span></span> <span data-ttu-id="28ce5-107">Vous pouvez également acheter des fonctionnalités avancées pour mieux gérer vos comptes.</span><span class="sxs-lookup"><span data-stu-id="28ce5-107">You can also purchase advanced features to better manage your accounts.</span></span>
  
<span data-ttu-id="28ce5-108">Azure AD offre également d’autres fonctionnalités, telles que la gestion des applications intégrées, que vous pouvez utiliser pour étendre et personnaliser vos abonnements Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="28ce5-108">Azure AD also offers other functionality, like managing integrated apps, that you can use to extend and customize your Microsoft 365 subscriptions.</span></span>
  
<span data-ttu-id="28ce5-109">Vous pouvez utiliser les conseillers au déploiement Azure AD pour une expérience de configuration et d’installation guidée dans le centre d’administration 365 de Microsoft (vous devez être connecté à Microsoft 365) :</span><span class="sxs-lookup"><span data-stu-id="28ce5-109">You can use the Azure AD deployment advisors for a guided setup and configuration experience in the Microsoft 365 admin center (you must be signed in to Microsoft 365):</span></span>

 - [<span data-ttu-id="28ce5-110">Conseiller Azure AD Connect</span><span class="sxs-lookup"><span data-stu-id="28ce5-110">Azure AD Connect advisor</span></span>](https://aka.ms/aadconnectpwsync)
 - [<span data-ttu-id="28ce5-111">Conseiller de déploiement AD FS</span><span class="sxs-lookup"><span data-stu-id="28ce5-111">AD FS deployment advisor</span></span>](https://aka.ms/adfsguidance)
 - [<span data-ttu-id="28ce5-112">Guide de configuration d’Azure AD</span><span class="sxs-lookup"><span data-stu-id="28ce5-112">Azure AD setup guide</span></span>](https://aka.ms/aadpguidance)
  
## <a name="azure-ad-editions-and-microsoft-365-identity-management"></a><span data-ttu-id="28ce5-113">La gestion des identités Azure AD Edition et Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="28ce5-113">Azure AD editions and Microsoft 365 identity management</span></span>

<span data-ttu-id="28ce5-114">Si vous disposez d’un abonnement payant à Microsoft 365, vous disposez également d’un abonnement Azure AD gratuit.</span><span class="sxs-lookup"><span data-stu-id="28ce5-114">If you have a paid subscription to Microsoft 365, you also have a free Azure AD subscription.</span></span> <span data-ttu-id="28ce5-115">Vous pouvez utiliser Azure AD pour créer et gérer des comptes d’utilisateurs et de groupes.</span><span class="sxs-lookup"><span data-stu-id="28ce5-115">You can use Azure AD to create and manage user and group accounts.</span></span> <span data-ttu-id="28ce5-116">Pour activer cet abonnement, vous devez effectuer une inscription unique.</span><span class="sxs-lookup"><span data-stu-id="28ce5-116">To activate this subscription, you have to complete a one-time registration.</span></span> <span data-ttu-id="28ce5-117">Par la suite, vous pouvez accéder à Azure AD à partir de votre centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="28ce5-117">Afterward, you can access Azure AD from your Microsoft 365 admin center.</span></span> 

<span data-ttu-id="28ce5-118">Pour obtenir des instructions sur l’enregistrement de votre abonnement Azure AD gratuit, consultez [la rubrique utiliser votre abonnement Azure ad gratuit](../compliance/use-your-free-azure-ad-subscription-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="28ce5-118">For instructions to register your free Azure AD subscription, see [use your free Azure AD subscription](../compliance/use-your-free-azure-ad-subscription-in-office-365.md).</span></span> <span data-ttu-id="28ce5-119">N’accédez pas directement à azure.microsoft.com pour vous inscrire ou vous obtiendrez une version d’évaluation ou un abonnement payant à Microsoft Azure qui est distinct de votre abonnement Azure AD gratuit avec Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="28ce5-119">Don't go directly to azure.microsoft.com to sign up or you'll end up with a trial or paid subscription to Microsoft Azure that is separate from your free Azure AD subscription with Microsoft 365.</span></span> 
  
<span data-ttu-id="28ce5-120">Avec l’abonnement gratuit, vous pouvez synchroniser avec des annuaires locaux, configurer l’authentification unique et effectuer une synchronisation avec de nombreux logiciels en tant qu’applications de service, telles que Salesforce, DropBox et bien d’autres encore.</span><span class="sxs-lookup"><span data-stu-id="28ce5-120">With the free subscription you can synchronize with on-premises directories, set up single sign-on, and synchronize with many software as service applications, such as Salesforce, DropBox, and many more.</span></span>
  
<span data-ttu-id="28ce5-121">Si vous souhaitez améliorer les fonctionnalités AD DS, la synchronisation bidirectionnelle et les autres fonctionnalités de gestion, vous pouvez mettre à niveau votre abonnement gratuit vers un abonnement payant payant.</span><span class="sxs-lookup"><span data-stu-id="28ce5-121">If you want enhanced AD DS functionality, bi-directional synchronization, and other management capabilities, you can upgrade your free subscription to a paid premium subscription.</span></span> <span data-ttu-id="28ce5-122">Pour plus d’informations, reportez-vous à la rubrique [Azure Active Directory Editions](https://azure.microsoft.com/pricing/details/active-directory/).</span><span class="sxs-lookup"><span data-stu-id="28ce5-122">For the details, see [Azure Active Directory editions](https://azure.microsoft.com/pricing/details/active-directory/).</span></span>
  
<span data-ttu-id="28ce5-123">Pour plus d’informations sur Microsoft 365 et Azure AD, voir [microsoft 365 Identity Models](about-microsoft-365-identity.md).</span><span class="sxs-lookup"><span data-stu-id="28ce5-123">For more information about Microsoft 365 and Azure AD, see [Microsoft 365 identity models](about-microsoft-365-identity.md).</span></span>
  
## <a name="extend-the-capabilities-of-your-microsoft-365-tenant"></a><span data-ttu-id="28ce5-124">Étendez les capacités de votre client Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="28ce5-124">Extend the capabilities of your Microsoft 365 tenant</span></span>

|<span data-ttu-id="28ce5-125">**Fonctionnalité**</span><span class="sxs-lookup"><span data-stu-id="28ce5-125">**Feature**</span></span>|<span data-ttu-id="28ce5-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="28ce5-126">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="28ce5-127">Applications intégrées</span><span class="sxs-lookup"><span data-stu-id="28ce5-127">Integrated apps</span></span>  <br/> |<span data-ttu-id="28ce5-128">Vous pouvez accorder à des applications individuelles l’accès à vos données Microsoft 365, telles que des courriers électroniques, des calendriers, des contacts, des utilisateurs, des groupes, des fichiers et des dossiers.</span><span class="sxs-lookup"><span data-stu-id="28ce5-128">You can grant individual apps access to your Microsoft 365 data, such as mail, calendars, contacts, users, groups, files, and folders.</span></span> <span data-ttu-id="28ce5-129">Vous pouvez également autoriser ces applications au niveau de l’administrateur général et les rendre accessibles à votre entreprise entière en enregistrant les applications dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="28ce5-129">You can also authorize these apps at global admin level and make them available to your entire company by registering the apps in Azure AD.</span></span> <span data-ttu-id="28ce5-130">Formore informations, consultez la rubrique [applications intégrées et Azure AD pour les administrateurs de Microsoft 365](integrated-apps-and-azure-ads.md).</span><span class="sxs-lookup"><span data-stu-id="28ce5-130">Formore information, see [Integrated Apps and Azure AD for Microsoft 365 administrators](integrated-apps-and-azure-ads.md).</span></span>  <br/> <span data-ttu-id="28ce5-131">Voir aussi [authentification unique](https://go.microsoft.com/fwlink/p/?LinkId=698604).</span><span class="sxs-lookup"><span data-stu-id="28ce5-131">Also see [Single sign-on](https://go.microsoft.com/fwlink/p/?LinkId=698604).</span></span>  <br/> |
|<span data-ttu-id="28ce5-132">PowerApps</span><span class="sxs-lookup"><span data-stu-id="28ce5-132">PowerApps</span></span>  <br/> | <span data-ttu-id="28ce5-133">Les applications Power sont des applications ciblées pour les appareils mobiles qui peuvent se connecter à vos sources de données existantes, telles que les listes SharePoint et les autres applications de données.</span><span class="sxs-lookup"><span data-stu-id="28ce5-133">Power apps are focused apps for mobile devices that can connect to your existing data sources like SharePoint lists and other data apps.</span></span> <span data-ttu-id="28ce5-134">Pour plus d’informations, reportez-vous à la rubrique [créer un PowerApp pour une liste dans SharePoint Online](https://support.office.com/article/9338b2d2-67ac-4b81-8e67-97da27e5e9ab) et la [page des PowerApp](https://powerapps.microsoft.com/) .</span><span class="sxs-lookup"><span data-stu-id="28ce5-134">See [Create a PowerApp for a list in SharePoint Online](https://support.office.com/article/9338b2d2-67ac-4b81-8e67-97da27e5e9ab) and the [PowerApps page](https://powerapps.microsoft.com/) for details.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="28ce5-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28ce5-135">See also</span></span>

[<span data-ttu-id="28ce5-136">Vue d’ensemble de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="28ce5-136">Microsoft 365 Enterprise overview</span></span>](microsoft-365-overview.md)
