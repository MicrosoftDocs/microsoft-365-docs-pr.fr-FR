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
description: 'Résumé : Découvrez pourquoi vous devez utiliser PowerShell pour gérer Microsoft 365, dans certains cas plus efficacement et dans d’autres cas, par nécessité.'
ms.openlocfilehash: d56a2cc47a06be911f1fd38aea3a557c631d2db0
ms.sourcegitcommit: 66b8fc1d8ba4f17487cd2004ac19cf2fff472f3d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/24/2020
ms.locfileid: "48754105"
---
# <a name="why-you-need-to-use-powershell-for-microsoft-365"></a><span data-ttu-id="f4131-103">Pourquoi utiliser PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f4131-103">Why you need to use PowerShell for Microsoft 365</span></span>

<span data-ttu-id="f4131-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="f4131-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="f4131-105">Avec le centre d’administration Microsoft 365, vous pouvez gérer vos licences et comptes d’utilisateur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f4131-105">With the Microsoft 365 admin center, you can manage your Microsoft 365 user accounts and licenses.</span></span> <span data-ttu-id="f4131-106">Vous pouvez également gérer vos services Microsoft 365, comme Exchange Online, teams et SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="f4131-106">You can also manage your Microsoft 365 services, such as Exchange Online, Teams, and SharePoint Online.</span></span> <span data-ttu-id="f4131-107">Si, à la place, vous utilisez PowerShell pour gérer ces services, vous pouvez et tirer parti de la ligne de commande et de l’environnement de langage de script pour la vitesse, l’automatisation et les fonctionnalités supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="f4131-107">If you instead use PowerShell to manage these services, you can and take advantage of the command-line and scripting language environment for speed, automation, and additional capabilities.</span></span>
  
<span data-ttu-id="f4131-108">Cet article explique comment utiliser PowerShell pour gérer Microsoft 365 afin de :</span><span class="sxs-lookup"><span data-stu-id="f4131-108">This article shows how to use PowerShell to manage Microsoft 365 to:</span></span>
  
- <span data-ttu-id="f4131-109">Révéler des informations supplémentaires qui ne sont pas visibles dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f4131-109">Reveal additional information that you can't see in the Microsoft 365 admin center</span></span>
    
- <span data-ttu-id="f4131-110">Configuration des fonctionnalités et des paramètres uniquement avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="f4131-110">Configure features and settings only possible with PowerShell</span></span>
    
- <span data-ttu-id="f4131-111">Effectuer des opérations en bloc</span><span class="sxs-lookup"><span data-stu-id="f4131-111">Do bulk operations</span></span>
    
- <span data-ttu-id="f4131-112">Filtrer les données</span><span class="sxs-lookup"><span data-stu-id="f4131-112">Filter data</span></span>
    
- <span data-ttu-id="f4131-113">Imprimer ou enregistrer des données</span><span class="sxs-lookup"><span data-stu-id="f4131-113">Print or save data</span></span>
    
- <span data-ttu-id="f4131-114">Gérer dans les services</span><span class="sxs-lookup"><span data-stu-id="f4131-114">Manage across services</span></span>
    
<span data-ttu-id="f4131-115">N’oubliez pas que PowerShell pour Microsoft 365 est un ensemble de modules pour Windows PowerShell, qui est un environnement de ligne de commande pour les plateformes et les services Windows.</span><span class="sxs-lookup"><span data-stu-id="f4131-115">Keep in mind that PowerShell for Microsoft 365 is a set of modules for Windows PowerShell, which is a command-line environment for Windows-based services and platforms.</span></span> <span data-ttu-id="f4131-116">Cet environnement crée un langage de commande de l’interpréteur de commandes pouvant être étendu à l’aide de modules supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="f4131-116">This environment creates a command-shell language that can be extended with additional modules.</span></span> <span data-ttu-id="f4131-117">Il permet d’exécuter des commandes ou des scripts simples ou complexes.</span><span class="sxs-lookup"><span data-stu-id="f4131-117">It provides a way to execute simple or complex commands or scripts.</span></span> <span data-ttu-id="f4131-118">Par exemple, après avoir installé PowerShell pour les modules Microsoft 365 et vous être connecté à votre abonnement Microsoft 365, vous pouvez exécuter la commande suivante pour répertorier toutes les boîtes aux lettres utilisateur pour Microsoft Exchange Online :</span><span class="sxs-lookup"><span data-stu-id="f4131-118">For example, after you install the PowerShell for Microsoft 365 modules and connect to your Microsoft 365 subscription, you can run the following command to list all the user mailboxes for Microsoft Exchange Online:</span></span>
  
```powershell
Get-Mailbox
```

<span data-ttu-id="f4131-119">Vous pouvez également obtenir la liste des boîtes aux lettres à l’aide du centre d’administration Microsoft 365, mais il n’est pas facile de compter les éléments dans toutes les listes de tous les sites de toutes les applications Web.</span><span class="sxs-lookup"><span data-stu-id="f4131-119">You could also get the list of mailboxes by using the Microsoft 365 admin center but counting the items in all the lists for all the sites for all of your web apps isn't easy.</span></span>
  
<span data-ttu-id="f4131-120">PowerShell pour Microsoft 365 est conçu pour vous aider à gérer Microsoft 365, et non à remplacer le centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f4131-120">PowerShell for Microsoft 365 is designed to help you manage Microsoft 365, not to replace the Microsoft 365 admin center.</span></span> <span data-ttu-id="f4131-121">Les administrateurs doivent pouvoir utiliser PowerShell pour Microsoft 365, car il existe des procédures de configuration qui ne peuvent être réalisées que par le biais de commandes PowerShell pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f4131-121">Admins need to be able to use PowerShell for Microsoft 365 because there are some configuration procedures that can only be done through PowerShell for Microsoft 365 commands.</span></span> <span data-ttu-id="f4131-122">Dans ce cas, vous devez savoir comment :</span><span class="sxs-lookup"><span data-stu-id="f4131-122">For these cases, you need to know how to:</span></span>
  
- <span data-ttu-id="f4131-123">Installez les modules PowerShell pour Microsoft 365 (une seule fois pour chaque ordinateur d’administrateur).</span><span class="sxs-lookup"><span data-stu-id="f4131-123">Install the PowerShell for Microsoft 365 modules (done only one time for each administrator computer).</span></span>
    
- <span data-ttu-id="f4131-124">Connectez-vous à votre abonnement Microsoft 365 (une fois pour chaque session PowerShell).</span><span class="sxs-lookup"><span data-stu-id="f4131-124">Connect to your Microsoft 365 subscription (one time for each PowerShell session).</span></span>
    
- <span data-ttu-id="f4131-125">Recueillez les informations nécessaires pour exécuter les commandes PowerShell requises pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f4131-125">Gather the information needed to run the required PowerShell for Microsoft 365 commands.</span></span>
    
- <span data-ttu-id="f4131-126">Exécutez les commandes PowerShell pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f4131-126">Run PowerShell for Microsoft 365 commands.</span></span>
    
<span data-ttu-id="f4131-127">Une fois que vous avez appris ces compétences de base, vous n’avez pas besoin de répertorier les utilisateurs de votre boîte aux lettres à l’aide de la commande **Get-Mailbox** .</span><span class="sxs-lookup"><span data-stu-id="f4131-127">After you learn these basic skills, you don't have to list your mailbox users by using the **Get-Mailbox** command.</span></span> <span data-ttu-id="f4131-128">Vous ne devez pas non plus comprendre comment créer une commande à l’instar de la commande citée précédemment pour compter tous les éléments de toutes les listes de tous les sites de toutes les applications Web.</span><span class="sxs-lookup"><span data-stu-id="f4131-128">You also don't have to understand how to create a new command like the command cited previously to count all the items in all the lists for all the sites for all of your web apps.</span></span> <span data-ttu-id="f4131-129">Microsoft et la communauté des administrateurs peuvent vous aider à effectuer ces tâches en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="f4131-129">Microsoft and the community of administrators can help you with such tasks as needed.</span></span>
  
