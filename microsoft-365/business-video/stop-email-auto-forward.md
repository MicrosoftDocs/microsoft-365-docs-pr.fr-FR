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
description: Découvrez comment arrêter le forwarding automatique des e-mails en créant une règle de flux de messagerie pour éviter le vol d’informations propriétaires.
ms.openlocfilehash: 82e4c80b0edc501889e0fc4dc28f1ec1ad703568
ms.sourcegitcommit: a05f61a291eb4595fa9313757a3815b7f217681d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2021
ms.locfileid: "52706473"
---
# <a name="stop-email-auto-forward"></a><span data-ttu-id="098e4-103">Arrêter le courrier électronique à l’avance automatique</span><span class="sxs-lookup"><span data-stu-id="098e4-103">Stop email auto-forward</span></span>

## <a name="watch-stop-auto-forwarding-emails"></a><span data-ttu-id="098e4-104">Regardez : arrêter le forwarding automatique des e-mails</span><span class="sxs-lookup"><span data-stu-id="098e4-104">Watch: Stop auto-forwarding emails</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2W6kS?autoplay=false]

<span data-ttu-id="098e4-105">Si un pirate informatique accède à la boîte aux lettres d’un utilisateur, il peut automatiquement le faire accéder à une adresse extérieure et voler des informations confidentielles.</span><span class="sxs-lookup"><span data-stu-id="098e4-105">If a hacker gains access to a user's mailbox, they can auto-forward the user's email to an outside address and steal proprietary information.</span></span> <span data-ttu-id="098e4-106">Vous pouvez arrêter cela en créant une règle de flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="098e4-106">You can stop this by creating a mail flow rule.</span></span>

## <a name="try-it"></a><span data-ttu-id="098e4-107">Essayez !</span><span class="sxs-lookup"><span data-stu-id="098e4-107">Try it!</span></span>

1. <span data-ttu-id="098e4-108">Dans le Microsoft 365 d’administration, sélectionnez **Exchange** **,** flux  de messagerie et sous l’onglet Règles, sélectionnez le signe plus et choisissez créer **une règle.**</span><span class="sxs-lookup"><span data-stu-id="098e4-108">From the Microsoft 365 admin center, select **Exchange**, **mail flow**, and on the **rules** tab, select the plus sign and choose **create a new rule**.</span></span>
1. <span data-ttu-id="098e4-109">Sélectionnez **plus d’options.**</span><span class="sxs-lookup"><span data-stu-id="098e4-109">Select **More options**.</span></span> <span data-ttu-id="098e4-110">Nommez votre nouvelle règle.</span><span class="sxs-lookup"><span data-stu-id="098e4-110">Name your new rule.</span></span>
1. <span data-ttu-id="098e4-111">Ensuite, ouvrez la drop-down pour **appliquer cette règle si**, sélectionnez **l’expéditeur,** puis **est interne externe**.</span><span class="sxs-lookup"><span data-stu-id="098e4-111">Then open the drop-down for **apply this rule if**, select **the sender**, and then **is external internal**.</span></span>
1. <span data-ttu-id="098e4-112">Sélectionnez **À l’intérieur de** l’organisation, puis **OK**.</span><span class="sxs-lookup"><span data-stu-id="098e4-112">Select **Inside the organization**, and then **OK**.</span></span>
1. <span data-ttu-id="098e4-113">Choose **add condition**, open the drop-down, select The message **properties**, then include the **message type**.</span><span class="sxs-lookup"><span data-stu-id="098e4-113">Choose **add condition**, open the drop-down, select **The message properties**, then **include the message type**.</span></span>
1. <span data-ttu-id="098e4-114">Ouvrez la drop-down sélectionner le type de **message,** sélectionnez **Auto-forward**, puis **OK**.</span><span class="sxs-lookup"><span data-stu-id="098e4-114">Open the **select message type** drop-down, choose **Auto-forward**, then **OK**.</span></span>
1. <span data-ttu-id="098e4-115">Ouvrez **la liste suivante,** sélectionnez Bloquer le **message,** puis **rejetez le message et incluez une explication.**</span><span class="sxs-lookup"><span data-stu-id="098e4-115">Open the **Do the following** drop-down, select **Block the message**, then **reject the message and include an explanation**.</span></span>
1. <span data-ttu-id="098e4-116">Entrez le texte du message pour votre explication, puis sélectionnez **OK.**</span><span class="sxs-lookup"><span data-stu-id="098e4-116">Enter the message text for your explanation, then select **OK**.</span></span>
1. <span data-ttu-id="098e4-117">Faites défiler jusqu’au bas et sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="098e4-117">Scroll to the bottom and select **Save**.</span></span>

    <span data-ttu-id="098e4-118">Votre règle a été créée et les pirates informatiques ne pourront plus envoyer automatiquement des messages.</span><span class="sxs-lookup"><span data-stu-id="098e4-118">Your rule has been created, and hackers will no longer be able to auto-forward messages.</span></span>

## <a name="related-content"></a><span data-ttu-id="098e4-119">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="098e4-119">Related content</span></span>

<span data-ttu-id="098e4-120">[Ajouter un autre alias de courrier pour un utilisateur](../admin/email/add-another-email-alias-for-a-user.md) (article)</span><span class="sxs-lookup"><span data-stu-id="098e4-120">[Add another email alias for a user](../admin/email/add-another-email-alias-for-a-user.md) (article)</span></span>\
<span data-ttu-id="098e4-121">[Configurer le transfert des e-mails dans Microsoft 365](../admin/email/configure-email-forwarding.md) (article)</span><span class="sxs-lookup"><span data-stu-id="098e4-121">[Configure email forwarding in Microsoft 365](../admin/email/configure-email-forwarding.md) (article)</span></span>\
<span data-ttu-id="098e4-122">[Rechercher et résoudre les problèmes de remise des e-mails en tant qu’administrateur Office 365 entreprise](/exchange/troubleshoot/email-delivery/email-delivery-issues) (article)</span><span class="sxs-lookup"><span data-stu-id="098e4-122">[Find and fix email delivery issues as an Office 365 for business admin](/exchange/troubleshoot/email-delivery/email-delivery-issues) (article)</span></span>