---
title: Pourquoi utiliser PowerShell pour Microsoft 365
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 07/17/2020
audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Ent_O365
f1.keywords:
- CSH
ms.custom: ''
ms.assetid: b3209b1a-40c7-4ede-8e78-8a88bb2adc8a
description: 'Résumé : Comprendre pourquoi vous devez utiliser PowerShell pour gérer les Microsoft 365, dans certains cas plus efficacement et dans d’autres cas par nécessité.'
ms.openlocfilehash: baae3f5682edb65f1bc8114fcc96021b144b93ab
ms.sourcegitcommit: 48195345b21b409b175d68acdc25d9f2fc4fc5f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "53228422"
---
# <a name="why-you-need-to-use-powershell-for-microsoft-365"></a><span data-ttu-id="31673-103">Pourquoi utiliser PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="31673-103">Why you need to use PowerShell for Microsoft 365</span></span>

<span data-ttu-id="31673-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="31673-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="31673-105">Grâce aux Centre d’administration Microsoft 365, vous pouvez gérer vos comptes d Microsoft 365 utilisateur et vos licences.</span><span class="sxs-lookup"><span data-stu-id="31673-105">With the Microsoft 365 admin center, you can manage your Microsoft 365 user accounts and licenses.</span></span> <span data-ttu-id="31673-106">Vous pouvez également gérer vos services Microsoft 365, tels que Exchange Online, Teams et SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="31673-106">You can also manage your Microsoft 365 services, such as Exchange Online, Teams, and SharePoint Online.</span></span> <span data-ttu-id="31673-107">Si vous utilisez PowerShell à la place pour gérer ces services, vous pouvez tirer parti de l’environnement de langage de script et de ligne de commande pour la vitesse, l’automatisation et des fonctionnalités supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="31673-107">If you instead use PowerShell to manage these services, you can and take advantage of the command-line and scripting language environment for speed, automation, and additional capabilities.</span></span>

<span data-ttu-id="31673-108">Cet article montre comment utiliser PowerShell pour gérer les Microsoft 365 à :</span><span class="sxs-lookup"><span data-stu-id="31673-108">This article shows how to use PowerShell to manage Microsoft 365 to:</span></span>

- <span data-ttu-id="31673-109">Révéler des informations supplémentaires que vous ne pouvez pas voir dans la Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="31673-109">Reveal additional information that you can't see in the Microsoft 365 admin center</span></span>

- <span data-ttu-id="31673-110">Configurer les fonctionnalités et les paramètres uniquement possible avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="31673-110">Configure features and settings only possible with PowerShell</span></span>

- <span data-ttu-id="31673-111">Faire des opérations en bloc</span><span class="sxs-lookup"><span data-stu-id="31673-111">Do bulk operations</span></span>

- <span data-ttu-id="31673-112">Filtrer les données</span><span class="sxs-lookup"><span data-stu-id="31673-112">Filter data</span></span>

- <span data-ttu-id="31673-113">Imprimer ou enregistrer des données</span><span class="sxs-lookup"><span data-stu-id="31673-113">Print or save data</span></span>

- <span data-ttu-id="31673-114">Gérer entre les services</span><span class="sxs-lookup"><span data-stu-id="31673-114">Manage across services</span></span>

<span data-ttu-id="31673-115">N’oubliez pas que PowerShell pour Microsoft 365 est un ensemble de modules pour Windows PowerShell, qui est un environnement de ligne de commande pour les plateformes et les services basés sur Windows.</span><span class="sxs-lookup"><span data-stu-id="31673-115">Keep in mind that PowerShell for Microsoft 365 is a set of modules for Windows PowerShell, which is a command-line environment for Windows-based services and platforms.</span></span> <span data-ttu-id="31673-116">Cet environnement crée un langage d’environnement de commande qui peut être étendu avec des modules supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="31673-116">This environment creates a command-shell language that can be extended with additional modules.</span></span> <span data-ttu-id="31673-117">Il permet d’exécuter des commandes ou des scripts simples ou complexes.</span><span class="sxs-lookup"><span data-stu-id="31673-117">It provides a way to execute simple or complex commands or scripts.</span></span> <span data-ttu-id="31673-118">Par exemple, après avoir installé les modules PowerShell pour Microsoft 365 et vous être connecté à votre abonnement Microsoft 365, vous pouvez exécuter la commande suivante pour lister toutes les boîtes aux lettres utilisateur pour Microsoft Exchange Online :</span><span class="sxs-lookup"><span data-stu-id="31673-118">For example, after you install the PowerShell for Microsoft 365 modules and connect to your Microsoft 365 subscription, you can run the following command to list all the user mailboxes for Microsoft Exchange Online:</span></span>

```powershell
Get-Mailbox
```

<span data-ttu-id="31673-119">Vous pouvez également obtenir la liste des boîtes aux lettres à l’aide du Centre d’administration Microsoft 365 mais il n’est pas facile de compter les éléments de toutes les listes de tous les sites pour toutes vos applications web.</span><span class="sxs-lookup"><span data-stu-id="31673-119">You could also get the list of mailboxes by using the Microsoft 365 admin center but counting the items in all the lists for all the sites for all of your web apps isn't easy.</span></span>

<span data-ttu-id="31673-120">PowerShell pour Microsoft 365 est conçu pour vous aider à gérer les Microsoft 365, et non à remplacer les Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="31673-120">PowerShell for Microsoft 365 is designed to help you manage Microsoft 365, not to replace the Microsoft 365 admin center.</span></span> <span data-ttu-id="31673-121">Les administrateurs doivent être en mesure d’utiliser PowerShell pour Microsoft 365 car certaines procédures de configuration peuvent uniquement être réalisées via PowerShell pour Microsoft 365 commandes.</span><span class="sxs-lookup"><span data-stu-id="31673-121">Admins need to be able to use PowerShell for Microsoft 365 because there are some configuration procedures that can only be done through PowerShell for Microsoft 365 commands.</span></span> <span data-ttu-id="31673-122">Pour ces cas, vous devez savoir comment :</span><span class="sxs-lookup"><span data-stu-id="31673-122">For these cases, you need to know how to:</span></span>

- <span data-ttu-id="31673-123">Installez PowerShell pour Microsoft 365 modules (effectués une seule fois pour chaque ordinateur administrateur).</span><span class="sxs-lookup"><span data-stu-id="31673-123">Install the PowerShell for Microsoft 365 modules (done only one time for each administrator computer).</span></span>

- <span data-ttu-id="31673-124">Connecter à votre abonnement Microsoft 365 (une fois pour chaque session PowerShell).</span><span class="sxs-lookup"><span data-stu-id="31673-124">Connect to your Microsoft 365 subscription (one time for each PowerShell session).</span></span>

- <span data-ttu-id="31673-125">Collectez les informations nécessaires pour exécuter le PowerShell requis Microsoft 365 commandes.</span><span class="sxs-lookup"><span data-stu-id="31673-125">Gather the information needed to run the required PowerShell for Microsoft 365 commands.</span></span>

- <span data-ttu-id="31673-126">Exécutez PowerShell pour Microsoft 365 commandes.</span><span class="sxs-lookup"><span data-stu-id="31673-126">Run PowerShell for Microsoft 365 commands.</span></span>

<span data-ttu-id="31673-127">Une fois que vous avez appris ces compétences de base, vous n’avez pas besoin de lister vos utilisateurs de boîte aux lettres à l’aide de la **commande Get-Mailbox.**</span><span class="sxs-lookup"><span data-stu-id="31673-127">After you learn these basic skills, you don't have to list your mailbox users by using the **Get-Mailbox** command.</span></span> <span data-ttu-id="31673-128">Vous n’avez pas non plus besoin de comprendre comment créer une commande comme celle mentionnée précédemment pour compter tous les éléments de toutes les listes pour tous les sites de toutes vos applications web.</span><span class="sxs-lookup"><span data-stu-id="31673-128">You also don't have to understand how to create a new command like the command cited previously to count all the items in all the lists for all the sites for all of your web apps.</span></span> <span data-ttu-id="31673-129">Microsoft et la communauté d’administrateurs peuvent vous aider à effectuer les tâches nécessaires.</span><span class="sxs-lookup"><span data-stu-id="31673-129">Microsoft and the community of administrators can help you with such tasks as needed.</span></span>

