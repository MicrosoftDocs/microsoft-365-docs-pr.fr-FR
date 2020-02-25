---
title: Effectuer un rachat administratif interne dans Office 365
f1.keywords:
- CSH
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
- Adm_NonTOC
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: b9707ec8-2247-4e25-9bad-f11ddbc686e4
description: Découvrez comment vérifier la propriété de votre messagerie et de votre domaine pour prendre le relais d’un locataire non géré dans Office 365
ms.openlocfilehash: e3c89e122264808e2a8631c07269ea263c87fdaa
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42244117"
---
# <a name="perform-an-internal-admin-takeover-in-office-365"></a><span data-ttu-id="aec16-103">Effectuer un rachat administratif interne dans Office 365</span><span class="sxs-lookup"><span data-stu-id="aec16-103">Perform an internal admin takeover in Office 365</span></span>

 <span data-ttu-id="aec16-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="aec16-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 

<span data-ttu-id="aec16-105">Si vous êtes un administrateur et que vous souhaitez prendre le relais d’un client non géré créé par un abonnement d’utilisateur libre-service, vous pouvez effectuer cette opération avec un test administratif interne.</span><span class="sxs-lookup"><span data-stu-id="aec16-105">If you are an admin and want to take over an unmanaged tenant created by a self-service user signup, you can do this with an internal admin takeover.</span></span>

