---
title: Type de ressource Fichier
description: Récupérer les alertes récentes de Microsoft Defender for Endpoint relatives aux fichiers.
keywords: api, api de graphique, api pris en charge, obtenir, alertes, récent
search.product: eADQiWindows 10XVcnh
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
ms.openlocfilehash: 9079a47dcc078b582586370b322502b74ce3838c
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51199980"
---
# <a name="file-resource-type"></a><span data-ttu-id="0ca34-104">Type de ressource Fichier</span><span class="sxs-lookup"><span data-stu-id="0ca34-104">File resource type</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="0ca34-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="0ca34-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="0ca34-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="0ca34-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="0ca34-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="0ca34-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


<span data-ttu-id="0ca34-108">Représente une entité de fichier dans Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0ca34-108">Represent a file entity in Defender for Endpoint.</span></span>

## <a name="methods"></a><span data-ttu-id="0ca34-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0ca34-109">Methods</span></span>
<span data-ttu-id="0ca34-110">Méthode</span><span class="sxs-lookup"><span data-stu-id="0ca34-110">Method</span></span>|<span data-ttu-id="0ca34-111">Type renvoyé</span><span class="sxs-lookup"><span data-stu-id="0ca34-111">Return Type</span></span> |<span data-ttu-id="0ca34-112">Description</span><span class="sxs-lookup"><span data-stu-id="0ca34-112">Description</span></span>
:---|:---|:---
[<span data-ttu-id="0ca34-113">Obtenir un fichier</span><span class="sxs-lookup"><span data-stu-id="0ca34-113">Get file</span></span>](get-file-information.md) | [<span data-ttu-id="0ca34-114">fichier</span><span class="sxs-lookup"><span data-stu-id="0ca34-114">file</span></span>](files.md) | <span data-ttu-id="0ca34-115">Obtenir un fichier unique</span><span class="sxs-lookup"><span data-stu-id="0ca34-115">Get a single file</span></span> 
[<span data-ttu-id="0ca34-116">Liste des alertes associées au fichier</span><span class="sxs-lookup"><span data-stu-id="0ca34-116">List file related alerts</span></span>](get-file-related-alerts.md) | <span data-ttu-id="0ca34-117">collection[alert](alerts.md)</span><span class="sxs-lookup"><span data-stu-id="0ca34-117">[alert](alerts.md) collection</span></span> | <span data-ttu-id="0ca34-118">Obtenez les [entités](alerts.md) d’alerte associées au fichier.</span><span class="sxs-lookup"><span data-stu-id="0ca34-118">Get the [alert](alerts.md) entities that are associated with the file.</span></span>
[<span data-ttu-id="0ca34-119">List file related machines</span><span class="sxs-lookup"><span data-stu-id="0ca34-119">List file related machines</span></span>](get-file-related-machines.md) | <span data-ttu-id="0ca34-120">[collection d’ordinateurs](machine.md)</span><span class="sxs-lookup"><span data-stu-id="0ca34-120">[machine](machine.md) collection</span></span> | <span data-ttu-id="0ca34-121">Obtenez les [entités de](machine.md) l’ordinateur associées à l’alerte.</span><span class="sxs-lookup"><span data-stu-id="0ca34-121">Get the [machine](machine.md) entities associated with the alert.</span></span>
[<span data-ttu-id="0ca34-122">statistiques de fichier</span><span class="sxs-lookup"><span data-stu-id="0ca34-122">file statistics</span></span>](get-file-statistics.md) | <span data-ttu-id="0ca34-123">Résumé des statistiques</span><span class="sxs-lookup"><span data-stu-id="0ca34-123">Statistics summary</span></span> | <span data-ttu-id="0ca34-124">Récupère la prévalence du fichier donné.</span><span class="sxs-lookup"><span data-stu-id="0ca34-124">Retrieves the prevalence for the given file.</span></span>


