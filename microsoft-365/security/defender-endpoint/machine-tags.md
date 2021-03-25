---
title: Créer et gérer des balises d’appareil
description: Utiliser des balises de périphérique pour grouper des appareils pour capturer le contexte et activer la création de listes dynamiques dans le cadre d’un incident
keywords: tags, device tags, device groups, groups, remediation, level, rules, aad group, role, assign, rank
search.product: eADQiWindows 10XVcnh
search.appverid: met150
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
ms.openlocfilehash: ffe7d13ca0943e8927d0d9ce663527fedf880e48
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51187588"
---
# <a name="create-and-manage-device-tags"></a><span data-ttu-id="acc3a-104">Créer et gérer des balises d’appareil</span><span class="sxs-lookup"><span data-stu-id="acc3a-104">Create and manage device tags</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="acc3a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="acc3a-105">**Applies to:**</span></span>
- [<span data-ttu-id="acc3a-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="acc3a-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="acc3a-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="acc3a-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="acc3a-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="acc3a-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="acc3a-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="acc3a-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="acc3a-110">Ajoutez des balises sur les appareils pour créer une affiliation de groupe logique.</span><span class="sxs-lookup"><span data-stu-id="acc3a-110">Add tags on devices to create a logical group affiliation.</span></span> <span data-ttu-id="acc3a-111">Les balises de périphériques permettent un mappage correct du réseau, ce qui vous permet d’attacher différentes balises pour capturer le contexte et activer la création de listes dynamiques dans le cadre d’un incident.</span><span class="sxs-lookup"><span data-stu-id="acc3a-111">Device tags support proper mapping of the network, enabling you to attach different tags to capture context and to enable dynamic list creation as part of an incident.</span></span> <span data-ttu-id="acc3a-112">Les balises peuvent être  utilisées comme filtre dans l’affichage Liste des appareils ou pour grouper des appareils.</span><span class="sxs-lookup"><span data-stu-id="acc3a-112">Tags can be used as a filter in **Devices list** view, or to group devices.</span></span> <span data-ttu-id="acc3a-113">Pour plus d’informations sur le regroupement d’appareils, voir [Créer et gérer des groupes d’appareils.](machine-groups.md)</span><span class="sxs-lookup"><span data-stu-id="acc3a-113">For more information on device grouping, see [Create and manage device groups](machine-groups.md).</span></span>

<span data-ttu-id="acc3a-114">Vous pouvez ajouter des balises sur les appareils en utilisant les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="acc3a-114">You can add tags on devices using the following ways:</span></span>

- <span data-ttu-id="acc3a-115">Utilisation du portail</span><span class="sxs-lookup"><span data-stu-id="acc3a-115">Using the portal</span></span>
- <span data-ttu-id="acc3a-116">Définition d’une valeur de clé de Registre</span><span class="sxs-lookup"><span data-stu-id="acc3a-116">Setting a registry key value</span></span>

> [!NOTE]
> <span data-ttu-id="acc3a-117">Il peut y avoir une certaine latence entre le moment où une balise est ajoutée à un appareil et sa disponibilité dans la liste des appareils et la page de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="acc3a-117">There may be some latency between the time a tag is added to a device and its availability in the devices list and device page.</span></span>  

<span data-ttu-id="acc3a-118">Pour ajouter des balises d’appareil à l’aide de l’API, voir [Api Ajouter ou supprimer des balises d’appareil.](add-or-remove-machine-tags.md)</span><span class="sxs-lookup"><span data-stu-id="acc3a-118">To add device tags using API, see [Add or remove device tags API](add-or-remove-machine-tags.md).</span></span>

## <a name="add-and-manage-device-tags-using-the-portal"></a><span data-ttu-id="acc3a-119">Ajouter et gérer des balises d’appareil à l’aide du portail</span><span class="sxs-lookup"><span data-stu-id="acc3a-119">Add and manage device tags using the portal</span></span>

1. <span data-ttu-id="acc3a-120">Sélectionnez l’appareil sur qui vous souhaitez gérer les balises.</span><span class="sxs-lookup"><span data-stu-id="acc3a-120">Select the device that you want to manage tags on.</span></span> <span data-ttu-id="acc3a-121">Vous pouvez sélectionner ou rechercher un appareil dans l’un des affichages suivants :</span><span class="sxs-lookup"><span data-stu-id="acc3a-121">You can select or search for a device from any of the following views:</span></span>

   - <span data-ttu-id="acc3a-122">**Tableau de bord Opérations de sécurité** : sélectionnez le nom de l’appareil dans la section Principaux appareils avec alertes actives.</span><span class="sxs-lookup"><span data-stu-id="acc3a-122">**Security operations dashboard** - Select the device name from the Top devices with active alerts section.</span></span>
   - <span data-ttu-id="acc3a-123">**File d’attente des alertes** : sélectionnez le nom de l’appareil à côté de l’icône de l’appareil dans la file d’attente des alertes.</span><span class="sxs-lookup"><span data-stu-id="acc3a-123">**Alerts queue** - Select the device name beside the device icon from the alerts queue.</span></span>
   - <span data-ttu-id="acc3a-124">**Liste des appareils** : sélectionnez le nom de l’appareil dans la liste des appareils.</span><span class="sxs-lookup"><span data-stu-id="acc3a-124">**Devices list** - Select the device name from the list of devices.</span></span>
   - <span data-ttu-id="acc3a-125">**Zone de recherche** : sélectionnez l’appareil dans le menu déroulant et entrez le nom de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="acc3a-125">**Search box** - Select Device from the drop-down menu and enter the device name.</span></span>

     <span data-ttu-id="acc3a-126">Vous pouvez également vous rendre sur la page d’alerte via le fichier et les vues IP.</span><span class="sxs-lookup"><span data-stu-id="acc3a-126">You can also get to the alert page through the file and IP views.</span></span>

2. <span data-ttu-id="acc3a-127">Sélectionnez **Gérer les balises** dans la ligne des actions de réponse.</span><span class="sxs-lookup"><span data-stu-id="acc3a-127">Select **Manage Tags** from the row of Response actions.</span></span>

    ![Image du bouton Gérer les balises](images/manage-tags.png)

3. <span data-ttu-id="acc3a-129">Tapez pour rechercher ou créer des balises</span><span class="sxs-lookup"><span data-stu-id="acc3a-129">Type to find or create tags</span></span>

    ![Image de l’ajout de balises sur un appareil1](images/new-tags.png)

<span data-ttu-id="acc3a-131">Les balises sont ajoutées à l’affichage de l’appareil et sont également reflétées dans l’affichage Liste **des** appareils.</span><span class="sxs-lookup"><span data-stu-id="acc3a-131">Tags are added to the device view and will also be reflected on the **Devices list** view.</span></span> <span data-ttu-id="acc3a-132">Vous pouvez ensuite utiliser le filtre **Balises** pour voir la liste des appareils appropriés.</span><span class="sxs-lookup"><span data-stu-id="acc3a-132">You can then use the **Tags** filter to see the relevant list of devices.</span></span>

>[!NOTE]
> <span data-ttu-id="acc3a-133">Le filtrage peut ne pas fonctionner sur les noms de balises qui contiennent des parenthèses.</span><span class="sxs-lookup"><span data-stu-id="acc3a-133">Filtering might not work on tag names that contain parenthesis.</span></span><br>
> <span data-ttu-id="acc3a-134">Lorsque vous créez une balise, une liste de balises existantes s’affiche.</span><span class="sxs-lookup"><span data-stu-id="acc3a-134">When you create a new tag, a list of existing tags are displayed.</span></span> <span data-ttu-id="acc3a-135">La liste affiche uniquement les balises créées via le portail.</span><span class="sxs-lookup"><span data-stu-id="acc3a-135">The list only shows tags created through the portal.</span></span> <span data-ttu-id="acc3a-136">Les balises existantes créées à partir d’appareils clients ne seront pas affichées.</span><span class="sxs-lookup"><span data-stu-id="acc3a-136">Existing tags created from client devices will not be displayed.</span></span>

<span data-ttu-id="acc3a-137">Vous pouvez également supprimer des balises de cet affichage.</span><span class="sxs-lookup"><span data-stu-id="acc3a-137">You can also delete tags from this view.</span></span>

![Image de l’ajout de balises sur un appareil2](images/more-manage-tags.png)

## <a name="add-device-tags-by-setting-a-registry-key-value"></a><span data-ttu-id="acc3a-139">Ajouter des balises d’appareil en définition d’une valeur de clé de Registre</span><span class="sxs-lookup"><span data-stu-id="acc3a-139">Add device tags by setting a registry key value</span></span>

>[!NOTE]
> <span data-ttu-id="acc3a-140">Applicable uniquement sur les appareils suivants :</span><span class="sxs-lookup"><span data-stu-id="acc3a-140">Applicable only on the following devices:</span></span>
>- <span data-ttu-id="acc3a-141">Windows 10, version 1709 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="acc3a-141">Windows 10, version 1709 or later</span></span>
>- <span data-ttu-id="acc3a-142">Windows Server, version 1803 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="acc3a-142">Windows Server, version 1803 or later</span></span>
>- <span data-ttu-id="acc3a-143">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="acc3a-143">Windows Server 2016</span></span>
>- <span data-ttu-id="acc3a-144">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="acc3a-144">Windows Server 2012 R2</span></span>
>- <span data-ttu-id="acc3a-145">Windows Server 2008 R2 SP1</span><span class="sxs-lookup"><span data-stu-id="acc3a-145">Windows Server 2008 R2 SP1</span></span>
>- <span data-ttu-id="acc3a-146">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="acc3a-146">Windows 8.1</span></span>
>- <span data-ttu-id="acc3a-147">Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="acc3a-147">Windows 7 SP1</span></span>

> [!NOTE] 
> <span data-ttu-id="acc3a-148">Le nombre maximal de caractères qui peuvent être définies dans une balise est de 200.</span><span class="sxs-lookup"><span data-stu-id="acc3a-148">The maximum number of characters that can be set in a tag is 200.</span></span>

<span data-ttu-id="acc3a-149">Les appareils avec des balises similaires peuvent être pratiques lorsque vous devez appliquer une action contextuelle sur une liste spécifique d’appareils.</span><span class="sxs-lookup"><span data-stu-id="acc3a-149">Devices with similar tags can be handy when you need to apply contextual action on a specific list of devices.</span></span>

<span data-ttu-id="acc3a-150">Utilisez l’entrée de clé de Registre suivante pour ajouter une balise sur un appareil :</span><span class="sxs-lookup"><span data-stu-id="acc3a-150">Use the following registry key entry to add a tag on a device:</span></span>

- <span data-ttu-id="acc3a-151">Clé de Registre : `HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows Advanced Threat Protection\DeviceTagging\`</span><span class="sxs-lookup"><span data-stu-id="acc3a-151">Registry key: `HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows Advanced Threat Protection\DeviceTagging\`</span></span>
- <span data-ttu-id="acc3a-152">Valeur de clé de Registre (REG_SZ) : `Group`</span><span class="sxs-lookup"><span data-stu-id="acc3a-152">Registry key value (REG_SZ): `Group`</span></span>
- <span data-ttu-id="acc3a-153">Données de clé de Registre : `Name of the tag you want to set`</span><span class="sxs-lookup"><span data-stu-id="acc3a-153">Registry key data: `Name of the tag you want to set`</span></span>

>[!NOTE]
><span data-ttu-id="acc3a-154">La balise d’appareil fait partie du rapport d’informations sur l’appareil qui est généré une fois par jour.</span><span class="sxs-lookup"><span data-stu-id="acc3a-154">The device tag is part of the device information report that's generated once a day.</span></span> <span data-ttu-id="acc3a-155">Vous pouvez également choisir de redémarrer le point de terminaison qui transférerait un nouveau rapport d’informations sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="acc3a-155">As an alternative, you may choose to restart the endpoint that would transfer a new device information report.</span></span>
> 
> <span data-ttu-id="acc3a-156">Si vous devez supprimer une balise ajoutée à l’aide de la clé de Registre ci-dessus, supprimez le contenu des données de clé de Registre au lieu de supprimer la clé « Group ».</span><span class="sxs-lookup"><span data-stu-id="acc3a-156">If you need to remove a tag that was added using the above Registry key, clear the contents of the Registry key data instead of removing the 'Group' key.</span></span>
