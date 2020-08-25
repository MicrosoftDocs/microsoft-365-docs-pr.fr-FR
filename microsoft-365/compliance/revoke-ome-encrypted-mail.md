---
title: Révoquer le courrier électronique chiffré par le chiffrement de messages avancé
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
manager: laurawi
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 06/11/2020
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
description: En tant qu’administrateur et expéditeur de message, vous pouvez révoquer certains courriers électroniques chiffrés avec le chiffrement de messages avancé Office 365.
ms.openlocfilehash: 79ab3ef801d4d19317cbf1416d858de74d9f1393
ms.sourcegitcommit: 22dab0f7604cc057a062698005ff901d40771692
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/25/2020
ms.locfileid: "46868940"
---
# <a name="revoke-email-encrypted-by-advanced-message-encryption"></a><span data-ttu-id="da63a-103">Révoquer le courrier électronique chiffré par le chiffrement de messages avancé</span><span class="sxs-lookup"><span data-stu-id="da63a-103">Revoke email encrypted by Advanced Message Encryption</span></span>

<span data-ttu-id="da63a-104">La révocation de messagerie est proposée dans le cadre du chiffrement avancé des messages Office 365.</span><span class="sxs-lookup"><span data-stu-id="da63a-104">Email revocation is offered as part of Office 365 Advanced Message Encryption.</span></span> <span data-ttu-id="da63a-105">Le chiffrement de messages avancé Office 365 est inclus dans [microsoft 365 entreprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 E5, Microsoft 365 E5 (tarification du personnel pour les personnes travaillant), Office 365 entreprise E5 (tarification du personnel pour les personnes à but lucratif) et Office 365 éducation a5.</span><span class="sxs-lookup"><span data-stu-id="da63a-105">Office 365 Advanced Message Encryption is included in [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 E5, Microsoft 365 E5 (Nonprofit Staff Pricing), Office 365 Enterprise E5 (Nonprofit Staff Pricing), and Office 365 Education A5.</span></span> <span data-ttu-id="da63a-106">Si votre organisation dispose d’un abonnement qui n’inclut pas le chiffrement de messages avancé Office 365, vous pouvez l’acheter avec le complément Microsoft 365 E5 Compliance SKU pour Microsoft 365 E3, Microsoft 365 E3 (tarification du personnel pour les salariés) ou le complément Office 365 Advanced Compliance SKU pour Microsoft 365 E3, Microsoft 365 E3 (tarification du personnel pour les salariés) ou Office 365 SKU.</span><span class="sxs-lookup"><span data-stu-id="da63a-106">If your organization has a subscription that does not include Office 365 Advanced Message Encryption, you can purchase it with the Microsoft 365 E5 Compliance SKU add-on for Microsoft 365 E3, Microsoft 365 E3 (Nonprofit Staff Pricing), or the Office 365 Advanced Compliance SKU add-on for Microsoft 365 E3, Microsoft 365 E3 (Nonprofit Staff Pricing), or Office 365 SKUs.</span></span>

<span data-ttu-id="da63a-107">Cet article fait partie d’une série d’articles plus large sur le [chiffrement de messages Office 365](ome.md).</span><span class="sxs-lookup"><span data-stu-id="da63a-107">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md).</span></span>

<span data-ttu-id="da63a-108">Si un message a été chiffré à l’aide du chiffrement de messages avancé Office 365 et que vous êtes un administrateur de Microsoft 365 ou que vous êtes l’expéditeur du message, vous pouvez le révoquer dans certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="da63a-108">If a message was encrypted using Office 365 Advanced Message Encryption, and you are a Microsoft 365 admin or you are the sender of the message, you can revoke the message under certain conditions.</span></span> <span data-ttu-id="da63a-109">Les administrateurs révoquent les messages à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="da63a-109">Admins revoke messages using PowerShell.</span></span> <span data-ttu-id="da63a-110">En tant qu’expéditeur, vous révoquez un message que vous avez envoyé directement à partir d’Outlook sur le Web.</span><span class="sxs-lookup"><span data-stu-id="da63a-110">As a sender, you revoke a message that you sent directly from Outlook on the web.</span></span> <span data-ttu-id="da63a-111">Cet article décrit les circonstances dans lesquelles la révocation est possible et comment procéder.</span><span class="sxs-lookup"><span data-stu-id="da63a-111">This article describes the circumstances under which revocation is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="da63a-112">Messages chiffrés que vous pouvez révoquer</span><span class="sxs-lookup"><span data-stu-id="da63a-112">Encrypted emails that you can revoke</span></span>

<span data-ttu-id="da63a-113">Les administrateurs et les expéditeurs de messages peuvent révoquer les messages électroniques chiffrés si le destinataire a reçu un message électronique chiffré, basé sur une liaison.</span><span class="sxs-lookup"><span data-stu-id="da63a-113">Admins and message senders can revoke encrypted emails if the recipient received a link-based, branded encrypted email.</span></span> <span data-ttu-id="da63a-114">Si le destinataire a reçu une expérience Inline native dans un client Outlook pris en charge, vous ne pouvez pas révoquer le message.</span><span class="sxs-lookup"><span data-stu-id="da63a-114">If the recipient received a native inline experience in a supported Outlook client, then you can't revoke the message.</span></span>

<span data-ttu-id="da63a-115">Si un destinataire reçoit une expérience basée sur la liaison ou si une expérience en ligne dépend du type d’identité du destinataire : Office 365 et les destinataires de comptes Microsoft (par exemple, les utilisateurs outlook.com) obtiennent une expérience inline dans les clients Outlook pris en charge.</span><span class="sxs-lookup"><span data-stu-id="da63a-115">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients.</span></span> <span data-ttu-id="da63a-116">Tous les autres types de destinataires, tels que Gmail et les destinataires Yahoo, obtiennent une expérience basée sur les liens.</span><span class="sxs-lookup"><span data-stu-id="da63a-116">All other recipient types, such as Gmail and Yahoo recipients, get a link-based experience.</span></span>

<span data-ttu-id="da63a-117">Les administrateurs et les expéditeurs de messages peuvent révoquer des messages chiffrés à l’aide du chiffrement appliqué directement à partir d’Outlook sur le Web.</span><span class="sxs-lookup"><span data-stu-id="da63a-117">Admins and message senders can revoke messages that are encrypted using encryption applied directly from Outlook on the web.</span></span> <span data-ttu-id="da63a-118">Par exemple, les messages chiffrés avec l’option chiffrer uniquement.</span><span class="sxs-lookup"><span data-stu-id="da63a-118">For example, messages encrypted with the Encrypt Only option.</span></span>

:::image type="content" source="../media/adhocencryptionrevoke.png" alt-text="Capture d’écran affichant l’option chiffrer uniquement dans Outlook sur le Web.":::

## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="da63a-120">Expérience de destinataire pour les messages électroniques chiffrés révoqués</span><span class="sxs-lookup"><span data-stu-id="da63a-120">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="da63a-121">Une fois qu’un e-mail a été révoqué, le destinataire reçoit une erreur lorsqu’il accède au courrier électronique chiffré via le portail de chiffrement des messages Office 365 : « le message a été révoqué par l’expéditeur ».</span><span class="sxs-lookup"><span data-stu-id="da63a-121">Once an email has been revoked, the recipient receives an error when they access the encrypted email through the Office 365 Message Encryption portal: "The message has been revoked by the sender".</span></span>

![Capture d’écran illustrant un message électronique chiffré révoqué.](../media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-message-that-you-sent"></a><span data-ttu-id="da63a-123">Procédure révoquer un message chiffré que vous avez envoyé</span><span class="sxs-lookup"><span data-stu-id="da63a-123">How to revoke an encrypted message that you sent</span></span>

<span data-ttu-id="da63a-124">Pour révoquer un message chiffré que vous avez envoyé, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="da63a-124">To revoke an encrypted message that you sent, complete these steps</span></span>

1. <span data-ttu-id="da63a-125">Dans Outlook sur le Web, dans votre dossier **envoyé** , accédez au message à révoquer.</span><span class="sxs-lookup"><span data-stu-id="da63a-125">In Outlook on the web, in your **Sent** folder, browse to the message you want to revoke.</span></span>

   <span data-ttu-id="da63a-126">Si le message est révocable, le lien « supprimer l’accès externe » apparaît en haut du message.</span><span class="sxs-lookup"><span data-stu-id="da63a-126">If the mail is revocable, you'll see the "Remove external access" link at the top of the message.</span></span>

    :::image type="content" source="../media/infoprotect-email-encryption/adhocencryptionrevokesentmsg.png" alt-text="Capture d’écran illustrant le courrier chiffré que vous souhaitez révoquer dans Outlook sur le Web.":::

2. <span data-ttu-id="da63a-128">Cliquez sur **Supprimer l’accès externe** pour révoquer le message.</span><span class="sxs-lookup"><span data-stu-id="da63a-128">Click **Remove external access** to revoke the message.</span></span>

   <span data-ttu-id="da63a-129">Le message indique que son statut est révoqué.</span><span class="sxs-lookup"><span data-stu-id="da63a-129">The message shows that its status is revoked.</span></span>

   :::image type="content" source="../media/adhocencryptionrevokedmsg.png" alt-text="Capture d’écran illustrant un message chiffré révoqué dans Outlook sur le Web.":::

## <a name="how-to-revoke-an-encrypted-message-as-an-administrator"></a><span data-ttu-id="da63a-131">Procédure révoquer un message chiffré en tant qu’administrateur</span><span class="sxs-lookup"><span data-stu-id="da63a-131">How to revoke an encrypted message as an administrator</span></span>

<span data-ttu-id="da63a-132">Les administrateurs de Microsoft 365 suivent ces étapes générales pour révoquer un message électronique chiffré éligible :</span><span class="sxs-lookup"><span data-stu-id="da63a-132">Microsoft 365 administrators follow these general steps to revoke an eligible encrypted email:</span></span>

- <span data-ttu-id="da63a-133">Obtenir l’ID du message électronique.</span><span class="sxs-lookup"><span data-stu-id="da63a-133">Get the Message ID of the email.</span></span>
- <span data-ttu-id="da63a-134">Vérifiez que vous pouvez révoquer le message.</span><span class="sxs-lookup"><span data-stu-id="da63a-134">Verify that you can revoke the message.</span></span>
- <span data-ttu-id="da63a-135">Révoquer le courrier.</span><span class="sxs-lookup"><span data-stu-id="da63a-135">Revoke the mail.</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="da63a-136">Étape 1.</span><span class="sxs-lookup"><span data-stu-id="da63a-136">Step 1.</span></span> <span data-ttu-id="da63a-137">Obtenir l’ID de message de l’e-mail</span><span class="sxs-lookup"><span data-stu-id="da63a-137">Obtain the Message ID of the email</span></span>

<span data-ttu-id="da63a-138">Avant de pouvoir révoquer un courrier chiffré, vous devez recueillir l’ID du message.</span><span class="sxs-lookup"><span data-stu-id="da63a-138">Before you can revoke an encrypted mail, gather the Message ID of the mail.</span></span> <span data-ttu-id="da63a-139">Le MessageId se présente généralement au format suivant :</span><span class="sxs-lookup"><span data-stu-id="da63a-139">The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="da63a-140">Il existe plusieurs façons de trouver l’ID de message de l’e-mail à révoquer.</span><span class="sxs-lookup"><span data-stu-id="da63a-140">There are multiple ways to find the Message ID of the email that you want to revoke.</span></span> <span data-ttu-id="da63a-141">Cette section décrit quelques options, mais vous pouvez utiliser n’importe quelle méthode qui fournit l’ID.</span><span class="sxs-lookup"><span data-stu-id="da63a-141">This section describes a couple of options, but you can use any method that provides the ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="da63a-142">Pour identifier l’ID de message du courrier électronique à révoquer à l’aide du suivi des messages dans le centre de sécurité &amp; conformité</span><span class="sxs-lookup"><span data-stu-id="da63a-142">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="da63a-143">Recherchez le courrier envoyé par l’expéditeur ou le destinataire à l’aide du [nouveau suivi des messages dans le centre de sécurité & conformité](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span><span class="sxs-lookup"><span data-stu-id="da63a-143">Search for the email by sender or recipient using [New Message Trace in Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>

2. <span data-ttu-id="da63a-144">Une fois que vous avez localisé l’e-mail, sélectionnez-le pour afficher le volet **Détails du suivi des messages** .</span><span class="sxs-lookup"><span data-stu-id="da63a-144">Once you've located the email, select it to bring up the **Message trace details** pane.</span></span> <span data-ttu-id="da63a-145">Pour **plus d’informations** , reportez-vous à l’ID du message.</span><span class="sxs-lookup"><span data-stu-id="da63a-145">Expand **More Information** to locate the Message ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="da63a-146">Pour identifier l’ID de message du courrier électronique à révoquer à l’aide des rapports de chiffrement de messages Office dans le centre de sécurité &amp; conformité</span><span class="sxs-lookup"><span data-stu-id="da63a-146">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="da63a-147">Dans le centre de sécurité &amp; conformité, accédez au **rapport de chiffrement des messages**.</span><span class="sxs-lookup"><span data-stu-id="da63a-147">In the Security &amp; Compliance Center, navigate to the **Message encryption report**.</span></span> <span data-ttu-id="da63a-148">Pour plus d’informations sur ce rapport, voir [afficher les rapports de sécurité de messagerie dans le centre de sécurité &amp; conformité](../security/office-365-security/view-email-security-reports.md).</span><span class="sxs-lookup"><span data-stu-id="da63a-148">For information on this report, see [View email security reports in the Security &amp; Compliance Center](../security/office-365-security/view-email-security-reports.md).</span></span>

2. <span data-ttu-id="da63a-149">Sélectionnez le tableau **afficher les détails** et identifiez le message à révoquer.</span><span class="sxs-lookup"><span data-stu-id="da63a-149">Choose the **View details** table and identify the message that you want to revoke.</span></span>

3. <span data-ttu-id="da63a-150">Double-cliquez sur le message pour afficher les détails qui incluent l’ID du message.</span><span class="sxs-lookup"><span data-stu-id="da63a-150">Double-click the message to view details that include the Message ID.</span></span>

### <a name="step-2-verify-that-the-mail-is-revocable"></a><span data-ttu-id="da63a-151">Étape 2.</span><span class="sxs-lookup"><span data-stu-id="da63a-151">Step 2.</span></span> <span data-ttu-id="da63a-152">Vérifier que le message est révocable</span><span class="sxs-lookup"><span data-stu-id="da63a-152">Verify that the mail is revocable</span></span>

<span data-ttu-id="da63a-153">Pour vérifier si vous pouvez révoquer un message, vérifiez si le champ État de révocation est visible dans le rapport de chiffrement, dans la table des **Détails** du centre de sécurité et de &amp; conformité.</span><span class="sxs-lookup"><span data-stu-id="da63a-153">To verify whether you can revoke a message, check whether the Revocation Status field is visible in the Encryption report, in the **Details** table in the Security &amp; Compliance Center.</span></span>

<span data-ttu-id="da63a-154">Pour vérifier si vous pouvez révoquer un message électronique particulier à l’aide de Windows PowerShell, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="da63a-154">To verify whether you can revoke a particular email message by using Windows PowerShell, complete these steps.</span></span>

1. <span data-ttu-id="da63a-155">À l’aide d’un compte professionnel ou scolaire disposant d’autorisations d’administrateur globales dans votre organisation, démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="da63a-155">Using a work or school account that has global administrator permissions in your organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="da63a-156">Pour obtenir des instructions, voir [Connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="da63a-156">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="da63a-157">Exécutez la cmdlet Get-OMEMessageStatus comme suit :</span><span class="sxs-lookup"><span data-stu-id="da63a-157">Run the Get-OMEMessageStatus cmdlet as follows:</span></span>

     ```powershell
     Get-OMEMessageStatus -MessageId "<message id>" | ft -a  Subject, IsRevocable
     ```

   <span data-ttu-id="da63a-158">Cette commande renvoie l’objet du message et indique si le message est révocable.</span><span class="sxs-lookup"><span data-stu-id="da63a-158">This command returns the subject of the message and whether the message is revocable.</span></span> <span data-ttu-id="da63a-159">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="da63a-159">For example,</span></span>

     ```text
     Subject        IsRevocable
     -------        -----------
     "Test message" True
     ```

### <a name="step-3-revoke-the-mail"></a><span data-ttu-id="da63a-160">Étape 3.</span><span class="sxs-lookup"><span data-stu-id="da63a-160">Step 3.</span></span> <span data-ttu-id="da63a-161">Révoquer le courrier</span><span class="sxs-lookup"><span data-stu-id="da63a-161">Revoke the mail</span></span>

<span data-ttu-id="da63a-162">Une fois que vous avez identifié l’ID du message que vous souhaitez révoquer et que vous avez vérifié que le message est révocable, vous pouvez le révoquer à l’aide du centre de sécurité &amp; conformité ou de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="da63a-162">Once you know the Message ID of the email you want to revoke, and you have verified that the message is revocable, you can revoke the email using the Security &amp; Compliance Center or Windows PowerShell.</span></span>

<span data-ttu-id="da63a-163">Pour révoquer le message à l’aide du centre de sécurité &amp; conformité</span><span class="sxs-lookup"><span data-stu-id="da63a-163">To revoke the message using the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="da63a-164">À l’aide d’un compte professionnel ou scolaire disposant d’autorisations d’administrateur globales dans votre organisation, connectez-vous au centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="da63a-164">Using a work or school account that has global administrator permissions in your organization, connect to the Security & Compliance Center.</span></span>

2. <span data-ttu-id="da63a-165">Dans le **rapport de chiffrement**, dans la table des **Détails** du message, choisissez **révoquer un message**.</span><span class="sxs-lookup"><span data-stu-id="da63a-165">In the **Encryption report**, in the **Details** table for the message, choose **Revoke message**.</span></span>

<span data-ttu-id="da63a-166">Pour révoquer un courrier électronique à l’aide de Windows PowerShell, utilisez la cmdlet Set-OMEMessageRevocation.</span><span class="sxs-lookup"><span data-stu-id="da63a-166">To revoke an email by using Windows PowerShell, use the Set-OMEMessageRevocation cmdlet.</span></span>

1. <span data-ttu-id="da63a-167">À l’aide d’un compte professionnel ou scolaire doté d’autorisations d’administrateur globales dans votre organisation, [Connectez-vous à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="da63a-167">Using a work or school account that has global administrator permissions in your organization, [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="da63a-168">Exécutez la cmdlet Set-OMEMessageRevocation comme suit :</span><span class="sxs-lookup"><span data-stu-id="da63a-168">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. <span data-ttu-id="da63a-169">Pour vérifier si l’e-mail a été révoqué, exécutez la cmdlet Get-OMEMessageStatus comme suit :</span><span class="sxs-lookup"><span data-stu-id="da63a-169">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```

    <span data-ttu-id="da63a-170">Si la révocation a réussi, l’applet de commande renvoie le résultat suivant :</span><span class="sxs-lookup"><span data-stu-id="da63a-170">If revocation was successful, the cmdlet returns the following result:</span></span>  

     ```text
     Revoked: True
     ```

## <a name="more-information-about-office-365-advanced-message-encryption"></a><span data-ttu-id="da63a-171">Plus d’informations sur le chiffrement de messages avancé Office 365</span><span class="sxs-lookup"><span data-stu-id="da63a-171">More information about Office 365 Advanced Message Encryption</span></span>

- [<span data-ttu-id="da63a-172">Chiffrement de messages avancé Office 365</span><span class="sxs-lookup"><span data-stu-id="da63a-172">Office 365 Advanced Message Encryption</span></span>](ome-advanced-message-encryption.md)

- [<span data-ttu-id="da63a-173">Office 365 Advanced message Encryption : expiration du courrier électronique</span><span class="sxs-lookup"><span data-stu-id="da63a-173">Office 365 Advanced Message Encryption - email expiration</span></span>](ome-advanced-expiration.md)

- [<span data-ttu-id="da63a-174">Description du service de conformité et de stratégie de message</span><span class="sxs-lookup"><span data-stu-id="da63a-174">Message policy and compliance service description</span></span>](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)
