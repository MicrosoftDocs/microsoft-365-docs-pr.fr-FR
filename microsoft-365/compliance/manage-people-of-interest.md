---
title: Gérer les personnes concernées par les enquêtes de données (aperçu)
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Découvrez comment gérer les personnes intéressantes pour l’étendue de votre recherche ou afficher des informations telles que les journaux de contact, d’emplacement et d’activité.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: 85f6bdbe7a0602f8ce0038a4aca912896d5c2079
ms.sourcegitcommit: 6501e01a9ab131205a3eef910e6cea7f65b3f010
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/30/2020
ms.locfileid: "46528170"
---
# <a name="manage-people-of-interest-in-data-investigations-preview"></a><span data-ttu-id="4573c-103">Gérer les personnes concernées par les enquêtes de données (aperçu)</span><span class="sxs-lookup"><span data-stu-id="4573c-103">Manage people of interest in Data Investigations (Preview)</span></span>

<span data-ttu-id="4573c-104">Les enquêtes sur les données impliquent souvent des personnes intéressantes.</span><span class="sxs-lookup"><span data-stu-id="4573c-104">Data investigations often involve people of interest.</span></span> <span data-ttu-id="4573c-105">En règle générale, il s’agit de personnes qui possèdent les données déplacées, sensibles ou malveillantes que vous recherchez ou qui cherchent à corriger.</span><span class="sxs-lookup"><span data-stu-id="4573c-105">Usually they are people who own the misplaced, sensitive, or malicious data that you're investigating or looking to remediate.</span></span> <span data-ttu-id="4573c-106">Dans les **enquêtes de données (** préversion), vous pouvez les ajouter pour découvrir les sources de données à utiliser pour la portée de votre recherche ou afficher des informations supplémentaires telles que les journaux de contact, d’emplacement et d’activité.</span><span class="sxs-lookup"><span data-stu-id="4573c-106">In **Data Investigations (Preview)**, you can add them to discover their data sources to use in scoping your search or view additional information such as contact, location, and activity logs.</span></span> 


## <a name="add-people-of-interest"></a><span data-ttu-id="4573c-107">Ajouter des personnes intéressantes</span><span class="sxs-lookup"><span data-stu-id="4573c-107">Add people of interest</span></span>

<span data-ttu-id="4573c-108">Dans l’onglet **personnes** , vous pouvez ajouter des personnes intéressantes et découvrir leurs sources de données telles que les boîtes aux lettres Exchange ou le site OneDrive entreprise que vous pouvez utiliser pour étendre votre recherche.</span><span class="sxs-lookup"><span data-stu-id="4573c-108">In **People of interest** tab, you can add people of interest and discover their data sources such as Exchange mailboxes or OneDrive for Business site that you can use to scope your search.</span></span> <span data-ttu-id="4573c-109">Lorsqu’elles sont délimitées par des personnes intéressantes, les recherches sont plus performantes et précises car l’outil rétraite les données non indexées telles que les images ou les types de fichiers non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4573c-109">When scoped down by people of interest, searches are more performant and accurate because the tool reprocesses any unindexed data such as images or unsupported file types.</span></span> <span data-ttu-id="4573c-110">Vous pouvez également consulter les informations de contact, les informations d’emplacement et les journaux d’activité que vous pouvez utiliser pour initier des communications ou approfondir leurs activités.</span><span class="sxs-lookup"><span data-stu-id="4573c-110">You can also see their contact information, location information and activity logs that you can use to initiate communications or further investigate their activities.</span></span> 

<span data-ttu-id="4573c-111">Pour ajouter des personnes intéressantes à une enquête :</span><span class="sxs-lookup"><span data-stu-id="4573c-111">To add people of interest to an investigation:</span></span>

1. <span data-ttu-id="4573c-112">À partir de la page **enquêtes de données (aperçu)** , accédez à votre enquête.</span><span class="sxs-lookup"><span data-stu-id="4573c-112">From the **Data Investigations (Preview)** page, go to your investigation.</span></span>
 
2. <span data-ttu-id="4573c-113">Une fois que vous avez sélectionné une enquête, accédez à l’onglet **personnes d’intérêt** et cliquez sur **+ Ajouter des personnes intéressantes**.</span><span class="sxs-lookup"><span data-stu-id="4573c-113">After you have selected an investigation, go to the **People of interest** tab and click **+ Add people of interest**.</span></span> 
 
