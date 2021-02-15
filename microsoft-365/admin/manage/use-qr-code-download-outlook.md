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
ms.openlocfilehash: 1e5207a2792b557689a306fa1474a2c5fac81ed9
ms.sourcegitcommit: 78f48304f990e969a052fe6536b2e8d6856e1086
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2021
ms.locfileid: "50242353"
---
# <a name="use-a-qr-code-to-sign-in-to-the-outlook-mobile-apps"></a><span data-ttu-id="76941-103">Utiliser un code QR pour vous inscrire aux applications mobiles Outlook</span><span class="sxs-lookup"><span data-stu-id="76941-103">Use a QR code to sign-in to the Outlook mobile apps</span></span>

> [!IMPORTANT]
> <span data-ttu-id="76941-104">Cette fonctionnalité est uniquement disponible pour les organisations qui ont mis en place la publication ciblée dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="76941-104">This feature is only available to organizations who have turned on Targeted Release in the Microsoft 365 admin center.</span></span> <span data-ttu-id="76941-105">Pour activer la version ciblée et en savoir plus sur son fonctionnement, voir Configurer les options de publication [standard ou ciblée.](release-options-in-office-365.md)</span><span class="sxs-lookup"><span data-stu-id="76941-105">To turn on Targeted release and learn more about how it works, see [Set up the Standard or Targeted release options](release-options-in-office-365.md).</span></span> <span data-ttu-id="76941-106">Nous allons développer davantage d’organisations au cours des prochaines semaines jusqu’à la prévisualisation publique.</span><span class="sxs-lookup"><span data-stu-id="76941-106">We’ll be expanding to more organizations in the coming weeks through public preview.</span></span> <span data-ttu-id="76941-107">La prévisualisation publique fournit un accès en avant-première aux fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="76941-107">Public preview provides early access to Microsoft 365 features.</span></span>

<span data-ttu-id="76941-108">En tant qu’administrateur Microsoft 365, vous pouvez permettre à vos utilisateurs de se connectent à Outlook pour Android ou à l’application iOS sur leurs appareils mobiles sans avoir à entrer leur nom d’utilisateur et leur mot de passe.</span><span class="sxs-lookup"><span data-stu-id="76941-108">As the Microsoft 365 administrator, you can enable your users to sign in to Outlook for Android or iOS app on their mobile devices without having to enter their username and password.</span></span> <span data-ttu-id="76941-109">En analysant un code QR, les utilisateurs peuvent s’authentifier en toute sécurité et se connectent à Outlook Mobile.</span><span class="sxs-lookup"><span data-stu-id="76941-109">By scanning a QR code, users can securely authenticate and sign in to Outlook mobile.</span></span>

<span data-ttu-id="76941-110">Dans Outlook sur le web ou dans d’autres applications Outlook de bureau, les utilisateurs peuvent voir des notifications les informant qu’ils peuvent utiliser Outlook sur leur appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="76941-110">In Outlook on the web or other desktop Outlook applications, users may see notifications informing them that they can use Outlook on their mobile device.</span></span> <span data-ttu-id="76941-111">Ces notifications peuvent être gérées par l’administrateur à l’aide d’Exchange Powershell.</span><span class="sxs-lookup"><span data-stu-id="76941-111">These notifications can be managed by the administrator using Exchange Powershell.</span></span> <span data-ttu-id="76941-112">Si les utilisateurs choisissent de s’envoyer eux-mêmes un SMS pour télécharger l’application sur leur appareil mobile, un code QR s’affiche sur leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="76941-112">If users choose to send themselves an SMS text message to download the app on their mobile device, a QR code will appear on their computer.</span></span> <span data-ttu-id="76941-113">Ils pourront analyser le code QR pour se connecter à Outlook sur leur téléphone ou tablette.</span><span class="sxs-lookup"><span data-stu-id="76941-113">They will be able to scan the QR code to log into Outlook on their phone or tablet.</span></span> <span data-ttu-id="76941-114">Ce code QR est un jeton à durée de vie courte qui ne peut être échangé qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="76941-114">This QR code is a short lived token that can only be redeemed once.</span></span>

> [!NOTE]
> <span data-ttu-id="76941-115">Dans certains cas, vos utilisateurs devront s’authentifier à nouveau sur leur ordinateur pour générer le code QR.</span><span class="sxs-lookup"><span data-stu-id="76941-115">In some cases, your users will have to re-authenticate on their computer to generate the QR code.</span></span>

## <a name="use-exchange-powershell"></a><span data-ttu-id="76941-116">Utiliser Exchange PowerShell</span><span class="sxs-lookup"><span data-stu-id="76941-116">Use Exchange PowerShell</span></span>

<span data-ttu-id="76941-117">Cette fonctionnalité est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="76941-117">This feature is on by default.</span></span> <span data-ttu-id="76941-118">Pour désactiver cette fonctionnalité, suivez les étapes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="76941-118">To disable this feature, follow the steps below.</span></span>

1. <span data-ttu-id="76941-119">[Connectez-vous à Exchange PowerShell.](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell?view=exchange-ps)</span><span class="sxs-lookup"><span data-stu-id="76941-119">[Connect to Exchange PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell?view=exchange-ps).</span></span>
2. <span data-ttu-id="76941-120">À l’aide de PowerShell, vous pouvez désactiver les notifications informant vos utilisateurs des applications mobiles Outlook.</span><span class="sxs-lookup"><span data-stu-id="76941-120">Using PowerShell, you can disable the notifications informing your users about the Outlook mobile apps.</span></span> <span data-ttu-id="76941-121">Cela empêche également l’affichage du flux de la signature du code QR.</span><span class="sxs-lookup"><span data-stu-id="76941-121">This will also prevent the QR code sign-in flow from being shown.</span></span>

```powershell
Set-OrganizationConfig -MobileAppEducationEnabled <Boolean>
```

<span data-ttu-id="76941-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76941-122">Related topics</span></span>

[<span data-ttu-id="76941-123">Set-OrganizationConfig</span><span class="sxs-lookup"><span data-stu-id="76941-123">Set-OrganizationConfig</span></span>](https://docs.microsoft.com/powershell/module/exchange/set-organizationconfig?view=exchange-ps)
