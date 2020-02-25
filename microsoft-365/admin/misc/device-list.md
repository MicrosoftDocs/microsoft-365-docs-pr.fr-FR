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
description: Découvrez comment créer un fichier CSV pour AutoPilo étain Microsoft 365 entreprise.
ms.openlocfilehash: cd317bd5edaa3fdaea8a704f79a269387e8fe1c1
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42254301"
---
# <a name="device-list-csv-file"></a><span data-ttu-id="d5981-103">Fichier CSV de liste d’appareils</span><span class="sxs-lookup"><span data-stu-id="d5981-103">Device list CSV-file</span></span>

## <a name="device-list-csv-file-format"></a><span data-ttu-id="d5981-104">Format de fichier. csv de liste d’appareils</span><span class="sxs-lookup"><span data-stu-id="d5981-104">Device list .csv file format</span></span>

<span data-ttu-id="d5981-105">Pour gérer et déployer des appareils via Windows AutoPilot, vous aurez besoin d’un fichier. csv contenant des informations spécifiques sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="d5981-105">To manage and deploy devices through Windows Autopilot, you'll need a .csv file that contains specific information about the devices.</span></span>
  
<span data-ttu-id="d5981-106">Les colonnes du fichier de liste d’appareils doivent avoir les en-têtes suivants dans l’ordre spécifié :</span><span class="sxs-lookup"><span data-stu-id="d5981-106">Columns in the device list file must have the following headers in the specified order:</span></span>
  
- <span data-ttu-id="d5981-107">Colonne A : Numéro de série de l'appareil</span><span class="sxs-lookup"><span data-stu-id="d5981-107">Column A: Device Serial Number</span></span>

- <span data-ttu-id="d5981-108">Colonne B : laisser vide</span><span class="sxs-lookup"><span data-stu-id="d5981-108">Column B: leave blank</span></span>

- <span data-ttu-id="d5981-109">Colonne C : Hachage du matériel</span><span class="sxs-lookup"><span data-stu-id="d5981-109">Column C: Hardware Hash</span></span>

<span data-ttu-id="d5981-110">Vous pouvez obtenir ces informations à partir de votre fournisseur de matériel ou vous pouvez utiliser le [script Get-WindowsAutoPilotInfo PowerShell](https://www.powershellgallery.com/packages/Get-WindowsAutoPilotInfo) qui génèrera un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="d5981-110">You can get this information from your hardware vendor, or you can use the [Get-WindowsAutoPilotInfo PowerShell script](https://www.powershellgallery.com/packages/Get-WindowsAutoPilotInfo) that will generate a CSV file.</span></span> 

<span data-ttu-id="d5981-111">Lorsque vous ajoutez des appareils, vous devez également les ajouter à un profil.</span><span class="sxs-lookup"><span data-stu-id="d5981-111">When you add devices, you also need to add them to a Profile.</span></span> <span data-ttu-id="d5981-112">Un profil est utilisé pour appliquer des profils de déploiement AutoPilot à un appareil ou à un groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="d5981-112">A profile is used to apply AutoPilot deployment profiles to a device or a group of devices.</span></span>
  
## <a name="related-articles"></a><span data-ttu-id="d5981-113">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="d5981-113">Related articles</span></span>

[<span data-ttu-id="d5981-114">Documentation et ressources pour Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="d5981-114">Microsoft 365 Business documentation and resources</span></span>](https://go.microsoft.com/fwlink/p/?linkid=853701)
  
[<span data-ttu-id="d5981-115">Prise en main de Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="d5981-115">Get started with Microsoft 365 Business</span></span>](https://support.office.com/article/496e690b-b75d-4ff5-bf34-cc32905d0364)
  
[<span data-ttu-id="d5981-116">Gérer Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="d5981-116">Manage Microsoft 365 Business</span></span>](https://support.office.com/article/27ff1678-865a-4707-8145-e1155aa815d6)
  