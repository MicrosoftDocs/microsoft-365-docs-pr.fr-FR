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
ms.openlocfilehash: 7220356cd79b03674661ace386fd1d38a7e39587
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46689638"
---
# <a name="why-you-need-to-use-powershell-for-microsoft-365"></a><span data-ttu-id="3736b-103">Pourquoi utiliser PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3736b-103">Why you need to use PowerShell for Microsoft 365</span></span>

<span data-ttu-id="3736b-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="3736b-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="3736b-105">Avec le centre d’administration Microsoft 365, vous pouvez non seulement gérer vos licences et comptes d’utilisateur 365 Microsoft, mais également gérer vos services Microsoft 365 tels qu’Exchange Online, teams et SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="3736b-105">With the Microsoft 365 admin center, you can not only manage your Microsoft 365 user accounts and licenses, but you can also manage your Microsoft 365 services such as Exchange Online, Teams, and SharePoint Online.</span></span> <span data-ttu-id="3736b-106">Toutefois, vous pouvez également gérer ces éléments avec les commandes PowerShell, en tirant parti d’un environnement de langage de script et de ligne de commande pour la vitesse, l’automatisation et la capacité supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="3736b-106">However, you can also manage these elements with PowerShell commands, taking advantage of a command-line and scripting language environment for speed, automation, and additional capability.</span></span>
  
<span data-ttu-id="3736b-107">Dans cet article, nous allons vous montrer les façons dont vous pouvez utiliser PowerShell pour gérer Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="3736b-107">In this article, we'll show you these ways in which you can use PowerShell to manage Microsoft 365:</span></span>
  
- <span data-ttu-id="3736b-108">Révéler des informations supplémentaires que vous ne pouvez pas voir avec le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3736b-108">Reveal additional information that you cannot see with the Microsoft 365 admin center</span></span>
    
- <span data-ttu-id="3736b-109">Configuration des fonctionnalités et des paramètres uniquement avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="3736b-109">Configure features and settings only possible with PowerShell</span></span>
    
- <span data-ttu-id="3736b-110">Effectuer des opérations en bloc</span><span class="sxs-lookup"><span data-stu-id="3736b-110">Perform bulk operations</span></span>
    
- <span data-ttu-id="3736b-111">Filtrage des données</span><span class="sxs-lookup"><span data-stu-id="3736b-111">Filtering data</span></span>
    
- <span data-ttu-id="3736b-112">Imprimer ou enregistrer des données</span><span class="sxs-lookup"><span data-stu-id="3736b-112">Print or save data</span></span>
    
- <span data-ttu-id="3736b-113">Gérer dans les services</span><span class="sxs-lookup"><span data-stu-id="3736b-113">Manage across services</span></span>
    
<span data-ttu-id="3736b-114">Avant de commencer, comprenez que PowerShell pour Microsoft 365 est un ensemble de modules pour Windows PowerShell, un environnement en ligne de commande pour les plateformes et les services Windows.</span><span class="sxs-lookup"><span data-stu-id="3736b-114">Before you begin, understand that PowerShell for Microsoft 365 is a set of modules for Windows PowerShell, a command-line environment for Windows-based services and platforms.</span></span> <span data-ttu-id="3736b-115">Cet environnement crée un langage de l’interpréteur de commandes qui peut être étendu avec des modules supplémentaires et permet d’exécuter des commandes ou des scripts simples ou complexes.</span><span class="sxs-lookup"><span data-stu-id="3736b-115">This environment creates a command shell language that can be extended with additional modules and provides a way to execute simple or complex commands or scripts.</span></span> <span data-ttu-id="3736b-116">Par exemple, après avoir installé PowerShell pour les modules Microsoft 365 et vous être connecté à votre abonnement Microsoft 365, vous pouvez exécuter cette commande pour répertorier toutes les boîtes aux lettres utilisateur pour Microsoft Exchange Online :</span><span class="sxs-lookup"><span data-stu-id="3736b-116">For example, after you install the PowerShell for Microsoft 365 modules and connect to your Microsoft 365 subscription, you can run this command to list all of the user mailboxes for Microsoft Exchange Online:</span></span>
  
```powershell
Get-Mailbox
```

<span data-ttu-id="3736b-117">Il est également facile d’obtenir la liste des boîtes aux lettres à l’aide du centre d’administration Microsoft 365, mais le nombre d’éléments dans toutes les listes de tous les sites de toutes les applications Web ne peut pas être facilement réalisé.</span><span class="sxs-lookup"><span data-stu-id="3736b-117">Getting the list of mailboxes can also be easily done using the Microsoft 365 admin center, but counting the number of items in all of the lists for all of the sites for all of your web apps cannot be easily done.</span></span>
  
<span data-ttu-id="3736b-118">Veuillez noter que PowerShell pour Microsoft 365 est conçu pour enrichir et améliorer votre capacité à gérer Microsoft 365, et non pour remplacer le centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3736b-118">Please note that PowerShell for Microsoft 365 is designed to augment and enhance your ability to manage Microsoft 365, not to replace the Microsoft 365 admin center.</span></span> <span data-ttu-id="3736b-119">En tant qu’administrateur, vous devez être au moins familiarisé avec l’utilisation de PowerShell pour Microsoft 365, car il existe des procédures de configuration qui ne peuvent être réalisées qu’avec les commandes PowerShell pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3736b-119">As an administrator, you must become at least comfortable with using PowerShell for Microsoft 365 because there are some configuration procedures that can only be done with PowerShell for Microsoft 365 commands.</span></span> <span data-ttu-id="3736b-120">Dans ces cas, vous devez savoir comment effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="3736b-120">In these cases, you will be required to understand how to:</span></span>
  
- <span data-ttu-id="3736b-121">Installez PowerShell pour les modules Microsoft 365 (opération faite une seule fois pour chaque ordinateur d’administrateur).</span><span class="sxs-lookup"><span data-stu-id="3736b-121">Install the PowerShell for Microsoft 365 modules (done only once for each administrator computer).</span></span>
    
- <span data-ttu-id="3736b-122">Connectez-vous à votre abonnement Microsoft 365 (opération terminée une fois pour chaque session PowerShell).</span><span class="sxs-lookup"><span data-stu-id="3736b-122">Connect to your Microsoft 365 subscription (done once for each PowerShell session).</span></span>
    
- <span data-ttu-id="3736b-123">Recueillez les informations nécessaires pour exécuter les commandes PowerShell requises pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3736b-123">Gather the information needed to run the required PowerShell for Microsoft 365 commands.</span></span>
    
- <span data-ttu-id="3736b-124">Exécutez correctement les commandes PowerShell pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3736b-124">Run the PowerShell for Microsoft 365 commands successfully.</span></span>
    
<span data-ttu-id="3736b-125">Une fois que vous avez acquis ces compétences de base, vous n'êtes plus obligé de répertorier vos utilisateurs de boîte aux lettres avec la commande **Get-Mailbox**, ni de comprendre comment créer une commande comme la précédente pour comptabiliser tous les éléments de toutes les listes de tous les sites pour toutes les applications web.</span><span class="sxs-lookup"><span data-stu-id="3736b-125">After learning these basic skills, you are not required to list your mailbox users with **Get-Mailbox** command, nor are you required to understand how to create a new command like the previous one to count all the items in all the lists for all of the sites for all of your web apps.</span></span> <span data-ttu-id="3736b-126">Microsoft et la communauté des administrateurs peuvent vous aider, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="3736b-126">Microsoft and the community of administrators can help you with that as needed.</span></span>
  
## <a name="powershell-for-microsoft-365-can-reveal-additional-information-that-you-cannot-see-with-the-microsoft-365-admin-center"></a><span data-ttu-id="3736b-127">PowerShell pour Microsoft 365 peut révéler des informations supplémentaires que vous ne pouvez pas voir avec le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3736b-127">PowerShell for Microsoft 365 can reveal additional information that you cannot see with the Microsoft 365 admin center</span></span>

