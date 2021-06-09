---
title: Supprimer un calendrier
ms.author: kwekua
author: kwekuako
manager: scotv
audience: Admin
ms.topic: article
ms.service: bookings
localization_priority: Normal
ms.assetid: 8c3a913c-2247-4519-894d-b6263eeb9920
description: Utilisez le centre Microsoft 365'administration ou Windows PowerShell pour supprimer des calendriers Bookings.
ms.openlocfilehash: 21fc7b9994ffd7f76ed04000a50bd0ee8f7f167e
ms.sourcegitcommit: 8998f70d3f7bd673f93f8d1cf12ce981b1b771c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51034090"
---
# <a name="delete-a-booking-calendar-in-bookings"></a><span data-ttu-id="e9ed1-103">Supprimer un calendrier de réservation dans Bookings</span><span class="sxs-lookup"><span data-stu-id="e9ed1-103">Delete a booking calendar in Bookings</span></span>

<span data-ttu-id="e9ed1-104">Cet article explique comment supprimer un calendrier de réservation indésirable.</span><span class="sxs-lookup"><span data-stu-id="e9ed1-104">This article explains how you can delete an unwanted booking calendar.</span></span> <span data-ttu-id="e9ed1-105">Vous pouvez supprimer le calendrier de réservation dans Microsoft 365'administration centrale ou vous pouvez utiliser PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e9ed1-105">You can delete the booking calendar in the Microsoft 365 admin center or you can use PowerShell.</span></span> <span data-ttu-id="e9ed1-106">Le calendrier Bookings est une boîte aux lettres dans Exchange Online vous supprimez le compte d’utilisateur correspondant pour supprimer le calendrier de réservation.</span><span class="sxs-lookup"><span data-stu-id="e9ed1-106">The Bookings calendar is a mailbox in Exchange Online so you delete the corresponding user account to delete the booking calendar.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e9ed1-107">Tous les calendriers de réservation que vous avez créés en 2017 ou avant doivent être supprimés à l’aide des instructions PowerShell de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="e9ed1-107">All booking calendars that you created in 2017 or before must be deleted using the PowerShell instructions on this topic.</span></span> <span data-ttu-id="e9ed1-108">Tous les calendriers de réservation créés en 2018 ou après peuvent être supprimés dans Microsoft 365'administration centrale.</span><span class="sxs-lookup"><span data-stu-id="e9ed1-108">All booking calendars created in 2018 or after can be deleted in the Microsoft 365 admin center.</span></span>

<span data-ttu-id="e9ed1-109">Le calendrier de réservation est l’endroit où sont stockées toutes les informations pertinentes sur ce calendrier de réservation et les données, notamment :</span><span class="sxs-lookup"><span data-stu-id="e9ed1-109">The booking calendar is where all relevant information about that booking calendar and data are stored, including:</span></span>

- <span data-ttu-id="e9ed1-110">Informations professionnelles, logo et heures de travail ajoutées lors de la création du calendrier de réservation</span><span class="sxs-lookup"><span data-stu-id="e9ed1-110">Business information, logo, and working hours added when the booking calendar was created</span></span>
- <span data-ttu-id="e9ed1-111">Personnel et services pertinents ajoutés lors de la création du calendrier de réservation</span><span class="sxs-lookup"><span data-stu-id="e9ed1-111">Relevant staff and services added when the booking calendar was created</span></span>
- <span data-ttu-id="e9ed1-112">Toutes les réservations et les congés ajoutés au calendrier de réservation une fois créés.</span><span class="sxs-lookup"><span data-stu-id="e9ed1-112">All bookings and time off appointments added to the booking calendar once it was created.</span></span>

> [!WARNING]
> <span data-ttu-id="e9ed1-113">Une fois qu’un calendrier de réservation est supprimé, ces informations supplémentaires sont également définitivement supprimées et ne peuvent pas être récupérées.</span><span class="sxs-lookup"><span data-stu-id="e9ed1-113">Once a booking calendar is deleted, this additional information is also permanently deleted and can't be recovered.</span></span>

## <a name="delete-a-booking-calendar-in-the-microsoft-365-admin-center"></a><span data-ttu-id="e9ed1-114">Supprimer un calendrier de réservation dans le centre d’administration Microsoft 365 de réservation</span><span class="sxs-lookup"><span data-stu-id="e9ed1-114">Delete a booking calendar in the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="e9ed1-115">Aller au Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="e9ed1-115">Go to the Microsoft 365 admin center.</span></span>

1. <span data-ttu-id="e9ed1-116">Dans le centre d'administration, sélectionnez **Utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="e9ed1-116">In the Admin center, select **Users**.</span></span>

   ![Image de l’interface utilisateur des utilisateurs Microsoft 365 centre d’administration](../media/bookings-admin-center-users.png)

