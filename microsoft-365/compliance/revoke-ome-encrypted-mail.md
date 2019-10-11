---
title: Révoquer les e-mails chiffrés par le chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 10/8/2019
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
description: En tant qu’administrateur Office 365, vous pouvez révoquer certains courriers électroniques chiffrés avec Office 365 Advanced message Encryption.
ms.openlocfilehash: 7adc5713c8753e0caf780bbacf98519665458c52
ms.sourcegitcommit: 27a7a373ca77375fdab0690a899135fad16c3cf5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2019
ms.locfileid: "37435548"
---
# <a name="revoke-email-encrypted-by-office-365-advanced-message-encryption"></a><span data-ttu-id="f18a0-103">Révoquer les e-mails chiffrés par le chiffrement de messages Office 365</span><span class="sxs-lookup"><span data-stu-id="f18a0-103">Revoke email encrypted by Office 365 Advanced Message Encryption</span></span>

<span data-ttu-id="f18a0-104">La révocation de messagerie est proposée dans le cadre du chiffrement avancé des messages Office 365.</span><span class="sxs-lookup"><span data-stu-id="f18a0-104">Email revocation is offered as part of Office 365 Advanced Message Encryption.</span></span> <span data-ttu-id="f18a0-105">Le chiffrement de messages avancé Office 365 est inclus dans [microsoft 365 entreprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 E5, Microsoft 365 E5 (tarification du personnel pour les personnes travaillant), Office 365 entreprise E5 (tarification du personnel pour les personnes à but lucratif) et Office 365 éducation a5.</span><span class="sxs-lookup"><span data-stu-id="f18a0-105">Office 365 Advanced Message Encryption is included in [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 E5, Microsoft 365 E5 (Nonprofit Staff Pricing), Office 365 Enterprise E5 (Nonprofit Staff Pricing), and Office 365 Education A5.</span></span> <span data-ttu-id="f18a0-106">Si votre organisation dispose d’un abonnement qui n’inclut pas le chiffrement de messages avancé Office 365, vous pouvez l’acheter avec le complément Microsoft 365 E5 Compliance SKU pour Microsoft 365 E3, Microsoft 365 E3 (tarification du personnel pour les salariés) ou Office 365 Advanced Module complémentaire de référence SKU de conformité pour Microsoft 365 E3, Microsoft 365 E3 (tarifs du personnel pour les salariés) ou Office 365 SKU.</span><span class="sxs-lookup"><span data-stu-id="f18a0-106">If your organization has a subscription that does not include Office 365 Advanced Message Encryption, you can purchase it with the Microsoft 365 E5 Compliance SKU add-on for Microsoft 365 E3, Microsoft 365 E3 (Nonprofit Staff Pricing), or the Office 365 Advanced Compliance SKU add-on for Microsoft 365 E3, Microsoft 365 E3 (Nonprofit Staff Pricing), or Office 365 SKUs.</span></span>

<span data-ttu-id="f18a0-107">Cet article fait partie d’une série d’articles plus large sur le [chiffrement de messages Office 365](ome.md).</span><span class="sxs-lookup"><span data-stu-id="f18a0-107">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md).</span></span>

<span data-ttu-id="f18a0-108">Si un message a été chiffré à l’aide du chiffrement de messages avancé Office 365 et que vous êtes un administrateur d’Office 365, vous pouvez révoquer le message dans certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="f18a0-108">If a message was encrypted using Office 365 Advanced Message Encryption, and you are an Office 365 admin, you can do revoke the message under certain conditions.</span></span> <span data-ttu-id="f18a0-109">Cet article décrit les circonstances dans lesquelles la révocation est possible et comment procéder.</span><span class="sxs-lookup"><span data-stu-id="f18a0-109">This article describes the circumstances under which revocation is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="f18a0-110">Messages chiffrés que vous pouvez révoquer</span><span class="sxs-lookup"><span data-stu-id="f18a0-110">Encrypted emails that you can revoke</span></span>

<span data-ttu-id="f18a0-111">Vous pouvez révoquer les messages électroniques chiffrés si le destinataire a reçu un message électronique chiffré, basé sur une liaison.</span><span class="sxs-lookup"><span data-stu-id="f18a0-111">You can revoke encrypted emails if the recipient received a link-based, branded encrypted email.</span></span> <span data-ttu-id="f18a0-112">Si le destinataire a reçu une expérience Inline native dans un client Outlook pris en charge, ces messages électroniques ne peuvent pas être révoqués.</span><span class="sxs-lookup"><span data-stu-id="f18a0-112">If the recipient received a native inline experience in a supported Outlook client, then those emails cannot be revoked.</span></span>

<span data-ttu-id="f18a0-113">Si un destinataire reçoit une expérience basée sur la liaison ou si une expérience en ligne dépend du type d’identité du destinataire : Office 365 et les destinataires de comptes Microsoft (par exemple, les utilisateurs outlook.com) obtiennent une expérience inline dans les clients Outlook pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f18a0-113">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft Account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients.</span></span> <span data-ttu-id="f18a0-114">Tous les autres types de destinataires, tels que les destinataires Gmail, bénéficient d’une expérience basée sur les liens.</span><span class="sxs-lookup"><span data-stu-id="f18a0-114">All other recipient types, such as Gmail recipients, get a link-based experience.</span></span>

## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="f18a0-115">Expérience de destinataire pour les messages électroniques chiffrés révoqués</span><span class="sxs-lookup"><span data-stu-id="f18a0-115">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="f18a0-116">Une fois qu’un e-mail a été révoqué, le destinataire reçoit une erreur lorsqu’il accède au courrier électronique chiffré via le portail de chiffrement des messages Office 365 : « le message a été révoqué par l’expéditeur ».</span><span class="sxs-lookup"><span data-stu-id="f18a0-116">Once an email has been revoked, the recipient receives an error when they access the encrypted email through the Office 365 Message Encryption portal: “The message has been revoked by the sender”.</span></span>

![Capture d’écran illustrant un message électronique chiffré révoqué.](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a><span data-ttu-id="f18a0-118">Procédure de révocation d’un message électronique chiffré</span><span class="sxs-lookup"><span data-stu-id="f18a0-118">How to revoke an encrypted email</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="f18a0-119">Étape 1.</span><span class="sxs-lookup"><span data-stu-id="f18a0-119">Step 1.</span></span> <span data-ttu-id="f18a0-120">Obtenir l’ID de message de l’e-mail</span><span class="sxs-lookup"><span data-stu-id="f18a0-120">Obtain the Message ID of the email</span></span>

<span data-ttu-id="f18a0-121">Avant de pouvoir révoquer un courrier chiffré, vous devez recueillir l’ID du message.</span><span class="sxs-lookup"><span data-stu-id="f18a0-121">Before you can revoke an encrypted mail you gather the Message ID of the mail.</span></span> <span data-ttu-id="f18a0-122">Le MessageId se présente généralement au format suivant :</span><span class="sxs-lookup"><span data-stu-id="f18a0-122">The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="f18a0-123">Il existe plusieurs façons de trouver l’ID de message de l’e-mail à révoquer.</span><span class="sxs-lookup"><span data-stu-id="f18a0-123">There are multiple ways to find the Message ID of the email that you want to revoke.</span></span> <span data-ttu-id="f18a0-124">Cette section décrit quelques options, mais vous pouvez utiliser n’importe quelle méthode qui fournit l’ID.</span><span class="sxs-lookup"><span data-stu-id="f18a0-124">This section describes a couple of options, but you can use any method that provides the ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="f18a0-125">Pour identifier l’ID de message du courrier électronique à révoquer à l’aide du suivi des messages &amp; dans le centre de sécurité conformité</span><span class="sxs-lookup"><span data-stu-id="f18a0-125">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="f18a0-126">Recherchez le courrier électronique envoyé par l’expéditeur ou le destinataire à l’aide du [nouveau suivi des messages dans le centre de conformité & la sécurité d’Office 365](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span><span class="sxs-lookup"><span data-stu-id="f18a0-126">Search for the email by sender or recipient using [New Message Trace in Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>

2. <span data-ttu-id="f18a0-127">Une fois que vous avez localisé l’e-mail, sélectionnez-le pour afficher le volet **Détails du suivi des messages** .</span><span class="sxs-lookup"><span data-stu-id="f18a0-127">Once you've located the email, select it to bring up the **Message trace details** pane.</span></span> <span data-ttu-id="f18a0-128">Pour **plus d’informations** , reportez-vous à l’ID du message.</span><span class="sxs-lookup"><span data-stu-id="f18a0-128">Expand **More Information** to locate the Message ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="f18a0-129">Pour identifier l’ID de message du courrier électronique à révoquer à l’aide des rapports de chiffrement de &amp; messages Office dans le centre de sécurité conformité</span><span class="sxs-lookup"><span data-stu-id="f18a0-129">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="f18a0-130">Dans le centre &amp; de sécurité conformité, accédez au **rapport de chiffrement des messages**.</span><span class="sxs-lookup"><span data-stu-id="f18a0-130">In the Security &amp; Compliance Center, navigate to the **Message encryption report**.</span></span> <span data-ttu-id="f18a0-131">Pour plus d’informations sur ce rapport, voir [afficher les rapports de sécurité &amp; de messagerie dans le centre de sécurité conformité](view-email-security-reports.md).</span><span class="sxs-lookup"><span data-stu-id="f18a0-131">For information on this report, see [View email security reports in the Security &amp; Compliance Center](view-email-security-reports.md).</span></span>

2. <span data-ttu-id="f18a0-132">Sélectionnez le tableau **afficher les détails** et identifiez le message à révoquer.</span><span class="sxs-lookup"><span data-stu-id="f18a0-132">Choose the **View details** table and identify the message that you want to revoke.</span></span>

3. <span data-ttu-id="f18a0-133">Double-cliquez sur le message pour afficher les détails qui incluent l’ID du message.</span><span class="sxs-lookup"><span data-stu-id="f18a0-133">Double-click the message to view details that include the Message ID.</span></span>

### <a name="step-2-verify-that-the-mail-is-revocable"></a><span data-ttu-id="f18a0-134">Étape 2.</span><span class="sxs-lookup"><span data-stu-id="f18a0-134">Step 2.</span></span> <span data-ttu-id="f18a0-135">Vérifier que le message est révocable</span><span class="sxs-lookup"><span data-stu-id="f18a0-135">Verify that the mail is revocable</span></span>

<span data-ttu-id="f18a0-136">Pour vérifier si vous pouvez révoquer un message, vérifiez si le champ État de révocation est visible dans le rapport de chiffrement, dans la table &amp; des **Détails** du centre de sécurité et de conformité.</span><span class="sxs-lookup"><span data-stu-id="f18a0-136">To verify whether you can revoke a message, check whether the Revocation Status field is visible in the Encryption report, in the **Details** table in the Security &amp; Compliance Center.</span></span>

<span data-ttu-id="f18a0-137">Pour vérifier si vous pouvez révoquer un message électronique particulier à l’aide de Windows PowerShell, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="f18a0-137">To verify whether you can revoke a particular email message by using Windows Powershell, complete these steps.</span></span>

1. <span data-ttu-id="f18a0-138">À l’aide d’un compte professionnel ou scolaire doté d’autorisations d’administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="f18a0-138">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="f18a0-139">Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="f18a0-139">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="f18a0-140">Exécutez la cmdlet Get-OMEMessageStatus comme suit :</span><span class="sxs-lookup"><span data-stu-id="f18a0-140">Run the Get-OMEMessageStatus cmdlet as follows:</span></span>

     ```powershell
     Get-OMEMessageStatus -MessageId "<message id>" | ft -a  Subject, IsRevocable
     ```

   <span data-ttu-id="f18a0-141">Cette valeur renvoie l’objet du message et indique si le message est révocable.</span><span class="sxs-lookup"><span data-stu-id="f18a0-141">This returns the subject of the message and whether the message is revocable.</span></span> <span data-ttu-id="f18a0-142">For example,</span><span class="sxs-lookup"><span data-stu-id="f18a0-142">For example,</span></span>

     ```text
     Subject IsRevocable
     ------- -----------
     “Test message”  True
     ```

### <a name="step-3-revoke-the-mail"></a><span data-ttu-id="f18a0-143">Étape 3.</span><span class="sxs-lookup"><span data-stu-id="f18a0-143">Step 3.</span></span> <span data-ttu-id="f18a0-144">Révoquer le courrier</span><span class="sxs-lookup"><span data-stu-id="f18a0-144">Revoke the mail</span></span>

<span data-ttu-id="f18a0-145">Une fois que vous avez identifié l’ID du message que vous souhaitez révoquer et que vous avez vérifié que le message est révocable, vous pouvez le révoquer à &amp; l’aide du centre de sécurité conformité ou de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f18a0-145">Once you know the Message ID of the email you want to revoke, and you have verified that the message is revocable, you can revoke the email using the Security &amp; Compliance Center or Windows Powershell.</span></span>

<span data-ttu-id="f18a0-146">Pour révoquer le message à l' &amp; aide du centre de sécurité conformité</span><span class="sxs-lookup"><span data-stu-id="f18a0-146">To revoke the message using the Security &amp; Compliance Center</span></span>

<span data-ttu-id="f18a0-147">Pour révoquer le courrier électronique dans &amp; le centre de sécurité conformité, dans le rapport de chiffrement, dans la table des **Détails** du message, sélectionnez **révoquer un message**.</span><span class="sxs-lookup"><span data-stu-id="f18a0-147">To revoke the email in the Security &amp; Compliance Center, in the Encryption report, in the **Details** table for the message, choose **Revoke message**.</span></span>

<span data-ttu-id="f18a0-148">Vous pouvez révoquer un courrier électronique à l’aide de Windows PowerShell à l’aide de la cmdlet Set-OMEMessageRevocation.</span><span class="sxs-lookup"><span data-stu-id="f18a0-148">You can revoke an email by using Windows Powershell by using the Set-OMEMessageRevocation cmdlet.</span></span>

1. <span data-ttu-id="f18a0-149">[Connectez-vous à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="f18a0-149">[Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="f18a0-150">Exécutez la cmdlet Set-OMEMessageRevocation comme suit :</span><span class="sxs-lookup"><span data-stu-id="f18a0-150">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. <span data-ttu-id="f18a0-151">Pour vérifier si l’e-mail a été révoqué, exécutez la cmdlet Get-OMEMessageStatus comme suit :</span><span class="sxs-lookup"><span data-stu-id="f18a0-151">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```

    <span data-ttu-id="f18a0-152">Si la révocation a réussi, l’applet de commande renvoie le résultat suivant :</span><span class="sxs-lookup"><span data-stu-id="f18a0-152">If revocation was successful, the cmdlet returns the following result:</span></span>  

     ```text
     Revoked: True
     ```

## <a name="more-information-about-office-365-advanced-message-encryption"></a><span data-ttu-id="f18a0-153">Plus d’informations sur le chiffrement de messages avancé Office 365</span><span class="sxs-lookup"><span data-stu-id="f18a0-153">More information about Office 365 Advanced Message Encryption</span></span>

- [<span data-ttu-id="f18a0-154">Chiffrement de messages avancé Office 365</span><span class="sxs-lookup"><span data-stu-id="f18a0-154">Office 365 Advanced Message Encryption</span></span>](ome-advanced-message-encryption.md)

- [<span data-ttu-id="f18a0-155">Office 365 Advanced message Encryption : expiration du courrier électronique</span><span class="sxs-lookup"><span data-stu-id="f18a0-155">Office 365 Advanced Message Encryption - email expiration</span></span>](ome-advanced-expiration.md)

- [<span data-ttu-id="f18a0-156">Description du service de conformité et de stratégie de message</span><span class="sxs-lookup"><span data-stu-id="f18a0-156">Message policy and compliance service description</span></span>](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)
