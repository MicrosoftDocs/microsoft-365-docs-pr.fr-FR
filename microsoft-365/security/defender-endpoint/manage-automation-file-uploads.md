---
title: Gérer les téléchargements de fichiers d’automatisation
description: Activer l’analyse de contenu et configurer l’extension de fichier et les extensions de pièce jointe de courrier électronique qui seront soumises à l’analyse
keywords: automation, fichier, téléchargements, contenu, analyse, fichier, extension, e-mail, pièce jointe
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
ms.openlocfilehash: c8935368e4439221f2ce21cfa620e540c02165f8
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51185848"
---
# <a name="manage-automation-file-uploads"></a><span data-ttu-id="15967-104">Gérer les téléchargements de fichiers d’automatisation</span><span class="sxs-lookup"><span data-stu-id="15967-104">Manage automation file uploads</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="15967-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="15967-105">**Applies to:**</span></span>
- [<span data-ttu-id="15967-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="15967-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="15967-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="15967-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="15967-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="15967-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="15967-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="15967-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-automationefileuploads-abovefoldlink)

<span data-ttu-id="15967-110">Activez la fonctionnalité d’analyse de contenu afin que certains fichiers et pièces jointes de courrier électronique soient automatiquement téléchargés vers le cloud pour une inspection supplémentaire dans l’examen automatisé.</span><span class="sxs-lookup"><span data-stu-id="15967-110">Enable the content analysis capability so that certain files and email attachments can automatically be uploaded to the cloud for additional inspection in Automated investigation.</span></span>

<span data-ttu-id="15967-111">Identifiez les fichiers et les pièces jointes en spécifiant les noms d’extension de fichier et les noms d’extension de pièce jointe de courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="15967-111">Identify the files and email attachments by specifying the file extension names and email attachment extension names.</span></span> 

<span data-ttu-id="15967-112">Par exemple, si vous ajoutez *exe* et *bat* en tant que noms d’extension de fichier ou de pièce jointe, tous les fichiers ou pièces jointes avec ces extensions seront automatiquement envoyés dans le cloud pour une inspection supplémentaire au cours de l’examen automatisé.</span><span class="sxs-lookup"><span data-stu-id="15967-112">For example, if you add *exe* and *bat* as file or attachment extension names, then all files or attachments with those extensions will automatically be sent to the cloud for additional inspection during Automated investigation.</span></span> 

## <a name="add-file-extension-names-and-attachment-extension-names"></a><span data-ttu-id="15967-113">Ajoutez des noms d’extension de fichier et des noms d’extension de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="15967-113">Add file extension names and attachment extension names.</span></span>

1. <span data-ttu-id="15967-114">Dans le volet de navigation, sélectionnez **Téléchargements** de fichiers Settings  >  **Automation.**</span><span class="sxs-lookup"><span data-stu-id="15967-114">In the navigation pane, select **Settings** > **Automation file uploads**.</span></span> 

2. <span data-ttu-id="15967-115">Basculez le paramètre d’analyse de contenu entre **Le et** **Le.**</span><span class="sxs-lookup"><span data-stu-id="15967-115">Toggle the content analysis setting between **On** and **Off**.</span></span>

3. <span data-ttu-id="15967-116">Configurez les noms d’extension suivants et séparez les noms d’extension par une virgule :</span><span class="sxs-lookup"><span data-stu-id="15967-116">Configure the following extension names and separate extension names with a comma:</span></span>
   - <span data-ttu-id="15967-117">**Noms d’extension de fichier** : les fichiers suspects, à l’exception des pièces jointes, seront envoyés pour inspection supplémentaire</span><span class="sxs-lookup"><span data-stu-id="15967-117">**File extension names** -  Suspicious files except email attachments will be submitted for additional inspection</span></span>
  

## <a name="related-topics"></a><span data-ttu-id="15967-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15967-118">Related topics</span></span>
- [<span data-ttu-id="15967-119">Gérer les exclusions de dossiers d’automatisation</span><span class="sxs-lookup"><span data-stu-id="15967-119">Manage automation folder exclusions</span></span>](manage-automation-folder-exclusions.md)
