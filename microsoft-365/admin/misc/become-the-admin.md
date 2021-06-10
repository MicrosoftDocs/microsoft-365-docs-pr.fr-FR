---
title: Effectuer une prise de contrôle d’administrateur interne
f1.keywords:
- CSH
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
- Adm_NonTOC
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: b9707ec8-2247-4e25-9bad-f11ddbc686e4
description: Découvrez comment vérifier la propriété de votre courrier électronique et de votre domaine pour prendre le contrôle d’un client non pris en charge créé par une inscription utilisateur en libre-service dans Microsoft 365.
ms.openlocfilehash: aa44023ffdc2b59e4db024706323c5b872566260
ms.sourcegitcommit: 17f0aada83627d9defa0acf4db03a2d58e46842f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52635985"
---
# <a name="perform-an-internal-admin-takeover"></a><span data-ttu-id="99b47-103">Effectuer une prise de contrôle d’administrateur interne</span><span class="sxs-lookup"><span data-stu-id="99b47-103">Perform an internal admin takeover</span></span>

 <span data-ttu-id="99b47-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="99b47-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span> 

<span data-ttu-id="99b47-105">Si vous êtes un administrateur et que vous souhaitez prendre le contrôle d’un client non pris en charge créé par une inscription d’utilisateur libre-service, vous pouvez le faire avec une prise de contrôle d’administrateur interne.</span><span class="sxs-lookup"><span data-stu-id="99b47-105">If you are an admin and want to take over an unmanaged tenant created by a self-service user signup, you can do this with an internal admin takeover.</span></span>

