---
title: Configurer une collection de certificats virtuels-Exchange Online
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 04a616e6-197c-490c-ae8c-c8d5f0f0b3dd
description: Les administrateurs peuvent apprendre à créer une collection de certificats virtuels qui sera utilisée pour valider les certificats S/MIME dans Exchange Online.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 16c6d38882a69feb46aa3e8fadccd6e005426304
ms.sourcegitcommit: e12fa502bc216f6083ef5666f693a04bb727d4df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "46825136"
---
# <a name="set-up-virtual-certificate-collection-in-exchange-online-to-validate-smime"></a><span data-ttu-id="6f1e9-103">Configurer la collection de certificats virtuels dans Exchange Online pour valider S/MIME</span><span class="sxs-lookup"><span data-stu-id="6f1e9-103">Set up virtual certificate collection in Exchange Online to validate S/MIME</span></span>

<span data-ttu-id="6f1e9-104">En tant qu’administrateur, vous devrez configurer une collection de certificats virtuels dans Exchange Online qui sera utilisée pour valider les certificats S/MIME.</span><span class="sxs-lookup"><span data-stu-id="6f1e9-104">As an admin, you will need to configure a virtual certificate collection in Exchange Online that will be used to validate S/MIME certificates.</span></span> <span data-ttu-id="6f1e9-105">Cette collection de certificats virtuels est configurée en tant que magasin de certificats avec une extension de nom de fichier SST.</span><span class="sxs-lookup"><span data-stu-id="6f1e9-105">This virtual certificate collection is set up as a certificate store with an SST filename extension.</span></span> <span data-ttu-id="6f1e9-106">Le fichier SST contient tous les certificats racine et intermédiaires utilisés lors de la validation d’un certificat S/MIME.</span><span class="sxs-lookup"><span data-stu-id="6f1e9-106">The SST file contains all the root and intermediate certificates that are used when validating an S/MIME certificate.</span></span>

## <a name="create-and-save-an-sst"></a><span data-ttu-id="6f1e9-107">Créer et enregistrer un fichier SST</span><span class="sxs-lookup"><span data-stu-id="6f1e9-107">Create and save an SST</span></span>

<span data-ttu-id="6f1e9-108">Vous pouvez créer ce fichier de magasin de certificats SST en exportant les certificats à partir d’un ordinateur approuvé à l’aide de la cmdlet **Export-certificat** dans Windows PowerShell et en spécifiant la valeur de _type_ SST.</span><span class="sxs-lookup"><span data-stu-id="6f1e9-108">You can create this SST certificate store file by exporting the certificates from a trusted machine using the **Export-Certificate** cmdlet in Windows PowerShell and specifying the _Type_ value as SST.</span></span> <span data-ttu-id="6f1e9-109">Pour obtenir des instructions, consultez la rubrique [Export-Certificate](https://docs.microsoft.com/powershell/module/pkiclient/export-certificate).</span><span class="sxs-lookup"><span data-stu-id="6f1e9-109">For instructions, see [Export-Certificate](https://docs.microsoft.com/powershell/module/pkiclient/export-certificate).</span></span>

<span data-ttu-id="6f1e9-110">Une fois que vous avez le fichier de magasin de certificats SST, utilisez la syntaxe suivante dans Exchange Online PowerShell pour enregistrer le contenu du fichier SST dans le magasin de certificats virtuels Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="6f1e9-110">Once you have the SST certificate store file, use the following syntax in Exchange Online PowerShell to save the SST file contents in the Exchange Online virtual certificate store.</span></span> <span data-ttu-id="6f1e9-111">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="6f1e9-111">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

```PowerShell
Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content <FileNameAndPath>.sst -Encoding Byte)
```

<span data-ttu-id="6f1e9-112">Cet exemple importe le fichier SST C:\My Documents\exported Rules Certificate Store. SST.</span><span class="sxs-lookup"><span data-stu-id="6f1e9-112">This example imports the SST file C:\My Documents\Exported Certificate Store.sst.</span></span>

```PowerShell
Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content "C:\My Documents\Exported Certificate Store.sst" -Encoding Byte)
```

<span data-ttu-id="6f1e9-113">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-SmimeConfig](https://docs.microsoft.com/powershell/module/exchange/set-smimeconfig).</span><span class="sxs-lookup"><span data-stu-id="6f1e9-113">For detailed syntax and parameter information, see [Set-SmimeConfig](https://docs.microsoft.com/powershell/module/exchange/set-smimeconfig).</span></span>

## <a name="ensuring-a-certificate-is-valid"></a><span data-ttu-id="6f1e9-114">S’assurer de la validité d’un certificat</span><span class="sxs-lookup"><span data-stu-id="6f1e9-114">Ensuring a certificate is valid</span></span>

<span data-ttu-id="6f1e9-115">Dans Exchange Online, seul le service SST est utilisé pour la validation des certificats.</span><span class="sxs-lookup"><span data-stu-id="6f1e9-115">In Exchange Online, only the SST is used for certificate validation.</span></span>

## <a name="more-information"></a><span data-ttu-id="6f1e9-116">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="6f1e9-116">More Information</span></span>

[<span data-ttu-id="6f1e9-117">S/MIME pour la signature et le chiffrement des messages</span><span class="sxs-lookup"><span data-stu-id="6f1e9-117">S/MIME for message signing and encryption</span></span>](s-mime-for-message-signing-and-encryption.md)

[<span data-ttu-id="6f1e9-118">Get-SmimeConfig</span><span class="sxs-lookup"><span data-stu-id="6f1e9-118">Get-SmimeConfig</span></span>](https://docs.microsoft.com/powershell/module/exchange/get-smimeconfig)
