---
title: Utiliser le contrôle de version des enregistrements pour mettre à jour les enregistrements stockés dans SharePoint ou OneDrive
f1.keywords:
- NOCSH
ms.author: cabailey
author: cabailey
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
- SPO_Content
search.appverid:
- MOE150
- MET150
description: Découvrir les enregistrements pour vous aider à implémenter une solution de gestion des enregistrements dans Microsoft 365.
ms.openlocfilehash: 943bf3949ab57eb4603695495d7a8ca0c4b90db7
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46695243"
---
# <a name="use-record-versioning-to-update-records-stored-in-sharepoint-or-onedrive"></a><span data-ttu-id="269ec-103">Utiliser le contrôle de version des enregistrements pour mettre à jour les enregistrements stockés dans SharePoint ou OneDrive</span><span class="sxs-lookup"><span data-stu-id="269ec-103">Use record versioning to update records stored in SharePoint or OneDrive</span></span>

><span data-ttu-id="269ec-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](https://aka.ms/ComplianceSD).*</span><span class="sxs-lookup"><span data-stu-id="269ec-104">*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*</span></span>

<span data-ttu-id="269ec-105">La possibilité de marquer un document en tant qu’[enregistrement](records.md) et de restreindre les actions pouvant être effectuées sur l’enregistrement constitue un objectif essentiel pour toute solution de gestion d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="269ec-105">The ability to mark a document as a [record](records.md) and restrict actions that can be performed on the record is an essential goal for any records management solution.</span></span> <span data-ttu-id="269ec-106">Cependant, une collaboration peut également être nécessaire pour permettre aux utilisateurs de créer des versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="269ec-106">However, collaboration might also be needed for people to create subsequent versions.</span></span>

<span data-ttu-id="269ec-107">Par exemple, il peut arriver que vous marquiez un contrat de vente sous forme d’un enregistrement, mais qu’ensuite vous deviez mettre à jour le contrat avec de nouvelles conditions et marquer la dernière version comme nouvel enregistrement tout en conservant la version précédente de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="269ec-107">For example, you might mark a sales contract as a record, but then need to update the contract with new terms and mark the latest version as a new record while still retaining the previous record version.</span></span> <span data-ttu-id="269ec-108">Pour ces types de scénarios, SharePoint et OneDrive Entreprise prennent désormais en charge le *contrôle de version d’enregistrement*.</span><span class="sxs-lookup"><span data-stu-id="269ec-108">For these types of scenarios, SharePoint and OneDrive support *record versioning*.</span></span> <span data-ttu-id="269ec-109">Les dossiers de bloc-notes OneNote ne prennent pas en charge le contrôle de version d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="269ec-109">OneNote notebook folders don't support record versioning.</span></span>

<span data-ttu-id="269ec-110">Pour utiliser le contrôle de version d’un enregistrement, commencez par [étiqueter le document et marquez-le en tant qu’enregistrement](declare-records.md).</span><span class="sxs-lookup"><span data-stu-id="269ec-110">To use record versioning, you first [label the document and mark it as a record](declare-records.md).</span></span> <span data-ttu-id="269ec-111">À ce stade, une propriété de document appelée *Statut de l’enregistrement* s’affiche en regard de l’étiquette de rétention, et le statut de l’enregistrement initial est **Verrouillé**.</span><span class="sxs-lookup"><span data-stu-id="269ec-111">At this point, a document property, called *Record status* is displayed next to the retention label, and the initial record status is **Locked**.</span></span> 

