---
title: Inscrire Microsoft Defender ATP pour les appareils macOS dans Jamf Pro
description: Inscrire Microsoft Defender ATP pour les appareils macOS dans Jamf Pro
keywords: microsoft, defender, atp, mac, installation, déployer, désinstallation, intune, jamfpro, macos,pépé, mojave, high sierra
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: ef6e387d4e945afb71f1fa6ecef9d78ba2d74a55
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51185682"
---
# <a name="enroll-microsoft-defender-for-endpoint-for-macos-devices-into-jamf-pro"></a><span data-ttu-id="40924-104">Inscrire Microsoft Defender pour endpoint pour les appareils macOS dans Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="40924-104">Enroll Microsoft Defender for Endpoint for macOS devices into Jamf Pro</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="40924-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="40924-105">**Applies to:**</span></span>
- [<span data-ttu-id="40924-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="40924-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="40924-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="40924-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="40924-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="40924-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="40924-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="40924-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

## <a name="enroll-macos-devices"></a><span data-ttu-id="40924-110">Inscrire des appareils macOS</span><span class="sxs-lookup"><span data-stu-id="40924-110">Enroll macOS devices</span></span>

<span data-ttu-id="40924-111">Il existe plusieurs méthodes pour être inscrit à JamF.</span><span class="sxs-lookup"><span data-stu-id="40924-111">There are multiple methods of getting enrolled to JamF.</span></span>

<span data-ttu-id="40924-112">Cet article vous guide sur deux méthodes :</span><span class="sxs-lookup"><span data-stu-id="40924-112">This article will guide you on two methods:</span></span>

- [<span data-ttu-id="40924-113">Méthode 1 : Invitations à l’inscription</span><span class="sxs-lookup"><span data-stu-id="40924-113">Method 1:  Enrollment Invitations</span></span>](#enrollment-method-1-enrollment-invitations)
- [<span data-ttu-id="40924-114">Méthode 2 : pré-étape des inscriptions</span><span class="sxs-lookup"><span data-stu-id="40924-114">Method 2:  Prestage Enrollments</span></span>](#enrollment-method-2-prestage-enrollments)

<span data-ttu-id="40924-115">Pour obtenir la liste complète, voir [à propos de l’inscription de l’ordinateur.](https://docs.jamf.com/9.9/casper-suite/administrator-guide/About_Computer_Enrollment.html)</span><span class="sxs-lookup"><span data-stu-id="40924-115">For a complete list, see [About Computer Enrollment](https://docs.jamf.com/9.9/casper-suite/administrator-guide/About_Computer_Enrollment.html).</span></span>


## <a name="enrollment-method-1-enrollment-invitations"></a><span data-ttu-id="40924-116">Méthode d’inscription 1 : invitations à l’inscription</span><span class="sxs-lookup"><span data-stu-id="40924-116">Enrollment Method 1: Enrollment Invitations</span></span>

1. <span data-ttu-id="40924-117">Dans le tableau de bord Jamf Pro, accédez aux **invitations d’inscription.**</span><span class="sxs-lookup"><span data-stu-id="40924-117">In the Jamf Pro dashboard, navigate to **Enrollment invitations**.</span></span>

    ![Image des paramètres de configuration1](images/a347307458d6a9bbfa88df7dbe15398f.png)

2. <span data-ttu-id="40924-119">Sélectionnez **+ Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="40924-119">Select **+ New**.</span></span>

    ![Fermeture d’une description de logo générée automatiquement](images/b6c7ad56d50f497c38fc14c1e315456c.png)

3. <span data-ttu-id="40924-121">Dans **Spécifier les destinataires de l'>** sous Adresses de messagerie, entrez les **adresses** de messagerie des destinataires.</span><span class="sxs-lookup"><span data-stu-id="40924-121">In **Specify Recipients for the Invitation** > under **Email Addresses** enter the e-mail address(es) of the recipients.</span></span>

    ![Image des paramètres de configuration2](images/718b9d609f9f77c8b13ba88c4c0abe5d.png)

    ![Image des paramètres de configuration3](images/ae3597247b6bc7c5347cf56ab1e820c0.png)

    <span data-ttu-id="40924-124">Par exemple : janedoe@contoso.com</span><span class="sxs-lookup"><span data-stu-id="40924-124">For example: janedoe@contoso.com</span></span>

    ![Image des paramètres de configuration4](images/4922c0fcdde4c7f73242b13bf5e35c19.png)

4. <span data-ttu-id="40924-126">Configurez le message pour l’invitation.</span><span class="sxs-lookup"><span data-stu-id="40924-126">Configure the message for the invitation.</span></span>

    ![Image des paramètres de configuration5](images/ce580aec080512d44a37ff8e82e5c2ac.png)

    ![Image des paramètres de configuration6](images/5856b765a6ce677caacb130ca36b1a62.png)

    ![Image des paramètres de configuration7](images/3ced5383a6be788486d89d407d042f28.png)

    ![Image des paramètres de configuration8](images/54be9c6ed5b24cebe628dc3cd9ca4089.png)

## <a name="enrollment-method-2-prestage-enrollments"></a><span data-ttu-id="40924-131">Enrollment Method 2: Prestage Enrollments</span><span class="sxs-lookup"><span data-stu-id="40924-131">Enrollment Method 2: Prestage Enrollments</span></span>

1. <span data-ttu-id="40924-132">Dans le tableau de bord Jamf Pro, accédez à **la préparation des inscriptions.**</span><span class="sxs-lookup"><span data-stu-id="40924-132">In the Jamf Pro dashboard, navigate to **Prestage enrollments**.</span></span>

    ![Image des paramètres de configuration9](images/6fd0cb2bbb0e60a623829c91fd0826ab.png)

2. <span data-ttu-id="40924-134">Suivez les instructions dans [Computer PreStage Enrollments](https://docs.jamf.com/9.9/casper-suite/administrator-guide/Computer_PreStage_Enrollments.html).</span><span class="sxs-lookup"><span data-stu-id="40924-134">Follow the instructions in [Computer PreStage Enrollments](https://docs.jamf.com/9.9/casper-suite/administrator-guide/Computer_PreStage_Enrollments.html).</span></span>

## <a name="enroll-macos-device"></a><span data-ttu-id="40924-135">Inscrire un appareil macOS</span><span class="sxs-lookup"><span data-stu-id="40924-135">Enroll macOS device</span></span>

1. <span data-ttu-id="40924-136">Sélectionnez **Continuer** et installez le certificat d’ac à partir d’une **fenêtre Préférences système.**</span><span class="sxs-lookup"><span data-stu-id="40924-136">Select **Continue** and install the CA certificate from a **System Preferences** window.</span></span>

    ![Image de Jamf Pro enrollment1](images/jamfpro-ca-certificate.png)

2. <span data-ttu-id="40924-138">Une fois le certificat d’ac installé, revenir à la fenêtre du navigateur, puis **sélectionnez Continuer** et installer le profil MDM.</span><span class="sxs-lookup"><span data-stu-id="40924-138">Once CA certificate is installed, return to the browser window and select **Continue** and install the MDM profile.</span></span> 

    ![Image de Jamf Pro enrollment2](images/jamfpro-install-mdm-profile.png)

3. <span data-ttu-id="40924-140">Sélectionnez **Autoriser** les téléchargements à partir de JAMF.</span><span class="sxs-lookup"><span data-stu-id="40924-140">Select **Allow** to downloads from JAMF.</span></span>

    ![Image de Jamf Pro enrollment3](images/jamfpro-download.png)

4. <span data-ttu-id="40924-142">Sélectionnez **Continuer** pour poursuivre l’installation du profil MDM.</span><span class="sxs-lookup"><span data-stu-id="40924-142">Select **Continue** to proceed with the MDM Profile installation.</span></span> 

    ![Image de Jamf Pro enrollment4](images/jamfpro-install-mdm.png)

5. <span data-ttu-id="40924-144">Sélectionnez **Continuer** à installer le profil MDM.</span><span class="sxs-lookup"><span data-stu-id="40924-144">Select **Continue** to install the MDM Profile.</span></span>

    ![Image de Jamf Pro enrollment5](images/jamfpro-mdm-unverified.png)

6. <span data-ttu-id="40924-146">Sélectionnez **Continuer**  pour terminer la configuration.</span><span class="sxs-lookup"><span data-stu-id="40924-146">Select **Continue**  to complete the configuration.</span></span> 

    ![Image de Jamf Pro enrollment6](images/jamfpro-mdm-profile.png)
