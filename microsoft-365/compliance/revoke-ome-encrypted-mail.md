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
description: En tant qu’administrateur et expéditeur de message, vous pouvez révoquer certains messages électroniques chiffrés avec Chiffrement avancé de messages Office 365.
ms.openlocfilehash: 340a9e73dba50e28223ee561db749a089c649df6
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51051716"
---
# <a name="revoke-email-encrypted-by-advanced-message-encryption"></a><span data-ttu-id="3c0af-103">Révoquer le courrier électronique chiffré par le chiffrement de messages avancé</span><span class="sxs-lookup"><span data-stu-id="3c0af-103">Revoke email encrypted by Advanced Message Encryption</span></span>

<span data-ttu-id="3c0af-104">La révocation des messages électroniques est proposée dans le cadre Chiffrement avancé de messages Office 365.</span><span class="sxs-lookup"><span data-stu-id="3c0af-104">Email revocation is offered as part of Office 365 Advanced Message Encryption.</span></span> <span data-ttu-id="3c0af-105">Chiffrement avancé de messages Office 365 est inclus dans [Microsoft 365 Entreprise E5,](https://www.microsoft.com/microsoft-365/enterprise/home)Office 365 E5, Microsoft 365 E5 (tarifs du personnel pour les associations), Office 365 Entreprise E5 (prix du personnel pour les associations) et Office 365 Éducation A5.</span><span class="sxs-lookup"><span data-stu-id="3c0af-105">Office 365 Advanced Message Encryption is included in [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 E5, Microsoft 365 E5 (Nonprofit Staff Pricing), Office 365 Enterprise E5 (Nonprofit Staff Pricing), and Office 365 Education A5.</span></span> <span data-ttu-id="3c0af-106">Si votre organisation dispose d’un abonnement qui n’inclut pas de Chiffrement avancé de messages Office 365, vous pouvez l’acheter avec le module Microsoft 365 E5 Conformité SKU pour Microsoft 365 E3, Microsoft 365 E3 (prix du personnel à but non lucratif) ou le module Conformité avancée Office 365 SKU pour les SKU Microsoft 365 E3, Microsoft 365 E3 (prix du personnel à but non lucratif) ou Office 365 SKU.</span><span class="sxs-lookup"><span data-stu-id="3c0af-106">If your organization has a subscription that does not include Office 365 Advanced Message Encryption, you can purchase it with the Microsoft 365 E5 Compliance SKU add-on for Microsoft 365 E3, Microsoft 365 E3 (Nonprofit Staff Pricing), or the Office 365 Advanced Compliance SKU add-on for Microsoft 365 E3, Microsoft 365 E3 (Nonprofit Staff Pricing), or Office 365 SKUs.</span></span>

<span data-ttu-id="3c0af-107">Cet article fait partie d’une série plus importante d’articles [sur chiffrement de messages Office 365](ome.md).</span><span class="sxs-lookup"><span data-stu-id="3c0af-107">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md).</span></span>

<span data-ttu-id="3c0af-108">Si un message a été chiffré à l’aide de Chiffrement avancé de messages Office 365 et que vous êtes un administrateur Microsoft 365 ou si vous êtes l’expéditeur du message, vous pouvez révoquer le message dans certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="3c0af-108">If a message was encrypted using Office 365 Advanced Message Encryption, and you are a Microsoft 365 admin or you are the sender of the message, you can revoke the message under certain conditions.</span></span> <span data-ttu-id="3c0af-109">Les administrateurs révoquent les messages à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3c0af-109">Admins revoke messages using PowerShell.</span></span> <span data-ttu-id="3c0af-110">En tant qu’expéditeur, vous révoquez un message que vous avez envoyé directement Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="3c0af-110">As a sender, you revoke a message that you sent directly from Outlook on the web.</span></span> <span data-ttu-id="3c0af-111">Cet article décrit les circonstances dans lesquelles la révocation est possible et comment le faire.</span><span class="sxs-lookup"><span data-stu-id="3c0af-111">This article describes the circumstances under which revocation is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="3c0af-112">Messages électroniques chiffrés que vous pouvez révoquer</span><span class="sxs-lookup"><span data-stu-id="3c0af-112">Encrypted emails that you can revoke</span></span>

