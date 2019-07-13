---
title: Détails du client Azure Active Directory
description: Cette rubrique décrit les modifications apportées à votre compte AAD lors de l’inscription dans le bureau géré Microsoft
keywords: Microsoft Managed Desktop, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.openlocfilehash: 6b2b30d8dedba1086bfa9268fb0fdbce20367c20
ms.sourcegitcommit: dd426c686b52cf79325f11022b2d99bc45285577
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/12/2019
ms.locfileid: "35643945"
---
# <a name="azure-active-directory-tenant-details"></a><span data-ttu-id="e155d-104">Détails du client Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="e155d-104">Azure Active Directory tenant details</span></span>
<span data-ttu-id="e155d-105">{Gory détails sur les comptes, les appels d’API, les perms, etc., etc.}</span><span class="sxs-lookup"><span data-stu-id="e155d-105">{gory details about accounts, API calls, perms, etc., etc.}</span></span>


## <a name="data-transmitted-to-and-from-your-aad-account"></a><span data-ttu-id="e155d-106">Données transmises vers et à partir de votre compte AAD</span><span class="sxs-lookup"><span data-stu-id="e155d-106">Data transmitted to and from your AAD account</span></span>


<span data-ttu-id="e155d-107">Données envoyées à votre compte à partir de Microsoft:</span><span class="sxs-lookup"><span data-stu-id="e155d-107">Data sent to your account from Microsoft:</span></span>

- <span data-ttu-id="e155d-108">Noms de groupes</span><span class="sxs-lookup"><span data-stu-id="e155d-108">Group names</span></span>
- <span data-ttu-id="e155d-109">Configuration de la stratégie de sécurité</span><span class="sxs-lookup"><span data-stu-id="e155d-109">Security policy configuration</span></span>
- <span data-ttu-id="e155d-110">Commandes de l’appareil</span><span class="sxs-lookup"><span data-stu-id="e155d-110">Device orders</span></span>
- <span data-ttu-id="e155d-111">Comptes d’utilisateur (msadmin, MSTest, mwaas_soc_ro, mwaas_wdgsoc)</span><span class="sxs-lookup"><span data-stu-id="e155d-111">User accounts (msadmin, mstest, mwaas_soc_ro, mwaas_wdgsoc)</span></span>
- <span data-ttu-id="e155d-112">Affectation de licences E5 aux comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="e155d-112">E5 License assignment to the user accounts</span></span>
- <span data-ttu-id="e155d-113">Stratégies de mise à jour Windows pour les sonneries de mise à jour</span><span class="sxs-lookup"><span data-stu-id="e155d-113">Windows update policies for update rings</span></span>

<span data-ttu-id="e155d-114">Données envoyées à Microsoft à partir de votre compte:</span><span class="sxs-lookup"><span data-stu-id="e155d-114">Data sent to Microsoft from your account:</span></span>

- <span data-ttu-id="e155d-115">Données de mise à jour des périphériques, d’utilisation et de fiabilité</span><span class="sxs-lookup"><span data-stu-id="e155d-115">Device update, usage and reliability data</span></span>
- <span data-ttu-id="e155d-116">Données de fiabilité et de déploiement d’application</span><span class="sxs-lookup"><span data-stu-id="e155d-116">App deployment and reliability data</span></span>
- <span data-ttu-id="e155d-117">Mise à jour et données de déploiement de stratégie de sécurité</span><span class="sxs-lookup"><span data-stu-id="e155d-117">Update and security policy deployment data</span></span>
- <span data-ttu-id="e155d-118">Utilisateurs affectés aux appareils</span><span class="sxs-lookup"><span data-stu-id="e155d-118">Users assigned to devices</span></span>  

<span data-ttu-id="e155d-119">Les données transmises à partir de votre compte sont stockées dans des bases de données SQL Azure dans le client Microsoft hébergé aux États-Unis.</span><span class="sxs-lookup"><span data-stu-id="e155d-119">Data transmitted from your account is stored in Azure SQL databases in the Microsoft tenant hosted in the USA.</span></span> <span data-ttu-id="e155d-120">Les données sont stockées et gérées conformément aux stratégies décrites dans {Microsoft Azure Security}.</span><span class="sxs-lookup"><span data-stu-id="e155d-120">Data is stored and handled in accordance the policies described in {Microsoft Azure security}.</span></span> 

## <a name="api-permissions-and-calls"></a><span data-ttu-id="e155d-121">Autorisations et appels d’API</span><span class="sxs-lookup"><span data-stu-id="e155d-121">API permissions and calls</span></span>

<span data-ttu-id="e155d-122">**Lors de l’enregistrement:**</span><span class="sxs-lookup"><span data-stu-id="e155d-122">**During enrollment:**</span></span>