## <a name="powershell-for-microsoft-365-can-reveal-information-that-you-cant-see-with-the-microsoft-365-admin-center"></a><span data-ttu-id="f4131-130">PowerShell pour Microsoft 365 peut révéler des informations que vous ne pouvez pas voir avec le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f4131-130">PowerShell for Microsoft 365 can reveal information that you can't see with the Microsoft 365 admin center</span></span>

<span data-ttu-id="f4131-131">Le centre d’administration Microsoft 365 affiche de nombreuses informations utiles.</span><span class="sxs-lookup"><span data-stu-id="f4131-131">The Microsoft 365 admin center displays many useful information.</span></span> <span data-ttu-id="f4131-132">Toutefois, il n’affiche pas toutes les informations que Microsoft 365 stocke sur les utilisateurs, les licences, les boîtes aux lettres et les sites.</span><span class="sxs-lookup"><span data-stu-id="f4131-132">But it doesn't display all the possible information that Microsoft 365 stores about users, licenses, mailboxes, and sites.</span></span> <span data-ttu-id="f4131-133">Voici un exemple pour *les utilisateurs et les groupes* dans le centre d’administration 365 de Microsoft :</span><span class="sxs-lookup"><span data-stu-id="f4131-133">Here's an example for *users and groups* in the Microsoft 365 admin center:</span></span>
  
![Exemple d’affichage des utilisateurs et des groupes dans le centre d’administration 365 de Microsoft.](../media/o365-powershell-users-and-groups.png)
  
<span data-ttu-id="f4131-135">Cet affichage fournit les informations dont vous avez besoin dans de nombreux cas.</span><span class="sxs-lookup"><span data-stu-id="f4131-135">This view provides the information that you need in many cases.</span></span> <span data-ttu-id="f4131-136">Toutefois, il peut arriver que vous ayez besoin de plus d'informations.</span><span class="sxs-lookup"><span data-stu-id="f4131-136">However, there are times when you need more.</span></span> <span data-ttu-id="f4131-137">Par exemple, les licences Microsoft 365 (et les fonctionnalités Microsoft 365 disponibles pour un utilisateur) dépendent en partie de l’emplacement géographique de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f4131-137">For example, Microsoft 365 licensing (and the Microsoft 365 features available to a user) depends in part on the user's geographic location.</span></span> <span data-ttu-id="f4131-138">Les stratégies et les fonctionnalités que vous pouvez étendre à un utilisateur résidant aux États-Unis peuvent ne pas être les mêmes que celles que vous pouvez étendre à un utilisateur en Inde ou en Belgique.</span><span class="sxs-lookup"><span data-stu-id="f4131-138">The policies and features that you can extend to a user who lives in the United States might not be the same as those that you can extend to a user in India or Belgium.</span></span> <span data-ttu-id="f4131-139">Suivez ces étapes dans le centre d’administration 365 de Microsoft pour déterminer l’emplacement géographique d’un utilisateur :</span><span class="sxs-lookup"><span data-stu-id="f4131-139">Follow these steps in the Microsoft 365 admin center to determine a user's geographic location:</span></span>
  
1. <span data-ttu-id="f4131-140">Double-cliquez sur l'élément **Nom d'affichage** de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f4131-140">Double-click the user's **Display Name**.</span></span>
    
2. <span data-ttu-id="f4131-141">Dans le volet d’affichage des propriétés utilisateur, sélectionnez **Détails**.</span><span class="sxs-lookup"><span data-stu-id="f4131-141">In the user properties display pane, select **details**.</span></span>
    
3. <span data-ttu-id="f4131-142">Dans l’affichage des détails, sélectionnez **Détails supplémentaires**.</span><span class="sxs-lookup"><span data-stu-id="f4131-142">In the details display, select **additional details**.</span></span>
    
4. <span data-ttu-id="f4131-143">Faites défiler jusqu’à ce que vous trouviez le **pays ou la région**de titre :</span><span class="sxs-lookup"><span data-stu-id="f4131-143">Scroll until you find the heading **Country or region**:</span></span>
    
     ![Exemple d’informations de région pour un utilisateur dans le centre d’administration Microsoft 365.](../media/o365-powershell-usage-location.png)
  
5. <span data-ttu-id="f4131-145">Écrivez le nom d'affichage et l'emplacement de l'utilisateur sur un morceau de papier, ou copiez-le et collez-le dans le Bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="f4131-145">Write the user's display name and location on a piece of paper, or copy and paste it into Notepad.</span></span>
    
<span data-ttu-id="f4131-146">Vous devez répéter cette procédure pour chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f4131-146">You must repeat this procedure for each user.</span></span> <span data-ttu-id="f4131-147">Si vous avez un grand nombre d’utilisateurs, ce processus peut être fastidieux.</span><span class="sxs-lookup"><span data-stu-id="f4131-147">If you have many users, this process can be tedious.</span></span> <span data-ttu-id="f4131-148">Avec PowerShell pour Microsoft 365, vous pouvez afficher ces informations pour tous vos utilisateurs à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="f4131-148">With PowerShell for Microsoft 365, you can display this information for all of your users by using the following command:</span></span>
  
```powershell
Get-AzureADUser | Select DisplayName, UsageLocation
```


>[!Note]
><span data-ttu-id="f4131-149">PowerShell Core ne prend pas en charge le module Microsoft Azure Active Directory pour les applets de commande et le module Windows PowerShell dont le nom est *MSOL* .</span><span class="sxs-lookup"><span data-stu-id="f4131-149">PowerShell Core doesn't support the Microsoft Azure Active Directory Module for Windows PowerShell module and cmdlets that have *Msol* in their name.</span></span> <span data-ttu-id="f4131-150">Vous devez exécuter ces applets de commande à partir de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f4131-150">You have to run these cmdlets from Windows PowerShell.</span></span>
>

<span data-ttu-id="f4131-151">Voici un exemple des résultats :</span><span class="sxs-lookup"><span data-stu-id="f4131-151">Here's an example of the results:</span></span>
  
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

<span data-ttu-id="f4131-152">L’interprétation de cette commande PowerShell est la suivante : obtenir tous les utilisateurs dans l’abonnement Microsoft 365 actuel (**Get-AzureADUser**), mais afficher uniquement le nom et l’emplacement de chaque utilisateur (**Select DisplayName, UsageLocation**).</span><span class="sxs-lookup"><span data-stu-id="f4131-152">The interpretation of this PowerShell command is: Get all of the users in the current Microsoft 365 subscription (**Get-AzureADUser**), but only display the name and location for each user (**Select DisplayName, UsageLocation**).</span></span>
  
<span data-ttu-id="f4131-153">Étant donné que PowerShell pour Microsoft 365 prend en charge une langue de commande, vous pouvez manipuler les informations obtenues par la commande **Get-AzureADUser** .</span><span class="sxs-lookup"><span data-stu-id="f4131-153">Because PowerShell for Microsoft 365 supports a command-shell language, you can further manipulate the information obtained by the **Get-AzureADUser** command.</span></span> <span data-ttu-id="f4131-154">Par exemple, vous voudrez peut-être trier ces utilisateurs en fonction de leur emplacement, en regroupant tous les utilisateurs brésiliens, tous les utilisateurs des États-Unis, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="f4131-154">For example, maybe you'd like to sort these users by their location, grouping all the Brazilian users together, all the United States users together, and so on.</span></span> <span data-ttu-id="f4131-155">Voici la commande :</span><span class="sxs-lookup"><span data-stu-id="f4131-155">Here's the command:</span></span>
  
```powershell
Get-AzureADUser | Select DisplayName, UsageLocation | Sort UsageLocation, DisplayName
```

<span data-ttu-id="f4131-156">Voici un exemple des résultats :</span><span class="sxs-lookup"><span data-stu-id="f4131-156">Here's an example of the results:</span></span>
  
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

<span data-ttu-id="f4131-157">L’interprétation de cette commande PowerShell est la suivante : obtenir tous les utilisateurs de l’abonnement Microsoft 365 actuel, mais afficher uniquement le nom et l’emplacement de chaque utilisateur et les trier d’abord en fonction de leur emplacement, puis leur nom (**Trier UsageLocation, DisplayName**).</span><span class="sxs-lookup"><span data-stu-id="f4131-157">The interpretation of this PowerShell command is: Get all the users in the current Microsoft 365 subscription, but only display the name and location for each user and sort them first by their location and then their name (**Sort UsageLocation, DisplayName**).</span></span>
  