## <a name="powershell-for-microsoft-365-can-reveal-information-that-you-cant-see-with-the-microsoft-365-admin-center"></a><span data-ttu-id="31673-130">PowerShell pour Microsoft 365 peut révéler des informations que vous ne pouvez pas voir avec le Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="31673-130">PowerShell for Microsoft 365 can reveal information that you can't see with the Microsoft 365 admin center</span></span>

<span data-ttu-id="31673-131">Le Centre d’administration Microsoft 365 affiche de nombreuses informations utiles.</span><span class="sxs-lookup"><span data-stu-id="31673-131">The Microsoft 365 admin center displays many useful information.</span></span> <span data-ttu-id="31673-132">Toutefois, il n’affiche pas toutes les informations que vous Microsoft 365 stockez sur les utilisateurs, les licences, les boîtes aux lettres et les sites.</span><span class="sxs-lookup"><span data-stu-id="31673-132">But it doesn't display all the possible information that Microsoft 365 stores about users, licenses, mailboxes, and sites.</span></span> <span data-ttu-id="31673-133">Voici un exemple pour les *utilisateurs et les groupes* de la Centre d’administration Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="31673-133">Here's an example for *users and groups* in the Microsoft 365 admin center:</span></span>

![Exemple d’affichage des utilisateurs et des groupes dans le Centre d’administration Microsoft 365.](../media/o365-powershell-users-and-groups.png)

<span data-ttu-id="31673-135">Cette vue fournit les informations dont vous avez besoin dans de nombreux cas.</span><span class="sxs-lookup"><span data-stu-id="31673-135">This view provides the information that you need in many cases.</span></span> <span data-ttu-id="31673-136">Toutefois, il peut arriver que vous ayez besoin de plus d'informations.</span><span class="sxs-lookup"><span data-stu-id="31673-136">However, there are times when you need more.</span></span> <span data-ttu-id="31673-137">Par exemple, Microsoft 365 licences (et les fonctionnalités Microsoft 365 disponibles pour un utilisateur) dépendent en partie de l’emplacement géographique de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="31673-137">For example, Microsoft 365 licensing (and the Microsoft 365 features available to a user) depends in part on the user's geographic location.</span></span> <span data-ttu-id="31673-138">Les stratégies et fonctionnalités que vous pouvez étendre à un utilisateur qui réside aux États-Unis peuvent ne pas être identiques à celles que vous pouvez étendre à un utilisateur en Inde ou en Belgique.</span><span class="sxs-lookup"><span data-stu-id="31673-138">The policies and features that you can extend to a user who lives in the United States might not be the same as those that you can extend to a user in India or Belgium.</span></span> <span data-ttu-id="31673-139">Suivez ces étapes dans la Centre d’administration Microsoft 365 pour déterminer l’emplacement géographique d’un utilisateur :</span><span class="sxs-lookup"><span data-stu-id="31673-139">Follow these steps in the Microsoft 365 admin center to determine a user's geographic location:</span></span>

1. <span data-ttu-id="31673-140">Double-cliquez sur l'élément **Nom d'affichage** de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="31673-140">Double-click the user's **Display Name**.</span></span>

2. <span data-ttu-id="31673-141">Dans le volet d’affichage des propriétés utilisateur, sélectionnez **détails.**</span><span class="sxs-lookup"><span data-stu-id="31673-141">In the user properties display pane, select **details**.</span></span>

3. <span data-ttu-id="31673-142">Dans l’affichage des détails, sélectionnez **des détails supplémentaires.**</span><span class="sxs-lookup"><span data-stu-id="31673-142">In the details display, select **additional details**.</span></span>

4. <span data-ttu-id="31673-143">Faites défiler jusqu’à ce que vous trouviez le titre **Pays ou région**:</span><span class="sxs-lookup"><span data-stu-id="31673-143">Scroll until you find the heading **Country or region**:</span></span>

     ![Exemple d’informations de région pour un utilisateur dans le Centre d’administration Microsoft 365.](../media/o365-powershell-usage-location.png)

5. <span data-ttu-id="31673-145">Écrivez le nom d'affichage et l'emplacement de l'utilisateur sur un morceau de papier, ou copiez-le et collez-le dans le Bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="31673-145">Write the user's display name and location on a piece of paper, or copy and paste it into Notepad.</span></span>

<span data-ttu-id="31673-146">Vous devez répéter cette procédure pour chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="31673-146">You must repeat this procedure for each user.</span></span> <span data-ttu-id="31673-147">Si vous avez de nombreux utilisateurs, ce processus peut être fastidieux.</span><span class="sxs-lookup"><span data-stu-id="31673-147">If you have many users, this process can be tedious.</span></span> <span data-ttu-id="31673-148">Avec PowerShell pour Microsoft 365, vous pouvez afficher ces informations pour tous vos utilisateurs à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="31673-148">With PowerShell for Microsoft 365, you can display this information for all of your users by using the following command:</span></span>

```powershell
Get-AzureADUser | Select DisplayName, UsageLocation
```


>[!Note]
><span data-ttu-id="31673-149">PowerShell Core ne prend pas en charge le module Microsoft Azure Active Directory pour Windows PowerShell et les cmdlets dont le nom comprend *Msol.*</span><span class="sxs-lookup"><span data-stu-id="31673-149">PowerShell Core doesn't support the Microsoft Azure Active Directory Module for Windows PowerShell module and cmdlets that have *Msol* in their name.</span></span> <span data-ttu-id="31673-150">Vous devez exécuter ces cmdlets à partir Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="31673-150">You have to run these cmdlets from Windows PowerShell.</span></span>
>

<span data-ttu-id="31673-151">Voici un exemple des résultats :</span><span class="sxs-lookup"><span data-stu-id="31673-151">Here's an example of the results:</span></span>

```powershell
DisplayName                               UsageLocation
-----------                               -------------
Bonnie Kearney                            GB
Fabrice Canel                             BR
Brian Johnson (TAILSPIN)                  US
Anne Wallace                              US
Alex Darrow                               US
David Longmuir                            BR
```

<span data-ttu-id="31673-152">L’interprétation de cette commande PowerShell est : Obtenir tous les utilisateurs de l’abonnement Microsoft 365 actuel (**Get-AzureADUser**), mais afficher uniquement le nom et l’emplacement de chaque utilisateur (**Sélectionnez DisplayName, UsageLocation**).</span><span class="sxs-lookup"><span data-stu-id="31673-152">The interpretation of this PowerShell command is: Get all of the users in the current Microsoft 365 subscription (**Get-AzureADUser**), but only display the name and location for each user (**Select DisplayName, UsageLocation**).</span></span>

<span data-ttu-id="31673-153">Étant donné que PowerShell pour Microsoft 365 prend en charge un langage d’shell de commande, vous pouvez manipuler davantage les informations obtenues par la commande **Get-AzureADUser.**</span><span class="sxs-lookup"><span data-stu-id="31673-153">Because PowerShell for Microsoft 365 supports a command-shell language, you can further manipulate the information obtained by the **Get-AzureADUser** command.</span></span> <span data-ttu-id="31673-154">Par exemple, vous souhaitez peut-être trier ces utilisateurs en fonction de leur emplacement, en regroupéssant tous les utilisateurs brésiliens, tous les utilisateurs des États-Unis, etc.</span><span class="sxs-lookup"><span data-stu-id="31673-154">For example, maybe you'd like to sort these users by their location, grouping all the Brazilian users together, all the United States users together, and so on.</span></span> <span data-ttu-id="31673-155">Voici la commande :</span><span class="sxs-lookup"><span data-stu-id="31673-155">Here's the command:</span></span>

```powershell
Get-AzureADUser | Select DisplayName, UsageLocation | Sort UsageLocation, DisplayName
```

<span data-ttu-id="31673-156">Voici un exemple des résultats :</span><span class="sxs-lookup"><span data-stu-id="31673-156">Here's an example of the results:</span></span>

```powershell
DisplayName                                 UsageLocation
-----------                                 -------------
David Longmuir                              BR
Fabrice Canel                               BR
Bonnie Kearney                              GB
Alex Darrow                                 US
Anne Wallace                                US
Brian Johnson (TAILSPIN)                    US
```

