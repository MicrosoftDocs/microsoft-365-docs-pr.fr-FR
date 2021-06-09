---
title: Créer des indicateurs basés sur des certificats
ms.reviewer: ''
description: Créez des indicateurs basés sur des certificats qui définissent la détection, la prévention et l’exclusion des entités.
keywords: ioc, certificat, certificats, gérer, autorisé, bloqué, bloquer, nettoyer, malveillant, hachage de fichier, adresse IP, url, domaine
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: b75a8cf1d2681281555a3b7bb80deadfc11ee44c
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52845449"
---
# <a name="create-indicators-based-on-certificates"></a><span data-ttu-id="94eb2-104">Créer des indicateurs basés sur des certificats</span><span class="sxs-lookup"><span data-stu-id="94eb2-104">Create indicators based on certificates</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="94eb2-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="94eb2-105">**Applies to:**</span></span>
- [<span data-ttu-id="94eb2-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="94eb2-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="94eb2-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="94eb2-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


><span data-ttu-id="94eb2-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="94eb2-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="94eb2-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="94eb2-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/en-us/WindowsForBusiness/windows-atp?ocid=docs-wdatp-automationexclusionlist-abovefoldlink)

<span data-ttu-id="94eb2-110">Vous pouvez créer des indicateurs pour les certificats.</span><span class="sxs-lookup"><span data-stu-id="94eb2-110">You can create indicators for certificates.</span></span> <span data-ttu-id="94eb2-111">Voici quelques cas d’utilisation courants :</span><span class="sxs-lookup"><span data-stu-id="94eb2-111">Some common use cases include:</span></span>

- <span data-ttu-id="94eb2-112">Scénarios dans le cas où vous devez déployer [](controlled-folders.md) des technologies de blocage, telles que les règles de réduction de la [surface](attack-surface-reduction.md) d’attaque et l’accès contrôlé aux dossiers, mais qui doivent autoriser les comportements des applications signées en ajoutant le certificat dans la liste d’autorisations.</span><span class="sxs-lookup"><span data-stu-id="94eb2-112">Scenarios when you need to deploy blocking technologies, such as [attack surface reduction rules](attack-surface-reduction.md) and [controlled folder access](controlled-folders.md) but need to allow behaviors from signed applications by adding the certificate in the allow list.</span></span>
- <span data-ttu-id="94eb2-113">Blocage de l’utilisation d’une application signée spécifique au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="94eb2-113">Blocking the use of a specific signed application across your organization.</span></span> <span data-ttu-id="94eb2-114">En créant un indicateur pour bloquer le certificat de l’application, l’antivirus Windows Defender empêchera les exécutions de fichiers (blocage et correction) et les examens et corrections automatisés se comporteront de la même manière.</span><span class="sxs-lookup"><span data-stu-id="94eb2-114">By creating an indicator to block the certificate of the application, Windows Defender AV will prevent file executions (block and remediate) and the Automated Investigation and Remediation behave the same.</span></span>


### <a name="before-you-begin"></a><span data-ttu-id="94eb2-115">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="94eb2-115">Before you begin</span></span>

<span data-ttu-id="94eb2-116">Il est important de comprendre les exigences suivantes avant de créer des indicateurs pour les certificats :</span><span class="sxs-lookup"><span data-stu-id="94eb2-116">It's important to understand the following requirements prior to creating indicators for certificates:</span></span>

- <span data-ttu-id="94eb2-117">Cette fonctionnalité est disponible si votre organisation utilise Antivirus Windows Defender protection basée sur le cloud est activée.</span><span class="sxs-lookup"><span data-stu-id="94eb2-117">This feature is available if your organization uses Windows Defender Antivirus and Cloud-based protection is enabled.</span></span> <span data-ttu-id="94eb2-118">Pour plus d’informations, [voir Gérer la protection basée sur le cloud.](/windows/security/threat-protection/microsoft-defender-antivirus/deploy-manage-report-microsoft-defender-antivirus)</span><span class="sxs-lookup"><span data-stu-id="94eb2-118">For more information, see [Manage cloud-based protection](/windows/security/threat-protection/microsoft-defender-antivirus/deploy-manage-report-microsoft-defender-antivirus).</span></span>
- <span data-ttu-id="94eb2-119">La version du client anti-programme malveillant doit être 4.18.1901.x ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="94eb2-119">The Antimalware client version must be  4.18.1901.x or later.</span></span>
- <span data-ttu-id="94eb2-120">Pris en charge sur les ordinateurs Windows 10, version 1703 ou ultérieure, Windows server 2016 et 2019.</span><span class="sxs-lookup"><span data-stu-id="94eb2-120">Supported on machines on Windows 10, version 1703 or later, Windows server 2016 and 2019.</span></span>
- <span data-ttu-id="94eb2-121">Les définitions de protection contre les virus et menaces doivent être à jour.</span><span class="sxs-lookup"><span data-stu-id="94eb2-121">The virus and threat protection definitions must be up to date.</span></span>
- <span data-ttu-id="94eb2-122">Cette fonctionnalité prend actuellement en charge l’entrée. CER ou . Extensions de fichier PEM.</span><span class="sxs-lookup"><span data-stu-id="94eb2-122">This feature currently supports entering .CER or .PEM file extensions.</span></span>

