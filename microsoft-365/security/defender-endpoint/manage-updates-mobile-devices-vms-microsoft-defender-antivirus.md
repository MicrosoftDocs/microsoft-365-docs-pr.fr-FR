---
title: Définir la façon dont les appareils mobiles sont mis à jour par l'Antivirus Microsoft Defender
description: Gérer la façon dont les appareils mobiles, tels que les ordinateurs portables, doivent être mis à jour avec les mises à jour de la protection antivirus Microsoft Defender.
keywords: mises à jour, protection, planification des mises à jour, batterie, appareil mobile, ordinateur portable, bloc-notes, opt-in, microsoft update, wsus, override
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
ms.localizationpriority: medium
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: f67330e1ccd7361c3982b76a6ab8754db23bd110
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51690394"
---
# <a name="manage-updates-for-mobile-devices-and-virtual-machines-vms"></a><span data-ttu-id="b3f6d-104">Gérer les mises à jour pour les périphériques mobiles et les machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="b3f6d-104">Manage updates for mobile devices and virtual machines (VMs)</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="b3f6d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b3f6d-105">**Applies to:**</span></span>

- [<span data-ttu-id="b3f6d-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b3f6d-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="b3f6d-107">Les appareils mobiles et les ordinateurs VM peuvent nécessiter une configuration plus importante pour s'assurer que les mises à jour n'ont pas d'impact sur les performances.</span><span class="sxs-lookup"><span data-stu-id="b3f6d-107">Mobile devices and VMs may require more configuration to ensure performance is not impacted by updates.</span></span>

<span data-ttu-id="b3f6d-108">Deux paramètres sont utiles pour ces appareils :</span><span class="sxs-lookup"><span data-stu-id="b3f6d-108">There are two settings that are useful for these devices:</span></span>

- <span data-ttu-id="b3f6d-109">Opter pour Microsoft Update sur des ordinateurs mobiles sans connexion WSUS</span><span class="sxs-lookup"><span data-stu-id="b3f6d-109">Opt in to Microsoft Update on mobile computers without a WSUS connection</span></span>
- <span data-ttu-id="b3f6d-110">Empêcher les mises à jour des informations de sécurité lors de l'exécution sur batterie</span><span class="sxs-lookup"><span data-stu-id="b3f6d-110">Prevent Security intelligence updates when running on battery power</span></span>

<span data-ttu-id="b3f6d-111">Les articles suivants peuvent également être utiles dans les situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b3f6d-111">The following articles may also be useful in these situations:</span></span>
- [<span data-ttu-id="b3f6d-112">Configuration des analyses de rattrapage et de planification</span><span class="sxs-lookup"><span data-stu-id="b3f6d-112">Configuring scheduled and catch-up scans</span></span>](scheduled-catch-up-scans-microsoft-defender-antivirus.md)
- [<span data-ttu-id="b3f6d-113">Gérer les mises à jour des points de terminaison qui ne sont plus à jour</span><span class="sxs-lookup"><span data-stu-id="b3f6d-113">Manage updates for endpoints that are out of date</span></span>](manage-outdated-endpoints-microsoft-defender-antivirus.md)
- [<span data-ttu-id="b3f6d-114">Guide de déploiement de l'Antivirus Microsoft Defender dans un environnement d'infrastructure de bureau virtuel (VDI)</span><span class="sxs-lookup"><span data-stu-id="b3f6d-114">Deployment guide for Microsoft Defender Antivirus in a virtual desktop infrastructure (VDI) environment</span></span>](deployment-vdi-microsoft-defender-antivirus.md)

## <a name="opt-in-to-microsoft-update-on-mobile-computers-without-a-wsus-connection"></a><span data-ttu-id="b3f6d-115">Opter pour Microsoft Update sur des ordinateurs mobiles sans connexion WSUS</span><span class="sxs-lookup"><span data-stu-id="b3f6d-115">Opt in to Microsoft Update on mobile computers without a WSUS connection</span></span>

<span data-ttu-id="b3f6d-116">Vous pouvez utiliser Microsoft Update pour maintenir à jour les informations de sécurité sur les appareils mobiles exécutant l'Antivirus Microsoft Defender lorsqu'ils ne sont pas connectés au réseau d'entreprise ou n'ont pas de connexion WSUS.</span><span class="sxs-lookup"><span data-stu-id="b3f6d-116">You can use Microsoft Update to keep Security intelligence on mobile devices running Microsoft Defender Antivirus up to date when they are not connected to the corporate network or don't otherwise have a WSUS connection.</span></span> 

<span data-ttu-id="b3f6d-117">Cela signifie que les mises à jour de protection peuvent être livrées aux appareils (via Microsoft Update) même si vous avez définie WSUS pour remplacer Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="b3f6d-117">This means that protection updates can be delivered to devices (via Microsoft Update) even if you have set WSUS to override Microsoft Update.</span></span>

<span data-ttu-id="b3f6d-118">Vous pouvez choisir Microsoft Update sur l'appareil mobile de l'une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="b3f6d-118">You can opt in to Microsoft Update on the mobile device in one of the following ways:</span></span>

- <span data-ttu-id="b3f6d-119">Modifiez le paramètre avec la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b3f6d-119">Change the setting with Group Policy.</span></span>
- <span data-ttu-id="b3f6d-120">Utilisez un script VBScript pour créer un script, puis exécutez-le sur chaque ordinateur de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="b3f6d-120">Use a VBScript to create a script, then run it on each computer in your network.</span></span>
- <span data-ttu-id="b3f6d-121">Choisissez manuellement chaque ordinateur de votre réseau via le menu **Paramètres.**</span><span class="sxs-lookup"><span data-stu-id="b3f6d-121">Manually opt in every computer on your network through the **Settings** menu.</span></span>

### <a name="use-group-policy-to-opt-in-to-microsoft-update"></a><span data-ttu-id="b3f6d-122">Utiliser la stratégie de groupe pour opter pour Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="b3f6d-122">Use Group Policy to opt in to Microsoft Update</span></span>

1. <span data-ttu-id="b3f6d-123">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l'objet de stratégie de groupe que vous souhaitez configurer et sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="b3f6d-123">On your Group Policy management machine, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and select **Edit**.</span></span>

2. <span data-ttu-id="b3f6d-124">Dans **l'Éditeur de gestion des stratégies de** groupe, allez à **Configuration ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="b3f6d-124">In the **Group Policy Management Editor** go to **Computer configuration**.</span></span>

3. <span data-ttu-id="b3f6d-125">Sélectionnez **stratégies** **puis modèles d'administration.**</span><span class="sxs-lookup"><span data-stu-id="b3f6d-125">Select **Policies** then **Administrative templates**.</span></span>

4. <span data-ttu-id="b3f6d-126">Développez l'arborescence **des composants Windows**  >  **Microsoft Defender Antivirus** Signature  >  **Updates**.</span><span class="sxs-lookup"><span data-stu-id="b3f6d-126">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > **Signature Updates**.</span></span>

5. <span data-ttu-id="b3f6d-127">Définissez **Autoriser les mises à** jour des informations de sécurité de Microsoft Update sur **Activé,** puis sélectionnez **OK.**</span><span class="sxs-lookup"><span data-stu-id="b3f6d-127">Set **Allow security intelligence updates from Microsoft Update** to **Enabled**, and then select  **OK**.</span></span>


### <a name="use-a-vbscript-to-opt-in-to-microsoft-update"></a><span data-ttu-id="b3f6d-128">Utiliser un VBScript pour opter pour Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="b3f6d-128">Use a VBScript to opt in to Microsoft Update</span></span>

1. <span data-ttu-id="b3f6d-129">Utilisez les instructions de l'article MSDN [Opt-In to Microsoft Update](/windows/win32/wua_sdk/opt-in-to-microsoft-update) pour créer le VBScript.</span><span class="sxs-lookup"><span data-stu-id="b3f6d-129">Use the instructions in the MSDN article [Opt-In to Microsoft Update](/windows/win32/wua_sdk/opt-in-to-microsoft-update) to create the VBScript.</span></span>

2. <span data-ttu-id="b3f6d-130">Exécutez le script VBScript que vous avez créé sur chaque ordinateur de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="b3f6d-130">Run the VBScript you created on each computer in your network.</span></span>

### <a name="manually-opt-in-to-microsoft-update"></a><span data-ttu-id="b3f6d-131">Opter manuellement pour Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="b3f6d-131">Manually opt in to Microsoft Update</span></span>

1. <span data-ttu-id="b3f6d-132">Ouvrez **Windows Update** dans Update **& paramètres** de sécurité sur l'ordinateur que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="b3f6d-132">Open **Windows Update** in **Update & security** settings on the computer you want to opt in.</span></span>

2. <span data-ttu-id="b3f6d-133">Sélectionnez **Options avancées.**</span><span class="sxs-lookup"><span data-stu-id="b3f6d-133">Select **Advanced** options.</span></span>

3. <span data-ttu-id="b3f6d-134">Cochez la case pour me fournir les mises à jour d'autres produits **Microsoft lorsque je met à jour Windows.**</span><span class="sxs-lookup"><span data-stu-id="b3f6d-134">Select the checkbox for **Give me updates for other Microsoft products when I update Windows**.</span></span>

## <a name="prevent-security-intelligence-updates-when-running-on-battery-power"></a><span data-ttu-id="b3f6d-135">Empêcher les mises à jour des informations de sécurité lors de l'exécution sur batterie</span><span class="sxs-lookup"><span data-stu-id="b3f6d-135">Prevent Security intelligence updates when running on battery power</span></span>

<span data-ttu-id="b3f6d-136">Vous pouvez configurer l'Antivirus Microsoft Defender pour télécharger les mises à jour de protection uniquement lorsque le PC est connecté à une source d'alimentation câblé.</span><span class="sxs-lookup"><span data-stu-id="b3f6d-136">You can configure Microsoft Defender Antivirus to only download protection updates when the PC is connected to a wired power source.</span></span> 

### <a name="use-group-policy-to-prevent-security-intelligence-updates-on-battery-power"></a><span data-ttu-id="b3f6d-137">Utiliser une stratégie de groupe pour empêcher les mises à jour des informations de sécurité sur l'alimentation de la batterie</span><span class="sxs-lookup"><span data-stu-id="b3f6d-137">Use Group Policy to prevent security intelligence updates on battery power</span></span>

1.  <span data-ttu-id="b3f6d-138">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, choisissez l'objet de stratégie de groupe que vous souhaitez configurer et ouvrez-le pour modification.</span><span class="sxs-lookup"><span data-stu-id="b3f6d-138">On your Group Policy management machine, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), choose the Group Policy Object you want to configure, and open it for editing.</span></span>

2.  <span data-ttu-id="b3f6d-139">Dans **l'Éditeur de gestion des stratégies de** groupe, allez à **Configuration ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="b3f6d-139">In the **Group Policy Management Editor** go to **Computer configuration**.</span></span>

3.  <span data-ttu-id="b3f6d-140">Sélectionnez **stratégies** **puis modèles d'administration.**</span><span class="sxs-lookup"><span data-stu-id="b3f6d-140">Select **Policies** then **Administrative templates**.</span></span>

4.  <span data-ttu-id="b3f6d-141">Développez l'arborescence des **composants Windows** Mises à jour des signatures de l'antivirus  >  **Microsoft Defender,** puis définissez Autoriser les mises à jour de  >   **l'intelligence** de sécurité lorsque vous exécutez sur batterie sur **Désactivé.**</span><span class="sxs-lookup"><span data-stu-id="b3f6d-141">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > **Signature Updates**, and then set **Allow security intelligence updates when running on battery power** to **Disabled**.</span></span> <span data-ttu-id="b3f6d-142">Puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="b3f6d-142">Then select **OK**.</span></span> 

<span data-ttu-id="b3f6d-143">Cette action empêche le téléchargement des mises à jour de protection lorsque le PC est sur batterie.</span><span class="sxs-lookup"><span data-stu-id="b3f6d-143">This action prevents protection updates from downloading when the PC is on battery power.</span></span>

## <a name="related-articles"></a><span data-ttu-id="b3f6d-144">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="b3f6d-144">Related articles</span></span>

- [<span data-ttu-id="b3f6d-145">Gérer les mises à jour de l'Antivirus Microsoft Defender et appliquer les lignes de base</span><span class="sxs-lookup"><span data-stu-id="b3f6d-145">Manage Microsoft Defender Antivirus updates and apply baselines</span></span>](manage-updates-baselines-microsoft-defender-antivirus.md)
- [<span data-ttu-id="b3f6d-146">Mettre à jour et gérer l'Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="b3f6d-146">Update and manage Microsoft Defender Antivirus in Windows 10</span></span>](deploy-manage-report-microsoft-defender-antivirus.md)