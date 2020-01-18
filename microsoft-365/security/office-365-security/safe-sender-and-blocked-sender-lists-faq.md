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
ms.openlocfilehash: 9c281460aeff64226343af5e5608ccf42fc83799
ms.sourcegitcommit: a122fd1fce523171529c7f610bb7faf09d30a8bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2020
ms.locfileid: "41238391"
---
# <a name="safe-sender-and-blocked-sender-lists-in-exchange-online"></a><span data-ttu-id="d6240-104">Listes des expéditeurs autorisés et des expéditeurs bloqués dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="d6240-104">Safe sender and blocked sender lists in Exchange Online</span></span>

<span data-ttu-id="d6240-p102">En tant qu'administrateur Exchange Online ou Exchange Online Protection (EOP), vous pouvez faire en sorte qu'un message électronique circulant via le service ne soit pas marqué comme courrier indésirable. Une manière de procéder consiste à créer des listes d'expéditeurs approuvés et d'expéditeurs bloqués pour les membres de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d6240-p102">As an Exchange Online or Exchange Online Protection (EOP) administrator, you can help ensure that an email message traveling through the service isn't marked as spam. One way to do this is to create safe sender and blocked sender lists for the people in your organization.</span></span>

<span data-ttu-id="d6240-107">*Reportez-vous à la version mise à jour des conseils et procédures relatifs à l’utilisation de ces listes en tant qu’administrateur* pour [empêcher que des messages électroniques soient marqués comme courrier indésirable dans Office 365](prevent-email-from-being-marked-as-spam.md).</span><span class="sxs-lookup"><span data-stu-id="d6240-107">*See the updated version of the tips and procedures for how to work with these lists as an admin in* [How to prevent good email from being marked as spam in Office 365](prevent-email-from-being-marked-as-spam.md).</span></span>

<span data-ttu-id="d6240-108">Si vous n’êtes pas un administrateur et que vous voulez simplement gérer votre courrier indésirable dans Outlook à l’aide d’une liste d’expéditeurs approuvés, consultez les étapes décrites dans la[rubrique vue d’ensemble du filtre de courrier indésirable](https://support.office.com/article/5ae3ea8e-cf41-4fa0-b02a-3b96e21de089).</span><span class="sxs-lookup"><span data-stu-id="d6240-108">If you're not an admin, and you just want to manage your own junk email in Outlook by using a safe sender list, check out the steps in the[Overview of the Junk Email Filter](https://support.office.com/article/5ae3ea8e-cf41-4fa0-b02a-3b96e21de089).</span></span>

## <a name="what-is-the-safe-and-blocked-sender-limits-in-exchange-online"></a><span data-ttu-id="d6240-109">Quelles sont les limites d’expéditeurs autorisés et d’expéditeurs bloqués dans Exchange Online ?</span><span class="sxs-lookup"><span data-stu-id="d6240-109">What is the safe and blocked sender limits in Exchange Online?</span></span>

<span data-ttu-id="d6240-p103">Les limites d’expéditeurs autorisés et d’expéditeurs bloqués dans Exchange Online diffèrent des limites d’Active Directory et d’Outlook. Ces limites sont :</span><span class="sxs-lookup"><span data-stu-id="d6240-p103">The safe and blocked sender limits in Exchange Online differ from the Active Directory and Outlook limits. They are:</span></span>

- <span data-ttu-id="d6240-112">Limite d’expéditeurs autorisés : 1 024</span><span class="sxs-lookup"><span data-stu-id="d6240-112">Safe sender limit: 1,024</span></span>

- <span data-ttu-id="d6240-113">Limite des expéditeurs bloqués : 500</span><span class="sxs-lookup"><span data-stu-id="d6240-113">Blocked sender limit: 500</span></span>

<span data-ttu-id="d6240-114">Remarque :</span><span class="sxs-lookup"><span data-stu-id="d6240-114">Note:</span></span>

<span data-ttu-id="d6240-115">Vous pouvez observer l’erreur décrite dans [KB2590466](https://support.microsoft.com/help/2590466/you-receive-the-error-junk-e-mail-validation-error-in-outlook-web-app).</span><span class="sxs-lookup"><span data-stu-id="d6240-115">You may experience the error that is described in [KB2590466](https://support.microsoft.com/help/2590466/you-receive-the-error-junk-e-mail-validation-error-in-outlook-web-app).</span></span> <span data-ttu-id="d6240-116">Pour résoudre ce problème, désactivez la case à cocher « approuver les courriers électroniques en provenance de mes contacts ».</span><span class="sxs-lookup"><span data-stu-id="d6240-116">To resolve this issue, clear the "Trust emails from my contacts" check box.</span></span> <span data-ttu-id="d6240-117">Vous pouvez également réduire le nombre d’adresses de messagerie figurant dans votre dossier de contacts par défaut afin de l’appliquer à la limite maximale autorisée de 1024 dans Exchange Online qui est définie pour l’attribut « Paramètres MaxSafeSenders ».</span><span class="sxs-lookup"><span data-stu-id="d6240-117">Alternatively, decrease the amount of email addresses that are in your default Contacts folder to bring it within the maximum allowed limit of 1024 in Exchange Online that is set for "MaxSafeSenders" attribute.</span></span> <span data-ttu-id="d6240-118">Pour plus d’informations sur cet attribut et sur la cmdlet Set-Mailbox, voirscript rubrique suivante :</span><span class="sxs-lookup"><span data-stu-id="d6240-118">For more information about this attribute and the Set-Mailbox cmdlet, seethe following topic:</span></span>

[<span data-ttu-id="d6240-119">Set-Mailbox</span><span class="sxs-lookup"><span data-stu-id="d6240-119">Set-Mailbox</span></span>](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Set-Mailbox)

## <a name="see-also"></a><span data-ttu-id="d6240-120">Consultez aussi</span><span class="sxs-lookup"><span data-stu-id="d6240-120">See also</span></span>

[<span data-ttu-id="d6240-121">Filtrage des expéditeurs dans Exchange Server</span><span class="sxs-lookup"><span data-stu-id="d6240-121">Sender filtering in Exchange Server</span></span>](https://docs.microsoft.com/exchange/antispam-and-antimalware/antispam-protection/sender-filtering)
