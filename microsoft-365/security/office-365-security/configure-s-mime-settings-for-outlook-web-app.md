---
title: Configurer les paramètres S/MIME dans Exchange Online pour Outlook sur le Web
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c7dee22c-9b5b-425c-91a9-d093204ff84e
ms.collection:
- M365-security-compliance
description: Brève description des administrateurs Exchange Online à faire pour afficher et configurer les paramètres S/MIME dans Outlook sur le Web dans Exchange Online.
ms.openlocfilehash: 408a8f7aed800175e7bae7af73d77f340359c17d
ms.sourcegitcommit: 70e920f76526f47fc849df615de4569e0ac2f4be
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2019
ms.locfileid: "38032439"
---
# <a name="configure-smime-settings-in-exchange-online-for-outlook-on-the-web"></a><span data-ttu-id="e7d93-103">Configurer les paramètres S/MIME dans Exchange Online pour Outlook sur le Web</span><span class="sxs-lookup"><span data-stu-id="e7d93-103">Configure S/MIME settings in Exchange Online for Outlook on the web</span></span>

<span data-ttu-id="e7d93-104">En tant qu’administrateur d’Exchange Online, vous pouvez configurer Outlook sur le Web (anciennement Outlook Web App) pour permettre l’envoi et la réception de messages protégés par S/MIME.</span><span class="sxs-lookup"><span data-stu-id="e7d93-104">As an admin for Exchange Online, you can set up Outlook on the web (formerly known as Outlook Web App) to allow sending and receiving S/MIME-protected messages.</span></span> <span data-ttu-id="e7d93-105">Utilisez les cmdlets **Get-SmimeConfig** et **Set-SmimeConfig** pour afficher et gérer cette fonctionnalité dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e7d93-105">Use the **Get-SmimeConfig** and **Set-SmimeConfig** cmdlets to view and manage this feature in Exchange Online PowerShell.</span></span> <span data-ttu-id="e7d93-106">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="e7d93-106">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>

<span data-ttu-id="e7d93-107">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-SmimeConfig](https://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx) et [Set-SmimeConfig](https://technet.microsoft.com/library/de357ce0-8143-4c36-8032-026292fc63f0.aspx).</span><span class="sxs-lookup"><span data-stu-id="e7d93-107">For detailed syntax and parameter information, see [Get-SmimeConfig](https://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx) and [Set-SmimeConfig](https://technet.microsoft.com/library/de357ce0-8143-4c36-8032-026292fc63f0.aspx).</span></span>

## <a name="considerations-for-chrome"></a><span data-ttu-id="e7d93-108">Considérations relatives au chrome</span><span class="sxs-lookup"><span data-stu-id="e7d93-108">Considerations for Chrome</span></span>

<span data-ttu-id="e7d93-109">Pour utiliser S/MIME dans Outlook sur le Web dans le navigateur Web Google Chrome, vous (ou un autre administrateur) devez définir et configurer la stratégie de chrome nommée **ExtensionInstallForcelist** pour installer l’extension S/MIME Microsoft dans Chrome.</span><span class="sxs-lookup"><span data-stu-id="e7d93-109">To use S/MIME in Outlook on the web in the Google Chrome web browser, you (or another admin) must set and configure the Chromium policy named **ExtensionInstallForcelist** to install the Microsoft S/MIME extension in Chrome.</span></span> <span data-ttu-id="e7d93-110">La valeur de la `maafgiompdekodanheihhgilkjchcakm;https://outlook.office.com/owa/SmimeCrxUpdate.ashx`stratégie est.</span><span class="sxs-lookup"><span data-stu-id="e7d93-110">The policy value is `maafgiompdekodanheihhgilkjchcakm;https://outlook.office.com/owa/SmimeCrxUpdate.ashx`.</span></span> <span data-ttu-id="e7d93-111">Et notez que l’application de cette stratégie nécessite des ordinateurs associés à un domaine, de sorte que l’utilisation de S/MIME dans Chrome requiert effectivement des ordinateurs liés à un domaine.</span><span class="sxs-lookup"><span data-stu-id="e7d93-111">And note that applying this policy requires domain-joined computers, so using S/MIME in Chrome effectively requires domain-joined computers.</span></span>

<span data-ttu-id="e7d93-112">Pour plus d’informations sur la stratégie **ExtensionInstallForcelist** , voir [ExtensionInstallForcelist](https://dev.chromium.org/administrators/policy-list-3#ExtensionInstallForcelist).</span><span class="sxs-lookup"><span data-stu-id="e7d93-112">For details about the **ExtensionInstallForcelist** policy, see [ExtensionInstallForcelist](https://dev.chromium.org/administrators/policy-list-3#ExtensionInstallForcelist).</span></span>

<span data-ttu-id="e7d93-113">Cette étape est requise pour utiliser Chrome ; il ne remplace pas le contrôle S/MIME qui est installé par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e7d93-113">This step is a prerequisite for using Chrome; it does not replace the S/MIME control that's installed by users.</span></span> <span data-ttu-id="e7d93-114">Les utilisateurs sont invités à télécharger et à installer le contrôle S/MIME dans Outlook sur le Web lors de leur première utilisation de S/MIME.</span><span class="sxs-lookup"><span data-stu-id="e7d93-114">Users are prompted to download and install the S/MIME control in Outlook on the web during their first use of S/MIME.</span></span> <span data-ttu-id="e7d93-115">Ou, les utilisateurs peuvent accéder de manière proactive à **S/MIME** dans leurs paramètres Outlook sur le Web pour obtenir le lien de téléchargement pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="e7d93-115">Or, users can proactively go to **S/MIME** in their Outlook on the web settings to get the download link for the control.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="e7d93-116">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="e7d93-116">For more information</span></span>

[<span data-ttu-id="e7d93-117">S/MIME pour la signature et le chiffrement des messages</span><span class="sxs-lookup"><span data-stu-id="e7d93-117">S/MIME for message signing and encryption</span></span>](s-mime-for-message-signing-and-encryption.md)