<span data-ttu-id="269ec-112">Vous pouvez effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="269ec-112">You can now do the following things:</span></span>

  - <span data-ttu-id="269ec-113">**Modifier sans limites et conserver les versions individuelles du document en tant qu’enregistrements en déverrouillant et verrouillant la propriété Statut de l’enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="269ec-113">**Continually edit and retain individual versions of the document as records, by unlocking and locking the Record status property.**</span></span> <span data-ttu-id="269ec-114">Une nouvelle version de l’enregistrement est uniquement conservée lorsque la propriété **État de l’enregistrement** est définie sur **Verrouillée**.</span><span class="sxs-lookup"><span data-stu-id="269ec-114">Only when the **Record status** property is set to **Locked** is a new version of the record retained.</span></span> <span data-ttu-id="269ec-115">Ce bouton bascule activé/désactivé permet de réduire le risque de conserver des versions et des copies du document superflues.</span><span class="sxs-lookup"><span data-stu-id="269ec-115">This toggle of locked and unlocked reduces the risk of retaining unnecessary versions and copies of the document.</span></span>

  - <span data-ttu-id="269ec-116">**Stockez automatiquement les enregistrements dans un référentiel d’enregistrements situé localement au sein de la collection de sites.**</span><span class="sxs-lookup"><span data-stu-id="269ec-116">**Have the records automatically stored in an in-place records repository located within the site collection.**</span></span> <span data-ttu-id="269ec-117">Chaque collection de sites dans SharePoint et OneDrive conserve le contenu dans la bibliothèque de conservation et de préservation.</span><span class="sxs-lookup"><span data-stu-id="269ec-117">Each site collection in SharePoint and OneDrive preserves content in its Preservation Hold library.</span></span> <span data-ttu-id="269ec-118">Les versions des enregistrements sont stockées dans le dossier Enregistrements de cette bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="269ec-118">Record versions are stored in the Records folder in this library.</span></span>

  - <span data-ttu-id="269ec-119">**Tenez à jour un document évolutif contenant toutes les versions.**</span><span class="sxs-lookup"><span data-stu-id="269ec-119">**Maintain an evergreen document that contains all versions.**</span></span> <span data-ttu-id="269ec-120">Par défaut, un historique des versions est disponible dans le menu élément pour chaque document SharePoint et OneDrive.</span><span class="sxs-lookup"><span data-stu-id="269ec-120">By default, each SharePoint and OneDrive document has a version history available on the item menu.</span></span> <span data-ttu-id="269ec-121">Dans cet historique des versions, vous pouvez facilement identifier quelles versions sont des enregistrements et afficher ces documents.</span><span class="sxs-lookup"><span data-stu-id="269ec-121">In this version history, you can easily see which versions are records and view those documents.</span></span>

<span data-ttu-id="269ec-122">Le contrôle de version d’enregistrement est disponible automatiquement pour tout document comportant une étiquette de rétention qui marque l’élément comme enregistrement.</span><span class="sxs-lookup"><span data-stu-id="269ec-122">Record versioning is automatically available for any document that has a retention label that marks the item as a record.</span></span> <span data-ttu-id="269ec-123">Lorsqu’un utilisateur affiche les propriétés du document à l’aide du volet Détails, il peut basculer le **Statut de l’enregistrement** de **Verrouillé** vers **Déverrouillé**.</span><span class="sxs-lookup"><span data-stu-id="269ec-123">When a user views the document properties by using the details pane, they can toggle the **Record status** from **Locked** to **Unlocked**.</span></span> <span data-ttu-id="269ec-124">Cette action crée un enregistrement dans le dossier Enregistrements de la bibliothèque de conservation et de préservation, où il résidera jusqu’à la fin de la période de rétention.</span><span class="sxs-lookup"><span data-stu-id="269ec-124">This action creates a record in the Records folder in the Preservation Hold library, where it resides for the remainder of its retention period.</span></span> 

<span data-ttu-id="269ec-125">Lorsque le document est déverrouillé, les utilisateurs disposant des autorisations de modification standard peuvent modifier le fichier.</span><span class="sxs-lookup"><span data-stu-id="269ec-125">While the document is unlocked, any user with standard edit permissions can edit the file.</span></span> <span data-ttu-id="269ec-126">Toutefois, les utilisateurs ne peuvent pas supprimer le fichier, car il est encore considéré comme un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="269ec-126">However, users can't delete the file, because it's still a record.</span></span> <span data-ttu-id="269ec-127">Lorsque la modification est terminée, un utilisateur peut basculer vers la bascule de l’**État de l’enregistrement** de **Déverrouillé** vers **Verrouillé**, ce qui empêche les modifications ultérieures dans ce statut.</span><span class="sxs-lookup"><span data-stu-id="269ec-127">When editing is complete, a  user can then toggle the **Record status** from **Unlocked** to **Locked**, which prevents further edits while in this status.</span></span>
<br/><br/>

![Propriété statut de l’enregistrement sur le document marqué en tant qu’enregistrement](../media/recordversioning8.png)

## <a name="locking-and-unlocking-a-record"></a><span data-ttu-id="269ec-129">Verrouillage et déverrouillage d'un enregistrement</span><span class="sxs-lookup"><span data-stu-id="269ec-129">Locking and unlocking a record</span></span>

<span data-ttu-id="269ec-130">Lorsqu’une étiquette de rétention qui marque le contenu en tant qu’enregistrement est appliquée à un document, tous les utilisateurs ayant des autorisations de collaboration ou un niveau d'autorisation plus réduit peuvent déverrouiller un enregistrement ou verrouiller un enregistrement déverrouillé.</span><span class="sxs-lookup"><span data-stu-id="269ec-130">After a retention label that marks content as a record is applied to a document, any user with Contribute permissions or a narrower permission level can unlock a record or lock an unlocked record.</span></span>
<br/><br/>

