---
title: Révoquer les e-mails chiffrés par le chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 4/30/2019
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
description: En tant qu’administrateur Office 365, vous pouvez révoquer certains courriers électroniques chiffrés avec Office 365 Advanced message Encryption.
ms.openlocfilehash: e55129f68c7add589bd973b36f069d7cdbf631cf
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37079782"
---
# <a name="revoke-email-encrypted-by-office-365-advanced-message-encryption"></a><span data-ttu-id="da112-103">Révoquer les e-mails chiffrés par le chiffrement de messages Office 365</span><span class="sxs-lookup"><span data-stu-id="da112-103">Revoke email encrypted by Office 365 Advanced Message Encryption</span></span>

<span data-ttu-id="da112-104">La révocation de messagerie est proposée dans le cadre du chiffrement avancé des messages Office 365.</span><span class="sxs-lookup"><span data-stu-id="da112-104">Email revocation is offered as part of Office 365 Advanced Message Encryption.</span></span> <span data-ttu-id="da112-105">Le chiffrement de messages avancé Office 365 est disponible en haut du chiffrement des messages Office 365 dans certains abonnements.</span><span class="sxs-lookup"><span data-stu-id="da112-105">Office 365 Advanced Message Encryption is available on top of Office 365 Message Encryption in certain subscriptions.</span></span> <span data-ttu-id="da112-106">Le chiffrement de messages avancé est inclus dans [Microsoft 365 entreprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 entreprise E5 et Office 365 éducation a5.</span><span class="sxs-lookup"><span data-stu-id="da112-106">Advanced Message Encryption is included in [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 Enterprise E5, and Office 365 Education A5.</span></span> <span data-ttu-id="da112-107">Si votre organisation possède un abonnement Office 365 qui n’inclut pas le chiffrement de messages avancé Office 365, vous pouvez acheter le chiffrement de messages avancé comme module complémentaire avec E5 conformité de la référence SKU de conformité avancée.</span><span class="sxs-lookup"><span data-stu-id="da112-107">If your organization has an Office 365 subscription that does not include Office 365 Advanced Message Encryption, you can purchase Advanced Message Encryption as an add-on with E5 Compliance of the Advanced Compliance SKU.</span></span>

<span data-ttu-id="da112-108">Cet article fait partie d’une série d’articles plus large sur le [chiffrement de messages Office 365](ome.md).</span><span class="sxs-lookup"><span data-stu-id="da112-108">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md).</span></span>

<span data-ttu-id="da112-109">Si un message a été chiffré à l’aide du chiffrement de messages avancé Office 365 et que vous êtes un administrateur d’Office 365, vous pouvez révoquer le message dans certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="da112-109">If a message was encrypted using Office 365 Advanced Message Encryption, and you are an Office 365 admin, you can do revoke the message under certain conditions.</span></span> <span data-ttu-id="da112-110">Cet article décrit les circonstances dans lesquelles la révocation est possible et comment procéder.</span><span class="sxs-lookup"><span data-stu-id="da112-110">This article describes the circumstances under which revocation is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="da112-111">Messages chiffrés que vous pouvez révoquer</span><span class="sxs-lookup"><span data-stu-id="da112-111">Encrypted emails that you can revoke</span></span>

<span data-ttu-id="da112-112">Vous pouvez révoquer les messages électroniques chiffrés si le destinataire a reçu un message électronique chiffré, basé sur une liaison.</span><span class="sxs-lookup"><span data-stu-id="da112-112">You can revoke encrypted emails if the recipient received a link-based, branded encrypted email.</span></span> <span data-ttu-id="da112-113">Si le destinataire a reçu une expérience Inline native dans un client Outlook pris en charge, ces messages électroniques ne peuvent pas être révoqués.</span><span class="sxs-lookup"><span data-stu-id="da112-113">If the recipient received a native inline experience in a supported Outlook client, then those emails cannot be revoked.</span></span>

<span data-ttu-id="da112-114">Si un destinataire reçoit une expérience basée sur la liaison ou si une expérience en ligne dépend du type d’identité du destinataire : Office 365 et les destinataires de comptes Microsoft (par exemple, les utilisateurs outlook.com) obtiennent une expérience inline dans les clients Outlook pris en charge.</span><span class="sxs-lookup"><span data-stu-id="da112-114">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft Account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients.</span></span> <span data-ttu-id="da112-115">Tous les autres types de destinataires, tels que les destinataires Gmail, bénéficient d’une expérience basée sur les liens.</span><span class="sxs-lookup"><span data-stu-id="da112-115">All other recipient types, such as Gmail recipients, get a link-based experience.</span></span>

## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="da112-116">Expérience de destinataire pour les messages électroniques chiffrés révoqués</span><span class="sxs-lookup"><span data-stu-id="da112-116">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="da112-117">Une fois qu’un e-mail a été révoqué, le destinataire reçoit une erreur lorsqu’il accède au courrier électronique chiffré via le portail de chiffrement des messages Office 365 : « le message a été révoqué par l’expéditeur ».</span><span class="sxs-lookup"><span data-stu-id="da112-117">Once an email has been revoked, the recipient receives an error when they access the encrypted email through the Office 365 Message Encryption portal: “The message has been revoked by the sender”.</span></span>

![Capture d’écran illustrant un message électronique chiffré révoqué.](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a><span data-ttu-id="da112-119">Procédure de révocation d’un message électronique chiffré</span><span class="sxs-lookup"><span data-stu-id="da112-119">How to revoke an encrypted email</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="da112-120">Étape 1.</span><span class="sxs-lookup"><span data-stu-id="da112-120">Step 1.</span></span> <span data-ttu-id="da112-121">Obtenir l’ID de message de l’e-mail</span><span class="sxs-lookup"><span data-stu-id="da112-121">Obtain the Message ID of the email</span></span>

<span data-ttu-id="da112-122">Avant de pouvoir révoquer un courrier chiffré, vous devez recueillir l’ID du message.</span><span class="sxs-lookup"><span data-stu-id="da112-122">Before you can revoke an encrypted mail you gather the Message ID of the mail.</span></span> <span data-ttu-id="da112-123">Le MessageId se présente généralement au format suivant :</span><span class="sxs-lookup"><span data-stu-id="da112-123">The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="da112-124">Il existe plusieurs façons de trouver l’ID de message de l’e-mail à révoquer.</span><span class="sxs-lookup"><span data-stu-id="da112-124">There are multiple ways to find the Message ID of the email that you want to revoke.</span></span> <span data-ttu-id="da112-125">Cette section décrit quelques options, mais vous pouvez utiliser n’importe quelle méthode qui fournit l’ID.</span><span class="sxs-lookup"><span data-stu-id="da112-125">This section describes a couple of options, but you can use any method that provides the ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="da112-126">Pour identifier l’ID de message du courrier électronique à révoquer à l’aide du suivi des messages &amp; dans le centre de sécurité conformité</span><span class="sxs-lookup"><span data-stu-id="da112-126">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="da112-127">Recherchez le courrier électronique envoyé par l’expéditeur ou le destinataire à l’aide du [nouveau suivi des messages dans le centre de conformité & la sécurité d’Office 365](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span><span class="sxs-lookup"><span data-stu-id="da112-127">Search for the email by sender or recipient using [New Message Trace in Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>

2. <span data-ttu-id="da112-128">Une fois que vous avez localisé l’e-mail, sélectionnez-le pour afficher le volet **Détails du suivi des messages** .</span><span class="sxs-lookup"><span data-stu-id="da112-128">Once you've located the email, select it to bring up the **Message trace details** pane.</span></span> <span data-ttu-id="da112-129">Pour **plus d’informations** , reportez-vous à l’ID du message.</span><span class="sxs-lookup"><span data-stu-id="da112-129">Expand **More Information** to locate the Message ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="da112-130">Pour identifier l’ID de message du courrier électronique à révoquer à l’aide des rapports de chiffrement de &amp; messages Office dans le centre de sécurité conformité</span><span class="sxs-lookup"><span data-stu-id="da112-130">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="da112-131">Dans le centre &amp; de sécurité conformité, accédez au **rapport de chiffrement des messages**.</span><span class="sxs-lookup"><span data-stu-id="da112-131">In the Security &amp; Compliance Center, navigate to the **Message encryption report**.</span></span> <span data-ttu-id="da112-132">Pour plus d’informations sur ce rapport, voir [afficher les rapports de sécurité &amp; de messagerie dans le centre de sécurité conformité](view-email-security-reports.md).</span><span class="sxs-lookup"><span data-stu-id="da112-132">For information on this report, see [View email security reports in the Security &amp; Compliance Center](view-email-security-reports.md).</span></span>

2. <span data-ttu-id="da112-133">Sélectionnez le tableau **afficher les détails** et identifiez le message à révoquer.</span><span class="sxs-lookup"><span data-stu-id="da112-133">Choose the **View details** table and identify the message that you want to revoke.</span></span>

3. <span data-ttu-id="da112-134">Double-cliquez sur le message pour afficher les détails qui incluent l’ID du message.</span><span class="sxs-lookup"><span data-stu-id="da112-134">Double-click the message to view details that include the Message ID.</span></span>

### <a name="step-2-verify-that-the-mail-is-revocable"></a><span data-ttu-id="da112-135">Étape 2.</span><span class="sxs-lookup"><span data-stu-id="da112-135">Step 2.</span></span> <span data-ttu-id="da112-136">Vérifier que le message est révocable</span><span class="sxs-lookup"><span data-stu-id="da112-136">Verify that the mail is revocable</span></span>

<span data-ttu-id="da112-137">Pour vérifier si vous pouvez révoquer un message, vérifiez si le champ État de révocation est visible dans le rapport de chiffrement, dans la table &amp; des **Détails** du centre de sécurité et de conformité.</span><span class="sxs-lookup"><span data-stu-id="da112-137">To verify whether you can revoke a message, check whether the Revocation Status field is visible in the Encryption report, in the **Details** table in the Security &amp; Compliance Center.</span></span>

<span data-ttu-id="da112-138">Pour vérifier si vous pouvez révoquer un message électronique particulier à l’aide de Windows PowerShell, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="da112-138">To verify whether you can revoke a particular email message by using Windows Powershell, complete these steps.</span></span>

1. <span data-ttu-id="da112-139">À l’aide d’un compte professionnel ou scolaire doté d’autorisations d’administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="da112-139">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="da112-140">Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="da112-140">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="da112-141">Exécutez la cmdlet Get-OMEMessageStatus comme suit :</span><span class="sxs-lookup"><span data-stu-id="da112-141">Run the Get-OMEMessageStatus cmdlet as follows:</span></span>

     ```powershell
     Get-OMEMessageStatus -MessageId "<message id>" | ft -a  Subject, IsRevocable
     ```

   <span data-ttu-id="da112-142">Cette valeur renvoie l’objet du message et indique si le message est révocable.</span><span class="sxs-lookup"><span data-stu-id="da112-142">This returns the subject of the message and whether the message is revocable.</span></span> <span data-ttu-id="da112-143">For example,</span><span class="sxs-lookup"><span data-stu-id="da112-143">For example,</span></span>

     ```text
     Subject IsRevocable
     ------- -----------
     “Test message”  True
     ```

### <a name="step-3-revoke-the-mail"></a><span data-ttu-id="da112-144">Étape 3.</span><span class="sxs-lookup"><span data-stu-id="da112-144">Step 3.</span></span> <span data-ttu-id="da112-145">Révoquer le courrier</span><span class="sxs-lookup"><span data-stu-id="da112-145">Revoke the mail</span></span>

<span data-ttu-id="da112-146">Une fois que vous avez identifié l’ID du message que vous souhaitez révoquer et que vous avez vérifié que le message est révocable, vous pouvez le révoquer à &amp; l’aide du centre de sécurité conformité ou de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="da112-146">Once you know the Message ID of the email you want to revoke, and you have verified that the message is revocable, you can revoke the email using the Security &amp; Compliance Center or Windows Powershell.</span></span>

<span data-ttu-id="da112-147">Pour révoquer le message à l' &amp; aide du centre de sécurité conformité</span><span class="sxs-lookup"><span data-stu-id="da112-147">To revoke the message using the Security &amp; Compliance Center</span></span>

<span data-ttu-id="da112-148">Pour révoquer le courrier électronique dans &amp; le centre de sécurité conformité, dans le rapport de chiffrement, dans la table des **Détails** du message, sélectionnez **révoquer un message**.</span><span class="sxs-lookup"><span data-stu-id="da112-148">To revoke the email in the Security &amp; Compliance Center, in the Encryption report, in the **Details** table for the message, choose **Revoke message**.</span></span>

<span data-ttu-id="da112-149">Vous pouvez révoquer un courrier électronique à l’aide de Windows PowerShell à l’aide de la cmdlet Set-OMEMessageRevocation.</span><span class="sxs-lookup"><span data-stu-id="da112-149">You can revoke an email by using Windows Powershell by using the Set-OMEMessageRevocation cmdlet.</span></span>

1. <span data-ttu-id="da112-150">[Connectez-vous à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="da112-150">[Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="da112-151">Exécutez la cmdlet Set-OMEMessageRevocation comme suit :</span><span class="sxs-lookup"><span data-stu-id="da112-151">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. <span data-ttu-id="da112-152">Pour vérifier si l’e-mail a été révoqué, exécutez la cmdlet Get-OMEMessageStatus comme suit :</span><span class="sxs-lookup"><span data-stu-id="da112-152">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```

    <span data-ttu-id="da112-153">Si la révocation a réussi, l’applet de commande renvoie le résultat suivant :</span><span class="sxs-lookup"><span data-stu-id="da112-153">If revocation was successful, the cmdlet returns the following result:</span></span>  

     ```text
     Revoked: True
     ```

## <a name="more-information-about-office-365-advanced-message-encryption"></a><span data-ttu-id="da112-154">Plus d’informations sur le chiffrement de messages avancé Office 365</span><span class="sxs-lookup"><span data-stu-id="da112-154">More information about Office 365 Advanced Message Encryption</span></span>

- [<span data-ttu-id="da112-155">Chiffrement de messages avancé Office 365</span><span class="sxs-lookup"><span data-stu-id="da112-155">Office 365 Advanced Message Encryption</span></span>](ome-advanced-message-encryption.md)

- [<span data-ttu-id="da112-156">Office 365 Advanced message Encryption : expiration du courrier électronique</span><span class="sxs-lookup"><span data-stu-id="da112-156">Office 365 Advanced Message Encryption - email expiration</span></span>](ome-advanced-expiration.md)

- [<span data-ttu-id="da112-157">Description du service de conformité et de stratégie de message</span><span class="sxs-lookup"><span data-stu-id="da112-157">Message policy and compliance service description</span></span>](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)
