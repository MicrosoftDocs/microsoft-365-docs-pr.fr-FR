---
title: Ajouter plusieurs utilisateurs en même temps à Microsoft 365 - Aide de l’administrateur
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
f1.keywords:
- CSH
ms.custom:
- Adm_O365
- O365P_AddUsersCSV
- O365M_AddUsersCSV
- O365E_AddUsersCSV
search.appverid:
- MET150
- MOP150
- MOE150
- MED150
- GMA150
- MBS150
- GEA150
- BCS160
description: 'Découvrez comment ajouter plusieurs utilisateurs à Microsoft 365 pour les entreprises à partir d’une liste dans une feuille de calcul ou un autre fichier au format CSV. Regardez une vidéo sur YouTube qui explique comment ajouter des comptes à Microsoft 365. À la fin de ce processus, chaque utilisateur ayant un compte aura une boîte aux lettres Microsoft 365. '
ms.openlocfilehash: 7629879990facbce57a6fbca1aa543471ad1b05b
ms.sourcegitcommit: 8849dd6f80217c29f427c7f008d918f30c792240
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/15/2021
ms.locfileid: "49877211"
---
# <a name="add-several-users-at-the-same-time-to-microsoft-365---admin-help"></a><span data-ttu-id="ee73f-105">Ajouter plusieurs utilisateurs en même temps à Microsoft 365 - Aide de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="ee73f-105">Add several users at the same time to Microsoft 365 - Admin Help</span></span>

