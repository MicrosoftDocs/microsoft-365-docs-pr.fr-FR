---
title: Fonctionnement des pièces jointes fiables de PACM
f1.keywords:
- NOCSH
ms.author: tracyp
author: msfttracyp
manager: dansimp
audience: Admin
ms.date: 05/17/2019
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: Découvrez comment protéger votre organisation contre les fichiers malveillants à l’aide de pièces jointes fiables ATP pour Office 365.
ms.openlocfilehash: a0d5923ccac525b23aa2ef6b45936524f0a7b483
ms.sourcegitcommit: a45cf8b887587a1810caf9afa354638e68ec5243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/05/2020
ms.locfileid: "44036655"
---
# <a name="how-atp-safe-attachments-works"></a><span data-ttu-id="91ee0-103">Fonctionnement des pièces jointes fiables de PACM</span><span class="sxs-lookup"><span data-stu-id="91ee0-103">How ATP Safe Attachments works</span></span>

## <a name="how-it-works"></a><span data-ttu-id="91ee0-104">Fonctionnement</span><span class="sxs-lookup"><span data-stu-id="91ee0-104">How it works</span></span>

<span data-ttu-id="91ee0-105">La fonctionnalité pièces jointes approuvées ATP vérifie les pièces jointes de courrier électronique pour les personnes de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="91ee0-105">The ATP Safe Attachments feature checks email attachments for people in your organization.</span></span> <span data-ttu-id="91ee0-106">Lorsqu’une stratégie de pièces jointes approuvées ATP est en place et qu’une personne concernée par cette stratégie affiche son courrier électronique dans Office 365, ses pièces jointes sont vérifiées et les actions appropriées sont prises, en fonction des stratégies de pièces jointes approuvées ATP.</span><span class="sxs-lookup"><span data-stu-id="91ee0-106">When an ATP Safe Attachments policy is in place and someone covered by that policy views their email in Office 365, their email attachments are checked and appropriate actions are taken, based on your ATP Safe Attachments policies.</span></span> <span data-ttu-id="91ee0-107">En fonction de la définition de vos stratégies, les utilisateurs peuvent continuer à travailler sans jamais savoir qu’ils ont reçu des fichiers malveillants.</span><span class="sxs-lookup"><span data-stu-id="91ee0-107">Depending on how your policies are defined, people can continue working without ever knowing they were sent malicious files.</span></span>
  
<span data-ttu-id="91ee0-108">Voici deux exemples de pièces jointes approuvées ATP au travail.</span><span class="sxs-lookup"><span data-stu-id="91ee0-108">Here are two examples of ATP Safe Attachments at work.</span></span>
  
- <span data-ttu-id="91ee0-109">**Exemple 1 : pièce jointe de message électronique** Supposons que Lee reçoit un message électronique comportant une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="91ee0-109">**Example 1: Email attachment** Suppose that Lee receives an email message that has an attachment.</span></span> <span data-ttu-id="91ee0-110">Il n’est pas évident de savoir si cette pièce jointe est fiable ou si elle contient en réalité des programmes malveillants conçus pour voler les informations d’identification utilisateur de Lee.</span><span class="sxs-lookup"><span data-stu-id="91ee0-110">It is not obvious to Lee whether that attachment is safe or actually contains malware designed to steal Lee's user credentials.</span></span> <span data-ttu-id="91ee0-111">Dans l’organisation de Lee, un administrateur de sécurité a défini une stratégie de pièces jointes approuvées ATP il y a quelques jours.</span><span class="sxs-lookup"><span data-stu-id="91ee0-111">In Lee's organization, a security administrator defined an ATP Safe Attachments policy a few days ago.</span></span> <span data-ttu-id="91ee0-112">Avec la fonctionnalité pièces jointes approuvées ATP, la pièce jointe est ouverte et testée dans un environnement virtuel avant que Lee la reçoive.</span><span class="sxs-lookup"><span data-stu-id="91ee0-112">With the ATP Safe Attachments feature, the email attachment is opened and tested in a virtual environment before Lee receives it.</span></span> <span data-ttu-id="91ee0-113">Si la pièce jointe est considérée comme malveillante, elle sera automatiquement supprimée.</span><span class="sxs-lookup"><span data-stu-id="91ee0-113">If the attachment is determined to be malicious, it will be removed automatically.</span></span> <span data-ttu-id="91ee0-114">Si la pièce jointe est sécurisée, elle s’ouvre comme prévu lorsque Lee clique dessus.</span><span class="sxs-lookup"><span data-stu-id="91ee0-114">If the attachment is safe, it will open as expected when Lee clicks on it.</span></span>

