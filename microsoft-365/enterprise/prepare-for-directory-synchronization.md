---
title: Préparer la synchronisation d'annuaires pour Microsoft 365
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/30/2020
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
f1.keywords:
- CSH
ms.custom:
- Adm_O365
- O365p_AddUsersWithDirSync
- O365M_AddUsersWithDirSync
- O365E_HRCSetupAADConnectAboutLM617031
- O365E_AddUsersWithDirSync
ms.collection:
- Ent_O365
- M365-identity-device-management
search.appverid:
- MET150
- MOP150
- MOE150
- MBS150
ms.assetid: 01920974-9e6f-4331-a370-13aea4e82b3e
description: Décrit comment préparer la mise en service des utilisateurs à Microsoft 365 à l’aide de la synchronisation d’annuaires et des avantages à long terme de cette méthode.
ms.openlocfilehash: b74310b0f444da118699c5ad5fbb68b15519b830
ms.sourcegitcommit: 45c0afcf958069c5c1b31f9b6c762d8dd806e1e9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2020
ms.locfileid: "48773984"
---
# <a name="prepare-for-directory-synchronization-to-microsoft-365"></a><span data-ttu-id="7bba3-103">Préparer la synchronisation d'annuaires pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7bba3-103">Prepare for directory synchronization to Microsoft 365</span></span>

<span data-ttu-id="7bba3-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="7bba3-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="7bba3-105">Les avantages de la synchronisation hybride des identités et des annuaires de votre organisation sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="7bba3-105">The benefits to hybrid identity and directory synchronization your organization include:</span></span>

- <span data-ttu-id="7bba3-106">Réduction des programmes d’administration au sein de votre organisation</span><span class="sxs-lookup"><span data-stu-id="7bba3-106">Reducing the administrative programs in your organization</span></span>
- <span data-ttu-id="7bba3-107">Activer le scénario d’authentification unique (facultatif)</span><span class="sxs-lookup"><span data-stu-id="7bba3-107">Optionally enabling single sign-on scenario</span></span>
- <span data-ttu-id="7bba3-108">Automatisation des modifications de compte dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7bba3-108">Automating account changes in Microsoft 365</span></span>