<span data-ttu-id="3c0af-113">Les administrateurs et les expéditeurs de messages peuvent révoquer des messages électroniques chiffrés si le destinataire a reçu un message électronique chiffré de marque basé sur un lien.</span><span class="sxs-lookup"><span data-stu-id="3c0af-113">Admins and message senders can revoke encrypted emails if the recipient received a link-based, branded encrypted email.</span></span> <span data-ttu-id="3c0af-114">Si le destinataire a reçu une expérience inline native dans un client Outlook pris en charge, vous ne pouvez pas révoquer le message.</span><span class="sxs-lookup"><span data-stu-id="3c0af-114">If the recipient received a native inline experience in a supported Outlook client, then you can't revoke the message.</span></span>

<span data-ttu-id="3c0af-115">Le fait qu’un destinataire reçoit une expérience basée sur un lien ou une expérience en ligne dépend du type d’identité du destinataire : les destinataires de compte Office 365 et Microsoft (par exemple, les utilisateurs outlook.com) bénéficient d’une expérience en ligne dans les clients Outlook pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3c0af-115">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients.</span></span> <span data-ttu-id="3c0af-116">Tous les autres types de destinataires, tels que les destinataires Gmail et Yahoo, offrent une expérience basée sur les liens.</span><span class="sxs-lookup"><span data-stu-id="3c0af-116">All other recipient types, such as Gmail and Yahoo recipients, get a link-based experience.</span></span>

<span data-ttu-id="3c0af-117">Les administrateurs et les expéditeurs de messages peuvent révoquer les messages chiffrés à l’aide du chiffrement appliqué Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="3c0af-117">Admins and message senders can revoke messages that are encrypted using encryption applied directly from Outlook on the web.</span></span> <span data-ttu-id="3c0af-118">Par exemple, les messages chiffrés avec l’option Chiffrer uniquement.</span><span class="sxs-lookup"><span data-stu-id="3c0af-118">For example, messages encrypted with the Encrypt Only option.</span></span>

:::image type="content" source="../media/adhocencryptionrevoke.png" alt-text="Capture d’écran montrant l’option Chiffrer Outlook sur le web.":::

## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="3c0af-120">Expérience de destinataire pour les e-mails chiffrés révoqués</span><span class="sxs-lookup"><span data-stu-id="3c0af-120">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="3c0af-121">Une fois qu’un e-mail a été révoqué, le destinataire reçoit une erreur lorsqu’il accède au courrier chiffré via le portail chiffrement de messages Office 365 : « Le message a été révoqué par l’expéditeur ».</span><span class="sxs-lookup"><span data-stu-id="3c0af-121">Once an email has been revoked, the recipient receives an error when they access the encrypted email through the Office 365 Message Encryption portal: "The message has been revoked by the sender".</span></span>

