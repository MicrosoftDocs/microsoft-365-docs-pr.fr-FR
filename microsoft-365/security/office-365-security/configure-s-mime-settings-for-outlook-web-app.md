---
title: Configurer les paramètres S/MIME - Exchange Online pour Outlook sur le web
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: how-to
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c7dee22c-9b5b-425c-91a9-d093204ff84e
ms.collection:
- M365-security-compliance
description: Brève description de ce que les administrateurs Exchange Online doivent faire pour afficher et configurer les paramètres S/MIME dans Outlook sur le web dans Exchange Online.
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 6eacc6a264682474054d0d3546b831039bee9a0c
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51203941"
---
# <a name="configure-smime-settings-in-exchange-online-for-outlook-on-the-web"></a><span data-ttu-id="30cae-103">Configurer les paramètres S/MIME dans Exchange Online pour Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="30cae-103">Configure S/MIME settings in Exchange Online for Outlook on the web</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="30cae-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="30cae-104">**Applies to**</span></span>
- [<span data-ttu-id="30cae-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="30cae-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="30cae-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="30cae-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="30cae-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="30cae-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="30cae-108">En tant qu’administrateur d’Exchange Online, vous pouvez configurer Outlook sur le web (anciennement Outlook Web App) pour autoriser l’envoi et la réception de messages protégés par S/MIME.</span><span class="sxs-lookup"><span data-stu-id="30cae-108">As an admin for Exchange Online, you can set up Outlook on the web (formerly known as Outlook Web App) to allow sending and receiving S/MIME-protected messages.</span></span> <span data-ttu-id="30cae-109">Utilisez les cmdlets **Get-SmimeConfig** et **Set-SmimeConfig** pour afficher et gérer cette fonctionnalité dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="30cae-109">Use the **Get-SmimeConfig** and **Set-SmimeConfig** cmdlets to view and manage this feature in Exchange Online PowerShell.</span></span> <span data-ttu-id="30cae-110">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="30cae-110">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

<span data-ttu-id="30cae-111">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-SmimeConfig](/powershell/module/exchange/get-smimeconfig) et [Set-SmimeConfig](/powershell/module/exchange/set-smimeconfig).</span><span class="sxs-lookup"><span data-stu-id="30cae-111">For detailed syntax and parameter information, see [Get-SmimeConfig](/powershell/module/exchange/get-smimeconfig) and [Set-SmimeConfig](/powershell/module/exchange/set-smimeconfig).</span></span>

## <a name="considerations-for-new-microsoft-edge-chromium-based"></a><span data-ttu-id="30cae-112">Considérations pour le nouveau Microsoft Edge (basé sur Chromium)</span><span class="sxs-lookup"><span data-stu-id="30cae-112">Considerations for new Microsoft Edge (Chromium-based)</span></span>

