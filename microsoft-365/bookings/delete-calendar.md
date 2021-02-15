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
description: Utilisez le Centre d’administration Microsoft 365 ou Windows PowerShell pour supprimer des calendriers Bookings.
ms.openlocfilehash: 2fcb92cee18d709ef0e1fa3faa0246e622a9f9db
ms.sourcegitcommit: 0402d3275632fceda9137b6abc3ce48c8020172a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/17/2020
ms.locfileid: "49126648"
---
# <a name="delete-a-booking-calendar-in-bookings"></a><span data-ttu-id="fcedb-103">Supprimer un calendrier de réservation dans Bookings</span><span class="sxs-lookup"><span data-stu-id="fcedb-103">Delete a booking calendar in Bookings</span></span>

<span data-ttu-id="fcedb-104">Cet article explique comment supprimer un calendrier de réservation indésirable.</span><span class="sxs-lookup"><span data-stu-id="fcedb-104">This article explains how you can delete an unwanted booking calendar.</span></span> <span data-ttu-id="fcedb-105">Vous pouvez supprimer le calendrier de réservation dans le Centre d’administration Microsoft 365 ou vous pouvez utiliser PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fcedb-105">You can delete the booking calendar in the Microsoft 365 admin center or you can use PowerShell.</span></span> <span data-ttu-id="fcedb-106">Le calendrier Bookings est une boîte aux lettres dans Exchange Online, vous supprimez le compte d’utilisateur correspondant pour supprimer le calendrier de réservation.</span><span class="sxs-lookup"><span data-stu-id="fcedb-106">The Bookings calendar is a mailbox in Exchange Online so you delete the corresponding user account to delete the booking calendar.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fcedb-107">Tous les calendriers de réservation que vous avez créés en 2017 ou avant doivent être supprimés à l’aide des instructions PowerShell de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="fcedb-107">All booking calendars that you created in 2017 or before must be deleted using the PowerShell instructions on this topic.</span></span> <span data-ttu-id="fcedb-108">Tous les calendriers de réservation créés en 2018 ou après peuvent être supprimés dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="fcedb-108">All booking calendars created in 2018 or after can be deleted in the Microsoft 365 admin center.</span></span>

<span data-ttu-id="fcedb-109">Le calendrier de réservation est l’endroit où sont stockées toutes les informations pertinentes sur ce calendrier de réservation et les données, notamment :</span><span class="sxs-lookup"><span data-stu-id="fcedb-109">The booking calendar is where all relevant information about that booking calendar and data are stored, including:</span></span>

- <span data-ttu-id="fcedb-110">Informations professionnelles, logo et heures de travail ajoutés lors de la création du calendrier de réservation</span><span class="sxs-lookup"><span data-stu-id="fcedb-110">Business information, logo, and working hours added when the booking calendar was created</span></span>
- <span data-ttu-id="fcedb-111">Personnel et services pertinents ajoutés lors de la création du calendrier de réservation</span><span class="sxs-lookup"><span data-stu-id="fcedb-111">Relevant staff and services added when the booking calendar was created</span></span>
- <span data-ttu-id="fcedb-112">Toutes les réservations et les congés ajoutés au calendrier de réservation une fois créés.</span><span class="sxs-lookup"><span data-stu-id="fcedb-112">All bookings and time off appointments added to the booking calendar once it was created.</span></span>

> [!WARNING]
> <span data-ttu-id="fcedb-113">Une fois qu’un calendrier de réservation est supprimé, ces informations supplémentaires sont également définitivement supprimées et ne peuvent pas être récupérées.</span><span class="sxs-lookup"><span data-stu-id="fcedb-113">Once a booking calendar is deleted, this additional information is also permanently deleted and can't be recovered.</span></span>

## <a name="delete-a-booking-calendar-in-the-microsoft-365-admin-center"></a><span data-ttu-id="fcedb-114">Supprimer un calendrier de réservation dans le Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="fcedb-114">Delete a booking calendar in the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="fcedb-115">Aller au Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="fcedb-115">Go to the Microsoft 365 admin center.</span></span>

1. <span data-ttu-id="fcedb-116">Dans le centre d'administration, sélectionnez **Utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="fcedb-116">In the Admin center, select **Users**.</span></span>

   ![Image de l’interface utilisateur utilisateur dans le Centre d’administration Microsoft 365](../media/bookings-admin-center-users.png)

