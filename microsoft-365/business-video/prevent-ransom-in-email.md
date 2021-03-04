---
title: Créer des règles pour vos e-mails pour les rançongiciels
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
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
description: Découvrez comment créer des règles de messagerie pour empêcher les ransomware.
ms.openlocfilehash: 0d8b4a9de881f47752ac0bfbf778453d6ee73046
ms.sourcegitcommit: 355bd51ab6a79d5c36a4e4f57df74ae6873eba19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "50422252"
---
# <a name="create-email-rules-to-prevent-ransomware"></a><span data-ttu-id="43f92-103">Créer des règles de messagerie pour empêcher les ransomware</span><span class="sxs-lookup"><span data-stu-id="43f92-103">Create email rules to prevent ransomware</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWrWGt?autoplay=false]

<span data-ttu-id="43f92-104">Microsoft 365 vous aide à protéger votre entreprise contre les ransomware en empêchant l’ouverture de fichiers potentiellement dangereux, tels que JavaScript, batch et executables, dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="43f92-104">Microsoft 365 helps protect your business against ransomware by preventing potentially dangerous files, like JavaScript, batch, and executables, from being opened in Outlook.</span></span> <span data-ttu-id="43f92-105">Pour augmenter ce niveau de protection en ajoutant des règles qui bloquent ou vous avertissent de types de fichiers supplémentaires, suivez ces étapes.</span><span class="sxs-lookup"><span data-stu-id="43f92-105">To increase this level of protection by adding rules that block or warn you of additional types of files, follow these steps.</span></span>

## <a name="try-it"></a><span data-ttu-id="43f92-106">Essayez !</span><span class="sxs-lookup"><span data-stu-id="43f92-106">Try it!</span></span>

1. <span data-ttu-id="43f92-107">Dans le Centre d’administration, [https://admin.microsoft.com](https://admin.microsoft.com) sélectionnez **Exchange** sous **Centres d’administration.**</span><span class="sxs-lookup"><span data-stu-id="43f92-107">From the admin center at [https://admin.microsoft.com](https://admin.microsoft.com), choose **Exchange** under **Admin centers**.</span></span>
1. <span data-ttu-id="43f92-108">Dans le menu de gauche, choisissez **flux de messagerie.**</span><span class="sxs-lookup"><span data-stu-id="43f92-108">From the menu on the left, choose **mail flow**.</span></span>
1. <span data-ttu-id="43f92-109">Sous l’onglet Règles, choisissez la flèche en haut du symbole plus (+), puis choisissez Créer **une règle.**</span><span class="sxs-lookup"><span data-stu-id="43f92-109">On the rules tab, choose the arrow next to the plus (+) symbol, and then choose **Create a new rule**.</span></span>
1. <span data-ttu-id="43f92-110">Dans la **page nouvelle règle,** entrez un nom pour votre règle, faites défiler vers le bas, puis choisissez **Plus d’options.**</span><span class="sxs-lookup"><span data-stu-id="43f92-110">On the **new rule** page, enter a name for your rule, scroll to the bottom, and then choose **More options**.</span></span>
1. <span data-ttu-id="43f92-111">Sous **Appliquer cette règle si**, sélectionnez **n’importe** quelle pièce jointe, puis sélectionnez **l’extension** de fichier inclut ces mots .</span><span class="sxs-lookup"><span data-stu-id="43f92-111">Under **Apply this rule if**, select **Any attachment**, and then select **file extension includes these words**.</span></span>
1. <span data-ttu-id="43f92-112">Dans la zone sous spécifier des mots ou des **expressions,** entrez les extensions de fichier à appliquer à la règle, telles que les extensions de fichier qui peuvent contenir des macros.</span><span class="sxs-lookup"><span data-stu-id="43f92-112">In the box under **specify words or phrases**, enter the file extensions that you want the rule to be applied to, such as file extensions that can contain macros.</span></span> <span data-ttu-id="43f92-113">Utilisez le symbole plus (+) pour les ajouter un par un.</span><span class="sxs-lookup"><span data-stu-id="43f92-113">Use the plus (+) symbol to add them one at a time.</span></span>

    <span data-ttu-id="43f92-114">En savoir plus sur les types de fichiers en lisant [Protéger contre les ransomware.](https://docs.microsoft.com/microsoft-365/admin/security-and-compliance/secure-your-business-data#ransomware)</span><span class="sxs-lookup"><span data-stu-id="43f92-114">Learn more about file types by reading [Protect against ransomware](https://docs.microsoft.com/microsoft-365/admin/security-and-compliance/secure-your-business-data#ransomware).</span></span>

1. <span data-ttu-id="43f92-115">Faites défiler vers le bas pour passer en revue votre liste, puis choisissez **OK**.</span><span class="sxs-lookup"><span data-stu-id="43f92-115">Scroll down to review your list, and then choose **OK**.</span></span>
1. <span data-ttu-id="43f92-116">Dans la **page nouvelle règle,** choisissez **ajouter une condition,** puis choisissez une condition sous **Faire ce qui suit**.</span><span class="sxs-lookup"><span data-stu-id="43f92-116">On the **new rule** page, choose **add condition**, and then choose a condition under **Do the following**.</span></span>
1. <span data-ttu-id="43f92-117">Vous avez le choix entre de nombreuses options de règle, mais dans cet exemple, nous allons choisir d’avertir le destinataire **avec un message**.</span><span class="sxs-lookup"><span data-stu-id="43f92-117">You have many rule options to choose from, but in this example we'll choose to **Notify the recipient with a message**.</span></span>
1. <span data-ttu-id="43f92-118">Entrez le texte du message pour votre notification, puis choisissez **OK**.</span><span class="sxs-lookup"><span data-stu-id="43f92-118">Enter message text for your notification, and then chose **OK**.</span></span>
1. <span data-ttu-id="43f92-119">Facultatif : sur **la** page nouvelle règle, choisissez ajouter une **exception,** puis entrez les détails des exceptions à votre règle, telles que les messages provenant d’expéditeurs fiables.</span><span class="sxs-lookup"><span data-stu-id="43f92-119">Optional: On the **new rule** page, choose **add exception**, and enter any details for exceptions to your rule, such as messages from trusted senders.</span></span>
1. <span data-ttu-id="43f92-120">Dans la page nouvelle règle, **sélectionnez Enregistrer** et examinez les informations récapitulatifs de règle fournies.</span><span class="sxs-lookup"><span data-stu-id="43f92-120">On the new rule page, choose **Save**, and review the rule summary information provided.</span></span>