<span data-ttu-id="f4131-158">Vous pouvez également utiliser un filtrage supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="f4131-158">You can also use additional filtering.</span></span> <span data-ttu-id="f4131-159">Par exemple, si vous voulez uniquement voir les informations relatives aux utilisateurs basés au Brésil, utilisez cette commande :</span><span class="sxs-lookup"><span data-stu-id="f4131-159">For example, if you only want to see information about users based in Brazil, use this command:</span></span>
  
```powershell
Get-AzureADUser | Where {$_.UsageLocation -eq "BR"} | Select DisplayName, UsageLocation 
```

<span data-ttu-id="f4131-160">Voici un exemple des résultats :</span><span class="sxs-lookup"><span data-stu-id="f4131-160">Here's an example of the results:</span></span>
  
```powershell
DisplayName                                           UsageLocation
-----------                                           -------------
David Longmuir                                        BR
Fabrice Canel                                         BR
```

<span data-ttu-id="f4131-161">L’interprétation de cette commande PowerShell est la suivante : obtenir tous les utilisateurs de l’abonnement Microsoft 365 actuel dont l’emplacement est le Brésil (**où {$ \_ . UsageLocation-EQ "BR"}**), puis affichez le nom et l’emplacement de chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f4131-161">The interpretation of this PowerShell command is: Get all the users in the current Microsoft 365 subscription whose location is Brazil (**Where {$\_.UsageLocation -eq "BR"}**) and then display the name and location for each user.</span></span>
  
 <span data-ttu-id="f4131-162">**Remarque sur les grands domaines**</span><span class="sxs-lookup"><span data-stu-id="f4131-162">**A note about large domains**</span></span>
  
<span data-ttu-id="f4131-163">Si vous disposez d’un grand domaine avec des dizaines de milliers d’utilisateurs, essayez quelques-uns des exemples présentés dans cet article peuvent conduire à une limitation.</span><span class="sxs-lookup"><span data-stu-id="f4131-163">If you have a large domain with tens of thousands of users, trying some of the examples we show in this article could lead to throttling.</span></span> <span data-ttu-id="f4131-164">En fonction de facteurs comme la puissance de calcul et la bande passante réseau disponible, il se peut que vous essayiez d’effectuer trop de tâches à la fois.</span><span class="sxs-lookup"><span data-stu-id="f4131-164">Based on factors like computing power and available network bandwidth, you may be trying to do too much at one time.</span></span> <span data-ttu-id="f4131-165">Les grandes organisations peuvent souhaiter fractionner certaines de ces opérations PowerShell en deux commandes.</span><span class="sxs-lookup"><span data-stu-id="f4131-165">Large organizations might want to split some of these PowerShell operations into two commands.</span></span>

<span data-ttu-id="f4131-166">Par exemple, la commande suivante renvoie tous les comptes d’utilisateur et indique le nom et l’emplacement de chacun :</span><span class="sxs-lookup"><span data-stu-id="f4131-166">For example, the following command returns all the user accounts and shows the name and location for each:</span></span>
  
```powershell
Get-AzureADUser | Select DisplayName, UsageLocation
```

<span data-ttu-id="f4131-167">Cela fonctionne bien pour les petits domaines.</span><span class="sxs-lookup"><span data-stu-id="f4131-167">That works great for smaller domains.</span></span> <span data-ttu-id="f4131-168">Toutefois, dans une organisation de grande taille, vous pouvez fractionner cette opération en deux commandes : une pour stocker les informations de compte d’utilisateur dans une variable et une autre pour afficher les informations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="f4131-168">But in a large organization, you might want to split that operation into two commands: one command to store the user account information in a variable and another to display the needed information.</span></span> <span data-ttu-id="f4131-169">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="f4131-169">Here's an example:</span></span>
  
```powershell
$x = Get-AzureADUser
$x | Select DisplayName, UsageLocation
```

<span data-ttu-id="f4131-170">L’interprétation de cet ensemble de commandes PowerShell est la suivante :</span><span class="sxs-lookup"><span data-stu-id="f4131-170">The interpretation of this set of PowerShell commands is:</span></span>
1. <span data-ttu-id="f4131-171">Obtenez tous les utilisateurs dans l’abonnement Microsoft 365 actuel et stockez les informations dans une variable nommée $x (**$x = Get-AzureADUser**).</span><span class="sxs-lookup"><span data-stu-id="f4131-171">Get all the users in the current Microsoft 365 subscription and store the information in a variable named $x (**$x = Get-AzureADUser**).</span></span>
1.  <span data-ttu-id="f4131-172">Affiche le contenu de la variable *$x*, mais inclut uniquement le nom et l’emplacement de chaque utilisateur (**$x | Sélectionnez DisplayName, UsageLocation**).</span><span class="sxs-lookup"><span data-stu-id="f4131-172">Display the contents of the variable *$x*, but only include the name and location for each user (**$x | Select DisplayName, UsageLocation**).</span></span>
  
## <a name="microsoft-365-has-features-that-you-can-only-configure-with-powershell-for-microsoft-365"></a><span data-ttu-id="f4131-173">Microsoft 365 dispose de fonctionnalités que vous pouvez configurer uniquement avec PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f4131-173">Microsoft 365 has features that you can only configure with PowerShell for Microsoft 365</span></span>

<span data-ttu-id="f4131-174">Le centre d’administration Microsoft 365 est destiné à fournir un accès à des tâches d’administration courantes et utiles qui s’appliquent à la plupart des environnements.</span><span class="sxs-lookup"><span data-stu-id="f4131-174">The Microsoft 365 admin center is intended to provide access to common, useful administrative tasks that apply to most environments.</span></span> <span data-ttu-id="f4131-175">En d’autres termes, le centre d’administration 365 de Microsoft a été conçu de sorte que l’administrateur par défaut puisse effectuer les tâches de gestion les plus courantes.</span><span class="sxs-lookup"><span data-stu-id="f4131-175">In other words, the Microsoft 365 admin center was designed so that the typical administrator can carry out the most-common management tasks.</span></span> <span data-ttu-id="f4131-176">Toutefois, certaines tâches ne peuvent pas être effectuées dans le centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="f4131-176">But there are some tasks that can't be done in the admin center.</span></span>
  
<span data-ttu-id="f4131-177">Par exemple, le centre d’administration de Skype entreprise Online offre quelques options pour créer des invitations personnalisées à une réunion :</span><span class="sxs-lookup"><span data-stu-id="f4131-177">For example, the Skype for Business Online admin center provides a few options for creating custom meeting invitations:</span></span>
  
![Exemple d’affichage d’invitations personnalisées à une réunion dans le Centre d’administration de Skype Entreprise Online.](../media/o365-powershell-meeting-invitation.png)
  
<span data-ttu-id="f4131-179">Avec ces paramètres, vous pouvez ajouter une touche de personnalisation et de professionnalisme aux invitations aux réunions.</span><span class="sxs-lookup"><span data-stu-id="f4131-179">With these settings, you can add a touch of personalization and professionalism to meeting invitations.</span></span> <span data-ttu-id="f4131-180">Toutefois, il existe d’autres paramètres de configuration de réunion que la simple création d’invitations aux réunions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="f4131-180">But there's more to meeting-configuration settings than simply creating custom meeting invitations.</span></span> <span data-ttu-id="f4131-181">Par défaut, les réunions autorisent :</span><span class="sxs-lookup"><span data-stu-id="f4131-181">For example, by default, meetings allow:</span></span>
  
- <span data-ttu-id="f4131-182">les utilisateurs anonymes à obtenir une entrée automatique à chaque réunion ;</span><span class="sxs-lookup"><span data-stu-id="f4131-182">Anonymous users to gain automatic entrance to each meeting.</span></span>
    
- <span data-ttu-id="f4131-183">les participants à enregistrer la réunion ;</span><span class="sxs-lookup"><span data-stu-id="f4131-183">Attendees to record the meeting.</span></span>
    