<span data-ttu-id="31673-157">L’interprétation de cette commande PowerShell est : Obtenir tous les utilisateurs de l’abonnement Microsoft 365 actuel, mais afficher uniquement le nom et l’emplacement de chaque utilisateur et les trier d’abord par leur emplacement, puis leur nom (**Sort UsageLocation, DisplayName**).</span><span class="sxs-lookup"><span data-stu-id="31673-157">The interpretation of this PowerShell command is: Get all the users in the current Microsoft 365 subscription, but only display the name and location for each user and sort them first by their location and then their name (**Sort UsageLocation, DisplayName**).</span></span>

<span data-ttu-id="31673-158">Vous pouvez également utiliser un filtrage supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="31673-158">You can also use additional filtering.</span></span> <span data-ttu-id="31673-159">Par exemple, si vous voulez uniquement voir les informations relatives aux utilisateurs basés au Brésil, utilisez cette commande :</span><span class="sxs-lookup"><span data-stu-id="31673-159">For example, if you only want to see information about users based in Brazil, use this command:</span></span>

```powershell
Get-AzureADUser | Where {$_.UsageLocation -eq "BR"} | Select DisplayName, UsageLocation
```

<span data-ttu-id="31673-160">Voici un exemple des résultats :</span><span class="sxs-lookup"><span data-stu-id="31673-160">Here's an example of the results:</span></span>

```powershell
DisplayName                                           UsageLocation
-----------                                           -------------
David Longmuir                                        BR
Fabrice Canel                                         BR
```