<span data-ttu-id="ee73f-106">Chaque personne de votre équipe a besoin d’un compte d’utilisateur pour pouvoir se connecter et accéder aux services Microsoft 365, tels que le courrier électronique et Office.</span><span class="sxs-lookup"><span data-stu-id="ee73f-106">Each person on your team needs a user account before they can sign in and access Microsoft 365 services, such as email and Office.</span></span> <span data-ttu-id="ee73f-107">Si votre équipe compte de nombreux membres, vous pouvez ajouter tous leurs comptes simultanément à partir d'une feuille de calcul Excel ou d'un autre fichier enregistré au format CSV.</span><span class="sxs-lookup"><span data-stu-id="ee73f-107">If you have a lot of people, you can add their accounts all at once from an Excel spreadsheet or other file saved in CSV format.</span></span> <span data-ttu-id="ee73f-108">[Vous ne savez pas quel est le format CSV](add-several-users-at-the-same-time.md#not-sure-what-csv-format-is)?</span><span class="sxs-lookup"><span data-stu-id="ee73f-108">[Not sure what CSV format is](add-several-users-at-the-same-time.md#not-sure-what-csv-format-is)?</span></span>
  
> [!NOTE]
> <span data-ttu-id="ee73f-109">Si le nouveau Centre d’administration Microsoft 365 n’est pas celui que vous utilisez, vous pouvez l’activer en sélectionnant le bouton bascule **Essayer le nouveau Centre d’administration** situé en haut de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="ee73f-109">If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.</span></span>

## <a name="add-multiple-users-in-the-microsoft-365-admin-center"></a><span data-ttu-id="ee73f-110">Ajouter plusieurs utilisateurs dans le Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ee73f-110">Add multiple users in the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="ee73f-111">Connectez-vous à Microsoft 365 à l’aide de votre compte professionnel ou scolaire.</span><span class="sxs-lookup"><span data-stu-id="ee73f-111">Sign in to Microsoft 365 with your work or school account.</span></span>

2. <span data-ttu-id="ee73f-112">Dans le Centre d’administration, sélectionnez **Utilisateurs** \> **actifs.**</span><span class="sxs-lookup"><span data-stu-id="ee73f-112">In the admin center, choose **Users** \> **Active users**.</span></span>

3. <span data-ttu-id="ee73f-113">Sélectionnez **Ajouter plusieurs utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="ee73f-113">Select **Add multiple users**.</span></span>

4. <span data-ttu-id="ee73f-114">Dans le panneau **Importer plusieurs utilisateurs**, vous pouvez éventuellement télécharger un exemple de fichier CSV avec ou sans exemple de données inclus.</span><span class="sxs-lookup"><span data-stu-id="ee73f-114">On the **Import multiple users** panel, you can optionally download a sample CSV file with or without sample data filled in.</span></span>

    <span data-ttu-id="ee73f-115">Votre feuille de calcul doit inclure exactement les mêmes en-tête de colonne **que** l’exemple (nom d’utilisateur, prénom, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="ee73f-115">Your spreadsheet needs to include the **exact same column headings** as the sample one (User Name, First Name, and so on).</span></span> <span data-ttu-id="ee73f-116">Si vous utilisez le modèle, ouvrez-le dans un outil d’édition de texte, tel que le Bloc-notes, et envisagez de laisser seules toutes les données de la ligne 1 et d’entrer uniquement les données des lignes 2 et suivantes.</span><span class="sxs-lookup"><span data-stu-id="ee73f-116">If you use the template, open it in a text editing tool, like Notepad, and consider leaving all the data in row 1 alone, and only entering data in rows 2 and below.</span></span>

    <span data-ttu-id="ee73f-117">Votre feuille de calcul doit également inclure des valeurs pour le nom d'utilisateur (tel que alexandre@contoso.com) et un nom complet (tel que Alexandre Chauvin) pour chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ee73f-117">Your spreadsheet also needs to include values for the user name (like bob@contoso.com) and a display name (like Bob Kelly) for each user.</span></span>

  ```
  User Name,First Name,Last Name,Display Name,Job Title,Department,Office Number,Office Phone,Mobile Phone,Fax,Address,City,State or Province,ZIP or Postal Code,Country or Region
  chris@contoso.com,Chris,Green,Chris Green,IT Manager,Information Technology,123451,123-555-1211,123-555-6641,123-555-6700,1 Microsoft way,Redmond,Wa,98052,United States
  ben@contoso.com,Ben,Andrews,Ben Andrews,IT Manager,Information Technology,123452,123-555-1212,123-555-6642,123-555-6700,1 Microsoft way,Redmond,Wa,98052,United States
  david@contoso.com,David,Longmuir,David Longmuir,IT Manager,Information Technology,123453,123-555-1213,123-555-6643,123-555-6700,1 Microsoft way,Redmond,Wa,98052,United States
  cynthia@contoso.com,Cynthia,Carey,Cynthia Carey,IT Manager,Information Technology,123454,123-555-1214,123-555-6644,123-555-6700,1 Microsoft way,Redmond,Wa,98052,United States
  melissa@contoso.com,Melissa,MacBeth,Melissa MacBeth,IT Manager,Information Technology,123455,123-555-1215,123-555-6645,123-555-6700,1 Microsoft way,Redmond,Wa,98052,United States
  
  ```

5. <span data-ttu-id="ee73f-118">Entrez un chemin d'accès dans la zone, ou choisissez **Parcourir** pour accéder à l'emplacement du fichier CSV, puis sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="ee73f-118">Enter a file path into the box, or choose **Browse** to browse to the CSV file location, then choose **Verify**.</span></span>
  
    <span data-ttu-id="ee73f-p104">S'il existe des problèmes avec le fichier, ceux-ci s'affichent dans le panneau. Vous pouvez également télécharger un fichier journal.</span><span class="sxs-lookup"><span data-stu-id="ee73f-p104">If there are problems with the file, the problem is displayed in the panel. You can also download a log file.</span></span>

6. <span data-ttu-id="ee73f-121">Dans la boîte de dialogue **Définir les options utilisateur**, vous pouvez définir le statut de connexion et choisir la licence produit à affecter à tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ee73f-121">On the **Set user options** dialog you can set the sign-in status and choose the product license that will be assigned to all users.</span></span>

7. <span data-ttu-id="ee73f-122">Dans la boîte de dialogue **Affichez vos résultats**, vous pouvez choisir d'envoyer les résultats à vous-même ou à d'autres utilisateurs (les mots de passe seront au format texte brut). En outre, vous pouvez voir combien d'utilisateurs ont été créés et si vous avez besoin d'acheter des licences supplémentaires pour les attribuer à certains des nouveaux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ee73f-122">On the **View your result** dialog you can choose to send the results to either yourself or other users (passwords will be in plain text) and you can see how many users were created, and if you need to purchase more licenses to assign to some of the new users.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ee73f-123">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="ee73f-123">Next steps</span></span>

- <span data-ttu-id="ee73f-124">Maintenant que ces personnes ont des comptes, elles doivent télécharger et installer ou [réinstaller Microsoft 365 ou Office 2016](https://support.office.com/article/4414eaaf-0478-48be-9c42-23adc4716658)sur un PC ou Mac.</span><span class="sxs-lookup"><span data-stu-id="ee73f-124">Now that these people have accounts, they need to [Download and install or reinstall Microsoft 365 or Office 2016 on a PC or Mac](https://support.office.com/article/4414eaaf-0478-48be-9c42-23adc4716658).</span></span> <span data-ttu-id="ee73f-125">Chaque personne de votre équipe peut installer Microsoft 365 sur 5 PC ou Mac au plus.</span><span class="sxs-lookup"><span data-stu-id="ee73f-125">Each person on your team can install Microsoft 365 on up to 5 PCs or Macs.</span></span>

- <span data-ttu-id="ee73f-126">Chaque utilisateur peut également configurer des applications Office et du courrier électronique sur un [appareil mobile](https://support.office.com/article/7dabb6cb-0046-40b6-81fe-767e0b1f014f) sur 5 tablettes et 5 téléphones au plus, tels que des iPhone, des iPads et des téléphones et tablettes Android.</span><span class="sxs-lookup"><span data-stu-id="ee73f-126">Each person can also [Set up Office apps and email on a mobile device](https://support.office.com/article/7dabb6cb-0046-40b6-81fe-767e0b1f014f) on up to 5 tablets and 5 phones, such as iPhones, iPads, and Android phones and tablets.</span></span> <span data-ttu-id="ee73f-127">Ainsi, ils peuvent modifier des fichiers Office n’importe où.</span><span class="sxs-lookup"><span data-stu-id="ee73f-127">This way they can edit Office files from anywhere.</span></span>

    <span data-ttu-id="ee73f-128">Voir [Configurer Microsoft 365](https://support.office.com/article/6a3a29a0-e616-4713-99d1-15eda62d04fa) pour les entreprises pour obtenir une liste complète des étapes de configuration.</span><span class="sxs-lookup"><span data-stu-id="ee73f-128">See [Set up Microsoft 365 for business](https://support.office.com/article/6a3a29a0-e616-4713-99d1-15eda62d04fa) for an end-to-end list of the setup steps.</span></span>

## <a name="more-information-about-how-to-add-users-to-microsoft-365"></a><span data-ttu-id="ee73f-129">Plus d’informations sur l’ajout d’utilisateurs à Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ee73f-129">More information about how to add users to Microsoft 365</span></span>

### <a name="not-sure-what-csv-format-is"></a><span data-ttu-id="ee73f-130">Qu'est-ce que le format CSV ?</span><span class="sxs-lookup"><span data-stu-id="ee73f-130">Not sure what CSV format is?</span></span>

<span data-ttu-id="ee73f-p107">Un fichier CSV inclut des valeurs séparées par des virgules. Vous pouvez créer ou modifier un fichier comme celui-ci avec un éditeur de texte ou un tableur comme Excel.</span><span class="sxs-lookup"><span data-stu-id="ee73f-p107">A CSV file is a file with comma separated values. You can create or edit a file like this with any text editor or spreadsheet program, such as Excel.</span></span>
  
<span data-ttu-id="ee73f-133">Vous pouvez télécharger [cet exemple de feuille de calcul](https://www.microsoft.com/download/details.aspx?id=45485) pour commencer.</span><span class="sxs-lookup"><span data-stu-id="ee73f-133">You can download [this sample spreadsheet](https://www.microsoft.com/download/details.aspx?id=45485) as a starting point.</span></span> <span data-ttu-id="ee73f-134">N’oubliez pas que Microsoft 365 nécessite des en-tête de colonne dans la première ligne, donc ne les remplacez pas par autre chose.</span><span class="sxs-lookup"><span data-stu-id="ee73f-134">Remember that Microsoft 365 requires column headings in the first row so don't replace them with something else.</span></span> 
  
<span data-ttu-id="ee73f-135">Enregistrez le fichier avec un nouveau nom et spécifiez le format CSV.</span><span class="sxs-lookup"><span data-stu-id="ee73f-135">Save the file with a new name, and specify CSV format.</span></span>
  
![Image expliquant comment enregistrer un fichier au format CSV dans Excel](../media/35a86ebe-63ab-4b4d-9a92-e177de33ebae.png)
  
<span data-ttu-id="ee73f-p109">Une fois le fichier enregistré, il est probable qu'un message indiquant que certaines fonctionnalités de votre classeur seront perdues si vous enregistrez le fichier au format CSV s'affiche. Ceci est normal. Cliquez sur **Oui** pour continuer.</span><span class="sxs-lookup"><span data-stu-id="ee73f-p109">When you save the file, you'll probably get a prompt that some features in your workbook will be lost if you save the file in CSV format. This is okay. Click **Yes** to continue.</span></span>
  
![Image de l'invite rencontrée dans Excel vous demandant si vous voulez vraiment enregistrer le fichier au format CSV](../media/51032a81-690c-45ef-bfc5-09ea7f790e98.png)
  
### <a name="tips-for-formatting-your-spreadsheet"></a><span data-ttu-id="ee73f-141">Conseils pour la mise en forme de votre feuille de calcul</span><span class="sxs-lookup"><span data-stu-id="ee73f-141">Tips for formatting your spreadsheet</span></span>

- <span data-ttu-id="ee73f-142">**Ai-je besoin des mêmes en-têtes de colonne que dans l'exemple de feuille de calcul ?**</span><span class="sxs-lookup"><span data-stu-id="ee73f-142">**Do I need the same column headings as in the sample spreadsheet?**</span></span> <span data-ttu-id="ee73f-143">Oui.</span><span class="sxs-lookup"><span data-stu-id="ee73f-143">Yes.</span></span> <span data-ttu-id="ee73f-144">La première ligne de l'exemple de feuille de calcul inclut les en-têtes de colonne.</span><span class="sxs-lookup"><span data-stu-id="ee73f-144">The sample spreadsheet contains column headings in the first row.</span></span> <span data-ttu-id="ee73f-145">Ces en-têtes sont obligatoires.</span><span class="sxs-lookup"><span data-stu-id="ee73f-145">These headings are required.</span></span> <span data-ttu-id="ee73f-146">Pour chaque utilisateur que vous souhaitez ajouter à Microsoft 365, créez une ligne sous le titre.</span><span class="sxs-lookup"><span data-stu-id="ee73f-146">For each user you want to add to Microsoft 365, create a row under the heading.</span></span> <span data-ttu-id="ee73f-147">Si vous ajoutez, modifiez ou supprimez des en-tête de colonne, Microsoft 365 risque de ne pas pouvoir créer d’utilisateurs à partir des informations du fichier.</span><span class="sxs-lookup"><span data-stu-id="ee73f-147">If you add, change, or delete any of the column headings, Microsoft 365 might not be able to create users from the information in the file.</span></span>

- <span data-ttu-id="ee73f-p111">**Que faire si je n'ai pas toutes les informations requises pour chaque utilisateur ?** Le nom de l'utilisateur et le nom d'affichage sont obligatoires. Vous ne pouvez pas ajouter un nouvel utilisateur sans ces informations. S'il vous manque d'autres informations, par exemple le numéro de télécopie, vous pouvez insérer un espace suivi d'une virgule pour indiquer que le champ est vide.</span><span class="sxs-lookup"><span data-stu-id="ee73f-p111">**What if I don't have all the information required for each user?** The user name and display name are required, and you cannot add a new user without this information. If you don't have some of the other information, such as the fax, you can use a space plus a comma to indicate that the field should remain blank.</span></span>

- <span data-ttu-id="ee73f-151">**Quelle peut être la taille de la feuille de calcul ?**</span><span class="sxs-lookup"><span data-stu-id="ee73f-151">**How small or large can the spreadsheet be?**</span></span> <span data-ttu-id="ee73f-152">La feuille de calcul doit avoir au moins deux lignes.</span><span class="sxs-lookup"><span data-stu-id="ee73f-152">The spreadsheet must have at least two rows.</span></span> <span data-ttu-id="ee73f-153">One is for the column headings (the user data column label) and one for the user.</span><span class="sxs-lookup"><span data-stu-id="ee73f-153">One is for the column headings (the user data column label) and one for the user.</span></span> <span data-ttu-id="ee73f-154">You cannot have more than 251 rows.</span><span class="sxs-lookup"><span data-stu-id="ee73f-154">You cannot have more than 251 rows.</span></span> <span data-ttu-id="ee73f-155">If you need to import more than 250 users, you can create more than one spreadsheet.</span><span class="sxs-lookup"><span data-stu-id="ee73f-155">If you need to import more than 250 users, you can create more than one spreadsheet.</span></span>

- <span data-ttu-id="ee73f-156">**Quelles langues puis-je utiliser ?**</span><span class="sxs-lookup"><span data-stu-id="ee73f-156">**What languages can I use?**</span></span> <span data-ttu-id="ee73f-157">Lorsque vous créez votre feuille de calcul, vous pouvez entrer des étiquettes de colonnes de données utilisateur dans n’importe quelle langue ou caractère, mais vous ne devez pas modifier l’ordre des étiquettes, comme illustré dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="ee73f-157">When you create your spreadsheet, you can enter user data column labels in any language or characters, but you must not change the order of the labels, as shown in the sample.</span></span> <span data-ttu-id="ee73f-158">You can then make entries into the fields, using any language or characters, and save your file in a Unicode or UTF-8 format.</span><span class="sxs-lookup"><span data-stu-id="ee73f-158">You can then make entries into the fields, using any language or characters, and save your file in a Unicode or UTF-8 format.</span></span>

- <span data-ttu-id="ee73f-p114">**Que dois-je faire si j'ajoute des utilisateurs de régions ou de pays différents ?** Créez une feuille de calcul distincte pour chaque zone. Vous devez exécuter l'Assistant Ajouter des utilisateurs en bloc avec chaque feuille de calcul, et donner ainsi un seul emplacement à tous les utilisateurs inclus dans le fichier que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="ee73f-p114">**What if I'm adding users from different countries or regions?** Create a separate spreadsheet for each area. You'll need to step through the Bulk add users wizard which each spreadsheet, giving a single location of all users included in the file that you're working with.</span></span>

- <span data-ttu-id="ee73f-p115">**Le nombre de caractères que je peux utiliser est-il limité ?** Le tableau suivant indique les étiquettes de colonne des données utilisateur et le nombre maximal de caractères autorisés pour chacune d'elles dans l'exemple de feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="ee73f-p115">**Is there a limit to the number of characters I can use?** The following table shows the user data column labels and the maximum character length for each in the sample spreadsheet.</span></span>

|<span data-ttu-id="ee73f-164">**Étiquette de colonne des données utilisateur**</span><span class="sxs-lookup"><span data-stu-id="ee73f-164">**User data column label**</span></span>|<span data-ttu-id="ee73f-165">**Longueur de caractères maximale**</span><span class="sxs-lookup"><span data-stu-id="ee73f-165">**Maximum character length**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ee73f-166">Nom d'utilisateur (requis)</span><span class="sxs-lookup"><span data-stu-id="ee73f-166">User Name (Required)</span></span>  <br/> |<span data-ttu-id="ee73f-167">79, y compris le signe at (@), au format name@domain. \<extension\> .</span><span class="sxs-lookup"><span data-stu-id="ee73f-167">79 including the at sign (@), in the format name@domain.\<extension\>.</span></span> <span data-ttu-id="ee73f-168">L’alias de l’utilisateur ne peut pas dépasser 50 caractères et le nom de domaine ne peut pas dépasser 48 caractères.</span><span class="sxs-lookup"><span data-stu-id="ee73f-168">The user's alias cannot exceed 50 characters, and the domain name cannot exceed 48 characters.</span></span>  <br/> |
|<span data-ttu-id="ee73f-169">Prénom</span><span class="sxs-lookup"><span data-stu-id="ee73f-169">First Name</span></span>  <br/> |<span data-ttu-id="ee73f-170">64</span><span class="sxs-lookup"><span data-stu-id="ee73f-170">64</span></span>  <br/> |
|<span data-ttu-id="ee73f-171">Nom</span><span class="sxs-lookup"><span data-stu-id="ee73f-171">Last Name</span></span>  <br/> |<span data-ttu-id="ee73f-172">64</span><span class="sxs-lookup"><span data-stu-id="ee73f-172">64</span></span>  <br/> |
|<span data-ttu-id="ee73f-173">Nom d'affichage (requis)</span><span class="sxs-lookup"><span data-stu-id="ee73f-173">Display Name (required)</span></span>  <br/> |<span data-ttu-id="ee73f-174">256</span><span class="sxs-lookup"><span data-stu-id="ee73f-174">256</span></span>  <br/> |
|<span data-ttu-id="ee73f-175">Poste</span><span class="sxs-lookup"><span data-stu-id="ee73f-175">Job Title</span></span>  <br/> |<span data-ttu-id="ee73f-176">64</span><span class="sxs-lookup"><span data-stu-id="ee73f-176">64</span></span>  <br/> |
|<span data-ttu-id="ee73f-177">Service</span><span class="sxs-lookup"><span data-stu-id="ee73f-177">Department</span></span>  <br/> |<span data-ttu-id="ee73f-178">64</span><span class="sxs-lookup"><span data-stu-id="ee73f-178">64</span></span>  <br/> |
|<span data-ttu-id="ee73f-179">Numéro du bureau</span><span class="sxs-lookup"><span data-stu-id="ee73f-179">Office Number</span></span>  <br/> |<span data-ttu-id="ee73f-180">128</span><span class="sxs-lookup"><span data-stu-id="ee73f-180">128</span></span>  <br/> |
|<span data-ttu-id="ee73f-181">Téléphone (bureau)</span><span class="sxs-lookup"><span data-stu-id="ee73f-181">Office Phone</span></span>  <br/> |<span data-ttu-id="ee73f-182">64</span><span class="sxs-lookup"><span data-stu-id="ee73f-182">64</span></span>  <br/> |
|<span data-ttu-id="ee73f-183">Téléphone mobile</span><span class="sxs-lookup"><span data-stu-id="ee73f-183">Mobile Phone</span></span>  <br/> |<span data-ttu-id="ee73f-184">64</span><span class="sxs-lookup"><span data-stu-id="ee73f-184">64</span></span>  <br/> |
|<span data-ttu-id="ee73f-185">Télécopie</span><span class="sxs-lookup"><span data-stu-id="ee73f-185">Fax</span></span>  <br/> |<span data-ttu-id="ee73f-186">64</span><span class="sxs-lookup"><span data-stu-id="ee73f-186">64</span></span>  <br/> |
|<span data-ttu-id="ee73f-187">Adresse</span><span class="sxs-lookup"><span data-stu-id="ee73f-187">Address</span></span>  <br/> |<span data-ttu-id="ee73f-188">1023</span><span class="sxs-lookup"><span data-stu-id="ee73f-188">1023</span></span>  <br/> |
|<span data-ttu-id="ee73f-189">Ville</span><span class="sxs-lookup"><span data-stu-id="ee73f-189">City</span></span>  <br/> |<span data-ttu-id="ee73f-190">128</span><span class="sxs-lookup"><span data-stu-id="ee73f-190">128</span></span>  <br/> |
|<span data-ttu-id="ee73f-191">Département ou région</span><span class="sxs-lookup"><span data-stu-id="ee73f-191">State or Province</span></span>  <br/> |<span data-ttu-id="ee73f-192">128</span><span class="sxs-lookup"><span data-stu-id="ee73f-192">128</span></span>  <br/> |
|<span data-ttu-id="ee73f-193">Code postal</span><span class="sxs-lookup"><span data-stu-id="ee73f-193">ZIP or Postal Code</span></span>  <br/> |<span data-ttu-id="ee73f-194">40</span><span class="sxs-lookup"><span data-stu-id="ee73f-194">40</span></span>  <br/> |
|<span data-ttu-id="ee73f-195">Pays ou région</span><span class="sxs-lookup"><span data-stu-id="ee73f-195">Country or Region</span></span>  <br/> |<span data-ttu-id="ee73f-196">128</span><span class="sxs-lookup"><span data-stu-id="ee73f-196">128</span></span>  <br/> |

### <a name="still-having-problems-when-adding-users-to-microsoft-365"></a><span data-ttu-id="ee73f-197">Vous avez encore des problèmes lors de l’ajout d’utilisateurs à Microsoft 365 ?</span><span class="sxs-lookup"><span data-stu-id="ee73f-197">Still having problems when adding users to Microsoft 365?</span></span>

- <span data-ttu-id="ee73f-p117">**Vérifiez que la feuille de calcul est correctement mise en forme.** Examinez les en-têtes des colonnes pour vous assurer qu'ils correspondent à ceux de l'exemple de fichier. Veillez à respecter le nombre de caractères autorisés et assurez-vous que chaque champ est séparé par une virgule.</span><span class="sxs-lookup"><span data-stu-id="ee73f-p117">**Double-check that the spreadsheet is formatted correctly.** Check the column headings to make sure they match the headings in the sample file. Make sure you're following the rules for character lengths and that each field is separated by a comma.</span></span>

- <span data-ttu-id="ee73f-201">**Si vous ne voyez pas les nouveaux utilisateurs dans Microsoft 365 immédiatement, patientez quelques minutes.**</span><span class="sxs-lookup"><span data-stu-id="ee73f-201">**If you don't see the new users in Microsoft 365 right away, wait a few minutes.**</span></span> <span data-ttu-id="ee73f-202">Les modifications apportées à tous les services dans Microsoft 365 peuvent prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="ee73f-202">It can take a little while for changes to go across all the services in Microsoft 365.</span></span> 

## <a name="related-articles"></a><span data-ttu-id="ee73f-203">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="ee73f-203">Related articles</span></span>

[<span data-ttu-id="ee73f-204">Ajouter des utilisateurs individuellement ou en bloc à Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ee73f-204">Add users individually or in bulk to Microsoft 365</span></span>](https://docs.microsoft.com/office365/admin/add-users/add-users)
