---
title: Configurer un certificat APNs pour les appareils iOS
f1.keywords: NOCSH
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom: AdminSurgePortfolio
description: Gérer les appareils iOS dans Basic Mobility and Security.
ms.openlocfilehash: 84f3589593ef26325397f5b6e90d5b21662d2352
ms.sourcegitcommit: 48195345b21b409b175d68acdc25d9f2fc4fc5f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "53228242"
---
# <a name="create-an-apns-certificate-for-ios-devices"></a><span data-ttu-id="37727-103">Configurer un certificat APNs pour les appareils iOS</span><span class="sxs-lookup"><span data-stu-id="37727-103">Create an APNs certificate for iOS devices</span></span>

<span data-ttu-id="37727-104">Pour gérer les appareils iOS tels que les iPad et les iPhone dans Basic Mobility and Security, créez un certificat APNs.</span><span class="sxs-lookup"><span data-stu-id="37727-104">To manage iOS devices such as iPads and iPhones in Basic Mobility and Security, create an APNs certificate.</span></span>

1. <span data-ttu-id="37727-105">Connectez-vous Microsoft 365 avec votre compte d’administrateur global.</span><span class="sxs-lookup"><span data-stu-id="37727-105">Sign in to Microsoft 365 with your global admin account.</span></span>

2. <span data-ttu-id="37727-106">Dans votre navigateur, tapez  <https://protection.office.com/> .</span><span class="sxs-lookup"><span data-stu-id="37727-106">In your browser, type <https://protection.office.com/>.</span></span>

3. <span data-ttu-id="37727-107">Sélectionnez  **Gestion des appareils de protection contre** la perte de   >  \*\*\*\* données, puis sélectionnez **Certificat APNs pour les appareils iOS.**</span><span class="sxs-lookup"><span data-stu-id="37727-107">Select  **Data loss prevention** > **Device management**, and choose **APNs Certificate for iOS devices**.</span></span>

4. <span data-ttu-id="37727-108">Dans la page Certificat de notification Push Apple Paramètres, choisissez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="37727-108">On the Apple Push Notification Certificate Settings page, choose **Next**.</span></span>

5. <span data-ttu-id="37727-109">Sélectionnez Télécharger votre fichier CSR et enregistrez la demande de signature de certificat dans un endroit de votre ordinateur que vous mémoriserez.</span><span class="sxs-lookup"><span data-stu-id="37727-109">Select Download your CSR file and save the certificate signing request to somewhere on your computer that you'll remember.</span></span> <span data-ttu-id="37727-110">Sélectionnez  **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="37727-110">Select  **Next**.</span></span>

6. <span data-ttu-id="37727-111">Dans la page Créer un certificat APNs :</span><span class="sxs-lookup"><span data-stu-id="37727-111">On the Create an APNs certificate page:</span></span>

    1. <span data-ttu-id="37727-112">Sélectionnez Le portail Apple APNS pour ouvrir le portail de certificats Push Apple.</span><span class="sxs-lookup"><span data-stu-id="37727-112">Select  Apple APNS Portal to open the Apple Push Certificates Portal.</span></span>

    2. <span data-ttu-id="37727-113">Sign in with an Apple ID.</span><span class="sxs-lookup"><span data-stu-id="37727-113">Sign in with an Apple ID.</span></span>

       > [!IMPORTANT]
       > <span data-ttu-id="37727-p102">Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate.</span><span class="sxs-lookup"><span data-stu-id="37727-p102">Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate.</span></span>

    3. <span data-ttu-id="37727-116">Sélectionnez  **Créer un certificat et**   acceptez les conditions d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="37727-116">Select  **Create a Certificate**  and accept the Terms of Use.</span></span>

    4. <span data-ttu-id="37727-117">Accédez à la demande de signature de certificat que vous avez téléchargée sur votre ordinateur à partir Microsoft 365, puis sélectionnez **Télécharger**.</span><span class="sxs-lookup"><span data-stu-id="37727-117">Browse to the certificate signing request you downloaded to your computer from Microsoft 365, and select **Upload**.</span></span>

       <span data-ttu-id="37727-118">Téléchargez le certificat APNs créé par le portail de certificats Push Apple sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="37727-118">Download the APNs certificate created by the Apple Push Certificate Portal to your computer.</span></span>

       > [!TIP]
       > <span data-ttu-id="37727-119">If you're having trouble downloading the certificate, refresh your browser.</span><span class="sxs-lookup"><span data-stu-id="37727-119">If you're having trouble downloading the certificate, refresh your browser.</span></span>

7. <span data-ttu-id="37727-120">Revenir à Microsoft 365, puis sélectionnez **Suivant** pour obtenir la   page Télécharger certificat   **APNS.**  </span><span class="sxs-lookup"><span data-stu-id="37727-120">Go back to Microsoft 365, and select **Next**  to get to the  **Upload APNS certificate** page.</span></span>

8. <span data-ttu-id="37727-121"> Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.</span><span class="sxs-lookup"><span data-stu-id="37727-121">Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.</span></span>

9. <span data-ttu-id="37727-122">Sélectionnez  **Terminer.**</span><span class="sxs-lookup"><span data-stu-id="37727-122">Select  **Finish**.</span></span>

<span data-ttu-id="37727-123">Pour terminer l’installation, revenir au Centre de sécurité  \*\*\*\* et conformité & stratégies de sécurité >Gestion des paramètres de gestion   >  \*\*\*\*   >  **des périphériques.**</span><span class="sxs-lookup"><span data-stu-id="37727-123">To complete setup, go back to the Security & Compliance Center > **Security policies** > **Device management** > **Manage settings**.</span></span>