1. <span data-ttu-id="fcedb-118">Sur la page **Utilisateurs actifs**, sélectionnez les noms des utilisateurs à supprimer, puis **Supprimer l'utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="fcedb-118">On the **Active Users** page, choose the names of the users that you want to delete, and then select **Delete user**.</span></span>

   ![Image de la suppression de l’interface utilisateur dans le Centre d’administration Microsoft 365](../media/bookings-delete-user.png)

## <a name="delete-a-booking-calendar-using-exchange-online-powershell"></a><span data-ttu-id="fcedb-120">Supprimer un calendrier de réservation à l’aide d’Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="fcedb-120">Delete a booking calendar using Exchange Online PowerShell</span></span>

<span data-ttu-id="fcedb-121">Consultez [La connexion à Exchange Online PowerShell pour les](https://docs.microsoft.com/powershell/exchange/exchange-online-powershell-v2?view=exchange-ps) conditions préalables et des instructions pour la connexion à Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fcedb-121">See [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online-powershell-v2?view=exchange-ps) for prerequisites and guidance for connecting to Exchange Online PowerShell.</span></span>

<span data-ttu-id="fcedb-122">Pour effectuer ces étapes, vous devez utiliser une fenêtre de commande Microsoft PowerShell active que vous avez exécutée en choisissant l’option « Exécuter en tant qu’administrateur ».</span><span class="sxs-lookup"><span data-stu-id="fcedb-122">To perform these steps, you must be using an active Microsoft PowerShell command window that you ran by choosing the “Run as administrator” option.</span></span>

1. <span data-ttu-id="fcedb-123">Entrez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="fcedb-123">Enter the following command:</span></span>

   ```PowerShell
    $user = get-credential
   ```

1. <span data-ttu-id="fcedb-124">Lorsque vous y êtes invité, connectez-vous avec les informations d’identification de l’administrateur client au client Microsoft 365 qui héberge le calendrier de réservation que vous souhaitez supprimer définitivement.</span><span class="sxs-lookup"><span data-stu-id="fcedb-124">When you are prompted, log on with tenant administrator credentials to the Microsoft 365 tenant that hosts the booking calendar you want to permanently delete.</span></span>

1. <span data-ttu-id="fcedb-125">À l’invite de commandes PowerShell, entrez la commande ci-après :</span><span class="sxs-lookup"><span data-stu-id="fcedb-125">At the PowerShell command prompt, enter this command:</span></span>

   ```PowerShell
    $s = New-Pssession -ConnectionUri https://outlook.office365.com/powershell-liveid -Credential $user -Authentication basic -AllowRedirection -ConfigurationName Microsoft.Exchange
   ```

1. <span data-ttu-id="fcedb-126">Entrez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="fcedb-126">Enter the following command:</span></span>

   ```PowerShell
    Import-PSSession $s
   ```

1. <span data-ttu-id="fcedb-127">Une fois cette commande traitée, entrez la commande suivante pour obtenir la liste des boîtes aux lettres de réservation dans votre client :</span><span class="sxs-lookup"><span data-stu-id="fcedb-127">Once this command is done processing, enter the following command to get a list of the booking mailboxes in your tenant:</span></span>

   ```PowerShell
    get-mailbox -RecipientTypeDetails Scheduling
   ```

1. <span data-ttu-id="fcedb-128">Tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="fcedb-128">Type the following command:</span></span>

   ```PowerShell
   remove-mailbox [BookingCalendarToDelete]
   ```

   > [!IMPORTANT]
   > <span data-ttu-id="fcedb-129">Faites attention à taper le nom exact de l’alias de boîte aux lettres de réservation que vous souhaitez supprimer définitivement.</span><span class="sxs-lookup"><span data-stu-id="fcedb-129">Be careful to type the exact name of the booking mailbox alias that you want to permanently delete.</span></span>

1. <span data-ttu-id="fcedb-130">Pour vérifier que le calendrier a été supprimé, entrez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="fcedb-130">To verify that the calendar has been deleted, enter the following command:</span></span>

   ```PowerShell
    get-mailbox -RecipientTypeDetails Scheduling
   ```

   <span data-ttu-id="fcedb-131">Le calendrier supprimé n’apparaîtra pas dans la sortie.</span><span class="sxs-lookup"><span data-stu-id="fcedb-131">The deleted calendar will not appear in the output.</span></span>
