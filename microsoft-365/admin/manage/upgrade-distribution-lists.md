---
title: Mettre à niveau les listes de distribution Microsoft 365 groupes dans Outlook
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
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 787d7a75-e201-46f3-a242-f698162ff09f
description: Découvrez comment mettre à niveau une ou plusieurs listes de distribution vers Microsoft 365 Groupes dans Outlook et comment utiliser PowerShell pour mettre à niveau plusieurs listes de distribution simultanément.
ms.openlocfilehash: d4686e7f2ec305194130b60fbacab24c9cf7f4e9
ms.sourcegitcommit: 4bcac4cb4f9399ebbd7c8cff0abb4d6ecedb731e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2021
ms.locfileid: "52698939"
---
# <a name="upgrade-distribution-lists-to-microsoft-365-groups-in-outlook"></a><span data-ttu-id="4750e-103">Mettre à niveau les listes de distribution Microsoft 365 groupes dans Outlook</span><span class="sxs-lookup"><span data-stu-id="4750e-103">Upgrade distribution lists to Microsoft 365 Groups in Outlook</span></span>

<span data-ttu-id="4750e-104">Vous pouvez mettre à niveau les listes de distribution Microsoft 365 groupes Outlook.</span><span class="sxs-lookup"><span data-stu-id="4750e-104">You can upgrade distribution lists to Microsoft 365 Groups in Outlook.</span></span> <span data-ttu-id="4750e-105">Il s’agit d’un excellent moyen de fournir aux listes de distribution de votre organisation toutes les fonctionnalités et fonctionnalités de Microsoft 365 groupes.</span><span class="sxs-lookup"><span data-stu-id="4750e-105">This is a great way to give your organization's distribution lists all the features and functionality of Microsoft 365 Groups.</span></span> [<span data-ttu-id="4750e-106">Pourquoi vous devriez mettre à niveau vos listes de distribution vers des groupes dans Outlook</span><span class="sxs-lookup"><span data-stu-id="4750e-106">Why you should upgrade your distribution lists to groups in Outlook</span></span>](https://support.microsoft.com/office/7fb3d880-593b-4909-aafa-950dd50ce188)

<span data-ttu-id="4750e-107">Vous pouvez mettre à niveau les DL une par une ou plusieurs en même temps.</span><span class="sxs-lookup"><span data-stu-id="4750e-107">You can upgrade DLs one at a time, or several at the same time.</span></span>

## <a name="upgrade-one-or-many-distribution-list-groups-to-microsoft-365-groups-in-outlook"></a><span data-ttu-id="4750e-108">Mettre à niveau un ou plusieurs groupes de listes de distribution vers Microsoft 365 groupes dans Outlook</span><span class="sxs-lookup"><span data-stu-id="4750e-108">Upgrade one or many distribution list groups to Microsoft 365 Groups in Outlook</span></span>

<span data-ttu-id="4750e-109">Vous devez être administrateur global ou administrateur Exchange pour mettre à niveau un groupe de listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="4750e-109">You must be a global admin or Exchange admin to upgrade a distribution list group.</span></span> <span data-ttu-id="4750e-110">Pour mettre à niveau vers Microsoft 365 groupes de distribution, le groupe de listes de distribution doit avoir un propriétaire avec une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="4750e-110">To upgrade to Microsoft 365 Groups, the distribution list group must have an owner with a mailbox.</span></span>

### <a name="use-the-new-eac-to-upgrade-one-or-many-distribution-list-groups-to-microsoft-365-groups-in-outlook"></a><span data-ttu-id="4750e-111">Utilisez le nouveau CENTRE D’EAC pour mettre à niveau un ou plusieurs groupes de listes de distribution vers Microsoft 365 groupes dans Outlook</span><span class="sxs-lookup"><span data-stu-id="4750e-111">Use the new EAC to upgrade one or many distribution list groups to Microsoft 365 Groups in Outlook</span></span>

