---
title: Créer un certificat APNs pour les appareils iOS
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
description: Gérer les appareils iOS dans la sécurité et la mobilité de base.
ms.openlocfilehash: 8b41c1c6c891a5d6cb98a6a381c65aa0310a1761
ms.sourcegitcommit: 2179abfe0b7a8bea917eb1c1057ed3795bdf91e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "47336871"
---
# <a name="create-an-apns-certificate-for-ios-devices"></a><span data-ttu-id="394c5-103">Créer un certificat APNs pour les appareils iOS</span><span class="sxs-lookup"><span data-stu-id="394c5-103">Create an APNs certificate for iOS devices</span></span>

<span data-ttu-id="394c5-104">Pour gérer les appareils iOS tels que iPad et iPhone dans la sécurité et la mobilité de base, créez un certificat APNs.</span><span class="sxs-lookup"><span data-stu-id="394c5-104">To manage iOS devices such as iPads and iPhones in Basic Mobility and Security, create an APNs certificate.</span></span>

1. <span data-ttu-id="394c5-105">Connectez-vous à Microsoft 365 avec votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="394c5-105">Sign in to Microsoft 365 with your global admin account.</span></span>
    
2. <span data-ttu-id="394c5-106">Dans votre navigateur, tapez  [https://protection.office.com](https://protection.office.com/) .</span><span class="sxs-lookup"><span data-stu-id="394c5-106">In your browser, type [https://protection.office.com](https://protection.office.com/).</span></span>
    
3. <span data-ttu-id="394c5-107">Sélectionnez gestion des périphériques de  **protection contre la perte de données**   >  **Device management**, puis choisissez le **certificat APNs pour les appareils iOS**.</span><span class="sxs-lookup"><span data-stu-id="394c5-107">Select  **Data loss prevention** > **Device management**, and choose **APNs Certificate for iOS devices**.</span></span>    

4. <span data-ttu-id="394c5-108">Sur la page Paramètres du certificat de notification de type Apple, choisissez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="394c5-108">On the Apple Push Notification Certificate Settings page, choose **Next**.</span></span>
    
5. <span data-ttu-id="394c5-109">Sélectionnez télécharger votre fichier CSR et enregistrez la demande de signature de certificat sur un emplacement de votre ordinateur dont vous vous souviendrez.</span><span class="sxs-lookup"><span data-stu-id="394c5-109">Select Download your CSR file and save the certificate signing request to somewhere on your computer that you'll remember.</span></span> <span data-ttu-id="394c5-110">Sélectionnez  **suivant**.</span><span class="sxs-lookup"><span data-stu-id="394c5-110">Select  **Next**.</span></span>
    
6. <span data-ttu-id="394c5-111">Sur la page créer un certificat APNs :</span><span class="sxs-lookup"><span data-stu-id="394c5-111">On the Create an APNs certificate page:</span></span>  

    1. <span data-ttu-id="394c5-112">Sélectionnez Apple APNS Portal pour ouvrir le portail Appled Certificates.</span><span class="sxs-lookup"><span data-stu-id="394c5-112">Select  Apple APNS Portal to open the Apple Push Certificates Portal.</span></span>
    
    2. <span data-ttu-id="394c5-113">Sign in with an Apple ID.</span><span class="sxs-lookup"><span data-stu-id="394c5-113">Sign in with an Apple ID.</span></span>   

    >[!IMPORTANT]
    ><span data-ttu-id="394c5-p102">Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate.</span><span class="sxs-lookup"><span data-stu-id="394c5-p102">Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate.</span></span>

    3. <span data-ttu-id="394c5-116">Sélectionnez  **créer un certificat**   et accepter les conditions d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="394c5-116">Select  **Create a Certificate**  and accept the Terms of Use.</span></span>
    
    4. <span data-ttu-id="394c5-117">Accédez à la demande de signature de certificat que vous avez téléchargée sur votre ordinateur à partir de Microsoft 365, puis sélectionnez **Télécharger**.</span><span class="sxs-lookup"><span data-stu-id="394c5-117">Browse to the certificate signing request you downloaded to your computer from Microsoft 365, and select **Upload**.</span></span>
    
        <span data-ttu-id="394c5-118">Téléchargez le certificat APNs créé par le portail de certificats poussés Apple sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="394c5-118">Download the APNs certificate created by the Apple Push Certificate Portal to your computer.</span></span>
    
       >[!TIP]
       ><span data-ttu-id="394c5-119">If you're having trouble downloading the certificate, refresh your browser.</span><span class="sxs-lookup"><span data-stu-id="394c5-119">If you're having trouble downloading the certificate, refresh your browser.</span></span>

7. <span data-ttu-id="394c5-120">Revenez à Microsoft 365, puis sélectionnez **suivant**   pour accéder à la page  **Télécharger le certificat APNs**   .</span><span class="sxs-lookup"><span data-stu-id="394c5-120">Go back to Microsoft 365, and select **Next**  to get to the  **Upload APNS certificate** page.</span></span>
    
8. <span data-ttu-id="394c5-121"> Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.</span><span class="sxs-lookup"><span data-stu-id="394c5-121">Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.</span></span>
    
9. <span data-ttu-id="394c5-122">Sélectionnez  **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="394c5-122">Select  **Finish**.</span></span>
    
<span data-ttu-id="394c5-123">Pour terminer l’installation, revenez au centre de sécurité & conformité >gestion des périphériques de  **sécurité**   >  **Device management**   >  **gérer les paramètres**.</span><span class="sxs-lookup"><span data-stu-id="394c5-123">To complete setup, go back to the Security & Compliance Center > **Security policies** > **Device management** > **Manage settings**.</span></span>