<span data-ttu-id="30cae-113">Pour utiliser S/MIME dans Outlook sur le web dans le nouveau navigateur web [Microsoft Edge,](https://www.microsoft.com/windows/microsoft-edge) vous (ou un autre administrateur) devez définir et configurer la stratégie de navigateur Microsoft Edge nommée **ExtensionInstallForcelist** pour installer l’extension Microsoft S/MIME dans le nouveau Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="30cae-113">To use S/MIME in Outlook on the web in the new [Microsoft Edge](https://www.microsoft.com/windows/microsoft-edge) web browser, you (or another admin) must set and configure the Microsoft Edge browser policy named **ExtensionInstallForcelist** to install the Microsoft S/MIME extension in the new Microsoft Edge.</span></span> <span data-ttu-id="30cae-114">La valeur de la stratégie `maafgiompdekodanheihhgilkjchcakm;https://outlook.office.com/owa/SmimeCrxUpdate.ashx` est .</span><span class="sxs-lookup"><span data-stu-id="30cae-114">The policy value is `maafgiompdekodanheihhgilkjchcakm;https://outlook.office.com/owa/SmimeCrxUpdate.ashx`.</span></span> <span data-ttu-id="30cae-115">Notez également que l’application de cette stratégie nécessite des appareils joints à un domaine ou à Azure AD, donc l’utilisation de S/MIME dans le nouveau navigateur Microsoft Edge nécessite effectivement des appareils joints à un domaine ou à Azure AD.</span><span class="sxs-lookup"><span data-stu-id="30cae-115">And note that applying this policy requires domain-joined or Azure AD-joined devices, so using S/MIME in the new Microsoft Edge browser effectively requires domain-joined or Azure AD-joined devices.</span></span>

<span data-ttu-id="30cae-116">Pour plus d’informations **sur la stratégie ExtensionInstallForcelist,** voir [ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist).</span><span class="sxs-lookup"><span data-stu-id="30cae-116">For details about the **ExtensionInstallForcelist** policy, see [ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist).</span></span>

<span data-ttu-id="30cae-117">Cette étape est une condition préalable à l’utilisation du nouveau Microsoft Edge . Il ne remplace pas le contrôle S/MIME installé par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="30cae-117">This step is a prerequisite for using new Microsoft Edge; it does not replace the S/MIME control that's installed by users.</span></span> <span data-ttu-id="30cae-118">Les utilisateurs sont invités à télécharger et installer le contrôle S/MIME dans Outlook sur le web lors de leur première utilisation de S/MIME.</span><span class="sxs-lookup"><span data-stu-id="30cae-118">Users are prompted to download and install the S/MIME control in Outlook on the web during their first use of S/MIME.</span></span> <span data-ttu-id="30cae-119">Les utilisateurs peuvent également se rendre de manière proactive sur **S/MIME** dans leurs paramètres Outlook sur le web pour obtenir le lien de téléchargement du contrôle.</span><span class="sxs-lookup"><span data-stu-id="30cae-119">Or, users can proactively go to **S/MIME** in their Outlook on the web settings to get the download link for the control.</span></span>

## <a name="considerations-for-chrome"></a><span data-ttu-id="30cae-120">Considérations pour Chrome</span><span class="sxs-lookup"><span data-stu-id="30cae-120">Considerations for Chrome</span></span>

<span data-ttu-id="30cae-121">Pour utiliser S/MIME dans Outlook sur le web dans le navigateur web Google Chrome, vous (ou un autre administrateur) devez définir et configurer la stratégie Chromium nommée **ExtensionInstallForcelist** pour installer l’extension Microsoft S/MIME dans Chrome.</span><span class="sxs-lookup"><span data-stu-id="30cae-121">To use S/MIME in Outlook on the web in the Google Chrome web browser, you (or another admin) must set and configure the Chromium policy named **ExtensionInstallForcelist** to install the Microsoft S/MIME extension in Chrome.</span></span> <span data-ttu-id="30cae-122">La valeur de la stratégie `maafgiompdekodanheihhgilkjchcakm;https://outlook.office.com/owa/SmimeCrxUpdate.ashx` est .</span><span class="sxs-lookup"><span data-stu-id="30cae-122">The policy value is `maafgiompdekodanheihhgilkjchcakm;https://outlook.office.com/owa/SmimeCrxUpdate.ashx`.</span></span> <span data-ttu-id="30cae-123">Notez également que l’application de cette stratégie nécessite des ordinateurs joints à un domaine, de sorte que l’utilisation de S/MIME dans Chrome nécessite effectivement des ordinateurs joints à un domaine.</span><span class="sxs-lookup"><span data-stu-id="30cae-123">And note that applying this policy requires domain-joined computers, so using S/MIME in Chrome effectively requires domain-joined computers.</span></span>

<span data-ttu-id="30cae-124">Pour plus d’informations **sur la stratégie ExtensionInstallForcelist,** voir [ExtensionInstallForcelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionInstallForcelist).</span><span class="sxs-lookup"><span data-stu-id="30cae-124">For details about the **ExtensionInstallForcelist** policy, see [ExtensionInstallForcelist](https://cloud.google.com/docs/chrome-enterprise/policies/?policy=ExtensionInstallForcelist).</span></span>

<span data-ttu-id="30cae-125">Cette étape est une condition préalable à l’utilisation de Chrome ; Il ne remplace pas le contrôle S/MIME installé par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="30cae-125">This step is a prerequisite for using Chrome; it does not replace the S/MIME control that's installed by users.</span></span> <span data-ttu-id="30cae-126">Les utilisateurs sont invités à télécharger et installer le contrôle S/MIME dans Outlook sur le web lors de leur première utilisation de S/MIME.</span><span class="sxs-lookup"><span data-stu-id="30cae-126">Users are prompted to download and install the S/MIME control in Outlook on the web during their first use of S/MIME.</span></span> <span data-ttu-id="30cae-127">Les utilisateurs peuvent également se rendre de manière proactive sur **S/MIME** dans leurs paramètres Outlook sur le web pour obtenir le lien de téléchargement du contrôle.</span><span class="sxs-lookup"><span data-stu-id="30cae-127">Or, users can proactively go to **S/MIME** in their Outlook on the web settings to get the download link for the control.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="30cae-128">Pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="30cae-128">For more information</span></span>

[<span data-ttu-id="30cae-129">S/MIME pour la signature et le chiffrement des messages</span><span class="sxs-lookup"><span data-stu-id="30cae-129">S/MIME for message signing and encryption</span></span>](s-mime-for-message-signing-and-encryption.md)