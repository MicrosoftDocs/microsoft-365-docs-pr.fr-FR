---
title: Créer des règles de messagerie pour les ransomware
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
description: Découvrez comment créer des règles de messagerie électronique pour empêcher les ransomware.
ms.openlocfilehash: 85898480438225848fc09db9a9c507045f8a182c
ms.sourcegitcommit: f231eece2927f0d01072fd092db1eab15525bbc2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "49701934"
---
# <a name="create-email-rules-to-prevent-ransomware"></a><span data-ttu-id="a96ac-103">Créer des règles de messagerie pour empêcher les ransomware</span><span class="sxs-lookup"><span data-stu-id="a96ac-103">Create email rules to prevent ransomware</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWrWGt?autoplay=false]

<span data-ttu-id="a96ac-104">Microsoft 365 vous aide à protéger votre entreprise contre les ransomware en empêchant l’ouverture de fichiers potentiellement dangereux, tels que JavaScript, batch et exécutables dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="a96ac-104">Microsoft 365 helps protect your business against ransomware by preventing potentially dangerous files, like JavaScript, batch, and executables, from being opened in Outlook.</span></span> <span data-ttu-id="a96ac-105">Pour augmenter ce niveau de protection en ajoutant des règles qui bloquent ou vous avertissent de types de fichiers supplémentaires, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="a96ac-105">To increase this level of protection by adding rules that block or warn you of additional types of files, follow these steps.</span></span>

## <a name="try-it"></a><span data-ttu-id="a96ac-106">Essayez !</span><span class="sxs-lookup"><span data-stu-id="a96ac-106">Try it!</span></span>

1. <span data-ttu-id="a96ac-107">Dans le centre d’administration [https://admin.microsoft.com](https://admin.microsoft.com) , sélectionnez **Exchange** sous **centres d’administration**.</span><span class="sxs-lookup"><span data-stu-id="a96ac-107">From the admin center at [https://admin.microsoft.com](https://admin.microsoft.com), choose **Exchange** under **Admin centers**.</span></span>
1. <span data-ttu-id="a96ac-108">Dans le menu de gauche, sélectionnez **flux de messagerie**.</span><span class="sxs-lookup"><span data-stu-id="a96ac-108">From the menu on the left, choose **mail flow**.</span></span>
1. <span data-ttu-id="a96ac-109">Dans l’onglet Règles, cliquez sur la flèche en regard du symbole plus (+), puis choisissez **créer une nouvelle règle**.</span><span class="sxs-lookup"><span data-stu-id="a96ac-109">On the rules tab, choose the arrow next to the plus (+) symbol, and then choose **Create a new rule**.</span></span>
1. <span data-ttu-id="a96ac-110">Sur la page **nouvelle règle** , entrez un nom pour votre règle, faites défiler vers le bas, puis choisissez **autres options**.</span><span class="sxs-lookup"><span data-stu-id="a96ac-110">On the **new rule** page, enter a name for your rule, scroll to the bottom, and then choose **More options**.</span></span>
1. <span data-ttu-id="a96ac-111">Sous **appliquer cette règle si**, sélectionnez **une pièce jointe**, puis sélectionnez l' **extension de fichier inclut ces mots**.</span><span class="sxs-lookup"><span data-stu-id="a96ac-111">Under **Apply this rule if**, select **Any attachment**, and then select **file extension includes these words**.</span></span>
1. <span data-ttu-id="a96ac-112">Dans la zone sous **spécifier des mots ou des expressions**, entrez les extensions de fichier auxquelles vous voulez appliquer la règle, par exemple les extensions de fichier pouvant contenir des macros.</span><span class="sxs-lookup"><span data-stu-id="a96ac-112">In the box under **specify words or phrases**, enter the file extensions that you want the rule to be applied to, such as file extensions that can contain macros.</span></span> <span data-ttu-id="a96ac-113">Utilisez le symbole plus (+) pour les ajouter un par un.</span><span class="sxs-lookup"><span data-stu-id="a96ac-113">Use the plus (+) symbol to add them one at a time.</span></span>

    <span data-ttu-id="a96ac-114">Pour plus d’informations sur les types de fichiers, consultez la rubrique [protection contre les ransomware](https://docs.microsoft.com/microsoft-365/admin/security-and-compliance/secure-your-business-data#ransomware).</span><span class="sxs-lookup"><span data-stu-id="a96ac-114">Learn more about file types by reading [Protect against ransomware](https://docs.microsoft.com/microsoft-365/admin/security-and-compliance/secure-your-business-data#ransomware).</span></span>

1. <span data-ttu-id="a96ac-115">Faites défiler vers le bas pour examiner votre liste, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a96ac-115">Scroll down to review your list, and then choose **OK**.</span></span>
1. <span data-ttu-id="a96ac-116">Sur la page **nouvelle règle** , choisissez **Ajouter une condition**, puis choisissez une condition sous **effectuer les opérations suivantes**.</span><span class="sxs-lookup"><span data-stu-id="a96ac-116">On the **new rule** page, choose **add condition**, and then choose a condition under **Do the following**.</span></span>
1. <span data-ttu-id="a96ac-117">Vous pouvez choisir parmi plusieurs options de règle, mais dans cet exemple, nous allons choisir d' **informer le destinataire avec un message**.</span><span class="sxs-lookup"><span data-stu-id="a96ac-117">You have many rule options to choose from, but in this example we'll choose to **Notify the recipient with a message**.</span></span>
1. <span data-ttu-id="a96ac-118">Entrez le texte du message pour votre notification, puis choisissez **OK**.</span><span class="sxs-lookup"><span data-stu-id="a96ac-118">Enter message text for your notification, and then chose **OK**.</span></span>
1. <span data-ttu-id="a96ac-119">Facultatif : sur la page **nouvelle règle** , choisissez **Ajouter une exception**, puis entrez les détails des exceptions à votre règle, par exemple les messages provenant d’expéditeurs approuvés.</span><span class="sxs-lookup"><span data-stu-id="a96ac-119">Optional: On the **new rule** page, choose **add exception**, and enter any details for exceptions to your rule, such as messages from trusted senders.</span></span>
1. <span data-ttu-id="a96ac-120">Sur la page nouvelle règle, sélectionnez **Enregistrer**, puis passez en revue les informations de résumé de la règle fournies.</span><span class="sxs-lookup"><span data-stu-id="a96ac-120">On the new rule page, choose **Save**, and review the rule summary information provided.</span></span>