---
title: Mettre à niveau les listes de distribution vers des groupes Microsoft 365 dans Outlook
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 787d7a75-e201-46f3-a242-f698162ff09f
description: Découvrez comment mettre à niveau une ou plusieurs listes de distribution vers des groupes Microsoft 365 dans Outlook, et comment utiliser PowerShell pour mettre à niveau plusieurs listes de distribution simultanément.
ms.openlocfilehash: 14eeedcc898c13c31362731699f575bc06f96878
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43627991"
---
# <a name="upgrade-distribution-lists-to-microsoft-365-groups-in-outlook"></a><span data-ttu-id="21aee-103">Mettre à niveau les listes de distribution vers des groupes Microsoft 365 dans Outlook</span><span class="sxs-lookup"><span data-stu-id="21aee-103">Upgrade distribution lists to Microsoft 365 Groups in Outlook</span></span>

<span data-ttu-id="21aee-104">Vous pouvez mettre à niveau les listes de distribution vers des groupes Microsoft 365 avec Outlook.</span><span class="sxs-lookup"><span data-stu-id="21aee-104">You can upgrade distribution lists to Microsoft 365 Groups with Outlook.</span></span> <span data-ttu-id="21aee-105">Il s’agit d’un excellent moyen d’accorder à la distribution de votre organisation toutes les fonctionnalités des groupes Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="21aee-105">This is a great way to give your organization's distribution lists all the features and functionality of Microsoft 365 Groups.</span></span> [<span data-ttu-id="21aee-106">Pourquoi devriez-vous mettre à niveau vos listes de distribution vers des groupes dans Outlook ?</span><span class="sxs-lookup"><span data-stu-id="21aee-106">Why you should upgrade your distribution lists to groups in Outlook</span></span>](https://support.office.com/article/7fb3d880-593b-4909-aafa-950dd50ce188.aspx)

<span data-ttu-id="21aee-107">Vous pouvez mettre à niveau les listes de distribution une par une ou plusieurs simultanément.</span><span class="sxs-lookup"><span data-stu-id="21aee-107">You can upgrade DLs one at a time, or several at the same time.</span></span>

## <a name="upgrade-one-or-many-distribution-lists-to-microsoft-365-groups-in-outlook"></a><span data-ttu-id="21aee-108">Mettre à niveau une ou plusieurs listes de distribution vers des groupes Microsoft 365 dans Outlook</span><span class="sxs-lookup"><span data-stu-id="21aee-108">Upgrade one or many distribution lists to Microsoft 365 Groups in Outlook</span></span>

<span data-ttu-id="21aee-109">Vous devez être un administrateur général ou un administrateur Exchange pour mettre à niveau une liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="21aee-109">You must be a global admin or Exchange admin to upgrade a distribution list.</span></span> <span data-ttu-id="21aee-110">Pour effectuer une mise à niveau vers les groupes Microsoft 365, un groupe de distribution doit avoir un propriétaire avec une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="21aee-110">To upgrade to Microsoft 365 Groups, a distribution group must have an owner with a mailbox.</span></span> 

1. <span data-ttu-id="21aee-111">Accédez au <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Centre d’administration Exchange</a>.</span><span class="sxs-lookup"><span data-stu-id="21aee-111">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Exchange admin center</a>.</span></span>

2. <span data-ttu-id="21aee-112">Dans le centre d’administration Exchange, accédez à **groupes**de **destinataires** \> .</span><span class="sxs-lookup"><span data-stu-id="21aee-112">In the Exchange admin center, go to **Recipients** \> **Groups**.</span></span><br/><span data-ttu-id="21aee-113">Vous verrez une notification indiquant que des listes de distribution (également appelées **groupes de distribution** ) sont éligibles pour être mises à niveau vers les groupes Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="21aee-113">You'll see a notice indicating you have distribution lists (also called **distribution groups** ) that are eligible to be upgraded to Microsoft 365 Groups.</span></span><br/> <span data-ttu-id="21aee-114">![Sélectionnez le bouton prise en main](../../media/8cf838b4-2644-401f-a366-08c1eea183eb.png)</span><span class="sxs-lookup"><span data-stu-id="21aee-114">![Select the Get started button](../../media/8cf838b4-2644-401f-a366-08c1eea183eb.png)</span></span>

