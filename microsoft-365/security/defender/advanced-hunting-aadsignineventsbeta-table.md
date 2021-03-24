---
title: Table AADSignInEventsBeta dans le schéma de recherche avancé
description: En savoir plus sur les informations associées à la table des événements de sign-in Azure Active Directory du schéma de recherche avancée
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema reference, kusto, table, column, data type, description, file, IP address, device, machine, user, account, identity, AAD
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: maccruz
author: schmurky
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: 7b595496c28710bfa25fc88653425242770bf57f
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51063617"
---
# <a name="aadsignineventsbeta"></a><span data-ttu-id="e7a96-104">AADSignInEventsBeta</span><span class="sxs-lookup"><span data-stu-id="e7a96-104">AADSignInEventsBeta</span></span>

<span data-ttu-id="e7a96-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e7a96-105">**Applies to:**</span></span>

- <span data-ttu-id="e7a96-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e7a96-106">Microsoft 365 Defender</span></span>

>[!IMPORTANT]
> <span data-ttu-id="e7a96-107">Le tableau est actuellement en version bêta et est proposé à court terme pour vous permettre de passer par les événements de signature `AADSignInEventsBeta` Azure Active Directory (AAD).</span><span class="sxs-lookup"><span data-stu-id="e7a96-107">The `AADSignInEventsBeta` table is currently in beta and is being offered on a short-term basis to allow you to hunt through Azure Active Directory (AAD) sign-in events.</span></span> <span data-ttu-id="e7a96-108">Nous finirons par déplacer toutes les informations de schéma de signature vers la `IdentityLogonEvents` table.</span><span class="sxs-lookup"><span data-stu-id="e7a96-108">We will eventually move all sign-in schema information to the `IdentityLogonEvents` table.</span></span><br><br>
> <span data-ttu-id="e7a96-109">Les clients qui peuvent accéder à Microsoft 365 Defender par le biais de la solution Microsoft Defender pour point de terminaison intégrée du Centre de sécurité Azure, mais qui n’ont pas de licences pour Microsoft Defender pour Office, Microsoft Defender pour l’identité ou Microsoft Cloud App Security, ne pourront pas afficher ce schéma.</span><span class="sxs-lookup"><span data-stu-id="e7a96-109">Customers who can access Microsoft 365 Defender through the Azure Security Center’s integrated Microsoft Defender for Endpoint solution, but do not have licenses for Microsoft Defender for Office, Microsoft Defender for Identity, or Microsoft Cloud App Security, will not be able to view this schema.</span></span> 

 

<span data-ttu-id="e7a96-110">Le tableau du schéma de recherche avancée contient des informations sur les cartes de visite interactives et `AADSignInEventsBeta` non interactives Azure Active Directory. En savoir plus sur les sign-ins dans les rapports [d’activité de sign-in Azure Active Directory - aperçu](/azure/active-directory/reports-monitoring/concept-all-sign-ins).</span><span class="sxs-lookup"><span data-stu-id="e7a96-110">The `AADSignInEventsBeta` table in the advanced hunting schema contains information about Azure Active Directory interactive and non-interactive sign-ins. Learn more about sign-ins in [Azure Active Directory sign-in activity reports - preview](/azure/active-directory/reports-monitoring/concept-all-sign-ins).</span></span>

<span data-ttu-id="e7a96-111">Utilisez cette référence pour créer des requêtes qui renvoient des informations de la table.</span><span class="sxs-lookup"><span data-stu-id="e7a96-111">Use this reference to construct queries that return information from the table.</span></span>
<span data-ttu-id="e7a96-112">Pour plus d’informations sur les autres tables du schéma de repérage avancé, consultez [la référence de repérage avancé](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-reference).</span><span class="sxs-lookup"><span data-stu-id="e7a96-112">For information on other tables in the advanced hunting schema, see [the advanced hunting reference](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-reference).</span></span>

 

 

