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
description: Découvrez le consentement des utilisateurs aux applications et comment les activer pour autoriser des applications tierces à accéder aux informations d’Microsoft 365 utilisateurs.
ms.openlocfilehash: b8f65b50e50b0e0b4d978388463bbd380ca60d4e
ms.sourcegitcommit: 686f192e1a650ec805fe8e908b46ca51771ed41f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52624500"
---
# <a name="managing-user-consent-to-apps-in-microsoft-365"></a><span data-ttu-id="ce226-103">Gestion du consentement des utilisateurs aux applications dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ce226-103">Managing user consent to apps in Microsoft 365</span></span>

<span data-ttu-id="ce226-104">Ce paramètre contrôle si les utilisateurs peuvent donner ce consentement aux applications qui utilisent OpenID Connecter et OAuth 2.0 pour la signature et les demandes d’accès aux données.</span><span class="sxs-lookup"><span data-stu-id="ce226-104">This setting controls whether users can give that consent to apps that use OpenID Connect and OAuth 2.0 for sign-in and requests to access data.</span></span> <span data-ttu-id="ce226-105">Une application peut être créée à partir de votre propre organisation, ou elle peut être créée à partir d’une autre Office 365 organisation ou d’un tiers.</span><span class="sxs-lookup"><span data-stu-id="ce226-105">An app can be created from within your own organization, or it can come from another Office 365 organization or a third-party.</span></span>

<span data-ttu-id="ce226-106">Si vous activer ce paramètre, ces applications demandent aux utilisateurs l’autorisation d’accéder aux données de votre organisation, et les utilisateurs peuvent choisir s’ils le souhaitent.</span><span class="sxs-lookup"><span data-stu-id="ce226-106">If you turn this setting on, those apps will ask users for permission to access your organization’s data, and users can choose whether to allow it.</span></span> <span data-ttu-id="ce226-107">Si vous la désactiver, les administrateurs doivent consentir à ces applications avant que les utilisateurs ne les utilisent.</span><span class="sxs-lookup"><span data-stu-id="ce226-107">If you turn this setting off, then admins must consent to those apps before users may use them.</span></span> <span data-ttu-id="ce226-108">Dans ce cas, envisagez de définir un flux de travail de consentement d’administrateur dans le portail Azure afin que les utilisateurs peuvent envoyer une demande d’approbation d’administrateur pour utiliser n’importe quelle application bloquée.</span><span class="sxs-lookup"><span data-stu-id="ce226-108">In this case, consider setting up an admin consent workflow in the Azure portal so users can send a request for admin approval to use any blocked app.</span></span>

<span data-ttu-id="ce226-109">Un utilisateur peut autoriser uniquement les applications dont il est propriétaire à accéder à ses informations Office 365.</span><span class="sxs-lookup"><span data-stu-id="ce226-109">A user can give access only to apps they own that access their Office 365 information.</span></span> <span data-ttu-id="ce226-110">Il ne peut pas autoriser une application à accéder aux informations d'un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ce226-110">They can't give an app access to any other user's information.</span></span>

## <a name="turning-user-consent-on-or-off"></a><span data-ttu-id="ce226-111">Autorisation de l’utilisateur sur ou hors de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="ce226-111">Turning user consent on or off</span></span>
<span data-ttu-id="ce226-112"><a name="__toc379982114"> </a></span><span class="sxs-lookup"><span data-stu-id="ce226-112"><a name="__toc379982114"> </a></span></span>

<span data-ttu-id="ce226-113">Voici comment activer ou désactiver le consentement de l’utilisateur pour les applications.</span><span class="sxs-lookup"><span data-stu-id="ce226-113">Here's how to turn User consent to apps on or off.</span></span>

1. <span data-ttu-id="ce226-114">Dans le Centre d’administration, allez à la page **Paramètres** Services de paramètres de l’organisation, puis sélectionnez Consentement de \>   >  [](https://go.microsoft.com/fwlink/p/?linkid=2053743) **l’utilisateur pour les applications.**</span><span class="sxs-lookup"><span data-stu-id="ce226-114">In the admin center, go to the **Settings** \> **Org settings** > [Services](https://go.microsoft.com/fwlink/p/?linkid=2053743) page, and then select **User consent to apps**.</span></span>

2. <span data-ttu-id="ce226-115">Dans la page **Consentement de l’utilisateur aux applications,** sélectionnez l’option pour activer ou désactiver le consentement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ce226-115">On the **User consent to apps** page, select the option to turn user consent on or off.</span></span>

## <a name="related-content"></a><span data-ttu-id="ce226-116">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="ce226-116">Related content</span></span> 
<span data-ttu-id="ce226-117"><a name="__toc379982114"> </a></span><span class="sxs-lookup"><span data-stu-id="ce226-117"><a name="__toc379982114"> </a></span></span>

<span data-ttu-id="ce226-118">[Configurer le flux de travail de consentement de l’administrateur](/azure/active-directory/manage-apps/configure-admin-consent-workflow) (article)</span><span class="sxs-lookup"><span data-stu-id="ce226-118">[Configure the admin consent workflow](/azure/active-directory/manage-apps/configure-admin-consent-workflow) (article)</span></span>\
<span data-ttu-id="ce226-119">[Gestion du consentement aux applications et évaluation des demandes de consentement](/azure/active-directory/manage-apps/manage-consent-requests) (article)</span><span class="sxs-lookup"><span data-stu-id="ce226-119">[Managing consent to applications and evaluating consent requests](/azure/active-directory/manage-apps/manage-consent-requests) (article)</span></span>