3. <span data-ttu-id="21aee-115">Sélectionnez une ou plusieurs listes de distribution (également appelées **groupe de distribution** ) dans la page **groupes** .</span><span class="sxs-lookup"><span data-stu-id="21aee-115">Select one or more distribution lists (also called a **distribution group** ) from the **groups** page.</span></span><br/><span data-ttu-id="21aee-116">![Sélectionner un groupe de distribution](../../media/2c303433-d60b-4100-a6ae-5809b03a8cdb.png)</span><span class="sxs-lookup"><span data-stu-id="21aee-116">![Select a distribution group](../../media/2c303433-d60b-4100-a6ae-5809b03a8cdb.png)</span></span>

4. <span data-ttu-id="21aee-117">Sélectionnez l’icône de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="21aee-117">Select the upgrade icon.</span></span><br/>![Icône de mise à niveau vers les groupes Microsoft 365](../../media/1e28cb3d-bff3-4be3-8329-1902d2d54720.png)

5. <span data-ttu-id="21aee-119">Dans la boîte de dialogue informations, sélectionnez **Oui** pour confirmer la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="21aee-119">On the information dialog, select **Yes** to confirm the upgrade.</span></span> <span data-ttu-id="21aee-120">Le processus commence immédiatement.</span><span class="sxs-lookup"><span data-stu-id="21aee-120">The process begins immediately.</span></span> <span data-ttu-id="21aee-121">En fonction de la taille et du nombre de listes de distribution que vous mettez à niveau, le processus peut prendre des minutes ou des heures.</span><span class="sxs-lookup"><span data-stu-id="21aee-121">Depending on the size and number of DLs you're upgrading, the process can take minutes or hours.</span></span><br/><span data-ttu-id="21aee-122">Si la liste de distribution ne peut pas être mise à niveau, une boîte de dialogue s’affiche.</span><span class="sxs-lookup"><span data-stu-id="21aee-122">If the distribution list can't be upgraded, a dialog appears saying so.</span></span> <span data-ttu-id="21aee-123">[Quels sont les listes de distribution qui ne peuvent pas être mises à niveau ?](#which-distribution-lists-cannot-be-upgraded).</span><span class="sxs-lookup"><span data-stu-id="21aee-123">See [Which distribution lists cannot be upgraded?](#which-distribution-lists-cannot-be-upgraded).</span></span>

6. <span data-ttu-id="21aee-124">Si vous mettez à niveau plusieurs listes de distribution, utilisez la liste déroulante pour filtrer les listes de distribution qui ont été mises à niveau.</span><span class="sxs-lookup"><span data-stu-id="21aee-124">If you're upgrading multiple distribution lists, use the drop-down list to filter which distribution lists have been upgraded.</span></span> <span data-ttu-id="21aee-125">Si la liste n’est pas complète, patientez un certain temps, puis sélectionnez **Actualiser** pour voir ce qui a été correctement mis à niveau.</span><span class="sxs-lookup"><span data-stu-id="21aee-125">If the list isn't complete, wait a while longer and then select **Refresh** to see what's been successfully upgraded.</span></span><br/><span data-ttu-id="21aee-126">Aucune notification ne vous indique quand le processus de mise à niveau est terminé pour toutes les listes de distribution que vous avez sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="21aee-126">There's no notice that tells you when the upgrade process has completed for all DLs you selected.</span></span> <span data-ttu-id="21aee-127">Vous pouvez le faire en vous recherchant dans la section **disponible pour la mise à niveau** ou les **listes de distribution**de contenu.</span><span class="sxs-lookup"><span data-stu-id="21aee-127">You can figure this out by looking to see what's listed under **Available for upgrade** or **Upgraded DLs**.</span></span>

7. <span data-ttu-id="21aee-128">Si vous avez sélectionné une LD pour la mise à niveau, mais qu’elle apparaît toujours sur la page comme disponible pour la mise à niveau, la mise à niveau a échoué.</span><span class="sxs-lookup"><span data-stu-id="21aee-128">If you selected a DL for upgrade, but it's still appears on the page as Available to upgrade, then it failed to upgrade.</span></span> <span data-ttu-id="21aee-129">Consultez [la procédure à suivre si la mise à niveau ne fonctionne pas](#what-to-do-if-the-upgrade-doesnt-work).</span><span class="sxs-lookup"><span data-stu-id="21aee-129">See [What to do if the upgrade doesn't work](#what-to-do-if-the-upgrade-doesnt-work).</span></span>

> [!NOTE]
> <span data-ttu-id="21aee-130">Si vous obtenez les messages de résumé des groupes que vous pouvez remarquer dans la partie inférieure, il est parfois proposé de vous permettre de mettre à niveau toutes les listes de distribution éligibles dont vous êtes propriétaire.</span><span class="sxs-lookup"><span data-stu-id="21aee-130">If you're getting the groups digest emails you may notice at the bottom that it will sometimes offer to let you upgrade any eligible distribution lists that you're the owner of.</span></span> <span data-ttu-id="21aee-131">Pour plus d’informations sur les e-mails de résumé [, consultez la rubrique utiliser une conversation de groupe dans Outlook](https://support.office.com/article/a0482e24-a769-4e39-a5ba-a7c56e828b22.aspx) .</span><span class="sxs-lookup"><span data-stu-id="21aee-131">See [Have a group conversation in Outlook](https://support.office.com/article/a0482e24-a769-4e39-a5ba-a7c56e828b22.aspx) for more information about digest emails.</span></span>


## <a name="what-to-do-if-the-upgrade-doesnt-work"></a><span data-ttu-id="21aee-132">Procédure à suivre en cas de non-fonctionnement de la mise à niveau</span><span class="sxs-lookup"><span data-stu-id="21aee-132">What to do if the upgrade doesn't work</span></span>

<span data-ttu-id="21aee-133">Les listes de distribution dont la mise à niveau échoue restent inchangées.</span><span class="sxs-lookup"><span data-stu-id="21aee-133">Distribution lists that fail to upgrade remain unchanged.</span></span>

<span data-ttu-id="21aee-134">Si une ou plusieurs listes de distribution **éligibles** ne peuvent pas être mises à niveau, ouvrez un [ticket de support](../contact-support-for-business-products.md).</span><span class="sxs-lookup"><span data-stu-id="21aee-134">If one or more **eligible** distribution lists fail to be upgraded, open a [Support ticket](../contact-support-for-business-products.md).</span></span> <span data-ttu-id="21aee-135">Le problème doit être remonté vers l’équipe d’ingénierie des groupes pour qu’il soit possible de déterminer le problème.</span><span class="sxs-lookup"><span data-stu-id="21aee-135">The issue will need to be escalated to the Groups Engineering team for them to figure out the problem.</span></span>

<span data-ttu-id="21aee-136">Il est possible que la liste de distribution n’ait pas été mise à niveau en raison d’une panne de service, mais très improbable.</span><span class="sxs-lookup"><span data-stu-id="21aee-136">It's possible that the distribution list didn't get upgraded because of a service outage, but pretty unlikely.</span></span> <span data-ttu-id="21aee-137">Si vous le souhaitez, patientez quelques instants, puis réessayez de mettre à niveau la nouvelle DL.</span><span class="sxs-lookup"><span data-stu-id="21aee-137">If you want, wait a while and then try to upgrade the DL again.</span></span>

## <a name="how-to-use-powershell-to-upgrade-several-distribution-lists-at-the-same-time"></a><span data-ttu-id="21aee-138">Comment utiliser PowerShell pour mettre à niveau plusieurs listes de distribution en même temps</span><span class="sxs-lookup"><span data-stu-id="21aee-138">How to use PowerShell to upgrade several distribution lists at the same time</span></span>

<span data-ttu-id="21aee-139">Si vous avez recours à PowerShell, il se peut que vous souhaitiez utiliser cet itinéraire au lieu d’utiliser l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="21aee-139">If you're experienced at using PowerShell, you might want to go this route instead of using the UI.</span></span> <span data-ttu-id="21aee-140">Nous disposons d’un ensemble d’applets de commande qui vous aideront à mettre à niveau les listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="21aee-140">We have a set of cmdlets that will help you upgrade distribution lists.</span></span> <span data-ttu-id="21aee-141">Voir ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="21aee-141">See below.</span></span>

### <a name="upgrade-a-single-dl"></a><span data-ttu-id="21aee-142">Mettre à niveau une seule LD</span><span class="sxs-lookup"><span data-stu-id="21aee-142">Upgrade a single DL</span></span>

<span data-ttu-id="21aee-143">Pour mettre à niveau une seule DL, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="21aee-143">To upgrade a single DL run the following command:</span></span>

`Upgrade-DistributionGroup -DlIdentities \<Dl SMTP address\>`

<span data-ttu-id="21aee-144">Par exemple, si vous souhaitez mettre à niveau une distribution de listes de distribution avec l’adresse SMTP dl1@contoso.com, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="21aee-144">For example, if you want to upgrade a DLs with SMTP address dl1@contoso.com, run the following command:</span></span>

`Upgrade-DistributionGroup -DlIdentities dl1@contoso.com`

> [!NOTE]
> <span data-ttu-id="21aee-145">Vous pouvez également mettre à niveau une seule liste de distribution vers un groupe Microsoft 365 à l’aide de l’applet de commande PowerShell [New-UnifiedGroup](https://go.microsoft.com/fwlink/?LinkID=786379)</span><span class="sxs-lookup"><span data-stu-id="21aee-145">You can also upgrade a single distribution list to a Microsoft 365 group using the [New-UnifiedGroup](https://go.microsoft.com/fwlink/?LinkID=786379) PowerShell cmdlet</span></span>

### <a name="upgrade-multiple-dls-in-a-batch"></a><span data-ttu-id="21aee-146">Mettre à niveau plusieurs listes de distribution dans un lot</span><span class="sxs-lookup"><span data-stu-id="21aee-146">Upgrade multiple DLs in a batch</span></span>

<span data-ttu-id="21aee-147">Vous pouvez également transmettre plusieurs listes de distribution par lots et les mettre à niveau ensemble :</span><span class="sxs-lookup"><span data-stu-id="21aee-147">You can also pass multiple DLs as a batch and upgrade them together:</span></span>

```
Upgrade-DistributionGroup -DlIdentities \<DL SMTP address1\>, \< DL SMTP address2\>,

\< DL SMTP address3\>, \< DL SMTP address 4\>
```

<span data-ttu-id="21aee-148">Par exemple, si vous souhaitez mettre à niveau cinq listes de distribution `dl1@contoso.com` avec `dl2@contoso.com`adresse `dl3@contoso.com`SMTP `dl4@contoso.com` et `dl5@contoso.com`, et, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="21aee-148">For example, if you want to upgrade five DLs with SMTP address `dl1@contoso.com` and `dl2@contoso.com`, `dl3@contoso.com`, `dl4@contoso.com` and `dl5@contoso.com`, run the following command:</span></span>

`Upgrade-DistributionGroup -DlIdentities dl1@contoso.com, dl2@contoso.com, dl3@contoso.com, dl4@contoso.com, dl5@contoso.com`

### <a name="upgrade-all-eligible-dls"></a><span data-ttu-id="21aee-149">Mettre à niveau toutes les listes de distribution éligibles</span><span class="sxs-lookup"><span data-stu-id="21aee-149">Upgrade all eligible DLs</span></span>

<span data-ttu-id="21aee-150">Il existe deux façons de mettre à niveau toutes les listes de distribution éligibles.</span><span class="sxs-lookup"><span data-stu-id="21aee-150">There are two ways in which you can upgrade all the eligible DLs.</span></span>

> [!NOTE]
> <span data-ttu-id="21aee-151">La cmdlet Upgrade-DistributionGroup ne reçoit pas de données du pipeline, pour cette raison, il est nécessaire d’utiliser{}l’opérateur « ForEach-Object » pour s’exécuter correctement.</span><span class="sxs-lookup"><span data-stu-id="21aee-151">The Upgrade-DistributionGroup cmdlet doesn't receive data from the pipeline, for this reason it's required to use "foreach-object{}" operator to run successfully.</span></span>

1. <span data-ttu-id="21aee-152">Obtenez les listes de distribution éligibles dans le client et mettez-les à niveau à l’aide de la commande de mise à niveau :</span><span class="sxs-lookup"><span data-stu-id="21aee-152">Get the eligible DLs in the tenant and upgrade them using the upgrade command:</span></span>

```
Get-EligibleDistributionGroupForMigration | Foreach-Object{
    Upgrade-DistributionGroup -DlIdentities $_.PrimarySMTPAddress
}
```

2. <span data-ttu-id="21aee-153">Obtenir la liste de toutes les listes de distribution et mettre à niveau uniquement les listes de distribution éligibles :</span><span class="sxs-lookup"><span data-stu-id="21aee-153">Get the list of all DLs and upgrade only the eligible DLs:</span></span>

```
Get-DistributionGroup| Foreach-Object{
    Upgrade-DistributionGroup -DlIdentities $_.PrimarySMTPAddress
}
```

## <a name="faq-about-upgrading-distribution-lists-to-microsoft-365-groups-in-outlook"></a><span data-ttu-id="21aee-154">Forum aux questions sur la mise à niveau des listes de distribution vers des groupes Microsoft 365 dans Outlook</span><span class="sxs-lookup"><span data-stu-id="21aee-154">FAQ about upgrading distribution lists to Microsoft 365 Groups in Outlook</span></span>

### <a name="which-distribution-lists-cannot-be-upgraded"></a><span data-ttu-id="21aee-155">Quelles listes de distribution ne peuvent pas être mises à niveau ?</span><span class="sxs-lookup"><span data-stu-id="21aee-155">Which distribution lists cannot be upgraded?</span></span>

<span data-ttu-id="21aee-156">Vous ne pouvez mettre à niveau que des listes de distribution non imbriquées gérées dans le Cloud, simples et non imbriquées.</span><span class="sxs-lookup"><span data-stu-id="21aee-156">You can only upgrade cloud-managed, simple, non-nested distribution lists.</span></span> <span data-ttu-id="21aee-157">Le tableau ci-dessous répertorie les listes de distribution qui **ne peuvent pas** être mises à niveau.</span><span class="sxs-lookup"><span data-stu-id="21aee-157">The table below lists distribution lists that **CANNOT** be upgraded.</span></span>

|<span data-ttu-id="21aee-158">**Property**</span><span class="sxs-lookup"><span data-stu-id="21aee-158">**Property**</span></span>|<span data-ttu-id="21aee-159">**Exclus?**</span><span class="sxs-lookup"><span data-stu-id="21aee-159">**Eligible?**</span></span>|
|:-----|:-----|
|<span data-ttu-id="21aee-160">Liste de distribution gérée locale.</span><span class="sxs-lookup"><span data-stu-id="21aee-160">On-premises managed distribution list.</span></span>  <br/> |<span data-ttu-id="21aee-161">Non</span><span class="sxs-lookup"><span data-stu-id="21aee-161">No</span></span>  <br/> |
|<span data-ttu-id="21aee-162">Listes de distribution imbriquées.</span><span class="sxs-lookup"><span data-stu-id="21aee-162">Nested distribution lists.</span></span> <span data-ttu-id="21aee-163">La liste de distribution a des groupes enfants ou est membre d’un autre groupe.</span><span class="sxs-lookup"><span data-stu-id="21aee-163">Distribution list either has child groups or is a member of another group.</span></span>  <br/> |<span data-ttu-id="21aee-164">Non</span><span class="sxs-lookup"><span data-stu-id="21aee-164">No</span></span>  <br/> |
|<span data-ttu-id="21aee-165">Listes de distribution avec des membres **RecipientTypeDetails** autres que **UserMailbox**, **SharedMailbox**, **TeamMailbox**, **MailUser**</span><span class="sxs-lookup"><span data-stu-id="21aee-165">Distribution lists with member **RecipientTypeDetails** other than **UserMailbox**, **SharedMailbox**, **TeamMailbox**, **MailUser**</span></span>  <br/> |<span data-ttu-id="21aee-166">Non</span><span class="sxs-lookup"><span data-stu-id="21aee-166">No</span></span>  <br/> |
|<span data-ttu-id="21aee-167">Liste de distribution contenant plus de 100 propriétaires</span><span class="sxs-lookup"><span data-stu-id="21aee-167">Distribution list which has more than 100 owners</span></span>  <br/> |<span data-ttu-id="21aee-168">Non</span><span class="sxs-lookup"><span data-stu-id="21aee-168">No</span></span>  <br/> |
|<span data-ttu-id="21aee-169">Liste de distribution qui ne possède que des membres mais pas de propriétaire</span><span class="sxs-lookup"><span data-stu-id="21aee-169">Distribution list which only has members but no owner</span></span>  <br/> |<span data-ttu-id="21aee-170">Non</span><span class="sxs-lookup"><span data-stu-id="21aee-170">No</span></span>  <br/> |
|<span data-ttu-id="21aee-171">Liste de distribution avec un alias contenant des caractères spéciaux</span><span class="sxs-lookup"><span data-stu-id="21aee-171">Distribution list which has alias containing special characters</span></span>  <br/> |<span data-ttu-id="21aee-172">Non</span><span class="sxs-lookup"><span data-stu-id="21aee-172">No</span></span>  <br/> |
|<span data-ttu-id="21aee-173">Si la liste de distribution est configurée pour être une adresse de transfert pour la boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="21aee-173">If the distribution list is configured to be a forwarding address for Shared Mailbox</span></span>  <br/> |<span data-ttu-id="21aee-174">Non</span><span class="sxs-lookup"><span data-stu-id="21aee-174">No</span></span>  <br/> |
|<span data-ttu-id="21aee-175">Si la LD fait partie de la restriction de l' **expéditeur** dans une autre DL.</span><span class="sxs-lookup"><span data-stu-id="21aee-175">If the DL is part of **Sender Restriction** in another DL.</span></span>  <br/> |<span data-ttu-id="21aee-176">Non</span><span class="sxs-lookup"><span data-stu-id="21aee-176">No</span></span>  <br/> |
|<span data-ttu-id="21aee-177">Groupes de sécurité</span><span class="sxs-lookup"><span data-stu-id="21aee-177">Security groups</span></span>  <br/> |<span data-ttu-id="21aee-178">Non</span><span class="sxs-lookup"><span data-stu-id="21aee-178">No</span></span>  <br/> |
|<span data-ttu-id="21aee-179">Listes de distribution dynamique</span><span class="sxs-lookup"><span data-stu-id="21aee-179">Dynamic Distribution lists</span></span>  <br/> |<span data-ttu-id="21aee-180">Non</span><span class="sxs-lookup"><span data-stu-id="21aee-180">No</span></span>  <br/> |
|<span data-ttu-id="21aee-181">Listes de distribution qui ont été converties en **RoomLists**</span><span class="sxs-lookup"><span data-stu-id="21aee-181">Distribution lists which were converted to **RoomLists**</span></span>  <br/> |<span data-ttu-id="21aee-182">Non</span><span class="sxs-lookup"><span data-stu-id="21aee-182">No</span></span>  <br/> |
|<span data-ttu-id="21aee-183">Listes de distribution où **MemberJoinRestriction** et/ou **MemberDepartRestriction** sont **fermés**</span><span class="sxs-lookup"><span data-stu-id="21aee-183">Distribution lists where **MemberJoinRestriction** and/or **MemberDepartRestriction** is **Closed**</span></span>  <br/> |<span data-ttu-id="21aee-184">Non</span><span class="sxs-lookup"><span data-stu-id="21aee-184">No</span></span>  <br/> |

### <a name="how-do-i-check-which-dls-are-eligible-for-upgrade"></a><span data-ttu-id="21aee-185">Comment puis-je vérifier quelles listes de distribution sont éligibles pour la mise à niveau ?</span><span class="sxs-lookup"><span data-stu-id="21aee-185">How do I check which DLs are eligible for upgrade?</span></span>

<span data-ttu-id="21aee-186">Si vous souhaitez vérifier si une LD est éligible ou non, vous pouvez exécuter la commande ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="21aee-186">If you want to check whether a DL is eligible or not, you can run the below command:</span></span>

`Get-DistributionGroup \<DL SMTP address\> | Get-EligibleDistributionGroupForMigration`

<span data-ttu-id="21aee-187">Si vous souhaitez vérifier quelles listes de distribution sont éligibles pour la mise à niveau, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="21aee-187">If you want to check which DLs are eligible for upgrade just run the following command:</span></span>

`Get-EligibleDistributionGroupForMigration`

### <a name="who-can-run-the-upgrade-scripts"></a><span data-ttu-id="21aee-188">Qui peut exécuter les scripts de mise à niveau ?</span><span class="sxs-lookup"><span data-stu-id="21aee-188">Who can run the upgrade scripts?</span></span>

<span data-ttu-id="21aee-189">Personnes disposant de droits d’administrateur général ou d’administrateur Exchange.</span><span class="sxs-lookup"><span data-stu-id="21aee-189">People with global admin or Exchange admin rights.</span></span>

### <a name="why-is-the-contact-card-still-showing-a-distribution-list-what-should-i-do-to-prevent-a-upgraded-distribution-list-from-showing-up-in-my-auto-suggest-list"></a><span data-ttu-id="21aee-190">Pourquoi la carte de visite affiche-t-elle toujours une liste de distribution ?</span><span class="sxs-lookup"><span data-stu-id="21aee-190">Why is the contact card still showing a distribution list?</span></span> <span data-ttu-id="21aee-191">Que dois-je faire pour empêcher qu’une liste de distribution mise à niveau ne s’affiche dans ma liste de suggestions automatiques ?</span><span class="sxs-lookup"><span data-stu-id="21aee-191">What should I do to prevent a upgraded distribution list from showing up in my auto suggest list?</span></span>

- <span data-ttu-id="21aee-192">Pour Outlook : lorsqu’une personne tente d’envoyer un courrier électronique dans Outlook en tapant le nom du groupe Microsoft 365 après la migration, le destinataire est résolu en tant que liste de distribution au lieu du groupe.</span><span class="sxs-lookup"><span data-stu-id="21aee-192">For Outlook: When someone tries to send an email in Outlook by typing the Microsoft 365 group name after migration, the recipient will be resolved as the distribution list instead of the group.</span></span> <span data-ttu-id="21aee-193">La carte de visite du destinataire est la carte de visite des listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="21aee-193">The contact card of the recipient will be the distribution lists contact card.</span></span> <span data-ttu-id="21aee-194">Cela est dû au cache de destinataires ou au cache de noms Nick dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="21aee-194">This is because of the recipient cache or nick name cache in Outlook.</span></span> <span data-ttu-id="21aee-195">Le message électronique est envoyé au groupe, mais risque de confusion pour l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="21aee-195">The email will be sent successfully to the group, but might cause confusion to the sender.</span></span><br/><span data-ttu-id="21aee-196">Vous pouvez effectuer les étapes de cette rubrique, des [informations sur la liste de saisie semi-automatique Outlook](https://go.microsoft.com/fwlink/?LinkID=798736) pour réinitialiser le cache, ce qui permet de résoudre ce problème.</span><span class="sxs-lookup"><span data-stu-id="21aee-196">You can perform the steps in this topic, [Information about the Outlook AutoComplete list](https://go.microsoft.com/fwlink/?LinkID=798736) to reset the cache, which will fix this issue.</span></span>

- <span data-ttu-id="21aee-197">Pour Outlook sur le Web : dans le cas d’Outlook sur le Web, le destinataire de la liste de distribution restera dans le cache.</span><span class="sxs-lookup"><span data-stu-id="21aee-197">For Outlook on the web: In case of Outlook on the web, the distribution list recipient will still remain in the cache.</span></span> <span data-ttu-id="21aee-198">Vous pouvez suivre les étapes de la section [supprimer le nom suggéré ou l’adresse de messagerie de la liste de saisie semi-automatique](https://support.office.com/article/9E1419D9-E88F-445B-B07F-F558B8A37C58.aspx) pour actualiser le cache pour afficher la carte de visite du groupe.</span><span class="sxs-lookup"><span data-stu-id="21aee-198">You can follow the steps in [Remove suggested name or email address from the Auto-Complete List](https://support.office.com/article/9E1419D9-E88F-445B-B07F-F558B8A37C58.aspx) to refresh the cache to see the group contact card.</span></span>

### <a name="do-new-group-members-get-a-welcome-email-in-their-inbox"></a><span data-ttu-id="21aee-199">Les nouveaux membres du groupe reçoivent-ils un message électronique de bienvenue dans leur boîte de réception ?</span><span class="sxs-lookup"><span data-stu-id="21aee-199">Do new group members get a welcome email in their inbox?</span></span>

<span data-ttu-id="21aee-200">Non.</span><span class="sxs-lookup"><span data-stu-id="21aee-200">No.</span></span> <span data-ttu-id="21aee-201">Le paramètre permettant d’activer les messages de bienvenue est défini sur false par défaut.</span><span class="sxs-lookup"><span data-stu-id="21aee-201">The setting to enable welcome messages is set to false by default.</span></span> <span data-ttu-id="21aee-202">Ce paramètre affecte les membres de groupe existants et nouveaux qui peuvent rejoindre une fois la migration terminée.</span><span class="sxs-lookup"><span data-stu-id="21aee-202">This setting affects both existing and new group members who may join after the migration is complete.</span></span> <span data-ttu-id="21aee-203">Si le propriétaire du groupe peut par la suite autoriser les utilisateurs invités, les utilisateurs invités ne reçoivent pas de courrier de bienvenue dans leur boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="21aee-203">If the group owner later allows guest users, guest users won't receive a welcome email in their inbox.</span></span> <span data-ttu-id="21aee-204">Les membres invités peuvent continuer à travailler avec le groupe.</span><span class="sxs-lookup"><span data-stu-id="21aee-204">Guest members can continue working with the group.</span></span>

### <a name="what-if-one-or-some-of-the-dls-are-not-upgraded"></a><span data-ttu-id="21aee-205">Que se passe-t-il si une ou plusieurs listes de distribution ne sont pas mises à niveau ?</span><span class="sxs-lookup"><span data-stu-id="21aee-205">What if one or some of the DLs are not upgraded?</span></span>

<span data-ttu-id="21aee-206">Dans certains cas, si DL est éligible mais n’a pas pu être mis à niveau.</span><span class="sxs-lookup"><span data-stu-id="21aee-206">There are some cases in which though DL is eligible but could not be upgraded.</span></span> <span data-ttu-id="21aee-207">La LD ne peut pas être mise à niveau et reste en tant que DL.</span><span class="sxs-lookup"><span data-stu-id="21aee-207">The DL does not get upgraded and remains as a DL.</span></span>

- <span data-ttu-id="21aee-208">Où l’administrateur a appliqué la **stratégie d’adresse de messagerie de groupe** pour les groupes au sein d’une organisation et tente de mettre à niveau les listes de distribution qui ne répondent pas aux critères, la DL ne bénéficie pas de la mise à niveau</span><span class="sxs-lookup"><span data-stu-id="21aee-208">Where admin has applied **Group Email Address Policy** for the groups in an organization and they try to upgrade DLs which doesn't fulfill the criteria, the DL does not get upgraded</span></span>

- <span data-ttu-id="21aee-209">Les listes de distribution avec **MemberJoinRestriction** ou **MemberDepartRestriction** définies sur **fermé**n’ont pas pu être mises à niveau</span><span class="sxs-lookup"><span data-stu-id="21aee-209">DLs with **MemberJoinRestriction** or **MemberDepartRestriction** set to **Closed**, could not be upgraded</span></span>

### <a name="what-happens-to-the-dl-if-the-upgrade-from-eac-fails"></a><span data-ttu-id="21aee-210">Qu’arrive-t-il à la DL si la mise à niveau à partir de l’erreur de l’administration Exchange</span><span class="sxs-lookup"><span data-stu-id="21aee-210">What happens to the DL if the upgrade from EAC fails?</span></span>

<span data-ttu-id="21aee-211">La mise à niveau se produit uniquement lorsque l’appel est envoyé au serveur.</span><span class="sxs-lookup"><span data-stu-id="21aee-211">The upgrade will happen only when the call is submitted to the server.</span></span> <span data-ttu-id="21aee-212">Si la mise à niveau échoue, vos listes de distribution seront intactes.</span><span class="sxs-lookup"><span data-stu-id="21aee-212">If the upgrade fails, your DLs will be intact.</span></span> <span data-ttu-id="21aee-213">Ils fonctionneront comme s’ils utilisaient.</span><span class="sxs-lookup"><span data-stu-id="21aee-213">They will work like they used to.</span></span>