| <span data-ttu-id="e7a96-113">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="e7a96-113">Column name</span></span>                 | <span data-ttu-id="e7a96-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="e7a96-114">Data type</span></span> | <span data-ttu-id="e7a96-115">Description</span><span class="sxs-lookup"><span data-stu-id="e7a96-115">Description</span></span>          |
|---------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `Timestamp`                       | <span data-ttu-id="e7a96-116">DateHeure</span><span class="sxs-lookup"><span data-stu-id="e7a96-116">datetime</span></span>      | <span data-ttu-id="e7a96-117">Date et heure de génération de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="e7a96-117">Date and time when the record was generated</span></span>                                                                                                                                         |
| `Application`                     | <span data-ttu-id="e7a96-118">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-118">string</span></span>        | <span data-ttu-id="e7a96-119">Application qui a effectué l’action enregistrée</span><span class="sxs-lookup"><span data-stu-id="e7a96-119">Application that performed the recorded action</span></span>                                                                                                                                       |
| `ApplicationId`                   | <span data-ttu-id="e7a96-120">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-120">string</span></span>        | <span data-ttu-id="e7a96-121">Identificateur unique de l’application</span><span class="sxs-lookup"><span data-stu-id="e7a96-121">Unique identifier for the application</span></span>                                                                                                                                               |
| `LogonType`                       | <span data-ttu-id="e7a96-122">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-122">string</span></span>        | <span data-ttu-id="e7a96-123">Type de session d’ouverture de session, spécifiquement interactive, interactive à distance (RDP), réseau, lot et service</span><span class="sxs-lookup"><span data-stu-id="e7a96-123">Type of logon session, specifically interactive, remote interactive (RDP), network, batch, and service</span></span>                                                                              |
| `ErrorCode`                       | <span data-ttu-id="e7a96-124">entier</span><span class="sxs-lookup"><span data-stu-id="e7a96-124">int</span></span>        | <span data-ttu-id="e7a96-125">Contient le code d’erreur si une erreur de se connecte se produit.</span><span class="sxs-lookup"><span data-stu-id="e7a96-125">Contains the error code if a sign-in error occurs.</span></span> <span data-ttu-id="e7a96-126">Pour trouver une description d’un code d’erreur spécifique, visitez <https://aka.ms/AADsigninsErrorCodes> .</span><span class="sxs-lookup"><span data-stu-id="e7a96-126">To find a description of a specific error code, visit <https://aka.ms/AADsigninsErrorCodes>.</span></span>                                     |
| `CorrelationId`                   | <span data-ttu-id="e7a96-127">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-127">string</span></span>        | <span data-ttu-id="e7a96-128">Identificateur unique de l’événement de signature</span><span class="sxs-lookup"><span data-stu-id="e7a96-128">Unique identifier of the sign-in event</span></span>                                                                                                                                              |
| `SessionId`                       | <span data-ttu-id="e7a96-129">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-129">string</span></span>        | <span data-ttu-id="e7a96-130">Numéro unique attribué à un utilisateur par le serveur d’un site web pour la durée de la visite ou de la session</span><span class="sxs-lookup"><span data-stu-id="e7a96-130">Unique number assigned to a user by a website's server for the duration of the visit or session</span></span>                                                                                     |
| `AccountDisplayName`              | <span data-ttu-id="e7a96-131">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-131">string</span></span>        | <span data-ttu-id="e7a96-132">Nom de l’utilisateur du compte affiché dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="e7a96-132">Name of the account user displayed in the address book.</span></span> <span data-ttu-id="e7a96-133">En règle générale, une combinaison d’un prénom ou d’un prénom donné, d’une initiale du deuxième prénom et d’un nom ou d’un nom de famille.</span><span class="sxs-lookup"><span data-stu-id="e7a96-133">Typically a combination of a given or first name, a middle initial, and a last name or surname.</span></span>                             |
| `AccountObjectId`                 | <span data-ttu-id="e7a96-134">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-134">string</span></span>        | <span data-ttu-id="e7a96-135">Identificateur unique du compte dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="e7a96-135">Unique identifier for the account in Azure AD</span></span>                                                                                                                                       |
| `AccountUpn`                      | <span data-ttu-id="e7a96-136">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-136">string</span></span>        | <span data-ttu-id="e7a96-137">Nom d’utilisateur principal (UPN) du compte</span><span class="sxs-lookup"><span data-stu-id="e7a96-137">User principal name (UPN) of the account</span></span>                                                                                                                                            |
| `IsExternalUser`                  | <span data-ttu-id="e7a96-138">entier</span><span class="sxs-lookup"><span data-stu-id="e7a96-138">int</span></span>        | <span data-ttu-id="e7a96-139">Indique si l’utilisateur qui s’est inscrit est externe.</span><span class="sxs-lookup"><span data-stu-id="e7a96-139">Indicates if the user that signed in is external.</span></span> <span data-ttu-id="e7a96-140">Valeurs possibles : -1 (non définie) , 0 (non externe), 1 (externe).</span><span class="sxs-lookup"><span data-stu-id="e7a96-140">Possible values: -1 (not set) , 0 (not external), 1 (external).</span></span>                                                                   |
| `IsGuestUser`                     | <span data-ttu-id="e7a96-141">booléen</span><span class="sxs-lookup"><span data-stu-id="e7a96-141">boolean</span></span>       | <span data-ttu-id="e7a96-142">Indique si l’utilisateur qui s’est inscrit est un invité dans le client</span><span class="sxs-lookup"><span data-stu-id="e7a96-142">Indicates whether the user that signed in is a guest in the tenant</span></span>                                                                                                                  |
| `AlternateSignInName`             | <span data-ttu-id="e7a96-143">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-143">string</span></span>        | <span data-ttu-id="e7a96-144">Nom d’utilisateur principal (UPN) local de l’utilisateur se signant à Azure AD</span><span class="sxs-lookup"><span data-stu-id="e7a96-144">On-premises user principal name (UPN) of the user signing in to Azure AD</span></span>                                                                                                            |
| `LastPasswordChangeTimestamp`     | <span data-ttu-id="e7a96-145">DateHeure</span><span class="sxs-lookup"><span data-stu-id="e7a96-145">datetime</span></span>        | <span data-ttu-id="e7a96-146">Date et heure de la dernière fois où l’utilisateur qui s’est inscrit a modifié son mot de passe</span><span class="sxs-lookup"><span data-stu-id="e7a96-146">Date and time when the user that signed in last changed their password</span></span>                                                                                                              |
| `ResourceDisplayName`             | <span data-ttu-id="e7a96-147">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-147">string</span></span>        | <span data-ttu-id="e7a96-148">Nom d’affichage de la ressource accessible</span><span class="sxs-lookup"><span data-stu-id="e7a96-148">Display name of the resource accessed</span></span>                                                                                                                                               |
| `ResourceId`                      | <span data-ttu-id="e7a96-149">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-149">string</span></span>        | <span data-ttu-id="e7a96-150">Identificateur unique de la ressource accessible</span><span class="sxs-lookup"><span data-stu-id="e7a96-150">Unique identifier of the resource accessed</span></span>                                                                                                                                          |
| `ResourceTenantId`                | <span data-ttu-id="e7a96-151">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-151">string</span></span>        | <span data-ttu-id="e7a96-152">Identificateur unique du client de la ressource à accès</span><span class="sxs-lookup"><span data-stu-id="e7a96-152">Unique identifier of the tenant of the resource accessed</span></span>                                                                                                                            |
| `DeviceName`                      | <span data-ttu-id="e7a96-153">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-153">string</span></span>        | <span data-ttu-id="e7a96-154">Nom de domaine complet (FQDN) de la machine</span><span class="sxs-lookup"><span data-stu-id="e7a96-154">Fully qualified domain name (FQDN) of the machine</span></span>                                                                                                                                   |
| `AadDeviceId`                     | <span data-ttu-id="e7a96-155">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-155">string</span></span>   |      <span data-ttu-id="e7a96-156">Identificateur unique de l’appareil dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="e7a96-156">Unique identifier for the device in Azure AD</span></span>                                                                                                                                                                               |
| `OSPlatform`                      | <span data-ttu-id="e7a96-157">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-157">string</span></span>        | <span data-ttu-id="e7a96-158">Plateforme du système d’exploitation client s’exécutant sur la machine.</span><span class="sxs-lookup"><span data-stu-id="e7a96-158">Platform of the operating system running on the machine.</span></span> <span data-ttu-id="e7a96-159">Cela indique des systèmes d’exploitation spécifiques, y compris des variantes au sein d’une même famille, telles que Windows 10 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e7a96-159">This indicates specific operating systems, including variations within the same family, such as Windows 10 and Windows 7.</span></span>  |
| `DeviceTrustType`                 | <span data-ttu-id="e7a96-160">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-160">string</span></span>        | <span data-ttu-id="e7a96-161">Indique le type d’confiance de l’appareil qui s’est connecté.</span><span class="sxs-lookup"><span data-stu-id="e7a96-161">Indicates the trust type of the device that signed in.</span></span> <span data-ttu-id="e7a96-162">Pour les scénarios d’appareil géré uniquement.</span><span class="sxs-lookup"><span data-stu-id="e7a96-162">For managed device scenarios only.</span></span> <span data-ttu-id="e7a96-163">Les valeurs possibles sont Workplace, AzureAd et ServerAd.</span><span class="sxs-lookup"><span data-stu-id="e7a96-163">Possible values are Workplace, AzureAd, and ServerAd.</span></span>                                     |
| `IsManaged`                       | <span data-ttu-id="e7a96-164">entier</span><span class="sxs-lookup"><span data-stu-id="e7a96-164">int</span></span>       | <span data-ttu-id="e7a96-165">Indique si l’appareil à l’origine de la connectez-vous est un appareil géré (1) ou non un appareil géré (0)</span><span class="sxs-lookup"><span data-stu-id="e7a96-165">Indicates whether the device that initiated the sign-in is a managed device (1) or not a managed device (0)</span></span>                                                                         |
| `IsCompliant`                     | <span data-ttu-id="e7a96-166">entier</span><span class="sxs-lookup"><span data-stu-id="e7a96-166">int</span></span>       | <span data-ttu-id="e7a96-167">Indique si l’appareil à l’origine de la signature est conforme (1) ou non conforme (0)</span><span class="sxs-lookup"><span data-stu-id="e7a96-167">Indicates whether the device that initiated the sign-in is compliant (1) or non-compliant (0)</span></span>                                                                                       |
| `AuthenticationProcessingDetails` | <span data-ttu-id="e7a96-168">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-168">string</span></span>        | <span data-ttu-id="e7a96-169">Détails sur le processeur d’authentification</span><span class="sxs-lookup"><span data-stu-id="e7a96-169">Details about the authentication processor</span></span>                                                                                                                                          |
| `AuthenticationRequirement`       | <span data-ttu-id="e7a96-170">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-170">string</span></span>        | <span data-ttu-id="e7a96-171">Type d’authentification requis pour la signature.</span><span class="sxs-lookup"><span data-stu-id="e7a96-171">Type of authentication required for the sign-in.</span></span> <span data-ttu-id="e7a96-172">Valeurs possibles : multiFactorAuthentication (l’authentification multifacteur était requise) et singleFactorAuthentication (aucune authentification multifacteur n’était requise).</span><span class="sxs-lookup"><span data-stu-id="e7a96-172">Possible values: multiFactorAuthentication (MFA was required) and singleFactorAuthentication (no MFA was required).</span></span>                |
| `TokenIssuerType`                 | <span data-ttu-id="e7a96-173">entier</span><span class="sxs-lookup"><span data-stu-id="e7a96-173">int</span></span>        | <span data-ttu-id="e7a96-174">Indique si l’émetteur de jeton est Azure Active Directory (0) ou services de fédération Active Directory (1)</span><span class="sxs-lookup"><span data-stu-id="e7a96-174">Indicates if the token issuer is Azure Active Directory (0) or Active Directory Federation Services (1)</span></span>                                                                             |
| `RiskLevelAggregated`                       | <span data-ttu-id="e7a96-175">entier</span><span class="sxs-lookup"><span data-stu-id="e7a96-175">int</span></span>        | <span data-ttu-id="e7a96-176">Niveau de risque agrégé lors de la signature.</span><span class="sxs-lookup"><span data-stu-id="e7a96-176">Aggregated risk level during sign-in.</span></span> <span data-ttu-id="e7a96-177">Valeurs possibles : 0 (niveau de risque agrégé non définie), 1 (aucun), 10 (faible), 50 (moyen) ou 100 (élevé).</span><span class="sxs-lookup"><span data-stu-id="e7a96-177">Possible values: 0 (aggregated risk level not set), 1 (none), 10 (low), 50 (medium), or 100 (high).</span></span>                               |
| `RiskDetails`                      | <span data-ttu-id="e7a96-178">entier</span><span class="sxs-lookup"><span data-stu-id="e7a96-178">int</span></span>        | <span data-ttu-id="e7a96-179">Détails sur l’état à risque de l’utilisateur qui s’est inscrit</span><span class="sxs-lookup"><span data-stu-id="e7a96-179">Details about the risky state of the user that signed in</span></span>                                                                                                                            |
| `RiskState`                       | <span data-ttu-id="e7a96-180">entier</span><span class="sxs-lookup"><span data-stu-id="e7a96-180">int</span></span>        | <span data-ttu-id="e7a96-181">Indique l’état de l’utilisateur à risque.</span><span class="sxs-lookup"><span data-stu-id="e7a96-181">Indicates risky user state.</span></span> <span data-ttu-id="e7a96-182">Valeurs possibles : 0 (aucun), 1 (sécurisé confirmé), 2 (corrigé), 3 (rejeté), 4 (à risque) ou 5 (confirmé compromis).</span><span class="sxs-lookup"><span data-stu-id="e7a96-182">Possible values: 0 (none), 1 (confirmed safe), 2 (remediated), 3 (dismissed), 4 (at risk), or 5 (confirmed compromised).</span></span>                                |
| `UserAgent`                       | <span data-ttu-id="e7a96-183">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-183">string</span></span>        | <span data-ttu-id="e7a96-184">Informations sur l’agent utilisateur à partir du navigateur web ou d’une autre application cliente</span><span class="sxs-lookup"><span data-stu-id="e7a96-184">User agent information from the web browser or other client application</span></span>                                                                                                             |
| `ClientAppUsed`                   | <span data-ttu-id="e7a96-185">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-185">string</span></span>        | <span data-ttu-id="e7a96-186">Indique l’application cliente utilisée</span><span class="sxs-lookup"><span data-stu-id="e7a96-186">Indicates the client app used</span></span>                                                                                                                                                       |
| `Browser`                         | <span data-ttu-id="e7a96-187">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-187">string</span></span>        | <span data-ttu-id="e7a96-188">Détails sur la version du navigateur utilisé pour se connecter</span><span class="sxs-lookup"><span data-stu-id="e7a96-188">Details about the version of the browser used to sign in</span></span>                                                                                                                            |
| `ConditionalAccessPolicies`       | <span data-ttu-id="e7a96-189">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-189">string</span></span>        | <span data-ttu-id="e7a96-190">Détails des stratégies d’accès conditionnel appliquées à l’événement de signature</span><span class="sxs-lookup"><span data-stu-id="e7a96-190">Details of the conditional access policies applied to the sign-in event</span></span>                                                                                                             |
| `ConditionalAccessStatus`         | <span data-ttu-id="e7a96-191">entier</span><span class="sxs-lookup"><span data-stu-id="e7a96-191">int</span></span>        | <span data-ttu-id="e7a96-192">État des stratégies d’accès conditionnel appliquées à la signature.</span><span class="sxs-lookup"><span data-stu-id="e7a96-192">Status of the conditional access policies applied to the sign-in.</span></span> <span data-ttu-id="e7a96-193">Les valeurs possibles sont 0 (stratégies appliquées), 1 (échec de tentative d’application des stratégies) ou 2 (stratégies non appliquées).</span><span class="sxs-lookup"><span data-stu-id="e7a96-193">Possible values are 0 (policies applied), 1 (attempt to apply policies failed), or 2 (policies not applied).</span></span>      |
| `IPAddress`                       | <span data-ttu-id="e7a96-194">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-194">string</span></span>        | <span data-ttu-id="e7a96-195">Adresse IP attribuée au point de terminaison et utilisée lors des communications réseau associées</span><span class="sxs-lookup"><span data-stu-id="e7a96-195">IP address assigned to the endpoint and used during related network communications</span></span>                                                                                                  |
| `Country`                     | <span data-ttu-id="e7a96-196">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-196">string</span></span>        | <span data-ttu-id="e7a96-197">Code à deux lettres indiquant le pays où l’adresse IP du client est géolocalisé</span><span class="sxs-lookup"><span data-stu-id="e7a96-197">Two-letter code indicating the country where the client IP address is geolocated</span></span>                                                                                                    |
| `State`                           | <span data-ttu-id="e7a96-198">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-198">string</span></span>        | <span data-ttu-id="e7a96-199">État où la se connecte s’est produite, si disponible</span><span class="sxs-lookup"><span data-stu-id="e7a96-199">State where the sign-in occurred, if available</span></span>                                                                                                                                      |
| `City`                            | <span data-ttu-id="e7a96-200">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-200">string</span></span>        | <span data-ttu-id="e7a96-201">Ville où se trouve l’utilisateur du compte</span><span class="sxs-lookup"><span data-stu-id="e7a96-201">City where the account user is located</span></span>                                                                                                                                              |
| `Latitude`                        | <span data-ttu-id="e7a96-202">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-202">string</span></span>        | <span data-ttu-id="e7a96-203">Coordonnées nord à sud de l’emplacement de la signature</span><span class="sxs-lookup"><span data-stu-id="e7a96-203">The north to south coordinates of the sign-in location</span></span>                                                                                                                              |
| `Longitude`                       | <span data-ttu-id="e7a96-204">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-204">string</span></span>        | <span data-ttu-id="e7a96-205">Coordonnées est à ouest de l’emplacement de la signature</span><span class="sxs-lookup"><span data-stu-id="e7a96-205">The east to west coordinates of the sign-in location</span></span>                                                                                                                                |
| `NetworkLocationDetails`          | <span data-ttu-id="e7a96-206">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-206">string</span></span>        | <span data-ttu-id="e7a96-207">Détails de l’emplacement réseau du processeur d’authentification de l’événement de authentification</span><span class="sxs-lookup"><span data-stu-id="e7a96-207">Network location details of the authentication processor of the sign-in event</span></span>                                                                                                       |
| `RequestId`                       | <span data-ttu-id="e7a96-208">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-208">string</span></span>        |  <span data-ttu-id="e7a96-209">Identificateur unique de la demande</span><span class="sxs-lookup"><span data-stu-id="e7a96-209">Unique identifier of the request</span></span>                                                                                                                                                   |
|`ReportId` | <span data-ttu-id="e7a96-210">string</span><span class="sxs-lookup"><span data-stu-id="e7a96-210">string</span></span> | <span data-ttu-id="e7a96-211">Identificateur unique de l’événement</span><span class="sxs-lookup"><span data-stu-id="e7a96-211">Unique identifier for the event</span></span> |

 

 

## <a name="related-articles"></a><span data-ttu-id="e7a96-212">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="e7a96-212">Related articles</span></span>

-   [<span data-ttu-id="e7a96-213">AADSpnSignInEventsBeta</span><span class="sxs-lookup"><span data-stu-id="e7a96-213">AADSpnSignInEventsBeta</span></span>](./advanced-hunting-aadspnsignineventsbeta-table.md)
-   [<span data-ttu-id="e7a96-214">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="e7a96-214">Advanced hunting overview</span></span>](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-overview)
-   [<span data-ttu-id="e7a96-215">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="e7a96-215">Learn the query language</span></span>](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-query-language)
-   [<span data-ttu-id="e7a96-216">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="e7a96-216">Understand the schema</span></span>](/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-schema-reference)

 