3. <span data-ttu-id="4573c-114">Choisissez les personnes que vous souhaitez ajouter à l’enquête.</span><span class="sxs-lookup"><span data-stu-id="4573c-114">Choose people that you want to add to the investigation.</span></span> <span data-ttu-id="4573c-115">Vous pouvez commencer par taper pour rechercher et sélectionner les utilisateurs dans Azure Active Directory de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4573c-115">You can start by typing to search and select the users from your organization's Azure Active Directory.</span></span>
 
4. <span data-ttu-id="4573c-116">Une fois que vous avez finalisé la liste des personnes intéressantes, cliquez sur **suivant** pour mapper leurs sources de données.</span><span class="sxs-lookup"><span data-stu-id="4573c-116">After you have finalized the list of people of interest, click **Next** to map their data sources.</span></span> 

5. <span data-ttu-id="4573c-117">Module Pour chaque personne, sélectionnez **Exchange** pour ajouter la boîte aux lettres Exchange principale de la personne et **onedrive** pour ajouter le site onedrive entreprise principal de la personne.</span><span class="sxs-lookup"><span data-stu-id="4573c-117">[Optional] For each person, select **Exchange** to add person's primary Exchange mailbox, and **OneDrive** to add person's primary OneDrive for Business site.</span></span>

6. <span data-ttu-id="4573c-118">Module Cliquez sur **suivant** pour ajouter d’autres sources de données que vous souhaitez associer à vos personnes intéressantes.</span><span class="sxs-lookup"><span data-stu-id="4573c-118">[Optional] Click **Next** to add any additional data sources that you want to associate with your people of interest.</span></span>

7. <span data-ttu-id="4573c-119">Module Sélectionnez **mettre à jour** pour affecter des emplacements de contenu, comme des boîtes aux lettres, des sites et des équipes à une personne.</span><span class="sxs-lookup"><span data-stu-id="4573c-119">[Optional] Select **Update** to assign content locations, like mailboxes, sites, and Teams to a person.</span></span> 

8. <span data-ttu-id="4573c-120">Module Dans le menu volant :</span><span class="sxs-lookup"><span data-stu-id="4573c-120">[Optional] In the flyout:</span></span>
   
    -  <span data-ttu-id="4573c-121">**Boîtes aux lettres Exchange** : cliquez sur **choisir les utilisateurs, les groupes ou les équipes** , puis cliquez à nouveau sur **choisir les utilisateurs, les groupes ou les équipes** .</span><span class="sxs-lookup"><span data-stu-id="4573c-121">**Exchange Mailboxes** - Click **Choose users, groups, or Teams** and then click **Choose users, groups, or teams** again.</span></span> <span data-ttu-id="4573c-122">Pour ajouter d’autres boîtes aux lettres, utilisez la zone de recherche pour rechercher des boîtes aux lettres utilisateur et des groupes de distribution.</span><span class="sxs-lookup"><span data-stu-id="4573c-122">To add more mailboxes, use the search box to find user mailboxes and distribution groups.</span></span> <span data-ttu-id="4573c-123">Vous pouvez également ajouter des boîtes aux lettres utilisées pour stocker un groupe Microsoft 365 ou des informations d’équipe Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4573c-123">You can also add mailboxes used to store a Microsoft 365 Group or a Microsoft Team information.</span></span> <span data-ttu-id="4573c-124">Activez la case à cocher utilisateur, groupe, équipe, cliquez sur **choisir**, puis sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="4573c-124">Select the user, group, team check box, click **Choose**, and then click **Done**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="4573c-125">Lorsque vous cliquez sur choisir les utilisateurs, les groupes ou les équipes pour spécifier des boîtes aux lettres, le sélecteur de boîtes aux lettres affiché est vide.</span><span class="sxs-lookup"><span data-stu-id="4573c-125">When you click Choose users, groups, or teams to specify mailboxes, the mailbox picker that's displayed is empty.</span></span> <span data-ttu-id="4573c-126">Il s’agit d’une conception qui améliore les performances.</span><span class="sxs-lookup"><span data-stu-id="4573c-126">This is by design to enhance performance.</span></span> <span data-ttu-id="4573c-127">Pour ajouter des personnes à cette liste, tapez un nom (un minimum de 3 caractères) dans la zone de recherche.</span><span class="sxs-lookup"><span data-stu-id="4573c-127">To add people to this list, type a name (a minimum of 3 characters) in the search box.</span></span>
     
     - <span data-ttu-id="4573c-128">**Sites SharePoint** : cliquez sur **choisir des sites** , puis cliquez à nouveau sur choisir les **sites** pour spécifier d’autres sites SharePoint et OneDrive entreprise que vous souhaitez ajouter à une personne.</span><span class="sxs-lookup"><span data-stu-id="4573c-128">**SharePoint Sites** - Click **Choose sites** and then click **Choose sites** again to specify additional SharePoint and OneDrive for Business sites that you want to add to a person.</span></span> <span data-ttu-id="4573c-129">Vous pouvez également ajouter l’URL du site SharePoint pour un groupe Microsoft 365 ou une équipe Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4573c-129">You can also add the URL for the SharePoint site for a Microsoft 365 Group or a Microsoft Team.</span></span> <span data-ttu-id="4573c-130">Tapez l’URL de chaque site que vous souhaitez attribuer.</span><span class="sxs-lookup"><span data-stu-id="4573c-130">Type the URL for each site that you want to assign.</span></span> <span data-ttu-id="4573c-131">Cliquez sur **choisir**, puis sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="4573c-131">Click **Choose**, and then click **Done**.</span></span>
     - <span data-ttu-id="4573c-132">**Microsoft** teams – cliquez sur **choisir teams** , puis cliquez sur **choisir les équipes** pour afficher la liste des groupes d’équipes Microsoft dont la personne est aujourd’hui membre.</span><span class="sxs-lookup"><span data-stu-id="4573c-132">**Microsoft Teams** – Click **Choose Teams** and then click **Choose Teams** again to view a list of Microsoft Team groups that the person is a member of today.</span></span> <span data-ttu-id="4573c-133">Sélectionnez les équipes que vous souhaitez ajouter à la personne.</span><span class="sxs-lookup"><span data-stu-id="4573c-133">Select the Teams that you want to add to the person.</span></span> <span data-ttu-id="4573c-134">Une fois sélectionné, le système identifie automatiquement & sélectionnez le site SharePoint et la boîte aux lettres de groupe associés associés à cette équipe Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4573c-134">Once selected, the system will automatically identify & select the associated SharePoint site and Group Mailbox associated to that Microsoft Team.</span></span> <span data-ttu-id="4573c-135">Cliquez sur **choisir**, puis sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="4573c-135">Click **Choose**, and then click **Done**.</span></span>
        
      > [!NOTE]
      > <span data-ttu-id="4573c-136">Pour ajouter des Microsoft teams supplémentaires, vous devez ajouter séparément la boîte aux lettres et le site SharePoint, comme indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="4573c-136">To add additional Microsoft Teams, you will need to separately add the mailbox and SharePoint site as shown above.</span></span>

