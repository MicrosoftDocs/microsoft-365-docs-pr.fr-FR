---
title: Importation en bloc de contacts externes dans Exchange Online
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
audience: End User
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOP150
ms.assetid: bed936bc-0969-4a6d-a7a5-66305c14e958
description: Découvrez comment les administrateurs peuvent utiliser Exchange Online PowerShell et un fichier CSV pour importer en bloc des contacts externes dans la liste d’adresses globale.
ms.openlocfilehash: 178e3676f8dc5fb59cdad9cc46d7ecbd9dddb90e
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50918210"
---
# <a name="bulk-import-external-contacts-to-exchange-online"></a><span data-ttu-id="72813-103">Importation en bloc de contacts externes dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="72813-103">Bulk import external contacts to Exchange Online</span></span>

<span data-ttu-id="72813-104">**Cet article est pour les administrateurs. Essayez-vous d’importer des contacts dans votre propre boîte aux lettres ? Voir [Importer des contacts dans Outlook](https://support.office.com/article/bb796340-b58a-46c1-90c7-b549b8f3c5f8)**</span><span class="sxs-lookup"><span data-stu-id="72813-104">**This article is for administrators. Are you trying to import contacts to your own mailbox? See [Import contacts to Outlook](https://support.office.com/article/bb796340-b58a-46c1-90c7-b549b8f3c5f8)**</span></span>
   
<span data-ttu-id="72813-105">Votre entreprise a-t-elle de nombreux contacts professionnels existants que vous souhaitez inclure dans le carnet d’adresses partagé (également appelé liste d’adresses globale) dans Exchange Online ?</span><span class="sxs-lookup"><span data-stu-id="72813-105">Does your company have lots of existing business contacts that you want to include in the shared address book (also called the global address list) in Exchange Online?</span></span> <span data-ttu-id="72813-106">Souhaitez-vous ajouter des contacts externes en tant que membres de groupes de distribution, comme vous le pouvez avec des utilisateurs au sein de votre entreprise ?</span><span class="sxs-lookup"><span data-stu-id="72813-106">Do you want to add external contacts as members of distribution groups, just like you can with users inside your company?</span></span> <span data-ttu-id="72813-107">Si c’est le cas, vous pouvez utiliser Exchange Online PowerShell et un fichier CSV (valeurs séparées par des virgules) pour importer en bloc des contacts externes dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="72813-107">If so, you can use Exchange Online PowerShell and a CSV (comma-separated value) file to bulk import external contacts into Exchange Online.</span></span> <span data-ttu-id="72813-108">Il s’agit d’un processus en trois étapes :</span><span class="sxs-lookup"><span data-stu-id="72813-108">It's a three-step process:</span></span>
  
[<span data-ttu-id="72813-109">Étape 1 : Créer un fichier CSV qui contient des informations sur les contacts externes</span><span class="sxs-lookup"><span data-stu-id="72813-109">Step 1: Create a CSV file that contains information about the external contacts</span></span>](#step-1-create-a-csv-file-that-contains-information-about-the-external-contacts)

[<span data-ttu-id="72813-110">Étape 2 : Créer les contacts externes avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="72813-110">Step 2: Create the external contacts with PowerShell</span></span>](#step-2-create-the-external-contacts-with-powershell) 

[<span data-ttu-id="72813-111">Étape 3 : Ajouter des informations aux propriétés des contacts externes</span><span class="sxs-lookup"><span data-stu-id="72813-111">Step 3: Add information to the properties of the external contacts</span></span>](#step-3-add-information-to-the-properties-of-the-external-contacts)

<span data-ttu-id="72813-112">Une fois que vous avez effectué ces étapes pour importer des contacts, vous pouvez effectuer les tâches supplémentaires suivantes :</span><span class="sxs-lookup"><span data-stu-id="72813-112">After you complete these steps to import contacts, you can perform these additional tasks:</span></span>
  
- [<span data-ttu-id="72813-113">Ajouter des contacts externes</span><span class="sxs-lookup"><span data-stu-id="72813-113">Add more external contacts</span></span>](#add-more-external-contacts)
  
- [<span data-ttu-id="72813-114">Masquer les contacts externes dans le carnet d’adresses partagé</span><span class="sxs-lookup"><span data-stu-id="72813-114">Hide external contacts from the shared address book</span></span>](#hide-external-contacts-from-the-shared-address-book)
  
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-external-contacts"></a><span data-ttu-id="72813-115">Étape 1 : Créer un fichier CSV qui contient des informations sur les contacts externes</span><span class="sxs-lookup"><span data-stu-id="72813-115">Step 1: Create a CSV file that contains information about the external contacts</span></span>

<span data-ttu-id="72813-116">La première étape consiste à créer un fichier CSV qui contient des informations sur chaque contact externe que vous souhaitez importer dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="72813-116">The first step is to create a CSV file that contains information about each external contact that you want to import to Exchange Online.</span></span> 
  
1. <span data-ttu-id="72813-117">Copiez le texte suivant dans un fichier texte dans le Bloc-notes et enregistrez-le sur votre bureau en tant que fichier CSV à l’aide du suffixe de nom de fichier .csv . par exemple, ExternalContacts.csv.</span><span class="sxs-lookup"><span data-stu-id="72813-117">Copy the following text to a text file in NotePad, and save it on your desktop as a CSV file by using a filename suffix of .csv; for example, ExternalContacts.csv.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="72813-118">Si votre langue contient des caractères spéciaux (par exemple, **å**, **ä** et **ö** en suédois), enregistrez le fichier CSV avec UTF-8 ou un autre codage Unicode lorsque vous enregistrez le fichier dans le Bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="72813-118">If your language contains special characters (such as **å**, **ä**, and **ö** in Swedish) save the CSV file with UTF-8 or other Unicode encoding when you save the file in NotePad.</span></span> 
  
    ```text
    ExternalEmailAddress,Name,FirstName,LastName,StreetAddress,City,StateorProvince,PostalCode,Phone,MobilePhone,Pager,HomePhone,Company,Title,OtherTelephone,Department,CountryOrRegion,Fax,Initials,Notes,Office,Manager
    danp@fabrikam.com,Dan Park,Dan,Park,1234 23rd Ave,Golden,CO,80215,206-111-1234,303-900-1234,555-1212,123-456-7890,Fabrikam,Shipping clerk,555-5555,Shipping,US,123-4567,R.,Good worker,31/1663,Dan Park
    pilar@contoso.com,Pilar Pinilla,Pilar,Pinilla,1234 Main St.,Seattle,WA,98017,206-555-0100,206-555-0101,206-555-0102,206-555-1234,Contoso,HR Manager,206-555-0104,Executive,US,206-555-0105,P.,Technical decision maker,31/1000,Dan Park
    ```

    <span data-ttu-id="72813-119">La première ligne, ou ligne d’en-tête, du fichier CSV répertorie les propriétés des contacts qui peuvent être utilisées lorsque vous les importez dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="72813-119">The first row, or header row, of the CSV file lists the properties of contacts that can be used when you import them to Exchange Online.</span></span> <span data-ttu-id="72813-120">Chaque nom de propriété est séparé par une virgule.</span><span class="sxs-lookup"><span data-stu-id="72813-120">Each property name is separated by a comma.</span></span> <span data-ttu-id="72813-121">Chaque ligne sous la ligne d’en-tête représente les valeurs de propriété pour l’importation d’un contact externe unique.</span><span class="sxs-lookup"><span data-stu-id="72813-121">Each row under the header row represents the property values for importing a single external contact.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="72813-122">Ce texte inclut des exemples de données que vous pouvez supprimer.</span><span class="sxs-lookup"><span data-stu-id="72813-122">This text includes sample data, which you can delete.</span></span> <span data-ttu-id="72813-123">Mais ne supprimez pas ou ne modifiez pas la première ligne (en-tête).</span><span class="sxs-lookup"><span data-stu-id="72813-123">But don't delete or change the first (header) row.</span></span> <span data-ttu-id="72813-124">Il contient toutes les propriétés des contacts externes.</span><span class="sxs-lookup"><span data-stu-id="72813-124">It contains all of the properties for the external contacts.</span></span> 
  
2. <span data-ttu-id="72813-125">Ouvrez le fichier CSV dans Microsoft Excel pour modifier le fichier CSV, car il est beaucoup plus facile d’utiliser Excel pour modifier le fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="72813-125">Open the CSV file in Microsoft Excel to edit the CSV file because it's much easier to use Excel to edit the CSV file.</span></span>
    
3. <span data-ttu-id="72813-126">Créez une ligne pour chaque contact que vous souhaitez importer dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="72813-126">Create a row for each contact that you want to import to Exchange Online.</span></span> <span data-ttu-id="72813-127">Remplir autant de cellules que possible.</span><span class="sxs-lookup"><span data-stu-id="72813-127">Populate as many of the cells as possible.</span></span> <span data-ttu-id="72813-128">Ces informations s’affichent dans le carnet d’adresses partagé pour chaque contact.</span><span class="sxs-lookup"><span data-stu-id="72813-128">This information will be displayed in the shared address book for each contact.</span></span> 
    
    > [!IMPORTANT]
    >  <span data-ttu-id="72813-129">Les propriétés suivantes (qui sont les quatre premiers éléments de la ligne d’en-tête) sont requises pour créer un contact externe et doivent être remplies dans le fichier CSV : **ExternalEmailAddress**, **Name**, **FirstName**, **LastName**.</span><span class="sxs-lookup"><span data-stu-id="72813-129">The following properties (which are the first four items in the header row) are required to create an external contact and must be populated in the CSV file: **ExternalEmailAddress**, **Name**, **FirstName**, **LastName**.</span></span> <span data-ttu-id="72813-130">La commande PowerShell que vous exécutez à l’étape 2 utilise les valeurs de ces propriétés pour créer les contacts.</span><span class="sxs-lookup"><span data-stu-id="72813-130">The PowerShell command that you run in Step 2 will use the values for these properties to create the contacts.</span></span> 

## <a name="step-2-create-the-external-contacts-with-powershell"></a><span data-ttu-id="72813-131">Étape 2 : Créer les contacts externes avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="72813-131">Step 2: Create the external contacts with PowerShell</span></span>

<span data-ttu-id="72813-132">L’étape suivante consiste à utiliser le fichier CSV que vous avez créé à l’étape 1 et PowerShell pour importer en bloc les contacts externes répertoriés dans le fichier CSV dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="72813-132">The next step is to use the CSV file that you created in Step 1 and PowerShell to bulk import the external contacts listed in the CSV file to Exchange Online.</span></span> 
  
1.  <span data-ttu-id="72813-133">Connectez PowerShell à votre organisation Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="72813-133">Connect PowerShell to your Exchange Online organization.</span></span> <span data-ttu-id="72813-134">Pour obtenir des instructions, consultez [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="72813-134">For step-by-step instructions, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="72813-135">N’oubliez pas d’utiliser le nom d’utilisateur et le mot de passe de votre compte d’administrateur général lorsque vous vous connectez à Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="72813-135">Be sure to use the user name and password for your global administrator account when you connect to Exchange Online PowerShell.</span></span> 
    
2. <span data-ttu-id="72813-136">Après avoir connecté PowerShell à Exchange Online, allez dans le dossier de bureau où vous avez enregistré le fichier CSV à l’étape 1 . par `C:\Users\Administrator\desktop` exemple.</span><span class="sxs-lookup"><span data-stu-id="72813-136">After you connect PowerShell to Exchange Online, go to the desktop folder where you saved the CSV file in Step 1; for example `C:\Users\Administrator\desktop`.</span></span>
    
3. <span data-ttu-id="72813-137">Exécutez la commande suivante pour créer les contacts externes :</span><span class="sxs-lookup"><span data-stu-id="72813-137">Run the following command to create the external contacts:</span></span>

    ```powershell
    Import-Csv .\ExternalContacts.csv|%{New-MailContact -Name $_.Name -DisplayName $_.Name -ExternalEmailAddress $_.ExternalEmailAddress -FirstName $_.FirstName -LastName $_.LastName}
    ```

    <span data-ttu-id="72813-138">La création des contacts peut prendre un certain temps, en fonction du nombre que vous importez.</span><span class="sxs-lookup"><span data-stu-id="72813-138">It might take a while to create the new contacts, depending on how many you're importing.</span></span> <span data-ttu-id="72813-139">Lorsque l’exécution de la commande est terminée, PowerShell affiche la liste des nouveaux contacts qui ont été créés.</span><span class="sxs-lookup"><span data-stu-id="72813-139">When the command is finished running, PowerShell displays a list of the new contacts that were created.</span></span> 
    
4. <span data-ttu-id="72813-140">Pour afficher les nouveaux contacts externes, go to the Exchange admin center (EAC), and then click **Recipients** \> **Contacts**.</span><span class="sxs-lookup"><span data-stu-id="72813-140">To view the new external contacts, go to the Exchange admin center (EAC), and then click **Recipients** \> **Contacts**.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="72813-141">Pour obtenir des instructions sur la connexion au CENTRE d’administration Exchange, consultez le Centre [d’administration Exchange dans Exchange Online.](/exchange/exchange-admin-center)</span><span class="sxs-lookup"><span data-stu-id="72813-141">For instructions for connecting to the EAC, see [Exchange admin center in Exchange Online](/exchange/exchange-admin-center).</span></span> 
  
5. <span data-ttu-id="72813-142">Si nécessaire, cliquez sur **Actualiser** pour mettre à jour la liste et voir les contacts externes qui ont été importés.</span><span class="sxs-lookup"><span data-stu-id="72813-142">If necessary, click **Refresh** to update the list and see the external contacts that were imported.</span></span> 
    
    <span data-ttu-id="72813-143">Les contacts importés apparaissent dans le carnet d’adresses partagé dans Outlook et Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="72813-143">The imported contacts will appear in the shared address book in Outlook and Outlook on the web.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="72813-144">Vous pouvez également afficher les contacts dans le Centre d’administration Microsoft 365 en allant **à** \> **Contacts des utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="72813-144">You can also view the contacts in the Microsoft 365 admin center by going to **Users** \> **Contacts**.</span></span> 

## <a name="step-3-add-information-to-the-properties-of-the-external-contacts"></a><span data-ttu-id="72813-145">Étape 3 : Ajouter des informations aux propriétés des contacts externes</span><span class="sxs-lookup"><span data-stu-id="72813-145">Step 3: Add information to the properties of the external contacts</span></span>

<span data-ttu-id="72813-146">Après avoir exécuté la commande à l’étape 2, les contacts externes sont créés, mais ils ne contiennent aucune information de contact ou d’organisation, c’est-à-dire les informations de la plupart des cellules du fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="72813-146">After you run the command in Step 2, the external contacts are created, but they don't contain any of the contact or organization information, which is the information from most of the cells in the CSV file.</span></span> <span data-ttu-id="72813-147">En effet, lorsque vous créez de nouveaux contacts externes, seules les propriétés requises sont remplies.</span><span class="sxs-lookup"><span data-stu-id="72813-147">This is because when you create new external contacts, only the required properties are populated.</span></span> <span data-ttu-id="72813-148">Ne vous inquiétez pas si vous n’avez pas toutes les informations remplies dans le fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="72813-148">Don't worry if you don't have all the information populated in the CSV file.</span></span> <span data-ttu-id="72813-149">S’il n’est pas là, il ne sera pas ajouté.</span><span class="sxs-lookup"><span data-stu-id="72813-149">If it's not there, it won't be added.</span></span>
  
1.  <span data-ttu-id="72813-150">Connectez PowerShell à votre organisation Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="72813-150">Connect PowerShell to your Exchange Online organization.</span></span> <span data-ttu-id="72813-151">Pour obtenir des instructions, consultez [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="72813-151">For step-by-step instructions, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>
    
2. <span data-ttu-id="72813-152">Go to the desktop folder where you saved the CSV file in Step 1; par exemple, `C:\Users\Administrator\desktop` .</span><span class="sxs-lookup"><span data-stu-id="72813-152">Go to the desktop folder where you saved the CSV file in Step 1; for example, `C:\Users\Administrator\desktop`.</span></span>
    
3. <span data-ttu-id="72813-153">Exécutez les deux commandes suivantes pour ajouter les autres propriétés du fichier CSV aux contacts externes que vous avez créés à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="72813-153">Run the following two commands to add the other properties from the CSV file to the external contacts that you created in Step 2.</span></span>
    
    ```powershell
    $Contacts = Import-CSV .\ExternalContacts.csv
  
    ```

    ```powershell
    $contacts | ForEach {Set-Contact $_.Name -StreetAddress $_.StreetAddress -City $_.City -StateorProvince $_.StateorProvince -PostalCode $_.PostalCode -Phone $_.Phone -MobilePhone $_.MobilePhone -Pager $_.Pager -HomePhone $_.HomePhone -Company $_.Company -Title $_.Title -OtherTelephone $_.OtherTelephone -Department $_.Department -Fax $_.Fax -Initials $_.Initials -Notes  $_.Notes -Office $_.Office -Manager $_.Manager}
    ```

    > [!NOTE]
    > <span data-ttu-id="72813-154">Le  _paramètre Manager_ peut être problématique.</span><span class="sxs-lookup"><span data-stu-id="72813-154">The  _Manager_ parameter might be problematic.</span></span> <span data-ttu-id="72813-155">Si la cellule est vide dans le fichier CSV, vous obtenez une erreur et aucune information de propriété n’est ajoutée au contact.</span><span class="sxs-lookup"><span data-stu-id="72813-155">If the cell is blank in the CSV file, you will get an error and none of the property information will be added to the contact.</span></span> <span data-ttu-id="72813-156">Si vous n’avez pas besoin de spécifier un responsable, supprimez simplement  ` -Manager $_.Manager ` la commande PowerShell précédente.</span><span class="sxs-lookup"><span data-stu-id="72813-156">If you don't need to specify a manager, then just delete  ` -Manager $_.Manager ` from the previous PowerShell command.</span></span> 
  
    <span data-ttu-id="72813-157">Là encore, la mise à jour des contacts peut prendre un certain temps, en fonction du nombre d’importations à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="72813-157">Again, it might take a while to update the contacts, depending on how many you imported in Step 1.</span></span> 
    
4. <span data-ttu-id="72813-158">Pour vérifier que les propriétés ont été ajoutées aux contacts :</span><span class="sxs-lookup"><span data-stu-id="72813-158">To verify that the properties were added to the contacts:</span></span> 
    
1. <span data-ttu-id="72813-159">Dans le CAE, accédez à **Destinataires** \> **Contacts**.</span><span class="sxs-lookup"><span data-stu-id="72813-159">In the EAC, go to **Recipients** \> **Contacts**.</span></span>
    
2. <span data-ttu-id="72813-160">Cliquez sur un contact, puis cliquez sur **Modifier** ![ ](../media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) l’icône pour afficher les propriétés du contact.</span><span class="sxs-lookup"><span data-stu-id="72813-160">Click a contact and then click **Edit** ![Edit icon](../media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) to display the contact's properties.</span></span> 
    
<span data-ttu-id="72813-161">Voilà !</span><span class="sxs-lookup"><span data-stu-id="72813-161">That's it!</span></span> <span data-ttu-id="72813-162">Les utilisateurs peuvent voir les contacts et les informations supplémentaires dans le carnet d’adresses Outlook et Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="72813-162">Users can see the contacts and the additional information in the address book Outlook and Outlook on the web.</span></span>
  
## <a name="add-more-external-contacts"></a><span data-ttu-id="72813-163">Ajouter des contacts externes</span><span class="sxs-lookup"><span data-stu-id="72813-163">Add more external contacts</span></span>

<span data-ttu-id="72813-164">Vous pouvez répéter les étapes 1 à 3 pour ajouter de nouveaux contacts externes dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="72813-164">You can repeat Steps 1 through Step 3 to add new external contacts in Exchange Online.</span></span> <span data-ttu-id="72813-165">Vous ou les utilisateurs de votre entreprise pouvez simplement ajouter une nouvelle ligne dans le fichier CSV du nouveau contact.</span><span class="sxs-lookup"><span data-stu-id="72813-165">You or users in your company can just add a new row in the CSV file for the new contact.</span></span> <span data-ttu-id="72813-166">Vous pouvez ensuite exécuter les commandes PowerShell des étapes 2 et 3 pour créer et ajouter des informations aux nouveaux contacts.</span><span class="sxs-lookup"><span data-stu-id="72813-166">Then you can run the PowerShell commands from Step 2 and Step 3 to create and add information to the new contacts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="72813-167">Lorsque vous exécutez la commande pour créer de nouveaux contacts, vous pouvez obtenir une erreur vous disant que les contacts qui ont été créés précédemment existent déjà.</span><span class="sxs-lookup"><span data-stu-id="72813-167">When you run the command to create new contacts, you might get an error saying that the contacts that were created earlier already exist.</span></span> <span data-ttu-id="72813-168">Toutefois, tout contact ajouté au fichier CSV est créé.</span><span class="sxs-lookup"><span data-stu-id="72813-168">But any new contact added to the CSV file is created.</span></span> 
  
## <a name="hide-external-contacts-from-the-shared-address-book"></a><span data-ttu-id="72813-169">Masquer les contacts externes dans le carnet d’adresses partagé></span><span class="sxs-lookup"><span data-stu-id="72813-169">Hide external contacts from the shared address book></span></span>

<span data-ttu-id="72813-170">Certaines sociétés peuvent utiliser des contacts externes uniquement pour pouvoir être ajoutées en tant que membres de groupes de distribution.</span><span class="sxs-lookup"><span data-stu-id="72813-170">Some companies may use external contacts only so they can be added as members of distribution groups.</span></span> <span data-ttu-id="72813-171">Dans ce scénario, il se peut qu’ils souhaitent masquer les contacts externes dans le carnet d’adresses partagé.</span><span class="sxs-lookup"><span data-stu-id="72813-171">In this scenario, they may want to hide external contacts from the shared address book.</span></span> <span data-ttu-id="72813-172">Voici comment procéder :</span><span class="sxs-lookup"><span data-stu-id="72813-172">Here's how:</span></span>
  
1.  <span data-ttu-id="72813-173">Connectez PowerShell à votre organisation Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="72813-173">Connect PowerShell to your Exchange Online organization.</span></span> <span data-ttu-id="72813-174">Pour obtenir des instructions, consultez [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="72813-174">For step-by-step instructions, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>
    
2. <span data-ttu-id="72813-175">Pour masquer un contact externe unique, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="72813-175">To hide a single external contact, run the following command.</span></span>
    
    ```powershell
    Set-MailContact <external contact> -HiddenFromAddressListsEnabled $true 
    ```

    <span data-ttu-id="72813-176">Par exemple, pour masquer Pilar Pinilla dans le carnet d’adresses partagé, exécutez la commande ci-après :</span><span class="sxs-lookup"><span data-stu-id="72813-176">For example, to hide Pilar Pinilla from the shared address book, run this command:</span></span>

    ```powershell
    Set-MailContact "Pilar Pinilla" -HiddenFromAddressListsEnabled $true
    ```

3. <span data-ttu-id="72813-177">Pour masquer tous les contacts externes du carnet d’adresses partagé, exécutez la commande ci-après :</span><span class="sxs-lookup"><span data-stu-id="72813-177">To hide all external contacts from the shared address book, run this command:</span></span>

    ```powershell
    Get-Contact -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'MailContact')} | Set-MailContact -HiddenFromAddressListsEnabled $true  
    ```

<span data-ttu-id="72813-178">Une fois que vous les avez cachés, les contacts externes ne sont pas affichés dans le carnet d’adresses partagé, mais vous pouvez toujours les ajouter en tant que membres d’un groupe de distribution.</span><span class="sxs-lookup"><span data-stu-id="72813-178">After you hide them, external contacts aren't displayed in the shared address book, but you can still add them as members of a distribution group.</span></span>