- <span data-ttu-id="f4131-184">tous les utilisateurs de votre organisation à être désignés en tant que présentateurs lorsqu’ils rejoignent la réunion.</span><span class="sxs-lookup"><span data-stu-id="f4131-184">All users from your organization to be designated as presenters when they join the meeting.</span></span>
    
<span data-ttu-id="f4131-185">Ces paramètres ne sont pas disponibles dans le centre d’administration de Skype entreprise online.</span><span class="sxs-lookup"><span data-stu-id="f4131-185">These settings aren't available from the Skype for Business Online admin center.</span></span> <span data-ttu-id="f4131-186">Vous pouvez les contrôler à partir de PowerShell pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f4131-186">You can control them from PowerShell for Microsoft 365.</span></span> <span data-ttu-id="f4131-187">Voici une commande qui désactive ces trois paramètres :</span><span class="sxs-lookup"><span data-stu-id="f4131-187">Here's a command that disables these three settings:</span></span>
  
```powershell
Set-CsMeetingConfiguration -AdmitAnonymousUsersByDefault $False -AllowConferenceRecording $False -DesignateAsPresenter "None"
```

> [!NOTE]
> <span data-ttu-id="f4131-188">Pour exécuter cette commande, vous devez installer le [module Skype entreprise Online PowerShell ](https://www.microsoft.com/download/details.aspx?id=39366).</span><span class="sxs-lookup"><span data-stu-id="f4131-188">To run this command, you must install the [Skype for Business Online PowerShell Module ](https://www.microsoft.com/download/details.aspx?id=39366).</span></span>
  
<span data-ttu-id="f4131-189">L’interprétation de cette commande PowerShell est la suivante :</span><span class="sxs-lookup"><span data-stu-id="f4131-189">The interpretation of this PowerShell command is:</span></span>
 
1. <span data-ttu-id="f4131-190">Dans les paramètres des nouvelles réunions Skype entreprise Online (**Set-CsMeetingConfiguration**), désactivez la fonctionnalité permettant aux utilisateurs anonymes d’accéder automatiquement aux réunions (**-AdmitAnonymousUsersByDefault $false**).</span><span class="sxs-lookup"><span data-stu-id="f4131-190">In the settings for new Skype for Business Online meetings (**Set-CsMeetingConfiguration**), disable allowing anonymous users to gain automatic entrance to meetings (**-AdmitAnonymousUsersByDefault $False**).</span></span>
2.  <span data-ttu-id="f4131-191">Désactiver la possibilité pour les participants d’enregistrer des réunions (**-AllowConferenceRecording $false**).</span><span class="sxs-lookup"><span data-stu-id="f4131-191">Disable the ability for attendees to record meetings (**-AllowConferenceRecording $False**).</span></span>
3. <span data-ttu-id="f4131-192">Ne désignez pas tous les utilisateurs de votre organisation en tant que présentateurs (**-DesignateAsPresenter "none"**).</span><span class="sxs-lookup"><span data-stu-id="f4131-192">Don't designate all users from your organization as presenters (**-DesignateAsPresenter "None"**).</span></span>
  
<span data-ttu-id="f4131-193">Pour restaurer ces paramètres par défaut (activer les options), exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="f4131-193">To restore these default settings (enable the options), run this command:</span></span>
  
```powershell
Set-CsMeetingConfiguration -AdmitAnonymousUsersByDefault $True -AllowConferenceRecording $True -DesignateAsPresenter "Company"
```

<span data-ttu-id="f4131-194">Il existe également d’autres scénarios similaires, c’est pourquoi les administrateurs doivent savoir exécuter les commandes PowerShell pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f4131-194">There are other similar scenarios as well, which is why administrators should know how to run PowerShell for Microsoft 365 commands.</span></span>
  
## <a name="powershell-for-microsoft-365-is-great-for-bulk-operations"></a><span data-ttu-id="f4131-195">PowerShell pour Microsoft 365 est idéal pour les opérations en bloc</span><span class="sxs-lookup"><span data-stu-id="f4131-195">PowerShell for Microsoft 365 is great for bulk operations</span></span>

<span data-ttu-id="f4131-196">Les interfaces visuelles comme le centre d’administration Microsoft 365 sont particulièrement utiles lorsque vous avez une seule opération à effectuer.</span><span class="sxs-lookup"><span data-stu-id="f4131-196">Visual interfaces like the Microsoft 365 admin center are most valuable when you have a single operation to do.</span></span> <span data-ttu-id="f4131-197">Par exemple, si vous avez besoin de désactiver un compte d’utilisateur, vous pouvez utiliser le centre d’administration pour localiser et désactiver rapidement une case à cocher.</span><span class="sxs-lookup"><span data-stu-id="f4131-197">For example, if you need to disable one user account, you can use the admin center to quickly locate and clear a checkbox.</span></span> <span data-ttu-id="f4131-198">Cela peut être plus simple que d’effectuer une opération similaire dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f4131-198">This may be easier than performing a similar operation in PowerShell.</span></span>
  
<span data-ttu-id="f4131-199">Toutefois, si vous devez modifier de nombreux éléments ou des éléments sélectionnés dans un grand nombre d’autres choses, le centre d’administration Microsoft 365 peut ne pas être le meilleur outil.</span><span class="sxs-lookup"><span data-stu-id="f4131-199">But if you have to change many things or some selected things within a large set of other things, the Microsoft 365 admin center might not be the best tool.</span></span> <span data-ttu-id="f4131-200">Par exemple, imaginons que vous devez modifier le préfixe sur des milliers de numéros de téléphone ou supprimer l’utilisateur spécifique *Ken Myer* de tous vos sites SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="f4131-200">For example, say you have to change the prefix on thousands of phone numbers or remove the specific user *Ken Myer* from all your SharePoint Online sites.</span></span> <span data-ttu-id="f4131-201">Comment pouvez-vous effectuer cette opération dans le centre d’administration 365 de Microsoft ?</span><span class="sxs-lookup"><span data-stu-id="f4131-201">How would you do that in the Microsoft 365 admin center?</span></span>
  
<span data-ttu-id="f4131-202">Pour le dernier exemple, imaginons que vous avez plusieurs centaines de sites SharePoint Online et que vous ne sachiez pas à qui elle appartient.</span><span class="sxs-lookup"><span data-stu-id="f4131-202">For the last example, say you have several hundred SharePoint Online sites, and you don't know which ones Ken Meyer is a member of.</span></span> <span data-ttu-id="f4131-203">Vous devez commencer par le centre d’administration 365 de Microsoft, puis effectuer cette procédure pour chaque site :</span><span class="sxs-lookup"><span data-stu-id="f4131-203">You would have to start at the Microsoft 365 admin center and then perform this procedure for each site:</span></span>
  
1. <span data-ttu-id="f4131-204">Sélectionnez l' **URL** du site.</span><span class="sxs-lookup"><span data-stu-id="f4131-204">Select the **URL** of the site.</span></span>
    
2. <span data-ttu-id="f4131-205">Dans la zone Propriétés de la **collection de sites** , sélectionnez le lien adresse du **site Web** pour ouvrir le site.</span><span class="sxs-lookup"><span data-stu-id="f4131-205">In the **site collection properties** box, select the **Web Site Address** link to open the site.</span></span>
    
3. <span data-ttu-id="f4131-206">Sur le site, sélectionnez **partager**.</span><span class="sxs-lookup"><span data-stu-id="f4131-206">On the site, select **Share**.</span></span>
    
4. <span data-ttu-id="f4131-207">Dans la boîte de dialogue **partager** , sélectionnez le lien qui affiche tous les utilisateurs disposant d’autorisations sur le site :</span><span class="sxs-lookup"><span data-stu-id="f4131-207">In the **Share** dialog box, select the link that shows all the users who have permissions to the site:</span></span>
    
     ![Exemple d’affichage des membres d’un site SharePoint Online dans le Centre d’administration SharePoint Online.](../media/o365-powershell-view-permissions.png)
  
5. <span data-ttu-id="f4131-209">Dans la boîte de dialogue **partagé avec** , sélectionnez **avancé**.</span><span class="sxs-lookup"><span data-stu-id="f4131-209">In the **Shared With** dialog box, select **Advanced**.</span></span>
    
6. <span data-ttu-id="f4131-210">Faites défiler vers le bas la liste des utilisateurs, recherchez et sélectionnez Ken Myer (en supposant qu’il dispose d’autorisations sur le site), puis sélectionnez **Supprimer les autorisations des utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="f4131-210">Scroll down the list of users, find and select Ken Myer (assuming he has permissions to the site), and then select **Remove User Permissions**.</span></span>
    
<span data-ttu-id="f4131-211">Cela prendrait *beaucoup* de temps pour plusieurs centaines de sites.</span><span class="sxs-lookup"><span data-stu-id="f4131-211">This would take a *long* time for several hundred sites.</span></span>
  
<span data-ttu-id="f4131-212">L’alternative consiste à exécuter la commande suivante dans PowerShell pour Microsoft 365 afin de supprimer Ken Myer de tous vos sites :</span><span class="sxs-lookup"><span data-stu-id="f4131-212">The alternative is to run the following command in PowerShell for Microsoft 365 to remove Ken Myer from all your sites:</span></span>
  
```powershell
Get-SPOSite | ForEach {Remove-SPOUser -Site $_.Url -LoginName "kenmyer@litwareinc.com"}
```

> [!NOTE]
> <span data-ttu-id="f4131-213">Cette commande exige que vous installiez le [module SharePoint Online PowerShell](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps).</span><span class="sxs-lookup"><span data-stu-id="f4131-213">This command requires that you install the [SharePoint Online PowerShell module](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps).</span></span> 
  
<span data-ttu-id="f4131-214">L’interprétation de cette commande PowerShell est la suivante : obtenir tous les sites SharePoint dans l’abonnement Microsoft 365 actuel (**Get-SPOSite**) et pour chaque site supprimez Ken Meyer de la liste des utilisateurs qui peuvent y accéder (**foreach {Remove-épouser-site $ \_ . URL-LoginName "kenmyer \@ litwareinc.com"}**).</span><span class="sxs-lookup"><span data-stu-id="f4131-214">The interpretation of this PowerShell command is: Get all of the SharePoint sites in the current Microsoft 365 subscription (**Get-SPOSite**) and for each site remove Ken Meyer from the list of users who can access it (**ForEach {Remove-SPOUser -Site $\_.Url -LoginName "kenmyer\@litwareinc.com"}**).</span></span>
  
<span data-ttu-id="f4131-215">Nous disons que Microsoft 365 supprime Ken Meyer de chaque site, y compris ceux auxquels il n’a pas accès.</span><span class="sxs-lookup"><span data-stu-id="f4131-215">We tell Microsoft 365 to remove Ken Meyer from every site, including those that he doesn't have access to.</span></span> <span data-ttu-id="f4131-216">Par conséquent, les résultats affichent des erreurs pour les sites auxquels il n’a pas accès.</span><span class="sxs-lookup"><span data-stu-id="f4131-216">So the results will show errors for those sites that he doesn't have access to.</span></span> <span data-ttu-id="f4131-217">Nous pouvons utiliser une condition supplémentaire sur cette commande pour supprimer Ken Meyer uniquement des sites qui l’ont sur leur liste de connexion.</span><span class="sxs-lookup"><span data-stu-id="f4131-217">We can use an additional condition on this command to remove Ken Meyer only from the sites that have him on their login list.</span></span> <span data-ttu-id="f4131-218">Toutefois, les erreurs renvoyées n’ont aucun effet sur les sites eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="f4131-218">But the errors that are returned cause no harm to the sites themselves.</span></span> <span data-ttu-id="f4131-219">L’exécution de cette commande peut prendre quelques minutes sur des centaines de sites, et non sur des heures de travail par le biais du centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f4131-219">This command might take a few minutes to run against hundreds of sites, rather than hours of working through the Microsoft 365 admin center.</span></span>
  
<span data-ttu-id="f4131-220">Voici un autre exemple d’opération en bloc.</span><span class="sxs-lookup"><span data-stu-id="f4131-220">Here's another bulk operation example.</span></span> <span data-ttu-id="f4131-221">Utilisez cette commande pour ajouter *Bonnie Kearney*, un nouvel administrateur SharePoint, à tous les sites de l’Organisation :</span><span class="sxs-lookup"><span data-stu-id="f4131-221">Use this command to add *Bonnie Kearney*, a new SharePoint administrator, to all sites in the organization:</span></span>
  
```powershell
Get-SPOSite | ForEach {Add-SPOUser -Site $_.Url -LoginName "bkearney@litwareinc.com" -Group "Members"}
```

<span data-ttu-id="f4131-222">L’interprétation de cette commande PowerShell est la suivante : obtenir tous les sites SharePoint de l’abonnement Microsoft 365 actuel et pour chaque site autoriser l’accès à Bonnie Kearney en ajoutant son nom de connexion au groupe membres du site (**foreach {Add-époux-site $ \_ . URL-LoginName "bkearney \@ litwareinc.com"-Group "members"}**).</span><span class="sxs-lookup"><span data-stu-id="f4131-222">The interpretation of this PowerShell command is: Get all the SharePoint sites in the current Microsoft 365 subscription and for each site allow Bonnie Kearney access by adding her login name to the Members group of the site (**ForEach {Add-SPOUser -Site $\_.Url -LoginName "bkearney\@litwareinc.com" -Group "Members"}**).</span></span>
  
## <a name="powershell-for-microsoft-365-is-great-at-filtering-data"></a><span data-ttu-id="f4131-223">PowerShell pour Microsoft 365 est idéal pour le filtrage des données</span><span class="sxs-lookup"><span data-stu-id="f4131-223">PowerShell for Microsoft 365 is great at filtering data</span></span>

<span data-ttu-id="f4131-224">Le centre d’administration 365 de Microsoft offre plusieurs méthodes pour filtrer vos données afin de localiser facilement un sous-ensemble ciblé d’informations.</span><span class="sxs-lookup"><span data-stu-id="f4131-224">The Microsoft 365 admin center provides several ways to filter your data to easily locate a targeted subset of information.</span></span> <span data-ttu-id="f4131-225">Par exemple, Exchange facilite le filtrage sur pratiquement toutes les propriétés de la boîte aux lettres d'un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f4131-225">For example, Exchange makes it easy to filter on practically any property of a user mailbox.</span></span> <span data-ttu-id="f4131-226">Par exemple, voici la liste des boîtes aux lettres de tous les utilisateurs vivant dans la ville de Bloomington :</span><span class="sxs-lookup"><span data-stu-id="f4131-226">For example, here's the list of mailboxes for all the users who live in the city of Bloomington:</span></span>
  
![Exemple de recherche avancée dans le centre d’administration Microsoft 365 pour obtenir la liste des boîtes aux lettres de tous les utilisateurs vivant dans la ville de Bloomington.](../media/o365-powershell-advanced-search.png)
  
<span data-ttu-id="f4131-228">Le Centre d'administration Exchange vous permet également de combiner des critères de filtre.</span><span class="sxs-lookup"><span data-stu-id="f4131-228">The Exchange Admin center also lets you combine filter criteria.</span></span> <span data-ttu-id="f4131-229">Par exemple, vous pouvez rechercher les boîtes aux lettres de toutes les personnes vivant dans Bloomington et travailler dans le service financier.</span><span class="sxs-lookup"><span data-stu-id="f4131-229">For example, you can find the mailboxes for all the people who live in Bloomington and work in the Finance department.</span></span>
  
<span data-ttu-id="f4131-230">Toutefois, il existe des limitations à ce que vous pouvez faire dans le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="f4131-230">But there are limitations to what you can do in the Exchange Admin center.</span></span> <span data-ttu-id="f4131-231">Par exemple, vous ne pouviez pas trouver facilement les boîtes aux lettres de personnes vivant dans Bloomington *ou* San Diego, ou les boîtes aux lettres de toutes les personnes qui ne vivent pas dans Bloomington.</span><span class="sxs-lookup"><span data-stu-id="f4131-231">For example, you couldn't as easily find the mailboxes of people who live in Bloomington *or* San Diego, or the mailboxes for all people who don't live in Bloomington.</span></span>
  
<span data-ttu-id="f4131-232">Vous pouvez utiliser la commande PowerShell suivante pour Microsoft 365 pour obtenir la liste des boîtes aux lettres de toutes les personnes vivant dans Bloomington ou San Diego :</span><span class="sxs-lookup"><span data-stu-id="f4131-232">You can use the following PowerShell for Microsoft 365 command to get a list of mailboxes for all the people who live in Bloomington or San Diego:</span></span>
  
```powershell
Get-User | Where {$_.RecipientTypeDetails -eq "UserMailbox" -and ($_.City -eq "San Diego" -or $_.City -eq "Bloomington")} | Select DisplayName, City
```

<span data-ttu-id="f4131-233">Voici un exemple des résultats :</span><span class="sxs-lookup"><span data-stu-id="f4131-233">Here's an example of the results:</span></span>
  
```powershell
DisplayName                              City
-----------                              ----
Alex Darrow                              San Diego
Bonnie Kearney                           San Diego
Julian Isla                              Bloomington
Rob Young                                Bloomington
```

<span data-ttu-id="f4131-234">L’interprétation de cette commande PowerShell est la suivante : obtenir tous les utilisateurs de l’abonnement Microsoft 365 actuel disposant d’une boîte aux lettres dans la ville de San Diego ou Bloomington (**où {$ \_ . RecipientTypeDetails-EQ "UserMailbox"-et ($ \_ . City-EQ "San Diego"-ou $ \_ . City-EQ "Bloomington")}**), puis affichez le nom et la ville de chacune d’entre elles (**Sélectionnez DisplayName, City**).</span><span class="sxs-lookup"><span data-stu-id="f4131-234">The interpretation of this PowerShell command is: Get all the users in the current Microsoft 365 subscription who have a mailbox in the city of San Diego or Bloomington (**Where {$\_.RecipientTypeDetails -eq "UserMailbox" -and ($\_.City -eq "San Diego" -or $\_.City -eq "Bloomington")}**), and then display the name and city for each (**Select DisplayName, City**).</span></span>
  
<span data-ttu-id="f4131-235">Et voici la commande permettant de répertorier toutes les boîtes aux lettres pour les personnes vivant à l’exception de Bloomington :</span><span class="sxs-lookup"><span data-stu-id="f4131-235">And here's the command to list all the mailboxes for people who live anywhere except Bloomington:</span></span>
  
```powershell
Get-User | Where {$_.RecipientTypeDetails -eq "UserMailbox" -and $_.City -ne "Bloomington"} | Select DisplayName, City
```

<span data-ttu-id="f4131-236">Voici un exemple des résultats :</span><span class="sxs-lookup"><span data-stu-id="f4131-236">Here's an example of the results:</span></span>
  
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

<span data-ttu-id="f4131-237">L’interprétation de cette commande PowerShell est la suivante : obtenir tous les utilisateurs de l’abonnement Microsoft 365 actuel disposant d’une boîte aux lettres qui ne se trouve pas dans la ville de Bloomington (**où {$ \_ . RecipientTypeDetails-EQ "UserMailbox"-et $ \_ . City-ne "Bloomington"}**), puis affichez le nom et la ville de chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="f4131-237">The interpretation of this PowerShell command is: Get all the users in the current Microsoft 365 subscription who have a mailbox not located in the city of Bloomington (**Where {$\_.RecipientTypeDetails -eq "UserMailbox" -and $\_.City -ne "Bloomington"}**), and then display the name and city for each.</span></span>
  
### <a name="use-wildcards"></a><span data-ttu-id="f4131-238">Utiliser des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="f4131-238">Use wildcards</span></span>

<span data-ttu-id="f4131-239">Vous pouvez également utiliser des caractères génériques dans vos filtres PowerShell pour faire correspondre une partie d’un nom.</span><span class="sxs-lookup"><span data-stu-id="f4131-239">You can also use wildcard characters in your PowerShell filters to match part of a name.</span></span> <span data-ttu-id="f4131-240">Par exemple, supposons que vous recherchez un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f4131-240">For example, suppose you're looking for a user account.</span></span> <span data-ttu-id="f4131-241">Tout ce dont vous pouvez vous souvenir est que le nom de famille de l’utilisateur était *Anderson* ou peut-être *sur Henderson* ou *Jorgenson*.</span><span class="sxs-lookup"><span data-stu-id="f4131-241">All you can remember is that the user's last name was *Anderson* or maybe *Henderson* or *Jorgenson*.</span></span>
  
<span data-ttu-id="f4131-242">Vous pouvez identifier cet utilisateur dans le centre d’administration 365 de Microsoft à l’aide de l’outil de recherche et en effectuant trois recherches différentes :</span><span class="sxs-lookup"><span data-stu-id="f4131-242">You could track down that user in the Microsoft 365 admin center by using the search tool and carrying out three different searches:</span></span>
  
- <span data-ttu-id="f4131-243">Une sur  *Anderson*</span><span class="sxs-lookup"><span data-stu-id="f4131-243">One for  *Anderson*</span></span> 
    
- <span data-ttu-id="f4131-244">Une sur  *Henderson*</span><span class="sxs-lookup"><span data-stu-id="f4131-244">One for  *Henderson*</span></span> 
    
- <span data-ttu-id="f4131-245">Une sur  *Jorgenson*</span><span class="sxs-lookup"><span data-stu-id="f4131-245">One for  *Jorgenson*</span></span> 
    
<span data-ttu-id="f4131-246">Étant donné que ces trois noms se terminent par « fils », vous pouvez indiquer à PowerShell d’afficher tous les utilisateurs dont le nom se termine par « fils ».</span><span class="sxs-lookup"><span data-stu-id="f4131-246">Because all three of these names end in "son", you can tell PowerShell to display all the users whose name ends in "son".</span></span> <span data-ttu-id="f4131-247">Voici la commande :</span><span class="sxs-lookup"><span data-stu-id="f4131-247">Here's the command:</span></span>
  
```powershell
Get-User -Filter '{LastName -like "*son"}'
```

<span data-ttu-id="f4131-248">L’interprétation de cette commande PowerShell est la suivante : obtenir tous les utilisateurs de l’abonnement Microsoft 365 actuel, mais utiliser un filtre qui répertorie uniquement les utilisateurs dont le nom de famille se termine par « fils » (**-Filter « {LastName-like " \* fils »}»**).</span><span class="sxs-lookup"><span data-stu-id="f4131-248">The interpretation of this PowerShell command is: Get all the users in the current Microsoft 365 subscription, but use a filter that only lists the users whose last names end in "son" (**-Filter '{LastName -like "\*son"}'**).</span></span> <span data-ttu-id="f4131-249">\*Représente un jeu de caractères quelconque, c’est-à-dire des lettres dans le nom de famille de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f4131-249">The \* stands for any set of characters, which are letters in the user's last name.</span></span>
  
## <a name="powershell-for-microsoft-365-makes-it-easy-to-print-or-save-data"></a><span data-ttu-id="f4131-250">PowerShell pour Microsoft 365 facilite l’impression ou l’enregistrement des données</span><span class="sxs-lookup"><span data-stu-id="f4131-250">PowerShell for Microsoft 365 makes it easy to print or save data</span></span>

<span data-ttu-id="f4131-251">Le centre d’administration Microsoft 365 vous permet d’afficher des listes de données.</span><span class="sxs-lookup"><span data-stu-id="f4131-251">The Microsoft 365 admin center lets you view lists of data.</span></span> <span data-ttu-id="f4131-252">Voici un exemple du centre d’administration de Skype entreprise Online affichant une liste d’utilisateurs qui ont été activés pour Skype entreprise Online :</span><span class="sxs-lookup"><span data-stu-id="f4131-252">Here's an example of the Skype for Business Online admin center displaying a list of users who have been enabled for Skype for Business Online:</span></span>
  
![Exemple de liste d’utilisateurs ayant été activés pour Skype Entreprise Online, affichée dans le Centre d’administration de Skype Entreprise Online.](../media/o365-powershell-lync-users.png)
  
<span data-ttu-id="f4131-254">Pour enregistrer ces informations dans un fichier, vous devez le coller dans un document ou une feuille de calcul Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="f4131-254">To save that information to a file, you must paste it into a document or Microsoft Excel worksheet.</span></span> <span data-ttu-id="f4131-255">Les deux cas peuvent nécessiter une mise en forme supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="f4131-255">Either case might require additional formatting.</span></span> <span data-ttu-id="f4131-256">En outre, le centre d’administration Microsoft 365 ne permet pas d’imprimer directement la liste affichée.</span><span class="sxs-lookup"><span data-stu-id="f4131-256">Additionally, the Microsoft 365 admin center doesn't provide a way to directly print the displayed list.</span></span>
  
<span data-ttu-id="f4131-257">Heureusement, vous pouvez utiliser PowerShell pour non seulement afficher la liste, mais aussi l’enregistrer dans un fichier facile à importer dans Excel.</span><span class="sxs-lookup"><span data-stu-id="f4131-257">Fortunately, you can use PowerShell to not only display the list but to save it to a file that can be easily imported into Excel.</span></span> <span data-ttu-id="f4131-258">Voici un exemple de commande permettant d’enregistrer des données utilisateur Skype entreprise Online dans un fichier de valeurs séparées par des virgules (CSV), qui peut ensuite être importé facilement sous forme de tableau dans une feuille de calcul Excel :</span><span class="sxs-lookup"><span data-stu-id="f4131-258">Here's an example command to save Skype for Business Online user data to a comma-separated values (CSV) file, which can then be easily imported as a table in an Excel worksheet:</span></span>
  
```powershell
Get-CsOnlineUser | Select DisplayName, UserPrincipalName, UsageLocation | Export-Csv -Path "C:\Logs\SfBUsers.csv" -NoTypeInformation
```

<span data-ttu-id="f4131-259">Voici un exemple des résultats :</span><span class="sxs-lookup"><span data-stu-id="f4131-259">Here's an example of the results:</span></span>
  
![Exemple de tableau importé dans une feuille de calcul Excel pour les données utilisateur de Skype entreprise Online qui a été enregistré dans un fichier de valeurs séparées par des virgules.](../media/o365-powershell-data-in-excel.png)
  
<span data-ttu-id="f4131-261">L’interprétation de cette commande PowerShell est la suivante : obtenir tous les utilisateurs de Skype entreprise Online dans l’abonnement Microsoft 365 actuel (**Get-CsOnlineUser**); obtenez uniquement le nom d’utilisateur, l’UPN et l’emplacement (**Sélectionnez DisplayName, userPrincipalName, UsageLocation**); Enregistrez ensuite ces informations dans un fichier CSV nommé C : \\ logs \\SfBUsers.csv (**Export-CSV-path "C : \\ logs \\SfBUsers.csv"-NoTypeInformation**).</span><span class="sxs-lookup"><span data-stu-id="f4131-261">The interpretation of this PowerShell command is: Get all the Skype for Business Online users in the current Microsoft 365 subscription (**Get-CsOnlineUser**); obtain only the user name, UPN, and location (**Select DisplayName, UserPrincipalName, UsageLocation**); and then save that information in a CSV file named C:\\Logs\\SfBUsers.csv (**Export-Csv -Path "C:\\Logs\\SfBUsers.csv" -NoTypeInformation**).</span></span>
  
<span data-ttu-id="f4131-262">Vous pouvez également utiliser les options pour enregistrer cette liste sous la forme d’un fichier XML ou d’une page HTML.</span><span class="sxs-lookup"><span data-stu-id="f4131-262">You can also use options to save this list as an XML file or an HTML page.</span></span> <span data-ttu-id="f4131-263">En fait, avec des commandes PowerShell supplémentaires, vous pouviez l’enregistrer directement sous forme de fichier Excel, avec n’importe quelle mise en forme personnalisée souhaitée.</span><span class="sxs-lookup"><span data-stu-id="f4131-263">In fact, with additional PowerShell commands, you could save it directly as an Excel file, with any custom formatting you want.</span></span>
  
<span data-ttu-id="f4131-264">Vous pouvez également envoyer la sortie d’une commande PowerShell qui affiche une liste directement sur l’imprimante par défaut dans Windows.</span><span class="sxs-lookup"><span data-stu-id="f4131-264">You can also send the output of a PowerShell command that displays a list directly to the default printer in Windows.</span></span> <span data-ttu-id="f4131-265">Voici un exemple de commande :</span><span class="sxs-lookup"><span data-stu-id="f4131-265">Here's an example command:</span></span>
  
```powershell
Get-CsOnlineUser | Select DisplayName, UserPrincipalName, UsageLocation | Out-Printer
```

<span data-ttu-id="f4131-266">Le document imprimé aura l'apparence suivante :</span><span class="sxs-lookup"><span data-stu-id="f4131-266">Here's what your printed document will look like:</span></span>
  
![Exemple de document imprimé correspondant à la sortie d’une commande PowerShell envoyée directement à l’imprimante par défaut dans Windows.](../media/o365-powershell-printed-data.png)
  
<span data-ttu-id="f4131-268">L’interprétation de cette commande PowerShell est la suivante : obtenir tous les utilisateurs de Skype entreprise Online dans l’abonnement Microsoft 365 actuel ; obtenir uniquement le nom d’utilisateur, l’UPN et l’emplacement ; puis envoyez ces informations à l’imprimante Windows par défaut (**out-Printer**).</span><span class="sxs-lookup"><span data-stu-id="f4131-268">The interpretation of this PowerShell command is: Get all the Skype for Business Online users in the current Microsoft 365 subscription; obtain only the user name, UPN, and location; and then send that information to the default Windows printer (**Out-Printer**).</span></span>
  
<span data-ttu-id="f4131-269">Le document imprimé a la même mise en forme que l’affichage dans la fenêtre de commande PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f4131-269">The printed document has the same simple formatting as the display in the PowerShell command window.</span></span> <span data-ttu-id="f4131-270">Pour obtenir une copie papier, ajoutez simplement **| Out-Printer** à la fin de la commande.</span><span class="sxs-lookup"><span data-stu-id="f4131-270">To get a hard copy, just add **| Out-Printer** to the end of the command.</span></span>
  
## <a name="powershell-for-microsoft-365-lets-you-manage-across-server-products"></a><span data-ttu-id="f4131-271">PowerShell pour Microsoft 365 vous permet de gérer tous les produits serveur</span><span class="sxs-lookup"><span data-stu-id="f4131-271">PowerShell for Microsoft 365 lets you manage across server products</span></span>

<span data-ttu-id="f4131-272">Les composants qui composent Microsoft 365 sont conçus pour fonctionner ensemble.</span><span class="sxs-lookup"><span data-stu-id="f4131-272">The components that make up Microsoft 365 are designed to work together.</span></span> <span data-ttu-id="f4131-273">Par exemple, supposons que vous ajoutez un nouvel utilisateur à Microsoft 365 et que vous spécifiez des informations telles que le service et le numéro de téléphone de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f4131-273">For example, suppose you add a new user to Microsoft 365, and you specify such information as the user's department and phone number.</span></span> <span data-ttu-id="f4131-274">Ces informations seront disponibles si vous accédez aux informations de l’utilisateur dans l’un des services Microsoft 365 : Skype entreprise Online, Exchange ou SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f4131-274">That information will then be available if you access the user's information in any of the Microsoft 365 services: Skype for Business Online, Exchange, or SharePoint.</span></span>
  
<span data-ttu-id="f4131-275">Toutefois, ceci concerne les informations communes qui couvrent une suite de produits.</span><span class="sxs-lookup"><span data-stu-id="f4131-275">But that's for common information that spans the suite of products.</span></span> <span data-ttu-id="f4131-276">Les informations propres au produit, telles que les informations sur la boîte aux lettres Exchange d’un utilisateur, ne sont généralement pas disponibles dans la suite.</span><span class="sxs-lookup"><span data-stu-id="f4131-276">Product-specific information, such as information about a user's Exchange mailbox, isn't typically available across the suite.</span></span> <span data-ttu-id="f4131-277">Par exemple, les informations indiquant si la boîte aux lettres d’un utilisateur est activée ou non sont disponibles uniquement dans le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="f4131-277">For example, information about whether a user's mailbox is enabled or not is available only in the Exchange admin center.</span></span>
  
<span data-ttu-id="f4131-278">Supposons que vous souhaitiez établir un rapport qui présente les informations suivantes pour tous les utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="f4131-278">Suppose you'd like to make a report that shows the following information for all your users:</span></span>
  
- <span data-ttu-id="f4131-279">Nom complet de l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="f4131-279">The user's display name</span></span>
    
- <span data-ttu-id="f4131-280">Si l’utilisateur est titulaire d’une licence pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f4131-280">Whether the user is licensed for Microsoft 365</span></span>
    
- <span data-ttu-id="f4131-281">Si la boîte aux lettres Exchange de l'utilisateur a été activée</span><span class="sxs-lookup"><span data-stu-id="f4131-281">Whether the user's Exchange mailbox has been enabled</span></span>
    
- <span data-ttu-id="f4131-282">Si l'utilisateur est activé pour Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="f4131-282">Whether the user is enabled for Skype for Business Online</span></span>
    
<span data-ttu-id="f4131-283">Vous ne pouvez pas facilement produire un tel rapport dans le centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f4131-283">You can't easily produce such a report in the Microsoft 365 admin center.</span></span> <span data-ttu-id="f4131-284">Au lieu de cela, vous devez créer un document distinct pour stocker les informations, telles qu’une feuille de calcul Excel.</span><span class="sxs-lookup"><span data-stu-id="f4131-284">Instead, you would have to create a separate document to store the information, such as an Excel worksheet.</span></span> <span data-ttu-id="f4131-285">Ensuite, obtenez tous les noms d’utilisateur et les informations de licence à partir du centre d’administration Microsoft 365, obtenez des informations de boîte aux lettres à partir du centre d’administration Exchange, obtenez des informations Skype entreprise Online à partir du centre d’administration de Skype entreprise Online, puis Combinez ces informations.</span><span class="sxs-lookup"><span data-stu-id="f4131-285">Then, get all the user names and licensing information from the Microsoft 365 admin center, get mailbox information from the Exchange Admin center, get Skype for Business Online information from the Skype for Business Online Admin center, and then combine that information.</span></span>
  
<span data-ttu-id="f4131-286">L’alternative consiste à utiliser un script PowerShell pour compiler le rapport pour vous.</span><span class="sxs-lookup"><span data-stu-id="f4131-286">The alternative is to use a PowerShell script to compile the report for you.</span></span>
  
<span data-ttu-id="f4131-287">L’exemple de script suivant est plus compliqué que les commandes que vous avez vues dans cet article.</span><span class="sxs-lookup"><span data-stu-id="f4131-287">The following example script is more complicated than the commands you've seen so far in this article.</span></span> <span data-ttu-id="f4131-288">Toutefois, il illustre la possibilité d’utiliser PowerShell pour créer des vues d’informations difficiles à obtenir autrement.</span><span class="sxs-lookup"><span data-stu-id="f4131-288">But, it shows the potential of using PowerShell to create information views that are difficult to get otherwise.</span></span> <span data-ttu-id="f4131-289">Voici le script à compiler et afficher la liste dont vous avez besoin :</span><span class="sxs-lookup"><span data-stu-id="f4131-289">Here's the script to compile and display the list you need:</span></span>
  
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

<span data-ttu-id="f4131-290">Voici un exemple des résultats :</span><span class="sxs-lookup"><span data-stu-id="f4131-290">Here's an example of the results:</span></span>
  
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

<span data-ttu-id="f4131-291">L’interprétation de ce script PowerShell est la suivante :</span><span class="sxs-lookup"><span data-stu-id="f4131-291">The interpretation of this PowerShell script is:</span></span>  

1. <span data-ttu-id="f4131-292">Obtenir tous les utilisateurs dans l’abonnement Microsoft 365 actuel et stocker les informations dans une variable nommée *$x* (**$x = Get-AzureADUser**).</span><span class="sxs-lookup"><span data-stu-id="f4131-292">Get all the users in the current Microsoft 365 subscription and store the information in a variable that's named *$x* (**$x = Get-AzureADUser**).</span></span>
1. <span data-ttu-id="f4131-293">Démarrez une boucle qui s’exécute sur tous les utilisateurs de la variable $x (**foreach ($i dans $x)**).</span><span class="sxs-lookup"><span data-stu-id="f4131-293">Start a loop that runs over all the users in the variable $x (**foreach ($i in $x)**).</span></span>  
1. <span data-ttu-id="f4131-294">Définissez une variable nommée *$y* et stockez-y les informations de boîte aux lettres de l’utilisateur (**$y = Get-Mailbox-Identity $i. userPrincipalName**).</span><span class="sxs-lookup"><span data-stu-id="f4131-294">Define a variable named *$y* and store the user's mailbox information in it (**$y = Get-Mailbox -Identity $i.UserPrincipalName**).</span></span>
1. <span data-ttu-id="f4131-295">Ajoutez une nouvelle propriété aux informations utilisateur nommées *IsMailBoxEnabled*.</span><span class="sxs-lookup"><span data-stu-id="f4131-295">Add a new property to the user information that's named *IsMailBoxEnabled*.</span></span> <span data-ttu-id="f4131-296">Définissez-la sur la valeur de la propriété IsMailBoxEnabled de la boîte aux lettres de l’utilisateur (**$i | Add-Member-MemberType NoteProperty-Name IsMailBoxEnabled-value $y. IsMailBoxEnabled**).</span><span class="sxs-lookup"><span data-stu-id="f4131-296">Set it to the value of the IsMailBoxEnabled property of the user's mailbox (**$i | Add-Member -MemberType NoteProperty -Name IsMailboxEnabled -Value $y.IsMailboxEnabled**).</span></span>
1. <span data-ttu-id="f4131-297">Définissez une variable nommée *$y*et stockez-y les informations Skype entreprise Online de l’utilisateur (**$y = Get-CsOnlineUser-Identity $i. userPrincipalName**).</span><span class="sxs-lookup"><span data-stu-id="f4131-297">Define a variable named *$y*, and store the user's Skype for Business Online information in it (**$y = Get-CsOnlineUser -Identity $i.UserPrincipalName**).</span></span>
1. <span data-ttu-id="f4131-298">Ajoutez une nouvelle propriété aux informations utilisateur nommées *EnabledForSfB*.</span><span class="sxs-lookup"><span data-stu-id="f4131-298">Add a new property to the user information that's named *EnabledForSfB*.</span></span> <span data-ttu-id="f4131-299">Définissez-la sur la valeur de la propriété Enabled des informations Skype entreprise Online de l’utilisateur (**$i | Add-Member-MemberType NoteProperty-Name EnabledForSfB-value $y. Enabled**).</span><span class="sxs-lookup"><span data-stu-id="f4131-299">Set it to the value of the Enabled property of the user's Skype for Business Online information (**$i | Add-Member -MemberType NoteProperty -Name EnabledForSfB -Value $y.Enabled**).</span></span>
1. <span data-ttu-id="f4131-300">Affichez la liste des utilisateurs, mais n’incluez que leur nom, qu’ils soient sous licence, et les deux nouvelles propriétés qui indiquent si leur boîte aux lettres est activée et si elles sont activées pour Skype entreprise Online (**$x | Sélectionnez DisplayName, IsLicensed, IsMailboxEnabled, EnabledforSfB**).</span><span class="sxs-lookup"><span data-stu-id="f4131-300">Display the list of users, but include only their name, whether they are licensed, and the two new properties that indicate whether their mailbox is enabled and whether they are enabled for Skype for Business Online (**$x | Select DisplayName, IsLicensed, IsMailboxEnabled, EnabledforSfB**).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f4131-301">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4131-301">See also</span></span>

[<span data-ttu-id="f4131-302">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f4131-302">Get started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="f4131-303">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="f4131-303">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="f4131-304">Utilisez Windows PowerShell pour créer des rapports dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f4131-304">Use Windows PowerShell to create reports in Microsoft 365</span></span>](use-windows-powershell-to-create-reports-in-microsoft-365.md)