<span data-ttu-id="7bba3-109">Pour plus d’informations sur les avantages liés à l’utilisation de la synchronisation d’annuaires, voir [Hybrid Identity with Azure Active Directory (Azure AD)](https://go.microsoft.com/fwlink/p/?LinkId=525398) et [Hybrid Identity for Microsoft 365](plan-for-directory-synchronization.md).</span><span class="sxs-lookup"><span data-stu-id="7bba3-109">For more information about the advantages of using directory synchronization, see [hybrid identity with Azure Active Directory (Azure AD)](https://go.microsoft.com/fwlink/p/?LinkId=525398) and [hybrid identity for Microsoft 365](plan-for-directory-synchronization.md).</span></span>

<span data-ttu-id="7bba3-110">Toutefois, la synchronisation d’annuaires nécessite une planification et une préparation pour garantir la synchronisation des services de domaine Active Directory (AD DS) avec le client Azure AD de votre abonnement Microsoft 365 avec un minimum d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="7bba3-110">However, directory synchronization requires planning and preparation to ensure that your Active Directory Domain Services (AD DS) synchronizes to the Azure AD tenant of your Microsoft 365 subscription with a minimum of errors.</span></span>

<span data-ttu-id="7bba3-111">Suivez les étapes ci-dessous pour obtenir les meilleurs résultats.</span><span class="sxs-lookup"><span data-stu-id="7bba3-111">Follow these steps in order for the best results.</span></span>

## <a name="1-directory-cleanup-tasks"></a><span data-ttu-id="7bba3-112">1. tâches de nettoyage d’annuaire</span><span class="sxs-lookup"><span data-stu-id="7bba3-112">1. Directory cleanup tasks</span></span>

<span data-ttu-id="7bba3-113">Avant de synchroniser vos services AD DS avec votre client Azure AD, vous devez nettoyer votre service AD DS.</span><span class="sxs-lookup"><span data-stu-id="7bba3-113">Before you synchronize your AD DS to your Azure AD tenant, you need to clean up your AD DS.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7bba3-114">Si vous n’effectuez pas de nettoyage AD DS avant de procéder à la synchronisation, cela peut entraîner un impact négatif important sur le processus de déploiement.</span><span class="sxs-lookup"><span data-stu-id="7bba3-114">If you don't perform AD DS cleanup before you synchronize, it can lead to a significant negative impact on the deployment process.</span></span> <span data-ttu-id="7bba3-115">Cela peut prendre des jours, voire des semaines, pour parcourir le cycle de synchronisation d’annuaires, l’identification des erreurs et la resynchronisation.</span><span class="sxs-lookup"><span data-stu-id="7bba3-115">It might take days, or even weeks, to go through the cycle of directory synchronization, identifying errors, and re-synchronization.</span></span>

<span data-ttu-id="7bba3-116">Dans votre AD DS, effectuez les tâches de nettoyage suivantes pour chaque compte d’utilisateur auquel est attribuée une licence Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="7bba3-116">In your AD DS, complete the following clean-up tasks for each user account that will be assigned a Microsoft 365 license:</span></span>

1. <span data-ttu-id="7bba3-117">Assurez-vous d’une adresse de messagerie unique et valide dans l’attribut **proxyAddresses** .</span><span class="sxs-lookup"><span data-stu-id="7bba3-117">Ensure a valid and unique email address in the **proxyAddresses** attribute.</span></span>

2. <span data-ttu-id="7bba3-118">Supprimez toutes les valeurs en double dans l’attribut **proxyAddresses** .</span><span class="sxs-lookup"><span data-stu-id="7bba3-118">Remove any duplicate values in the **proxyAddresses** attribute.</span></span>

3. <span data-ttu-id="7bba3-119">Dans la mesure du possible, vérifiez que la valeur de l’attribut **userPrincipalName** est valide et unique dans l’objet **User** de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7bba3-119">If possible, ensure a valid and unique value for the **userPrincipalName** attribute in the user's **user** object.</span></span> <span data-ttu-id="7bba3-120">Pour une expérience de synchronisation optimale, vérifiez que l’UPN AD DS correspond à l’UPN Azure AD.</span><span class="sxs-lookup"><span data-stu-id="7bba3-120">For the best synchronization experience, ensure that the AD DS UPN matches the Azure AD UPN.</span></span> <span data-ttu-id="7bba3-121">Si un utilisateur n’a pas de valeur pour l’attribut **userPrincipalName** , l’objet **User** doit contenir une valeur valide et unique pour l’attribut **sAMAccountName** .</span><span class="sxs-lookup"><span data-stu-id="7bba3-121">If a user does not have a value for the **userPrincipalName** attribute, then the **user** object must contain a valid and unique value for the **sAMAccountName** attribute.</span></span> <span data-ttu-id="7bba3-122">Supprimez toutes les valeurs en double dans l’attribut **userPrincipalName** .</span><span class="sxs-lookup"><span data-stu-id="7bba3-122">Remove any duplicate values in the **userPrincipalName** attribute.</span></span>

4. <span data-ttu-id="7bba3-123">Pour une utilisation optimale de la liste d’adresses globale (LAG), assurez-vous que les informations figurant dans les attributs suivants du compte d’utilisateur AD DS sont correctes :</span><span class="sxs-lookup"><span data-stu-id="7bba3-123">For optimal use of the global address list (GAL), ensure the information in the following attributes of the AD DS user account is correct:</span></span>

   - <span data-ttu-id="7bba3-124">givenName</span><span class="sxs-lookup"><span data-stu-id="7bba3-124">givenName</span></span>
   - <span data-ttu-id="7bba3-125">surname</span><span class="sxs-lookup"><span data-stu-id="7bba3-125">surname</span></span>
   - <span data-ttu-id="7bba3-126">displayName</span><span class="sxs-lookup"><span data-stu-id="7bba3-126">displayName</span></span>
   - <span data-ttu-id="7bba3-127">Fonction</span><span class="sxs-lookup"><span data-stu-id="7bba3-127">Job Title</span></span>
   - <span data-ttu-id="7bba3-128">Service</span><span class="sxs-lookup"><span data-stu-id="7bba3-128">Department</span></span>
   - <span data-ttu-id="7bba3-129">Bureau</span><span class="sxs-lookup"><span data-stu-id="7bba3-129">Office</span></span>
   - <span data-ttu-id="7bba3-130">Téléphone (bureau)</span><span class="sxs-lookup"><span data-stu-id="7bba3-130">Office Phone</span></span>
   - <span data-ttu-id="7bba3-131">Téléphone mobile</span><span class="sxs-lookup"><span data-stu-id="7bba3-131">Mobile Phone</span></span>
   - <span data-ttu-id="7bba3-132">Numéro de télécopie</span><span class="sxs-lookup"><span data-stu-id="7bba3-132">Fax Number</span></span>
   - <span data-ttu-id="7bba3-133">Rue</span><span class="sxs-lookup"><span data-stu-id="7bba3-133">Street Address</span></span>
   - <span data-ttu-id="7bba3-134">Ville</span><span class="sxs-lookup"><span data-stu-id="7bba3-134">City</span></span>
   - <span data-ttu-id="7bba3-135">Département ou région</span><span class="sxs-lookup"><span data-stu-id="7bba3-135">State or Province</span></span>
   - <span data-ttu-id="7bba3-136">Code postal</span><span class="sxs-lookup"><span data-stu-id="7bba3-136">Zip or Postal Code</span></span>
   - <span data-ttu-id="7bba3-137">Pays ou région</span><span class="sxs-lookup"><span data-stu-id="7bba3-137">Country or Region</span></span>

## <a name="2-directory-object-and-attribute-preparation"></a><span data-ttu-id="7bba3-138">2. préparation de l’objet et des attributs de l’annuaire</span><span class="sxs-lookup"><span data-stu-id="7bba3-138">2. Directory object and attribute preparation</span></span>

<span data-ttu-id="7bba3-139">La réussite de la synchronisation d’annuaires entre vos services de domaine Active Directory et Microsoft 365 nécessite que vos attributs AD DS soient correctement préparés.</span><span class="sxs-lookup"><span data-stu-id="7bba3-139">Successful directory synchronization between your AD DS and Microsoft 365 requires that your AD DS attributes are properly prepared.</span></span> <span data-ttu-id="7bba3-140">Par exemple, vous devez vous assurer que des caractères spécifiques ne sont pas utilisés dans certains attributs synchronisés avec l’environnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7bba3-140">For example, you need to ensure that specific characters aren't used in certain attributes that are synchronized with the Microsoft 365 environment.</span></span> <span data-ttu-id="7bba3-141">Les caractères inattendus ne provoquent pas l’échec de la synchronisation d’annuaires, mais peuvent renvoyer un avertissement.</span><span class="sxs-lookup"><span data-stu-id="7bba3-141">Unexpected characters do not cause directory synchronization to fail but might return a warning.</span></span> <span data-ttu-id="7bba3-142">Les caractères non valides entraînent l’échec de la synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="7bba3-142">Invalid characters will cause directory synchronization to fail.</span></span>

<span data-ttu-id="7bba3-143">La synchronisation d’annuaires échoue également si certains de vos utilisateurs AD DS possèdent un ou plusieurs attributs en double.</span><span class="sxs-lookup"><span data-stu-id="7bba3-143">Directory synchronization will also fail if some of your AD DS users have one or more duplicate attributes.</span></span> <span data-ttu-id="7bba3-144">Chaque utilisateur doit avoir des attributs uniques.</span><span class="sxs-lookup"><span data-stu-id="7bba3-144">Each user must have unique attributes.</span></span>

<span data-ttu-id="7bba3-145">Les attributs que vous devez préparer sont répertoriés ici :</span><span class="sxs-lookup"><span data-stu-id="7bba3-145">The attributes that you need to prepare are listed here:</span></span>

- <span data-ttu-id="7bba3-146">**displayName**</span><span class="sxs-lookup"><span data-stu-id="7bba3-146">**displayName**</span></span>

  - <span data-ttu-id="7bba3-147">Si l’attribut existe dans l’objet utilisateur, il sera synchronisé avec Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7bba3-147">If the attribute exists in the user object, it will be synchronized with Microsoft 365.</span></span>
  - <span data-ttu-id="7bba3-148">Si cet attribut existe dans l’objet User, il doit y avoir une valeur pour lui.</span><span class="sxs-lookup"><span data-stu-id="7bba3-148">If this attribute exists in the user object, there must be a value for it.</span></span> <span data-ttu-id="7bba3-149">Autrement dit, l’attribut ne doit pas être vide.</span><span class="sxs-lookup"><span data-stu-id="7bba3-149">That is, the attribute must not be blank.</span></span>
  - <span data-ttu-id="7bba3-150">Nombre maximal de caractères : 256</span><span class="sxs-lookup"><span data-stu-id="7bba3-150">Maximum number of characters: 256</span></span>

- <span data-ttu-id="7bba3-151">**givenName**</span><span class="sxs-lookup"><span data-stu-id="7bba3-151">**givenName**</span></span>

  - <span data-ttu-id="7bba3-152">Si l’attribut existe dans l’objet utilisateur, il sera synchronisé avec Microsoft 365, mais Microsoft 365 ne l’exige pas ou ne l’utilise pas.</span><span class="sxs-lookup"><span data-stu-id="7bba3-152">If the attribute exists in the user object, it will be synchronized with Microsoft 365, but Microsoft 365 does not require or use it.</span></span>
  - <span data-ttu-id="7bba3-153">Nombre maximal de caractères : 64</span><span class="sxs-lookup"><span data-stu-id="7bba3-153">Maximum number of characters: 64</span></span>

- <span data-ttu-id="7bba3-154">**e-mails**</span><span class="sxs-lookup"><span data-stu-id="7bba3-154">**mail**</span></span>

  - <span data-ttu-id="7bba3-155">La valeur de l’attribut doit être unique dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="7bba3-155">The attribute value must be unique within the directory.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7bba3-156">S’il existe des valeurs en double, le premier utilisateur avec la valeur est synchronisé.</span><span class="sxs-lookup"><span data-stu-id="7bba3-156">If there are duplicate values, the first user with the value is synchronized.</span></span> <span data-ttu-id="7bba3-157">Les utilisateurs suivants n’apparaîtront pas dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7bba3-157">Subsequent users will not appear in Microsoft 365.</span></span> <span data-ttu-id="7bba3-158">Vous devez modifier la valeur dans Microsoft 365 ou modifier les deux valeurs dans les services de domaine Active Directory (AD DS) afin que les deux utilisateurs apparaissent dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7bba3-158">You must modify either the value in Microsoft 365 or modify both of the values in AD DS in order for both users to appear in Microsoft 365.</span></span>

- <span data-ttu-id="7bba3-159">**mailnickname** (alias Exchange)</span><span class="sxs-lookup"><span data-stu-id="7bba3-159">**mailNickname** (Exchange alias)</span></span>

  - <span data-ttu-id="7bba3-160">La valeur de l’attribut ne peut pas commencer par un point (.).</span><span class="sxs-lookup"><span data-stu-id="7bba3-160">The attribute value cannot begin with a period (.).</span></span>
  - <span data-ttu-id="7bba3-161">La valeur de l’attribut doit être unique dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="7bba3-161">The attribute value must be unique within the directory.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7bba3-162">Les traits de soulignement (« _ ») dans le nom synchronisé indiquent que la valeur d’origine de cet attribut contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="7bba3-162">Underscores ("_") in the synchronized name indicates that the original value of this attribute contains invalid characters.</span></span> <span data-ttu-id="7bba3-163">Pour plus d’informations sur cet attribut, consultez la rubrique [Exchange alias attribute](https://docs.microsoft.com/powershell/module/exchange/set-mailbox).</span><span class="sxs-lookup"><span data-stu-id="7bba3-163">For more information on this attribute, see [Exchange alias attribute](https://docs.microsoft.com/powershell/module/exchange/set-mailbox).</span></span>
    >

- <span data-ttu-id="7bba3-164">**proxyAddresses**</span><span class="sxs-lookup"><span data-stu-id="7bba3-164">**proxyAddresses**</span></span>

  - <span data-ttu-id="7bba3-165">Attribut à valeurs multiples</span><span class="sxs-lookup"><span data-stu-id="7bba3-165">Multiple-value attribute</span></span>
  - <span data-ttu-id="7bba3-166">Nombre maximal de caractères par valeur : 256</span><span class="sxs-lookup"><span data-stu-id="7bba3-166">Maximum number of characters per value: 256</span></span>
  - <span data-ttu-id="7bba3-167">La valeur de l’attribut ne doit pas contenir d’espace.</span><span class="sxs-lookup"><span data-stu-id="7bba3-167">The attribute value must not contain a space.</span></span>
  - <span data-ttu-id="7bba3-168">La valeur de l’attribut doit être unique dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="7bba3-168">The attribute value must be unique within the directory.</span></span>
  - <span data-ttu-id="7bba3-169">Caractères non valides : \< \> ();, [] "'</span><span class="sxs-lookup"><span data-stu-id="7bba3-169">Invalid characters: \< \> ( ) ; , [ ] " '</span></span>

    <span data-ttu-id="7bba3-170">Notez que les caractères non valides s’appliquent aux caractères qui suivent le délimiteur de type et à «  : », ce qui signifie que SMTP :User@contso.com est autorisé, mais SMTP :user :M@contoso.com ne l’est pas.</span><span class="sxs-lookup"><span data-stu-id="7bba3-170">Note that the invalid characters apply to the characters following the type delimiter and ":", such that SMTP:User@contso.com is allowed, but SMTP:user:M@contoso.com is not.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="7bba3-171">Toutes les adresses SMTP (simple mail transport Protocol) doivent respecter les normes de messagerie électronique.</span><span class="sxs-lookup"><span data-stu-id="7bba3-171">All Simple Mail Transport Protocol (SMTP) addresses should comply with email messaging standards.</span></span> <span data-ttu-id="7bba3-172">S’il existe des adresses en double ou indésirables, consultez la rubrique d’aide [suppression des adresses de proxy en double et indésirables dans Exchange](https://go.microsoft.com/fwlink/?LinkId=293860).</span><span class="sxs-lookup"><span data-stu-id="7bba3-172">If duplicate or unwanted addresses exist, see the Help topic [Removing duplicate and unwanted proxy addresses in Exchange](https://go.microsoft.com/fwlink/?LinkId=293860).</span></span>

- <span data-ttu-id="7bba3-173">**sAMAccountName**</span><span class="sxs-lookup"><span data-stu-id="7bba3-173">**sAMAccountName**</span></span>

  - <span data-ttu-id="7bba3-174">Nombre maximal de caractère : 20</span><span class="sxs-lookup"><span data-stu-id="7bba3-174">Maximum number of characters: 20</span></span>
  - <span data-ttu-id="7bba3-175">La valeur de l’attribut doit être unique dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="7bba3-175">The attribute value must be unique within the directory.</span></span>
  - <span data-ttu-id="7bba3-176">Caractères non valides : [\ "|,/ : \< \> + =;?</span><span class="sxs-lookup"><span data-stu-id="7bba3-176">Invalid characters: [ \ " | , / : \< \> + = ; ?</span></span> <span data-ttu-id="7bba3-177">\* ']</span><span class="sxs-lookup"><span data-stu-id="7bba3-177">\* ']</span></span>
  - <span data-ttu-id="7bba3-178">Si un utilisateur a un attribut **sAMAccountName** non valide mais qu’il dispose d’un attribut **userPrincipalName** valide, le compte d’utilisateur est créé dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7bba3-178">If a user has an invalid **sAMAccountName** attribute but has a valid **userPrincipalName** attribute, the user account is created in Microsoft 365.</span></span>
  - <span data-ttu-id="7bba3-179">Si **sAMAccountName** et **userPrincipalName** sont tous deux incorrects, l’attribut **userPrincipalName** AD DS doit être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="7bba3-179">If both **sAMAccountName** and **userPrincipalName** are invalid, the AD DS **userPrincipalName** attribute must be updated.</span></span>

- <span data-ttu-id="7bba3-180">**sn** (nom)</span><span class="sxs-lookup"><span data-stu-id="7bba3-180">**sn** (surname)</span></span>

  - <span data-ttu-id="7bba3-181">Si l’attribut existe dans l’objet utilisateur, il sera synchronisé avec Microsoft 365, mais Microsoft 365 ne l’exige pas ou ne l’utilise pas.</span><span class="sxs-lookup"><span data-stu-id="7bba3-181">If the attribute exists in the user object, it will be synchronized with Microsoft 365, but Microsoft 365 does not require or use it.</span></span>

- <span data-ttu-id="7bba3-182">**targetAddress**</span><span class="sxs-lookup"><span data-stu-id="7bba3-182">**targetAddress**</span></span>

    <span data-ttu-id="7bba3-183">L’attribut **TargetAddress** (par exemple, SMTP :Tom@contoso.com) qui est rempli pour l’utilisateur doit apparaître dans la liste d’adresses globale de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7bba3-183">It's required that the **targetAddress** attribute (for example, SMTP:tom@contoso.com) that's populated for the user must appear in the Microsoft 365 GAL.</span></span> <span data-ttu-id="7bba3-184">Dans les scénarios de migration de messagerie tiers, cela nécessite l’extension de schéma Microsoft 365 pour les services de domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7bba3-184">In third-party messaging migration scenarios, this would require the Microsoft 365 schema extension for the AD DS.</span></span> <span data-ttu-id="7bba3-185">L’extension de schéma Microsoft 365 ajoutera également d’autres attributs utiles pour gérer les objets Microsoft 365 qui sont renseignés à l’aide d’un outil de synchronisation d’annuaires à partir d’AD DS.</span><span class="sxs-lookup"><span data-stu-id="7bba3-185">The Microsoft 365 schema extension would also add other useful attributes to manage Microsoft 365 objects that are populated by using a directory synchronization tool from AD DS.</span></span> <span data-ttu-id="7bba3-186">Par exemple, l’attribut **msExchHideFromAddressLists** pour gérer les boîtes aux lettres masquées ou les groupes de distribution est ajouté.</span><span class="sxs-lookup"><span data-stu-id="7bba3-186">For example, the **msExchHideFromAddressLists** attribute to manage hidden mailboxes or distribution groups would be added.</span></span>

  - <span data-ttu-id="7bba3-187">Nombre maximal de caractères : 256</span><span class="sxs-lookup"><span data-stu-id="7bba3-187">Maximum number of characters: 256</span></span>
  - <span data-ttu-id="7bba3-188">La valeur de l’attribut ne doit pas contenir d’espace.</span><span class="sxs-lookup"><span data-stu-id="7bba3-188">The attribute value must not contain a space.</span></span>
  - <span data-ttu-id="7bba3-189">La valeur de l’attribut doit être unique dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="7bba3-189">The attribute value must be unique within the directory.</span></span>
  - <span data-ttu-id="7bba3-190">Caractères non valides : \ \< \> ();, [] "</span><span class="sxs-lookup"><span data-stu-id="7bba3-190">Invalid characters: \ \< \> ( ) ; , [ ] "</span></span>
  - <span data-ttu-id="7bba3-191">Toutes les adresses SMTP (simple mail transport Protocol) doivent respecter les normes de messagerie électronique.</span><span class="sxs-lookup"><span data-stu-id="7bba3-191">All Simple Mail Transport Protocol (SMTP) addresses should comply with email messaging standards.</span></span>

- <span data-ttu-id="7bba3-192">**userPrincipalName**</span><span class="sxs-lookup"><span data-stu-id="7bba3-192">**userPrincipalName**</span></span>

  - <span data-ttu-id="7bba3-193">L’attribut **userPrincipalName** doit être au format de connexion de style Internet où le nom d’utilisateur est suivi par le signe arobase (@) et un nom de domaine : par exemple, user@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="7bba3-193">The **userPrincipalName** attribute must be in the Internet-style sign-in format where the user name is followed by the at sign (@) and a domain name: for example, user@contoso.com.</span></span> <span data-ttu-id="7bba3-194">Toutes les adresses SMTP (simple mail transport Protocol) doivent respecter les normes de messagerie électronique.</span><span class="sxs-lookup"><span data-stu-id="7bba3-194">All Simple Mail Transport Protocol (SMTP) addresses should comply with email messaging standards.</span></span>
  - <span data-ttu-id="7bba3-195">Le nombre maximal de caractères pour l’attribut **userPrincipalName** est 113.</span><span class="sxs-lookup"><span data-stu-id="7bba3-195">The maximum number of characters for the **userPrincipalName** attribute is 113.</span></span> <span data-ttu-id="7bba3-196">Un nombre de caractères spécifique est autorisé avant et après le signe @, comme suit :</span><span class="sxs-lookup"><span data-stu-id="7bba3-196">A specific number of characters are permitted before and after the at sign (@), as follows:</span></span>
  - <span data-ttu-id="7bba3-197">Nombre maximal de caractères pour le nom d’utilisateur devant le signe arobase (@) : 64</span><span class="sxs-lookup"><span data-stu-id="7bba3-197">Maximum number of characters for the username that is in front of the at sign (@): 64</span></span>
  - <span data-ttu-id="7bba3-198">Nombre maximal de caractères pour le nom de domaine qui suit le signe arobase (@) : 48</span><span class="sxs-lookup"><span data-stu-id="7bba3-198">Maximum number of characters for the domain name following the at sign (@): 48</span></span>
  - <span data-ttu-id="7bba3-199">Caractères non valides : \% &amp; \* +/= ?</span><span class="sxs-lookup"><span data-stu-id="7bba3-199">Invalid characters: \ % &amp; \* + / = ?</span></span> <span data-ttu-id="7bba3-200">{ } | \< \> ( ) ; : , [ ] "</span><span class="sxs-lookup"><span data-stu-id="7bba3-200">{ } | \< \> ( ) ; : , [ ] "</span></span>
  - <span data-ttu-id="7bba3-201">Caractères autorisés : A – Z, a-z, 0 – 9, '.</span><span class="sxs-lookup"><span data-stu-id="7bba3-201">Characters allowed: A – Z, a - z, 0 – 9, ' .</span></span> <span data-ttu-id="7bba3-202">- _ !</span><span class="sxs-lookup"><span data-stu-id="7bba3-202">- _ !</span></span> <span data-ttu-id="7bba3-203"># ^ ~</span><span class="sxs-lookup"><span data-stu-id="7bba3-203"># ^ ~</span></span>
  - <span data-ttu-id="7bba3-204">Les lettres avec des signes diacritiques, tels que les trémas, les accents et les tildes, sont des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="7bba3-204">Letters with diacritical marks, such as umlauts, accents, and tildes, are invalid characters.</span></span>
  - <span data-ttu-id="7bba3-205">Le caractère @ est requis dans chaque valeur **userPrincipalName** .</span><span class="sxs-lookup"><span data-stu-id="7bba3-205">The @ character is required in each **userPrincipalName** value.</span></span>
  - <span data-ttu-id="7bba3-206">Le caractère @ ne peut pas être le premier caractère dans chaque valeur **userPrincipalName** .</span><span class="sxs-lookup"><span data-stu-id="7bba3-206">The @ character cannot be the first character in each **userPrincipalName** value.</span></span>
  - <span data-ttu-id="7bba3-207">Le nom d’utilisateur ne peut pas se terminer par un point (.), une esperluette ( &amp; ), un espace ou un signe arobase (@).</span><span class="sxs-lookup"><span data-stu-id="7bba3-207">The username cannot end with a period (.), an ampersand (&amp;), a space, or an at sign (@).</span></span>
  - <span data-ttu-id="7bba3-208">Le nom d’utilisateur ne peut pas contenir d’espaces.</span><span class="sxs-lookup"><span data-stu-id="7bba3-208">The username cannot contain any spaces.</span></span>
  - <span data-ttu-id="7bba3-209">Les domaines routables doivent être utilisés ; par exemple, les domaines locaux ou internes ne peuvent pas être utilisés.</span><span class="sxs-lookup"><span data-stu-id="7bba3-209">Routable domains must be used; for example, local or internal domains cannot be used.</span></span>
  - <span data-ttu-id="7bba3-210">Unicode est converti en caractères de trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="7bba3-210">Unicode is converted to underscore characters.</span></span>
  - <span data-ttu-id="7bba3-211">**userPrincipalName** ne peut pas contenir de valeurs en double dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="7bba3-211">**userPrincipalName** cannot contain any duplicate values in the directory.</span></span>

## <a name="3-prepare-the-userprincipalname-attribute"></a><span data-ttu-id="7bba3-212">3. préparer l’attribut userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7bba3-212">3. Prepare the userPrincipalName attribute</span></span>

<span data-ttu-id="7bba3-213">Active Directory est conçu pour permettre aux utilisateurs finaux de votre organisation de se connecter à votre annuaire à l’aide de **sAMAccountName** ou de **userPrincipalName** .</span><span class="sxs-lookup"><span data-stu-id="7bba3-213">Active Directory is designed to allow the end users in your organization to sign in to your directory by using either **sAMAccountName** or **userPrincipalName** .</span></span> <span data-ttu-id="7bba3-214">De même, les utilisateurs finaux peuvent se connecter à Microsoft 365 en utilisant le nom d’utilisateur principal (UPN) de leur compte professionnel ou scolaire.</span><span class="sxs-lookup"><span data-stu-id="7bba3-214">Similarly, end users can sign in to Microsoft 365 by using the user principal name (UPN) of their work or school account.</span></span> <span data-ttu-id="7bba3-215">La synchronisation d’annuaires tente de créer des utilisateurs dans Azure Active Directory à l’aide du même nom d’utilisateur principal qui se trouve dans votre AD DS.</span><span class="sxs-lookup"><span data-stu-id="7bba3-215">Directory synchronization attempts to create new users in Azure Active Directory by using the same UPN that's in your AD DS.</span></span> <span data-ttu-id="7bba3-216">Le nom d’utilisateur principal est mis en forme comme une adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="7bba3-216">The UPN is formatted like an email address.</span></span>

<span data-ttu-id="7bba3-217">Dans Microsoft 365, le nom d’utilisateur principal est l’attribut par défaut utilisé pour générer l’adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="7bba3-217">In Microsoft 365, the UPN is the default attribute that's used to generate the email address.</span></span> <span data-ttu-id="7bba3-218">Il est facile d’obtenir le **userPrincipalName** (dans AD DS et dans Azure AD) et l’adresse de messagerie principale dans **proxyAddresses** définie sur différentes valeurs.</span><span class="sxs-lookup"><span data-stu-id="7bba3-218">It's easy to get **userPrincipalName** (in AD DS and in Azure AD) and the primary email address in **proxyAddresses** set to different values.</span></span> <span data-ttu-id="7bba3-219">Lorsqu’elles sont définies sur des valeurs différentes, les administrateurs et les utilisateurs finaux peuvent être confondus.</span><span class="sxs-lookup"><span data-stu-id="7bba3-219">When they are set to different values, there can be confusion for administrators and end users.</span></span>

<span data-ttu-id="7bba3-220">Il est préférable d’aligner ces attributs afin de réduire la confusion.</span><span class="sxs-lookup"><span data-stu-id="7bba3-220">It's best to align these attributes to reduce confusion.</span></span> <span data-ttu-id="7bba3-221">Pour répondre aux exigences de l’authentification unique avec les services ADFS (Active Directory Federation Services) 2,0, vous devez vous assurer que l’UPN dans Azure Active Directory et votre AD DS correspondent et utilise un espace de noms de domaine valide.</span><span class="sxs-lookup"><span data-stu-id="7bba3-221">To meet the requirements of single sign-on with Active Directory Federation Services (AD FS) 2.0, you need to ensure that the UPNs in Azure Active Directory and your AD DS match and are using a valid domain namespace.</span></span>

## <a name="4-add-an-alternative-upn-suffix-to-ad-ds"></a><span data-ttu-id="7bba3-222">4. Ajoutez un autre suffixe UPN à AD DS.</span><span class="sxs-lookup"><span data-stu-id="7bba3-222">4. Add an alternative UPN suffix to AD DS</span></span>

<span data-ttu-id="7bba3-223">Vous devrez peut-être ajouter un autre suffixe UPN pour associer les informations d’identification d’entreprise de l’utilisateur à l’environnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7bba3-223">You may need to add an alternative UPN suffix to associate the user's corporate credentials with the Microsoft 365 environment.</span></span> <span data-ttu-id="7bba3-224">Un suffixe UPN est la partie d’un UPN située à droite du caractère @.</span><span class="sxs-lookup"><span data-stu-id="7bba3-224">A UPN suffix is the part of a UPN to the right of the @ character.</span></span> <span data-ttu-id="7bba3-225">Les UPN qui sont utilisés pour l’authentification unique peuvent contenir des lettres, des chiffres, des points, des traits d’unions et des traits de soulignement, mais aucun autre type de caractère.</span><span class="sxs-lookup"><span data-stu-id="7bba3-225">UPNs that are used for single sign-on can contain letters, numbers, periods, dashes, and underscores, but no other types of characters.</span></span>

<span data-ttu-id="7bba3-226">Pour plus d’informations sur l’ajout d’un autre suffixe UPN à Active Directory, consultez la rubrique [préparer la synchronisation d’annuaires]( https://go.microsoft.com/fwlink/p/?LinkId=525430).</span><span class="sxs-lookup"><span data-stu-id="7bba3-226">For more information on how to add an alternative UPN suffix to Active Directory, see [Prepare for directory synchronization]( https://go.microsoft.com/fwlink/p/?LinkId=525430).</span></span>

## <a name="5-match-the-ad-ds-upn-with-the-microsoft-365-upn"></a><span data-ttu-id="7bba3-227">5. faire correspondre l’UPN AD DS avec le nom UPN Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7bba3-227">5. Match the AD DS UPN with the Microsoft 365 UPN</span></span>

<span data-ttu-id="7bba3-228">Si vous avez déjà configuré la synchronisation d’annuaires, il se peut que l’UPN de l’utilisateur pour Microsoft 365 ne corresponde pas à l’UPN AD DS de l’utilisateur défini dans votre AD DS.</span><span class="sxs-lookup"><span data-stu-id="7bba3-228">If you've already set up directory synchronization, the user's UPN for Microsoft 365 may not match the user's AD DS UPN that's defined in your AD DS.</span></span> <span data-ttu-id="7bba3-229">Cela peut se produire lorsqu’un utilisateur obtient une licence avant la vérification du domaine.</span><span class="sxs-lookup"><span data-stu-id="7bba3-229">This can occur when a user was assigned a license before the domain was verified.</span></span> <span data-ttu-id="7bba3-230">Pour résoudre ce problème, utilisez [PowerShell pour corriger le nom UPN en double](https://go.microsoft.com/fwlink/p/?LinkId=396730) afin de mettre à jour l’UPN de l’utilisateur afin de s’assurer que l’upn Microsoft 365 correspond au nom d’utilisateur et au domaine de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="7bba3-230">To fix this, use [PowerShell to fix duplicate UPN](https://go.microsoft.com/fwlink/p/?LinkId=396730) to update the user's UPN to ensure that the Microsoft 365 UPN matches the corporate user name and domain.</span></span> <span data-ttu-id="7bba3-231">Si vous mettez à jour l’UPN dans AD DS et souhaitez le synchroniser avec l’identité Azure Active Directory, vous devez supprimer la licence de l’utilisateur dans Microsoft 365 avant d’apporter les modifications dans AD DS.</span><span class="sxs-lookup"><span data-stu-id="7bba3-231">If you are updating the UPN in the AD DS and would like it to synchronize with the Azure Active Directory identity, you need to remove the user's license in Microsoft 365 prior to making the changes in AD DS.</span></span>

<span data-ttu-id="7bba3-232">Découvrez également [Comment préparer un domaine non routable (par exemple, le domaine. local) pour la synchronisation d’annuaires](prepare-a-non-routable-domain-for-directory-synchronization.md).</span><span class="sxs-lookup"><span data-stu-id="7bba3-232">Also see [How to prepare a non-routable domain (such as .local domain) for directory synchronization](prepare-a-non-routable-domain-for-directory-synchronization.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="7bba3-233">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="7bba3-233">Next steps</span></span>

<span data-ttu-id="7bba3-234">Si vous avez terminé les étapes 1 à 5 ci-dessus, voir [configurer la synchronisation d’annuaires](set-up-directory-synchronization.md).</span><span class="sxs-lookup"><span data-stu-id="7bba3-234">If you have done steps 1 through 5 above, see [Set up directory synchronization](set-up-directory-synchronization.md).</span></span>
