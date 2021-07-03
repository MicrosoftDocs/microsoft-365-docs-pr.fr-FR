---
title: 'Microsoft 365 Prise en charge des applications clientes : accès conditionnel'
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-subscription-management
f1.keywords:
- NOCSH
description: Dans cet article, découvrez les plateformes, les clients et les modules PowerShell qui peuvent Access pour Microsoft 365.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 763380429b8643c5dd01971117fccb040a9a0210
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53286560"
---
# <a name="microsoft-365-client-app-support-conditional-access"></a><span data-ttu-id="5851a-103">Microsoft 365 Prise en charge des applications clientes : accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="5851a-103">Microsoft 365 Client App Support: Conditional Access</span></span>

<span data-ttu-id="5851a-104">Dans l’espace de travail moderne, les utilisateurs peuvent accéder aux ressources de votre organisation à l’aide de différents appareils et applications de n’importe où.</span><span class="sxs-lookup"><span data-stu-id="5851a-104">In the modern workplace, users can access your organization's resources using various devices and apps from anywhere.</span></span> <span data-ttu-id="5851a-105">Par conséquent, le simple fait de se concentrer sur les personnes qui peuvent accéder à une ressource ne suffit plus.</span><span class="sxs-lookup"><span data-stu-id="5851a-105">As a result, just focusing on who can access a resource is not sufficient anymore.</span></span> <span data-ttu-id="5851a-106">Votre organisation doit également prendre en charge comment et où une ressource est accessible dans votre infrastructure de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="5851a-106">Your organization must also support how and where a resource is accessed in your access control infrastructure.</span></span>

<span data-ttu-id="5851a-107">Avec Azure Active Directory’accès conditionnel basé sur l’authentification multifacteur, l’emplacement et l’appareil, vous pouvez répondre à cette nouvelle exigence.</span><span class="sxs-lookup"><span data-stu-id="5851a-107">With Azure Active Directory device, location, and multi-factor authentication-based Conditional Access, you can meet this new requirement.</span></span> <span data-ttu-id="5851a-108">L’accès conditionnel est une fonctionnalité de Azure Active Directory qui vous permet d’appliquer des contrôles sur l’accès aux applications dans votre environnement, en fonction de conditions spécifiques et gérés à partir d’un emplacement central.</span><span class="sxs-lookup"><span data-stu-id="5851a-108">Conditional Access is a capability of Azure Active Directory that enables you to enforce controls on the access to apps in your environment, all based on specific conditions and managed from a central location.</span></span>

<span data-ttu-id="5851a-109">En savoir plus sur [Azure Active Directory l’accès conditionnel.](/azure/active-directory/conditional-access/)</span><span class="sxs-lookup"><span data-stu-id="5851a-109">Learn more about [Azure Active Directory Conditional Access](/azure/active-directory/conditional-access/).</span></span>

## <a name="supported-clients--platforms"></a><span data-ttu-id="5851a-110">Clients pris en charge & plateformes</span><span class="sxs-lookup"><span data-stu-id="5851a-110">Supported clients & platforms</span></span>

<span data-ttu-id="5851a-111">Les dernières versions des plateformes et des clients suivants offrent une prise en charge de l’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="5851a-111">The latest versions of the following clients and platforms support conditional access.</span></span> <span data-ttu-id="5851a-112">Pour plus d’informations sur la prise en charge de la plateforme dans Microsoft 365, voir [La Microsoft 365](/microsoft-365/microsoft-365-and-office-resources).</span><span class="sxs-lookup"><span data-stu-id="5851a-112">For more information about platform support in Microsoft 365, see [System requirements for Microsoft 365](/microsoft-365/microsoft-365-and-office-resources).</span></span>
<br>
<br>

[!INCLUDE [Conditional access services support table](../includes/microsoft-365-client-support-conditional-access-include.md)]

## <a name="supported-powershell-modules"></a><span data-ttu-id="5851a-113">Modules PowerShell pris en charge</span><span class="sxs-lookup"><span data-stu-id="5851a-113">Supported PowerShell modules</span></span>

- [<span data-ttu-id="5851a-114">Azure Active Directory PowerShell</span><span class="sxs-lookup"><span data-stu-id="5851a-114">Azure Active Directory PowerShell</span></span>](/powershell/azure/active-directory/overview)
- [<span data-ttu-id="5851a-115">Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="5851a-115">Exchange Online PowerShell</span></span>](/powershell/exchange/exchange-online-powershell)
- [<span data-ttu-id="5851a-116">SharePoint Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="5851a-116">SharePoint Online PowerShell</span></span>](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)
