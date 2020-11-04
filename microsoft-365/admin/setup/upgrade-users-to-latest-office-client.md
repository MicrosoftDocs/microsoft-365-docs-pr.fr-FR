---
title: Mettre à niveau votre Office 2010 vers Microsoft 365-Microsoft 365 admin
f1.keywords:
- NOCSH
ms.author: kwekua
author: kwekuako
manager: scotv
audience: Admin
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- Adm_TOC
search.appverid:
- BCS160
- MET150
- MOE150
ms.custom:
- fwlink 824861; CampaignID
- O365_Comm_SR_UpgradeOffice
- seo-marvel-may2020
- fwlink 824861; CampaignID O365_Comm_SR_UpgradeOffice
- AdminSurgePortfolio
ms.assetid: f6b00895-b5fd-4af6-a656-b7788ea20cbb
description: Découvrez comment mettre à niveau Microsoft Office vers le dernier client Office pour les utilisateurs de votre organisation.
ms.openlocfilehash: 596dfc8f4a005d01c0bf330243bf1fb3c639f97e
ms.sourcegitcommit: 7355cc8871cde5fac6d7d6dcecc3e41e35601623
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "48906440"
---
# <a name="upgrade-your-microsoft-365-for-business-users-to-the-latest-office-client"></a><span data-ttu-id="caf01-103">Mettre à niveau vos utilisateurs Microsoft 365 vers le dernier client Office</span><span class="sxs-lookup"><span data-stu-id="caf01-103">Upgrade your Microsoft 365 for business users to the latest Office client</span></span>

## <a name="office-2010-reaches-end-of-support"></a><span data-ttu-id="caf01-104">Office 2010 atteint la fin de l’assistance</span><span class="sxs-lookup"><span data-stu-id="caf01-104">Office 2010 reaches end-of-support</span></span>

<span data-ttu-id="caf01-105">Office 2010 a atteint sa fin d’assistance le 13 octobre 2020.</span><span class="sxs-lookup"><span data-stu-id="caf01-105">Office 2010 reached its end of support on October 13, 2020.</span></span> <span data-ttu-id="caf01-106">Microsoft ne fournit plus les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="caf01-106">Microsoft will no longer provide the following:</span></span>

- <span data-ttu-id="caf01-107">Support technique pour les problèmes</span><span class="sxs-lookup"><span data-stu-id="caf01-107">Technical support for issues</span></span>

- <span data-ttu-id="caf01-108">Correctifs de bogues pour les problèmes découverts</span><span class="sxs-lookup"><span data-stu-id="caf01-108">Bug fixes for issues that are discovered</span></span>

- <span data-ttu-id="caf01-109">Correctifs de sécurité pour les vulnérabilités découvertes</span><span class="sxs-lookup"><span data-stu-id="caf01-109">Security fixes for vulnerabilities that are discovered</span></span>