<span data-ttu-id="3736b-128">Le centre d’administration Microsoft 365 affiche un grand nombre d’informations utiles, mais cela ne signifie pas qu’il affiche toutes les informations possibles stockées par Microsoft 365 sur les utilisateurs, les licences, les boîtes aux lettres et les sites.</span><span class="sxs-lookup"><span data-stu-id="3736b-128">The Microsoft 365 admin center displays a lot of useful information, but that doesn't mean that it displays all the possible information that Microsoft 365 stores on users, licenses, mailboxes, and sites.</span></span> <span data-ttu-id="3736b-129">Voici un exemple pour **les utilisateurs et les groupes** dans le centre d’administration 365 de Microsoft :</span><span class="sxs-lookup"><span data-stu-id="3736b-129">Here is an example for **users and groups** in the Microsoft 365 admin center:</span></span>
  
![Exemple d’affichage des utilisateurs et des groupes dans le centre d’administration 365 de Microsoft.](../media/o365-powershell-users-and-groups.png)
  
<span data-ttu-id="3736b-131">Dans de nombreux cas, cela permet d'afficher les informations que vous devez connaître.</span><span class="sxs-lookup"><span data-stu-id="3736b-131">For many purposes, this displays the information you need to know.</span></span> <span data-ttu-id="3736b-132">Toutefois, il peut arriver que vous ayez besoin de plus d'informations.</span><span class="sxs-lookup"><span data-stu-id="3736b-132">However, there are times when you need more.</span></span> <span data-ttu-id="3736b-133">Par exemple, les licences Microsoft 365 (et les fonctionnalités Microsoft 365 disponibles pour un utilisateur) dépendent en partie de l’emplacement géographique de cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3736b-133">For example, Microsoft 365 licensing (and the Microsoft 365 features available to a user) depend in part on that user's geographic location.</span></span> <span data-ttu-id="3736b-134">Les stratégies et les fonctionnalités que vous pouvez étendre à un utilisateur qui vit aux États-Unis peuvent ne pas être les mêmes que celles que vous pouvez étendre à un utilisateur qui vit en Inde ou en Belgique.</span><span class="sxs-lookup"><span data-stu-id="3736b-134">The policies and features you can extend to a user who lives in the United States might not be the same as the policies and features you can extend to a user who lives in India or in Belgium.</span></span> <span data-ttu-id="3736b-135">Vous pouvez utiliser le centre d’administration Microsoft 365 pour déterminer l’emplacement géographique d’un utilisateur en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="3736b-135">You can use the Microsoft 365 admin center to determine a user's geographic location with these steps:</span></span>
  
1. <span data-ttu-id="3736b-136">Double-cliquez sur l'élément **Nom d'affichage** de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3736b-136">Double-click the user's **Display Name**.</span></span>
    
2. <span data-ttu-id="3736b-137">Dans le volet d'affichage des propriétés utilisateur, cliquez sur **détails**.</span><span class="sxs-lookup"><span data-stu-id="3736b-137">In the user properties display pane, click **details**.</span></span>
    
3. <span data-ttu-id="3736b-138">Dans l'affichage des détails, cliquez sur **détails supplémentaires**.</span><span class="sxs-lookup"><span data-stu-id="3736b-138">In the details display, click **additional details**.</span></span>
    
4. <span data-ttu-id="3736b-139">Faites défiler la liste vers le bas jusqu'à ce que vous voyiez l'en-tête **Pays ou région**:</span><span class="sxs-lookup"><span data-stu-id="3736b-139">Scroll down until you see the heading **Country or region**:</span></span>
    
     ![Exemple d’informations de région pour un utilisateur dans le centre d’administration Microsoft 365.](../media/o365-powershell-usage-location.png)
  
5. <span data-ttu-id="3736b-141">Écrivez le nom d'affichage et l'emplacement de l'utilisateur sur un morceau de papier, ou copiez-le et collez-le dans le Bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="3736b-141">Write the user's display name and location on a piece of paper, or copy and paste it into Notepad.</span></span> 
    
<span data-ttu-id="3736b-142">Vous devez répéter cette procédure pour chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3736b-142">You must repeat this procedure for each user.</span></span> <span data-ttu-id="3736b-143">Si les utilisateurs sont nombreux, cela peut être une tâche fastidieuse.</span><span class="sxs-lookup"><span data-stu-id="3736b-143">For many users, this can be a tedious task.</span></span> <span data-ttu-id="3736b-144">Avec PowerShell pour Microsoft 365, vous pouvez afficher ces informations pour tous vos utilisateurs à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="3736b-144">With PowerShell for Microsoft 365, you can display this information for all of your users with the following command:</span></span>
  
```powershell
Get-AzureADUser | Select DisplayName, UsageLocation
```


>[!Note]
><span data-ttu-id="3736b-145">PowerShell Core ne prend pas en charge le module Microsoft Azure Active Directory pour Windows PowerShell et les applets de commande incluant **Msol** dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="3736b-145">PowerShell Core does not support the Microsoft Azure Active Directory Module for Windows PowerShell module and cmdlets with **Msol** in their name.</span></span> <span data-ttu-id="3736b-146">Pour continuer à utiliser ces applets de commande, vous devez les exécuter à partir de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3736b-146">To continue using these cmdlets, you must run them from Windows PowerShell.</span></span>
>

<span data-ttu-id="3736b-147">Voici un exemple d’affichage :</span><span class="sxs-lookup"><span data-stu-id="3736b-147">Here is an example of the display:</span></span>
  
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

> [!TIP]
>  <span data-ttu-id="3736b-148">L’interprétation de cette commande PowerShell est la suivante : obtenir tous les utilisateurs dans l’abonnement Microsoft 365 actuel ( **Get-AzureADUser** ), mais afficher uniquement le nom et l’emplacement de chaque utilisateur ( **Select DisplayName, UsageLocation** ).</span><span class="sxs-lookup"><span data-stu-id="3736b-148">The interpretation of this PowerShell command is: Get all of the users in the current Microsoft 365 subscription ( **Get-AzureADUser** ), but only display the name and location for each user ( **Select DisplayName, UsageLocation** ).</span></span>
  
<span data-ttu-id="3736b-149">Étant donné que PowerShell pour Microsoft 365 prend en charge une langue de l’interpréteur de commandes, vous pouvez manipuler les informations obtenues à partir de la commande **Get-AzureADUser** .</span><span class="sxs-lookup"><span data-stu-id="3736b-149">Because PowerShell for Microsoft 365 supports a command shell language, you can further manipulate the information obtained from the **Get-AzureADUser** command.</span></span> <span data-ttu-id="3736b-150">Par exemple, vous voudrez peut-être trier ces utilisateurs en fonction de leur emplacement, en regroupant tous les utilisateurs brésiliens, tous les utilisateurs des États-Unis, etc. Voici la commande :</span><span class="sxs-lookup"><span data-stu-id="3736b-150">For example, maybe you'd like to sort these users by their location, grouping all the Brazilian users together, all the United States users together, etc. Here is the command:</span></span>
  
```powershell
Get-AzureADUser | Select DisplayName, UsageLocation | Sort UsageLocation, DisplayName
```

<span data-ttu-id="3736b-151">Voici un exemple d’affichage :</span><span class="sxs-lookup"><span data-stu-id="3736b-151">Here is an example of the display:</span></span>
  
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

> [!TIP]
>  <span data-ttu-id="3736b-152">L’interprétation de cette commande PowerShell est la suivante : obtenir tous les utilisateurs de l’abonnement Microsoft 365 actuel, mais afficher uniquement le nom et l’emplacement de chaque utilisateur et les trier d’abord en fonction de leur emplacement, puis leur nom ( **Trier UsageLocation, DisplayName** ).</span><span class="sxs-lookup"><span data-stu-id="3736b-152">The interpretation of this PowerShell command is: Get all of the users in the current Microsoft 365 subscription, but only display the name and location for each user and sort them first by their location, and then their names ( **Sort UsageLocation, DisplayName** ).</span></span>
  
