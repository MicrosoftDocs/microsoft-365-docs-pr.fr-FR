---
title: Utiliser un code QR pour vous inscrire aux applications mobiles Outlook
f1.keywords:
- NOCSH
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- Adm_TOC
ms.custom:
- AdminSurgePortfolio
description: Découvrez comment utiliser un code QR pour authentifier et télécharger Outlook Mobile.
ms.openlocfilehash: b9e433e0c7d3f5f3466924b318e242e5ac29181c
ms.sourcegitcommit: 719b89baca1bae14455acf2e517ec18fc473636c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50122371"
---
# <a name="use-a-qr-code-to-sign-in-to-the-outlook-mobile-apps"></a><span data-ttu-id="3b11d-103">Utiliser un code QR pour vous inscrire aux applications mobiles Outlook</span><span class="sxs-lookup"><span data-stu-id="3b11d-103">Use a QR code to sign-in to the Outlook mobile apps</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3b11d-104">Cette fonctionnalité Microsoft 365 est en prévisualisation publique.</span><span class="sxs-lookup"><span data-stu-id="3b11d-104">This Microsoft 365 feature is in public preview.</span></span> <span data-ttu-id="3b11d-105">La prévisualisation publique fournit un accès en avant-première aux fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3b11d-105">Public preview provides early access to Microsoft 365 features.</span></span>

<span data-ttu-id="3b11d-106">En tant qu’administrateur Microsoft 365, vous pouvez permettre à vos utilisateurs de se connectent à Outlook pour Android ou à l’application iOS sur leurs appareils mobiles sans avoir à entrer leur nom d’utilisateur et leur mot de passe.</span><span class="sxs-lookup"><span data-stu-id="3b11d-106">As the Microsoft 365 administrator, you can enable your users to sign in to Outlook for Android or iOS app on their mobile devices without having to enter their username and password.</span></span> <span data-ttu-id="3b11d-107">En analysant un code QR, les utilisateurs peuvent s’authentifier et se connectent en toute sécurité à Outlook Mobile.</span><span class="sxs-lookup"><span data-stu-id="3b11d-107">By scanning a QR code, users can securely authenticate and sign in to Outlook mobile.</span></span>

<span data-ttu-id="3b11d-108">Dans Outlook sur le web ou dans d’autres applications Outlook de bureau, les utilisateurs peuvent voir des notifications les informant qu’ils peuvent utiliser Outlook sur leur appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="3b11d-108">In Outlook on the web or other desktop Outlook applications, users may see notifications informing them that they can use Outlook on their mobile device.</span></span> <span data-ttu-id="3b11d-109">Ces notifications peuvent être gérées par l’administrateur à l’aide d’Exchange Powershell.</span><span class="sxs-lookup"><span data-stu-id="3b11d-109">These notifications can be managed by the administrator using Exchange Powershell.</span></span> <span data-ttu-id="3b11d-110">Si les utilisateurs choisissent de s’envoyer eux-mêmes un SMS pour télécharger l’application sur leur appareil mobile, un code QR s’affiche sur leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3b11d-110">If users choose to send themselves an SMS text message to download the app on their mobile device, a QR code will appear on their computer.</span></span> <span data-ttu-id="3b11d-111">Ils pourront analyser le code QR pour se connecter à Outlook sur leur téléphone ou tablette.</span><span class="sxs-lookup"><span data-stu-id="3b11d-111">They will be able to scan the QR code to log into Outlook on their phone or tablet.</span></span> <span data-ttu-id="3b11d-112">Ce code QR est un jeton à durée de vie courte qui ne peut être échangé qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="3b11d-112">This QR code is a short lived token that can only be redeemed once.</span></span>

> [!NOTE]
> <span data-ttu-id="3b11d-113">Dans certains cas, vos utilisateurs devront s’authentifier à nouveau sur leur ordinateur pour générer le code QR.</span><span class="sxs-lookup"><span data-stu-id="3b11d-113">In some cases, your users will have to re-authenticate on their computer to generate the QR code.</span></span>

## <a name="use-exchange-powershell"></a><span data-ttu-id="3b11d-114">Utiliser Exchange PowerShell</span><span class="sxs-lookup"><span data-stu-id="3b11d-114">Use Exchange PowerShell</span></span>

<span data-ttu-id="3b11d-115">Cette expérience est en place par défaut.</span><span class="sxs-lookup"><span data-stu-id="3b11d-115">This experience is on by default.</span></span> <span data-ttu-id="3b11d-116">Pour désactiver cette fonctionnalité, suivez les étapes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="3b11d-116">To disable this feature, follow the steps below.</span></span>

1. <span data-ttu-id="3b11d-117">[Connectez-vous à Exchange PowerShell.](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell?view=exchange-ps)</span><span class="sxs-lookup"><span data-stu-id="3b11d-117">[Connect to Exchange PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell?view=exchange-ps).</span></span>
2. <span data-ttu-id="3b11d-118">À l’aide de PowerShell, vous pouvez désactiver les notifications informant vos utilisateurs des applications mobiles Outlook.</span><span class="sxs-lookup"><span data-stu-id="3b11d-118">Using PowerShell, you can disable the notifications informing your users about the Outlook mobile apps.</span></span> <span data-ttu-id="3b11d-119">Cela empêche également l’affichage du flux de la signature du code QR.</span><span class="sxs-lookup"><span data-stu-id="3b11d-119">This will also prevent the QR code sign-in flow from being shown.</span></span>

```powershell
Set-OrganizationConfig -MobileAppEducationEnabled <Boolean>
```

<span data-ttu-id="3b11d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b11d-120">Related topics</span></span>

[<span data-ttu-id="3b11d-121">Set-OrganizationConfig</span><span class="sxs-lookup"><span data-stu-id="3b11d-121">Set-OrganizationConfig</span></span>](https://docs.microsoft.com/powershell/module/exchange/set-organizationconfig?view=exchange-ps)
