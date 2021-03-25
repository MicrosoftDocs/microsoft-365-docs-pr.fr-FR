---
title: Synchronisation des certificats utilisateur vers Office 365 pour S/MIME
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: 12/09/2016
audience: ITPro
ms.topic: how-to
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 351c932e-99c1-4512-a6e8-788e90b7838f
ms.custom:
- seo-marvel-apr2020
description: Dans cet article, vous allez apprendre à publier les certificats appropriés dans Office 365 avant d’envoyer des messages protégés par S/MIME dans Exchange Online.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 387f9f405afd45254c6568aa92334a7ee5b4171f
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51204623"
---
# <a name="sync-user-certificates-to-office-365-for-smime"></a><span data-ttu-id="c22e6-103">Synchronisation des certificats utilisateur vers Office 365 pour S/MIME</span><span class="sxs-lookup"><span data-stu-id="c22e6-103">Sync user certificates to Office 365 for S/MIME</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="c22e6-104">Pour qu’une personne puisse envoyer des messages protégés par S/MIME dans Exchange Online, les certificats appropriés doivent être mis en place.</span><span class="sxs-lookup"><span data-stu-id="c22e6-104">Before anyone can send S/MIME-protected messages in Exchange Online, the appropriate certificates must be set up.</span></span> <span data-ttu-id="c22e6-105">Pour envoyer des messages chiffrés via Exchange Online, l’application de messagerie de l’expéditeur utilise le certificat public du destinataire pour chiffrer le message.</span><span class="sxs-lookup"><span data-stu-id="c22e6-105">To send encrypted messages through Exchange Online, the sender's email app uses the public certificate of the recipient to encrypt the message.</span></span> <span data-ttu-id="c22e6-106">Ce certificat X.509 public doit être publié sur Office 365.</span><span class="sxs-lookup"><span data-stu-id="c22e6-106">This public X.509 certificate has to be published to Office 365.</span></span>

## <a name="to-sync-certificates-that-support-smime"></a><span data-ttu-id="c22e6-107">Synchronisation de certificats prenant en charge S/MIME</span><span class="sxs-lookup"><span data-stu-id="c22e6-107">To Sync certificates that support S/MIME</span></span>

<span data-ttu-id="c22e6-108">Commencez la configuration de S/MIME en émettant des certificats et en les publiant dans votre service de domaine Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="c22e6-108">Begin setting up S/MIME by issuing certificates and publishing them in your local Active Directory Domain Service.</span></span> <span data-ttu-id="c22e6-109">Pour plus d'informations, reportez-vous à la rubrique [Vue d'ensemble des services de certificats Active Directory](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831740(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="c22e6-109">For more information, see [Active Directory Certificate Services Overview](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831740(v=ws.11)).</span></span>

<span data-ttu-id="c22e6-110">Une fois vos certificats publiés, utilisez l’outil Azure AD Connect pour synchroniser les données utilisateur de votre environnement Exchange local avec Office 365.</span><span class="sxs-lookup"><span data-stu-id="c22e6-110">After your certificates are published, use the Azure AD Connect tool to synchronize user data from your on-premises Exchange environment to Office 365.</span></span> <span data-ttu-id="c22e6-111">Pour plus d’informations sur ce processus, voir synchronisation Azure AD Connect : Comprendre [et personnaliser la synchronisation.](/azure/active-directory/hybrid/how-to-connect-sync-whatis)</span><span class="sxs-lookup"><span data-stu-id="c22e6-111">For more information on this process, see [Azure AD Connect sync: Understand and customize synchronization](/azure/active-directory/hybrid/how-to-connect-sync-whatis).</span></span>

<span data-ttu-id="c22e6-112">En plus de synchroniser d’autres données d’annuaire, à des fins S/MIME, l’outil synchronise les attributs  **userCertificate** et **userSMIMECertificate** pour chaque objet utilisateur afin que les données soient utilisées pour signer et chiffrer des messages.</span><span class="sxs-lookup"><span data-stu-id="c22e6-112">Along with synchronizing other directory data, for S/MIME purposes, the tool will synchronize the  **userCertificate** and **userSMIMECertificate** attributes for each user object so the data can be used to sign and encrypt messages.</span></span>

## <a name="more-information"></a><span data-ttu-id="c22e6-113">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="c22e6-113">More Information</span></span>

[<span data-ttu-id="c22e6-114">S/MIME pour la signature et le chiffrement des messages</span><span class="sxs-lookup"><span data-stu-id="c22e6-114">S/MIME for message signing and encryption</span></span>](s-mime-for-message-signing-and-encryption.md)

[<span data-ttu-id="c22e6-115">Qu’est-ce qu’Azure AD Connect ?</span><span class="sxs-lookup"><span data-stu-id="c22e6-115">What is Azure AD Connect?</span></span>](/azure/active-directory/hybrid/whatis-azure-ad-connect)