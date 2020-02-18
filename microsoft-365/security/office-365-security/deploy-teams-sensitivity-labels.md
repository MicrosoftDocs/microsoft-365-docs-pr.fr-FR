---
title: Protéger des fichiers dans Teams avec des étiquettes de confidentialité
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 10/31/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom:
- Ent_Solutions
ms.assetid: 5b9c8e41-25d2-436d-89bb-9aecb9ec2b80
description: 'Résumé : appliquez des étiquettes de confidentialité pour protéger les fichiers d’une équipe hautement confidentielle.'
ms.openlocfilehash: b263aeae335b83cadb45b16d70a2a45d56f1cbd3
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42083366"
---
# <a name="protect-files-in-teams-with-sensitivity-labels"></a><span data-ttu-id="1fa7a-103">Protéger des fichiers dans Teams avec des étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="1fa7a-103">Protect files in teams with sensitivity labels</span></span>


<span data-ttu-id="1fa7a-104">Contrairement à une étiquette de confidentialité pour les données hautement réglementées qu’une personne peut appliquer à n’importe quel fichier, une équipe hautement confidentielle doit avoir sa propre étiquette ou sous-étiquette de sorte que les fichiers auxquels elle est attribuée :</span><span class="sxs-lookup"><span data-stu-id="1fa7a-104">Unlike a sensitivity label for highly regulated data that anyone can apply to any file, a highly confidential team needs its own label or sublabel so that assigned files:</span></span>

- <span data-ttu-id="1fa7a-105">Soient chiffrés individuellement.</span><span class="sxs-lookup"><span data-stu-id="1fa7a-105">Are individually encrypted.</span></span>
- <span data-ttu-id="1fa7a-106">Contiennent des autorisations personnalisées de sorte que seuls les membres de l’équipe puissent l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="1fa7a-106">Contain custom permissions so that only members of the team can open it.</span></span>

<span data-ttu-id="1fa7a-107">Pour atteindre ce niveau de sécurité supplémentaire pour les fichiers stockés sur le site SharePoint sous-jacent d’une équipe, vous devez configurer une étiquette de confidentialité personnalisée qui est soit sa propre étiquette, soit une sous-étiquette de l’étiquette générale pour les données hautement réglementées.</span><span class="sxs-lookup"><span data-stu-id="1fa7a-107">To accomplish this additional level of security for files stored in the underlying SharePoint site of a team, you must configure a customized sensitivity label that is either its own label or a sublabel of the general label for highly regulated data.</span></span> <span data-ttu-id="1fa7a-108">Seuls les membres de l’équipe peuvent consulter l’étiquette ou sous-étiquette personnalisée dans leur liste d’étiquettes.</span><span class="sxs-lookup"><span data-stu-id="1fa7a-108">Only team members will see the customized label or sublabel in their list of labels.</span></span>

<span data-ttu-id="1fa7a-109">Utilisez une étiquette de confidentialité lorsque vous avez besoin d’un petit nombre d’étiquettes à la fois pour un usage global et pour des équipes privées individuelles.</span><span class="sxs-lookup"><span data-stu-id="1fa7a-109">Use a sensitivity label when you need a small number of labels for both global use and individual private teams.</span></span> 

<span data-ttu-id="1fa7a-110">Utilisez une sous-étiquette de confidentialité lorsque vous avez un grand nombre d’étiquettes ou si vous souhaitez organiser les étiquettes pour les équipes hautement confidentielles sous l’étiquette hautement réglementée.</span><span class="sxs-lookup"><span data-stu-id="1fa7a-110">Use a sensitivity sublabel when you have a large number of labels or want to organize labels for highly confidential teams under the highly regulated label.</span></span>

<span data-ttu-id="1fa7a-111">Suivez [ces instructions](https://docs.microsoft.com/microsoft-365/compliance/encryption-sensitivity-labels) pour configurer une étiquette distincte ou une sous-étiquette avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="1fa7a-111">Use [these instructions](https://docs.microsoft.com/microsoft-365/compliance/encryption-sensitivity-labels) to configure a separate label or a sublabel with the following settings:</span></span>

- <span data-ttu-id="1fa7a-112">Le nom de l’étiquette ou de la sous-étiquette contient le nom de l’équipe</span><span class="sxs-lookup"><span data-stu-id="1fa7a-112">The name of the label or sublabel contains the name of the team</span></span>
- <span data-ttu-id="1fa7a-113">Le chiffrement est activé</span><span class="sxs-lookup"><span data-stu-id="1fa7a-113">Encryption is enabled</span></span>
- <span data-ttu-id="1fa7a-114">Le groupe Office 365 de l’équipe possède des autorisations de co-édition</span><span class="sxs-lookup"><span data-stu-id="1fa7a-114">The Office 365 group for the team has Co-Author permissions</span></span>

<span data-ttu-id="1fa7a-115">Une fois que vous avez créé, publiez la nouvelle étiquette ou sous-étiquette pour vos utilisateurs, puis appliquez-les aux fichiers en local avant de les charger dans l’équipe ou plus tard une fois que le fichier est stocké dans l’équipe.</span><span class="sxs-lookup"><span data-stu-id="1fa7a-115">After creating, publish the new label or sublabel for your users, who can then apply them to files either locally before uploading them to the team or later once the file is stored in the team.</span></span>

<span data-ttu-id="1fa7a-116">Voici la configuration de l’équipe hautement confidentielle qui utilise des étiquettes de confidentialité pour le chiffrement des fichiers et les autorisations.</span><span class="sxs-lookup"><span data-stu-id="1fa7a-116">Here is the configuration of the highly confidential team that uses sensitivity labels for file encryption and permissions.</span></span>

![Protection de niveau de référence pour une équipe publique.](../../media/highly-confidential-team-dlp-sensitivity-labels.png)


## <a name="see-also"></a><span data-ttu-id="1fa7a-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fa7a-118">See Also</span></span>

[<span data-ttu-id="1fa7a-119">Sécuriser des fichiers dans Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="1fa7a-119">Secure files in Microsoft Teams</span></span>](secure-files-in-teams.md)
  
[<span data-ttu-id="1fa7a-120">Adoption du cloud et solutions hybrides</span><span class="sxs-lookup"><span data-stu-id="1fa7a-120">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
