---
title: Définir une date d’expiration pour les e-mails chiffrés par le chiffrement avancé de messages Office 365
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/8/2019
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Utilisez le chiffrement de messages avancé Office 365 pour étendre votre sécurité de messagerie en définissant une date d’expiration pour les e-mails via un modèle personnalisé.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: bbd018e55592e5b17149edf1a4dc0907c0184417
ms.sourcegitcommit: 6647055154002c7d3b8f7ce25ad53c9636bc8066
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2020
ms.locfileid: "48769164"
---
# <a name="set-an-expiration-date-for-email-encrypted-by-office-365-advanced-message-encryption"></a><span data-ttu-id="162e1-103">Définir une date d’expiration pour les e-mails chiffrés par le chiffrement avancé de messages Office 365</span><span class="sxs-lookup"><span data-stu-id="162e1-103">Set an expiration date for email encrypted by Office 365 Advanced Message Encryption</span></span>

<span data-ttu-id="162e1-104">Le chiffrement de messages avancé Office 365 est inclus dans [microsoft 365 entreprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 E5, Microsoft 365 E5 (tarification du personnel pour les personnes travaillant), Office 365 entreprise E5 (tarification du personnel pour les personnes à but lucratif) et Office 365 éducation a5.</span><span class="sxs-lookup"><span data-stu-id="162e1-104">Office 365 Advanced Message Encryption is included in [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 E5, Microsoft 365 E5 (Nonprofit Staff Pricing), Office 365 Enterprise E5 (Nonprofit Staff Pricing), and Office 365 Education A5.</span></span> <span data-ttu-id="162e1-105">Si votre organisation dispose d’un abonnement qui n’inclut pas le chiffrement de messages avancé Office 365, vous pouvez l’acheter avec le complément Microsoft 365 E5 Compliance SKU pour Microsoft 365 E3, Microsoft 365 E3 (tarification du personnel pour les salariés) ou le complément Office 365 Advanced Compliance SKU pour Microsoft 365 E3, Microsoft 365 E3 (tarification du personnel pour les salariés) ou Office 365 SKU.</span><span class="sxs-lookup"><span data-stu-id="162e1-105">If your organization has a subscription that does not include Office 365 Advanced Message Encryption, you can purchase it with the Microsoft 365 E5 Compliance SKU add-on for Microsoft 365 E3, Microsoft 365 E3 (Nonprofit Staff Pricing), or the Office 365 Advanced Compliance SKU add-on for Microsoft 365 E3, Microsoft 365 E3 (Nonprofit Staff Pricing), or Office 365 SKUs.</span></span>

<span data-ttu-id="162e1-106">Vous pouvez utiliser l’expiration des messages envoyés par vos utilisateurs à des destinataires externes qui utilisent le portail OME pour accéder à des e-mails chiffrés.</span><span class="sxs-lookup"><span data-stu-id="162e1-106">You can use message expiration on emails that your users send to external recipients who use the OME Portal to access encrypted emails.</span></span> <span data-ttu-id="162e1-107">Vous obligez les destinataires à utiliser le portail OME pour afficher et répondre à des messages électroniques chiffrés envoyés par votre organisation à l’aide d’un modèle personnalisé qui spécifie une date d’expiration dans Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="162e1-107">You force recipients to use the OME portal to view and reply to encrypted emails sent by your organization by using a custom branded template that specifies an expiration date in Windows PowerShell.</span></span>

<span data-ttu-id="162e1-108">En tant qu’administrateur général Office 365, lorsque vous appliquez la marque de votre entreprise pour personnaliser l’apparence des messages électroniques de votre organisation, vous pouvez également spécifier une expiration pour ces messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="162e1-108">As an Office 365 global administrator, when you apply your company brand to customize the look of your organization's email messages, you can also specify an expiration for these email messages.</span></span> <span data-ttu-id="162e1-109">Avec le chiffrement de messages avancé Office 365, vous pouvez créer plusieurs modèles pour les messages électroniques chiffrés provenant de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="162e1-109">With Office 365 Advanced Message Encryption, you can create multiple templates for encrypted emails that originate from your organization.</span></span> <span data-ttu-id="162e1-110">À l’aide d’un modèle, vous pouvez contrôler la durée pendant laquelle les destinataires ont accès aux messages envoyés par vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="162e1-110">Using a template, you can control how long recipients have access to mail sent by your users.</span></span>

<span data-ttu-id="162e1-111">Lorsqu’un utilisateur final reçoit un message dont la date d’expiration est définie, l’utilisateur voit la date d’expiration dans le message du wrapper.</span><span class="sxs-lookup"><span data-stu-id="162e1-111">When an end user receives mail that has an expiration date set, the user sees the expiration date in the wrapper email.</span></span> <span data-ttu-id="162e1-112">Si un utilisateur tente d’ouvrir un message expiré, une erreur s’affiche dans le portail OME.</span><span class="sxs-lookup"><span data-stu-id="162e1-112">If a user tries to open an expired mail, an error appears in the OME portal.</span></span>

<span data-ttu-id="162e1-113">Vous pouvez uniquement définir des dates d’expiration pour les messages électroniques adressés à des destinataires externes.</span><span class="sxs-lookup"><span data-stu-id="162e1-113">You can only set expiration dates for emails to external recipients.</span></span>

<span data-ttu-id="162e1-114">Avec le chiffrement de messages avancé Office 365, chaque fois que vous appliquez une personnalisation personnalisée, Office 365 applique le wrapper aux messages électroniques qui correspondent à la règle de flux de messagerie à laquelle vous appliquez le modèle.</span><span class="sxs-lookup"><span data-stu-id="162e1-114">With Office 365 Advanced Message Encryption, anytime you apply custom branding, the Office 365 applies the wrapper to email that fits the mail flow rule to which you apply the template.</span></span> <span data-ttu-id="162e1-115">De plus, vous ne pouvez utiliser l’expiration que si vous utilisez une personnalisation personnalisée.</span><span class="sxs-lookup"><span data-stu-id="162e1-115">In addition, you can only use expiration if you use custom branding.</span></span>

## <a name="create-a-custom-branding-template-to-force-mail-expiration-by-using-powershell"></a><span data-ttu-id="162e1-116">Créer un modèle de personnalisation pour forcer l’expiration du courrier à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="162e1-116">Create a custom branding template to force mail expiration by using PowerShell</span></span>

1. <span data-ttu-id="162e1-117">[Connectez-vous à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell) avec un compte disposant d’autorisations d’administrateur globales au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="162e1-117">[Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell) with an account that has global administrator permissions in your organization.</span></span>

2. <span data-ttu-id="162e1-118">Exécutez l’applet de commande New-OMEConfiguration.</span><span class="sxs-lookup"><span data-stu-id="162e1-118">Run the New-OMEConfiguration cmdlet.</span></span>

    ```powershell
    New-OMEConfiguration -Identity "Expire in 7 days" -ExternalMailExpiryInDays 7
    ```

<span data-ttu-id="162e1-119">Où :</span><span class="sxs-lookup"><span data-stu-id="162e1-119">Where:</span></span>

- <span data-ttu-id="162e1-120">`Identity` est le nom du modèle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="162e1-120">`Identity` is the name of the custom template.</span></span>

- <span data-ttu-id="162e1-121">`ExternalMailExpiryInDays` identifie le nombre de jours pendant lesquels les destinataires peuvent conserver leur courrier avant d’expirer.</span><span class="sxs-lookup"><span data-stu-id="162e1-121">`ExternalMailExpiryInDays` identifies the number of days that recipients can keep mail before it expires.</span></span> <span data-ttu-id="162e1-122">Vous pouvez utiliser n’importe quelle valeur comprise entre 1 et 730 jours.</span><span class="sxs-lookup"><span data-stu-id="162e1-122">You can use any value between 1–730 days.</span></span>

## <a name="more-information-about-office-365-advanced-message-encryption"></a><span data-ttu-id="162e1-123">Plus d’informations sur le chiffrement de messages avancé Office 365</span><span class="sxs-lookup"><span data-stu-id="162e1-123">More information about Office 365 Advanced Message Encryption</span></span>

- [<span data-ttu-id="162e1-124">Chiffrement de messages avancé Office 365</span><span class="sxs-lookup"><span data-stu-id="162e1-124">Office 365 Advanced Message Encryption</span></span>](ome-advanced-message-encryption.md)

- [<span data-ttu-id="162e1-125">Révoquer les e-mails chiffrés par le chiffrement de messages Office 365</span><span class="sxs-lookup"><span data-stu-id="162e1-125">Revoke email encrypted by Office 365 Advanced Message Encryption</span></span>](revoke-ome-encrypted-mail.md)

- [<span data-ttu-id="162e1-126">Description du service de conformité et de stratégie de message</span><span class="sxs-lookup"><span data-stu-id="162e1-126">Message policy and compliance service description</span></span>](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)
