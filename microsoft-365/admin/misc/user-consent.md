---
title: Gestion du consentement de l’utilisateur pour les applications dans Microsoft 365
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
description: Découvrez le consentement de l’utilisateur pour les applications et comment l’activer pour permettre aux applications tierces d’accéder aux informations Microsoft 365.
ms.openlocfilehash: 955ae9e58c14dbb8012a440ef6c336f44b0760a4
ms.sourcegitcommit: da34ac08c7d029c2c42d4428d0bb03fd57c448be
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/12/2020
ms.locfileid: "48999570"
---
# <a name="managing-user-consent-to-apps-in-microsoft-365"></a><span data-ttu-id="43234-103">Gestion du consentement de l’utilisateur pour les applications dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="43234-103">Managing user consent to apps in Microsoft 365</span></span>

<span data-ttu-id="43234-104">Ce paramètre contrôle si les utilisateurs peuvent accorder cette consentement aux applications qui utilisent OpenID Connect et OAuth 2,0 pour la connexion et les demandes d’accès aux données.</span><span class="sxs-lookup"><span data-stu-id="43234-104">This setting controls whether users can give that consent to apps that use OpenID Connect and OAuth 2.0 for sign-in and requests to access data.</span></span> <span data-ttu-id="43234-105">Une application peut être créée au sein de votre organisation ou peut provenir d’une autre organisation Office 365 ou d’une tierce partie.</span><span class="sxs-lookup"><span data-stu-id="43234-105">An app can be created from within your own organization, or it can come from another Office 365 organization or a third-party.</span></span>

<span data-ttu-id="43234-106">Si vous activez ce paramètre, ces applications demandent aux utilisateurs l’autorisation d’accéder aux données de votre organisation, et les utilisateurs peuvent choisir de les autoriser ou non.</span><span class="sxs-lookup"><span data-stu-id="43234-106">If you turn this setting on, those apps will ask users for permission to access your organization’s data, and users can choose whether to allow it.</span></span> <span data-ttu-id="43234-107">Si vous désactivez ce paramètre, les administrateurs doivent consentir à ces applications avant que les utilisateurs puissent les utiliser.</span><span class="sxs-lookup"><span data-stu-id="43234-107">If you turn this setting off, then admins must consent to those apps before users may use them.</span></span> <span data-ttu-id="43234-108">Dans ce cas, envisagez de configurer un flux de travail de consentement administratif dans le portail Azure pour permettre aux utilisateurs d’envoyer une demande d’approbation à l’administrateur afin d’utiliser une application bloquée.</span><span class="sxs-lookup"><span data-stu-id="43234-108">In this case, consider setting up an admin consent workflow in the Azure portal so users can send a request for admin approval to use any blocked app.</span></span>

<span data-ttu-id="43234-109">Un utilisateur peut autoriser uniquement les applications dont il est propriétaire à accéder à ses informations Office 365.</span><span class="sxs-lookup"><span data-stu-id="43234-109">A user can give access only to apps they own that access their Office 365 information.</span></span> <span data-ttu-id="43234-110">Il ne peut pas autoriser une application à accéder aux informations d'un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="43234-110">They can't give an app access to any other user's information.</span></span>

## <a name="turning-user-consent-on-or-off"></a><span data-ttu-id="43234-111">Activation ou désactivation du consentement de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="43234-111">Turning user consent on or off</span></span>
<span data-ttu-id="43234-112"><a name="__toc379982114"> </a></span><span class="sxs-lookup"><span data-stu-id="43234-112"><a name="__toc379982114"> </a></span></span>

<span data-ttu-id="43234-113">Voici comment activer ou désactiver le consentement de l’utilisateur pour les applications.</span><span class="sxs-lookup"><span data-stu-id="43234-113">Here's how to turn User consent to apps on or off.</span></span>

1. <span data-ttu-id="43234-114">Dans le centre d’administration, accédez à la page **paramètres** d’organisation des paramètres, puis \> **Org settings**  >  [Services](https://go.microsoft.com/fwlink/p/?linkid=2053743) sélectionnez **consentement de l’utilisateur pour les applications**.</span><span class="sxs-lookup"><span data-stu-id="43234-114">In the admin center, go to the **Settings** \> **Org settings** > [Services](https://go.microsoft.com/fwlink/p/?linkid=2053743) page, and then select **User consent to apps**.</span></span>

2. <span data-ttu-id="43234-115">Sur la page de **consentement de l’utilisateur pour les applications** , sélectionnez l’option permettant d’activer ou de désactiver le consentement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="43234-115">On the **User consent to apps** page, select the option to turn user consent on or off.</span></span>

## <a name="more-info"></a><span data-ttu-id="43234-116">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="43234-116">More info</span></span>
<span data-ttu-id="43234-117"><a name="__toc379982114"> </a></span><span class="sxs-lookup"><span data-stu-id="43234-117"><a name="__toc379982114"> </a></span></span>

<span data-ttu-id="43234-118">Pour en savoir plus sur la configuration de vos paramètres de consentement dans Azure Active Directory, consultez [la rubrique Configurer le flux de travail de consentement de l’administrateur](https://docs.microsoft.com/azure/active-directory/manage-apps/configure-admin-consent-workflow).</span><span class="sxs-lookup"><span data-stu-id="43234-118">To learn about how to configure your consent settings in Azure active directory, read [Configure the admin consent workflow](https://docs.microsoft.com/azure/active-directory/manage-apps/configure-admin-consent-workflow).</span></span>

<span data-ttu-id="43234-119">Pour en savoir plus sur la gestion du consentement de l’utilisateur pour les applications, consultez la rubrique [gestion du consentement sur les applications et évaluation des demandes de consentement](https://docs.microsoft.com/azure/active-directory/manage-apps/manage-consent-requests).</span><span class="sxs-lookup"><span data-stu-id="43234-119">To learn about managing user consent to apps, read [Managing consent to applications and evaluating consent requests](https://docs.microsoft.com/azure/active-directory/manage-apps/manage-consent-requests).</span></span>