> [!NOTE]
> <span data-ttu-id="aec16-106">Un self-service s’abonner à un service Cloud qui utilise Azure AD ajoute l’utilisateur à un annuaire Azure AD non géré ou « Ombré » et crée un locataire non géré.</span><span class="sxs-lookup"><span data-stu-id="aec16-106">A self-service sign up for any cloud service that uses Azure AD will add the user to an unmanaged or "shadow" Azure AD directory and create an unmanaged tenant.</span></span> <span data-ttu-id="aec16-107">Un locataire non géré est un répertoire sans administrateur global.</span><span class="sxs-lookup"><span data-stu-id="aec16-107">An unmanaged tenant is a directory without a global administrator.</span></span> <span data-ttu-id="aec16-108">Pour déterminer si un client est géré ou non géré, consultez la rubrique [Determining client type](https://docs.microsoft.com/power-platform/admin/powerapps-gdpr-dsr-guide-systemlogs#determining-tenant-type).</span><span class="sxs-lookup"><span data-stu-id="aec16-108">To determine whether a tenant is managed or unmanaged, please see [Determining Tenant Type](https://docs.microsoft.com/power-platform/admin/powerapps-gdpr-dsr-guide-systemlogs#determining-tenant-type).</span></span> 
  
## <a name="step-1-verify-your-email-address"></a><span data-ttu-id="aec16-109">Étape 1 : vérifier votre adresse de messagerie</span><span class="sxs-lookup"><span data-stu-id="aec16-109">Step 1: Verify your email address</span></span>

> [!NOTE]
> <span data-ttu-id="aec16-110">Si le self-service est activé dans votre client, les utilisateurs peuvent s’abonner à des services gratuits, comme Power BI, de leur côté.</span><span class="sxs-lookup"><span data-stu-id="aec16-110">If self-service is enabled in your tenant, users can subscribe to free services, such as Power BI, on their own.</span></span> <span data-ttu-id="aec16-111">Ces étapes supposent qu’un abonnement d’utilisateur libre-service a créé le locataire non géré que vous souhaitez prendre en compte en tant qu’administrateur. La première étape consiste à créer un contexte utilisateur dans le locataire non géré à l’aide de Power BI pour illustrer le chemin de la prise en compte de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="aec16-111">These steps assume that a self-service user subscription has created the unmanaged tenant you want to take over as admin. In the first step you create a user context in the unmanaged tenant, using Power BI to illustrate the admin takeover path.</span></span>

1. <span data-ttu-id="aec16-112">Pour vous inscrire à Power bi, accédez au [site Power bi](https://powerbi.com) et sélectionnez **Démarrer** > la**version d’évaluation** gratuite de démarrage gratuit (dans la zone partager avec Power bi Pro).</span><span class="sxs-lookup"><span data-stu-id="aec16-112">To sign up for Power BI, go to the [Power BI site](https://powerbi.com) and select **Start Free** > **Start free trial** (in Share with Power BI Pro box).</span></span> 

2. <span data-ttu-id="aec16-113">Inscrivez-vous à l’aide d’un compte d’utilisateur qui utilise le nom de `powerbiadmin@contoso.com`domaine de votre organisation (par exemple).</span><span class="sxs-lookup"><span data-stu-id="aec16-113">Sign up with a user account that uses the domain name of your organization (like `powerbiadmin@contoso.com`).</span></span> <span data-ttu-id="aec16-114">Si votre compte est déjà utilisé, connectez-vous à l’aide de votre mot de passe actuel.</span><span class="sxs-lookup"><span data-stu-id="aec16-114">If your account is already in use, sign in using your current password.</span></span>

3. <span data-ttu-id="aec16-115">Consultez votre courrier électronique pour obtenir le **Code de vérification** et entrez le code permettant de valider votre adresse e-mail.</span><span class="sxs-lookup"><span data-stu-id="aec16-115">Check your email for the **verification code** and enter the code to validate your email address.</span></span>
    
## <a name="step-2-create-a-new-account"></a><span data-ttu-id="aec16-116">Étape 2 : créer un compte</span><span class="sxs-lookup"><span data-stu-id="aec16-116">Step 2: Create a new account</span></span>

1. <span data-ttu-id="aec16-117">Lorsque vous entrez le code de vérification, vous accédez à une page où vous pouvez créer un compte.</span><span class="sxs-lookup"><span data-stu-id="aec16-117">When you enter the verification code, you'll be brought to a page where you can create a new account.</span></span> 
    
2. <span data-ttu-id="aec16-118">Renseignez les champs nom d’utilisateur et mot de passe avec le compte que vous souhaitez utiliser, puis sélectionnez **Démarrer**.</span><span class="sxs-lookup"><span data-stu-id="aec16-118">Fill in the user name and password fields with the account that you want to use, then select **Start**.</span></span> 
    
## <a name="step-3-verify-domain-ownership-and-become-the-admin"></a><span data-ttu-id="aec16-119">Étape 3 : vérifier la propriété du domaine et devenir administrateur</span><span class="sxs-lookup"><span data-stu-id="aec16-119">Step 3: Verify domain ownership and become the admin</span></span>

1. <span data-ttu-id="aec16-120">L’Assistant d' **administration** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="aec16-120">The **Become the admin** wizard will open.</span></span> <span data-ttu-id="aec16-121">Si l’Assistant ne démarre pas, recherchez la vignette **administrateur** et sélectionnez-la.</span><span class="sxs-lookup"><span data-stu-id="aec16-121">If the wizard doesn't start, look for the **Admin** tile and select it.</span></span> 

2. <span data-ttu-id="aec16-122">Sélectionnez **Oui, je veux être l’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="aec16-122">Select **Yes, I want to be the admin**.</span></span>

3. <span data-ttu-id="aec16-123">Vérifiez que vous êtes propriétaire du domaine que vous souhaitez prendre en charge en ajoutant un enregistrement TXT à votre bureau d’enregistrement de domaines.</span><span class="sxs-lookup"><span data-stu-id="aec16-123">Verify that you own the domain you want to take over by adding a TXT record to your domain registrar.</span></span> <span data-ttu-id="aec16-124">L’Assistant vous donnera l’enregistrement TXT à ajouter, ainsi qu’un lien vers le site Web de votre registraire, ainsi qu’un lien vers des instructions pas à pas.</span><span class="sxs-lookup"><span data-stu-id="aec16-124">The wizard will give you the TXT record to add, as well as provide a link to your registrar's website, and a link to step-by-step instructions.</span></span>
    
4. <span data-ttu-id="aec16-125">Une fois que vous avez ajouté l’enregistrement TXT à votre site de serveur d’inscriptions, revenez à l’Assistant et sélectionnez **OK, j’ai ajouté l’enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="aec16-125">Once you've added the TXT record to your registrar site, return to the wizard and select **Okay, I've added the record**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="aec16-126">La prise en charge du client de cliché instantané n’a aucun impact sur les informations ou services existants.</span><span class="sxs-lookup"><span data-stu-id="aec16-126">Taking over the shadow tenant will not impact any existing information or services.</span></span> <span data-ttu-id="aec16-127">Toutefois, si un utilisateur du domaine s’est inscrit à des services nécessitant une licence, vous serez invité à acheter des licences pour ceux-ci dans le cadre de la prise en charge du rôle d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="aec16-127">However, if any users in the domain have signed up for services that require a license, you'll be asked to buy licenses for them as part of taking over the admin role.</span></span> <span data-ttu-id="aec16-128">Vous pouvez ajouter ou supprimer des licences une fois que le processus d’installation de l’administrateur est terminé.</span><span class="sxs-lookup"><span data-stu-id="aec16-128">You can add or remove licenses once the admin setup process is finished.</span></span> 
  
## <a name="related-articles"></a><span data-ttu-id="aec16-129">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="aec16-129">Related articles</span></span>

<span data-ttu-id="aec16-130">YouTube : [3 steps to do an IT Admin Takeover for Power BI and Office 365 (Prise de contrôle administratif pour Power BI et Office 365 en 3 étapes)](https://www.youtube.com/watch?v=xt5EsrQBZZk)</span><span class="sxs-lookup"><span data-stu-id="aec16-130">YouTube: [3 steps to do an IT Admin Takeover for Power BI and Office 365](https://www.youtube.com/watch?v=xt5EsrQBZZk)</span></span>

[<span data-ttu-id="aec16-131">Prise en compte de l’administrateur dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="aec16-131">Admin takeover in Azure AD</span></span>](https://docs.microsoft.com/azure/active-directory/users-groups-roles/domains-admin-takeover)

[<span data-ttu-id="aec16-132">Obtenir de l’aide sur les domaines Office 365</span><span class="sxs-lookup"><span data-stu-id="aec16-132">Get help with Office 365 domains</span></span>](../get-help-with-domains/get-help-with-domains.md)

[<span data-ttu-id="aec16-133">Utilisation de l’authentification en libre-service dans votre organisation</span><span class="sxs-lookup"><span data-stu-id="aec16-133">Using self-service sign up in your organization</span></span>](self-service-sign-up.md)
  
[<span data-ttu-id="aec16-134">Présentation du rôle d’administrateur de service Power BI</span><span class="sxs-lookup"><span data-stu-id="aec16-134">Understanding the Power BI service administrator role</span></span>](https://docs.microsoft.com/power-bi/service-admin-role)