1. <span data-ttu-id="4750e-112">Accédez au nouveau [centre Exchange’administration,](https://admin.exchange.microsoft.com)puis accédez à **Groupes de destinataires.** \> </span><span class="sxs-lookup"><span data-stu-id="4750e-112">Go to the new [Exchange admin center](https://admin.exchange.microsoft.com), and navigate to **Recipients** \> **Groups**.</span></span>

2. <span data-ttu-id="4750e-113">Sélectionnez le groupe de listes de distribution (également appelé groupe de **distribution)** que vous souhaitez mettre à niveau vers Microsoft 365 groupe à partir de la page **Groupes.**</span><span class="sxs-lookup"><span data-stu-id="4750e-113">Select the distribution list group (also called a **distribution group**) that you want to upgrade to Microsoft 365 group from the **Groups** page.</span></span>

3. <span data-ttu-id="4750e-114">Sélectionnez le **groupe de distribution Mise à niveau dans** la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="4750e-114">Select the **Upgrade distribution group** from the tool bar.</span></span>

4. <span data-ttu-id="4750e-115">Dans la boîte de dialogue **Prêt pour la mise à niveau ?**, cliquez sur Mettre à **niveau.**</span><span class="sxs-lookup"><span data-stu-id="4750e-115">In the dialog box **Ready to upgrade?**, click **Upgrade**.</span></span> <span data-ttu-id="4750e-116">Le processus commence immédiatement.</span><span class="sxs-lookup"><span data-stu-id="4750e-116">The process begins immediately.</span></span> <span data-ttu-id="4750e-117">Selon la taille et le nombre de groupes de listes de distribution que vous êtes en train de mettre à niveau, le processus peut prendre des minutes ou des heures.</span><span class="sxs-lookup"><span data-stu-id="4750e-117">Depending on the size and number of distribution list groups you're upgrading, the process can take minutes or hours.</span></span>

> [!NOTE]
> <span data-ttu-id="4750e-118">Une bannière en haut indique que la mise à niveau, par exemple, les groupes *de distribution ont été mis à niveau. La réflexion des modifications prend 5 minutes. Filtrez par Microsoft 365 pour voir les groupes de distrubtion* mis à niveau.</span><span class="sxs-lookup"><span data-stu-id="4750e-118">A banner at the top indicates the upgrade, for example, *Distribution group(s) has been upgraded. It will take 5 minutes to reflect the changes. Filter by Microsoft 365 groups to see the upgraded distrubtion groups(s)*.</span></span>

### <a name="use-the-classic-eac-to-upgrade-one-or-many-distribution-list-groups-to-microsoft-365-groups-in-outlook"></a><span data-ttu-id="4750e-119">Utiliser le CENTRE D’EAC classique pour mettre à niveau un ou plusieurs groupes de listes de distribution vers Microsoft 365 groupes dans Outlook</span><span class="sxs-lookup"><span data-stu-id="4750e-119">Use the Classic EAC to upgrade one or many distribution list groups to Microsoft 365 Groups in Outlook</span></span>

1. <span data-ttu-id="4750e-120">Go to the Classic <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Exchange admin center</a>.</span><span class="sxs-lookup"><span data-stu-id="4750e-120">Go to the Classic <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Exchange admin center</a>.</span></span>

2. <span data-ttu-id="4750e-121">Dans le Centre d’administration Exchange classique, allez à **Groupes de** \> **destinataires.**</span><span class="sxs-lookup"><span data-stu-id="4750e-121">In the Classic Exchange admin center, go to **Recipients** \> **Groups**.</span></span><br/><span data-ttu-id="4750e-122">Vous verrez un avis indiquant que vous avez des listes de distribution (également appelées groupes de **distribution)** qui peuvent être mises à niveau vers Microsoft 365 groupes.</span><span class="sxs-lookup"><span data-stu-id="4750e-122">You'll see a notice indicating you have distribution lists (also called **distribution groups**) that are eligible to be upgraded to Microsoft 365 Groups.</span></span><br/> <span data-ttu-id="4750e-123">![Sélectionner le bouton Commencer](../../media/8cf838b4-2644-401f-a366-08c1eea183eb.png)</span><span class="sxs-lookup"><span data-stu-id="4750e-123">![Select the Get started button](../../media/8cf838b4-2644-401f-a366-08c1eea183eb.png)</span></span>

3. <span data-ttu-id="4750e-124">Sélectionnez une ou plusieurs listes de distribution (également appelées groupe de **distribution)** dans la page **des groupes.**</span><span class="sxs-lookup"><span data-stu-id="4750e-124">Select one or more distribution lists (also called a **distribution group**) from the **groups** page.</span></span><br/><span data-ttu-id="4750e-125">![Sélectionner un groupe de distribution](../../media/2c303433-d60b-4100-a6ae-5809b03a8cdb.png)</span><span class="sxs-lookup"><span data-stu-id="4750e-125">![Select a distribution group](../../media/2c303433-d60b-4100-a6ae-5809b03a8cdb.png)</span></span>

4. <span data-ttu-id="4750e-126">Sélectionnez l’icône de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="4750e-126">Select the upgrade icon.</span></span><br/>![Icône Mise à niveau vers Microsoft 365 groupes](../../media/1e28cb3d-bff3-4be3-8329-1902d2d54720.png)

5. <span data-ttu-id="4750e-128">Dans la boîte de dialogue d’informations, **sélectionnez Oui** pour confirmer la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="4750e-128">On the information dialog, select **Yes** to confirm the upgrade.</span></span> <span data-ttu-id="4750e-129">Le processus commence immédiatement.</span><span class="sxs-lookup"><span data-stu-id="4750e-129">The process begins immediately.</span></span> <span data-ttu-id="4750e-130">Selon la taille et le nombre de DLs que vous êtes en train de mettre à niveau, le processus peut prendre des minutes ou des heures.</span><span class="sxs-lookup"><span data-stu-id="4750e-130">Depending on the size and number of DLs you're upgrading, the process can take minutes or hours.</span></span><br/><span data-ttu-id="4750e-131">Si la liste de distribution ne peut pas être mise à niveau, une boîte de dialogue s’affiche.</span><span class="sxs-lookup"><span data-stu-id="4750e-131">If the distribution list can't be upgraded, a dialog appears saying so.</span></span> <span data-ttu-id="4750e-132">Voir [quelles listes de distribution ne peuvent pas être mises à niveau ?](#which-distribution-lists-cant-be-upgraded).</span><span class="sxs-lookup"><span data-stu-id="4750e-132">See [Which distribution lists cannot be upgraded?](#which-distribution-lists-cant-be-upgraded).</span></span>

6. <span data-ttu-id="4750e-133">Si vous êtes en train de mettre à niveau plusieurs listes de distribution, utilisez la liste de listes listes pour filtrer les listes de distribution qui ont été mises à niveau.</span><span class="sxs-lookup"><span data-stu-id="4750e-133">If you're upgrading multiple distribution lists, use the drop-down list to filter which distribution lists have been upgraded.</span></span> <span data-ttu-id="4750e-134">Si la liste n’est pas terminée, patientez un peu plus longtemps, puis sélectionnez **Actualiser** pour voir ce qui a été correctement mis à niveau.</span><span class="sxs-lookup"><span data-stu-id="4750e-134">If the list isn't complete, wait a while longer and then select **Refresh** to see what's been successfully upgraded.</span></span><br/><span data-ttu-id="4750e-135">Aucun avis ne vous indique à quel moment le processus de mise à niveau est terminé pour toutes les DL que vous avez sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="4750e-135">There's no notice that tells you when the upgrade process has completed for all DLs you selected.</span></span> <span data-ttu-id="4750e-136">Vous pouvez le comprendre en cherchant à voir ce qui est répertorié sous **Disponible** pour la mise à niveau ou les **DL mises à niveau.**</span><span class="sxs-lookup"><span data-stu-id="4750e-136">You can figure this out by looking to see what's listed under **Available for upgrade** or **Upgraded DLs**.</span></span>

7. <span data-ttu-id="4750e-137">Si vous avez sélectionné une DL pour la mise à niveau, mais qu’elle apparaît toujours sur la page comme disponible pour la mise à niveau, elle n’a pas réussi à mettre à niveau.</span><span class="sxs-lookup"><span data-stu-id="4750e-137">If you selected a DL for upgrade, but it's still appeared on the page as Available to upgrade, then it failed to upgrade.</span></span> <span data-ttu-id="4750e-138">Voir [que faire si la mise à niveau ne fonctionne pas](#what-to-do-if-the-upgrade-doesnt-work).</span><span class="sxs-lookup"><span data-stu-id="4750e-138">See [What to do if the upgrade doesn't work](#what-to-do-if-the-upgrade-doesnt-work).</span></span>

> [!NOTE]
> <span data-ttu-id="4750e-139">Si vous avez reçu les e-mails de condensé de groupes, vous remarquerez peut-être en bas qu’il propose parfois de vous laisser mettre à niveau les listes de distribution éligibles dont vous êtes le propriétaire.</span><span class="sxs-lookup"><span data-stu-id="4750e-139">If you're getting the groups digest emails you may notice at the bottom that it will sometimes offer to let you upgrade any eligible distribution lists that you're the owner of.</span></span> <span data-ttu-id="4750e-140">Voir [Avoir une conversation de groupe dans Outlook](https://support.microsoft.com/office/a0482e24-a769-4e39-a5ba-a7c56e828b22) pour plus d’informations sur les e-mails digest.</span><span class="sxs-lookup"><span data-stu-id="4750e-140">See [Have a group conversation in Outlook](https://support.microsoft.com/office/a0482e24-a769-4e39-a5ba-a7c56e828b22) for more information about digest emails.</span></span>

## <a name="what-to-do-if-the-upgrade-doesnt-work"></a><span data-ttu-id="4750e-141">Que faire si la mise à niveau ne fonctionne pas</span><span class="sxs-lookup"><span data-stu-id="4750e-141">What to do if the upgrade doesn't work</span></span>

<span data-ttu-id="4750e-142">Les listes de distribution qui échouent à la mise à niveau restent inchangées.</span><span class="sxs-lookup"><span data-stu-id="4750e-142">Distribution lists that fail to upgrade remain unchanged.</span></span>

<span data-ttu-id="4750e-143">Si une ou plusieurs listes **de** distribution éligibles ne peuvent pas être mises à niveau, ouvrez un [ticket de support.](../../business-video/get-help-support.md)</span><span class="sxs-lookup"><span data-stu-id="4750e-143">If one or more **eligible** distribution lists fail to be upgraded, open a [Support ticket](../../business-video/get-help-support.md).</span></span> <span data-ttu-id="4750e-144">Le problème doit être recalcalé à l’équipe d’ingénierie des groupes pour qu’il en soit ainsi.</span><span class="sxs-lookup"><span data-stu-id="4750e-144">The issue will need to be escalated to the Groups Engineering team for them to figure out the problem.</span></span>

<span data-ttu-id="4750e-145">Il est possible que la liste de distribution n’a pas été mise à niveau en raison d’une panne de service, mais peu probable.</span><span class="sxs-lookup"><span data-stu-id="4750e-145">It's possible that the distribution list didn't get upgraded because of a service outage, but unlikely.</span></span> <span data-ttu-id="4750e-146">Si vous le souhaitez, patientez un certain temps, puis réessayez de mettre à niveau la DL.</span><span class="sxs-lookup"><span data-stu-id="4750e-146">If you want, wait a while and then try to upgrade the DL again.</span></span>

## <a name="how-to-use-powershell-to-upgrade-several-distribution-lists-at-the-same-time"></a><span data-ttu-id="4750e-147">Comment utiliser PowerShell pour mettre à niveau plusieurs listes de distribution en même temps</span><span class="sxs-lookup"><span data-stu-id="4750e-147">How to use PowerShell to upgrade several distribution lists at the same time</span></span>

<span data-ttu-id="4750e-148">Si vous avez l’expérience de l’utilisation de PowerShell, vous pouvez utiliser cet itinéraire au lieu d’utiliser l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4750e-148">If you're experienced at using PowerShell, you might want to go this route instead of using the UI.</span></span> <span data-ttu-id="4750e-149">Nous avons un ensemble de cmdlets qui vous aideront à mettre à niveau les listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="4750e-149">We have a set of cmdlets that will help you upgrade distribution lists.</span></span> <span data-ttu-id="4750e-150">Voir ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="4750e-150">See below.</span></span>

### <a name="upgrade-a-single-dl"></a><span data-ttu-id="4750e-151">Mettre à niveau une seule DL</span><span class="sxs-lookup"><span data-stu-id="4750e-151">Upgrade a single DL</span></span>

<span data-ttu-id="4750e-152">Pour mettre à niveau une seule DL, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="4750e-152">To upgrade a single DL, run the following command:</span></span>

```PowerShell
Upgrade-DistributionGroup -DlIdentities <Dl SMTP address>
```

<span data-ttu-id="4750e-153">Par exemple, si vous souhaitez mettre à niveau une DL avec des adresses SMTP dl1@contoso.com, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="4750e-153">For example, if you want to upgrade a DL with SMTP address dl1@contoso.com, run the following command:</span></span>

```PowerShell
Upgrade-DistributionGroup -DlIdentities dl1@contoso.com
```

> [!NOTE]
> <span data-ttu-id="4750e-154">Vous pouvez également mettre à niveau une liste de distribution unique vers un groupe Microsoft 365 à l’aide de l’cmdlet [PowerShell New-UnifiedGroup](/powershell/module/exchange/new-unifiedgroup)</span><span class="sxs-lookup"><span data-stu-id="4750e-154">You can also upgrade a single distribution list to a Microsoft 365 group using the [New-UnifiedGroup](/powershell/module/exchange/new-unifiedgroup) PowerShell cmdlet</span></span>

### <a name="upgrade-multiple-dls-in-a-batch"></a><span data-ttu-id="4750e-155">Mettre à niveau plusieurs DLs dans un lot</span><span class="sxs-lookup"><span data-stu-id="4750e-155">Upgrade multiple DLs in a batch</span></span>

<span data-ttu-id="4750e-156">Vous pouvez également passer plusieurs DLs en tant que lot et les mettre à niveau ensemble :</span><span class="sxs-lookup"><span data-stu-id="4750e-156">You can also pass multiple DLs as a batch and upgrade them together:</span></span>

```PowerShell
Upgrade-DistributionGroup -DlIdentities <DL SMTP address1>, <DL SMTP address2>,
<DL SMTP address3>, <DL SMTP address4>
```

<span data-ttu-id="4750e-157">Par exemple, si vous souhaitez mettre à niveau cinq DLs avec l’adresse SMTP `dl1@contoso.com` `dl2@contoso.com` `dl3@contoso.com` et, `dl4@contoso.com` `dl5@contoso.com` et, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="4750e-157">For example, if you want to upgrade five DLs with SMTP address `dl1@contoso.com` and `dl2@contoso.com`, `dl3@contoso.com`, `dl4@contoso.com` and `dl5@contoso.com`, run the following command:</span></span>

`Upgrade-DistributionGroup -DlIdentities dl1@contoso.com, dl2@contoso.com, dl3@contoso.com, dl4@contoso.com, dl5@contoso.com`

### <a name="upgrade-all-eligible-dls"></a><span data-ttu-id="4750e-158">Mettre à niveau toutes les DL éligibles</span><span class="sxs-lookup"><span data-stu-id="4750e-158">Upgrade all eligible DLs</span></span>

<span data-ttu-id="4750e-159">Il existe deux façons de mettre à niveau toutes les DL éligibles.</span><span class="sxs-lookup"><span data-stu-id="4750e-159">There are two ways in which you can upgrade all the eligible DLs.</span></span>

> [!NOTE]
> <span data-ttu-id="4750e-160">La cmdlet Upgrade-DistributionGroup ne reçoit pas de données du pipeline, c’est pourquoi il est nécessaire d’utiliser l’opérateur « foreach-object » pour s’exécuter {} correctement.</span><span class="sxs-lookup"><span data-stu-id="4750e-160">The Upgrade-DistributionGroup cmdlet doesn't receive data from the pipeline, for this reason it's required to use "foreach-object{}" operator to run successfully.</span></span>

1. <span data-ttu-id="4750e-161">Obtenez les DL éligibles dans le client et faites-les mettre à niveau à l’aide de la commande de mise à niveau :</span><span class="sxs-lookup"><span data-stu-id="4750e-161">Get the eligible DLs in the tenant and upgrade them using the upgrade command:</span></span>

```PowerShell
Get-EligibleDistributionGroupForMigration | Foreach-Object{
    Upgrade-DistributionGroup -DlIdentities $_.PrimarySMTPAddress
}
```

2. <span data-ttu-id="4750e-162">Obtenir la liste de toutes les DL et mettre à niveau uniquement les DL éligibles :</span><span class="sxs-lookup"><span data-stu-id="4750e-162">Get the list of all DLs and upgrade only the eligible DLs:</span></span>

```PowerShell
Get-DistributionGroup| Foreach-Object{
    Upgrade-DistributionGroup -DlIdentities $_.PrimarySMTPAddress
}
```

## <a name="faq-about-upgrading-distribution-lists-to-microsoft-365-groups-in-outlook"></a><span data-ttu-id="4750e-163">FAQ sur la mise à niveau de listes de distribution Microsoft 365 groupes dans Outlook</span><span class="sxs-lookup"><span data-stu-id="4750e-163">FAQ about upgrading distribution lists to Microsoft 365 Groups in Outlook</span></span>

### <a name="which-distribution-lists-cant-be-upgraded"></a><span data-ttu-id="4750e-164">Quelles listes de distribution ne peuvent pas être mises à niveau ?</span><span class="sxs-lookup"><span data-stu-id="4750e-164">Which distribution lists can't be upgraded?</span></span>

<span data-ttu-id="4750e-165">Vous pouvez uniquement mettre à niveau des listes de distribution non imbrique, simples et gérées dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="4750e-165">You can only upgrade cloud-managed, simple, non-nested distribution lists.</span></span> <span data-ttu-id="4750e-166">Le tableau ci-dessous répertorie les listes de distribution qui **ne peuvent** pas être mises à niveau.</span><span class="sxs-lookup"><span data-stu-id="4750e-166">The table below lists distribution lists that **CANNOT** be upgraded.</span></span>

|<span data-ttu-id="4750e-167">**Property**</span><span class="sxs-lookup"><span data-stu-id="4750e-167">**Property**</span></span>|<span data-ttu-id="4750e-168">**Éligible ?**</span><span class="sxs-lookup"><span data-stu-id="4750e-168">**Eligible?**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4750e-169">Liste de distribution gérée sur site.</span><span class="sxs-lookup"><span data-stu-id="4750e-169">On-premises managed distribution list.</span></span>  <br/> |<span data-ttu-id="4750e-170">Non</span><span class="sxs-lookup"><span data-stu-id="4750e-170">No</span></span>  <br/> |
|<span data-ttu-id="4750e-171">Listes de distribution imbrmbrées.</span><span class="sxs-lookup"><span data-stu-id="4750e-171">Nested distribution lists.</span></span> <span data-ttu-id="4750e-172">La liste de distribution a des groupes enfants ou est membre d’un autre groupe.</span><span class="sxs-lookup"><span data-stu-id="4750e-172">Distribution list either has child groups or is a member of another group.</span></span>  <br/> |<span data-ttu-id="4750e-173">Non</span><span class="sxs-lookup"><span data-stu-id="4750e-173">No</span></span>  <br/> |
|<span data-ttu-id="4750e-174">Listes de distribution dont le **membre RecipientTypeDetails** est autre que **UserMailbox**, **SharedMailbox**, **TeamMailbox**, **MailUser**</span><span class="sxs-lookup"><span data-stu-id="4750e-174">Distribution lists with member **RecipientTypeDetails** other than **UserMailbox**, **SharedMailbox**, **TeamMailbox**, **MailUser**</span></span>  <br/> |<span data-ttu-id="4750e-175">Non</span><span class="sxs-lookup"><span data-stu-id="4750e-175">No</span></span>  <br/> |
|<span data-ttu-id="4750e-176">Liste de distribution avec plus de 100 propriétaires</span><span class="sxs-lookup"><span data-stu-id="4750e-176">Distribution list that has more than 100 owners</span></span>  <br/> |<span data-ttu-id="4750e-177">Non</span><span class="sxs-lookup"><span data-stu-id="4750e-177">No</span></span>  <br/> |
|<span data-ttu-id="4750e-178">Liste de distribution qui ne possède que des membres, mais pas de propriétaire</span><span class="sxs-lookup"><span data-stu-id="4750e-178">Distribution list that only has members but no owner</span></span>  <br/> |<span data-ttu-id="4750e-179">Non</span><span class="sxs-lookup"><span data-stu-id="4750e-179">No</span></span>  <br/> |
|<span data-ttu-id="4750e-180">Liste de distribution avec alias contenant des caractères spéciaux</span><span class="sxs-lookup"><span data-stu-id="4750e-180">Distribution list that has alias containing special characters</span></span>  <br/> |<span data-ttu-id="4750e-181">Non</span><span class="sxs-lookup"><span data-stu-id="4750e-181">No</span></span>  <br/> |
|<span data-ttu-id="4750e-182">Si la liste de distribution est configurée pour être une adresse de forwarding pour la boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="4750e-182">If the distribution list is configured to be a forwarding address for Shared Mailbox</span></span>  <br/> |<span data-ttu-id="4750e-183">Non</span><span class="sxs-lookup"><span data-stu-id="4750e-183">No</span></span>  <br/> |
|<span data-ttu-id="4750e-184">Si la DL fait partie de **la restriction de l’expéditeur** dans une autre DL.</span><span class="sxs-lookup"><span data-stu-id="4750e-184">If the DL is part of **Sender Restriction** in another DL.</span></span>  <br/> |<span data-ttu-id="4750e-185">Non</span><span class="sxs-lookup"><span data-stu-id="4750e-185">No</span></span>  <br/> |
|<span data-ttu-id="4750e-186">Groupes de sécurité</span><span class="sxs-lookup"><span data-stu-id="4750e-186">Security groups</span></span>  <br/> |<span data-ttu-id="4750e-187">Non</span><span class="sxs-lookup"><span data-stu-id="4750e-187">No</span></span>  <br/> |
|<span data-ttu-id="4750e-188">Listes de distribution dynamique</span><span class="sxs-lookup"><span data-stu-id="4750e-188">Dynamic Distribution lists</span></span>  <br/> |<span data-ttu-id="4750e-189">Non</span><span class="sxs-lookup"><span data-stu-id="4750e-189">No</span></span>  <br/> |
|<span data-ttu-id="4750e-190">Listes de distribution qui ont été converties **en RoomLists**</span><span class="sxs-lookup"><span data-stu-id="4750e-190">Distribution lists that were converted to **RoomLists**</span></span>  <br/> |<span data-ttu-id="4750e-191">Non</span><span class="sxs-lookup"><span data-stu-id="4750e-191">No</span></span>  <br/> |
|<span data-ttu-id="4750e-192">Listes de distribution **où MemberJoinRestriction** et/ou **MemberDepartRestriction** est **fermé**</span><span class="sxs-lookup"><span data-stu-id="4750e-192">Distribution lists where **MemberJoinRestriction** and/or **MemberDepartRestriction** is **Closed**</span></span>  <br/> |<span data-ttu-id="4750e-193">Non</span><span class="sxs-lookup"><span data-stu-id="4750e-193">No</span></span>  <br/> |

### <a name="check-which-dls-are-eligible-for-upgrade"></a><span data-ttu-id="4750e-194">Vérifier les DL éligibles pour la mise à niveau</span><span class="sxs-lookup"><span data-stu-id="4750e-194">Check which DLs are eligible for upgrade</span></span>

<span data-ttu-id="4750e-195">Si vous souhaitez vérifier si une DL est éligible ou non, vous pouvez exécuter la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="4750e-195">If you want to check whether a DL is eligible or not, you can run the below command:</span></span>

`Get-DistributionGroup <DL SMTP address> | Get-EligibleDistributionGroupForMigration`

<span data-ttu-id="4750e-196">Si vous souhaitez vérifier les DL éligibles pour la mise à niveau, exécutez simplement la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="4750e-196">If you want to check which DLs are eligible for upgrade just run the following command:</span></span>

`Get-EligibleDistributionGroupForMigration`

### <a name="who-can-run-the-upgrade-scripts"></a><span data-ttu-id="4750e-197">Qui pouvez exécuter les scripts de mise à niveau ?</span><span class="sxs-lookup"><span data-stu-id="4750e-197">Who can run the upgrade scripts?</span></span>

<span data-ttu-id="4750e-198">Personnes ayant des droits d’administrateur global ou Exchange’administrateur.</span><span class="sxs-lookup"><span data-stu-id="4750e-198">People with global admin or Exchange admin rights.</span></span>

### <a name="why-is-the-contact-card-still-showing-a-distribution-list-what-should-i-do-to-prevent-an-upgraded-distribution-list-from-showing-up-in-my-auto-suggest-list"></a><span data-ttu-id="4750e-199">Pourquoi la carte de visite affiche-t-elle toujours une liste de distribution ?</span><span class="sxs-lookup"><span data-stu-id="4750e-199">Why is the contact card still showing a distribution list?</span></span> <span data-ttu-id="4750e-200">Que dois-je faire pour empêcher l’affichage d’une liste de distribution mise à niveau dans ma liste de suggestions automatiques ?</span><span class="sxs-lookup"><span data-stu-id="4750e-200">What should I do to prevent an upgraded distribution list from showing up in my auto suggest list?</span></span>

- <span data-ttu-id="4750e-201">Par Outlook : lorsqu’une personne tente d’envoyer un courrier électronique dans Outlook en tapant le nom du groupe Microsoft 365 après la migration, le destinataire est résolu en tant que liste de distribution au lieu du groupe.</span><span class="sxs-lookup"><span data-stu-id="4750e-201">For Outlook: When someone tries to send an email in Outlook by typing the Microsoft 365 group name after migration, the recipient will be resolved as the distribution list instead of the group.</span></span> <span data-ttu-id="4750e-202">La carte de visite du destinataire sera la carte de visite des listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="4750e-202">The contact card of the recipient will be the distribution lists contact card.</span></span> <span data-ttu-id="4750e-203">Cela est dû au cache de destinataires ou au cache de noms de pseudo dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="4750e-203">This is because of the recipient cache or nick name cache in Outlook.</span></span> <span data-ttu-id="4750e-204">L’e-mail est envoyé au groupe, mais peut être source de confusion pour l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="4750e-204">The email will be sent successfully to the group, but might cause confusion to the sender.</span></span><br/><span data-ttu-id="4750e-205">Vous pouvez effectuer les étapes de cet article, Information [about the Outlook AutoComplete list](/outlook/troubleshoot/contacts/information-about-the-outlook-autocomplete-list) to reset the cache, which will fix this issue.</span><span class="sxs-lookup"><span data-stu-id="4750e-205">You can perform the steps in this article, [Information about the Outlook AutoComplete list](/outlook/troubleshoot/contacts/information-about-the-outlook-autocomplete-list) to reset the cache, which will fix this issue.</span></span>

- <span data-ttu-id="4750e-206">Pour Outlook sur le web : en cas de Outlook sur le web, le destinataire de la liste de distribution reste dans le cache.</span><span class="sxs-lookup"><span data-stu-id="4750e-206">For Outlook on the web: In case of Outlook on the web, the distribution list recipient will still remain in the cache.</span></span> <span data-ttu-id="4750e-207">Vous pouvez suivre [](https://support.microsoft.com/office/9E1419D9-E88F-445B-B07F-F558B8A37C58) les étapes de la procédure de suppression du nom suggéré ou de l’adresse de messagerie de la liste de mise à jour automatique pour actualiser le cache et voir la carte de visite du groupe.</span><span class="sxs-lookup"><span data-stu-id="4750e-207">You can follow the steps in [Remove suggested name or email address from the Auto-Complete List](https://support.microsoft.com/office/9E1419D9-E88F-445B-B07F-F558B8A37C58) to refresh the cache to see the group contact card.</span></span>

### <a name="do-new-group-members-get-a-welcome-email-in-their-inbox"></a><span data-ttu-id="4750e-208">Les nouveaux membres du groupe obtiennent-ils un e-mail de bienvenue dans leur boîte de réception ?</span><span class="sxs-lookup"><span data-stu-id="4750e-208">Do new group members get a welcome email in their inbox?</span></span>

<span data-ttu-id="4750e-209">Non.</span><span class="sxs-lookup"><span data-stu-id="4750e-209">No.</span></span> <span data-ttu-id="4750e-210">Le paramètre permettant d’activer les messages d’accueil est false par défaut.</span><span class="sxs-lookup"><span data-stu-id="4750e-210">The setting to enable welcome messages is set to false by default.</span></span> <span data-ttu-id="4750e-211">Ce paramètre affecte à la fois les membres existants et les nouveaux membres du groupe qui peuvent rejoindre le groupe une fois la migration terminée.</span><span class="sxs-lookup"><span data-stu-id="4750e-211">This setting affects both existing and new group members who may join after the migration is complete.</span></span> <span data-ttu-id="4750e-212">Si le propriétaire du groupe autorise ultérieurement les utilisateurs invités, les utilisateurs invités ne reçoivent pas de message électronique de bienvenue dans leur boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="4750e-212">If the group owner later allows guest users, guest users won't receive a welcome email in their inbox.</span></span> <span data-ttu-id="4750e-213">Les membres invités peuvent continuer à travailler avec le groupe.</span><span class="sxs-lookup"><span data-stu-id="4750e-213">Guest members can continue working with the group.</span></span>

### <a name="what-if-one-or-some-of-the-dls-are-not-upgraded"></a><span data-ttu-id="4750e-214">Que se passe-t-il si une ou certaines DL ne sont pas mises à niveau ?</span><span class="sxs-lookup"><span data-stu-id="4750e-214">What if one or some of the DLs are not upgraded?</span></span>

<span data-ttu-id="4750e-215">Dans certains cas, la DL est éligible, mais n’a pas pu être mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="4750e-215">There are some cases in which though DL is eligible but could not be upgraded.</span></span> <span data-ttu-id="4750e-216">La DL n’est pas mise à niveau et reste en tant que DL.</span><span class="sxs-lookup"><span data-stu-id="4750e-216">The DL does not get upgraded and remains as a DL.</span></span>

- <span data-ttu-id="4750e-217">Lorsque l’administrateur a appliqué la stratégie d’adresse de messagerie de groupe pour les groupes d’une organisation et qu’il essaie de mettre à niveau les DL qui ne remplissent pas les critères, la DL n’est pas mise à niveau </span><span class="sxs-lookup"><span data-stu-id="4750e-217">Where admin has applied **Group Email Address Policy** for the groups in an organization and they try to upgrade DLs that doesn't fulfill the criteria, the DL does not get upgraded</span></span>

- <span data-ttu-id="4750e-218">DLs with **MemberJoinRestriction** or **MemberDepartRestriction** set to **Closed**, could not be upgraded</span><span class="sxs-lookup"><span data-stu-id="4750e-218">DLs with **MemberJoinRestriction** or **MemberDepartRestriction** set to **Closed**, could not be upgraded</span></span>

### <a name="what-happens-to-the-dl-if-the-upgrade-from-eac-fails"></a><span data-ttu-id="4750e-219">Qu’advient-il de la DL en cas d’échec de la mise à niveau à partir du EAC ?</span><span class="sxs-lookup"><span data-stu-id="4750e-219">What happens to the DL if the upgrade from EAC fails?</span></span>

<span data-ttu-id="4750e-220">La mise à niveau se produit uniquement lorsque l’appel est soumis au serveur.</span><span class="sxs-lookup"><span data-stu-id="4750e-220">The upgrade will happen only when the call is submitted to the server.</span></span> <span data-ttu-id="4750e-221">Si la mise à niveau échoue, vos DL sont intactes.</span><span class="sxs-lookup"><span data-stu-id="4750e-221">If the upgrade fails, your DLs will be intact.</span></span> <span data-ttu-id="4750e-222">Ils fonctionneront comme avant.</span><span class="sxs-lookup"><span data-stu-id="4750e-222">They will work like they used to.</span></span>

## <a name="related-content"></a><span data-ttu-id="4750e-223">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="4750e-223">Related content</span></span>

<span data-ttu-id="4750e-224">[Comparer les groupes](../create-groups/compare-groups.md) (article)</span><span class="sxs-lookup"><span data-stu-id="4750e-224">[Compare groups](../create-groups/compare-groups.md) (article)</span></span>\
<span data-ttu-id="4750e-225">[Expliquer Microsoft 365 groupes à vos utilisateurs](../create-groups/explain-groups-knowledge-worker.md) (article)</span><span class="sxs-lookup"><span data-stu-id="4750e-225">[Explaining Microsoft 365 Groups to your users](../create-groups/explain-groups-knowledge-worker.md) (article)</span></span>\
[<span data-ttu-id="4750e-226">Ajouter ou supprimer des membres de groupes Microsoft 365 à l’aide du Centre d’administration</span><span class="sxs-lookup"><span data-stu-id="4750e-226">Add or remove members from Microsoft 365 groups using the admin center</span></span>](../create-groups/add-or-remove-members-from-groups.md)
