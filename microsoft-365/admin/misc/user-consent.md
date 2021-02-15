---
title: Gestion du consentement des utilisateurs aux applications dans Microsoft 365
f1.keywords:
- CSH
ms.author: kwekua
author: kwekua
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
ms.assetid: 7e453a40-66df-44ab-92a1-96786cb7fb34
description: Découvrez le consentement des utilisateurs aux applications et comment les activer pour autoriser des applications tierces à accéder aux informations Microsoft 365 des utilisateurs.
ms.openlocfilehash: 955ae9e58c14dbb8012a440ef6c336f44b0760a4
ms.sourcegitcommit: da34ac08c7d029c2c42d4428d0bb03fd57c448be
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/12/2020
ms.locfileid: "48999570"
---
# <a name="managing-user-consent-to-apps-in-microsoft-365"></a><span data-ttu-id="e61bc-103">Gestion du consentement des utilisateurs aux applications dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="e61bc-103">Managing user consent to apps in Microsoft 365</span></span>

<span data-ttu-id="e61bc-104">Ce paramètre contrôle si les utilisateurs peuvent donner ce consentement aux applications qui utilisent OpenID Connect et OAuth 2.0 pour la connexion et les demandes d’accès aux données.</span><span class="sxs-lookup"><span data-stu-id="e61bc-104">This setting controls whether users can give that consent to apps that use OpenID Connect and OAuth 2.0 for sign-in and requests to access data.</span></span> <span data-ttu-id="e61bc-105">Une application peut être créée à partir de votre propre organisation, ou elle peut être créée à partir d’une autre organisation Office 365 ou d’un tiers.</span><span class="sxs-lookup"><span data-stu-id="e61bc-105">An app can be created from within your own organization, or it can come from another Office 365 organization or a third-party.</span></span>

<span data-ttu-id="e61bc-106">Si vous allumez ce paramètre, ces applications demandent aux utilisateurs l’autorisation d’accéder aux données de votre organisation, et les utilisateurs peuvent choisir s’ils le souhaitent.</span><span class="sxs-lookup"><span data-stu-id="e61bc-106">If you turn this setting on, those apps will ask users for permission to access your organization’s data, and users can choose whether to allow it.</span></span> <span data-ttu-id="e61bc-107">Si vous la désactiver, les administrateurs doivent consentir à ces applications avant que les utilisateurs ne les utilisent.</span><span class="sxs-lookup"><span data-stu-id="e61bc-107">If you turn this setting off, then admins must consent to those apps before users may use them.</span></span> <span data-ttu-id="e61bc-108">Dans ce cas, envisagez de définir un flux de travail de consentement d’administrateur dans le portail Azure afin que les utilisateurs peuvent envoyer une demande d’approbation d’administrateur pour utiliser n’importe quelle application bloquée.</span><span class="sxs-lookup"><span data-stu-id="e61bc-108">In this case, consider setting up an admin consent workflow in the Azure portal so users can send a request for admin approval to use any blocked app.</span></span>

<span data-ttu-id="e61bc-109">Un utilisateur peut autoriser uniquement les applications dont il est propriétaire à accéder à ses informations Office 365.</span><span class="sxs-lookup"><span data-stu-id="e61bc-109">A user can give access only to apps they own that access their Office 365 information.</span></span> <span data-ttu-id="e61bc-110">Il ne peut pas autoriser une application à accéder aux informations d'un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e61bc-110">They can't give an app access to any other user's information.</span></span>

## <a name="turning-user-consent-on-or-off"></a><span data-ttu-id="e61bc-111">Autorisation de l’utilisateur sur ou hors de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="e61bc-111">Turning user consent on or off</span></span>
<span data-ttu-id="e61bc-112"><a name="__toc379982114"> </a></span><span class="sxs-lookup"><span data-stu-id="e61bc-112"><a name="__toc379982114"> </a></span></span>

<span data-ttu-id="e61bc-113">Voici comment activer ou désactiver le consentement de l’utilisateur pour les applications.</span><span class="sxs-lookup"><span data-stu-id="e61bc-113">Here's how to turn User consent to apps on or off.</span></span>

1. <span data-ttu-id="e61bc-114">Dans le Centre d’administration, allez à la page  \> **Paramètres Org settings** Services, puis sélectionnez Consentement de l’utilisateur  >  [](https://go.microsoft.com/fwlink/p/?linkid=2053743) pour **les applications.**</span><span class="sxs-lookup"><span data-stu-id="e61bc-114">In the admin center, go to the **Settings** \> **Org settings** > [Services](https://go.microsoft.com/fwlink/p/?linkid=2053743) page, and then select **User consent to apps**.</span></span>

2. <span data-ttu-id="e61bc-115">Dans la page **Consentement de l’utilisateur aux applications,** sélectionnez l’option pour activer ou désactiver le consentement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e61bc-115">On the **User consent to apps** page, select the option to turn user consent on or off.</span></span>

## <a name="more-info"></a><span data-ttu-id="e61bc-116">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="e61bc-116">More info</span></span>
<span data-ttu-id="e61bc-117"><a name="__toc379982114"> </a></span><span class="sxs-lookup"><span data-stu-id="e61bc-117"><a name="__toc379982114"> </a></span></span>

<span data-ttu-id="e61bc-118">Pour en savoir plus sur la configuration de vos paramètres de consentement dans Azure Active Directory, lisez Configurer le flux de travail [de consentement de l’administrateur.](https://docs.microsoft.com/azure/active-directory/manage-apps/configure-admin-consent-workflow)</span><span class="sxs-lookup"><span data-stu-id="e61bc-118">To learn about how to configure your consent settings in Azure active directory, read [Configure the admin consent workflow](https://docs.microsoft.com/azure/active-directory/manage-apps/configure-admin-consent-workflow).</span></span>

<span data-ttu-id="e61bc-119">Pour en savoir plus sur la gestion du consentement des utilisateurs pour les applications, lisez Gérer le consentement des [applications et évaluer les demandes de consentement.](https://docs.microsoft.com/azure/active-directory/manage-apps/manage-consent-requests)</span><span class="sxs-lookup"><span data-stu-id="e61bc-119">To learn about managing user consent to apps, read [Managing consent to applications and evaluating consent requests](https://docs.microsoft.com/azure/active-directory/manage-apps/manage-consent-requests).</span></span>