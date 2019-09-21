---
title: Listes des expéditeurs autorisés et des expéditeurs bloqués dans Exchange Online
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 111ab6b0-2dd2-4a87-a928-4931df6b3c4d
ms.collection:
- M365-security-compliance
description: En tant qu'administrateur Exchange Online ou Exchange Online Protection (EOP), vous pouvez faire en sorte qu'un message électronique circulant via le service ne soit pas marqué comme courrier indésirable. Une manière de procéder consiste à créer des listes d'expéditeurs approuvés et d'expéditeurs bloqués pour les membres de votre organisation.
ms.openlocfilehash: 5b1082e0a8f492da1ebc559b0958a6ef76f9a70c
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37080369"
---
# <a name="safe-sender-and-blocked-sender-lists-in-exchange-online"></a><span data-ttu-id="83bdb-104">Listes des expéditeurs autorisés et des expéditeurs bloqués dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="83bdb-104">Safe sender and blocked sender lists in Exchange Online</span></span>

<span data-ttu-id="83bdb-p102">En tant qu'administrateur Exchange Online ou Exchange Online Protection (EOP), vous pouvez faire en sorte qu'un message électronique circulant via le service ne soit pas marqué comme courrier indésirable. Une manière de procéder consiste à créer des listes d'expéditeurs approuvés et d'expéditeurs bloqués pour les membres de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="83bdb-p102">As an Exchange Online or Exchange Online Protection (EOP) administrator, you can help ensure that an email message traveling through the service isn't marked as spam. One way to do this is to create safe sender and blocked sender lists for the people in your organization.</span></span> 
  
 <span data-ttu-id="83bdb-107">*Consultez la version mise à jour des conseils et procédures sur l'utilisation de ces listes comme administrateur dans la rubrique relative à la* [procédure visant à empêcher que des courriers électroniques faux positifs soient marqués comme courrier indésirable à l'aide d'une liste fiable ou d'autres techniques](https://go.microsoft.com/fwlink/p/?LinkID=534224).</span><span class="sxs-lookup"><span data-stu-id="83bdb-107">*See the updated version of the tips and procedures for how to work with these lists as an admin in* [Prevent false positive email marked as spam with a safelist or other techniques](https://go.microsoft.com/fwlink/p/?LinkID=534224).</span></span> 
  
<span data-ttu-id="83bdb-108">Si vous n'êtes pas administrateur et que vous souhaitez simplement gérer votre propre courrier indésirable dans Outlook en utilisant une liste d'expéditeurs approuvés, consultez les étapes décrites dans cette présentation du [filtre de courrier indésirable](https://go.microsoft.com/fwlink/?LinkId=817222).</span><span class="sxs-lookup"><span data-stu-id="83bdb-108">If you're not an admin, and you just want to manage your own junk email in Outlook by using a safe sender list, check out the steps in this overview of [the Junk Email Filter](https://go.microsoft.com/fwlink/?LinkId=817222).</span></span> 
  
## <a name="what-is-the-safe-and-blocked-sender-limits-in-exchange-online"></a><span data-ttu-id="83bdb-109">Quelles sont les limites d’expéditeurs autorisés et d’expéditeurs bloqués dans Exchange Online ?</span><span class="sxs-lookup"><span data-stu-id="83bdb-109">What is the safe and blocked sender limits in Exchange Online?</span></span>

<span data-ttu-id="83bdb-p103">Les limites d’expéditeurs autorisés et d’expéditeurs bloqués dans Exchange Online diffèrent des limites d’Active Directory et d’Outlook. Ces limites sont :</span><span class="sxs-lookup"><span data-stu-id="83bdb-p103">The safe and blocked sender limits in Exchange Online differ from the Active Directory and Outlook limits. They are:</span></span>
  
- <span data-ttu-id="83bdb-112">Limite d’expéditeurs autorisés : 1 024</span><span class="sxs-lookup"><span data-stu-id="83bdb-112">Safe sender limit: 1,024</span></span>
    
- <span data-ttu-id="83bdb-113">Limite des expéditeurs bloqués : 500</span><span class="sxs-lookup"><span data-stu-id="83bdb-113">Blocked sender limit: 500</span></span>
    
<span data-ttu-id="83bdb-114">Remarque :</span><span class="sxs-lookup"><span data-stu-id="83bdb-114">Note:</span></span>
  
<span data-ttu-id="83bdb-115">Vous pouvez observer l’erreur décrite dans [KB2590466](https://support.microsoft.com/help/2590466/you-receive-the-error-junk-e-mail-validation-error-in-outlook-web-app).</span><span class="sxs-lookup"><span data-stu-id="83bdb-115">You may experience the error that is described in [KB2590466](https://support.microsoft.com/help/2590466/you-receive-the-error-junk-e-mail-validation-error-in-outlook-web-app).</span></span> <span data-ttu-id="83bdb-116">Pour résoudre ce problème, désactivez la case à cocher « approuver les courriers électroniques en provenance de mes contacts ».</span><span class="sxs-lookup"><span data-stu-id="83bdb-116">To resolve this issue, clear the "Trust emails from my contacts" check box.</span></span> <span data-ttu-id="83bdb-117">Vous pouvez également réduire le nombre d’adresses de messagerie figurant dans votre dossier de contacts par défaut afin de l’appliquer à la limite maximale autorisée de 1024 dans Exchange Online qui est définie pour l’attribut « Paramètres MaxSafeSenders ».</span><span class="sxs-lookup"><span data-stu-id="83bdb-117">Alternatively, decrease the amount of email addresses that are in your default Contacts folder to bring it within the maximum allowed limit of 1024 in Exchange Online that is set for "MaxSafeSenders" attribute.</span></span> <span data-ttu-id="83bdb-118">Pour plus d’informations sur cet attribut et sur la cmdlet Set-Mailbox, voirscript rubrique suivante :</span><span class="sxs-lookup"><span data-stu-id="83bdb-118">For more information about this attribute and the Set-Mailbox cmdlet, seethe following topic:</span></span>
  
[<span data-ttu-id="83bdb-119">Set-Mailbox</span><span class="sxs-lookup"><span data-stu-id="83bdb-119">Set-Mailbox</span></span>](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Set-Mailbox)
  
## <a name="see-also"></a><span data-ttu-id="83bdb-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83bdb-120">See also</span></span>

[<span data-ttu-id="83bdb-121">Sender filtering in Exchange 2016</span><span class="sxs-lookup"><span data-stu-id="83bdb-121">Sender filtering in Exchange 2016</span></span>](http://technet.microsoft.com/library/b833f864-ff10-46a0-a653-28fb9ba30896.aspx)

