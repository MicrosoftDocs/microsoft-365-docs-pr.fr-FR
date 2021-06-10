---
title: Répertorier les appareils exposés d’une activité de correction
description: Retourne des informations sur les appareils exposés pour la tâche de correction spécifiée.
keywords: api, correction, api de correction, obtenir, tâches de correction, correction des appareils exposés
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: v-jweston
author: jweston-1
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
MS.technology: mde
ms.custom: api
ms.openlocfilehash: 9b10659f76e5b05bea11f5c6c55ca7c2a34a2db5
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52772160"
---
# <a name="list-exposed-devices-of-one-remediation-activity"></a><span data-ttu-id="3ad33-104">Répertorier les appareils exposés d’une activité de correction</span><span class="sxs-lookup"><span data-stu-id="3ad33-104">List exposed devices of one remediation activity</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="3ad33-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3ad33-105">**Applies to:**</span></span>

- [<span data-ttu-id="3ad33-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3ad33-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="3ad33-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3ad33-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="3ad33-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="3ad33-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="3ad33-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="3ad33-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

[!include[Prerelease information](../../includes/prerelease.md)]

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="api-description"></a><span data-ttu-id="3ad33-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="3ad33-110">API Description</span></span>

<span data-ttu-id="3ad33-111">Retourne des informations sur les appareils exposés pour la tâche de correction spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3ad33-111">Returns information about exposed devices for the specified remediation task.</span></span>

<span data-ttu-id="3ad33-112">[En savoir plus sur les activités de correction.](tvm-remediation.md)</span><span class="sxs-lookup"><span data-stu-id="3ad33-112">[Learn more about remediation activities](tvm-remediation.md).</span></span>

## <a name="list-exposed-devices-associated-with-a-remediation-task-id"></a><span data-ttu-id="3ad33-113">Liste des appareils exposés associés à une tâche de correction (ID)</span><span class="sxs-lookup"><span data-stu-id="3ad33-113">List exposed devices associated with a remediation task (id)</span></span>

<span data-ttu-id="3ad33-114">**URL :** GET: /api/remediationTasks/ \{ id \} /machineReferences</span><span class="sxs-lookup"><span data-stu-id="3ad33-114">**URL:** GET: /api/remediationTasks/\{id\}/machineReferences</span></span>

## <a name="permissions"></a><span data-ttu-id="3ad33-115">Autorisations</span><span class="sxs-lookup"><span data-stu-id="3ad33-115">Permissions</span></span>

<span data-ttu-id="3ad33-116">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="3ad33-116">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="3ad33-117">Pour plus d’informations, notamment sur le choix des autorisations, voir Utiliser Microsoft Defender pour les API de point de [terminaison pour plus d’informations.](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="3ad33-117">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs for details.](apis-intro.md)</span></span>

<span data-ttu-id="3ad33-118">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="3ad33-118">Permission type</span></span> | <span data-ttu-id="3ad33-119">Autorisation</span><span class="sxs-lookup"><span data-stu-id="3ad33-119">Permission</span></span> | <span data-ttu-id="3ad33-120">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="3ad33-120">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="3ad33-121">Application</span><span class="sxs-lookup"><span data-stu-id="3ad33-121">Application</span></span> | <span data-ttu-id="3ad33-122">RemediationTask.Read.All</span><span class="sxs-lookup"><span data-stu-id="3ad33-122">RemediationTask.Read.All</span></span> | <span data-ttu-id="3ad33-123">\'Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités\'</span><span class="sxs-lookup"><span data-stu-id="3ad33-123">\'Read Threat and Vulnerability Management vulnerability information\'</span></span>
<span data-ttu-id="3ad33-124">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="3ad33-124">Delegated (work or school account)</span></span> | <span data-ttu-id="3ad33-125">RemediationTask.Read.Read</span><span class="sxs-lookup"><span data-stu-id="3ad33-125">RemediationTask.Read.Read</span></span> | <span data-ttu-id="3ad33-126">\'Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités\'</span><span class="sxs-lookup"><span data-stu-id="3ad33-126">\'Read Threat and Vulnerability Management vulnerability information\'</span></span>

## <a name="properties-details"></a><span data-ttu-id="3ad33-127">Détails des propriétés</span><span class="sxs-lookup"><span data-stu-id="3ad33-127">Properties details</span></span>

<span data-ttu-id="3ad33-128">Propriété (id)</span><span class="sxs-lookup"><span data-stu-id="3ad33-128">Property (id)</span></span> | <span data-ttu-id="3ad33-129">Type de données</span><span class="sxs-lookup"><span data-stu-id="3ad33-129">Data type</span></span> | <span data-ttu-id="3ad33-130">Description</span><span class="sxs-lookup"><span data-stu-id="3ad33-130">Description</span></span> | <span data-ttu-id="3ad33-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="3ad33-131">Example</span></span>
:---|:---|:---|:---
<span data-ttu-id="3ad33-132">id</span><span class="sxs-lookup"><span data-stu-id="3ad33-132">id</span></span> | <span data-ttu-id="3ad33-133">String</span><span class="sxs-lookup"><span data-stu-id="3ad33-133">String</span></span> | <span data-ttu-id="3ad33-134">ID d’appareil</span><span class="sxs-lookup"><span data-stu-id="3ad33-134">Device ID</span></span> | <span data-ttu-id="3ad33-135">w2957837fwda8w9ae7f023dba081059dw8d94503</span><span class="sxs-lookup"><span data-stu-id="3ad33-135">w2957837fwda8w9ae7f023dba081059dw8d94503</span></span>
<span data-ttu-id="3ad33-136">computerDnsName</span><span class="sxs-lookup"><span data-stu-id="3ad33-136">computerDnsName</span></span> | <span data-ttu-id="3ad33-137">String</span><span class="sxs-lookup"><span data-stu-id="3ad33-137">String</span></span> | <span data-ttu-id="3ad33-138">Nom du périphérique</span><span class="sxs-lookup"><span data-stu-id="3ad33-138">Device name</span></span> | <span data-ttu-id="3ad33-139">PC-SRV2012R2Foo.UserNameVldNet.local</span><span class="sxs-lookup"><span data-stu-id="3ad33-139">PC-SRV2012R2Foo.UserNameVldNet.local</span></span>
<span data-ttu-id="3ad33-140">osPlatform</span><span class="sxs-lookup"><span data-stu-id="3ad33-140">osPlatform</span></span> | <span data-ttu-id="3ad33-141">String</span><span class="sxs-lookup"><span data-stu-id="3ad33-141">String</span></span> | <span data-ttu-id="3ad33-142">Système d’exploitation d’appareil</span><span class="sxs-lookup"><span data-stu-id="3ad33-142">Device operating system</span></span> | <span data-ttu-id="3ad33-143">WindowsServer2012R2</span><span class="sxs-lookup"><span data-stu-id="3ad33-143">WindowsServer2012R2</span></span>
<span data-ttu-id="3ad33-144">rbacGroupName</span><span class="sxs-lookup"><span data-stu-id="3ad33-144">rbacGroupName</span></span> | <span data-ttu-id="3ad33-145">String</span><span class="sxs-lookup"><span data-stu-id="3ad33-145">String</span></span> | <span data-ttu-id="3ad33-146">Nom du groupe d’appareils associé à cet appareil</span><span class="sxs-lookup"><span data-stu-id="3ad33-146">Name of the device group this device is associated with</span></span> | <span data-ttu-id="3ad33-147">Serveurs</span><span class="sxs-lookup"><span data-stu-id="3ad33-147">Servers</span></span>

## <a name="example"></a><span data-ttu-id="3ad33-148">Exemple</span><span class="sxs-lookup"><span data-stu-id="3ad33-148">Example</span></span>

### <a name="request-example"></a><span data-ttu-id="3ad33-149">Exemple de requête</span><span class="sxs-lookup"><span data-stu-id="3ad33-149">Request example</span></span>

```http
GET https://api-luna.securitycenter.windows.com/api/remediationtasks/03942ef5-aecb-4c6e-b555-d6a97013844c/machinereferences
```

### <a name="response-example"></a><span data-ttu-id="3ad33-150">Exemple de réponse</span><span class="sxs-lookup"><span data-stu-id="3ad33-150">Response example</span></span>

```json
{
    "@odata.context": "https://wpatdadi-luna-stg.cloudapp.net/api/$metadata#MachineReferences",
    "value": [
        {
            "id": "3cb5df6bb3640a2d37ad09fcd357b182d684fafc",
            "computerDnsName": "ComputerPII_2ea21b2d97c9df23c143ad9e3e454cb674232529.DomainPII_21eed80b086e79bdfa178eabfa25e8be9acfa346.corp.contoso.com",
            "osPlatform": "WindowsServer2016",
            "rbacGroupName": "UnassignedGroup",
            
        },
        {
            "id": "3d9b1ca53e8f077199c7dcbfc9dbfa78f9bf1918",
            "computerDnsName": "ComputerPII_001d606fc149567c192747f48fae304b43c0ddba.DomainxPII_21eed80b086e79bdfa178eabfa25e8be9acfa346.corp.contoso.com",
            "osPlatform": "WindowsServer2012R2",
            "rbacGroupName": "UnassignedGroup",
            
        },
        {
            "id": "3db8b27e6172951d7ea2e2d75945abec56feaf82",
            "computerDnsName": "ComputerPII_ce60cfbjj4b82a091deb5eae560332bba99a9bd7.DomainPII_0bc1aee0fa396d175e514bd61a9e7a5b2b07ee8e.corp.contoso.com",
            "osPlatform": "WindowsServer2016",
            "rbacGroupName": "UnassignedGroup",
            
        },
        {
            "id": "3bad326dcda5b53fab47408cd4a7080f3f3cc8ab",
            "computerDnsName": "ComputerPII_b6b35960dd6539d1d1cef5ada02e235e7b357408.DomainPII_21eed80b089e76bdfa178eadfa25e8de9acfa346.corp.contoso.com",
            "osPlatform": "WindowsServer2012R2",
            "rbacGroupName": "UnassignedGroup",
            
        }
]
}
```

## <a name="see-also"></a><span data-ttu-id="3ad33-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ad33-151">See also</span></span>

- [<span data-ttu-id="3ad33-152">Méthodes et propriétés de correction</span><span class="sxs-lookup"><span data-stu-id="3ad33-152">Remediation methods and properties</span></span>](get-remediation-methods-properties.md)

- [<span data-ttu-id="3ad33-153">Obtenir une activité de correction par son ID</span><span class="sxs-lookup"><span data-stu-id="3ad33-153">Get one remediation activity by Id</span></span>](get-remediation-one-activity.md)

- [<span data-ttu-id="3ad33-154">Répertorier toutes les activités de correction</span><span class="sxs-lookup"><span data-stu-id="3ad33-154">List all remediation activities</span></span>](get-remediation-all-activities.md)

- [<span data-ttu-id="3ad33-155">Menaces basées sur les risques & gestion des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="3ad33-155">Risk-based threat & vulnerability management</span></span>](next-gen-threat-and-vuln-mgt.md)

- [<span data-ttu-id="3ad33-156">Vulnérabilités de votre organisation</span><span class="sxs-lookup"><span data-stu-id="3ad33-156">Vulnerabilities in your organization</span></span>](tvm-weaknesses.md)
