---
title: Importer un ensemble de termes avec un format SKOS
description: Découvrez comment importer un ensemble de termes avec un format SKOS
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
audience: admin
ms.prod: microsoft-365-enterprise
ms.topic: article
ms.service: ''
ms.collection: enabler-strategic
search.appverid: ''
localization_priority: Priority
ms.openlocfilehash: ba0f240caa8b3452783436e9a35c53d44baba894
ms.sourcegitcommit: 162c01dfaa2fdb3225ce4c24964c1065ce22ed5d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2021
ms.locfileid: "49976434"
---
# <a name="import-a-term-set-using-a-skos-based-format"></a><span data-ttu-id="29ef1-103">Importer un ensemble de termes avec un format SKOS</span><span class="sxs-lookup"><span data-stu-id="29ef1-103">Import a term set using a SKOS-based format</span></span>

<span data-ttu-id="29ef1-104">Importer un ensemble de termes avec un format basé sur SKOS.</span><span class="sxs-lookup"><span data-stu-id="29ef1-104">You can import a term set using a SKOS-based format.</span></span> <span data-ttu-id="29ef1-105">Si vous souhaitez en savoir plus sur le format, veuillez consulter la rubrique [Référence de format SKOS pour la taxonomie SharePoint](skos-format-reference.md).</span><span class="sxs-lookup"><span data-stu-id="29ef1-105">For details about the format, see [SharePoint taxonomy SKOS format reference](skos-format-reference.md).</span></span>

<span data-ttu-id="29ef1-106">Nous vous recommandons d’inclure moins de 20 000 termes dans vos fichiers d’importation.</span><span class="sxs-lookup"><span data-stu-id="29ef1-106">We recommend keeping your import files to less than 20,000 terms.</span></span> <span data-ttu-id="29ef1-107">Les fichiers plus volumineux peuvent augmenter le temps de validation et d’importation.</span><span class="sxs-lookup"><span data-stu-id="29ef1-107">Larger files can increase the time taken for validation and import.</span></span>

1. <span data-ttu-id="29ef1-108">Dans le Centre d’administration SharePoint, développez **Services de contenu**, puis cliquez sur **Magasin de termes**.</span><span class="sxs-lookup"><span data-stu-id="29ef1-108">In the SharePoint admin center, expand **Content services**, and then click **Term store**.</span></span>

2. <span data-ttu-id="29ef1-109">Sélectionnez le groupe de termes où vous souhaitez importer l’ensemble de termes.</span><span class="sxs-lookup"><span data-stu-id="29ef1-109">Select the term group where you want to import the term set.</span></span>

3. <span data-ttu-id="29ef1-110">Dans la barre de commandes, cliquez sur **Importer l’ensemble de termes**.</span><span class="sxs-lookup"><span data-stu-id="29ef1-110">In the command bar, click **Import term set**.</span></span>
 
4.  <span data-ttu-id="29ef1-111">Si vous voulez télécharger un fichier échantillon à utiliser en tant que modèle, cliquez sur **sample-metadata.ttl** pour obtenir un exemple de fichier qui utilise le format SKOS.</span><span class="sxs-lookup"><span data-stu-id="29ef1-111">If you want to download a sample file to use as a template, click **sample-metadata.ttl** to get a sample file that uses the SKOS-based format.</span></span>
 
5.  <span data-ttu-id="29ef1-112">Créez le fichier d’importation contenant les ensembles de termes et les termes à importer.</span><span class="sxs-lookup"><span data-stu-id="29ef1-112">Create the import file that contains the term sets & terms you wish to import.</span></span>

6.  <span data-ttu-id="29ef1-113">Sous **Format de fichier**, sélectionnez **SKOS (\*.ttl)**.</span><span class="sxs-lookup"><span data-stu-id="29ef1-113">Under **File format**, select **SKOS (\*.ttl)**.</span></span>

7.  <span data-ttu-id="29ef1-114">Cliquez sur **Parcourir**, puis ajoutez votre fichier d’importation.</span><span class="sxs-lookup"><span data-stu-id="29ef1-114">Click **Browse** and navigate to and add your import file.</span></span>

8.  <span data-ttu-id="29ef1-115">Cliquez sur **Importer**.</span><span class="sxs-lookup"><span data-stu-id="29ef1-115">Click **Import**.</span></span> <span data-ttu-id="29ef1-116">Ne fermez le panneau qu’une fois l’importation terminée.</span><span class="sxs-lookup"><span data-stu-id="29ef1-116">Do not close the panel until the import completes.</span></span>

<span data-ttu-id="29ef1-117">Une fois le fichier correctement importé, un message de réussite s’affiche, puis le magasin de termes est actualisé. Vous pouvez alors accéder aux nouveaux ensembles de termes récemment créés.</span><span class="sxs-lookup"><span data-stu-id="29ef1-117">On successful import of the file, a success message will be displayed, and the term store will refresh and you can navigate to the newly created term sets.</span></span>

## <a name="see-also"></a><span data-ttu-id="29ef1-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29ef1-118">See also</span></span>

[<span data-ttu-id="29ef1-119">Présentation des métadonnées gérées</span><span class="sxs-lookup"><span data-stu-id="29ef1-119">Introduction to managed metadata</span></span>](https://docs.microsoft.com/sharepoint/managed-metadata)

[<span data-ttu-id="29ef1-120">Présentation de la compréhension de document</span><span class="sxs-lookup"><span data-stu-id="29ef1-120">Document understanding overview</span></span>](document-understanding-overview.md)

[<span data-ttu-id="29ef1-121">Importer des ensembles de termes (niveau du site)</span><span class="sxs-lookup"><span data-stu-id="29ef1-121">Import term sets (site level)</span></span>](https://support.microsoft.com/office/168fbc86-7fce-4288-9a1f-b83fc3921c18)