<span data-ttu-id="4573c-137">Une fois que vous avez terminé le mappage des sources de données aux personnes intéressantes, vous pouvez voir le résumé du nombre total de boîtes aux lettres, de sites et d’équipes que vous venez d’ajouter.</span><span class="sxs-lookup"><span data-stu-id="4573c-137">After you have finished mapping data sources to people of interest, you can see the summary of total mailboxes, sites, and Teams that you just added.</span></span> <span data-ttu-id="4573c-138">Si vous mappez des sources de données supplémentaires à des personnes intéressantes et que votre recherche par des personnes intéressantes, le mappage des documents à des personnes d’intérêt persiste tout au long de l’enquête, ce qui facilite l’Organisation des preuves ou la génération d’un rapport par des personnes intéressantes.</span><span class="sxs-lookup"><span data-stu-id="4573c-138">If you map any additional data sources to people of interest and scope your search by people of interest, the mapping of document to people of interest persist throughout the investigation, making it easier to organize evidence or generate report by people of interest.</span></span> 

## <a name="view-additional-people-of-interest-information"></a><span data-ttu-id="4573c-139">Afficher des informations supplémentaires sur les personnes concernées</span><span class="sxs-lookup"><span data-stu-id="4573c-139">View additional people of interest information</span></span>

<span data-ttu-id="4573c-140">Dans l’onglet **personnes** , cliquez sur une personne que vous avez ajoutée.</span><span class="sxs-lookup"><span data-stu-id="4573c-140">In **People of interest** tab, click on a person that you added.</span></span> <span data-ttu-id="4573c-141">Dans un menu volant, vous verrez :</span><span class="sxs-lookup"><span data-stu-id="4573c-141">In a flyout, you'll see:</span></span>

