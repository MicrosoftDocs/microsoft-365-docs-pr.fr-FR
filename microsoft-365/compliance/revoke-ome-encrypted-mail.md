---
title: Révoquer les e-mails chiffrés par le chiffrement de messages Office 365
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
manager: laurawi
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 02/28/2020
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
description: En tant qu’administrateur Office 365, vous pouvez révoquer certains courriers électroniques chiffrés avec Office 365 Advanced message Encryption.
ms.openlocfilehash: 0e3ef031e61ed8bc7dd450e7ef61b6b7f41152c6
ms.sourcegitcommit: 004f01fc5d5bdb8aac03d69692d86c38b5e05e14
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2020
ms.locfileid: "42333701"
---
# <a name="revoke-email-encrypted-by-office-365-advanced-message-encryption"></a><span data-ttu-id="bba7e-103">Révoquer les e-mails chiffrés par le chiffrement de messages Office 365</span><span class="sxs-lookup"><span data-stu-id="bba7e-103">Revoke email encrypted by Office 365 Advanced Message Encryption</span></span>

<span data-ttu-id="bba7e-104">La révocation de messagerie est proposée dans le cadre du chiffrement avancé des messages Office 365.</span><span class="sxs-lookup"><span data-stu-id="bba7e-104">Email revocation is offered as part of Office 365 Advanced Message Encryption.</span></span> <span data-ttu-id="bba7e-105">Le chiffrement de messages avancé Office 365 est inclus dans [microsoft 365 entreprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 E5, Microsoft 365 E5 (tarification du personnel pour les personnes travaillant), Office 365 entreprise E5 (tarification du personnel pour les personnes à but lucratif) et Office 365 éducation a5.</span><span class="sxs-lookup"><span data-stu-id="bba7e-105">Office 365 Advanced Message Encryption is included in [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 E5, Microsoft 365 E5 (Nonprofit Staff Pricing), Office 365 Enterprise E5 (Nonprofit Staff Pricing), and Office 365 Education A5.</span></span> <span data-ttu-id="bba7e-106">Si votre organisation dispose d’un abonnement qui n’inclut pas le chiffrement de messages avancé Office 365, vous pouvez l’acheter avec le complément Microsoft 365 E5 Compliance SKU pour Microsoft 365 E3, Microsoft 365 E3 (tarification du personnel pour les salariés) ou Office 365 Advanced Module complémentaire de référence SKU de conformité pour Microsoft 365 E3, Microsoft 365 E3 (tarifs du personnel pour les salariés) ou Office 365 SKU.</span><span class="sxs-lookup"><span data-stu-id="bba7e-106">If your organization has a subscription that does not include Office 365 Advanced Message Encryption, you can purchase it with the Microsoft 365 E5 Compliance SKU add-on for Microsoft 365 E3, Microsoft 365 E3 (Nonprofit Staff Pricing), or the Office 365 Advanced Compliance SKU add-on for Microsoft 365 E3, Microsoft 365 E3 (Nonprofit Staff Pricing), or Office 365 SKUs.</span></span>

<span data-ttu-id="bba7e-107">Cet article fait partie d’une série d’articles plus large sur le [chiffrement de messages Office 365](ome.md).</span><span class="sxs-lookup"><span data-stu-id="bba7e-107">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md).</span></span>

<span data-ttu-id="bba7e-108">Si un message a été chiffré à l’aide du chiffrement de messages avancé Office 365 et que vous êtes un administrateur d’Office 365, vous pouvez révoquer le message dans certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="bba7e-108">If a message was encrypted using Office 365 Advanced Message Encryption, and you are an Office 365 admin, you can revoke the message under certain conditions.</span></span> <span data-ttu-id="bba7e-109">Cet article décrit les circonstances dans lesquelles la révocation est possible et comment procéder.</span><span class="sxs-lookup"><span data-stu-id="bba7e-109">This article describes the circumstances under which revocation is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="bba7e-110">Messages chiffrés que vous pouvez révoquer</span><span class="sxs-lookup"><span data-stu-id="bba7e-110">Encrypted emails that you can revoke</span></span>

<span data-ttu-id="bba7e-111">Vous pouvez révoquer les messages électroniques chiffrés si le destinataire a reçu un message électronique chiffré, basé sur une liaison.</span><span class="sxs-lookup"><span data-stu-id="bba7e-111">You can revoke encrypted emails if the recipient received a link-based, branded encrypted email.</span></span> <span data-ttu-id="bba7e-112">Si le destinataire a reçu une expérience Inline native dans un client Outlook pris en charge, vous ne pouvez pas les révoquer.</span><span class="sxs-lookup"><span data-stu-id="bba7e-112">If the recipient received a native inline experience in a supported Outlook client, then you can't revoke those.</span></span>

<span data-ttu-id="bba7e-113">Si un destinataire reçoit une expérience basée sur la liaison ou si une expérience en ligne dépend du type d’identité du destinataire : Office 365 et les destinataires de comptes Microsoft (par exemple, les utilisateurs outlook.com) obtiennent une expérience inline dans les clients Outlook pris en charge.</span><span class="sxs-lookup"><span data-stu-id="bba7e-113">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft Account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients.</span></span> <span data-ttu-id="bba7e-114">Tous les autres types de destinataires, tels que les destinataires Gmail, bénéficient d’une expérience basée sur les liens.</span><span class="sxs-lookup"><span data-stu-id="bba7e-114">All other recipient types, such as Gmail recipients, get a link-based experience.</span></span>

## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="bba7e-115">Expérience de destinataire pour les messages électroniques chiffrés révoqués</span><span class="sxs-lookup"><span data-stu-id="bba7e-115">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="bba7e-116">Une fois qu’un e-mail a été révoqué, le destinataire reçoit une erreur lorsqu’il accède au courrier électronique chiffré via le portail de chiffrement des messages Office 365 : « le message a été révoqué par l’expéditeur ».</span><span class="sxs-lookup"><span data-stu-id="bba7e-116">Once an email has been revoked, the recipient receives an error when they access the encrypted email through the Office 365 Message Encryption portal: “The message has been revoked by the sender”.</span></span>

![Capture d’écran illustrant un message électronique chiffré révoqué.](../media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a><span data-ttu-id="bba7e-118">Procédure de révocation d’un message électronique chiffré</span><span class="sxs-lookup"><span data-stu-id="bba7e-118">How to revoke an encrypted email</span></span>

<span data-ttu-id="bba7e-119">Les administrateurs d’Office 365 suivent ces étapes générales pour révoquer un message électronique chiffré éligible :</span><span class="sxs-lookup"><span data-stu-id="bba7e-119">Office 365 administrators follow these general steps to revoke an eligible encrypted email:</span></span>

- <span data-ttu-id="bba7e-120">Obtenir l’ID du message électronique.</span><span class="sxs-lookup"><span data-stu-id="bba7e-120">Get the Message ID of the email.</span></span>
- <span data-ttu-id="bba7e-121">Vérifiez que vous pouvez révoquer le message.</span><span class="sxs-lookup"><span data-stu-id="bba7e-121">Verify that you can revoke the message.</span></span>
- <span data-ttu-id="bba7e-122">Révoquer le courrier.</span><span class="sxs-lookup"><span data-stu-id="bba7e-122">Revoke the mail.</span></span>

<span data-ttu-id="bba7e-123">Continuez à lire les instructions détaillées pour chaque étape du processus de révocation.</span><span class="sxs-lookup"><span data-stu-id="bba7e-123">Keep reading for in-depth instructions for each step in the revocation process.</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="bba7e-124">Étape 1.</span><span class="sxs-lookup"><span data-stu-id="bba7e-124">Step 1.</span></span> <span data-ttu-id="bba7e-125">Obtenir l’ID de message de l’e-mail</span><span class="sxs-lookup"><span data-stu-id="bba7e-125">Obtain the Message ID of the email</span></span>

<span data-ttu-id="bba7e-126">Avant de pouvoir révoquer un courrier chiffré, vous devez recueillir l’ID du message.</span><span class="sxs-lookup"><span data-stu-id="bba7e-126">Before you can revoke an encrypted mail, gather the Message ID of the mail.</span></span> <span data-ttu-id="bba7e-127">Le MessageId se présente généralement au format suivant :</span><span class="sxs-lookup"><span data-stu-id="bba7e-127">The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="bba7e-128">Il existe plusieurs façons de trouver l’ID de message de l’e-mail à révoquer.</span><span class="sxs-lookup"><span data-stu-id="bba7e-128">There are multiple ways to find the Message ID of the email that you want to revoke.</span></span> <span data-ttu-id="bba7e-129">Cette section décrit quelques options, mais vous pouvez utiliser n’importe quelle méthode qui fournit l’ID.</span><span class="sxs-lookup"><span data-stu-id="bba7e-129">This section describes a couple of options, but you can use any method that provides the ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="bba7e-130">Pour identifier l’ID de message du courrier électronique à révoquer à l’aide du suivi des messages &amp; dans le centre de sécurité conformité</span><span class="sxs-lookup"><span data-stu-id="bba7e-130">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="bba7e-131">Recherchez le courrier électronique envoyé par l’expéditeur ou le destinataire à l’aide du [nouveau suivi des messages dans le centre de conformité & la sécurité d’Office 365](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span><span class="sxs-lookup"><span data-stu-id="bba7e-131">Search for the email by sender or recipient using [New Message Trace in Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>

2. <span data-ttu-id="bba7e-132">Une fois que vous avez localisé l’e-mail, sélectionnez-le pour afficher le volet **Détails du suivi des messages** .</span><span class="sxs-lookup"><span data-stu-id="bba7e-132">Once you've located the email, select it to bring up the **Message trace details** pane.</span></span> <span data-ttu-id="bba7e-133">Pour **plus d’informations** , reportez-vous à l’ID du message.</span><span class="sxs-lookup"><span data-stu-id="bba7e-133">Expand **More Information** to locate the Message ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="bba7e-134">Pour identifier l’ID de message du courrier électronique à révoquer à l’aide des rapports de chiffrement de &amp; messages Office dans le centre de sécurité conformité</span><span class="sxs-lookup"><span data-stu-id="bba7e-134">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="bba7e-135">Dans le centre &amp; de sécurité conformité, accédez au **rapport de chiffrement des messages**.</span><span class="sxs-lookup"><span data-stu-id="bba7e-135">In the Security &amp; Compliance Center, navigate to the **Message encryption report**.</span></span> <span data-ttu-id="bba7e-136">Pour plus d’informations sur ce rapport, voir [afficher les rapports de sécurité &amp; de messagerie dans le centre de sécurité conformité](../security/office-365-security/view-email-security-reports.md).</span><span class="sxs-lookup"><span data-stu-id="bba7e-136">For information on this report, see [View email security reports in the Security &amp; Compliance Center](../security/office-365-security/view-email-security-reports.md).</span></span>

2. <span data-ttu-id="bba7e-137">Sélectionnez le tableau **afficher les détails** et identifiez le message à révoquer.</span><span class="sxs-lookup"><span data-stu-id="bba7e-137">Choose the **View details** table and identify the message that you want to revoke.</span></span>

3. <span data-ttu-id="bba7e-138">Double-cliquez sur le message pour afficher les détails qui incluent l’ID du message.</span><span class="sxs-lookup"><span data-stu-id="bba7e-138">Double-click the message to view details that include the Message ID.</span></span>

### <a name="step-2-verify-that-the-mail-is-revocable"></a><span data-ttu-id="bba7e-139">Étape 2.</span><span class="sxs-lookup"><span data-stu-id="bba7e-139">Step 2.</span></span> <span data-ttu-id="bba7e-140">Vérifier que le message est révocable</span><span class="sxs-lookup"><span data-stu-id="bba7e-140">Verify that the mail is revocable</span></span>

<span data-ttu-id="bba7e-141">Pour vérifier si vous pouvez révoquer un message, vérifiez si le champ État de révocation est visible dans le rapport de chiffrement, dans la table &amp; des **Détails** du centre de sécurité et de conformité.</span><span class="sxs-lookup"><span data-stu-id="bba7e-141">To verify whether you can revoke a message, check whether the Revocation Status field is visible in the Encryption report, in the **Details** table in the Security &amp; Compliance Center.</span></span>

<span data-ttu-id="bba7e-142">Pour vérifier si vous pouvez révoquer un message électronique particulier à l’aide de Windows PowerShell, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="bba7e-142">To verify whether you can revoke a particular email message by using Windows PowerShell, complete these steps.</span></span>

1. <span data-ttu-id="bba7e-143">À l’aide d’un compte professionnel ou scolaire doté d’autorisations d’administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="bba7e-143">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="bba7e-144">Pour obtenir des instructions, voir [Connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="bba7e-144">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="bba7e-145">Exécutez la cmdlet Get-OMEMessageStatus comme suit :</span><span class="sxs-lookup"><span data-stu-id="bba7e-145">Run the Get-OMEMessageStatus cmdlet as follows:</span></span>

     ```powershell
     Get-OMEMessageStatus -MessageId "<message id>" | ft -a  Subject, IsRevocable
     ```

   <span data-ttu-id="bba7e-146">Cette commande renvoie l’objet du message et indique si le message est révocable.</span><span class="sxs-lookup"><span data-stu-id="bba7e-146">This command returns the subject of the message and whether the message is revocable.</span></span> <span data-ttu-id="bba7e-147">For example,</span><span class="sxs-lookup"><span data-stu-id="bba7e-147">For example,</span></span>

     ```text
     Subject        IsRevocable
     -------        -----------
     “Test message” True
     ```

### <a name="step-3-revoke-the-mail"></a><span data-ttu-id="bba7e-148">Étape 3.</span><span class="sxs-lookup"><span data-stu-id="bba7e-148">Step 3.</span></span> <span data-ttu-id="bba7e-149">Révoquer le courrier</span><span class="sxs-lookup"><span data-stu-id="bba7e-149">Revoke the mail</span></span>

<span data-ttu-id="bba7e-150">Une fois que vous avez identifié l’ID du message que vous souhaitez révoquer et que vous avez vérifié que le message est révocable, vous pouvez le révoquer à &amp; l’aide du centre de sécurité conformité ou de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bba7e-150">Once you know the Message ID of the email you want to revoke, and you have verified that the message is revocable, you can revoke the email using the Security &amp; Compliance Center or Windows PowerShell.</span></span>

<span data-ttu-id="bba7e-151">Pour révoquer le message à l' &amp; aide du centre de sécurité conformité</span><span class="sxs-lookup"><span data-stu-id="bba7e-151">To revoke the message using the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="bba7e-152">À l’aide d’un compte professionnel ou scolaire doté d’autorisations d’administrateur globales dans votre organisation Office 365, connectez-vous au centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="bba7e-152">Using a work or school account that has global administrator permissions in your Office 365 organization, connect to the Security & Compliance Center.</span></span>

2. <span data-ttu-id="bba7e-153">Dans le **rapport de chiffrement**, dans la table des **Détails** du message, choisissez **révoquer un message**.</span><span class="sxs-lookup"><span data-stu-id="bba7e-153">In the **Encryption report**, in the **Details** table for the message, choose **Revoke message**.</span></span>

<span data-ttu-id="bba7e-154">Pour révoquer un courrier électronique à l’aide de Windows PowerShell, utilisez la cmdlet Set-OMEMessageRevocation.</span><span class="sxs-lookup"><span data-stu-id="bba7e-154">To revoke an email by using Windows PowerShell, use the Set-OMEMessageRevocation cmdlet.</span></span>

1. <span data-ttu-id="bba7e-155">À l’aide d’un compte professionnel ou scolaire doté d’autorisations d’administrateur globales dans votre organisation Office 365, [Connectez-vous à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="bba7e-155">Using a work or school account that has global administrator permissions in your Office 365 organization, [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="bba7e-156">Exécutez la cmdlet Set-OMEMessageRevocation comme suit :</span><span class="sxs-lookup"><span data-stu-id="bba7e-156">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. <span data-ttu-id="bba7e-157">Pour vérifier si l’e-mail a été révoqué, exécutez la cmdlet Get-OMEMessageStatus comme suit :</span><span class="sxs-lookup"><span data-stu-id="bba7e-157">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```

    <span data-ttu-id="bba7e-158">Si la révocation a réussi, l’applet de commande renvoie le résultat suivant :</span><span class="sxs-lookup"><span data-stu-id="bba7e-158">If revocation was successful, the cmdlet returns the following result:</span></span>  

     ```text
     Revoked: True
     ```

## <a name="more-information-about-office-365-advanced-message-encryption"></a><span data-ttu-id="bba7e-159">Plus d’informations sur le chiffrement de messages avancé Office 365</span><span class="sxs-lookup"><span data-stu-id="bba7e-159">More information about Office 365 Advanced Message Encryption</span></span>

- [<span data-ttu-id="bba7e-160">Chiffrement de messages avancé Office 365</span><span class="sxs-lookup"><span data-stu-id="bba7e-160">Office 365 Advanced Message Encryption</span></span>](ome-advanced-message-encryption.md)

- [<span data-ttu-id="bba7e-161">Office 365 Advanced message Encryption : expiration du courrier électronique</span><span class="sxs-lookup"><span data-stu-id="bba7e-161">Office 365 Advanced Message Encryption - email expiration</span></span>](ome-advanced-expiration.md)

- [<span data-ttu-id="bba7e-162">Description du service de conformité et de stratégie de message</span><span class="sxs-lookup"><span data-stu-id="bba7e-162">Message policy and compliance service description</span></span>](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)