## <a name="properties"></a><span data-ttu-id="0ca34-125">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0ca34-125">Properties</span></span>
|<span data-ttu-id="0ca34-126">Propriété</span><span class="sxs-lookup"><span data-stu-id="0ca34-126">Property</span></span> | <span data-ttu-id="0ca34-127">Type</span><span class="sxs-lookup"><span data-stu-id="0ca34-127">Type</span></span>    |   <span data-ttu-id="0ca34-128">Description</span><span class="sxs-lookup"><span data-stu-id="0ca34-128">Description</span></span> |
|:---|:---|:---|
|<span data-ttu-id="0ca34-129">sha1</span><span class="sxs-lookup"><span data-stu-id="0ca34-129">sha1</span></span> | <span data-ttu-id="0ca34-130">Chaîne</span><span class="sxs-lookup"><span data-stu-id="0ca34-130">String</span></span> | <span data-ttu-id="0ca34-131">Hachage Sha1 du contenu du fichier</span><span class="sxs-lookup"><span data-stu-id="0ca34-131">Sha1 hash of the file content</span></span> |
|<span data-ttu-id="0ca34-132">sha256</span><span class="sxs-lookup"><span data-stu-id="0ca34-132">sha256</span></span> | <span data-ttu-id="0ca34-133">Chaîne</span><span class="sxs-lookup"><span data-stu-id="0ca34-133">String</span></span> | <span data-ttu-id="0ca34-134">Hachage Sha256 du contenu du fichier</span><span class="sxs-lookup"><span data-stu-id="0ca34-134">Sha256 hash of the file content</span></span> |
|<span data-ttu-id="0ca34-135">globalPrevalence</span><span class="sxs-lookup"><span data-stu-id="0ca34-135">globalPrevalence</span></span> | <span data-ttu-id="0ca34-136">Nullable long</span><span class="sxs-lookup"><span data-stu-id="0ca34-136">Nullable long</span></span> | <span data-ttu-id="0ca34-137">Prévalence des fichiers au sein de l’organisation</span><span class="sxs-lookup"><span data-stu-id="0ca34-137">File prevalence across organization</span></span> |
|<span data-ttu-id="0ca34-138">globalFirstObserved</span><span class="sxs-lookup"><span data-stu-id="0ca34-138">globalFirstObserved</span></span> | <span data-ttu-id="0ca34-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0ca34-139">DateTimeOffset</span></span> | <span data-ttu-id="0ca34-140">Première observation du fichier</span><span class="sxs-lookup"><span data-stu-id="0ca34-140">First time the file was observed</span></span> |
|<span data-ttu-id="0ca34-141">globalLastObserved</span><span class="sxs-lookup"><span data-stu-id="0ca34-141">globalLastObserved</span></span> | <span data-ttu-id="0ca34-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0ca34-142">DateTimeOffset</span></span> | <span data-ttu-id="0ca34-143">Dernière observation du fichier</span><span class="sxs-lookup"><span data-stu-id="0ca34-143">Last time the file was observed</span></span> |
|<span data-ttu-id="0ca34-144">size</span><span class="sxs-lookup"><span data-stu-id="0ca34-144">size</span></span> | <span data-ttu-id="0ca34-145">Nullable long</span><span class="sxs-lookup"><span data-stu-id="0ca34-145">Nullable long</span></span> | <span data-ttu-id="0ca34-146">Taille du fichier</span><span class="sxs-lookup"><span data-stu-id="0ca34-146">Size of the file</span></span> |
|<span data-ttu-id="0ca34-147">fileType</span><span class="sxs-lookup"><span data-stu-id="0ca34-147">fileType</span></span> | <span data-ttu-id="0ca34-148">Chaîne</span><span class="sxs-lookup"><span data-stu-id="0ca34-148">String</span></span> | <span data-ttu-id="0ca34-149">Type du fichier</span><span class="sxs-lookup"><span data-stu-id="0ca34-149">Type of the file</span></span> |
|<span data-ttu-id="0ca34-150">isPeFile</span><span class="sxs-lookup"><span data-stu-id="0ca34-150">isPeFile</span></span> | <span data-ttu-id="0ca34-151">Boolean</span><span class="sxs-lookup"><span data-stu-id="0ca34-151">Boolean</span></span> | <span data-ttu-id="0ca34-152">true si le fichier est portable exécutable (par exemple, « DLL », « EXE », etc.)</span><span class="sxs-lookup"><span data-stu-id="0ca34-152">true if the file is portable executable (e.g. "DLL", "EXE", etc.)</span></span> |
|<span data-ttu-id="0ca34-153">filePublisher</span><span class="sxs-lookup"><span data-stu-id="0ca34-153">filePublisher</span></span> | <span data-ttu-id="0ca34-154">Chaîne</span><span class="sxs-lookup"><span data-stu-id="0ca34-154">String</span></span> | <span data-ttu-id="0ca34-155">Éditeur de fichiers</span><span class="sxs-lookup"><span data-stu-id="0ca34-155">File publisher</span></span> |
|<span data-ttu-id="0ca34-156">fileProductName</span><span class="sxs-lookup"><span data-stu-id="0ca34-156">fileProductName</span></span> | <span data-ttu-id="0ca34-157">Chaîne</span><span class="sxs-lookup"><span data-stu-id="0ca34-157">String</span></span> | <span data-ttu-id="0ca34-158">Nom du produit</span><span class="sxs-lookup"><span data-stu-id="0ca34-158">Product name</span></span> |
|<span data-ttu-id="0ca34-159">signataire</span><span class="sxs-lookup"><span data-stu-id="0ca34-159">signer</span></span> | <span data-ttu-id="0ca34-160">Chaîne</span><span class="sxs-lookup"><span data-stu-id="0ca34-160">String</span></span> | <span data-ttu-id="0ca34-161">Signataire de fichiers</span><span class="sxs-lookup"><span data-stu-id="0ca34-161">File signer</span></span> |
|<span data-ttu-id="0ca34-162">émetteur</span><span class="sxs-lookup"><span data-stu-id="0ca34-162">issuer</span></span> | <span data-ttu-id="0ca34-163">Chaîne</span><span class="sxs-lookup"><span data-stu-id="0ca34-163">String</span></span> | <span data-ttu-id="0ca34-164">Émetteur de fichier</span><span class="sxs-lookup"><span data-stu-id="0ca34-164">File issuer</span></span> |
|<span data-ttu-id="0ca34-165">signerHash</span><span class="sxs-lookup"><span data-stu-id="0ca34-165">signerHash</span></span> | <span data-ttu-id="0ca34-166">Chaîne</span><span class="sxs-lookup"><span data-stu-id="0ca34-166">String</span></span> | <span data-ttu-id="0ca34-167">Hachage du certificat de signature</span><span class="sxs-lookup"><span data-stu-id="0ca34-167">Hash of the signing certificate</span></span> |
|<span data-ttu-id="0ca34-168">isValidCertificate</span><span class="sxs-lookup"><span data-stu-id="0ca34-168">isValidCertificate</span></span> | <span data-ttu-id="0ca34-169">Boolean</span><span class="sxs-lookup"><span data-stu-id="0ca34-169">Boolean</span></span> | <span data-ttu-id="0ca34-170">Le certificat de signature a été vérifié avec succès par l’agent Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="0ca34-170">Was signing certificate successfully verified by Microsoft Defender for Endpoint agent</span></span> |
|<span data-ttu-id="0ca34-171">determinationType</span><span class="sxs-lookup"><span data-stu-id="0ca34-171">determinationType</span></span> | <span data-ttu-id="0ca34-172">Chaîne</span><span class="sxs-lookup"><span data-stu-id="0ca34-172">String</span></span> | <span data-ttu-id="0ca34-173">Type de détermination du fichier</span><span class="sxs-lookup"><span data-stu-id="0ca34-173">The determination type of the file</span></span> |
|<span data-ttu-id="0ca34-174">determinationValue</span><span class="sxs-lookup"><span data-stu-id="0ca34-174">determinationValue</span></span> | <span data-ttu-id="0ca34-175">Chaîne</span><span class="sxs-lookup"><span data-stu-id="0ca34-175">String</span></span> | <span data-ttu-id="0ca34-176">Valeur de détermination</span><span class="sxs-lookup"><span data-stu-id="0ca34-176">Determination value</span></span> |


## <a name="json-representation"></a><span data-ttu-id="0ca34-177">Représentation Json</span><span class="sxs-lookup"><span data-stu-id="0ca34-177">Json representation</span></span>

```json
{
    "sha1": "4388963aaa83afe2042a46a3c017ad50bdcdafb3",
    "sha256": "413c58c8267d2c8648d8f6384bacc2ae9c929b2b96578b6860b5087cd1bd6462",
    "globalPrevalence": 180022,
    "globalFirstObserved": "2017-09-19T03:51:27.6785431Z",
    "globalLastObserved": "2020-01-06T03:59:21.3229314Z",
    "size": 22139496,
    "fileType": "APP",
    "isPeFile": true,
    "filePublisher": "CHENGDU YIWO Tech Development Co., Ltd.",
    "fileProductName": "EaseUS MobiSaver for Android",
    "signer": "CHENGDU YIWO Tech Development Co., Ltd.",
    "issuer": "VeriSign Class 3 Code Signing 2010 CA",
    "signerHash": "6c3245d4a9bc0244d99dff27af259cbbae2e2d16",
    "isValidCertificate": false,
    "determinationType": "Pua",
    "determinationValue": "PUA:Win32/FusionCore"
}
```
