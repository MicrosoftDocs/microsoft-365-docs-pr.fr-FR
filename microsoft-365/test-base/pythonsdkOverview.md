---
title: SDK de base de test pour Python
description: Informations sur la compréhension du SDK test base pour Python
search.appverid: MET150
author: mansipatel-usl
ms.author: mapatel
manager: rshastri
audience: Software-Vendor
ms.topic: article
ms.date: 07/06/2021
ms.service: virtual-desktop
localization_priority: Normal
ms.collection: TestBase-M365
ms.custom: ''
ms.reviewer: mapatel
f1.keywords: NOCSH
ms.openlocfilehash: c7f2d4b7b600e84b2ed35cce320dcb7d7191ecfc
ms.sourcegitcommit: b0f464b6300e2977ed51395473a6b2e02b18fc9e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "53322797"
---
# <a name="test-base-sdk-for-python"></a><span data-ttu-id="f01c7-103">SDK de base de test pour Python</span><span class="sxs-lookup"><span data-stu-id="f01c7-103">Test Base SDK for Python</span></span>

## <a name="overview"></a><span data-ttu-id="f01c7-104">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="f01c7-104">Overview</span></span>
<span data-ttu-id="f01c7-105">Le SDK de base de test peut être utilisé pour interagir avec la ressource de base de test Azure.</span><span class="sxs-lookup"><span data-stu-id="f01c7-105">The Test Base SDK can be used to interact with the Azure test base resource.</span></span> <span data-ttu-id="f01c7-106">(c’est-à-dire, gérer votre package d’application, inclure créer un package, modifier un package et supprimer un package)</span><span class="sxs-lookup"><span data-stu-id="f01c7-106">(i.e. manage your application package, include create package, edit package and delete package)</span></span>

<span data-ttu-id="f01c7-107">Avec le SDK, le résumé du test et le résultat d’analyse qui peuvent être obtenus incluent : scriptExecution, fiabilité, memoryUtilization, cpuUtilization, memoryRegression, cpuRegression.</span><span class="sxs-lookup"><span data-stu-id="f01c7-107">With the SDK, the test summary and Analysis Result which can be gotten include : scriptExecution, reliability, memoryUtilization, cpuUtilization, memoryRegression, cpuRegression.</span></span>

<span data-ttu-id="f01c7-108">Avec le SDK de base de test, vous pouvez intégrer la base de test dans votre pipeline CI/CD.</span><span class="sxs-lookup"><span data-stu-id="f01c7-108">With the Test Base SDK, you can integrate test base in your CI/CD pipeline.</span></span>

## <a name="client-library"></a><span data-ttu-id="f01c7-109">Bibliothèque cliente</span><span class="sxs-lookup"><span data-stu-id="f01c7-109">Client Library</span></span>

<span data-ttu-id="f01c7-110">Installez le package de base de test avec le pip.</span><span class="sxs-lookup"><span data-stu-id="f01c7-110">Install the test base package with pip.</span></span>

~~~
pip install  Microsoft.Testbase
~~~
 
## <a name="example"></a><span data-ttu-id="f01c7-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="f01c7-111">Example</span></span>
