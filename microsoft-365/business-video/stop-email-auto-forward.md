---
title: Arrêter les messages électroniques de transfert automatique
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
ms.collection:
- M365-subscription-management
- Adm_O365
ms.custom:
- AdminSurgePortfolio
- adminvideo
monikerRange: o365-worldwide
search.appverid:
- BCS160
- MET150
- MOE150
description: Découvrez comment arrêter le transfert automatique des courriers électroniques.
ms.openlocfilehash: 0683e133f6c261dc19cc098b13be298cd8086001
ms.sourcegitcommit: f231eece2927f0d01072fd092db1eab15525bbc2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "49702019"
---
# <a name="stop-email-auto-forward"></a><span data-ttu-id="75e33-103">Arrêter l’envoi automatique de messages électroniques</span><span class="sxs-lookup"><span data-stu-id="75e33-103">Stop email auto-forward</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2W6kS?autoplay=false]

<span data-ttu-id="75e33-104">Si un pirate accède à la boîte aux lettres d’un utilisateur, il peut transférer automatiquement le courrier électronique de l’utilisateur vers une adresse externe et voler des informations propriétaires.</span><span class="sxs-lookup"><span data-stu-id="75e33-104">If a hacker gains access to a user's mailbox, they can auto-forward the user's email to an outside address and steal proprietary information.</span></span> <span data-ttu-id="75e33-105">Vous pouvez l’arrêter en créant une règle de flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="75e33-105">You can stop this by creating a mail flow rule.</span></span>

## <a name="try-it"></a><span data-ttu-id="75e33-106">Essayez !</span><span class="sxs-lookup"><span data-stu-id="75e33-106">Try it!</span></span>

1. <span data-ttu-id="75e33-107">Dans le centre d’administration 365 de Microsoft, sélectionnez **Exchange**, **flux de messagerie**, puis sous l’onglet **règles** , sélectionnez le signe plus et choisissez **créer une nouvelle règle**.</span><span class="sxs-lookup"><span data-stu-id="75e33-107">From the Microsoft 365 admin center, select **Exchange**, **mail flow**, and on the **rules** tab, select the plus sign and choose **create a new rule**.</span></span>
1. <span data-ttu-id="75e33-108">Sélectionnez **plus d’options**.</span><span class="sxs-lookup"><span data-stu-id="75e33-108">Select **More options**.</span></span> <span data-ttu-id="75e33-109">Nommez votre nouvelle règle.</span><span class="sxs-lookup"><span data-stu-id="75e33-109">Name your new rule.</span></span>
1. <span data-ttu-id="75e33-110">Ensuite, ouvrez la liste déroulante pour **appliquer cette règle si**, sélectionnez **l’expéditeur**, puis **externe interne**.</span><span class="sxs-lookup"><span data-stu-id="75e33-110">Then open the drop-down for **apply this rule if**, select **the sender**, and then **is external internal**.</span></span>
1. <span data-ttu-id="75e33-111">Sélectionnez **dans l’organisation**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="75e33-111">Select **Inside the organization**, and then **OK**.</span></span>
1. <span data-ttu-id="75e33-112">Choisissez **Ajouter une condition**, ouvrez la liste déroulante, sélectionnez **les propriétés du message**, puis **le type de message**.</span><span class="sxs-lookup"><span data-stu-id="75e33-112">Choose **add condition**, open the drop-down, select **The message properties**, then **include the message type**.</span></span>
1. <span data-ttu-id="75e33-113">Ouvrez la liste déroulante **Sélectionner un type de message** , choisissez **transfert automatique**, puis **OK**.</span><span class="sxs-lookup"><span data-stu-id="75e33-113">Open the **select message type** drop-down, choose **Auto-forward**, then **OK**.</span></span>
1. <span data-ttu-id="75e33-114">Ouvrez la liste déroulante **effectuer les opérations suivantes** , sélectionnez **bloquer le message**, puis **rejeter le message et inclure une explication**.</span><span class="sxs-lookup"><span data-stu-id="75e33-114">Open the **Do the following** drop-down, select **Block the message**, then **reject the message and include an explanation**.</span></span>
1. <span data-ttu-id="75e33-115">Entrez le texte du message correspondant à votre explication, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="75e33-115">Enter the message text for your explanation, then select **OK**.</span></span>
1. <span data-ttu-id="75e33-116">Faites défiler vers le bas, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="75e33-116">Scroll to the bottom and select **Save**.</span></span>

    <span data-ttu-id="75e33-117">Votre règle a été créée et les pirates ne seront plus en mesure de transférer automatiquement les messages.</span><span class="sxs-lookup"><span data-stu-id="75e33-117">Your rule has been created, and hackers will no longer be able to auto-forward messages.</span></span>