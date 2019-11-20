---
title: Configurer l’authentification multifacteur
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- M365-identity-device-management
ms.custom:
- MiniMaven
- MSB365
- OKR_SMB_M365
search.appverid:
- BCS160
- MET150
description: Configurez l’authentification multifacteur pour Microsoft 365 Business.
ms.openlocfilehash: 59a3ff7a9494ccfc44fa701c6f605a9bd9eeafcf
ms.sourcegitcommit: 5d11f516e78ea4a74145e19ba2300f0792c8bac1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/19/2019
ms.locfileid: "38715056"
---
# <a name="multi-factor-authentication"></a><span data-ttu-id="eab1d-103">	Authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="eab1d-103">Multi-factor authentication</span></span>

<span data-ttu-id="eab1d-104">L’authentification multifacteur (MFA) exige que les utilisateurs se connectent avec une deuxième méthode pour vérifier leur identité avec un appel téléphonique ou avec une application d’authentificateur.</span><span class="sxs-lookup"><span data-stu-id="eab1d-104">Multi-factor authentication (MFA) requires users to sign in with a second method to verify their identity with a phone call or with an authenticator app.</span></span>

## <a name="set-up-mfa-in-the-microsoft-365-admin-center"></a><span data-ttu-id="eab1d-105">Configurer MFA dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="eab1d-105">Set up MFA in the Microsoft 365 admin center</span></span>

<span data-ttu-id="eab1d-106">[![Étiquette vous informant le centre d’administration est en train de changer et vous pouvez trouver plus de détails à ce sujet à l’adresse aka.ms/aboutM365preview.](media/m365admincenterchanging.png)](https://docs.microsoft.com/office365/admin/microsoft-365-admin-center-preview)</span><span class="sxs-lookup"><span data-stu-id="eab1d-106">[![Label to let you know the admin center is changing and you can find more details at aka.ms/aboutM365preview.](media/m365admincenterchanging.png)](https://docs.microsoft.com/office365/admin/microsoft-365-admin-center-preview)</span></span>

1. <span data-ttu-id="eab1d-107">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) à l’aide de vos informations d’identification d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="eab1d-107">Sign in to [Microsoft 365 admin center](https://admin.microsoft.com) by using your global admin credentials.</span></span> 
2. <span data-ttu-id="eab1d-108">Dans le volet de navigation de gauche, sélectionnez **configuration**.</span><span class="sxs-lookup"><span data-stu-id="eab1d-108">On the left nav, choose **Setup**.</span></span>
3. <span data-ttu-id="eab1d-109">Sur la page installation, choisissez **affichage** sur la carte **Multi-Factor Authentication (MFA)** .</span><span class="sxs-lookup"><span data-stu-id="eab1d-109">On the Setup page, choose **View** on the **Turn on multi-factor authentication (MFA)** card.</span></span>
4. <span data-ttu-id="eab1d-110">Sur la page **activer l’authentification multifacteur** , sélectionnez **prise en main**ou **gérer** si vous avez déjà configuré MFA et souhaitez apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="eab1d-110">On the **Turn on MFA** page, choose **Get started**, or **Manage** if you have already set up MFA and want to make changes.</span></span> 

  <span data-ttu-id="eab1d-111">:::image type="content" source="media/turnonmfa.png" alt-text="Capture d’écran de l’activation de la page MFA.":::</span><span class="sxs-lookup"><span data-stu-id="eab1d-111">:::image type="content" source="media/turnonmfa.png" alt-text="Screenshot of turn on MFA page.":::</span></span>

5. <span data-ttu-id="eab1d-112">Dans le panneau **renforcer la sécurité** de la connexion, vérifiez les deux options **exiger une authentification multifacteur pour les administrateurs**, puis choisissez **créer une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="eab1d-112">On the **Strengthen sign-in security** panel, check both or one of **Require multi-factor authentication for admins**, and then choose **Create policy**.</span></span>
