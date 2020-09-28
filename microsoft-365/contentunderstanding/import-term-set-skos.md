---
title: Importer un ensemble de termes à l’aide d’un format basé sur SKOS
description: Découvrez comment importer un ensemble de termes à l’aide d’un format basé sur SKOS
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
audience: admin
ms.prod: microsoft-365-enterprise
ms.topic: article
ms.service: ''
search.appverid: ''
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: aaed88463f690853672780b48a8ee3857a956847
ms.sourcegitcommit: 15be7822220041c25fc52565f1c64d252e442d89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48295892"
---
# <a name="import-a-term-set-using-a-skos-based-format"></a><span data-ttu-id="8f5dd-103">Importer un ensemble de termes à l’aide d’un format basé sur SKOS</span><span class="sxs-lookup"><span data-stu-id="8f5dd-103">Import a term set using a SKOS-based format</span></span>

<span data-ttu-id="8f5dd-104">Vous pouvez importer un ensemble de termes à l’aide d’un format SKOS.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-104">You can import a term set using a SKOS-based format.</span></span> <span data-ttu-id="8f5dd-105">Pour plus d’informations sur le format, reportez-vous à la rubrique [référence de format SKOS taxonomie SharePoint](skos-format-reference.md).</span><span class="sxs-lookup"><span data-stu-id="8f5dd-105">For details about the format, see [SharePoint taxonomy SKOS format reference](skos-format-reference.md).</span></span>

<span data-ttu-id="8f5dd-106">Nous vous recommandons de conserver vos fichiers d’importation à moins de 20 000 termes.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-106">We recommend keeping your import files to less than 20,000 terms.</span></span> <span data-ttu-id="8f5dd-107">Les fichiers plus volumineux peuvent augmenter le temps de validation et d’importation.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-107">Larger files can increase the time taken for validation and import.</span></span>

1. <span data-ttu-id="8f5dd-108">Dans le centre d’administration SharePoint, développez **services de contenu**, puis cliquez sur **magasin de termes**.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-108">In the SharePoint admin center, expand **Content services**, and then click **Term store**.</span></span>

2. <span data-ttu-id="8f5dd-109">Sélectionnez le groupe de termes dans lequel vous souhaitez importer l’ensemble de termes.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-109">Select the term group where you want to import the term set.</span></span>

3. <span data-ttu-id="8f5dd-110">Dans la barre de commandes, cliquez sur **importer l’ensemble de termes**.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-110">In the command bar, click **Import term set**.</span></span>
 
4.  <span data-ttu-id="8f5dd-111">Si vous souhaitez télécharger un exemple de fichier à utiliser en tant que modèle, cliquez sur **Sample-Metadata. TTL** pour obtenir un exemple de fichier qui utilise le format SKOS.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-111">If you want to download a sample file to use as a template, click **sample-metadata.ttl** to get a sample file that uses the SKOS-based format.</span></span>
 
5.  <span data-ttu-id="8f5dd-112">Créez le fichier d’importation contenant les ensembles de termes & termes que vous souhaitez importer.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-112">Create the import file that contains the term sets & terms you wish to import.</span></span>

6.  <span data-ttu-id="8f5dd-113">Sous **format de fichier**, sélectionnez **SKOS (\*. TTL)**.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-113">Under **File format**, select **SKOS (\*.ttl)**.</span></span>

7.  <span data-ttu-id="8f5dd-114">Cliquez sur **Parcourir** , puis accédez à votre fichier d’importation et ajoutez-le.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-114">Click **Browse** and navigate to and add your import file.</span></span>

8.  <span data-ttu-id="8f5dd-115">Cliquez sur **Importer**.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-115">Click **Import**.</span></span> <span data-ttu-id="8f5dd-116">Ne fermez pas le panneau tant que l’importation n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-116">Do not close the panel until the import completes.</span></span>

<span data-ttu-id="8f5dd-117">Lors de l’importation réussie du fichier, un message de réussite s’affiche et le magasin de termes est actualisé et vous pouvez accéder aux nouveaux ensembles de termes.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-117">On successful import of the file, a success message will be displayed, and the term store will refresh and you can navigate to the newly created term sets.</span></span>

## <a name="see-also"></a><span data-ttu-id="8f5dd-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f5dd-118">See also</span></span>

[<span data-ttu-id="8f5dd-119">Présentation des métadonnées gérées</span><span class="sxs-lookup"><span data-stu-id="8f5dd-119">Introduction to managed metadata</span></span>](https://docs.microsoft.com/sharepoint/managed-metadata)

[<span data-ttu-id="8f5dd-120">Présentation de l’explication des documents</span><span class="sxs-lookup"><span data-stu-id="8f5dd-120">Document understanding overview</span></span>](document-understanding-overview.md)

[<span data-ttu-id="8f5dd-121">Importer des ensembles de termes (niveau site)</span><span class="sxs-lookup"><span data-stu-id="8f5dd-121">Import term sets (site level)</span></span>](https://support.microsoft.com/office/168fbc86-7fce-4288-9a1f-b83fc3921c18)