>[!IMPORTANT]
> - <span data-ttu-id="94eb2-123">Un certificat feuille valide est un certificat de signature qui possède un chemin de certification valide et doit être chaîné à l’autorité de certification racine (CA) approuvé par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="94eb2-123">A valid leaf certificate is a signing certificate that has a valid certification path and must be chained to the Root Certificate Authority (CA) trusted by Microsoft.</span></span>  <span data-ttu-id="94eb2-124">Sinon, un certificat personnalisé (auto-signé) peut être utilisé tant qu’il est approuvé par le client (le certificat de l’autorité de certification racine est installé sous l’ordinateur local « Autorités de certification racines de confiance »).</span><span class="sxs-lookup"><span data-stu-id="94eb2-124">Alternatively, a custom (self-signed) certificate can be used as long as it's trusted by the client (Root CA certificate is installed under the Local Machine 'Trusted Root Certification Authorities').</span></span>
>- <span data-ttu-id="94eb2-125">Les enfants ou le parent des IOC de certificats d’autorisation/de blocage ne sont pas inclus dans la fonctionnalité autoriser/bloquer les IoC, seuls les certificats feuille sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="94eb2-125">The children or parent of the allow/block certificate IOCs are not included in the allow/block IoC functionality, only leaf certificates are supported.</span></span>
>- <span data-ttu-id="94eb2-126">Les certificats signés par Microsoft ne peuvent pas être bloqués.</span><span class="sxs-lookup"><span data-stu-id="94eb2-126">Microsoft signed certificates cannot be blocked.</span></span>

#### <a name="create-an-indicator-for-certificates-from-the-settings-page"></a><span data-ttu-id="94eb2-127">Créez un indicateur pour les certificats à partir de la page paramètres :</span><span class="sxs-lookup"><span data-stu-id="94eb2-127">Create an indicator for certificates from the settings page:</span></span>

>[!IMPORTANT]
> <span data-ttu-id="94eb2-128">La création et la suppression d’un certificat IoC peuvent prendre jusqu’à 3 heures.</span><span class="sxs-lookup"><span data-stu-id="94eb2-128">It can take up to 3 hours to create and remove a certificate IoC.</span></span>

1. <span data-ttu-id="94eb2-129">Dans le volet de navigation, sélectionnez **Paramètres**  >  **indicateurs.**</span><span class="sxs-lookup"><span data-stu-id="94eb2-129">In the navigation pane, select **Settings** > **Indicators**.</span></span>  

2. <span data-ttu-id="94eb2-130">Sélectionnez **l’onglet** Certificat.</span><span class="sxs-lookup"><span data-stu-id="94eb2-130">Select the **Certificate** tab.</span></span>

3. <span data-ttu-id="94eb2-131">Sélectionnez **Ajouter un indicateur**.</span><span class="sxs-lookup"><span data-stu-id="94eb2-131">Select **Add indicator**.</span></span>

4. <span data-ttu-id="94eb2-132">Spécifiez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="94eb2-132">Specify the following details:</span></span>
   - <span data-ttu-id="94eb2-133">Indicateur : spécifiez les détails de l’entité et définissez l’expiration de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="94eb2-133">Indicator - Specify the entity details and define the expiration of the indicator.</span></span>
   - <span data-ttu-id="94eb2-134">Action : spécifiez l’action à prendre et fournissez une description.</span><span class="sxs-lookup"><span data-stu-id="94eb2-134">Action - Specify the action to be taken and provide a description.</span></span>
   - <span data-ttu-id="94eb2-135">Étendue : définir l’étendue du groupe d’ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="94eb2-135">Scope - Define the scope of the machine group.</span></span>

5. <span data-ttu-id="94eb2-136">Consultez les détails de l’onglet Résumé, puis cliquez sur **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="94eb2-136">Review the details in the Summary tab, then click **Save**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94eb2-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94eb2-137">Related topics</span></span>
- [<span data-ttu-id="94eb2-138">Créer des indicateurs</span><span class="sxs-lookup"><span data-stu-id="94eb2-138">Create indicators</span></span>](manage-indicators.md)
- [<span data-ttu-id="94eb2-139">Créer des indicateurs pour les fichiers</span><span class="sxs-lookup"><span data-stu-id="94eb2-139">Create indicators for files</span></span>](indicator-file.md)
- [<span data-ttu-id="94eb2-140">Créer des indicateurs pour les IP et URL/domaines</span><span class="sxs-lookup"><span data-stu-id="94eb2-140">Create indicators for IPs and URLs/domains</span></span>](indicator-ip-domain.md)
- [<span data-ttu-id="94eb2-141">Gérer des indicateurs</span><span class="sxs-lookup"><span data-stu-id="94eb2-141">Manage indicators</span></span>](indicator-manage.md)