- <span data-ttu-id="91ee0-115">**Exemple 2 : fichier dans SharePoint Online** Supposons que Jean a reçu un fichier et l’a téléchargé dans une bibliothèque dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="91ee0-115">**Example 2: File in SharePoint Online** Suppose that Jean received a file and uploaded it into a library in SharePoint Online.</span></span> <span data-ttu-id="91ee0-116">Jean partage le lien vers le fichier avec le reste de l’équipe, sans savoir que le fichier est réellement malveillant.</span><span class="sxs-lookup"><span data-stu-id="91ee0-116">Jean shares the link to the file with the rest of the team, not knowing that the file is actually malicious.</span></span> <span data-ttu-id="91ee0-117">Heureusement, la protection avancée contre les menaces [pour SharePoint, OneDrive et Microsoft teams](atp-for-spo-odb-and-teams.md) détecte le fichier malveillant et le bloque.</span><span class="sxs-lookup"><span data-stu-id="91ee0-117">Fortunately, [ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) detects the malicious file and blocks it.</span></span> <span data-ttu-id="91ee0-118">Quelques jours plus tard, Chris ouvre le document.</span><span class="sxs-lookup"><span data-stu-id="91ee0-118">A few days later, Chris goes to open the document.</span></span> <span data-ttu-id="91ee0-119">Bien que Chris puisse voir le fichier, Chris ne peut pas l’ouvrir ou le partager, ce qui protège son ordinateur et d’autres personnes du fichier malveillant.</span><span class="sxs-lookup"><span data-stu-id="91ee0-119">Although Chris can see the file is there, Chris cannot open or share it, which protects Chris's computer and others from the malicious file.</span></span>

<span data-ttu-id="91ee0-120">Les stratégies de pièces jointes approuvées ATP peuvent être appliquées à des personnes ou des groupes spécifiques de votre organisation ou à votre domaine entier.</span><span class="sxs-lookup"><span data-stu-id="91ee0-120">ATP Safe Attachments policies can be applied to specific people or groups in your organization, or to your entire domain.</span></span> <span data-ttu-id="91ee0-121">En outre, les stratégies de pièces jointes approuvées ATP peuvent être configurées pour utiliser les pièces jointes des espaces réservés pendant l’analyse des pièces jointes réelles.</span><span class="sxs-lookup"><span data-stu-id="91ee0-121">In addition, ATP Safe Attachments policies can be configured to use placeholder attachments while actual attachments are being scanned.</span></span> <span data-ttu-id="91ee0-122">Pour en savoir plus, consultez la rubrique **[configurer des stratégies de pièces jointes approuvées ATP dans Office 365](set-up-atp-safe-attachments-policies.md)**.</span><span class="sxs-lookup"><span data-stu-id="91ee0-122">To learn more, see **[Set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md)**.</span></span>

> [!NOTE]
> <span data-ttu-id="91ee0-123">L’analyse des pièces jointes approuvées ATP a lieu dans la région où se trouvent vos données.</span><span class="sxs-lookup"><span data-stu-id="91ee0-123">ATP Safe Attachments scanning takes place in the same region where your data resides.</span></span> <span data-ttu-id="91ee0-124">Pour plus d’informations sur la géographie du centre de données, voir [où se trouvent vos données ?](https://products.office.com/where-is-your-data-located?geo=All)</span><span class="sxs-lookup"><span data-stu-id="91ee0-124">For more information about data center geography, see [Where is your data located?](https://products.office.com/where-is-your-data-located?geo=All)</span></span> 

