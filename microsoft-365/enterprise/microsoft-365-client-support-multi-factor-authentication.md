---
title: 'Microsoft 365 Prise en charge des applications clientes : authentification multifacteur'
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Strat_O365_Enterprise
- M365-subscription-management
search.appverid:
- MET150
f1.keywords:
- NOCSH
description: Dans cet article, découvrez les plateformes, les clients et les modules PowerShell qui la prise en charge de l’authentification multifacteur pour Microsoft 365.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 8749c05e3f7ce5dacf7d3ed1eaa46a46a20482d5
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53286452"
---
# <a name="microsoft-365-client-app-support-multi-factor-authentication"></a><span data-ttu-id="f5f12-103">Microsoft 365 Prise en charge des applications clientes : authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="f5f12-103">Microsoft 365 Client App Support: Multi-factor authentication</span></span>

<span data-ttu-id="f5f12-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="f5f12-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="f5f12-105">Pour fournir un niveau de sécurité supplémentaire pour les sign-ins, les clients peuvent être configurés pour utiliser l’authentification multifacteur (MFA), qui utilise à la fois un mot de passe utilisateur et une autre méthode de vérification utilisateur en fonction des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="f5f12-105">To provide an additional level of security for sign-ins, clients may be configured to use multi-factor authentication (MFA), which uses both a user password and another user verification method based on:</span></span>

- <span data-ttu-id="f5f12-106">Quelque chose en leur possession qui n’est pas facilement dupliqué, tel qu’un smartphone.</span><span class="sxs-lookup"><span data-stu-id="f5f12-106">Something  in their possession that is not easily duplicated, such as a smart phone.</span></span>
- <span data-ttu-id="f5f12-107">Quelque chose que l’utilisateur possède de manière unique et err ment, par exemple ses empreintes digitales, son visage ou tout autre attribut biométrique</span><span class="sxs-lookup"><span data-stu-id="f5f12-107">Something the user has uniquely and biologically, such as their fingerprints, face, or other biometric attribute</span></span>

<span data-ttu-id="f5f12-108">En savoir plus sur [l’authentification multifacteur.](/azure/active-directory/authentication/multi-factor-authentication)</span><span class="sxs-lookup"><span data-stu-id="f5f12-108">Learn more about [multi-factor authentication](/azure/active-directory/authentication/multi-factor-authentication).</span></span>

## <a name="supported-clients--platforms"></a><span data-ttu-id="f5f12-109">Clients pris en charge & plateformes</span><span class="sxs-lookup"><span data-stu-id="f5f12-109">Supported clients & platforms</span></span>

<span data-ttu-id="f5f12-110">Les dernières versions des plateformes et des clients suivants prisent en charge l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="f5f12-110">The latest versions of the following clients and platforms support multi-factor authentication.</span></span> <span data-ttu-id="f5f12-111">Pour plus d’informations sur la prise en charge de la plateforme dans Microsoft 365, voir [La Microsoft 365](/microsoft-365/microsoft-365-and-office-resources).</span><span class="sxs-lookup"><span data-stu-id="f5f12-111">For more information about platform support in Microsoft 365, see [System requirements for Microsoft 365](/microsoft-365/microsoft-365-and-office-resources).</span></span>
<br>
<br>

[!INCLUDE [Multi-factor authentication services support table](../includes/microsoft-365-client-support-modern-authentication-include.md)]

## <a name="supported-powershell-modules"></a><span data-ttu-id="f5f12-112">Modules PowerShell pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5f12-112">Supported PowerShell modules</span></span>

- [<span data-ttu-id="f5f12-113">Azure Active Directory PowerShell</span><span class="sxs-lookup"><span data-stu-id="f5f12-113">Azure Active Directory PowerShell</span></span>](/powershell/azure/active-directory/overview)
- [<span data-ttu-id="f5f12-114">Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="f5f12-114">Exchange Online PowerShell</span></span>](/powershell/exchange/exchange-online-powershell)
- [<span data-ttu-id="f5f12-115">SharePoint Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="f5f12-115">SharePoint Online PowerShell</span></span>](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)