<span data-ttu-id="e155d-123">Autorisations d’API:</span><span class="sxs-lookup"><span data-stu-id="e155d-123">API permissions:</span></span>
- <span data-ttu-id="e155d-124">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e155d-124">DeviceManagementServiceConfig.ReadWrite.All</span></span>
- <span data-ttu-id="e155d-125">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="e155d-125">Directory.AccessAsUser.All</span></span>
- <span data-ttu-id="e155d-126">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e155d-126">User.ReadWrite.All</span></span>
- <span data-ttu-id="e155d-127">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e155d-127">DeviceManagementConfiguration.ReadWrite.All</span></span>
- <span data-ttu-id="e155d-128">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e155d-128">DeviceManagementManagedDevices.ReadWrite.All</span></span>
- <span data-ttu-id="e155d-129">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e155d-129">Group.ReadWrite.All</span></span>

<span data-ttu-id="e155d-130">Appels d’API:</span><span class="sxs-lookup"><span data-stu-id="e155d-130">API calls:</span></span>
- <span data-ttu-id="e155d-131">POST/organization/{organizationId}/setMobileDeviceManagementAuthority</span><span class="sxs-lookup"><span data-stu-id="e155d-131">POST /organization/{organizationId}/setMobileDeviceManagementAuthority</span></span>
- <span data-ttu-id="e155d-132">GET/POST/directoryRoles/{id}/members</span><span class="sxs-lookup"><span data-stu-id="e155d-132">GET/POST /directoryRoles/{id}/members</span></span>
- <span data-ttu-id="e155d-133">GET/POST/Users</span><span class="sxs-lookup"><span data-stu-id="e155d-133">GET/POST /users</span></span>
- <span data-ttu-id="e155d-134">GET/POST/Groups</span><span class="sxs-lookup"><span data-stu-id="e155d-134">GET/POST /groups</span></span>
- <span data-ttu-id="e155d-135">CORRECTIF/Groups/{ID}</span><span class="sxs-lookup"><span data-stu-id="e155d-135">PATCH /groups/{id}</span></span>
- <span data-ttu-id="e155d-136">GET/POST/deviceManagement/deviceConfigurations</span><span class="sxs-lookup"><span data-stu-id="e155d-136">GET/POST /deviceManagement/deviceConfigurations</span></span>
- <span data-ttu-id="e155d-137">OBTENIR/deviceManagement/detectedApps</span><span class="sxs-lookup"><span data-stu-id="e155d-137">GET /deviceManagement/detectedApps</span></span>

<span data-ttu-id="e155d-138">**Après l’enregistrement, lors de la gestion ordinaire:**</span><span class="sxs-lookup"><span data-stu-id="e155d-138">**After enrollment, during ordinary management:**</span></span>

<span data-ttu-id="e155d-139">Autorisations d’API:</span><span class="sxs-lookup"><span data-stu-id="e155d-139">API permissions:</span></span>
- <span data-ttu-id="e155d-140">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e155d-140">DeviceManagementManagedDevices.ReadWrite.All</span></span>
- <span data-ttu-id="e155d-141">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e155d-141">DeviceManagementApps.ReadWrite.All</span></span>
- <span data-ttu-id="e155d-142">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e155d-142">DeviceManagementConfiguration.ReadWrite.All</span></span>
- <span data-ttu-id="e155d-143">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="e155d-143">Reports.Read.All</span></span>
- <span data-ttu-id="e155d-144">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e155d-144">User.ReadWrite.All</span></span>
- <span data-ttu-id="e155d-145">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e155d-145">Group.ReadWrite.All</span></span>
- <span data-ttu-id="e155d-146">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="e155d-146">Directory.AccessAsUser.All</span></span>