<span data-ttu-id="31673-161">L’interprétation de cette commande PowerShell est : Obtenir tous les utilisateurs de l’abonnement Microsoft 365 actuel dont l’emplacement est le Brésil (**Où {$ \_ . UsageLocation -eq « BR"}**), puis affiche le nom et l’emplacement de chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="31673-161">The interpretation of this PowerShell command is: Get all the users in the current Microsoft 365 subscription whose location is Brazil (**Where {$\_.UsageLocation -eq "BR"}**) and then display the name and location for each user.</span></span>

 <span data-ttu-id="31673-162">**Remarque sur les domaines de grande taille**</span><span class="sxs-lookup"><span data-stu-id="31673-162">**A note about large domains**</span></span>

<span data-ttu-id="31673-163">Si vous avez un grand domaine avec des dizaines de milliers d’utilisateurs, la tentative de certains des exemples que nous présentons dans cet article peut entraîner une limitation.</span><span class="sxs-lookup"><span data-stu-id="31673-163">If you have a large domain with tens of thousands of users, trying some of the examples we show in this article could lead to throttling.</span></span> <span data-ttu-id="31673-164">En fonction de facteurs tels que la puissance de calcul et la bande passante réseau disponible, vous essayez peut-être d’en faire trop en même temps.</span><span class="sxs-lookup"><span data-stu-id="31673-164">Based on factors like computing power and available network bandwidth, you may be trying to do too much at one time.</span></span> <span data-ttu-id="31673-165">Les grandes organisations peuvent vouloir fractionner certaines de ces opérations PowerShell en deux commandes.</span><span class="sxs-lookup"><span data-stu-id="31673-165">Large organizations might want to split some of these PowerShell operations into two commands.</span></span>

<span data-ttu-id="31673-166">Par exemple, la commande suivante renvoie tous les comptes d’utilisateur et affiche le nom et l’emplacement de chacun d’eux :</span><span class="sxs-lookup"><span data-stu-id="31673-166">For example, the following command returns all the user accounts and shows the name and location for each:</span></span>

```powershell
Get-AzureADUser | Select DisplayName, UsageLocation
```

<span data-ttu-id="31673-167">Cela fonctionne bien pour les petits domaines.</span><span class="sxs-lookup"><span data-stu-id="31673-167">That works great for smaller domains.</span></span> <span data-ttu-id="31673-168">Toutefois, dans une grande organisation, vous pouvez fractionner cette opération en deux commandes : une commande pour stocker les informations du compte d’utilisateur dans une variable et une autre pour afficher les informations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="31673-168">But in a large organization, you might want to split that operation into two commands: one command to store the user account information in a variable and another to display the needed information.</span></span> <span data-ttu-id="31673-169">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="31673-169">Here's an example:</span></span>

```powershell
$x = Get-AzureADUser
$x | Select DisplayName, UsageLocation
```

<span data-ttu-id="31673-170">L’interprétation de cet ensemble de commandes PowerShell est la :</span><span class="sxs-lookup"><span data-stu-id="31673-170">The interpretation of this set of PowerShell commands is:</span></span>
1. <span data-ttu-id="31673-171">Obtenez tous les utilisateurs de l’abonnement Microsoft 365 actuel et stockez les informations dans une variable nommée $x (**$x = Get-AzureADUser**).</span><span class="sxs-lookup"><span data-stu-id="31673-171">Get all the users in the current Microsoft 365 subscription and store the information in a variable named $x (**$x = Get-AzureADUser**).</span></span>
1.  <span data-ttu-id="31673-172">Afficher le contenu de la variable *$x,* mais inclure uniquement le nom et l’emplacement de chaque utilisateur (**$x | Sélectionnez DisplayName, UsageLocation**).</span><span class="sxs-lookup"><span data-stu-id="31673-172">Display the contents of the variable *$x*, but only include the name and location for each user (**$x | Select DisplayName, UsageLocation**).</span></span>

## <a name="microsoft-365-has-features-that-you-can-only-configure-with-powershell-for-microsoft-365"></a><span data-ttu-id="31673-173">Microsoft 365 comporte des fonctionnalités que vous pouvez uniquement configurer avec PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="31673-173">Microsoft 365 has features that you can only configure with PowerShell for Microsoft 365</span></span>

<span data-ttu-id="31673-174">Le Centre d’administration Microsoft 365 est destiné à fournir un accès aux tâches administratives courantes et utiles qui s’appliquent à la plupart des environnements.</span><span class="sxs-lookup"><span data-stu-id="31673-174">The Microsoft 365 admin center is intended to provide access to common, useful administrative tasks that apply to most environments.</span></span> <span data-ttu-id="31673-175">En d’autres termes, le Centre d’administration Microsoft 365 a été conçu pour que l’administrateur classique puisse effectuer les tâches de gestion les plus courantes.</span><span class="sxs-lookup"><span data-stu-id="31673-175">In other words, the Microsoft 365 admin center was designed so that the typical administrator can carry out the most-common management tasks.</span></span> <span data-ttu-id="31673-176">Certaines tâches ne peuvent toutefois pas être réalisées dans le Centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="31673-176">But there are some tasks that can't be done in the admin center.</span></span>

<span data-ttu-id="31673-177">Par exemple, le Centre d Skype Entreprise Online propose quelques options pour créer des invitations personnalisées aux réunions :</span><span class="sxs-lookup"><span data-stu-id="31673-177">For example, the Skype for Business Online admin center provides a few options for creating custom meeting invitations:</span></span>

![Exemple d’affichage d’invitations personnalisées à une réunion dans le Centre d’administration de Skype Entreprise Online.](../media/o365-powershell-meeting-invitation.png)

<span data-ttu-id="31673-179">Avec ces paramètres, vous pouvez ajouter une touche de personnalisation et de professionnalisme aux invitations aux réunions.</span><span class="sxs-lookup"><span data-stu-id="31673-179">With these settings, you can add a touch of personalization and professionalism to meeting invitations.</span></span> <span data-ttu-id="31673-180">Toutefois, les paramètres de configuration de réunion ne se contentent pas de créer des invitations personnalisées à une réunion.</span><span class="sxs-lookup"><span data-stu-id="31673-180">But there's more to meeting-configuration settings than simply creating custom meeting invitations.</span></span> <span data-ttu-id="31673-181">Par défaut, les réunions autorisent :</span><span class="sxs-lookup"><span data-stu-id="31673-181">For example, by default, meetings allow:</span></span>

- <span data-ttu-id="31673-182">les utilisateurs anonymes à obtenir une entrée automatique à chaque réunion ;</span><span class="sxs-lookup"><span data-stu-id="31673-182">Anonymous users to gain automatic entrance to each meeting.</span></span>

- <span data-ttu-id="31673-183">les participants à enregistrer la réunion ;</span><span class="sxs-lookup"><span data-stu-id="31673-183">Attendees to record the meeting.</span></span>

- <span data-ttu-id="31673-184">tous les utilisateurs de votre organisation à être désignés en tant que présentateurs lorsqu’ils rejoignent la réunion.</span><span class="sxs-lookup"><span data-stu-id="31673-184">All users from your organization to be designated as presenters when they join the meeting.</span></span>

<span data-ttu-id="31673-185">Ces paramètres ne sont pas disponibles dans le centre d’administration Skype Entreprise Online.</span><span class="sxs-lookup"><span data-stu-id="31673-185">These settings aren't available from the Skype for Business Online admin center.</span></span> <span data-ttu-id="31673-186">Vous pouvez les contrôler à partir de PowerShell pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="31673-186">You can control them from PowerShell for Microsoft 365.</span></span> <span data-ttu-id="31673-187">Voici une commande qui désactive ces trois paramètres :</span><span class="sxs-lookup"><span data-stu-id="31673-187">Here's a command that disables these three settings:</span></span>

```powershell
Set-CsMeetingConfiguration -AdmitAnonymousUsersByDefault $False -AllowConferenceRecording $False -DesignateAsPresenter "None"
```

> [!NOTE]
> <span data-ttu-id="31673-188">Pour exécuter cette commande, vous devez installer le [module Skype Entreprise Online PowerShell](https://www.microsoft.com/download/details.aspx?id=39366).</span><span class="sxs-lookup"><span data-stu-id="31673-188">To run this command, you must install the [Skype for Business Online PowerShell Module](https://www.microsoft.com/download/details.aspx?id=39366).</span></span>

<span data-ttu-id="31673-189">L’interprétation de cette commande PowerShell est la :</span><span class="sxs-lookup"><span data-stu-id="31673-189">The interpretation of this PowerShell command is:</span></span>

1. <span data-ttu-id="31673-190">Dans les paramètres des nouvelles réunions Skype Entreprise Online (**Set-CsMeetingConfiguration**), désactivez l’accès automatique des utilisateurs anonymes aux réunions (**-AdmitAnonymousUsersByDefault $False**).</span><span class="sxs-lookup"><span data-stu-id="31673-190">In the settings for new Skype for Business Online meetings (**Set-CsMeetingConfiguration**), disable allowing anonymous users to gain automatic entrance to meetings (**-AdmitAnonymousUsersByDefault $False**).</span></span>
2.  <span data-ttu-id="31673-191">Désactivez la possibilité pour les participants d’enregistrer les réunions (**-AllowConferenceRecording $False**).</span><span class="sxs-lookup"><span data-stu-id="31673-191">Disable the ability for attendees to record meetings (**-AllowConferenceRecording $False**).</span></span>
3. <span data-ttu-id="31673-192">Ne désignez pas tous les utilisateurs de votre organisation comme présentateurs (**-DesignateAsPresenter « None »**).</span><span class="sxs-lookup"><span data-stu-id="31673-192">Don't designate all users from your organization as presenters (**-DesignateAsPresenter "None"**).</span></span>

<span data-ttu-id="31673-193">Pour restaurer ces paramètres par défaut (activer les options), exécutez la commande ci-après :</span><span class="sxs-lookup"><span data-stu-id="31673-193">To restore these default settings (enable the options), run this command:</span></span>

```powershell
Set-CsMeetingConfiguration -AdmitAnonymousUsersByDefault $True -AllowConferenceRecording $True -DesignateAsPresenter "Company"
```

<span data-ttu-id="31673-194">Il existe également d’autres scénarios similaires, c’est pourquoi les administrateurs doivent savoir comment exécuter PowerShell pour Microsoft 365 commandes.</span><span class="sxs-lookup"><span data-stu-id="31673-194">There are other similar scenarios as well, which is why administrators should know how to run PowerShell for Microsoft 365 commands.</span></span>

## <a name="powershell-for-microsoft-365-is-great-for-bulk-operations"></a><span data-ttu-id="31673-195">PowerShell pour les Microsoft 365 est idéal pour les opérations en bloc</span><span class="sxs-lookup"><span data-stu-id="31673-195">PowerShell for Microsoft 365 is great for bulk operations</span></span>

<span data-ttu-id="31673-196">Les interfaces visuelles telles que Centre d’administration Microsoft 365 sont plus utiles lorsque vous avez une seule opération à faire.</span><span class="sxs-lookup"><span data-stu-id="31673-196">Visual interfaces like the Microsoft 365 admin center are most valuable when you have a single operation to do.</span></span> <span data-ttu-id="31673-197">Par exemple, si vous devez désactiver un compte d’utilisateur, vous pouvez utiliser le Centre d’administration pour localiser et désactiver rapidement une case à cocher.</span><span class="sxs-lookup"><span data-stu-id="31673-197">For example, if you need to disable one user account, you can use the admin center to quickly locate and clear a checkbox.</span></span> <span data-ttu-id="31673-198">Cela peut être plus facile que d’effectuer une opération similaire dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="31673-198">This may be easier than performing a similar operation in PowerShell.</span></span>

<span data-ttu-id="31673-199">Toutefois, si vous devez modifier de nombreux éléments ou certains éléments sélectionnés dans un grand nombre d’autres éléments, le Centre d’administration Microsoft 365 peut ne pas être le meilleur outil.</span><span class="sxs-lookup"><span data-stu-id="31673-199">But if you have to change many things or some selected things within a large set of other things, the Microsoft 365 admin center might not be the best tool.</span></span> <span data-ttu-id="31673-200">Par exemple, vous devez modifier le préfixe sur des milliers de numéros de téléphone ou supprimer l’utilisateur *spécifique Ken Myer* de tous vos sites SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="31673-200">For example, say you have to change the prefix on thousands of phone numbers or remove the specific user *Ken Myer* from all your SharePoint Online sites.</span></span> <span data-ttu-id="31673-201">Comment le feriez-vous dans la Centre d’administration Microsoft 365 ?</span><span class="sxs-lookup"><span data-stu-id="31673-201">How would you do that in the Microsoft 365 admin center?</span></span>

<span data-ttu-id="31673-202">Pour le dernier exemple, dites que vous avez plusieurs centaines de sites SharePoint Online et que vous ne connaissez pas ceux dont Ken Meyer est membre.</span><span class="sxs-lookup"><span data-stu-id="31673-202">For the last example, say you have several hundred SharePoint Online sites, and you don't know which ones Ken Meyer is a member of.</span></span> <span data-ttu-id="31673-203">Vous devez commencer à l’Centre d’administration Microsoft 365 puis effectuer cette procédure pour chaque site :</span><span class="sxs-lookup"><span data-stu-id="31673-203">You would have to start at the Microsoft 365 admin center and then perform this procedure for each site:</span></span>

1. <span data-ttu-id="31673-204">Sélectionnez **l’URL** du site.</span><span class="sxs-lookup"><span data-stu-id="31673-204">Select the **URL** of the site.</span></span>

2. <span data-ttu-id="31673-205">Dans la **zone des propriétés de la collection** de sites, sélectionnez le lien Adresse du site **Web** pour ouvrir le site.</span><span class="sxs-lookup"><span data-stu-id="31673-205">In the **site collection properties** box, select the **Web Site Address** link to open the site.</span></span>

3. <span data-ttu-id="31673-206">Sur le site, sélectionnez **Partager.**</span><span class="sxs-lookup"><span data-stu-id="31673-206">On the site, select **Share**.</span></span>

4. <span data-ttu-id="31673-207">Dans la **boîte de** dialogue Partager, sélectionnez le lien qui affiche tous les utilisateurs qui ont des autorisations sur le site :</span><span class="sxs-lookup"><span data-stu-id="31673-207">In the **Share** dialog box, select the link that shows all the users who have permissions to the site:</span></span>

     ![Exemple d’affichage des membres d’un site SharePoint Online dans le Centre d’administration SharePoint Online.](../media/o365-powershell-view-permissions.png)

5. <span data-ttu-id="31673-209">Dans la **boîte de dialogue Partagé avec,** sélectionnez **Avancé.**</span><span class="sxs-lookup"><span data-stu-id="31673-209">In the **Shared With** dialog box, select **Advanced**.</span></span>

6. <span data-ttu-id="31673-210">Faites défiler la liste des utilisateurs vers le bas, recherchez et sélectionnez Ken Myer (en supposant qu’il dispose d’autorisations sur le site), puis sélectionnez Supprimer les **autorisations utilisateur.**</span><span class="sxs-lookup"><span data-stu-id="31673-210">Scroll down the list of users, find and select Ken Myer (assuming he has permissions to the site), and then select **Remove User Permissions**.</span></span>

<span data-ttu-id="31673-211">Cela peut prendre beaucoup *de temps* pour plusieurs centaines de sites.</span><span class="sxs-lookup"><span data-stu-id="31673-211">This would take a *long* time for several hundred sites.</span></span>

<span data-ttu-id="31673-212">L’alternative consiste à exécuter la commande suivante dans PowerShell pour Microsoft 365 pour supprimer Ken Myer de tous vos sites :</span><span class="sxs-lookup"><span data-stu-id="31673-212">The alternative is to run the following command in PowerShell for Microsoft 365 to remove Ken Myer from all your sites:</span></span>

```powershell
Get-SPOSite | ForEach {Remove-SPOUser -Site $_.Url -LoginName "kenmyer@litwareinc.com"}
```

> [!NOTE]
> <span data-ttu-id="31673-213">Cette commande nécessite que vous installiez SharePoint [module PowerShell en ligne.](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)</span><span class="sxs-lookup"><span data-stu-id="31673-213">This command requires that you install the [SharePoint Online PowerShell module](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps).</span></span>

<span data-ttu-id="31673-214">L’interprétation de cette commande PowerShell est : Obtenir tous les sites SharePoint dans l’abonnement Microsoft 365 actuel (**Get-SPOSite**) et pour chaque site, supprimez KenLier de la liste des utilisateurs qui peuvent y accéder (**ForEach {Remove-SPOUser -Site $ \_ . Url -LoginName « kenmyer \@ litwareinc.com"}**).</span><span class="sxs-lookup"><span data-stu-id="31673-214">The interpretation of this PowerShell command is: Get all of the SharePoint sites in the current Microsoft 365 subscription (**Get-SPOSite**) and for each site remove Ken Meyer from the list of users who can access it (**ForEach {Remove-SPOUser -Site $\_.Url -LoginName "kenmyer\@litwareinc.com"}**).</span></span>

<span data-ttu-id="31673-215">Nous vous Microsoft 365 de supprimer Ken Meyer de chaque site, y compris ceux à lesquels il n’a pas accès.</span><span class="sxs-lookup"><span data-stu-id="31673-215">We tell Microsoft 365 to remove Ken Meyer from every site, including those that he doesn't have access to.</span></span> <span data-ttu-id="31673-216">Les résultats indiquent donc des erreurs pour les sites à qui il n’a pas accès.</span><span class="sxs-lookup"><span data-stu-id="31673-216">So the results will show errors for those sites that he doesn't have access to.</span></span> <span data-ttu-id="31673-217">Nous pouvons utiliser une condition supplémentaire sur cette commande pour supprimer KenCourir uniquement des sites qui l’ont sur leur liste de connexion.</span><span class="sxs-lookup"><span data-stu-id="31673-217">We can use an additional condition on this command to remove Ken Meyer only from the sites that have him on their login list.</span></span> <span data-ttu-id="31673-218">Toutefois, les erreurs renvoyées ne provoquent aucun dommage pour les sites eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="31673-218">But the errors that are returned cause no harm to the sites themselves.</span></span> <span data-ttu-id="31673-219">Cette commande peut prendre quelques minutes pour s’exécuter sur des centaines de sites, plutôt que des heures de travail sur le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="31673-219">This command might take a few minutes to run against hundreds of sites, rather than hours of working through the Microsoft 365 admin center.</span></span>

<span data-ttu-id="31673-220">Voici un autre exemple d’opération en bloc.</span><span class="sxs-lookup"><span data-stu-id="31673-220">Here's another bulk operation example.</span></span> <span data-ttu-id="31673-221">Utilisez cette commande pour ajouter Une nouvelle administrateur SharePoint *à* tous les sites de l’organisation :</span><span class="sxs-lookup"><span data-stu-id="31673-221">Use this command to add *Bonnie Kearney*, a new SharePoint administrator, to all sites in the organization:</span></span>

```powershell
Get-SPOSite | ForEach {Add-SPOUser -Site $_.Url -LoginName "bkearney@litwareinc.com" -Group "Members"}
```

<span data-ttu-id="31673-222">L’interprétation de cette commande PowerShell est la : Obtenir tous les sites SharePoint dans l’abonnement Microsoft 365 actuel et pour chaque site autoriser l’accès à Las Kearney en ajoutant son nom de connexion au groupe Membres du site (**ForEach {Add-SPOUser -Site $ \_ . Url -LoginName « bkearney \@ litwareinc.com » -Group « Members"}**).</span><span class="sxs-lookup"><span data-stu-id="31673-222">The interpretation of this PowerShell command is: Get all the SharePoint sites in the current Microsoft 365 subscription and for each site allow Bonnie Kearney access by adding her login name to the Members group of the site (**ForEach {Add-SPOUser -Site $\_.Url -LoginName "bkearney\@litwareinc.com" -Group "Members"}**).</span></span>

## <a name="powershell-for-microsoft-365-is-great-at-filtering-data"></a><span data-ttu-id="31673-223">PowerShell pour Microsoft 365 est idéal pour filtrer des données</span><span class="sxs-lookup"><span data-stu-id="31673-223">PowerShell for Microsoft 365 is great at filtering data</span></span>

<span data-ttu-id="31673-224">Le Centre d’administration Microsoft 365 propose plusieurs façons de filtrer vos données pour localiser facilement un sous-ensemble ciblé d’informations.</span><span class="sxs-lookup"><span data-stu-id="31673-224">The Microsoft 365 admin center provides several ways to filter your data to easily locate a targeted subset of information.</span></span> <span data-ttu-id="31673-225">Par exemple, Exchange facilite le filtrage sur pratiquement toutes les propriétés de la boîte aux lettres d'un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="31673-225">For example, Exchange makes it easy to filter on practically any property of a user mailbox.</span></span> <span data-ttu-id="31673-226">Par exemple, voici la liste des boîtes aux lettres pour tous les utilisateurs qui habitent à Bloomington :</span><span class="sxs-lookup"><span data-stu-id="31673-226">For example, here's the list of mailboxes for all the users who live in the city of Bloomington:</span></span>

![Exemple d’une recherche avancée dans le Centre d’administration Microsoft 365 liste des boîtes aux lettres de tous les utilisateurs qui habitent à Bloomington.](../media/o365-powershell-advanced-search.png)

<span data-ttu-id="31673-228&quot;>Le Centre d'administration Exchange vous permet également de combiner des critères de filtre.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;31673-228&quot;>The Exchange Admin center also lets you combine filter criteria.</span></span> <span data-ttu-id=&quot;31673-229&quot;>Par exemple, vous pouvez trouver les boîtes aux lettres de toutes les personnes qui habitent à Bloomington et travaillent au service financier.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;31673-229&quot;>For example, you can find the mailboxes for all the people who live in Bloomington and work in the Finance department.</span></span>

<span data-ttu-id=&quot;31673-230&quot;>Toutefois, il existe des limites à ce que vous pouvez faire dans le Centre d Exchange’administration.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;31673-230&quot;>But there are limitations to what you can do in the Exchange Admin center.</span></span> <span data-ttu-id=&quot;31673-231&quot;>Par exemple, vous ne pouviez pas trouver aussi facilement les boîtes aux lettres des personnes qui habitent à *Bloomington* ou San Diego, ou les boîtes aux lettres de toutes les personnes qui n’habitent pas à Bloomington.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;31673-231&quot;>For example, you couldn't as easily find the mailboxes of people who live in Bloomington *or* San Diego, or the mailboxes for all people who don't live in Bloomington.</span></span>

<span data-ttu-id=&quot;31673-232&quot;>Vous pouvez utiliser la commande PowerShell pour Microsoft 365 suivante pour obtenir la liste des boîtes aux lettres de toutes les personnes qui habitent à Bloomington ou San Diego :</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;31673-232&quot;>You can use the following PowerShell for Microsoft 365 command to get a list of mailboxes for all the people who live in Bloomington or San Diego:</span></span>

```powershell
Get-User | Where {$_.RecipientTypeDetails -eq &quot;UserMailbox&quot; -and ($_.City -eq &quot;San Diego&quot; -or $_.City -eq &quot;Bloomington")} | Select DisplayName, City
```

<span data-ttu-id="31673-233">Voici un exemple des résultats :</span><span class="sxs-lookup"><span data-stu-id="31673-233">Here's an example of the results:</span></span>

```powershell
DisplayName                              City
-----------                              ----
Alex Darrow                              San Diego
Bonnie Kearney                           San Diego
Julian Isla                              Bloomington
Rob Young                                Bloomington
```

<span data-ttu-id="31673-234">L’interprétation de cette commande PowerShell est : Obtenir tous les utilisateurs de l’abonnement Microsoft 365 actuel qui ont une boîte aux lettres dans la ville de San Diego ou Bloomington (**Où {$ \_ . RecipientTypeDetails -eq « UserMailbox » -and ($ \_ . City -eq « San Diego » -or $ \_ . Ville -eq « Bloomington »)}**), puis afficher le nom et la ville pour chaque (**Sélectionnez DisplayName, Ville**).</span><span class="sxs-lookup"><span data-stu-id="31673-234">The interpretation of this PowerShell command is: Get all the users in the current Microsoft 365 subscription who have a mailbox in the city of San Diego or Bloomington (**Where {$\_.RecipientTypeDetails -eq "UserMailbox" -and ($\_.City -eq "San Diego" -or $\_.City -eq "Bloomington")}**), and then display the name and city for each (**Select DisplayName, City**).</span></span>

<span data-ttu-id="31673-235">Et voici la commande pour lister toutes les boîtes aux lettres des personnes qui habitent n’importe où à l’exception de Bloomington :</span><span class="sxs-lookup"><span data-stu-id="31673-235">And here's the command to list all the mailboxes for people who live anywhere except Bloomington:</span></span>

```powershell
Get-User | Where {$_.RecipientTypeDetails -eq "UserMailbox" -and $_.City -ne "Bloomington"} | Select DisplayName, City
```

<span data-ttu-id="31673-236">Voici un exemple des résultats :</span><span class="sxs-lookup"><span data-stu-id="31673-236">Here's an example of the results:</span></span>

```powershell
DisplayName                               City
-----------                               ----
MOD Administrator                         Redmond
Alex Darrow                               San Diego
Allie Bellew                              Bellevue
Anne Wallace                              Louisville
Aziz Hassouneh                            Cairo
Belinda Newman                            Charlotte
Bonnie Kearney                            San Diego
David Longmuir                            Waukesha
Denis Dehenne                             Birmingham
Garret Vargas                             Seattle
Garth Fort                                Tulsa
Janet Schorr                              Bellevue
```

<span data-ttu-id="31673-237">L’interprétation de cette commande PowerShell est : Obtenir tous les utilisateurs de l’abonnement Microsoft 365 actuel qui ont une boîte aux lettres qui ne se trouve pas dans la ville de Bloomington (**Où {$ \_ . RecipientTypeDetails -eq « UserMailbox » -and $ \_ . City -ne « Bloomington"}**), puis afficher le nom et la ville pour chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="31673-237">The interpretation of this PowerShell command is: Get all the users in the current Microsoft 365 subscription who have a mailbox not located in the city of Bloomington (**Where {$\_.RecipientTypeDetails -eq "UserMailbox" -and $\_.City -ne "Bloomington"}**), and then display the name and city for each.</span></span>

### <a name="use-wildcards"></a><span data-ttu-id="31673-238">Utiliser des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="31673-238">Use wildcards</span></span>

<span data-ttu-id="31673-239">Vous pouvez également utiliser des caractères génériques dans vos filtres PowerShell pour faire correspondre une partie d’un nom.</span><span class="sxs-lookup"><span data-stu-id="31673-239">You can also use wildcard characters in your PowerShell filters to match part of a name.</span></span> <span data-ttu-id="31673-240">Par exemple, supposons que vous recherchiez un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="31673-240">For example, suppose you're looking for a user account.</span></span> <span data-ttu-id="31673-241">Tout ce que vous vous souvenez, c’est que le nom de famille de l’utilisateur était *Anderson* ou *peut-être À la place* de *Sondesser ou Dersonson*.</span><span class="sxs-lookup"><span data-stu-id="31673-241">All you can remember is that the user's last name was *Anderson* or maybe *Henderson* or *Jorgenson*.</span></span>

<span data-ttu-id="31673-242">Vous pouvez suivre cet utilisateur dans le Centre d’administration Microsoft 365 l’aide de l’outil de recherche et effectuer trois recherches différentes :</span><span class="sxs-lookup"><span data-stu-id="31673-242">You could track down that user in the Microsoft 365 admin center by using the search tool and carrying out three different searches:</span></span>

- <span data-ttu-id="31673-243">Une sur  *Anderson*</span><span class="sxs-lookup"><span data-stu-id="31673-243">One for  *Anderson*</span></span>

- <span data-ttu-id="31673-244">Une sur  *Henderson*</span><span class="sxs-lookup"><span data-stu-id="31673-244">One for  *Henderson*</span></span>

- <span data-ttu-id="31673-245">Une sur  *Jorgenson*</span><span class="sxs-lookup"><span data-stu-id="31673-245">One for  *Jorgenson*</span></span>

<span data-ttu-id="31673-246">Étant donné que ces trois noms se terminent par « son », vous pouvez indiquer à PowerShell d’afficher tous les utilisateurs dont le nom se termine par « son ».</span><span class="sxs-lookup"><span data-stu-id="31673-246">Because all three of these names end in "son", you can tell PowerShell to display all the users whose name ends in "son".</span></span> <span data-ttu-id="31673-247">Voici la commande :</span><span class="sxs-lookup"><span data-stu-id="31673-247">Here's the command:</span></span>

```powershell
Get-User -Filter '{LastName -like "*son"}'
```

<span data-ttu-id="31673-248">L’interprétation de cette commande PowerShell est : Obtenir tous les utilisateurs de l’abonnement Microsoft 365 actuel, mais utiliser un filtre qui répertorie uniquement les utilisateurs dont le nom de famille se termine par « son » (**-Filter '{LastName -like " \* son"}'**).</span><span class="sxs-lookup"><span data-stu-id="31673-248">The interpretation of this PowerShell command is: Get all the users in the current Microsoft 365 subscription, but use a filter that only lists the users whose last names end in "son" (**-Filter '{LastName -like "\*son"}'**).</span></span> <span data-ttu-id="31673-249">Signifie tout ensemble de caractères, qui sont des lettres dans le nom \* de famille de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="31673-249">The \* stands for any set of characters, which are letters in the user's last name.</span></span>

## <a name="powershell-for-microsoft-365-makes-it-easy-to-print-or-save-data"></a><span data-ttu-id="31673-250">PowerShell pour Microsoft 365 facilite l’impression ou l’enregistrer des données</span><span class="sxs-lookup"><span data-stu-id="31673-250">PowerShell for Microsoft 365 makes it easy to print or save data</span></span>

<span data-ttu-id="31673-251">Le Centre d’administration Microsoft 365 vous permet d’afficher des listes de données.</span><span class="sxs-lookup"><span data-stu-id="31673-251">The Microsoft 365 admin center lets you view lists of data.</span></span> <span data-ttu-id="31673-252">Voici un exemple du Centre d’administration Skype Entreprise Online affichant la liste des utilisateurs qui ont été activés pour Skype Entreprise Online :</span><span class="sxs-lookup"><span data-stu-id="31673-252">Here's an example of the Skype for Business Online admin center displaying a list of users who have been enabled for Skype for Business Online:</span></span>

![Exemple de liste d’utilisateurs ayant été activés pour Skype Entreprise Online, affichée dans le Centre d’administration de Skype Entreprise Online.](../media/o365-powershell-lync-users.png)

<span data-ttu-id="31673-254">Pour enregistrer ces informations dans un fichier, vous devez les coller dans un document ou Microsoft Excel feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="31673-254">To save that information to a file, you must paste it into a document or Microsoft Excel worksheet.</span></span> <span data-ttu-id="31673-255">Les deux cas peuvent nécessiter une mise en forme supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="31673-255">Either case might require additional formatting.</span></span> <span data-ttu-id="31673-256">En outre, le Centre d’administration Microsoft 365 ne fournit pas un moyen d’imprimer directement la liste affichée.</span><span class="sxs-lookup"><span data-stu-id="31673-256">Additionally, the Microsoft 365 admin center doesn't provide a way to directly print the displayed list.</span></span>

<span data-ttu-id="31673-257">Heureusement, vous pouvez utiliser PowerShell non seulement pour afficher la liste, mais aussi pour l’enregistrer dans un fichier qui peut être facilement importé dans Excel.</span><span class="sxs-lookup"><span data-stu-id="31673-257">Fortunately, you can use PowerShell to not only display the list but to save it to a file that can be easily imported into Excel.</span></span> <span data-ttu-id="31673-258">Voici un exemple de commande pour enregistrer les données utilisateur Skype Entreprise Online dans un fichier de valeurs séparées par des virgules (CSV), qui peut ensuite être facilement importé en tant que table dans une feuille de calcul Excel :</span><span class="sxs-lookup"><span data-stu-id="31673-258">Here's an example command to save Skype for Business Online user data to a comma-separated values (CSV) file, which can then be easily imported as a table in an Excel worksheet:</span></span>

```powershell
Get-CsOnlineUser | Select DisplayName, UserPrincipalName, UsageLocation | Export-Csv -Path "C:\Logs\SfBUsers.csv" -NoTypeInformation
```

<span data-ttu-id="31673-259">Voici un exemple des résultats :</span><span class="sxs-lookup"><span data-stu-id="31673-259">Here's an example of the results:</span></span>

![Exemple de tableau importé dans une feuille de calcul Excel pour Skype Entreprise données utilisateur en ligne enregistrées dans un fichier de valeurs séparées par des virgules.](../media/o365-powershell-data-in-excel.png)

<span data-ttu-id="31673-261">L’interprétation de cette commande PowerShell est : Obtenir tous les utilisateurs Skype Entreprise Online dans l’abonnement Microsoft 365 actuel (**Get-CsOnlineUser**) ; obtenir uniquement le nom d’utilisateur, l’UPN et l’emplacement (**Select DisplayName, UserPrincipalName, UsageLocation**) ; puis enregistrez ces informations dans un fichier CSV nommé C: \\ Logs \\SfBUsers.csv (**Export-Csv -Path « C: \\ Logs \\SfBUsers.csv » -NoTypeInformation**).</span><span class="sxs-lookup"><span data-stu-id="31673-261">The interpretation of this PowerShell command is: Get all the Skype for Business Online users in the current Microsoft 365 subscription (**Get-CsOnlineUser**); obtain only the user name, UPN, and location (**Select DisplayName, UserPrincipalName, UsageLocation**); and then save that information in a CSV file named C:\\Logs\\SfBUsers.csv (**Export-Csv -Path "C:\\Logs\\SfBUsers.csv" -NoTypeInformation**).</span></span>

<span data-ttu-id="31673-262">Vous pouvez également utiliser des options pour enregistrer cette liste en tant que fichier XML ou page HTML.</span><span class="sxs-lookup"><span data-stu-id="31673-262">You can also use options to save this list as an XML file or an HTML page.</span></span> <span data-ttu-id="31673-263">En fait, avec des commandes PowerShell supplémentaires, vous pouvez l’enregistrer directement en tant que fichier Excel, avec n’importe quelle mise en forme personnalisée que vous souhaitez.</span><span class="sxs-lookup"><span data-stu-id="31673-263">In fact, with additional PowerShell commands, you could save it directly as an Excel file, with any custom formatting you want.</span></span>

<span data-ttu-id="31673-264">Vous pouvez également envoyer la sortie d’une commande PowerShell qui affiche une liste directement à l’imprimante par défaut dans Windows.</span><span class="sxs-lookup"><span data-stu-id="31673-264">You can also send the output of a PowerShell command that displays a list directly to the default printer in Windows.</span></span> <span data-ttu-id="31673-265">Voici un exemple de commande :</span><span class="sxs-lookup"><span data-stu-id="31673-265">Here's an example command:</span></span>

```powershell
Get-CsOnlineUser | Select DisplayName, UserPrincipalName, UsageLocation | Out-Printer
```

<span data-ttu-id="31673-266">Le document imprimé aura l'apparence suivante :</span><span class="sxs-lookup"><span data-stu-id="31673-266">Here's what your printed document will look like:</span></span>

![Exemple de document imprimé qui était la sortie d’une commande PowerShell envoyée directement à l’imprimante par défaut dans Windows.](../media/o365-powershell-printed-data.png)

<span data-ttu-id="31673-268">L’interprétation de cette commande PowerShell est la Skype Entreprise utilisateurs en ligne dans l’abonnement Microsoft 365 actuel ; obtenir uniquement le nom d’utilisateur, l’UPN et l’emplacement ; puis envoyez ces informations à l’imprimante Windows par défaut (**Out-Printer**).</span><span class="sxs-lookup"><span data-stu-id="31673-268">The interpretation of this PowerShell command is: Get all the Skype for Business Online users in the current Microsoft 365 subscription; obtain only the user name, UPN, and location; and then send that information to the default Windows printer (**Out-Printer**).</span></span>

<span data-ttu-id="31673-269">Le document imprimé a la même mise en forme simple que l’affichage dans la fenêtre de commande PowerShell.</span><span class="sxs-lookup"><span data-stu-id="31673-269">The printed document has the same simple formatting as the display in the PowerShell command window.</span></span> <span data-ttu-id="31673-270">Pour obtenir une copie papier, ajoutez **simplement | Out-Printer** à la fin de la commande.</span><span class="sxs-lookup"><span data-stu-id="31673-270">To get a hard copy, just add **| Out-Printer** to the end of the command.</span></span>

## <a name="powershell-for-microsoft-365-lets-you-manage-across-server-products"></a><span data-ttu-id="31673-271">PowerShell pour Microsoft 365 vous permet de gérer les différents produits serveur</span><span class="sxs-lookup"><span data-stu-id="31673-271">PowerShell for Microsoft 365 lets you manage across server products</span></span>

<span data-ttu-id="31673-272">Les composants qui Microsoft 365 sont conçus pour fonctionner ensemble.</span><span class="sxs-lookup"><span data-stu-id="31673-272">The components that make up Microsoft 365 are designed to work together.</span></span> <span data-ttu-id="31673-273">Par exemple, supposons que vous ajoutez un nouvel utilisateur à Microsoft 365 et que vous spécifiez des informations telles que le service et le numéro de téléphone de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="31673-273">For example, suppose you add a new user to Microsoft 365, and you specify such information as the user's department and phone number.</span></span> <span data-ttu-id="31673-274">Ces informations seront ensuite disponibles si vous accédez aux informations de l’utilisateur dans l’un des services Microsoft 365 : Skype Entreprise Online, Exchange ou SharePoint.</span><span class="sxs-lookup"><span data-stu-id="31673-274">That information will then be available if you access the user's information in any of the Microsoft 365 services: Skype for Business Online, Exchange, or SharePoint.</span></span>

<span data-ttu-id="31673-275">Toutefois, ceci concerne les informations communes qui couvrent une suite de produits.</span><span class="sxs-lookup"><span data-stu-id="31673-275">But that's for common information that spans the suite of products.</span></span> <span data-ttu-id="31673-276">Les informations spécifiques au produit, telles que les informations sur la boîte aux lettres Exchange’un utilisateur, ne sont généralement pas disponibles dans la suite.</span><span class="sxs-lookup"><span data-stu-id="31673-276">Product-specific information, such as information about a user's Exchange mailbox, isn't typically available across the suite.</span></span> <span data-ttu-id="31673-277">Par exemple, les informations permettant d’activer ou non la boîte aux lettres d’un utilisateur sont disponibles uniquement dans Exchange’administration centrale.</span><span class="sxs-lookup"><span data-stu-id="31673-277">For example, information about whether a user's mailbox is enabled or not is available only in the Exchange admin center.</span></span>

<span data-ttu-id="31673-278">Supposons que vous souhaitiez établir un rapport qui présente les informations suivantes pour tous les utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="31673-278">Suppose you'd like to make a report that shows the following information for all your users:</span></span>

- <span data-ttu-id="31673-279">Nom complet de l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="31673-279">The user's display name</span></span>

- <span data-ttu-id="31673-280">Si l’utilisateur est titulaire d’une licence Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="31673-280">Whether the user is licensed for Microsoft 365</span></span>

- <span data-ttu-id="31673-281">Si la boîte aux lettres Exchange de l'utilisateur a été activée</span><span class="sxs-lookup"><span data-stu-id="31673-281">Whether the user's Exchange mailbox has been enabled</span></span>

- <span data-ttu-id="31673-282">Si l'utilisateur est activé pour Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="31673-282">Whether the user is enabled for Skype for Business Online</span></span>

<span data-ttu-id="31673-283">Vous ne pouvez pas facilement produire un tel rapport dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="31673-283">You can't easily produce such a report in the Microsoft 365 admin center.</span></span> <span data-ttu-id="31673-284">Au lieu de cela, vous devez créer un document distinct pour stocker les informations, telles qu’Excel feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="31673-284">Instead, you would have to create a separate document to store the information, such as an Excel worksheet.</span></span> <span data-ttu-id="31673-285">Ensuite, obtenez tous les noms d’utilisateur et les informations de licence du Centre d’administration Microsoft 365, obtenez des informations de boîte aux lettres à partir du Centre d’administration Exchange, obtenez des informations Skype Entreprise Online à partir du Centre d’administration Skype Entreprise Online, puis combinez ces informations.</span><span class="sxs-lookup"><span data-stu-id="31673-285">Then, get all the user names and licensing information from the Microsoft 365 admin center, get mailbox information from the Exchange Admin center, get Skype for Business Online information from the Skype for Business Online Admin center, and then combine that information.</span></span>

<span data-ttu-id="31673-286">L’alternative consiste à utiliser un script PowerShell pour compiler le rapport à votre place.</span><span class="sxs-lookup"><span data-stu-id="31673-286">The alternative is to use a PowerShell script to compile the report for you.</span></span>

<span data-ttu-id="31673-287">L’exemple de script suivant est plus compliqué que les commandes que vous avez vues jusqu’à présent dans cet article.</span><span class="sxs-lookup"><span data-stu-id="31673-287">The following example script is more complicated than the commands you've seen so far in this article.</span></span> <span data-ttu-id="31673-288">Toutefois, il montre le potentiel de l’utilisation de PowerShell pour créer des affichages d’informations difficiles à obtenir autrement.</span><span class="sxs-lookup"><span data-stu-id="31673-288">But, it shows the potential of using PowerShell to create information views that are difficult to get otherwise.</span></span> <span data-ttu-id="31673-289">Voici le script pour compiler et afficher la liste dont vous avez besoin :</span><span class="sxs-lookup"><span data-stu-id="31673-289">Here's the script to compile and display the list you need:</span></span>

```powershell
$x = Get-AzureADUser

foreach ($i in $x)
    {
      $y = Get-Mailbox -Identity $i.UserPrincipalName
      $i | Add-Member -MemberType NoteProperty -Name IsMailboxEnabled -Value $y.IsMailboxEnabled

      $y = Get-CsOnlineUser -Identity $i.UserPrincipalName
      $i | Add-Member -MemberType NoteProperty -Name EnabledForSfB -Value $y.Enabled
    }

$x | Select DisplayName, IsLicensed, IsMailboxEnabled, EnabledforSfB
```

<span data-ttu-id="31673-290">Voici un exemple des résultats :</span><span class="sxs-lookup"><span data-stu-id="31673-290">Here's an example of the results:</span></span>

```powershell
DisplayName             IsLicensed   IsMailboxEnabled   EnabledForSfB
-----------             ----------   ----------------   --------------
Bonnie Kearney          True         True               True
Fabrice Canel           True         True               True
Brian Johnson           False        True               False
Anne Wallace            True         True               True
Alex Darrow             True         True               True
David Longmuir          True         True               True
Katy Jordan             False        True               False
Molly Dempsey           False        True               False
```

<span data-ttu-id="31673-291">L’interprétation de ce script PowerShell est la suivant :</span><span class="sxs-lookup"><span data-stu-id="31673-291">The interpretation of this PowerShell script is:</span></span>

1. <span data-ttu-id="31673-292">Obtenez tous les utilisateurs de l’abonnement Microsoft 365 actuel et stockez les informations dans une variable nommée *$x* (**$x = Get-AzureADUser**).</span><span class="sxs-lookup"><span data-stu-id="31673-292">Get all the users in the current Microsoft 365 subscription and store the information in a variable that's named *$x* (**$x = Get-AzureADUser**).</span></span>
1. <span data-ttu-id="31673-293">Démarrez une boucle qui s’exécute sur tous les utilisateurs de la variable $x **(foreach ($i en $x)**).</span><span class="sxs-lookup"><span data-stu-id="31673-293">Start a loop that runs over all the users in the variable $x (**foreach ($i in $x)**).</span></span>
1. <span data-ttu-id="31673-294">Définissez une variable nommée *$y* et stockez-y les informations de boîte aux lettres de l’utilisateur (**$y = Get-Mailbox -Identity $i.UserPrincipalName**).</span><span class="sxs-lookup"><span data-stu-id="31673-294">Define a variable named *$y* and store the user's mailbox information in it (**$y = Get-Mailbox -Identity $i.UserPrincipalName**).</span></span>
1. <span data-ttu-id="31673-295">Ajoutez une nouvelle propriété aux informations utilisateur *nommées IsMailBoxEnabled*.</span><span class="sxs-lookup"><span data-stu-id="31673-295">Add a new property to the user information that's named *IsMailBoxEnabled*.</span></span> <span data-ttu-id="31673-296">Définissez-la sur la valeur de la propriété IsMailBoxEnabled de la boîte aux lettres de l’utilisateur (**$i | Add-Member -MemberType NoteProperty -Name IsMailboxEnabled -Value $y.IsMailboxEnabled**).</span><span class="sxs-lookup"><span data-stu-id="31673-296">Set it to the value of the IsMailBoxEnabled property of the user's mailbox (**$i | Add-Member -MemberType NoteProperty -Name IsMailboxEnabled -Value $y.IsMailboxEnabled**).</span></span>
1. <span data-ttu-id="31673-297">Définissez une variable nommée *$y* et stockez-y les informations Skype Entreprise Online de l’utilisateur (**$y = Get-CsOnlineUser -Identity $i.UserPrincipalName**).</span><span class="sxs-lookup"><span data-stu-id="31673-297">Define a variable named *$y*, and store the user's Skype for Business Online information in it (**$y = Get-CsOnlineUser -Identity $i.UserPrincipalName**).</span></span>
1. <span data-ttu-id="31673-298">Ajoutez une nouvelle propriété aux informations utilisateur *nommées EnabledForSfB*.</span><span class="sxs-lookup"><span data-stu-id="31673-298">Add a new property to the user information that's named *EnabledForSfB*.</span></span> <span data-ttu-id="31673-299">Définissez-la sur la valeur de la propriété Enabled des informations Skype Entreprise Online de l’utilisateur (**$i | Add-Member -MemberType NoteProperty -Name EnabledForSfB -Value $y.Enabled**).</span><span class="sxs-lookup"><span data-stu-id="31673-299">Set it to the value of the Enabled property of the user's Skype for Business Online information (**$i | Add-Member -MemberType NoteProperty -Name EnabledForSfB -Value $y.Enabled**).</span></span>
1. <span data-ttu-id="31673-300">Affichez la liste des utilisateurs, mais incluez uniquement leur nom, s’ils sont titulaires d’une licence ou non, et les deux nouvelles propriétés qui indiquent si leur boîte aux lettres est activée et si elles sont activées pour Skype Entreprise Online (**$x | Sélectionnez DisplayName, IsLicensed, IsMailboxEnabled, EnabledforSfB**).</span><span class="sxs-lookup"><span data-stu-id="31673-300">Display the list of users, but include only their name, whether they are licensed, and the two new properties that indicate whether their mailbox is enabled and whether they are enabled for Skype for Business Online (**$x | Select DisplayName, IsLicensed, IsMailboxEnabled, EnabledforSfB**).</span></span>

## <a name="see-also"></a><span data-ttu-id="31673-301">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31673-301">See also</span></span>

[<span data-ttu-id="31673-302">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="31673-302">Get started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)

[<span data-ttu-id="31673-303">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="31673-303">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)

[<span data-ttu-id="31673-304">Utilisez Windows PowerShell pour créer des rapports dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="31673-304">Use Windows PowerShell to create reports in Microsoft 365</span></span>](use-windows-powershell-to-create-reports-in-microsoft-365.md)