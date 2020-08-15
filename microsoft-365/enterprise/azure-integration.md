---
title: Intégration Azure avec Microsoft 365
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 10/09/2019
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
ms.openlocfilehash: 045760f000abdbf053e09d89b296fbafa4c24786
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46690168"
---
# <a name="azure-integration-with-microsoft-365"></a><span data-ttu-id="491c9-103">Intégration Azure avec Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="491c9-103">Azure integration with Microsoft 365</span></span>

<span data-ttu-id="491c9-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="491c9-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="491c9-105">Microsoft 365 utilise Azure Active Directory (Azure AD) pour gérer les identités des utilisateurs en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="491c9-105">Microsoft 365 uses Azure Active Directory (Azure AD) to manage user identities behind the scenes.</span></span> <span data-ttu-id="491c9-106">Votre abonnement Microsoft 365 inclut un abonnement gratuit à Azure AD afin que vous puissiez intégrer Microsoft 365 à Azure AD si vous souhaitez synchroniser les mots de passe ou configurer l’authentification unique avec votre environnement local.</span><span class="sxs-lookup"><span data-stu-id="491c9-106">Your Microsoft 365 subscription includes a free subscription to Azure AD so that you can integrate Microsoft 365 with Azure AD if you want to sync passwords or set up single sign-on with your on-premises environment.</span></span> <span data-ttu-id="491c9-107">Vous pouvez également acheter des fonctionnalités avancées pour mieux gérer vos comptes.</span><span class="sxs-lookup"><span data-stu-id="491c9-107">You can also buy advanced features to better manage your accounts.</span></span>
  
<span data-ttu-id="491c9-108">Azure offre également d’autres fonctionnalités, telles que la gestion des applications intégrées, que vous pouvez utiliser pour étendre et personnaliser vos abonnements Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="491c9-108">Azure also offers other functionality, like managing integrated apps, that you can use to extend and customize your Microsoft 365 subscriptions.</span></span>
  