> [!NOTE]
> <span data-ttu-id="99b47-106">Une inscription en libre-service pour tout service cloud qui utilise Azure AD ajoute l’utilisateur à un répertoire Azure AD non pris en compte ou « shadow » et crée un client non pris en compte.</span><span class="sxs-lookup"><span data-stu-id="99b47-106">A self-service sign up for any cloud service that uses Azure AD will add the user to an unmanaged or "shadow" Azure AD directory and create an unmanaged tenant.</span></span> <span data-ttu-id="99b47-107">Un client non gérant est un répertoire sans administrateur général.</span><span class="sxs-lookup"><span data-stu-id="99b47-107">An unmanaged tenant is a directory without a global administrator.</span></span> <span data-ttu-id="99b47-108">Pour déterminer si un client est géré ou non, voir [Déterminer le type de client.](/power-platform/admin/powerapps-gdpr-dsr-guide-systemlogs#determining-tenant-type)</span><span class="sxs-lookup"><span data-stu-id="99b47-108">To determine whether a tenant is managed or unmanaged, please see [Determining Tenant Type](/power-platform/admin/powerapps-gdpr-dsr-guide-systemlogs#determining-tenant-type).</span></span> 
  
## <a name="step-1-verify-your-email-address"></a><span data-ttu-id="99b47-109">Étape 1 : Vérifier votre adresse de messagerie</span><span class="sxs-lookup"><span data-stu-id="99b47-109">Step 1: Verify your email address</span></span>

> [!NOTE]
> <span data-ttu-id="99b47-110">Si le libre-service est activé dans votre client, les utilisateurs peuvent s’abonner à des services gratuits, tels que Power BI, eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="99b47-110">If self-service is enabled in your tenant, users can subscribe to free services, such as Power BI, on their own.</span></span> <span data-ttu-id="99b47-111">Ces étapes supposent qu’un abonnement utilisateur libre-service a créé le client non pris en compte que vous souhaitez prendre en tant qu’administrateur. Dans la première étape, vous créez un contexte utilisateur dans le client non Power BI pour illustrer le chemin d’accès de prise de contrôle de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="99b47-111">These steps assume that a self-service user subscription has created the unmanaged tenant you want to take over as admin. In the first step you create a user context in the unmanaged tenant, using Power BI to illustrate the admin takeover path.</span></span>

1. <span data-ttu-id="99b47-112">Pour vous inscrire à Power BI, allez sur le site  [Power BI et](https://powerbi.com) sélectionnez Démarrer l’essai gratuit gratuit (dans la zone Partager  >   avec Power BI Pro).</span><span class="sxs-lookup"><span data-stu-id="99b47-112">To sign up for Power BI, go to the [Power BI site](https://powerbi.com) and select **Start Free** > **Start free trial** (in Share with Power BI Pro box).</span></span> 

2. <span data-ttu-id="99b47-113">Inscrivez-vous avec un compte d’utilisateur qui utilise le nom de domaine de votre organisation (comme `powerbiadmin@contoso.com` ).</span><span class="sxs-lookup"><span data-stu-id="99b47-113">Sign up with a user account that uses the domain name of your organization (like `powerbiadmin@contoso.com`).</span></span> <span data-ttu-id="99b47-114">Si votre compte est déjà utilisé, connectez-vous à l’aide de votre mot de passe actuel.</span><span class="sxs-lookup"><span data-stu-id="99b47-114">If your account is already in use, sign in using your current password.</span></span>

3. <span data-ttu-id="99b47-115">Recherchez le **code de vérification dans votre** courrier électronique et entrez-le pour valider votre adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="99b47-115">Check your email for the **verification code** and enter the code to validate your email address.</span></span>
    
## <a name="step-2-create-a-new-account"></a><span data-ttu-id="99b47-116">Étape 2 : Créer un compte</span><span class="sxs-lookup"><span data-stu-id="99b47-116">Step 2: Create a new account</span></span>

1. <span data-ttu-id="99b47-117">Lorsque vous entrez le code de vérification, vous êtes conduit à une page dans laquelle vous pouvez créer un compte.</span><span class="sxs-lookup"><span data-stu-id="99b47-117">When you enter the verification code, you'll be brought to a page where you can create a new account.</span></span> 
    
2. <span data-ttu-id="99b47-118">Remplissez les champs nom d’utilisateur et mot de passe avec le compte que vous souhaitez utiliser, puis sélectionnez **Démarrer.**</span><span class="sxs-lookup"><span data-stu-id="99b47-118">Fill in the user name and password fields with the account that you want to use, then select **Start**.</span></span> 
    
## <a name="step-3-verify-domain-ownership-and-become-the-admin"></a><span data-ttu-id="99b47-119">Étape 3 : Vérifier la propriété du domaine et devenir l’administrateur</span><span class="sxs-lookup"><span data-stu-id="99b47-119">Step 3: Verify domain ownership and become the admin</span></span>

1. <span data-ttu-id="99b47-120">**L’Assistant Devenir administrateur** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="99b47-120">The **Become the admin** wizard will open.</span></span> <span data-ttu-id="99b47-121">Si l’Assistant ne démarre pas, recherchez la vignette **Administrateur** et sélectionnez-la.</span><span class="sxs-lookup"><span data-stu-id="99b47-121">If the wizard doesn't start, look for the **Admin** tile and select it.</span></span> 

2. <span data-ttu-id="99b47-122">Sélectionnez **Oui, je veux être l’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="99b47-122">Select **Yes, I want to be the admin**.</span></span>

3. <span data-ttu-id="99b47-123">Vérifiez que vous êtes propriétaire du domaine à prendre en compte en ajoutant un enregistrement TXT à votre bureau d’enregistrement de domaines.</span><span class="sxs-lookup"><span data-stu-id="99b47-123">Verify that you own the domain you want to take over by adding a TXT record to your domain registrar.</span></span> <span data-ttu-id="99b47-124">L’Assistant vous fournira l’enregistrement TXT à ajouter, ainsi qu’un lien vers le site web de votre bureau d’enregistrement et un lien vers des instructions pas à pas.</span><span class="sxs-lookup"><span data-stu-id="99b47-124">The wizard will give you the TXT record to add, as well as provide a link to your registrar's website, and a link to step-by-step instructions.</span></span>
    
4. <span data-ttu-id="99b47-125">Une fois que vous avez ajouté l’enregistrement TXT à votre site de bureau d’enregistrement, revenir à l’Assistant et sélectionnez **Ok, j’ai ajouté l’enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="99b47-125">Once you've added the TXT record to your registrar site, return to the wizard and select **Okay, I've added the record**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="99b47-126">Le fait de prendre le contrôle du client de secours n’aura aucun impact sur les informations ou les services existants.</span><span class="sxs-lookup"><span data-stu-id="99b47-126">Taking over the shadow tenant will not impact any existing information or services.</span></span> <span data-ttu-id="99b47-127">Toutefois, si des utilisateurs du domaine se sont inscrits aux services qui nécessitent une licence, vous serez invité à acheter des licences pour eux dans le cadre de la prise de contrôle du rôle d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="99b47-127">However, if any users in the domain have signed up for services that require a license, you'll be asked to buy licenses for them as part of taking over the admin role.</span></span> <span data-ttu-id="99b47-128">Vous pouvez acheter ou supprimer des licences une fois le processus de configuration de l’administrateur terminé.</span><span class="sxs-lookup"><span data-stu-id="99b47-128">You can buy or remove licenses once the admin setup process is finished.</span></span>
  
## <a name="related-content"></a><span data-ttu-id="99b47-129">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="99b47-129">Related content</span></span>

<span data-ttu-id="99b47-130">YouTube : [3 étapes pour une](https://www.youtube.com/watch?v=xt5EsrQBZZk) prise de contrôle d’administrateur informatique pour Power BI et Microsoft 365 (vidéo)</span><span class="sxs-lookup"><span data-stu-id="99b47-130">YouTube: [3 steps to do an IT Admin Takeover for Power BI and Microsoft 365](https://www.youtube.com/watch?v=xt5EsrQBZZk) (video)</span></span>\
<span data-ttu-id="99b47-131">[Prise de contrôle par l’administrateur dans Azure AD](/azure/active-directory/users-groups-roles/domains-admin-takeover) (article)</span><span class="sxs-lookup"><span data-stu-id="99b47-131">[Admin takeover in Azure AD](/azure/active-directory/users-groups-roles/domains-admin-takeover) (article)</span></span>\
<span data-ttu-id="99b47-132">[Utilisation de l’inscription en libre-service dans votre organisation](self-service-sign-up.md) (article)</span><span class="sxs-lookup"><span data-stu-id="99b47-132">[Using self-service sign up in your organization](self-service-sign-up.md) (article)</span></span>\
<span data-ttu-id="99b47-133">[Understanding the Power BI service administrator role](/power-bi/service-admin-role) (article)</span><span class="sxs-lookup"><span data-stu-id="99b47-133">[Understanding the Power BI service administrator role](/power-bi/service-admin-role) (article)</span></span>