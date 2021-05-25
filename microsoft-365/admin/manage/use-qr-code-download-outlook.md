---
title: Utiliser un code QR pour vous Outlook applications mobiles
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
description: Découvrez comment utiliser un code QR pour vous authentifier et télécharger Outlook mobile.
ms.openlocfilehash: 2c1853a6ea1dd1a5d2ad30b975d1dbd23b942040
ms.sourcegitcommit: 17f0aada83627d9defa0acf4db03a2d58e46842f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52635997"
---
# <a name="use-a-qr-code-to-sign-in-to-the-outlook-mobile-apps"></a><span data-ttu-id="167f2-103">Utiliser un code QR pour vous Outlook applications mobiles</span><span class="sxs-lookup"><span data-stu-id="167f2-103">Use a QR code to sign-in to the Outlook mobile apps</span></span>

> [!IMPORTANT]
> <span data-ttu-id="167f2-104">Cette fonctionnalité est uniquement disponible pour les organisations qui ont mis en place la publication ciblée dans Microsoft 365'administration centrale.</span><span class="sxs-lookup"><span data-stu-id="167f2-104">This feature is only available to organizations that have turned on Targeted Release in the Microsoft 365 admin center.</span></span> <span data-ttu-id="167f2-105">Pour activer la version ciblée et en savoir plus sur son fonctionnement, voir Configurer les options de publication [standard ou ciblée.](release-options-in-office-365.md)</span><span class="sxs-lookup"><span data-stu-id="167f2-105">To turn on Targeted release and learn more about how it works, see [Set up the Standard or Targeted release options](release-options-in-office-365.md).</span></span> <span data-ttu-id="167f2-106">Nous allons développer davantage d’organisations au cours des prochaines semaines jusqu’à la prévisualisation publique.</span><span class="sxs-lookup"><span data-stu-id="167f2-106">We’ll be expanding to more organizations in the coming weeks through public preview.</span></span> <span data-ttu-id="167f2-107">La prévisualisation publique fournit un accès en avant-première Microsoft 365 fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="167f2-107">Public preview provides early access to Microsoft 365 features.</span></span>

<span data-ttu-id="167f2-108">En tant qu’administrateur Microsoft 365, vous pouvez permettre à vos utilisateurs de se connectés à Outlook pour Android ou l’application iOS sur leurs appareils mobiles sans avoir à entrer leur nom d’utilisateur et leur mot de passe.</span><span class="sxs-lookup"><span data-stu-id="167f2-108">As the Microsoft 365 administrator, you can enable your users to sign in to Outlook for Android or iOS app on their mobile devices without having to enter their username and password.</span></span> <span data-ttu-id="167f2-109">En analysant un code QR, les utilisateurs peuvent s’authentifier en toute sécurité et se Outlook mobile.</span><span class="sxs-lookup"><span data-stu-id="167f2-109">By scanning a QR code, users can securely authenticate and sign in to Outlook mobile.</span></span>

<span data-ttu-id="167f2-110">Dans Outlook web ou d’autres applications de bureau Outlook, les utilisateurs peuvent voir des notifications les informant qu’ils peuvent utiliser Outlook sur leur appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="167f2-110">In Outlook on the web or other desktop Outlook applications, users may see notifications informing them that they can use Outlook on their mobile device.</span></span> <span data-ttu-id="167f2-111">Ces notifications peuvent être gérées par l’administrateur à l’aide Exchange PowerShell.</span><span class="sxs-lookup"><span data-stu-id="167f2-111">These notifications can be managed by the administrator using Exchange Powershell.</span></span> <span data-ttu-id="167f2-112">Si les utilisateurs choisissent de s’envoyer SMS message texte pour télécharger l’application sur leur appareil mobile, un code QR s’affiche sur leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="167f2-112">If users choose to send themselves an SMS text message to download the app on their mobile device, a QR code will appear on their computer.</span></span> <span data-ttu-id="167f2-113">Ils pourront analyser le code QR pour se connecter Outlook téléphone ou tablette.</span><span class="sxs-lookup"><span data-stu-id="167f2-113">They will be able to scan the QR code to log into Outlook on their phone or tablet.</span></span> <span data-ttu-id="167f2-114">Ce code QR est un jeton à durée de vie courte qui ne peut être échangé qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="167f2-114">This QR code is a short lived token that can only be redeemed once.</span></span>

> [!NOTE]
> <span data-ttu-id="167f2-115">Dans certains cas, vos utilisateurs doivent s’authentifier à nouveau sur leur ordinateur pour générer le code QR.</span><span class="sxs-lookup"><span data-stu-id="167f2-115">In some cases, your users must re-authenticate on their computer to generate the QR code.</span></span>

## <a name="use-exchange-powershell"></a><span data-ttu-id="167f2-116">Utiliser Exchange PowerShell</span><span class="sxs-lookup"><span data-stu-id="167f2-116">Use Exchange PowerShell</span></span>

<span data-ttu-id="167f2-117">Cette fonctionnalité est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="167f2-117">This feature is on by default.</span></span> <span data-ttu-id="167f2-118">Pour désactiver cette fonctionnalité, suivez les étapes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="167f2-118">To disable this feature, follow the steps below.</span></span>

1. <span data-ttu-id="167f2-119">[Connecter à Exchange PowerShell.](/powershell/exchange/connect-to-exchange-online-powershell?view=exchange-ps)</span><span class="sxs-lookup"><span data-stu-id="167f2-119">[Connect to Exchange PowerShell](/powershell/exchange/connect-to-exchange-online-powershell?view=exchange-ps).</span></span>
2. <span data-ttu-id="167f2-120">À l’aide de PowerShell, vous pouvez désactiver les notifications informant vos utilisateurs des Outlook applications mobiles.</span><span class="sxs-lookup"><span data-stu-id="167f2-120">Using PowerShell, you can disable the notifications informing your users about the Outlook mobile apps.</span></span> <span data-ttu-id="167f2-121">Cela empêche également l’affichage du flux de la signature du code QR.</span><span class="sxs-lookup"><span data-stu-id="167f2-121">This also prevents the QR code sign-in flow from being shown.</span></span>

```powershell
Set-OrganizationConfig -MobileAppEducationEnabled <Boolean>
```

## <a name="related-content"></a><span data-ttu-id="167f2-122">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="167f2-122">Related content</span></span>

<span data-ttu-id="167f2-123">[Configurer les options de publication standard](release-options-in-office-365.md) ou ciblée (article)</span><span class="sxs-lookup"><span data-stu-id="167f2-123">[Set up the Standard or Targeted release options](release-options-in-office-365.md) (article)</span></span>\
<span data-ttu-id="167f2-124">[Set-OrganizationConfig](/powershell/module/exchange/set-organizationconfig?view=exchange-ps) (article)</span><span class="sxs-lookup"><span data-stu-id="167f2-124">[Set-OrganizationConfig](/powershell/module/exchange/set-organizationconfig?view=exchange-ps) (article)</span></span>