![Capture d’écran shows a revoked encrypted email.](../media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-message-that-you-sent"></a><span data-ttu-id="3c0af-123">Comment révoquer un message chiffré que vous avez envoyé</span><span class="sxs-lookup"><span data-stu-id="3c0af-123">How to revoke an encrypted message that you sent</span></span>

<span data-ttu-id="3c0af-124">Vous pouvez révoquer un message que vous avez envoyé à un destinataire unique qui utilise un compte social tel que gmail.com ou yahoo.com.</span><span class="sxs-lookup"><span data-stu-id="3c0af-124">You can revoke a mail that you sent to a single recipient that uses a social account such as gmail.com or yahoo.com.</span></span> <span data-ttu-id="3c0af-125">En d’autres termes, vous pouvez révoquer un message électronique envoyé à un seul destinataire qui a reçu l’expérience basée sur un lien.</span><span class="sxs-lookup"><span data-stu-id="3c0af-125">In other words, you can revoke an email sent to a single recipient that received the link-based experience.</span></span>

<span data-ttu-id="3c0af-126">Vous ne pouvez pas révoquer un courrier que vous avez envoyé à un destinataire qui utilise un compte scolaire ou scolaire de Office 365 ou Microsoft 365 ou d’un utilisateur qui utilise un compte Microsoft, par exemple, un compte outlook.com.</span><span class="sxs-lookup"><span data-stu-id="3c0af-126">You cannot revoke a mail that you sent to a recipient that uses a work or school account from Office 365 or Microsoft 365 or a user that uses a Microsoft account, for example, an outlook.com account.</span></span> 

<span data-ttu-id="3c0af-127">Pour révoquer un message chiffré que vous avez envoyé, complétez ces étapes</span><span class="sxs-lookup"><span data-stu-id="3c0af-127">To revoke an encrypted message that you sent, complete these steps</span></span>

1. <span data-ttu-id="3c0af-128">Dans Outlook sur le web, dans votre dossier **Envoyé,** accédez au message que vous souhaitez révoquer.</span><span class="sxs-lookup"><span data-stu-id="3c0af-128">In Outlook on the web, in your **Sent** folder, browse to the message you want to revoke.</span></span>

   <span data-ttu-id="3c0af-129">Si le message est révocable, vous verrez le lien « Supprimer l’accès externe » en haut du message.</span><span class="sxs-lookup"><span data-stu-id="3c0af-129">If the mail is revocable, you'll see the "Remove external access" link at the top of the message.</span></span>

    :::image type="content" source="../media/infoprotect-email-encryption/adhocencryptionrevokesentmsg.png" alt-text="Capture d’écran montrant le courrier chiffré que vous souhaitez révoquer dans Outlook sur le web.":::

2. <span data-ttu-id="3c0af-131">Cliquez **sur Supprimer l’accès** externe pour révoquer le message.</span><span class="sxs-lookup"><span data-stu-id="3c0af-131">Click **Remove external access** to revoke the message.</span></span>

   <span data-ttu-id="3c0af-132">Le message indique que son état est révoqué.</span><span class="sxs-lookup"><span data-stu-id="3c0af-132">The message shows that its status is revoked.</span></span>

   :::image type="content" source="../media/adhocencryptionrevokedmsg.png" alt-text="Capture d’écran montrant un message chiffré révoqué Outlook sur le web.":::

## <a name="how-to-revoke-an-encrypted-message-as-an-administrator"></a><span data-ttu-id="3c0af-134">Comment révoquer un message chiffré en tant qu’administrateur</span><span class="sxs-lookup"><span data-stu-id="3c0af-134">How to revoke an encrypted message as an administrator</span></span>

<span data-ttu-id="3c0af-135">Microsoft 365 administrateurs suivent les étapes générales suivantes pour révoquer un e-mail chiffré éligible :</span><span class="sxs-lookup"><span data-stu-id="3c0af-135">Microsoft 365 administrators follow these general steps to revoke an eligible encrypted email:</span></span>

- <span data-ttu-id="3c0af-136">Obtenez l’ID de message de l’e-mail.</span><span class="sxs-lookup"><span data-stu-id="3c0af-136">Get the Message ID of the email.</span></span>
- <span data-ttu-id="3c0af-137">Vérifiez que vous pouvez révoquer le message.</span><span class="sxs-lookup"><span data-stu-id="3c0af-137">Verify that you can revoke the message.</span></span>
- <span data-ttu-id="3c0af-138">Révoquer le courrier.</span><span class="sxs-lookup"><span data-stu-id="3c0af-138">Revoke the mail.</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="3c0af-139">Étape 1.</span><span class="sxs-lookup"><span data-stu-id="3c0af-139">Step 1.</span></span> <span data-ttu-id="3c0af-140">Obtenir l’ID de message de l’e-mail</span><span class="sxs-lookup"><span data-stu-id="3c0af-140">Obtain the Message ID of the email</span></span>

<span data-ttu-id="3c0af-141">Avant de révoquer un message chiffré, collectez l’ID de message du message.</span><span class="sxs-lookup"><span data-stu-id="3c0af-141">Before you can revoke an encrypted mail, gather the Message ID of the mail.</span></span> <span data-ttu-id="3c0af-142">Le MessageId est généralement au format :</span><span class="sxs-lookup"><span data-stu-id="3c0af-142">The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="3c0af-143">Il existe plusieurs façons de rechercher l’ID de message de l’e-mail que vous souhaitez révoquer.</span><span class="sxs-lookup"><span data-stu-id="3c0af-143">There are multiple ways to find the Message ID of the email that you want to revoke.</span></span> <span data-ttu-id="3c0af-144">Cette section décrit quelques options, mais vous pouvez utiliser n’importe quelle méthode qui fournit l’ID.</span><span class="sxs-lookup"><span data-stu-id="3c0af-144">This section describes a couple of options, but you can use any method that provides the ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="3c0af-145">Pour identifier l’ID du message que vous souhaitez révoquer à l’aide du suivi des messages dans le Centre de conformité &amp; de sécurité</span><span class="sxs-lookup"><span data-stu-id="3c0af-145">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="3c0af-146">Recherchez le courrier électronique par expéditeur ou destinataire à l’aide du Nouveau suivi des messages dans le [Centre de sécurité & conformité.](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/)</span><span class="sxs-lookup"><span data-stu-id="3c0af-146">Search for the email by sender or recipient using [New Message Trace in Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>

2. <span data-ttu-id="3c0af-147">Une fois que vous avez localisé l’e-mail, sélectionnez-le pour faire monter le volet **Détails** du suivi des messages.</span><span class="sxs-lookup"><span data-stu-id="3c0af-147">Once you've located the email, select it to bring up the **Message trace details** pane.</span></span> <span data-ttu-id="3c0af-148">Développez **plus d’informations** pour localiser l’ID de message.</span><span class="sxs-lookup"><span data-stu-id="3c0af-148">Expand **More Information** to locate the Message ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="3c0af-149">Pour identifier l’ID de message de l’e-mail que vous souhaitez révoquer à l’aide Office rapports de chiffrement de messages dans le Centre de conformité &amp; de sécurité</span><span class="sxs-lookup"><span data-stu-id="3c0af-149">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="3c0af-150">Dans le Centre de &amp; conformité de sécurité, accédez au rapport de **chiffrement des messages.**</span><span class="sxs-lookup"><span data-stu-id="3c0af-150">In the Security &amp; Compliance Center, navigate to the **Message encryption report**.</span></span> <span data-ttu-id="3c0af-151">Pour plus d’informations sur ce rapport, voir Afficher les rapports de sécurité du courrier [électronique dans le Centre de conformité de &amp; sécurité.](../security/defender-365-security/view-email-security-reports.md)</span><span class="sxs-lookup"><span data-stu-id="3c0af-151">For information on this report, see [View email security reports in the Security &amp; Compliance Center](../security/defender-365-security/view-email-security-reports.md).</span></span>

2. <span data-ttu-id="3c0af-152">Choisissez la **table Afficher les détails** et identifiez le message que vous souhaitez révoquer.</span><span class="sxs-lookup"><span data-stu-id="3c0af-152">Choose the **View details** table and identify the message that you want to revoke.</span></span>

3. <span data-ttu-id="3c0af-153">Double-cliquez sur le message pour afficher les détails qui incluent l’ID de message.</span><span class="sxs-lookup"><span data-stu-id="3c0af-153">Double-click the message to view details that include the Message ID.</span></span>

### <a name="step-2-verify-that-the-mail-is-revocable"></a><span data-ttu-id="3c0af-154">Étape 2.</span><span class="sxs-lookup"><span data-stu-id="3c0af-154">Step 2.</span></span> <span data-ttu-id="3c0af-155">Vérifier que le courrier est révocable</span><span class="sxs-lookup"><span data-stu-id="3c0af-155">Verify that the mail is revocable</span></span>

<span data-ttu-id="3c0af-156">Pour vérifier si vous pouvez révoquer un message, vérifiez si le champ État de révocation est visible dans le rapport de chiffrement, dans la table **Détails** du Centre de conformité de &amp; sécurité.</span><span class="sxs-lookup"><span data-stu-id="3c0af-156">To verify whether you can revoke a message, check whether the Revocation Status field is visible in the Encryption report, in the **Details** table in the Security &amp; Compliance Center.</span></span>

<span data-ttu-id="3c0af-157">Pour vérifier si vous pouvez révoquer un message électronique particulier à l’Windows PowerShell, complétez ces étapes.</span><span class="sxs-lookup"><span data-stu-id="3c0af-157">To verify whether you can revoke a particular email message by using Windows PowerShell, complete these steps.</span></span>

1. <span data-ttu-id="3c0af-158">À l’aide d’un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général dans votre organisation, démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="3c0af-158">Using a work or school account that has global administrator permissions in your organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="3c0af-159">Pour obtenir des instructions, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="3c0af-159">For instructions, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="3c0af-160">Exécutez la cmdlet Get-OMEMessageStatus suivante :</span><span class="sxs-lookup"><span data-stu-id="3c0af-160">Run the Get-OMEMessageStatus cmdlet as follows:</span></span>

     ```powershell
     Get-OMEMessageStatus -MessageId "<message id>" | ft -a  Subject, IsRevocable
     ```

   <span data-ttu-id="3c0af-161">Cette commande renvoie l’objet du message et si le message est révocable.</span><span class="sxs-lookup"><span data-stu-id="3c0af-161">This command returns the subject of the message and whether the message is revocable.</span></span> <span data-ttu-id="3c0af-162">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="3c0af-162">For example,</span></span>

     ```console
     Subject        IsRevocable
     -------        -----------
     "Test message" True
     ```

### <a name="step-3-revoke-the-mail"></a><span data-ttu-id="3c0af-163">Étape 3.</span><span class="sxs-lookup"><span data-stu-id="3c0af-163">Step 3.</span></span> <span data-ttu-id="3c0af-164">Révoquer le courrier</span><span class="sxs-lookup"><span data-stu-id="3c0af-164">Revoke the mail</span></span>

<span data-ttu-id="3c0af-165">Une fois que vous connaissez l’ID du message que vous souhaitez révoquer et que vous avez vérifié que le message est révocable, vous pouvez révoquer le message à l’aide du Centre de conformité de sécurité ou &amp; Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3c0af-165">Once you know the Message ID of the email you want to revoke, and you have verified that the message is revocable, you can revoke the email using the Security &amp; Compliance Center or Windows PowerShell.</span></span>

<span data-ttu-id="3c0af-166">Pour révoquer le message à l’aide du Centre de &amp; conformité de sécurité</span><span class="sxs-lookup"><span data-stu-id="3c0af-166">To revoke the message using the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="3c0af-167">À l’aide d’un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général dans votre organisation, connectez-vous au Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="3c0af-167">Using a work or school account that has global administrator permissions in your organization, connect to the Security & Compliance Center.</span></span>

2. <span data-ttu-id="3c0af-168">In the **Encryption report**, in the **Details** table for the message, choose **Revoke message**.</span><span class="sxs-lookup"><span data-stu-id="3c0af-168">In the **Encryption report**, in the **Details** table for the message, choose **Revoke message**.</span></span>

<span data-ttu-id="3c0af-169">Pour révoquer un e-mail à l’Windows PowerShell, utilisez la cmdlet Set-OMEMessageRevocation'accès.</span><span class="sxs-lookup"><span data-stu-id="3c0af-169">To revoke an email by using Windows PowerShell, use the Set-OMEMessageRevocation cmdlet.</span></span>

1. <span data-ttu-id="3c0af-170">À l’aide d’un compte scolaire ou scolaire qui dispose d’autorisations d’administrateur général dans votre organisation, Connecter [pour Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="3c0af-170">Using a work or school account that has global administrator permissions in your organization, [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

2. <span data-ttu-id="3c0af-171">Exécutez la cmdlet Set-OMEMessageRevocation suivante :</span><span class="sxs-lookup"><span data-stu-id="3c0af-171">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. <span data-ttu-id="3c0af-172">Pour vérifier si l’e-mail a été révoqué, exécutez la cmdlet Get-OMEMessageStatus suivante :</span><span class="sxs-lookup"><span data-stu-id="3c0af-172">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```

    <span data-ttu-id="3c0af-173">Si la révocation a réussi, la cmdlet renvoie le résultat suivant :</span><span class="sxs-lookup"><span data-stu-id="3c0af-173">If revocation was successful, the cmdlet returns the following result:</span></span>  

     ```console
     Revoked: True
     ```

## <a name="more-information-about-office-365-advanced-message-encryption"></a><span data-ttu-id="3c0af-174">Plus d’informations sur Chiffrement avancé de messages Office 365</span><span class="sxs-lookup"><span data-stu-id="3c0af-174">More information about Office 365 Advanced Message Encryption</span></span>

- [<span data-ttu-id="3c0af-175">Chiffrement de messages avancé Office 365</span><span class="sxs-lookup"><span data-stu-id="3c0af-175">Office 365 Advanced Message Encryption</span></span>](ome-advanced-message-encryption.md)

- [<span data-ttu-id="3c0af-176">Chiffrement avancé de messages Office 365 - expiration du courrier électronique</span><span class="sxs-lookup"><span data-stu-id="3c0af-176">Office 365 Advanced Message Encryption - email expiration</span></span>](ome-advanced-expiration.md)

- [<span data-ttu-id="3c0af-177">Description du service de conformité et de stratégie de message</span><span class="sxs-lookup"><span data-stu-id="3c0af-177">Message policy and compliance service description</span></span>](/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)