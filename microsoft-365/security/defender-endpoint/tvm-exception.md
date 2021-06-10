---
title: Créer et afficher des exceptions pour les recommandations de sécurité - Gestion des menaces et des vulnérabilités
description: Créez et surveillez les exceptions pour les recommandations de sécurité Gestion des menaces et des vulnérabilités.
keywords: Correction tvm De Microsoft Defender pour point de terminaison, Microsoft Defender pour tvm de point de terminaison, Gestion des menaces et des vulnérabilités, & gestion des vulnérabilités contre les menaces, correction des menaces & gestion des vulnérabilités, correction tvm intune, sccm de correction tvm
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 1af8e5ec9d3aef560c739de5212e8118cf89cd7a
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51933744"
---
# <a name="create-and-view-exceptions-for-security-recommendations---threat-and-vulnerability-management"></a><span data-ttu-id="e5624-104">Créer et afficher des exceptions pour les recommandations de sécurité - Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="e5624-104">Create and view exceptions for security recommendations - threat and vulnerability management</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="e5624-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e5624-105">**Applies to:**</span></span>

- [<span data-ttu-id="e5624-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e5624-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="e5624-107">Menaces et gestion des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="e5624-107">Threat and vulnerability management</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="e5624-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e5624-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


><span data-ttu-id="e5624-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="e5624-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="e5624-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="e5624-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-portaloverview-abovefoldlink)

<span data-ttu-id="e5624-111">En remplacement d’une demande de correction lorsqu’une recommandation n’est pas pertinente pour le moment, vous pouvez créer des exceptions pour les recommandations.</span><span class="sxs-lookup"><span data-stu-id="e5624-111">As an alternative to a remediation request when a recommendation is not relevant at the moment, you can create exceptions for recommendations.</span></span> <span data-ttu-id="e5624-112">Si votre organisation dispose de groupes d’appareils, vous serez en mesure d’étenduer l’exception à des groupes d’appareils spécifiques.</span><span class="sxs-lookup"><span data-stu-id="e5624-112">If your organization has device groups, you will be able to scope the exception to specific device groups.</span></span> <span data-ttu-id="e5624-113">Des exceptions peuvent être créées pour les groupes d’appareils sélectionnés ou pour tous les groupes d’appareils passés et présents.</span><span class="sxs-lookup"><span data-stu-id="e5624-113">Exceptions can either be created for selected device groups, or for all device groups past and present.</span></span>  

<span data-ttu-id="e5624-114">Lorsqu’une exception est créée pour une recommandation, la recommandation n’est pas active avant la fin de la durée de l’exception.</span><span class="sxs-lookup"><span data-stu-id="e5624-114">When an exception is created for a recommendation, the recommendation will not be active until the end of the exception duration.</span></span> <span data-ttu-id="e5624-115">L’état de recommandation change en **Exception complète ou** Exception **partielle** (par groupe d’appareils).</span><span class="sxs-lookup"><span data-stu-id="e5624-115">The recommendation state will change to **Full exception** or **Partial exception** (by device group).</span></span>

## <a name="permissions"></a><span data-ttu-id="e5624-116">Autorisations</span><span class="sxs-lookup"><span data-stu-id="e5624-116">Permissions</span></span>