![Le statut de l’enregistrement indique que le document enregistré est déverrouillé](../media/recordversioning9.png)

<span data-ttu-id="269ec-132">Lorsqu’un utilisateur déverrouille un enregistrement, il se produit les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="269ec-132">When a user unlocks a record, the following actions occur:</span></span>

1. <span data-ttu-id="269ec-133">Si la collection de sites actuelle ne possède pas de bibliothèque de conservation et de préservation, une bibliothèque est créée.</span><span class="sxs-lookup"><span data-stu-id="269ec-133">If the current site collection doesn't have a Preservation Hold library, one is created.</span></span>

2. <span data-ttu-id="269ec-134">Si la bibliothèque de conservation et de préservation ne possède pas de dossier Enregistrements, un dossier est créé.</span><span class="sxs-lookup"><span data-stu-id="269ec-134">If the Preservation Hold library doesn't have a Records folder, one is created.</span></span>

3. <span data-ttu-id="269ec-135">Une action **Copier vers** copie la dernière version du document dans le dossier Enregistrements.</span><span class="sxs-lookup"><span data-stu-id="269ec-135">A **Copy to** action copies the latest version of the document to the Records folder.</span></span> <span data-ttu-id="269ec-136">L’action **Copier vers** inclut uniquement la dernière version et aucune version antérieure.</span><span class="sxs-lookup"><span data-stu-id="269ec-136">The **Copy to** action includes only the latest version and no prior versions.</span></span> <span data-ttu-id="269ec-137">Ce document copié est désormais considéré comme une version d’enregistrement du document et son nom de fichier présente le format suivant : \[Titre GUID Version\#\]</span><span class="sxs-lookup"><span data-stu-id="269ec-137">This copied document is now considered a record version of the document, and its file name has the format: \[Title GUID Version\#\]</span></span>

4. <span data-ttu-id="269ec-138">La copie créée dans le dossier Enregistrements est ajoutée à l’historique des versions du document d’origine et cette version affiche le mot **Enregistrement** dans le champ commentaires.</span><span class="sxs-lookup"><span data-stu-id="269ec-138">The copy created in the Records folder is added to the version history of the original document, and this version shows the word **Record** in the comments field.</span></span>

5. <span data-ttu-id="269ec-139">Le document d’origine est une nouvelle version qui peut être modifiée, mais pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="269ec-139">The original document is a new version that can be edited, but not deleted.</span></span> <span data-ttu-id="269ec-140">La colonne bibliothèque de documents **L’Élément est un Enregistrement** affiche toujours la valeur **Oui** parce que le document est encore considéré comme un enregistrement, même s’il peut désormais être modifié.</span><span class="sxs-lookup"><span data-stu-id="269ec-140">The document library column **Item is a Record** still shows the **Yes** value because the document is still a record, even if it can now be edited.</span></span>

<span data-ttu-id="269ec-141">Lorsqu’un utilisateur verrouille un enregistrement, le document d’origine ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="269ec-141">When a user locks a record, the original document again can't be edited.</span></span> <span data-ttu-id="269ec-142">Mais c’est l’action de déverrouiller un enregistrement qui copie une version dans le dossier Enregistrements de la bibliothèque de conservation et de préservation.</span><span class="sxs-lookup"><span data-stu-id="269ec-142">But it is the action of unlocking a record that copies a version to the Records folder in the Preservation Hold library.</span></span>

## <a name="record-versions"></a><span data-ttu-id="269ec-143">Versions d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="269ec-143">Record versions</span></span>

<span data-ttu-id="269ec-144">Chaque fois qu’un utilisateur déverrouille un enregistrement, la version la plus récente est copiée dans le dossier Enregistrements de la bibliothèque de conservation et de préservation et cette version contient la valeur **Enregistrement** dans le champ **Commentaires** de l’historique des versions.</span><span class="sxs-lookup"><span data-stu-id="269ec-144">Each time a user unlocks a record, the latest version is copied to the Records folder in the Preservation Hold library, and that version contains the value of **Record** in the **Comments** field of the version history.</span></span>
<br/><br/>

![Enregistrement affiché dans la bibliothèque de conservation et de préservation](../media/recordversioning10.png)

<span data-ttu-id="269ec-146">Pour afficher l’historique des versions, sélectionnez un document dans la bibliothèque de documents, puis cliquez sur **Historique des versions** dans le menu élément.</span><span class="sxs-lookup"><span data-stu-id="269ec-146">To view the version history, select a document in the document library and then click **Version history** in the item menu.</span></span>

## <a name="where-records-are-stored"></a><span data-ttu-id="269ec-147">Où sont stockés les enregistrements</span><span class="sxs-lookup"><span data-stu-id="269ec-147">Where records are stored</span></span>

<span data-ttu-id="269ec-148">Les enregistrements sont stockés dans le dossier Enregistrements de la bibliothèque de conservation et de préservation du site de niveau supérieur de la collection de sites.</span><span class="sxs-lookup"><span data-stu-id="269ec-148">Records are stored in the Records folder in the Preservation Hold library in the top-level site in the site collection.</span></span> <span data-ttu-id="269ec-149">Dans le volet de navigation gauche, dans le site de niveau supérieur, sélectionnez **Contenu du site** \> **Bibliothèque de conservation et de préservation**.</span><span class="sxs-lookup"><span data-stu-id="269ec-149">In the left navigation on the top-level site, choose **Site contents** \> **Preservation Hold Library**.</span></span>
<br/><br/>

![Bibliothèque de conservation et de préservation](../media/recordversioning11.png)

<br/><br/>

![Dossier Enregistrements dans la bibliothèque de conservation et de préservation](../media/recordversioning12.png)

<span data-ttu-id="269ec-152">La bibliothèque de conservation et de préservation est visible uniquement par les administrateurs de collection de sites.</span><span class="sxs-lookup"><span data-stu-id="269ec-152">The Preservation Hold library is visible only to site collection admins.</span></span> <span data-ttu-id="269ec-153">De plus, la bibliothèque de conservation et de préservation n’existe pas par défaut.</span><span class="sxs-lookup"><span data-stu-id="269ec-153">Also, the Preservation Hold library doesn't exist by default.</span></span> <span data-ttu-id="269ec-154">Elle est créée uniquement lorsque le contenu soumis à une étiquette de rétention ou une stratégie de rétention est supprimé pour la première fois dans la collection de sites.</span><span class="sxs-lookup"><span data-stu-id="269ec-154">It's created only when content subject to a retention label or retention policy is deleted for the first time in the site collection.</span></span>

## <a name="searching-the-audit-log-for-record-versioning-events"></a><span data-ttu-id="269ec-155">Rechercher dans le journal d’audit les événements de contrôle de version d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="269ec-155">Searching the audit log for record versioning events</span></span>

<span data-ttu-id="269ec-156">Les actions de verrouillage et déverrouillage des enregistrements sont enregistrées dans le journal d’audit.</span><span class="sxs-lookup"><span data-stu-id="269ec-156">The actions of locking and unlocking records are logged in the audit log.</span></span> <span data-ttu-id="269ec-157">Vous pouvez rechercher les activités spécifiques **Statut de l’enregistrement basculé sur verrouillé** et **Statut de l’enregistrement basculé sur déverrouillé**, situées dans la section **Activités de fichier et de page** dans la liste déroulante **Activités** sur la page **Effectuer une recherche dans le journal d’audit** du centre de sécurité et conformité.</span><span class="sxs-lookup"><span data-stu-id="269ec-157">You can search for the specific activities **Changed record status to locked** and **Changed record status to unlocked**, which are located in the **File and page activities** section in the **Activities** dropdown list on the **Audit log search** page in the security and compliance center.</span></span>
<br/><br/>

![Rechercher dans le journal d’audit des événements de contrôle de version d’enregistrement](../media/recordversioning13.png)

<span data-ttu-id="269ec-159">Pour plus d’informations sur la recherche de ces événements, voir la section « Activités de fichier et de page » dans [Effectuer une recherche dans le journal d’audit dans le Centre de sécurité et conformité](search-the-audit-log-in-security-and-compliance.md#file-and-page-activities).</span><span class="sxs-lookup"><span data-stu-id="269ec-159">For more information about searching for these events, see the "File and page activities" section in [Search the audit log in the Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md#file-and-page-activities).</span></span>

## <a name="next-steps"></a><span data-ttu-id="269ec-160">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="269ec-160">Next steps</span></span>

<span data-ttu-id="269ec-161">Pour marquer du contenu en tant qu’enregistrement, consultez [Déclarer des enregistrements à l’aide d’étiquettes de rétention](declare-records.md).</span><span class="sxs-lookup"><span data-stu-id="269ec-161">To mark content as a record, see [Declare records by using retention labels](declare-records.md).</span></span>

<span data-ttu-id="269ec-162">Si vous souhaitez en savoir plus sur la destruction des enregistrements, voir [Disposition de contenu](disposition.md).</span><span class="sxs-lookup"><span data-stu-id="269ec-162">To learn about disposition of records, see [Disposing of content](disposition.md).</span></span>