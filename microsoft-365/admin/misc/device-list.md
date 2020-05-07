---
title: Fichier CSV de liste d’appareils
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
ms.custom:
- MSB365
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 932e3676-2491-49f0-9177-d893d2f5276e
ROBOTS: NOINDEX
description: Découvrez comment créer un fichier CSV pour AutoPilot dans Microsoft 365 pour les entreprises.
ms.openlocfilehash: c83862675db1372aa2cef27c727c04577b4cf5a3
ms.sourcegitcommit: 7f307b4f583b602f11f69adae46d7f3bf6982c65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2020
ms.locfileid: "44064650"
---
# <a name="device-list-csv-file"></a><span data-ttu-id="ebf3b-103">Fichier CSV de liste d’appareils</span><span class="sxs-lookup"><span data-stu-id="ebf3b-103">Device list CSV-file</span></span>

## <a name="device-list-csv-file-format"></a><span data-ttu-id="ebf3b-104">Format de fichier. csv de liste d’appareils</span><span class="sxs-lookup"><span data-stu-id="ebf3b-104">Device list .csv file format</span></span>

<span data-ttu-id="ebf3b-105">Pour gérer et déployer des appareils via Windows AutoPilot, vous aurez besoin d’un fichier. csv contenant des informations spécifiques sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="ebf3b-105">To manage and deploy devices through Windows Autopilot, you'll need a .csv file that contains specific information about the devices.</span></span>
  
<span data-ttu-id="ebf3b-106">Les colonnes du fichier de liste d’appareils doivent avoir les en-têtes suivants dans l’ordre spécifié :</span><span class="sxs-lookup"><span data-stu-id="ebf3b-106">Columns in the device list file must have the following headers in the specified order:</span></span>
  
- <span data-ttu-id="ebf3b-107">Colonne A : Numéro de série de l'appareil</span><span class="sxs-lookup"><span data-stu-id="ebf3b-107">Column A: Device Serial Number</span></span>

- <span data-ttu-id="ebf3b-108">Colonne B : laisser vide</span><span class="sxs-lookup"><span data-stu-id="ebf3b-108">Column B: leave blank</span></span>

- <span data-ttu-id="ebf3b-109">Colonne C : Hachage du matériel</span><span class="sxs-lookup"><span data-stu-id="ebf3b-109">Column C: Hardware Hash</span></span>

<span data-ttu-id="ebf3b-110">Vous pouvez obtenir ces informations à partir de votre fournisseur de matériel ou vous pouvez utiliser le [script Get-WindowsAutoPilotInfo PowerShell](https://www.powershellgallery.com/packages/Get-WindowsAutoPilotInfo) qui génèrera un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="ebf3b-110">You can get this information from your hardware vendor, or you can use the [Get-WindowsAutoPilotInfo PowerShell script](https://www.powershellgallery.com/packages/Get-WindowsAutoPilotInfo) that will generate a CSV file.</span></span> 

<span data-ttu-id="ebf3b-111">Lorsque vous ajoutez des appareils, vous devez également les ajouter à un profil.</span><span class="sxs-lookup"><span data-stu-id="ebf3b-111">When you add devices, you also need to add them to a Profile.</span></span> <span data-ttu-id="ebf3b-112">Un profil est utilisé pour appliquer des profils de déploiement AutoPilot à un appareil ou à un groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="ebf3b-112">A profile is used to apply AutoPilot deployment profiles to a device or a group of devices.</span></span>
  
## <a name="related-articles"></a><span data-ttu-id="ebf3b-113">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="ebf3b-113">Related articles</span></span>

[<span data-ttu-id="ebf3b-114">Documentation et ressources de Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="ebf3b-114">Microsoft 365 for business documentation and resources</span></span>](https://go.microsoft.com/fwlink/p/?linkid=853701)
  
[<span data-ttu-id="ebf3b-115">Prise en main de Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="ebf3b-115">Get started with Microsoft 365 for business</span></span>](https://docs.microsoft.com/microsoft-365/business/microsoft-365-business-overview)
  
[<span data-ttu-id="ebf3b-116">Gérer Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="ebf3b-116">Manage Microsoft 365 for business</span></span>](https://docs.microsoft.com/microsoft-365/business/manage)
  