<span data-ttu-id="e5624-117">Seuls les utilisateurs ayant des autorisations de « gestion des exceptions » peuvent gérer les exceptions (y compris la création ou l’annulation).</span><span class="sxs-lookup"><span data-stu-id="e5624-117">Only users with “exceptions handling” permissions can manage exceptions (including creating or canceling).</span></span> <span data-ttu-id="e5624-118">[En savoir plus sur les rôles RBAC.](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="e5624-118">[Learn more about RBAC roles](user-roles.md).</span></span>

![Affichage de l’autorisation de gestion des exceptions.](images/tvm-exception-permissions.png)

## <a name="create-an-exception"></a><span data-ttu-id="e5624-120">Créer une exception</span><span class="sxs-lookup"><span data-stu-id="e5624-120">Create an exception</span></span>

<span data-ttu-id="e5624-121">Sélectionnez une recommandation de sécurité pour la création d’une exception, puis sélectionnez **Options d’exception** et remplissez le formulaire.</span><span class="sxs-lookup"><span data-stu-id="e5624-121">Select a security recommendation you would like create an exception for, and then select **Exception options** and fill out the form.</span></span>  

![Affichage de l’emplacement du bouton « options d’exception » dans un volant de recommandations de sécurité.](images/tvm-exception-options.png)

### <a name="exception-by-device-group"></a><span data-ttu-id="e5624-123">Exception par groupe d’appareils</span><span class="sxs-lookup"><span data-stu-id="e5624-123">Exception by device group</span></span>

<span data-ttu-id="e5624-124">Appliquez l’exception à tous les groupes d’appareils actuels ou choisissez des groupes d’appareils spécifiques.</span><span class="sxs-lookup"><span data-stu-id="e5624-124">Apply the exception to all current device groups or choose specific device groups.</span></span> <span data-ttu-id="e5624-125">Les groupes d’appareils futurs ne seront pas inclus dans l’exception.</span><span class="sxs-lookup"><span data-stu-id="e5624-125">Future device groups won't be included in the exception.</span></span> <span data-ttu-id="e5624-126">Les groupes d’appareils qui ont déjà une exception ne sont pas affichés dans la liste.</span><span class="sxs-lookup"><span data-stu-id="e5624-126">Device groups that already have an exception will not be displayed in the list.</span></span> <span data-ttu-id="e5624-127">Si vous sélectionnez uniquement certains groupes d’appareils, l’état de recommandation change de « actif » à « exception partielle ».</span><span class="sxs-lookup"><span data-stu-id="e5624-127">If you only select certain device groups, the recommendation state will change from “active” to “partial exception.”</span></span> <span data-ttu-id="e5624-128">L’état est « exception complète » si vous sélectionnez tous les groupes d’appareils.</span><span class="sxs-lookup"><span data-stu-id="e5624-128">The state will change to “full exception” if you select all the device groups.</span></span>

![Affichage de la dropdown des groupes d’appareils.](images/tvm-exception-device-group-500.png)

#### <a name="filtered-views"></a><span data-ttu-id="e5624-130">Affichages filtrés</span><span class="sxs-lookup"><span data-stu-id="e5624-130">Filtered views</span></span>

<span data-ttu-id="e5624-131">Si vous avez filtré par groupe d’appareils sur l’une des pages Gestion des menaces et des vulnérabilités, seuls vos groupes d’appareils filtrés apparaîtront en tant qu’options.</span><span class="sxs-lookup"><span data-stu-id="e5624-131">If you have filtered by device group on any of the threat and vulnerability management pages, only your filtered device groups will appear as options.</span></span>

<span data-ttu-id="e5624-132">Il s’agit du bouton à filtrer par groupe d’appareils sur l’une Gestion des menaces et des vulnérabilités pages suivantes :</span><span class="sxs-lookup"><span data-stu-id="e5624-132">This is the button to filter by device group on any of the threat and vulnerability management pages:</span></span> 

![Affichage du filtre des groupes d’appareils sélectionnés.](images/tvm-selected-device-groups.png)

<span data-ttu-id="e5624-134">Affichage des exceptions avec groupes d’appareils filtrés :</span><span class="sxs-lookup"><span data-stu-id="e5624-134">Exception view with filtered device groups:</span></span>

![Affichage de la dropdown de groupe d’appareils filtré.](images/tvm-exception-device-filter500.png)

#### <a name="large-number-of-device-groups"></a><span data-ttu-id="e5624-136">Grand nombre de groupes d’appareils</span><span class="sxs-lookup"><span data-stu-id="e5624-136">Large number of device groups</span></span>

<span data-ttu-id="e5624-137">Si votre organisation compte plus de 20 groupes d’appareils, sélectionnez **Modifier** en plus de l’option de groupe d’appareils filtré.</span><span class="sxs-lookup"><span data-stu-id="e5624-137">If your organization has more than 20 device groups, select **Edit** next to the filtered device group option.</span></span>

![Montrant comment modifier un grand nombre de groupes.](images/tvm-exception-edit-groups.png)

<span data-ttu-id="e5624-139">Un volant s’affiche où vous pouvez rechercher et choisir les groupes d’appareils que vous souhaitez inclure.</span><span class="sxs-lookup"><span data-stu-id="e5624-139">A flyout will appear where you can search and choose device groups you want included.</span></span> <span data-ttu-id="e5624-140">Sélectionnez l’icône de coche sous Recherche pour vérifier/décocher tout.</span><span class="sxs-lookup"><span data-stu-id="e5624-140">Select the check mark icon below Search to check/uncheck all.</span></span>

![Affichage du volant de groupe d’appareils de grande taille.](images/tvm-exception-device-group-flyout-400.png)

### <a name="global-exceptions"></a><span data-ttu-id="e5624-142">Exceptions globales</span><span class="sxs-lookup"><span data-stu-id="e5624-142">Global exceptions</span></span>

<span data-ttu-id="e5624-143">Si vous avez des autorisations d’administrateur général, vous pourrez créer et annuler une exception globale.</span><span class="sxs-lookup"><span data-stu-id="e5624-143">If you have global administrator permissions, you will be able to create and cancel a global exception.</span></span> <span data-ttu-id="e5624-144">Elle affecte tous **les** groupes d’appareils actuels et futurs de votre organisation, et seul un utilisateur ayant des autorisations similaires peut le modifier.</span><span class="sxs-lookup"><span data-stu-id="e5624-144">It affects **all** current and future device groups in your organization, and only a user with similar permission would be able to change it.</span></span> <span data-ttu-id="e5624-145">L’état de recommandation va changer de « actif » à « exception complète ».</span><span class="sxs-lookup"><span data-stu-id="e5624-145">The recommendation state will change from “active” to “full exception.”</span></span>

![Affichage de l’option d’exception globale.](images/tvm-exception-global.png)

<span data-ttu-id="e5624-147">Voici quelques éléments à garder à l’esprit :</span><span class="sxs-lookup"><span data-stu-id="e5624-147">Some things to keep in mind:</span></span>

- <span data-ttu-id="e5624-148">Si une recommandation fait l’objet d’une exception globale, les exceptions nouvellement créées pour les groupes d’appareils sont suspendues jusqu’à ce que l’exception globale ait expiré ou ait été annulée.</span><span class="sxs-lookup"><span data-stu-id="e5624-148">If a recommendation is under global exception, then newly created exceptions for device groups will be suspended until the global exception has expired or been cancelled.</span></span> <span data-ttu-id="e5624-149">Après ce point, les nouvelles exceptions de groupe d’appareils entreront en vigueur jusqu’à leur expiration.</span><span class="sxs-lookup"><span data-stu-id="e5624-149">After that point, the new device group exceptions will go into effect until they expire.</span></span>
- <span data-ttu-id="e5624-150">Si une recommandation a déjà des exceptions pour des groupes d’appareils spécifiques et qu’une exception globale est créée, l’exception de groupe d’appareils est suspendue jusqu’à son expiration ou l’exception globale est annulée avant son expiration.</span><span class="sxs-lookup"><span data-stu-id="e5624-150">If a recommendation already has exceptions for specific device groups and a global exception is created, then the device group exception will be suspended until it expires or the global exception is cancelled before it expires.</span></span>

### <a name="justification"></a><span data-ttu-id="e5624-151">Justification</span><span class="sxs-lookup"><span data-stu-id="e5624-151">Justification</span></span>

<span data-ttu-id="e5624-152">Sélectionnez votre justification pour l’exception que vous devez déposer au lieu de corriger la recommandation de sécurité en question.</span><span class="sxs-lookup"><span data-stu-id="e5624-152">Select your justification for the exception you need to file instead of remediating the security recommendation in question.</span></span> <span data-ttu-id="e5624-153">Remplissez le contexte de justification, puis définissez la durée de l’exception.</span><span class="sxs-lookup"><span data-stu-id="e5624-153">Fill out the justification context, then set the exception duration.</span></span>

<span data-ttu-id="e5624-154">La liste suivante détaille les justifications des options d’exception :</span><span class="sxs-lookup"><span data-stu-id="e5624-154">The following list details the justifications behind the exception options:</span></span>

- <span data-ttu-id="e5624-155">**Contrôle tiers** - Un produit ou un logiciel tiers répond déjà à cette recommandation : le choix de ce type de justification réduit votre score d’exposition et augmente votre score de sécurité car votre risque est réduit</span><span class="sxs-lookup"><span data-stu-id="e5624-155">**Third party control** - A third party product or software already addresses this recommendation       - Choosing this justification type will lower your exposure score and increase your secure score because your risk is reduced</span></span>
- <span data-ttu-id="e5624-156">**Atténuation de remplacement** : un outil interne répond déjà à cette recommandation : le choix de ce type de justification réduit votre score d’exposition et augmente votre score de sécurité car votre risque est réduit</span><span class="sxs-lookup"><span data-stu-id="e5624-156">**Alternate mitigation** - An internal tool already addresses this recommendation       - Choosing this justification type will lower your exposure score and increase your secure score because your risk is reduced</span></span>
- <span data-ttu-id="e5624-157">**Risque accepté :** pose un risque faible et/ou l’implémentation de la recommandation est trop coûteuse</span><span class="sxs-lookup"><span data-stu-id="e5624-157">**Risk accepted** - Poses low risk and/or implementing the recommendation is too expensive</span></span>
- <span data-ttu-id="e5624-158">**Correction planifiée (grâce)** : déjà planifiée mais en attente d’exécution ou d’autorisation</span><span class="sxs-lookup"><span data-stu-id="e5624-158">**Planned remediation (grace)** - Already planned but is awaiting execution or authorization</span></span>

## <a name="view-all-exceptions"></a><span data-ttu-id="e5624-159">Afficher toutes les exceptions</span><span class="sxs-lookup"><span data-stu-id="e5624-159">View all exceptions</span></span>

<span data-ttu-id="e5624-160">Accédez à **l’onglet Exceptions** dans la page **Correction.**</span><span class="sxs-lookup"><span data-stu-id="e5624-160">Navigate to the **Exceptions** tab in the **Remediation** page.</span></span> <span data-ttu-id="e5624-161">Vous pouvez filtrer par justification, type et état.</span><span class="sxs-lookup"><span data-stu-id="e5624-161">You can filter by justification, type, and status.</span></span>

 <span data-ttu-id="e5624-162">Sélectionnez une exception pour ouvrir un volant avec plus de détails.</span><span class="sxs-lookup"><span data-stu-id="e5624-162">Select an exception to open a flyout with more details.</span></span> <span data-ttu-id="e5624-163">Les exceptions par groupe d’appareils auront une liste de chaque groupe d’appareils couvert par l’exception, que vous pouvez exporter.</span><span class="sxs-lookup"><span data-stu-id="e5624-163">Exceptions per devices group will have a list of every device group the exception covers, which you can export.</span></span> <span data-ttu-id="e5624-164">Vous pouvez également afficher la recommandation associée ou annuler l’exception.</span><span class="sxs-lookup"><span data-stu-id="e5624-164">You can also view the related recommendation or cancel the exception.</span></span>

![Affichage de l’onglet « Exceptions » dans la page Correction.](images/tvm-exception-view.png)

## <a name="how-to-cancel-an-exception"></a><span data-ttu-id="e5624-166">Comment annuler une exception</span><span class="sxs-lookup"><span data-stu-id="e5624-166">How to cancel an exception</span></span>

<span data-ttu-id="e5624-167">Pour annuler une exception, accédez à **l’onglet Exceptions** dans la page **Correction.**</span><span class="sxs-lookup"><span data-stu-id="e5624-167">To cancel an exception, navigate to the **Exceptions** tab in the **Remediation** page.</span></span> <span data-ttu-id="e5624-168">Sélectionnez l’exception.</span><span class="sxs-lookup"><span data-stu-id="e5624-168">Select the exception.</span></span>

<span data-ttu-id="e5624-169">Pour annuler l’exception pour tous les groupes d’appareils ou pour une exception globale, sélectionnez l’exception Annuler pour tous les groupes **d’appareils.**</span><span class="sxs-lookup"><span data-stu-id="e5624-169">To cancel the exception for all device groups or for a global exception, select the **Cancel exception for all device groups** button.</span></span> <span data-ttu-id="e5624-170">Vous pourrez uniquement annuler les exceptions pour les groupes d’appareils pour qui vous avez des autorisations.</span><span class="sxs-lookup"><span data-stu-id="e5624-170">You will only be able to cancel exceptions for device groups you have permissions for.</span></span>

![Bouton Annuler.](images/tvm-exception-cancel.png)

### <a name="cancel-the-exception-for-a-specific-device-group"></a><span data-ttu-id="e5624-172">Annuler l’exception pour un groupe d’appareils spécifique</span><span class="sxs-lookup"><span data-stu-id="e5624-172">Cancel the exception for a specific device group</span></span>

<span data-ttu-id="e5624-173">Sélectionnez le groupe d’appareils spécifique pour annuler l’exception.</span><span class="sxs-lookup"><span data-stu-id="e5624-173">Select the specific device group to cancel the exception for it.</span></span> <span data-ttu-id="e5624-174">Un volant s’affiche pour le groupe d’appareils, et vous pouvez sélectionner **l’exception Annuler.**</span><span class="sxs-lookup"><span data-stu-id="e5624-174">A flyout will appear for the device group, and you can select **Cancel exception**.</span></span>

![Montrant comment sélectionner un groupe d’appareils spécifique.](images/tvm-exception-device-group-hover.png)

## <a name="view-impact-after-exceptions-are-applied"></a><span data-ttu-id="e5624-176">Afficher l’impact après application des exceptions</span><span class="sxs-lookup"><span data-stu-id="e5624-176">View impact after exceptions are applied</span></span>

<span data-ttu-id="e5624-177">Dans la page Sécurité Recommandations,  sélectionnez Personnaliser les colonnes et cochez les cases pour les appareils exposés **(après les exceptions)** et **l’impact (après les exceptions).**</span><span class="sxs-lookup"><span data-stu-id="e5624-177">In the Security Recommendations page, select **Customize columns** and check the boxes for **Exposed devices (after exceptions)** and **Impact (after exceptions)**.</span></span>

![Affichage des options de personnalisation des colonnes.](images/tvm-after-exceptions.png)

<span data-ttu-id="e5624-179">La colonne appareils exposés (après les exceptions) affiche les autres appareils qui sont encore exposés aux vulnérabilités après l’application des exceptions.</span><span class="sxs-lookup"><span data-stu-id="e5624-179">The exposed devices (after exceptions) column shows the remaining devices that are still exposed to vulnerabilities after exceptions are applied.</span></span> <span data-ttu-id="e5624-180">Les justifications d’exception qui affectent l’exposition incluent « contrôle tiers » et « atténuation de remplacement ».</span><span class="sxs-lookup"><span data-stu-id="e5624-180">Exception justifications that affect the exposure include ‘third party control’ and ‘alternate mitigation’.</span></span> <span data-ttu-id="e5624-181">D’autres justifications ne réduisent pas l’exposition d’un appareil et sont toujours considérées comme exposées.</span><span class="sxs-lookup"><span data-stu-id="e5624-181">Other justifications do not reduce the exposure of a device, and they are still considered exposed.</span></span>

<span data-ttu-id="e5624-182">L’impact (après les exceptions) indique l’impact restant sur le score d’exposition ou le score sécurisé après l’application des exceptions.</span><span class="sxs-lookup"><span data-stu-id="e5624-182">The impact (after exceptions) shows remaining impact to exposure score or secure score after exceptions are applied.</span></span> <span data-ttu-id="e5624-183">Les justifications d’exception qui affectent les scores incluent « contrôle tiers » et « atténuation alternative ».</span><span class="sxs-lookup"><span data-stu-id="e5624-183">Exception justifications that affect the scores include ‘third party control’ and ‘alternate mitigation.’</span></span> <span data-ttu-id="e5624-184">D’autres justifications ne réduisent pas l’exposition d’un appareil, de sorte que le score d’exposition et le score de sécurité ne changent pas.</span><span class="sxs-lookup"><span data-stu-id="e5624-184">Other justifications do not reduce the exposure of a device, and so the exposure score and secure score do not change.</span></span>

![Affichage des colonnes dans le tableau.](images/tvm-after-exceptions-table.png)

## <a name="related-topics"></a><span data-ttu-id="e5624-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5624-186">Related topics</span></span>

- [<span data-ttu-id="e5624-187">Vue d’ensemble gestion des vulnérabilités menaces et gestion des vulnérabilités menaces</span><span class="sxs-lookup"><span data-stu-id="e5624-187">Threat and vulnerability management overview</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="e5624-188">Corriger des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="e5624-188">Remediate vulnerabilities</span></span>](tvm-remediation.md)
- [<span data-ttu-id="e5624-189">Recommandations de sécurité</span><span class="sxs-lookup"><span data-stu-id="e5624-189">Security recommendations</span></span>](tvm-security-recommendation.md)
- [<span data-ttu-id="e5624-190">Score d'exposition</span><span class="sxs-lookup"><span data-stu-id="e5624-190">Exposure score</span></span>](tvm-exposure-score.md)
- [<span data-ttu-id="e5624-191">Niveau de sécurité Microsoft pour les appareils</span><span class="sxs-lookup"><span data-stu-id="e5624-191">Microsoft Secure Score for Devices</span></span>](tvm-microsoft-secure-score-devices.md)