1. <span data-ttu-id="e9ed1-118">Sur la page **Utilisateurs actifs**, sélectionnez les noms des utilisateurs à supprimer, puis **Supprimer l'utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="e9ed1-118">On the **Active Users** page, choose the names of the users that you want to delete, and then select **Delete user**.</span></span>

   ![Image de la suppression de l’interface utilisateur dans Microsoft 365'administration centrale](../media/bookings-delete-user.png)

## <a name="delete-a-booking-calendar-using-exchange-online-powershell"></a><span data-ttu-id="e9ed1-120">Supprimer un calendrier de réservation à l’Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="e9ed1-120">Delete a booking calendar using Exchange Online PowerShell</span></span>

<span data-ttu-id="e9ed1-121">Consultez [Connecter à Exchange Online PowerShell pour les](/powershell/exchange/exchange-online-powershell-v2?view=exchange-ps) conditions préalables et des instructions pour la connexion Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e9ed1-121">See [Connect to Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell-v2?view=exchange-ps) for prerequisites and guidance for connecting to Exchange Online PowerShell.</span></span>

<span data-ttu-id="e9ed1-122">Pour effectuer ces étapes, vous devez utiliser une fenêtre de commande Microsoft PowerShell active que vous avez exécutée en choisissant l’option « Exécuter en tant qu’administrateur ».</span><span class="sxs-lookup"><span data-stu-id="e9ed1-122">To perform these steps, you must be using an active Microsoft PowerShell command window that you ran by choosing the “Run as administrator” option.</span></span>

1. <span data-ttu-id="e9ed1-123">Dans une fenêtre PowerShell, chargez le module EXO V2 en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="e9ed1-123">In a PowerShell window, load the EXO V2 module by running the following command:</span></span>

   ```powershell
   Import-Module ExchangeOnlineManagement
   ```

   > [!NOTE]
   > <span data-ttu-id="e9ed1-124">Si vous avez déjà [installé le module EXO v2](/powershell/exchange/exchange-online-powershell-v2?view=exchange-ps#install-and-maintain-the-exo-v2-module), la commande précédente fonctionnera comme écrite.</span><span class="sxs-lookup"><span data-stu-id="e9ed1-124">If you've already [installed the EXO V2 module](/powershell/exchange/exchange-online-powershell-v2?view=exchange-ps#install-and-maintain-the-exo-v2-module), the previous command will work as written.</span></span>
   
2. <span data-ttu-id="e9ed1-125">La commande à exécuter utilise la syntaxe suivante:</span><span class="sxs-lookup"><span data-stu-id="e9ed1-125">The command that you need to run uses the following syntax:</span></span>

   ```powershell
   Connect-ExchangeOnline -UserPrincipalName <UPN> 
   ```

   - <span data-ttu-id="e9ed1-126">_\<UPN\>_ est votre compte au format du nom d’utilisateur principal (par exemple, `john@contoso.com`).</span><span class="sxs-lookup"><span data-stu-id="e9ed1-126">_\<UPN\>_ is your account in user principal name format (for example, `john@contoso.com`).</span></span>

3. <span data-ttu-id="e9ed1-127">Lorsque vous y êtes invité, connectez-vous avec les informations d’identification d’administrateur client au client Microsoft 365 qui héberge le calendrier de réservation que vous souhaitez supprimer définitivement.</span><span class="sxs-lookup"><span data-stu-id="e9ed1-127">When you are prompted, log on with tenant administrator credentials to the Microsoft 365 tenant that hosts the booking calendar you want to permanently delete.</span></span>

4. <span data-ttu-id="e9ed1-128">Une fois cette commande traitée, entrez la commande suivante pour obtenir la liste des boîtes aux lettres de réservation dans votre client :</span><span class="sxs-lookup"><span data-stu-id="e9ed1-128">Once this command is done processing, enter the following command to get a list of the booking mailboxes in your tenant:</span></span>

   ```powershell
   Get-EXOMailbox -RecipientTypeDetails SchedulingMailbox
   ```

5. <span data-ttu-id="e9ed1-129">Tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="e9ed1-129">Type the following command:</span></span>

   ```powershell
   remove-mailbox [BookingCalendarToDelete]
   ```

   > [!IMPORTANT]
   > <span data-ttu-id="e9ed1-130">Faites attention à taper le nom exact de l’alias de boîte aux lettres de réservation que vous souhaitez supprimer définitivement.</span><span class="sxs-lookup"><span data-stu-id="e9ed1-130">Be careful to type the exact name of the booking mailbox alias that you want to permanently delete.</span></span>

6. <span data-ttu-id="e9ed1-131">Pour vérifier que le calendrier a été supprimé, entrez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="e9ed1-131">To verify that the calendar has been deleted, enter the following command:</span></span>

   ```powershell
    Get-EXOMailbox -RecipientTypeDetails SchedulingMailbox
   ```

   <span data-ttu-id="e9ed1-132">Le calendrier supprimé n’apparaîtra pas dans la sortie.</span><span class="sxs-lookup"><span data-stu-id="e9ed1-132">The deleted calendar will not appear in the output.</span></span>
