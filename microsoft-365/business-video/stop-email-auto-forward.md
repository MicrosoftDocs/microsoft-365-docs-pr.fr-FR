---
title: Arrêter le transfert automatique d’e-mails
f1.keywords:
- NOCSH
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
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
description: Découvrez comment arrêter le forwarding automatique des e-mails.
ms.openlocfilehash: b6715cfdf8622521d977e0746cb9a340a8f70a5c
ms.sourcegitcommit: 53acc851abf68e2272e75df0856c0e16b0c7e48d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "51578602"
---
# <a name="stop-email-auto-forward"></a><span data-ttu-id="97050-103">Arrêter le courrier électronique à l’avance automatique</span><span class="sxs-lookup"><span data-stu-id="97050-103">Stop email auto-forward</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2W6kS?autoplay=false]

<span data-ttu-id="97050-104">Si un pirate informatique accède à la boîte aux lettres d’un utilisateur, il peut automatiquement envoyer son courrier électronique à une adresse externe et voler des informations confidentielles.</span><span class="sxs-lookup"><span data-stu-id="97050-104">If a hacker gains access to a user's mailbox, they can auto-forward the user's email to an outside address and steal proprietary information.</span></span> <span data-ttu-id="97050-105">Vous pouvez arrêter cela en créant une règle de flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="97050-105">You can stop this by creating a mail flow rule.</span></span>

## <a name="try-it"></a><span data-ttu-id="97050-106">Essayez !</span><span class="sxs-lookup"><span data-stu-id="97050-106">Try it!</span></span>

1. <span data-ttu-id="97050-107">Dans le Centre d’administration Microsoft 365, sélectionnez **Exchange** **,** flux de messagerie et sous l’onglet Règles, sélectionnez le signe plus, puis créez **une règle.** </span><span class="sxs-lookup"><span data-stu-id="97050-107">From the Microsoft 365 admin center, select **Exchange**, **mail flow**, and on the **rules** tab, select the plus sign and choose **create a new rule**.</span></span>
1. <span data-ttu-id="97050-108">Sélectionnez **plus d’options.**</span><span class="sxs-lookup"><span data-stu-id="97050-108">Select **More options**.</span></span> <span data-ttu-id="97050-109">Nommez votre nouvelle règle.</span><span class="sxs-lookup"><span data-stu-id="97050-109">Name your new rule.</span></span>
1. <span data-ttu-id="97050-110">Ensuite, ouvrez la drop-down pour **appliquer cette règle si**, sélectionnez **l’expéditeur,** puis **est interne externe**.</span><span class="sxs-lookup"><span data-stu-id="97050-110">Then open the drop-down for **apply this rule if**, select **the sender**, and then **is external internal**.</span></span>
1. <span data-ttu-id="97050-111">Sélectionnez **À l’intérieur de** l’organisation, puis **OK**.</span><span class="sxs-lookup"><span data-stu-id="97050-111">Select **Inside the organization**, and then **OK**.</span></span>
1. <span data-ttu-id="97050-112">Choose **add condition**, open the drop-down, select The message **properties**, then include the **message type**.</span><span class="sxs-lookup"><span data-stu-id="97050-112">Choose **add condition**, open the drop-down, select **The message properties**, then **include the message type**.</span></span>
1. <span data-ttu-id="97050-113">Ouvrez la drop-down sélectionner le type de **message,** **sélectionnez Auto-forward**, puis **OK**.</span><span class="sxs-lookup"><span data-stu-id="97050-113">Open the **select message type** drop-down, choose **Auto-forward**, then **OK**.</span></span>
1. <span data-ttu-id="97050-114">Ouvrez **la liste suivante,** sélectionnez Bloquer le **message,** puis **rejetez le message et incluez une explication.**</span><span class="sxs-lookup"><span data-stu-id="97050-114">Open the **Do the following** drop-down, select **Block the message**, then **reject the message and include an explanation**.</span></span>
1. <span data-ttu-id="97050-115">Entrez le texte du message pour votre explication, puis sélectionnez **OK.**</span><span class="sxs-lookup"><span data-stu-id="97050-115">Enter the message text for your explanation, then select **OK**.</span></span>
1. <span data-ttu-id="97050-116">Faites défiler jusqu’au bas et sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="97050-116">Scroll to the bottom and select **Save**.</span></span>

    <span data-ttu-id="97050-117">Votre règle a été créée et les pirates informatiques ne pourront plus envoyer automatiquement des messages.</span><span class="sxs-lookup"><span data-stu-id="97050-117">Your rule has been created, and hackers will no longer be able to auto-forward messages.</span></span>