<span data-ttu-id="caf01-110">Pour plus d’informations, voir la feuille [de route de fin d’assistance pour Office 2010](https://docs.microsoft.com/deployoffice/endofsupport/office-2010-end-support-roadmap) .</span><span class="sxs-lookup"><span data-stu-id="caf01-110">See [Office 2010 end of support roadmap](https://docs.microsoft.com/deployoffice/endofsupport/office-2010-end-support-roadmap) for more information.</span></span>

 <span data-ttu-id="caf01-111">**Est-ce la bonne rubrique pour vous ?**</span><span class="sxs-lookup"><span data-stu-id="caf01-111">**Is this the right topic for you?**</span></span>
  
 <span data-ttu-id="caf01-112">Si vous êtes l’administrateur responsable de l’abonnement Microsoft 365 pour les entreprises au sein de votre organisation, vous êtes au bon endroit.</span><span class="sxs-lookup"><span data-stu-id="caf01-112">If you're the admin responsible for the Microsoft 365 for business subscription in your organization, you're in the right place.</span></span> <span data-ttu-id="caf01-113">Les administrateurs sont généralement responsables des tâches telles que la gestion des utilisateurs, la réinitialisation des mots de passe, la gestion des installations d’Office et l’ajout ou la suppression de licences.</span><span class="sxs-lookup"><span data-stu-id="caf01-113">Admins are typically responsible for tasks like managing users, resetting passwords, managing Office installs and adding or removing licenses.</span></span>

 <span data-ttu-id="caf01-114">Si vous n’êtes pas un administrateur et que vous disposez d’un produit de la [famille Microsoft 365](https://support.microsoft.com/office/28cbc8cf-1332-4f04-9123-9b660abb629e#BKMK_OfficePlans) , consultez [la rubrique Comment mettre à niveau Office](https://support.microsoft.com/office/ee68f6cf-422f-464a-82ec-385f65391350) pour obtenir des informations sur la mise à niveau de votre ancienne version d’Office.</span><span class="sxs-lookup"><span data-stu-id="caf01-114">If you're not an admin and you have a [Microsoft 365 Family](https://support.microsoft.com/office/28cbc8cf-1332-4f04-9123-9b660abb629e#BKMK_OfficePlans) product, see [How do I upgrade Office](https://support.microsoft.com/office/ee68f6cf-422f-464a-82ec-385f65391350) for information about upgrading your older, home use version of Office.</span></span>

## <a name="get-ready-to-upgrade-to-microsoft-365"></a><span data-ttu-id="caf01-115">Préparer la mise à niveau vers Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="caf01-115">Get ready to upgrade to Microsoft 365</span></span>

<span data-ttu-id="caf01-116">En tant qu’administrateur, vous contrôlez la version des personnes Office de votre organisation pouvant être installées.</span><span class="sxs-lookup"><span data-stu-id="caf01-116">As an admin, you control what version of Office people in your organization can install.</span></span> <span data-ttu-id="caf01-117">Nous vous recommandons vivement d’aider les utilisateurs de votre organisation qui exécutent des versions antérieures d’Office, comme Office 2010, Office 2013 ou Office 2016 à effectuer une mise à niveau vers la dernière version, afin de tirer parti de ses améliorations en matière de sécurité et de productivité.</span><span class="sxs-lookup"><span data-stu-id="caf01-117">We highly recommend that you help users in your organization running older versions of Office such as Office 2010, Office 2013, or Office 2016 upgrade to the latest version to take advantage of its security and productivity improvements.</span></span>

## <a name="upgrade-steps"></a><span data-ttu-id="caf01-118">Étapes de mise à niveau</span><span class="sxs-lookup"><span data-stu-id="caf01-118">Upgrade steps</span></span>

<span data-ttu-id="caf01-119">Les étapes ci-dessous vous guideront tout au long du processus de mise à niveau de vos utilisateurs vers le dernier client de bureau Office.</span><span class="sxs-lookup"><span data-stu-id="caf01-119">The steps below will guide you through the process of upgrading your users to the latest Office desktop client.</span></span> <span data-ttu-id="caf01-120">Nous vous recommandons de lire ces étapes avant de commencer le processus de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="caf01-120">We recommend you read through these steps before beginning the upgrade process.</span></span>
  
## <a name="step-1---check-system-requirements"></a><span data-ttu-id="caf01-121">Étape 1 : vérifier la configuration système requise</span><span class="sxs-lookup"><span data-stu-id="caf01-121">Step 1 - Check system requirements</span></span>

<span data-ttu-id="caf01-122">[Vérifiez la configuration système requise](https://www.microsoft.com/microsoft-365/microsoft-365-and-office-resources) pour Office afin de vous assurer que vos appareils sont compatibles avec la dernière version d’Office.</span><span class="sxs-lookup"><span data-stu-id="caf01-122">[Check the system requirements](https://www.microsoft.com/microsoft-365/microsoft-365-and-office-resources) for Office to make sure your devices are compatible with the latest version of Office.</span></span> <span data-ttu-id="caf01-123">Par exemple, les versions plus récentes d’Office ne peuvent pas être installées sur des ordinateurs exécutant Windows XP ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="caf01-123">For example, newer versions of Office can't be installed on computers running Windows XP or Windows Vista.</span></span>
  
> [!TIP]
> <span data-ttu-id="caf01-124">Si des utilisateurs de votre organisation exécutent des versions antérieures de Windows sur leurs PC ou ordinateurs portables, nous vous recommandons d’effectuer une mise à niveau vers Windows 10.</span><span class="sxs-lookup"><span data-stu-id="caf01-124">If you have users in your organization running older versions of Windows on their PCs or laptops, we recommend upgrading to Windows 10.</span></span> <span data-ttu-id="caf01-125">Windows 7 a atteint la fin de la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="caf01-125">Windows 7 has reached end of support.</span></span> <span data-ttu-id="caf01-126">La [prise en charge de Windows 7 se termine au 1er janvier 2020](https://www.microsoft.com/microsoft-365/windows/end-of-windows-7-support?rtc=1) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="caf01-126">Read [Support for Windows 7 ends in January 2020](https://www.microsoft.com/microsoft-365/windows/end-of-windows-7-support?rtc=1) for more info.</span></span>

<span data-ttu-id="caf01-127">Consultez la [Configuration requise pour Windows 10](https://www.microsoft.com/windows/windows-10-specifications) pour savoir si vous pouvez mettre à niveau les systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="caf01-127">Check out the [Windows 10 system requirements](https://www.microsoft.com/windows/windows-10-specifications) to see if you can upgrade their operating systems.</span></span>

### <a name="check-application-compatibility"></a><span data-ttu-id="caf01-128">Vérifier la compatibilité des applications</span><span class="sxs-lookup"><span data-stu-id="caf01-128">Check application compatibility</span></span>

<span data-ttu-id="caf01-129">Pour garantir la réussite de la mise à niveau, nous vous recommandons d’identifier vos applications Office, y compris les scripts VBA, les macros, les compléments tiers et les documents et feuilles de calcul complexes, et d’évaluer leur compatibilité avec la dernière version d’Office.</span><span class="sxs-lookup"><span data-stu-id="caf01-129">To ensure a successful upgrade, we recommend identifying your Office applications--including VBA scripts, macros, third-party add-ins, and complex documents and spreadsheets--and assessing their compatibility with the latest version of Office.</span></span>
  
<span data-ttu-id="caf01-130">Par exemple, si vous utilisez des compléments tiers avec votre installation d’Office actuelle, contactez le fabricant afin de vous assurer qu’ils sont compatibles avec la dernière version d’Office.</span><span class="sxs-lookup"><span data-stu-id="caf01-130">For example, if you're using third-party add-ins with your current Office install, contact the manufacture to make sure they're compatible with the latest version of Office.</span></span>
  
## <a name="step-2---check-your-existing-subscription-plan"></a><span data-ttu-id="caf01-131">Étape 2 : vérifier votre plan d’abonnement existant</span><span class="sxs-lookup"><span data-stu-id="caf01-131">Step 2 - Check your existing subscription plan</span></span>

<span data-ttu-id="caf01-132">Certains plans Microsoft 365 n’incluent pas les versions de bureau complètes d’Office et les étapes de mise à niveau sont différentes si votre plan n’inclut pas Office.</span><span class="sxs-lookup"><span data-stu-id="caf01-132">Some Microsoft 365 plans don't include the full desktop versions of Office and the steps to upgrade are different if your plan doesn't include Office.</span></span>
  
<span data-ttu-id="caf01-133">Vous ne savez pas quel plan d’abonnement vous avez ?</span><span class="sxs-lookup"><span data-stu-id="caf01-133">Not sure which subscription plan you have?</span></span> <span data-ttu-id="caf01-134">Consultez la rubrique [relative à l’abonnement Microsoft 365 pour les entreprises](../admin-overview/what-subscription-do-i-have.md) .</span><span class="sxs-lookup"><span data-stu-id="caf01-134">See [What Microsoft 365 for business subscription do I have?](../admin-overview/what-subscription-do-i-have.md)</span></span>
  
<span data-ttu-id="caf01-135">Si votre offre existante inclut Office, passez à l' [étape 3 : désinstaller Office](#step-3---uninstall-office).</span><span class="sxs-lookup"><span data-stu-id="caf01-135">If your existing plan includes Office, move on to [Step 3 - Uninstall Office](#step-3---uninstall-office).</span></span>
  
<span data-ttu-id="caf01-136">Si votre offre existante n’inclut pas Office, sélectionnez l’une des options ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="caf01-136">If your existing plan doesn't include Office, then select from the options below:</span></span>
  
### <a name="upgrade-options-for-plans-that-dont-include-office"></a><span data-ttu-id="caf01-137">Options de mise à niveau pour les plans qui n’incluent pas Office</span><span class="sxs-lookup"><span data-stu-id="caf01-137">Upgrade options for plans that don't include Office</span></span>

 <span data-ttu-id="caf01-138">**Option 1 : modifier les abonnements Office**</span><span class="sxs-lookup"><span data-stu-id="caf01-138">**Option 1: Switch Office subscriptions**</span></span>

<span data-ttu-id="caf01-139">Basculer vers un abonnement qui inclut Office.</span><span class="sxs-lookup"><span data-stu-id="caf01-139">Switch to a subscription that includes Office.</span></span> <span data-ttu-id="caf01-140">Voir [basculer vers une autre offre Microsoft 365 for Business](../../commerce/subscriptions/switch-to-a-different-plan.md).</span><span class="sxs-lookup"><span data-stu-id="caf01-140">See [Switch to a different Microsoft 365 for business plan](../../commerce/subscriptions/switch-to-a-different-plan.md).</span></span>

<span data-ttu-id="caf01-141">**Option 2 : acheter des achats individuels d’Office, ou acheter Office par le biais d’une licence en volume**</span><span class="sxs-lookup"><span data-stu-id="caf01-141">**Option 2: Buy individual, one-time purchases of Office, or buy Office through a volume license**</span></span>

 - <span data-ttu-id="caf01-142">Acheter un seul achat d’Office.</span><span class="sxs-lookup"><span data-stu-id="caf01-142">Buy an individual, one-time purchase of Office.</span></span> <span data-ttu-id="caf01-143">Voir [Office famille &amp; ](https://products.office.com/home-and-business) ou [Office Professionnel](https://products.office.com/professional)</span><span class="sxs-lookup"><span data-stu-id="caf01-143">See [Office Home &amp; Business](https://products.office.com/home-and-business) or [Office Professional](https://products.office.com/professional)</span></span>

     <span data-ttu-id="caf01-144">OR</span><span class="sxs-lookup"><span data-stu-id="caf01-144">OR</span></span>

 - <span data-ttu-id="caf01-145">Acheter plusieurs copies d’Office par le biais d’une licence en volume.</span><span class="sxs-lookup"><span data-stu-id="caf01-145">Buy multiple copies of Office through a volume license.</span></span> <span data-ttu-id="caf01-146">Consultez la rubrique [comparer les suites disponibles via le gestionnaire de licences en volume](https://products.office.com/business/microsoft-office-volume-licensing-suites-comparison).</span><span class="sxs-lookup"><span data-stu-id="caf01-146">See, [Compare suites available through volume licensing](https://products.office.com/business/microsoft-office-volume-licensing-suites-comparison).</span></span>

## <a name="step-3---uninstall-office"></a><span data-ttu-id="caf01-147">Étape 3 : désinstaller Office</span><span class="sxs-lookup"><span data-stu-id="caf01-147">Step 3 - Uninstall Office</span></span>

<span data-ttu-id="caf01-148">Avant d’installer la dernière version d’Office, nous vous recommandons de désinstaller toutes les versions antérieures d’Office.</span><span class="sxs-lookup"><span data-stu-id="caf01-148">Before installing the latest version of Office, we recommend you uninstall all older versions of Office.</span></span> <span data-ttu-id="caf01-149">Toutefois, si vous changez d’avis sur la mise à niveau d’Office, notez les instances suivantes où vous ne pourrez pas réinstaller Office après l’avoir désinstallé.</span><span class="sxs-lookup"><span data-stu-id="caf01-149">However, if you change your mind about upgrading Office, note the following instances where you won't be able to reinstall Office after uninstalling it.</span></span>
  
<span data-ttu-id="caf01-150">Nous vous recommandons d’utiliser des compléments tiers, de contacter le fabricant pour voir s’il existe une mise à jour qui fonctionnera avec la dernière version d’Office.</span><span class="sxs-lookup"><span data-stu-id="caf01-150">We recommend if you have third-party add-ins, contact the manufacturer to see if there's an update that will work with the latest version of Office.</span></span>

### <a name="select-the-version-of-office-you-want-to-uninstall"></a><span data-ttu-id="caf01-151">Sélectionnez la version d’Office que vous souhaitez désinstaller</span><span class="sxs-lookup"><span data-stu-id="caf01-151">Select the version of Office you want to uninstall</span></span>

- [<span data-ttu-id="caf01-152">À partir d’un PC</span><span class="sxs-lookup"><span data-stu-id="caf01-152">From a PC</span></span>](https://support.microsoft.com/office/9dd49b83-264a-477a-8fcc-2fdf5dbf61d8)

- [<span data-ttu-id="caf01-153">À partir d’un Mac</span><span class="sxs-lookup"><span data-stu-id="caf01-153">From a Mac</span></span>](https://support.microsoft.com/office/eefa1199-5b58-43af-8a3d-b73dc1a8cae3)
  
### <a name="known-issues-trying-to-reinstall-older-versions-of-office-after-an-uninstall"></a><span data-ttu-id="caf01-154">Problèmes connus lors de la tentative de réinstallation d’anciennes versions d’Office après une désinstallation</span><span class="sxs-lookup"><span data-stu-id="caf01-154">Known issues trying to reinstall older versions of Office after an uninstall</span></span>

 <span data-ttu-id="caf01-155">**Office via une licence en volume** Si vous n’avez plus accès aux fichiers sources de ces versions de licence en volume d’Office, vous ne pourrez pas le réinstaller.</span><span class="sxs-lookup"><span data-stu-id="caf01-155">**Office through a volume license** If you no longer have access to the source files of these volume license versions of Office, you won't be able to reinstall it.</span></span>

 <span data-ttu-id="caf01-156">**Office préinstallé sur votre ordinateur** Si vous n’avez plus de disque ni de clé de produit (si Office est fourni avec un), vous ne pourrez pas le réinstaller.</span><span class="sxs-lookup"><span data-stu-id="caf01-156">**Office pre-installed on your computer** If you no longer have a disc or product key (if Office came with one) you won't be able to reinstall it.</span></span>

 <span data-ttu-id="caf01-157">**Abonnements non pris en charge** Si votre copie d’Office a été obtenue via des abonnements abandonnés, tels qu’Office 365 Small Business Premium ou Office 365 Mid-Size Business, vous ne pourrez pas installer une version antérieure d’Office, sauf si vous disposez de la clé de produit fournie avec votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="caf01-157">**Non-supported subscriptions** If your copy of Office was obtained through discontinued subscriptions, such as Office 365 Small Business Premium or Office 365 Mid-size Business, you won't be able to install an older version of Office unless you have the product key that came with your subscription.</span></span>

<span data-ttu-id="caf01-158">Si vous préférez installer votre ancienne version d’Office avec la dernière version, vous pouvez consulter la liste des versions dans lesquelles cette version est prise en charge dans, [installer et utiliser différentes versions d’Office sur le même PC](https://support.microsoft.com/office/6ebb44ce-18a3-43f9-a187-b78c513788bf).</span><span class="sxs-lookup"><span data-stu-id="caf01-158">If you'd prefer to install your older version of Office side-by-side with the latest version, you can see a list of versions where this is supported in, [Install and use different versions of Office on the same PC](https://support.microsoft.com/office/6ebb44ce-18a3-43f9-a187-b78c513788bf).</span></span> <span data-ttu-id="caf01-159">Une installation côte à côte peut être le bon choix pour vous, si, par exemple, vous avez installé des compléments tiers que vous utilisez avec votre ancienne version d’Office et que vous n’êtes pas encore sûr qu’ils sont compatibles avec la dernière version.</span><span class="sxs-lookup"><span data-stu-id="caf01-159">A side-by-side installation might be the right choice for you, if for example, you've installed third-party add-ins you're using with your older version of Office and you're not yet sure they're compatible with the latest version.</span></span>

## <a name="step-4---assign-office-licenses-to-users"></a><span data-ttu-id="caf01-160">Étape 4 : attribuer des licences Office à des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="caf01-160">Step 4 - Assign Office licenses to users</span></span>

<span data-ttu-id="caf01-161">Si vous ne l’avez pas encore fait, attribuez des licences aux utilisateurs de votre organisation qui ont besoin d’installer Office, reportez-vous à [attribuer des licences aux utilisateurs dans Microsoft 365 pour les entreprises](../manage/assign-licenses-to-users.md).</span><span class="sxs-lookup"><span data-stu-id="caf01-161">If you haven't already done so, assign licenses to any users in your organization who need to install Office, see [Assign licenses to users in Microsoft 365 for business](../manage/assign-licenses-to-users.md).</span></span>
  
## <a name="step-5---install-office"></a><span data-ttu-id="caf01-162">Étape 5 : installer Office</span><span class="sxs-lookup"><span data-stu-id="caf01-162">Step 5 - Install Office</span></span>

<span data-ttu-id="caf01-163">Une fois que vous avez vérifié les utilisateurs que vous souhaitez mettre à niveau, la dernière étape consiste à installer Office, voir [Télécharger et installer ou réinstaller Office sur votre PC ou Mac](https://support.microsoft.com/office/4414eaaf-0478-48be-9c42-23adc4716658).</span><span class="sxs-lookup"><span data-stu-id="caf01-163">After you've verified the users you want to upgrade all have licenses, the final step is to have them install Office, see [Download and install or reinstall Office on your PC or Mac](https://support.microsoft.com/office/4414eaaf-0478-48be-9c42-23adc4716658).</span></span>
  
> [!TIP]
> <span data-ttu-id="caf01-164">Si vous ne souhaitez pas que vos utilisateurs installent Office eux-mêmes, consultez la rubrique [gérer les paramètres de téléchargement de logiciels dans office 365](https://docs.microsoft.com/DeployOffice/manage-software-download-settings-office-365).</span><span class="sxs-lookup"><span data-stu-id="caf01-164">If you don't want your users installing Office themselves, see [Manage software download settings in Office 365](https://docs.microsoft.com/DeployOffice/manage-software-download-settings-office-365).</span></span> <span data-ttu-id="caf01-165">Vous pouvez utiliser l' [outil déploiement d’Office](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool) pour télécharger le logiciel Office sur votre réseau local, puis déployer Office à l’aide de la méthode de déploiement de logiciels que vous utilisez généralement.</span><span class="sxs-lookup"><span data-stu-id="caf01-165">You can use the [Office Deployment Tool](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool) to download the Office software to your local network and then deploy Office by using the software deployment method you typically use.</span></span>