<span data-ttu-id="491c9-109">Vous pouvez utiliser les conseillers de déploiement Azure AD pour une expérience de configuration et d’installation guidée (vous devez être connecté à Microsoft 365) :</span><span class="sxs-lookup"><span data-stu-id="491c9-109">You can use the Azure AD deployment advisors for a guided setup and configuration experience (you must be signed in to Microsoft 365):</span></span>

 - [<span data-ttu-id="491c9-110">Conseiller Azure AD Connect</span><span class="sxs-lookup"><span data-stu-id="491c9-110">Azure AD Connect advisor</span></span>](https://aka.ms/aadconnectpwsync)
 - [<span data-ttu-id="491c9-111">Conseiller de déploiement AD FS</span><span class="sxs-lookup"><span data-stu-id="491c9-111">AD FS deployment advisor</span></span>](https://aka.ms/adfsguidance)
 - [<span data-ttu-id="491c9-112">Guide de configuration d’Azure AD</span><span class="sxs-lookup"><span data-stu-id="491c9-112">Azure AD setup guide</span></span>](https://aka.ms/aadpguidance)
  
## <a name="azure-ad-editions-and-microsoft-365-identity-management"></a><span data-ttu-id="491c9-113">La gestion des identités Azure AD Edition et Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="491c9-113">Azure AD editions and Microsoft 365 identity management</span></span>

<span data-ttu-id="491c9-114">Si vous disposez d’un abonnement payant à Microsoft 365, vous disposez également d’un abonnement gratuit à Azure AD.</span><span class="sxs-lookup"><span data-stu-id="491c9-114">If you have a paid subscription to Microsoft 365, you also have a free subscription to Azure AD.</span></span> <span data-ttu-id="491c9-115">Vous pouvez utiliser Azure AD pour créer et gérer des comptes d’utilisateurs et de groupes.</span><span class="sxs-lookup"><span data-stu-id="491c9-115">You can use Azure AD to create and manage user and group accounts.</span></span> <span data-ttu-id="491c9-116">Pour activer cet abonnement, vous devez effectuer une inscription unique.</span><span class="sxs-lookup"><span data-stu-id="491c9-116">To activate this subscription you have to complete a one-time registration.</span></span> <span data-ttu-id="491c9-117">Par la suite, vous pouvez accéder à Azure AD à partir de votre centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="491c9-117">Afterward, you can access Azure AD from your Microsoft 365 admin center.</span></span> 

<span data-ttu-id="491c9-118">Pour obtenir des instructions, consultez [la rubrique utiliser votre abonnement Azure ad gratuit](https://go.microsoft.com/fwlink/p/?LinkId=617127).</span><span class="sxs-lookup"><span data-stu-id="491c9-118">For instructions, see [use your free Azure AD subscription](https://go.microsoft.com/fwlink/p/?LinkId=617127).</span></span> <span data-ttu-id="491c9-119">Suivez les instructions pour enregistrer l’abonnement Azure AD gratuit fourni avec votre abonnement à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="491c9-119">Follow the instructions to register the free Azure AD subscription that comes with your subscription to Microsoft 365.</span></span> <span data-ttu-id="491c9-120">N’accédez pas directement à azure.microsoft.com pour vous inscrire ou vous obtiendrez une version d’évaluation ou un abonnement payant à Microsoft Azure qui est distinct de votre version gratuite pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="491c9-120">Don't go directly to azure.microsoft.com to sign up or you'll end up with a trial or paid subscription to Microsoft Azure that is separate from your free one for Microsoft 365.</span></span> 
  
<span data-ttu-id="491c9-121">Avec l’abonnement gratuit, vous pouvez synchroniser avec des annuaires locaux, configurer l’authentification unique et effectuer une synchronisation avec de nombreux logiciels en tant qu’applications de service, telles que Salesforce, DropBox et bien d’autres encore.</span><span class="sxs-lookup"><span data-stu-id="491c9-121">With the free subscription you can synchronize with on-premises directories, set up single sign-on, and synchronize with many software as service applications, such as Salesforce, DropBox and many more.</span></span>
  
<span data-ttu-id="491c9-122">Si vous souhaitez améliorer la fonctionnalité des services de domaine Active Directory (AD DS), la synchronisation bidirectionnelle et d’autres fonctionnalités de gestion, vous pouvez mettre à niveau votre abonnement gratuit vers un abonnement Premium payant.</span><span class="sxs-lookup"><span data-stu-id="491c9-122">If you want enhanced Active Directory Domain Services (AD DS) functionality, bi-directional synchronization, and other management capabilities, you can upgrade your free subscription to a paid premium subscription.</span></span> <span data-ttu-id="491c9-123">Pour plus d’informations, reportez-vous à [Azure Active Directory Editions](https://azure.microsoft.com/pricing/details/active-directory/).</span><span class="sxs-lookup"><span data-stu-id="491c9-123">For details see [Azure Active Directory editions](https://azure.microsoft.com/pricing/details/active-directory/).</span></span>
  
<span data-ttu-id="491c9-124">Pour plus d’informations sur Microsoft 365 et Azure AD, consultez la rubrique [Understanding microsoft 365 Identity and Azure Active Directory](about-microsoft-365-identity.md).</span><span class="sxs-lookup"><span data-stu-id="491c9-124">For more information about Microsoft 365 and Azure AD, see [Understanding Microsoft 365 Identity and Azure Active Directory](about-microsoft-365-identity.md).</span></span>
  
## <a name="extend-the-capabilities-of-your-microsoft-365-tenant"></a><span data-ttu-id="491c9-125">Étendez les capacités de votre client Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="491c9-125">Extend the capabilities of your Microsoft 365 tenant</span></span>

|<span data-ttu-id="491c9-126">**Fonctionnalité**</span><span class="sxs-lookup"><span data-stu-id="491c9-126">**Feature**</span></span>|<span data-ttu-id="491c9-127">**Description**</span><span class="sxs-lookup"><span data-stu-id="491c9-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="491c9-128">Applications intégrées</span><span class="sxs-lookup"><span data-stu-id="491c9-128">Integrated apps</span></span>  <br/> |<span data-ttu-id="491c9-129">Vous pouvez accorder à des applications individuelles l’accès à vos données Microsoft 365, tels que le courrier, les calendriers, les contacts, les utilisateurs, les groupes, les fichiers et les dossiers.</span><span class="sxs-lookup"><span data-stu-id="491c9-129">You can grant individual apps access to your Microsoft 365 data, like mail, calendars, contacts, users, groups, files, and folders.</span></span> <span data-ttu-id="491c9-130">Vous pouvez également autoriser ces applications au niveau de l’administrateur général et les rendre accessibles à votre entreprise entière en enregistrant les applications dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="491c9-130">You can also authorize these apps at global admin level and make them available to your entire company by registering the apps in Azure AD.</span></span> <span data-ttu-id="491c9-131">Pour plus d’informations, consultez la rubrique [applications intégrées et Azure AD pour les administrateurs Microsoft 365](https://support.office.com/article/cb2250e3-451e-416f-bf4e-363549652c2a).</span><span class="sxs-lookup"><span data-stu-id="491c9-131">For details see [Integrated Apps and Azure AD for Microsoft 365 administrators](https://support.office.com/article/cb2250e3-451e-416f-bf4e-363549652c2a).</span></span>  <br/> <span data-ttu-id="491c9-132">Voir aussi l' [authentification unique pour les applications](https://go.microsoft.com/fwlink/p/?LinkId=698604).</span><span class="sxs-lookup"><span data-stu-id="491c9-132">Also see [single sign-on to applications](https://go.microsoft.com/fwlink/p/?LinkId=698604).</span></span>  <br/> |
|<span data-ttu-id="491c9-133">PowerApps</span><span class="sxs-lookup"><span data-stu-id="491c9-133">PowerApps</span></span>  <br/> | <span data-ttu-id="491c9-134">Les applications Power sont des applications ciblées pour les appareils mobiles qui peuvent se connecter à vos sources de données existantes, telles que les listes SharePoint et les autres applications de données.</span><span class="sxs-lookup"><span data-stu-id="491c9-134">Power apps are focused apps for mobile devices that can connect to your existing data sources like SharePoint lists, and other data apps.</span></span> <span data-ttu-id="491c9-135">Pour plus d’informations, reportez-vous à [la page créer un PowerApp pour une liste dans SharePoint Online](https://support.office.com/article/9338b2d2-67ac-4b81-8e67-97da27e5e9ab) et les [PowerApp](https://powerapps.microsoft.com/) .</span><span class="sxs-lookup"><span data-stu-id="491c9-135">See [Create a PowerApp for a list in SharePoint Online](https://support.office.com/article/9338b2d2-67ac-4b81-8e67-97da27e5e9ab) and [PowerApps page](https://powerapps.microsoft.com/) for details.</span></span>  <br/> |
   
<span data-ttu-id="491c9-136">Pour plus d’informations, consultez la rubrique [applications intégrées et Azure AD pour les administrateurs de Microsoft 365](integrated-apps-and-azure-ads.md) et la [Galerie d’applications Azure ad et l’authentification unique](https://docs.microsoft.com/azure/active-directory/manage-apps/what-is-single-sign-on).</span><span class="sxs-lookup"><span data-stu-id="491c9-136">Learn more at [Integrated Apps and Azure AD for Microsoft 365 administrators](integrated-apps-and-azure-ads.md) and [Azure AD application gallery and single-sign-on](https://docs.microsoft.com/azure/active-directory/manage-apps/what-is-single-sign-on).</span></span>

## <a name="see-also"></a><span data-ttu-id="491c9-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="491c9-137">See also</span></span>

[<span data-ttu-id="491c9-138">Vue d’ensemble de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="491c9-138">Microsoft 365 Enterprise overview</span></span>](microsoft-365-overview.md)