<span data-ttu-id="3736b-p110">Vous pouvez également employer un filtrage supplémentaire. Par exemple, si vous voulez uniquement voir les informations relatives aux utilisateurs situés au Brésil, utilisez cette commande :</span><span class="sxs-lookup"><span data-stu-id="3736b-p110">You can also employ additional filtering. For example, if you only want to see information about users based in Brazil, use this command:</span></span>
  
```powershell
Get-AzureADUser | Where {$_.UsageLocation -eq "BR"} | Select DisplayName, UsageLocation 
```

<span data-ttu-id="3736b-155">Voici un exemple d’affichage :</span><span class="sxs-lookup"><span data-stu-id="3736b-155">Here is an example of the display:</span></span>
  
```powershell
DisplayName                                           UsageLocation
-----------                                           -------------
David Longmuir                                        BR
Fabrice Canel                                         BR
```

> [!TIP]
>  <span data-ttu-id="3736b-156">L’interprétation de cette commande PowerShell est la suivante : obtenir tous les utilisateurs de l’abonnement Microsoft 365 actuel dont l’emplacement est le Brésil ( **où {$ \_ . UsageLocation-EQ "BR"}** ), puis affichez le nom et l’emplacement de chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3736b-156">The interpretation of this PowerShell command is: Get all of the users in the current Microsoft 365 subscription whose location is Brazil ( **Where {$\_.UsageLocation -eq "BR"}** ), then display the name and location for each user.</span></span>
  
 <span data-ttu-id="3736b-157">**Rapide remarque concernant les domaines plus volumineux**</span><span class="sxs-lookup"><span data-stu-id="3736b-157">**A Quick Note Regarding Larger Domains**</span></span>
  
<span data-ttu-id="3736b-158">Si vous avez un très grand domaine, disons avec des dizaines de milliers d'utilisateurs, l'exécution de certains des exemples que nous vous présentons dans cet article pourrait conduire à une « limitation de bande passante ».</span><span class="sxs-lookup"><span data-stu-id="3736b-158">If you have a very large domain with tens of thousands of users, trying some of the examples we show in this article could lead to "throttling."</span></span> <span data-ttu-id="3736b-159">Cela signifie que, selon des éléments tels que la puissance de l'ordinateur et la bande passante réseau disponible, vous essayez d'effectuer un trop grand nombre d'actions à la fois.</span><span class="sxs-lookup"><span data-stu-id="3736b-159">That means that, based on things like computing power and available network bandwidth, you're trying to do a little too much at one time.</span></span> <span data-ttu-id="3736b-160">Pour cette raison, les organisations de plus grande taille peuvent souhaiter diviser certaines de ces commandes PowerShell pour Microsoft 365 en deux commandes.</span><span class="sxs-lookup"><span data-stu-id="3736b-160">Because of that, larger organizations might want to split some of these PowerShell for Microsoft 365 commands into two commands.</span></span> <span data-ttu-id="3736b-161">Par exemple, cette commande renvoie tous les comptes d'utilisateur et affiche le nom et l'emplacement pour chacun d'entre eux :</span><span class="sxs-lookup"><span data-stu-id="3736b-161">For example, this one command returns all the user accounts and shows the name and location for each:</span></span>
  
```powershell
Get-AzureADUser | Select DisplayName, UsageLocation
```

<span data-ttu-id="3736b-p112">Cela fonctionne bien pour les petits domaines. Dans une grande organisation, en revanche, vous devrez peut-être diviser cette commande en deux : une commande pour stocker les informations de compte d'utilisateur dans une variable et une autre commande pour afficher les informations nécessaires. Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="3736b-p112">That works great for smaller domains. In a large organization, however, you might need to split that into two commands: one command to store the user account information in a variable and another command to display the needed information. Here is an example:</span></span>
  
```powershell
$x = Get-AzureADUser
$x | Select DisplayName, UsageLocation
```

<span data-ttu-id="3736b-165">L’interprétation de cet ensemble de commandes PowerShell est la suivante :</span><span class="sxs-lookup"><span data-stu-id="3736b-165">The interpretation of this set of PowerShell commands is:</span></span>
- <span data-ttu-id="3736b-166">Obtenez tous les utilisateurs dans l’abonnement Microsoft 365 actuel et stockez les informations dans une variable nommée $x ( **$x = Get-AzureADUser** ).</span><span class="sxs-lookup"><span data-stu-id="3736b-166">Get all of the users in the current Microsoft 365 subscription and store the information in a variable named $x ( **$x = Get-AzureADUser** ).</span></span>
- <span data-ttu-id="3736b-167">Affiche le contenu de la variable $x, mais inclut uniquement le nom et l’emplacement de chaque utilisateur ( **$x | Select DisplayName, UsageLocation** ).</span><span class="sxs-lookup"><span data-stu-id="3736b-167">Display the contents of the variable $x, but only include the name and location for each user ( **$x | Select DisplayName, UsageLocation** ).</span></span>
  
## <a name="microsoft-365-has-features-that-you-can-only-configure-with-powershell-for-microsoft-365"></a><span data-ttu-id="3736b-168">Microsoft 365 dispose de fonctionnalités que vous pouvez configurer uniquement avec PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3736b-168">Microsoft 365 has features that you can only configure with PowerShell for Microsoft 365</span></span>

<span data-ttu-id="3736b-169">Le centre d’administration Microsoft 365 est destiné à fournir un accès aux tâches d’administration les plus courantes ou les plus pertinentes qui s’appliquent à la plupart des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="3736b-169">The Microsoft 365 admin center is intended to provide access to the most common or meaningful administrative tasks that apply to most people.</span></span> <span data-ttu-id="3736b-170">En d’autres termes, le centre d’administration Microsoft 365 a été conçu afin que l’administrateur par défaut puisse utiliser l’outil pour effectuer les tâches de gestion les plus courantes.</span><span class="sxs-lookup"><span data-stu-id="3736b-170">In other words, the Microsoft 365 admin center was designed so that the typical administrator could use the tool to carry out the most common management tasks.</span></span> <span data-ttu-id="3736b-171">Par cette définition, cela signifie qu’il existe certaines tâches qui ne peuvent pas être exécutées à l’aide du centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3736b-171">By this definition, that means that there are some tasks that can't be completed by using the Microsoft 365 admin center.</span></span>
  
<span data-ttu-id="3736b-172">Par exemple, le Centre d'administration Skype Entreprise Online offre plusieurs options permettant de créer des invitations personnalisées aux réunions :</span><span class="sxs-lookup"><span data-stu-id="3736b-172">For example, the Skype for Business Online Admin center provides a few options for creating custom meeting invitations:</span></span>
  
![Exemple d’affichage d’invitations personnalisées à une réunion dans le Centre d’administration de Skype Entreprise Online.](../media/o365-powershell-meeting-invitation.png)
  
<span data-ttu-id="3736b-p114">Avec ces paramètres, vous pouvez ajouter une touche de personnalisation et de professionnalisme aux invitations aux réunions. Cependant, les paramètres de configuration de réunion ne se résument pas à la simple création d'invitations personnalisées aux réunions. Par défaut, les réunions autorisent :</span><span class="sxs-lookup"><span data-stu-id="3736b-p114">With these settings, you can add a touch of personalization and professionalism to meeting invitations. However, there's more to meeting configuration settings than simply creating custom meeting invitations. For example, by default, meetings allow:</span></span>
  
- <span data-ttu-id="3736b-177">les utilisateurs anonymes à obtenir une entrée automatique à chaque réunion ;</span><span class="sxs-lookup"><span data-stu-id="3736b-177">Anonymous users to gain automatic entrance to each meeting.</span></span>
    
- <span data-ttu-id="3736b-178">les participants à enregistrer la réunion ;</span><span class="sxs-lookup"><span data-stu-id="3736b-178">Attendees to record the meeting.</span></span>
    