<span data-ttu-id="e155d-147">Appels d’API:</span><span class="sxs-lookup"><span data-stu-id="e155d-147">API calls:</span></span>
- <span data-ttu-id="e155d-148">GET/POST/directoryRoles/{id}/members</span><span class="sxs-lookup"><span data-stu-id="e155d-148">GET/POST /directoryRoles/{id}/members</span></span>
- <span data-ttu-id="e155d-149">GET/PATCH/POST/Users</span><span class="sxs-lookup"><span data-stu-id="e155d-149">GET/PATCH/POST /users</span></span>
- <span data-ttu-id="e155d-150">GET/POST/Groups</span><span class="sxs-lookup"><span data-stu-id="e155d-150">GET/POST /groups</span></span>
- <span data-ttu-id="e155d-151">CORRECTIF/Groups/{ID}</span><span class="sxs-lookup"><span data-stu-id="e155d-151">PATCH /groups/{id}</span></span>
- <span data-ttu-id="e155d-152">GET/POST/deviceManagement/deviceConfigurations</span><span class="sxs-lookup"><span data-stu-id="e155d-152">GET/POST /deviceManagement/deviceConfigurations</span></span>
- <span data-ttu-id="e155d-153">GET/POST/deviceAppManagement/mobileApps</span><span class="sxs-lookup"><span data-stu-id="e155d-153">GET/POST /deviceAppManagement/mobileApps</span></span>
- <span data-ttu-id="e155d-154">OBTENIR/deviceManagement/detectedApps</span><span class="sxs-lookup"><span data-stu-id="e155d-154">GET /deviceManagement/detectedApps</span></span>
- <span data-ttu-id="e155d-155">OBTENIR/Devices</span><span class="sxs-lookup"><span data-stu-id="e155d-155">GET /devices</span></span>
- <span data-ttu-id="e155d-156">POST/Users/{ID | userPrincipalName}/assignLicense</span><span class="sxs-lookup"><span data-stu-id="e155d-156">POST /users/{id | userPrincipalName}/assignLicense</span></span>
- <span data-ttu-id="e155d-157">OBTENIR/subscribedSkus</span><span class="sxs-lookup"><span data-stu-id="e155d-157">GET /subscribedSkus</span></span>

## <a name="accounts-used-by-microsoft-managed-desktop"></a><span data-ttu-id="e155d-158">Comptes utilisés par le bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="e155d-158">Accounts used by Microsoft Managed Desktop</span></span>





| <span data-ttu-id="e155d-159">Compte</span><span class="sxs-lookup"><span data-stu-id="e155d-159">Account</span></span> | <span data-ttu-id="e155d-160">Description</span><span class="sxs-lookup"><span data-stu-id="e155d-160">Description</span></span>  | <span data-ttu-id="e155d-161">Accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="e155d-161">Conditional access</span></span>  | <span data-ttu-id="e155d-162">	Authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="e155d-162">Multi-factor authentication</span></span>  | <span data-ttu-id="e155d-163">Pourquoi cela est-il correct?</span><span class="sxs-lookup"><span data-stu-id="e155d-163">Why this is OK</span></span> |
|---------|---------|---------|---------|--------------|
| <span data-ttu-id="e155d-164">msadmin @ \* onmmicrosoft. com</span><span class="sxs-lookup"><span data-stu-id="e155d-164">msadmin@\*onmmicrosoft.com</span></span> | <span data-ttu-id="e155d-165">Compte de service limité avec des privilèges d’administrateur, utilisé en tant qu’utilisateur Microsoft Intune et administrateur d’utilisateurs {qu’est-ce que c’est?}</span><span class="sxs-lookup"><span data-stu-id="e155d-165">Limited service account with administrator privileges, used as a Microsoft Intune and User administrator {what's this?}</span></span> <span data-ttu-id="e155d-166">pour définir et configurer le client pour les appareils de bureau modernes Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e155d-166">to define and configure the tenant for Microsoft Modern Desktop devices.</span></span><span data-ttu-id="e155d-167">Ne dispose pas d’autorisations de connexion interactive; effectue des opérations uniquement via le service.</span><span class="sxs-lookup"><span data-stu-id="e155d-167">  Does not have interactive login permissions; performs operations only through the service.</span></span>  | <span data-ttu-id="e155d-168">Exclus, car il ne provient pas de votre réseau</span><span class="sxs-lookup"><span data-stu-id="e155d-168">Excluded, because it doesn't originate in your network</span></span>        | <span data-ttu-id="e155d-169">Exclu car il n’existe aucune ouverture de session interactive</span><span class="sxs-lookup"><span data-stu-id="e155d-169">Excluded because there is no interactive logon</span></span>        | <span data-ttu-id="e155d-170">Mot de passe stocké dans Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="e155d-170">Password stored in Azure Key Vault</span></span> |
| <span data-ttu-id="e155d-171">MSTest @ \* onmmicrosoft. com</span><span class="sxs-lookup"><span data-stu-id="e155d-171">mstest@\*onmmicrosoft.com</span></span>     |         |         |         |
| <span data-ttu-id="e155d-172">mssupport @ \* onmmicrosoft. com</span><span class="sxs-lookup"><span data-stu-id="e155d-172">mssupport@\*onmmicrosoft.com</span></span>     |         |         |         |
| <span data-ttu-id="e155d-173">msadminint @ \* onmmicrosoft. com</span><span class="sxs-lookup"><span data-stu-id="e155d-173">msadminint@\*onmmicrosoft.com</span></span>     |         |         |         |