- <span data-ttu-id="4573c-142">Informations de contact</span><span class="sxs-lookup"><span data-stu-id="4573c-142">Contact information</span></span>

  - <span data-ttu-id="4573c-143">**Nom d’affichage**: nom de la personne affiché dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="4573c-143">**Display Name**: The person's name displayed in the address book.</span></span> <span data-ttu-id="4573c-144">Il s’agit généralement de la combinaison du prénom, de l’initiale du deuxième prénom et du nom de famille.</span><span class="sxs-lookup"><span data-stu-id="4573c-144">This is usually the combination of first name, middle initial, and last name.</span></span>
  - <span data-ttu-id="4573c-145">**Mail/SMTP**: adresse SMTP de la personne, par exemple, Jeff@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="4573c-145">**Mail/SMTP**: The SMTP address of the person, for example, jeff@contoso.onmicrosoft.com.</span></span>  
  - <span data-ttu-id="4573c-146">**Titre**: fonction.</span><span class="sxs-lookup"><span data-stu-id="4573c-146">**Title**: Job title.</span></span>
  - <span data-ttu-id="4573c-147">**Department**: nom du service dans lequel la personne travaille.</span><span class="sxs-lookup"><span data-stu-id="4573c-147">**Department**: The name of the department in which the person works.</span></span>
  - <span data-ttu-id="4573c-148">**Responsable**: le responsable de la personne.</span><span class="sxs-lookup"><span data-stu-id="4573c-148">**Manager**: The person's manager.</span></span> <span data-ttu-id="4573c-149">Le responsable reçoit les communications d’escalade de cette personne.</span><span class="sxs-lookup"><span data-stu-id="4573c-149">Manager receives any escalation communications for this person.</span></span>
  
- <span data-ttu-id="4573c-150">Informations d’emplacement</span><span class="sxs-lookup"><span data-stu-id="4573c-150">Location information</span></span>

  - <span data-ttu-id="4573c-151">**Ville**: ville dans laquelle se trouve la personne.</span><span class="sxs-lookup"><span data-stu-id="4573c-151">**City**: The city in which the person is located.</span></span>
  - <span data-ttu-id="4573c-152">**État**: département ou région où se trouve la personne.</span><span class="sxs-lookup"><span data-stu-id="4573c-152">**State**: The state or province in which the person is located.</span></span>
  - <span data-ttu-id="4573c-153">**Pays/région**: pays/région où se trouve la personne ; par exemple, « US » ou « UK ».</span><span class="sxs-lookup"><span data-stu-id="4573c-153">**Country/Region**: The country/region in which the person is located; for example, "US" or "UK".</span></span>
  - <span data-ttu-id="4573c-154">**Office**: l’emplacement du Bureau de la personne.</span><span class="sxs-lookup"><span data-stu-id="4573c-154">**Office**: The office location of the person.</span></span>

- <span data-ttu-id="4573c-155">État de traitement</span><span class="sxs-lookup"><span data-stu-id="4573c-155">Processing status</span></span>

  - <span data-ttu-id="4573c-156">**État**de l’indexation : état de l’indexation profonde des sources de données</span><span class="sxs-lookup"><span data-stu-id="4573c-156">**Indexing status**: Status of deep indexing the data sources</span></span>
  - <span data-ttu-id="4573c-157">**Indexation de la dernière heure de mise à jour**: horodatage du dernier déclenchement du travail d’indexation approfondie.</span><span class="sxs-lookup"><span data-stu-id="4573c-157">**Indexing Last Updated Time**: Timestamp of when the deep indexing job was last triggered.</span></span>
  - <span data-ttu-id="4573c-158">**Sources de données**: affiche le nombre de boîtes aux lettres, de sites et d’équipes mappées à la personne</span><span class="sxs-lookup"><span data-stu-id="4573c-158">**Data sources**: Shows the count of mailboxes, sites, and Teams mapped to the person</span></span>

- <span data-ttu-id="4573c-159">Mettre à jour l’index</span><span class="sxs-lookup"><span data-stu-id="4573c-159">Update index</span></span>
    - <span data-ttu-id="4573c-160">Vous pouvez réindexer les sources de données de cette personne.</span><span class="sxs-lookup"><span data-stu-id="4573c-160">You can reindex this person's data sources.</span></span> 

- <span data-ttu-id="4573c-161">Afficher l’activité</span><span class="sxs-lookup"><span data-stu-id="4573c-161">View activity</span></span> 

    - <span data-ttu-id="4573c-162">Vous pouvez afficher et rechercher les journaux d’activité de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4573c-162">You can view and search user's activity logs.</span></span> <span data-ttu-id="4573c-163">Pour plus d’informations, consultez la rubrique [View People of Interest Activity](view-people-of-interest-activity.md) .</span><span class="sxs-lookup"><span data-stu-id="4573c-163">For more information, see [View people of interest activity](view-people-of-interest-activity.md)</span></span> 