- <span data-ttu-id="3736b-179">tous les utilisateurs de votre organisation à être désignés en tant que présentateurs lorsqu’ils rejoignent la réunion.</span><span class="sxs-lookup"><span data-stu-id="3736b-179">All users from your organization to be designated as presenters when they join the meeting.</span></span>
    
<span data-ttu-id="3736b-180">Ces paramètres ne sont pas disponibles à partir du Centre d'administration Skype Entreprise Online.</span><span class="sxs-lookup"><span data-stu-id="3736b-180">These settings are not available from the Skype for Business Online Admin center.</span></span> <span data-ttu-id="3736b-181">Toutefois, vous pouvez les contrôler à partir de PowerShell pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3736b-181">However, you can control them from PowerShell for Microsoft 365.</span></span> <span data-ttu-id="3736b-182">Voici une commande qui désactive ces trois paramètres :</span><span class="sxs-lookup"><span data-stu-id="3736b-182">Here is a command that disables these three settings:</span></span>
  
```powershell
Set-CsMeetingConfiguration -AdmitAnonymousUsersByDefault $False -AllowConferenceRecording $False -DesignateAsPresenter "None"
```

> [!NOTE]
> <span data-ttu-id="3736b-183">Cette commande exige que vous installiez le [module Windows PowerShell pour Skype Entreprise Online](https://www.microsoft.com/download/details.aspx?id=39366).</span><span class="sxs-lookup"><span data-stu-id="3736b-183">This command requires that you install the [Skype for Business Online PowerShell Module ](https://www.microsoft.com/download/details.aspx?id=39366).</span></span> 
  
> [!TIP]
>  <span data-ttu-id="3736b-184">L’interprétation de cette commande PowerShell est la suivante : pour les paramètres des nouvelles réunions Skype entreprise Online ( **Set-CsMeetingConfiguration** ), Disable autorisant les utilisateurs anonymes à obtenir une entrée automatique des réunions ( **-AdmitAnonymousUsersByDefault $false** ), désactivez la possibilité pour les participants d’enregistrer des **réunions (** **-AllowConferenceRecording $false** ) et ne désignez pas tous les utilisateurs de votre organisation comme présentateurs</span><span class="sxs-lookup"><span data-stu-id="3736b-184">The interpretation of this PowerShell command is: For the settings for new Skype for Business Online meetings ( **Set-CsMeetingConfiguration** ), disable allowing anonymous users to gain automatic entrance to meetings ( **-AdmitAnonymousUsersByDefault $False** ), disable the ability for attendees to record meetings ( **-AllowConferenceRecording $False** ), and do not designate all users from your organization as presenters ( **-DesignateAsPresenter "None"** ).</span></span>
  
<span data-ttu-id="3736b-185">Si vous changez d’avis et souhaitez restaurer ces paramètres par défaut (tous les activer), exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="3736b-185">If you change your mind and want to restore these default settings (all of them enabled), run this command:</span></span>
  
```powershell
Set-CsMeetingConfiguration -AdmitAnonymousUsersByDefault $True -AllowConferenceRecording $True -DesignateAsPresenter "Company"
```

<span data-ttu-id="3736b-186">Il s'agit juste d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="3736b-186">This is just one example.</span></span> <span data-ttu-id="3736b-187">Il en existe d’autres, c’est pourquoi vous devez être familiarisé avec l’exécution de PowerShell pour les commandes Microsoft 365 en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="3736b-187">There are others, which is why you, as an administrator, need to be comfortable with running PowerShell for Microsoft 365 commands.</span></span>
  
## <a name="powershell-for-microsoft-365-is-great-at-carrying-out-bulk-operations"></a><span data-ttu-id="3736b-188">PowerShell pour Microsoft 365 est idéal pour effectuer des opérations en bloc</span><span class="sxs-lookup"><span data-stu-id="3736b-188">PowerShell for Microsoft 365 is great at carrying out bulk operations</span></span>

<span data-ttu-id="3736b-189">Traditionnellement, les interfaces visuelles telles que le centre d’administration Microsoft 365 sont plus utiles lorsque vous avez une seule opération à effectuer.</span><span class="sxs-lookup"><span data-stu-id="3736b-189">Historically, visual interfaces like the Microsoft 365 admin center are most valuable when you have a single operation to perform.</span></span> <span data-ttu-id="3736b-190">Par exemple, si vous avez besoin de désactiver un compte d’utilisateur, vous pouvez utiliser le centre d’administration Microsoft 365 pour localiser et désactiver rapidement une case à cocher.</span><span class="sxs-lookup"><span data-stu-id="3736b-190">For example, if you need to disable one user account, you can use the Microsoft 365 admin center to quickly locate and clear a checkbox.</span></span> <span data-ttu-id="3736b-191">Cela peut être plus simple que d’effectuer une opération similaire dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3736b-191">This can be simpler than performing a similar operation in PowerShell.</span></span>
  
<span data-ttu-id="3736b-192">Toutefois, si vous devez modifier de nombreux éléments ou des éléments sélectionnés dans un grand nombre d’autres choses, le centre d’administration de Microsoft 365 peut ne pas être le meilleur moyen de votre temps.</span><span class="sxs-lookup"><span data-stu-id="3736b-192">But if you have to change many things or some selected things within a large set of other things, the Microsoft 365 admin center might not be the best use of your time.</span></span> <span data-ttu-id="3736b-193">Par exemple, si vous deviez modifier le préfixe sur des milliers de numéros de téléphone ou si vous avez besoin de supprimer un utilisateur spécifique, Ken Myer, de tous vos sites SharePoint Online, comment pouvez-vous le faire dans le centre d’administration 365 de Microsoft ?</span><span class="sxs-lookup"><span data-stu-id="3736b-193">For example, if you had to change the prefix on thousands of phone numbers or you needed to remove a specific user, Ken Myer, from all of your SharePoint Online sites, how would you do that in the Microsoft 365 admin center?</span></span>
  
<span data-ttu-id="3736b-194">Pour ce dernier exemple, vous disposez de plusieurs centaines de sites SharePoint Online et vous ne savez même pas desquels Ken Meyer est membre.</span><span class="sxs-lookup"><span data-stu-id="3736b-194">For the latter example, you have several hundred SharePoint Online sites and you don't know even know which ones of which Ken Meyer is a member.</span></span> <span data-ttu-id="3736b-195">Cela signifie que vous devrez démarrer à partir du centre d’administration 365 de Microsoft, puis effectuer cette procédure pour chaque site :</span><span class="sxs-lookup"><span data-stu-id="3736b-195">That means you'll have to start at the Microsoft 365 admin center and then perform this procedure for each site:</span></span>
  
1. <span data-ttu-id="3736b-196">Cliquez sur l' **URL** du site.</span><span class="sxs-lookup"><span data-stu-id="3736b-196">Click the **URL** of the site.</span></span>
    
2. <span data-ttu-id="3736b-197">Dans la zone **Propriétés de la collection de sites**, cliquez sur le lien **Adresse du site web** pour accéder au site.</span><span class="sxs-lookup"><span data-stu-id="3736b-197">In the **site collection properties** box, click the **Web Site Address** link to open the site.</span></span>
    
3. <span data-ttu-id="3736b-198">Sur le site, cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="3736b-198">On the site, click **Share**.</span></span>
    
4. <span data-ttu-id="3736b-199">Dans la boîte de dialogue **Partager**, cliquez sur le lien qui affiche tous les utilisateurs disposant d'autorisations sur le site :</span><span class="sxs-lookup"><span data-stu-id="3736b-199">In the **Share** dialog box click the link that shows you all the users who have permissions to the site:</span></span>
    
     ![Exemple d’affichage des membres d’un site SharePoint Online dans le Centre d’administration SharePoint Online.](../media/o365-powershell-view-permissions.png)
  
5. <span data-ttu-id="3736b-201">Dans la boîte de dialogue **Partagé avec**, cliquez sur **Avancé**.</span><span class="sxs-lookup"><span data-stu-id="3736b-201">In the **Shared With** dialog box, click **Advanced**.</span></span>
    
6. <span data-ttu-id="3736b-202">Faites défiler vers le bas la liste des utilisateurs, recherchez et sélectionnez Ken Myer (en supposant qu'il dispose d'autorisations sur le site), puis cliquez sur **Supprimer les autorisations des utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="3736b-202">Scroll down the list of users, find and select Ken Myer (assuming he has permissions to the site), and then click **Remove User Permissions**.</span></span>
    
<span data-ttu-id="3736b-203">Réaliser la procédure pour plusieurs centaines de sites peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="3736b-203">This can take a long time for several hundred sites.</span></span>
  
<span data-ttu-id="3736b-204">Vous pouvez également utiliser PowerShell pour Microsoft 365 et la commande suivante pour supprimer Ken Myer de tous vos sites :</span><span class="sxs-lookup"><span data-stu-id="3736b-204">The alternative is to use PowerShell for Microsoft 365 and the following command to remove Ken Myer from all of your sites:</span></span>
  
```powershell
Get-SPOSite | ForEach {Remove-SPOUser -Site $_.Url -LoginName "kenmyer@litwareinc.com"}
```

> [!NOTE]
> <span data-ttu-id="3736b-205">Cette commande exige que vous installiez le [module SharePoint Online PowerShell](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps).</span><span class="sxs-lookup"><span data-stu-id="3736b-205">This command requires that you install the [SharePoint Online PowerShell module](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps).</span></span> 
  
> [!TIP]
>  <span data-ttu-id="3736b-206">L’interprétation de cette commande PowerShell est la suivante : obtenir tous les sites SharePoint dans l’abonnement Microsoft 365 actuel ( **Get-SPOSite** ) et pour chaque site, supprimez Ken Meyer de la liste des utilisateurs qui peuvent y accéder ( **foreach {Remove-épouser-site $ \_ . URL-LoginName "kenmyer@litwareinc.com"}** ).</span><span class="sxs-lookup"><span data-stu-id="3736b-206">The interpretation of this PowerShell command is:  Get all of the SharePoint sites in the current Microsoft 365 subscription ( **Get-SPOSite** ) and for each site, remove Ken Meyer from the list of users who can access it ( **ForEach {Remove-SPOUser -Site $\_.Url -LoginName "kenmyer@litwareinc.com"}** ).</span></span>
  
<span data-ttu-id="3736b-207">Étant donné que nous indiquons à Microsoft 365 de supprimer Ken Meyer de chaque site, y compris ceux auxquels il n’a pas accès, l’affichage de cette commande affiche des erreurs pour les sites dans lesquels il n’a pas accès.</span><span class="sxs-lookup"><span data-stu-id="3736b-207">Because we are telling Microsoft 365 to remove Ken Meyer from every site, including those in which he does not have access, the display of this command will show errors for those sites in which he does not currently have access.</span></span> <span data-ttu-id="3736b-208">Nous pouvons utiliser une condition supplémentaire sur cette commande pour supprimer Ken Meyer uniquement des sites qui l'ont dans leur liste de connexion, mais les erreurs répertoriées ne nuisent pas aux sites eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="3736b-208">We can use an additional condition on this command to remove Key Meyer only from the sites that have him in their login list, but the listed errors cause no harm to the sites themselves.</span></span> <span data-ttu-id="3736b-209">L’exécution de cette commande peut prendre quelques minutes sur des centaines de sites, et non sur des heures de travail par le biais du centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3736b-209">This command might take a few minutes to run against hundreds of sites, rather than hours of working through the Microsoft 365 admin center.</span></span>
  
<span data-ttu-id="3736b-p121">Voici un autre exemple d’opération en bloc. Utilisez cette commande pour ajouter Bonnie Kearney, une nouvelle administratrice SharePoint, à tous les sites de l’organisation :</span><span class="sxs-lookup"><span data-stu-id="3736b-p121">Here is another bulk operation example. Use this command to add Bonnie Kearney, a new SharePoint administrator, to all of the sites in the organization:</span></span>
  
```powershell
Get-SPOSite | ForEach {Add-SPOUser -Site $_.Url -LoginName "bkearney@litwareinc.com" -Group "Members"}
```

> [!TIP]
>  <span data-ttu-id="3736b-212">L’interprétation de cette commande PowerShell est la suivante : obtenir tous les sites SharePoint de l’abonnement Microsoft 365 actuel et pour chaque site, autoriser l’accès Kearney Bonnie en ajoutant son nom de connexion au groupe membres du site ( **foreach {Add-époux-site $ \_ . URL-LoginName "bkearney@litwareinc.com"-Group "members"}** ).</span><span class="sxs-lookup"><span data-stu-id="3736b-212">The interpretation of this PowerShell command is:  Get all of the SharePoint sites in the current Microsoft 365 subscription and for each site, allow Bonnie Kearney access by adding her login name to the Members group of the site ( **ForEach {Add-SPOUser -Site $\_.Url -LoginName "bkearney@litwareinc.com" -Group "Members"}** ).</span></span>
  
## <a name="powershell-for-microsoft-365-is-great-at-filtering-data"></a><span data-ttu-id="3736b-213">PowerShell pour Microsoft 365 est idéal pour le filtrage des données</span><span class="sxs-lookup"><span data-stu-id="3736b-213">PowerShell for Microsoft 365 is great at filtering data</span></span>

<span data-ttu-id="3736b-214">Le centre d’administration 365 de Microsoft offre plusieurs méthodes pour filtrer vos données afin de localiser rapidement et facilement un sous-ensemble ciblé d’informations.</span><span class="sxs-lookup"><span data-stu-id="3736b-214">The Microsoft 365 admin center provides several different ways to filter your data to quickly and easily locate a targeted subset of information.</span></span> <span data-ttu-id="3736b-215">Par exemple, Exchange facilite le filtrage sur pratiquement toutes les propriétés de la boîte aux lettres d'un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3736b-215">For example, Exchange makes it easy to filter on practically any property of a user mailbox.</span></span> <span data-ttu-id="3736b-216">Par exemple, voici la liste des boîtes aux lettres de tous les utilisateurs qui habitent Bloomington :</span><span class="sxs-lookup"><span data-stu-id="3736b-216">For example, here is the list of mailboxes for all the users who live in the city of Bloomington:</span></span>
  
![Exemple de recherche avancée dans le centre d’administration Microsoft 365 pour obtenir la liste des boîtes aux lettres de tous les utilisateurs vivant dans la ville de Bloomington.](../media/o365-powershell-advanced-search.png)
  
<span data-ttu-id="3736b-p123">Le Centre d'administration Exchange vous permet également de combiner des critères de filtre. Par exemple, vous pouvez trouver les boîtes aux lettres de toutes les personnes qui habitent à Bloomington et travaillent dans le service Finances.</span><span class="sxs-lookup"><span data-stu-id="3736b-p123">The Exchange Admin center also lets you combine filter criteria. For example, you can find the mailboxes for all the people who live in Bloomington and who work in the Finance department.</span></span> 
  
<span data-ttu-id="3736b-p124">Toutefois, il existe des limites à ce que vous pouvez faire dans le Centre d'administration Exchange. Par exemple, vous souhaitez peut-être trouver les boîtes aux lettres des personnes qui habitent à Bloomington ou San Diego, ou les boîtes aux lettres de toutes les personnes qui n'habitent pas à Bloomington.</span><span class="sxs-lookup"><span data-stu-id="3736b-p124">However, there are limitations to what you can do in the Exchange Admin center. For example, maybe you'd like to find the mailboxes of people who live in Bloomington or San Diego, or the mailboxes for all the people who don't live in Bloomington.</span></span> 
  
<span data-ttu-id="3736b-222">Avec PowerShell pour Microsoft 365, vous pouvez obtenir la liste des boîtes aux lettres de toutes les personnes vivant dans les villes de Bloomington ou San Diego avec cette commande :</span><span class="sxs-lookup"><span data-stu-id="3736b-222">With PowerShell for Microsoft 365, you can get a list of mailboxes for all the people who live in the cities of Bloomington or San Diego with this command:</span></span>
  
```powershell
Get-User | Where {$_.RecipientTypeDetails -eq "UserMailbox" -and ($_.City -eq "San Diego" -or $_.City -eq "Bloomington")} | Select DisplayName, City
```

<span data-ttu-id="3736b-223">Voici un exemple d’affichage :</span><span class="sxs-lookup"><span data-stu-id="3736b-223">Here is an example of the display:</span></span>
  
```powershell
DisplayName                              City
-----------                              ----
Alex Darrow                              San Diego
Bonnie Kearney                           San Diego
Julian Isla                              Bloomington
Rob Young                                Bloomington
```

> [!TIP]
>  <span data-ttu-id="3736b-224">L’interprétation de cette commande PowerShell est la suivante : obtenir tous les utilisateurs de l’abonnement Microsoft 365 actuel disposant d’une boîte aux lettres dans les villes de San Diego ou Bloomington ( **où {$ \_ . RecipientTypeDetails-EQ "UserMailbox"-et ($ \_ . City-EQ "San Diego"-ou $ \_ . City-EQ "Bloomington")}** ), puis affichez le nom et la ville de chacune d’entre elles ( **Sélectionnez DisplayName, City** ).</span><span class="sxs-lookup"><span data-stu-id="3736b-224">The interpretation of this PowerShell command is: Get all of the users in the current Microsoft 365 subscription who have a mailbox in the cities of either San Diego or Bloomington ( **Where {$\_.RecipientTypeDetails -eq "UserMailbox" -and ($\_.City -eq "San Diego" -or $\_.City -eq "Bloomington")}** ), then display the name and city for each ( **Select DisplayName, City** ).</span></span>
  
<span data-ttu-id="3736b-225">Pour répertorier toutes les boîtes aux lettres des personnes habitant n’importe où sauf à Bloomington, voici la commande :</span><span class="sxs-lookup"><span data-stu-id="3736b-225">To list all the mailboxes for people who live anywhere except Bloomington, here is the command:</span></span>
  
```powershell
Get-User | Where {$_.RecipientTypeDetails -eq "UserMailbox" -and $_.City -ne "Bloomington"} | Select DisplayName, City
```

<span data-ttu-id="3736b-226">Voici un exemple d’affichage :</span><span class="sxs-lookup"><span data-stu-id="3736b-226">Here is an example of the display:</span></span>
  
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

> [!TIP]
>  <span data-ttu-id="3736b-227">L’interprétation de cette commande PowerShell est la suivante : obtenir tous les utilisateurs de l’abonnement Microsoft 365 actuel qui disposent d’une boîte aux lettres qui ne se trouve pas dans la ville de Bloomington ( **où {$ \_ . RecipientTypeDetails-EQ "UserMailbox"-et $ \_ . Ville-ne "Bloomington"}** ), puis affiche le nom et la ville de chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="3736b-227">The interpretation of this PowerShell command is: Get all of the users in the current Microsoft 365 subscription who have a mailbox not located in the city of Bloomington ( **Where {$\_.RecipientTypeDetails -eq "UserMailbox" -and $\_.City -ne "Bloomington"}** ), then display the name and city for each.</span></span>
  
<span data-ttu-id="3736b-228">Vous pouvez également utiliser des caractères génériques dans vos filtres PowerShell pour faire correspondre une partie d’un nom.</span><span class="sxs-lookup"><span data-stu-id="3736b-228">You can also use wildcard characters in your PowerShell filters to match part of a name.</span></span> <span data-ttu-id="3736b-229">Par exemple, supposons que vous recherchiez un compte d'utilisateur et que vous vous rappeliez uniquement que son nom est Anderson, ou Henderson, ou bien Jorgenson.</span><span class="sxs-lookup"><span data-stu-id="3736b-229">For example, suppose you're looking for a user account, and all you can remember is that their last name was Anderson, or maybe Henderson, or maybe it was Jorgenson.</span></span>
  
<span data-ttu-id="3736b-230">Vous pouvez identifier cet utilisateur dans le centre d’administration 365 de Microsoft à l’aide de l’outil de recherche et en effectuant trois recherches différentes :</span><span class="sxs-lookup"><span data-stu-id="3736b-230">You could track down that user in the Microsoft 365 admin center by using the search tool and carrying out three different searches:</span></span>
  
- <span data-ttu-id="3736b-231">Une sur  *Anderson*</span><span class="sxs-lookup"><span data-stu-id="3736b-231">One for  *Anderson*</span></span> 
    
- <span data-ttu-id="3736b-232">Une sur  *Henderson*</span><span class="sxs-lookup"><span data-stu-id="3736b-232">One for  *Henderson*</span></span> 
    
- <span data-ttu-id="3736b-233">Une sur  *Jorgenson*</span><span class="sxs-lookup"><span data-stu-id="3736b-233">One for  *Jorgenson*</span></span> 
    
<span data-ttu-id="3736b-234">Étant donné que ces trois noms se terminent par « fils », vous pouvez indiquer à PowerShell d’afficher tous les utilisateurs dont le nom se termine par « fils ».</span><span class="sxs-lookup"><span data-stu-id="3736b-234">Because all three of these names end in "son", you can tell PowerShell to display all the users whose name ends in "son".</span></span> <span data-ttu-id="3736b-235">Voici la commande :</span><span class="sxs-lookup"><span data-stu-id="3736b-235">Here is the command:</span></span>
  
```powershell
Get-User -Filter '{LastName -like "*son"}'
```

> [!TIP]
>  <span data-ttu-id="3736b-236">L’interprétation de cette commande PowerShell est la suivante : obtenir tous les utilisateurs de l’abonnement Microsoft 365 actuel, mais utiliser un filtre qui répertorie uniquement les utilisateurs dont le nom de famille se termine par « fils » ( **-Filter « {LastName-like " \* fils »}»** ).</span><span class="sxs-lookup"><span data-stu-id="3736b-236">The interpretation of this PowerShell command is: Get all of the users in the current Microsoft 365 subscription, but use a filter that only lists the users whose last names end in "son" ( **-Filter '{LastName -like "\*son"}'** ).</span></span> <span data-ttu-id="3736b-237">\*Représente un ensemble de caractères, qui sont des lettres dans le cas du nom de famille de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3736b-237">The \* stands for any set of characters, which are letters in the case of the user's last name.</span></span>
  
## <a name="powershell-for-microsoft-365-makes-it-easy-to-print-or-save-data"></a><span data-ttu-id="3736b-238">PowerShell pour Microsoft 365 facilite l’impression ou l’enregistrement des données</span><span class="sxs-lookup"><span data-stu-id="3736b-238">PowerShell for Microsoft 365 makes it easy to print or save data</span></span>

<span data-ttu-id="3736b-239">Le centre d’administration Microsoft 365 vous permet d’afficher des listes de données.</span><span class="sxs-lookup"><span data-stu-id="3736b-239">The Microsoft 365 admin center lets you view lists of data.</span></span> <span data-ttu-id="3736b-240">Voici un exemple dans lequel le Centre d'administration Skype Entreprise Online affiche la liste des utilisateurs qui ont été activés pour Skype Entreprise Online :</span><span class="sxs-lookup"><span data-stu-id="3736b-240">Here is an example of the Skype for Business Online Admin center displaying a list of users who have been enabled for Skype for Business Online:</span></span>
  
![Exemple de liste d’utilisateurs ayant été activés pour Skype Entreprise Online, affichée dans le Centre d’administration de Skype Entreprise Online.](../media/o365-powershell-lync-users.png)
  
<span data-ttu-id="3736b-242">Pour enregistrer ces informations dans un fichier, vous devez les copier-coller dans un document ou dans Excel.</span><span class="sxs-lookup"><span data-stu-id="3736b-242">To save that information to a file, you must copy and paste it into a document or Excel.</span></span> <span data-ttu-id="3736b-243">Dans les deux cas, la copie peut nécessiter une mise en forme supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="3736b-243">In either case, the copy might require additional formatting.</span></span> <span data-ttu-id="3736b-244">En outre, le centre d’administration Microsoft 365 ne permet pas d’imprimer directement la liste affichée.</span><span class="sxs-lookup"><span data-stu-id="3736b-244">Additionally, the Microsoft 365 admin center does not provide a way to directly print the displayed list.</span></span>
  
<span data-ttu-id="3736b-245">Heureusement, vous pouvez utiliser PowerShell pour non seulement afficher la liste, mais l’enregistrer dans un fichier qui peut être facilement importé dans Excel.</span><span class="sxs-lookup"><span data-stu-id="3736b-245">Fortunately, you can use PowerShell to not only display the list, but save it to a file that can be easily imported into Excel.</span></span> <span data-ttu-id="3736b-246">Voici un exemple de commande permettant d'enregistrer des données utilisateur Skype Entreprise Online dans un fichier au format CSV (valeurs séparées par des virgules), fichier qui peut être facilement importé sous forme de tableau dans une feuille de calcul Excel :</span><span class="sxs-lookup"><span data-stu-id="3736b-246">Here is an example command to save Skype for Business Online user data to a comma-separated values (CSV) file, a file that can be easily imported as a table in an Excel worksheet:</span></span>
  
```powershell
Get-CsOnlineUser | Select DisplayName, UserPrincipalName, UsageLocation | Export-Csv -Path "C:\Logs\SfBUsers.csv" -NoTypeInformation
```

<span data-ttu-id="3736b-247">Voici un exemple d’affichage :</span><span class="sxs-lookup"><span data-stu-id="3736b-247">Here is an example of the display:</span></span>
  
![Exemple de table importée dans une feuille de calcul Excel pour des données Skype Entreprise Online qui ont été enregistrées dans un fichier de valeurs séparées par des virgules (CSV).](../media/o365-powershell-data-in-excel.png)
  
> [!TIP]
>  <span data-ttu-id="3736b-249">L’interprétation de cette commande PowerShell est : obtenir tous les utilisateurs de Skype entreprise Online dans l’abonnement Microsoft 365 actuel ( **Get-CsOnlineUser** ), obtenir uniquement le nom d’utilisateur, l’UPN et l’emplacement ( **Select DisplayName, userPrincipalName, UsageLocation** ), puis enregistrer ces informations dans le fichier CSV nommé C : \\ logs \\SfBUsers.csv ( **Export-CSV-path "C : \\ logs \\SfBUsers.csv"-NoTypeInformation** ).</span><span class="sxs-lookup"><span data-stu-id="3736b-249">The interpretation of this PowerShell command is: Get all of the Skype for Business Online users in the current Microsoft 365 subscription ( **Get-CsOnlineUser** ), obtain only the user name, UPN, and location ( **Select DisplayName, UserPrincipalName, UsageLocation** ), and then save that information in CSV file named C:\\Logs\\SfBUsers.csv ( **Export-Csv -Path "C:\\Logs\\SfBUsers.csv" -NoTypeInformation** ).</span></span>
  
<span data-ttu-id="3736b-p131">Vous pouvez également utiliser des options pour enregistrer cette liste sous forme de fichier XML ou de page HTML. En fait, avec les commandes PowerShell supplémentaires, vous pouvez l’enregistrer directement dans un fichier Excel, avec la mise en forme personnalisée de votre choix.</span><span class="sxs-lookup"><span data-stu-id="3736b-p131">You can also use options to save this list as an XML file or as an HTML page. In fact, with additional PowerShell commands, you could save it directly as an Excel file, with any custom formatting you desire.</span></span> 
  
<span data-ttu-id="3736b-252">Vous pouvez également envoyer la sortie d’une commande PowerShell qui affiche une liste directement sur l’imprimante par défaut dans Windows.</span><span class="sxs-lookup"><span data-stu-id="3736b-252">You can also send the output of a PowerShell command that displays a list directly to the default printer in Windows.</span></span> <span data-ttu-id="3736b-253">Voici un exemple de commande :</span><span class="sxs-lookup"><span data-stu-id="3736b-253">Here is an example command:</span></span>
  
```powershell
Get-CsOnlineUser | Select DisplayName, UserPrincipalName, UsageLocation | Out-Printer
```

<span data-ttu-id="3736b-254">Le document imprimé aura l'apparence suivante :</span><span class="sxs-lookup"><span data-stu-id="3736b-254">Here's what your printed document will look like:</span></span>
  
![Exemple de document imprimé correspondant à la sortie d’une commande PowerShell indiquée directement sur l’imprimante par défaut dans Windows.](../media/o365-powershell-printed-data.png)
  
> [!TIP]
>  <span data-ttu-id="3736b-256">L’interprétation de cette commande PowerShell est la suivante : obtenir tous les utilisateurs de Skype entreprise Online dans l’abonnement Microsoft 365 actuel, obtenir uniquement le nom d’utilisateur, l’UPN et l’emplacement, puis envoyer ces informations à l’imprimante Windows par défaut ( **out-Printer** ).</span><span class="sxs-lookup"><span data-stu-id="3736b-256">The interpretation of this PowerShell command is:  Get all of the Skype for Business Online users in the current Microsoft 365 subscription, obtain only the user name, UPN, and location, and then send that information to the default Windows printer ( **Out-Printer** ).</span></span>
  
<span data-ttu-id="3736b-257">Le document imprimé a la même mise en forme que l’affichage dans la fenêtre de commande PowerShell, mais une fois que vous avez créé une commande PowerShell pour répertorier ce dont vous avez besoin, ajoutez simplement **| Out-Printer** à la fin de la commande pour obtenir une copie matérielle.</span><span class="sxs-lookup"><span data-stu-id="3736b-257">The printed document has the same simple formatting as the display within the PowerShell command window, but once you have created a PowerShell command to list what you need, you just add **| Out-Printer** to the end of the command to get a hard copy to work from.</span></span>
  
## <a name="powershell-for-microsoft-365-lets-you-manage-across-server-products"></a><span data-ttu-id="3736b-258">PowerShell pour Microsoft 365 vous permet de gérer tous les produits serveur</span><span class="sxs-lookup"><span data-stu-id="3736b-258">PowerShell for Microsoft 365 lets you manage across server products</span></span>

<span data-ttu-id="3736b-259">Les différents composants qui composent Microsoft 365 sont conçus pour fonctionner ensemble.</span><span class="sxs-lookup"><span data-stu-id="3736b-259">The different components that make up Microsoft 365 are designed to work together.</span></span> <span data-ttu-id="3736b-260">Par exemple, supposons que vous ajoutez un nouvel utilisateur à Microsoft 365 et, lorsque vous le faites, vous spécifiez des informations telles que le service et le numéro de téléphone de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3736b-260">For example, suppose you add a new user to Microsoft 365 and, when you do, you specify such information as the user's department and phone number.</span></span> <span data-ttu-id="3736b-261">Ces informations seront disponibles si vous accédez aux informations de l’utilisateur à l’aide de l’un des services Microsoft 365 : Skype entreprise Online, Exchange ou SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="3736b-261">That information will then be available if you access the user's information using any of the Microsoft 365 services: Skype for Business Online, Exchange, or SharePoint Online.</span></span>
  
<span data-ttu-id="3736b-p134">Toutefois, ceci concerne les informations communes qui couvrent une suite de produits. Les informations propres à un produit (par exemple, des informations sur la boîte aux lettres Exchange d'un utilisateur) ne sont généralement pas disponibles dans la suite. Par exemple, si vous voulez savoir si la boîte aux lettres d'un utilisateur est activée ou non, cette information est disponible uniquement dans le Centre d'administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="3736b-p134">But that's for common information that spans the suite of products. Product-specific information-for example, information about a user's Exchange mailbox-is typically not available across the suite. For example, if you want to know if a user's mailbox is enabled or not, that information is available only in the Exchange Admin center.</span></span> 
  
<span data-ttu-id="3736b-265">Supposons que vous souhaitiez établir un rapport qui présente les informations suivantes pour tous les utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="3736b-265">Suppose you'd like to make a report that shows the following information for all your users:</span></span>
  
- <span data-ttu-id="3736b-266">Nom complet de l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="3736b-266">The user's display name</span></span>
    
- <span data-ttu-id="3736b-267">Si l’utilisateur est titulaire d’une licence pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3736b-267">Whether the user is licensed for Microsoft 365</span></span>
    
- <span data-ttu-id="3736b-268">Si la boîte aux lettres Exchange de l'utilisateur a été activée</span><span class="sxs-lookup"><span data-stu-id="3736b-268">Whether the user's Exchange mailbox has been enabled</span></span>
    
- <span data-ttu-id="3736b-269">Si l'utilisateur est activé pour Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="3736b-269">Whether the user is enabled for Skype for Business Online</span></span>
    
<span data-ttu-id="3736b-270">Actuellement, vous ne pouvez pas utiliser le centre d’administration Microsoft 365 pour produire un tel rapport.</span><span class="sxs-lookup"><span data-stu-id="3736b-270">You currently cannot use the Microsoft 365 admin center to easily produce such a report.</span></span> <span data-ttu-id="3736b-271">Au lieu de cela, vous devrez créer un document distinct pour stocker les informations, comme une feuille de calcul Excel, et obtenir tous les noms d’utilisateur et les informations de licence à partir du centre d’administration 365 de Microsoft, obtenir des informations de boîte aux lettres à partir du centre d’administration Exchange, obtenir des informations Skype entreprise Online à partir du centre d’administration Skype entreprise Online, puis assembler</span><span class="sxs-lookup"><span data-stu-id="3736b-271">Instead, you'll have to create a separate document to store the information, like an Excel worksheet, and get all the user names and licensing information from the Microsoft 365 admin center, get mailbox information from the Exchange Admin center, get Skype for Business Online information from the Skype for Business Online Admin center, and then collate and combine that information.</span></span>
  
<span data-ttu-id="3736b-272">L’alternative consiste à utiliser un script PowerShell pour compiler ce rapport pour vous.</span><span class="sxs-lookup"><span data-stu-id="3736b-272">The alternative is to use a PowerShell script to compile that report for you.</span></span>
  
<span data-ttu-id="3736b-273">L'exemple de script suivant est plus complexe que les commandes que vous avez vues jusqu'à présent dans cet article.</span><span class="sxs-lookup"><span data-stu-id="3736b-273">The following example script is more complicated than the commands you have seen so far in this article.</span></span> <span data-ttu-id="3736b-274">Toutefois, il illustre la possibilité d’utiliser PowerShell pour créer des affichages d’informations qui sont très difficiles à faire autrement.</span><span class="sxs-lookup"><span data-stu-id="3736b-274">But, it shows the potential of using PowerShell to create views of information that are very difficult to do otherwise.</span></span> <span data-ttu-id="3736b-275">Voici le script qui peut compiler et afficher la liste nécessaire :</span><span class="sxs-lookup"><span data-stu-id="3736b-275">Here is the script that can compile and display the needed list:</span></span>
  
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

<span data-ttu-id="3736b-276">Voici un exemple d’affichage :</span><span class="sxs-lookup"><span data-stu-id="3736b-276">Here is an example of the display:</span></span>
  
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

<span data-ttu-id="3736b-277">L’interprétation de ce script PowerShell est la suivante :</span><span class="sxs-lookup"><span data-stu-id="3736b-277">The interpretation of this PowerShell script is:</span></span>  

- <span data-ttu-id="3736b-278">Obtenez tous les utilisateurs dans l’abonnement Microsoft 365 actuel et stockez les informations dans une variable nommée $x ( **$x = Get-AzureADUser** ).</span><span class="sxs-lookup"><span data-stu-id="3736b-278">Get all of the users in the current Microsoft 365 subscription and store the information in a variable named $x ( **$x = Get-AzureADUser** ).</span></span>
- <span data-ttu-id="3736b-279">Démarre une boucle qui s’exécute sur tous les utilisateurs dans la variable nommée $x ( **foreach ($i in $x)** ).</span><span class="sxs-lookup"><span data-stu-id="3736b-279">Start a loop that runs over all the users in the variable named $x ( **foreach ($i in $x)** ).</span></span>  
- <span data-ttu-id="3736b-280">Définit une variable nommée $y et y stocke des informations sur la boîte aux lettres de l’utilisateur ( **$y = Get-Mailbox -Identity $i.UserPrincipalName** ).</span><span class="sxs-lookup"><span data-stu-id="3736b-280">Define a variable named $y and store the user's mailbox information in it ( **$y = Get-Mailbox -Identity $i.UserPrincipalName** ).</span></span>
- <span data-ttu-id="3736b-281">Ajoute une nouvelle propriété dans les informations utilisateur nommée IsMailBoxEnabled et la définit sur la valeur de la propriété IsMailBoxEnabled de la boîte aux lettres de l’utilisateur ( **$i | Add-Member -MemberType NoteProperty -Name IsMailboxEnabled -Value $y.IsMailboxEnabled** ).</span><span class="sxs-lookup"><span data-stu-id="3736b-281">Add a new property to the user information named IsMailBoxEnabled and set it to the value of the IsMailBoxEnabled property of the user's mailbox ( **$i | Add-Member -MemberType NoteProperty -Name IsMailboxEnabled -Value $y.IsMailboxEnabled** ).</span></span>
- <span data-ttu-id="3736b-282">Définit une variable nommée $y et y stocke les informations Skype Entreprise Online de l’utilisateur ( **$y = Get-CsOnlineUser -Identity $i.UserPrincipalName** ).</span><span class="sxs-lookup"><span data-stu-id="3736b-282">Define a variable named $y and store the user's Skype for Business Online information in it ( **$y = Get-CsOnlineUser -Identity $i.UserPrincipalName** ).</span></span>
- <span data-ttu-id="3736b-283">Ajoute une nouvelle propriété dans les informations utilisateur nommée EnabledForSfB et la définit sur la valeur de la propriété Enabled des informations Skype Entreprise Online ( **$i | Add-Member -MemberType NoteProperty -Name EnabledForSfB -Value $y.Enabled** ).</span><span class="sxs-lookup"><span data-stu-id="3736b-283">Add a new property to the user information named EnabledForSfB and set it to the value of the Enabled property of the user's Skype for Business Online information ( **$i | Add-Member -MemberType NoteProperty -Name EnabledForSfB -Value $y.Enabled** ).</span></span>
- <span data-ttu-id="3736b-284">Affiche la liste des utilisateurs, mais indique uniquement leur nom, s’ils disposent d’une licence, et les deux nouvelles propriétés qui spécifient si leur boîte aux lettres est activée et si elles sont activées pour Skype Entreprise Online ( **$x | Select DisplayName, IsLicensed, IsMailboxEnabled, EnabledforSfB** ).</span><span class="sxs-lookup"><span data-stu-id="3736b-284">Display the list of users, but include only their name, whether they are licensed, and the two new properties that indicate whether their mailbox is enabled and whether they are enabled for Skype for Business Online ( **$x | Select DisplayName, IsLicensed, IsMailboxEnabled, EnabledforSfB** ).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3736b-285">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3736b-285">See also</span></span>

[<span data-ttu-id="3736b-286">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3736b-286">Getting started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="3736b-287">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="3736b-287">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="3736b-288">Utilisez Windows PowerShell pour créer des rapports dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3736b-288">Use Windows PowerShell to create reports in Microsoft 365</span></span>](use-windows-powershell-to-create-reports-in-microsoft-365.md)

