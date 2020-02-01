---
title: Synchronisation des certificats utilisateur vers Office 365 pour S/MIME
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: 12/09/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 351c932e-99c1-4512-a6e8-788e90b7838f
description: Pour qu'une personne puisse envoyer des messages protégés par S/MIME, les certificats appropriés doivent être configurés. Pour envoyer des messages chiffrés par Exchange Online, le programme de messagerie de l'expéditeur utilise le certificat public du destinataire pour chiffrer le message. Ce certificat X.509 public doit être publié sur Office 365.
ms.openlocfilehash: a62af3b176f29ec2bd8c97ae02178c87b7a63544
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41598191"
---
# <a name="sync-user-certificates-to-office-365-for-smime"></a><span data-ttu-id="8e7e5-105">Synchronisation des certificats utilisateur vers Office 365 pour S/MIME</span><span class="sxs-lookup"><span data-stu-id="8e7e5-105">Sync user certificates to Office 365 for S/MIME</span></span>

<span data-ttu-id="8e7e5-106">Pour qu’une personne puisse envoyer des messages protégés par S/MIME dans Exchange Online, les certificats appropriés doivent être configurés.</span><span class="sxs-lookup"><span data-stu-id="8e7e5-106">Before anyone can send S/MIME-protected messages in Exchange Online, the appropriate certificates must be set up.</span></span> <span data-ttu-id="8e7e5-107">Pour envoyer des messages chiffrés via Exchange Online, l’application de messagerie de l’expéditeur utilise le certificat public du destinataire pour chiffrer le message.</span><span class="sxs-lookup"><span data-stu-id="8e7e5-107">To send encrypted messages through Exchange Online, the sender's email app uses the public certificate of the recipient to encrypt the message.</span></span> <span data-ttu-id="8e7e5-108">Ce certificat X.509 public doit être publié sur Office 365.</span><span class="sxs-lookup"><span data-stu-id="8e7e5-108">This public X.509 certificate has to be published to Office 365.</span></span>

## <a name="to-sync-certificates-that-support-smime"></a><span data-ttu-id="8e7e5-109">Synchronisation de certificats prenant en charge S/MIME</span><span class="sxs-lookup"><span data-stu-id="8e7e5-109">To Sync certificates that support S/MIME</span></span>

<span data-ttu-id="8e7e5-110">Commencez la configuration de S/MIME en émettant des certificats et en les publiant dans votre service de domaine Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="8e7e5-110">Begin setting up S/MIME by issuing certificates and publishing them in your local Active Directory Domain Service.</span></span> <span data-ttu-id="8e7e5-111">Pour plus d'informations, reportez-vous à la rubrique [Vue d'ensemble des services de certificats Active Directory](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831740(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="8e7e5-111">For more information, see [Active Directory Certificate Services Overview](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831740(v=ws.11)).</span></span>

<span data-ttu-id="8e7e5-112">Une fois vos certificats publiés, utilisez l’outil Azure AD Connect pour synchroniser les données utilisateur de votre environnement Exchange local avec Office 365.</span><span class="sxs-lookup"><span data-stu-id="8e7e5-112">After your certificates are published, use the Azure AD Connect tool to synchronize user data from your on-premises Exchange environment to Office 365.</span></span> <span data-ttu-id="8e7e5-113">Pour plus d’informations sur ce processus, reportez-vous à la rubrique session de [synchronisation Azure ad Connect : comprendre et personnaliser la synchronisation](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-whatis).</span><span class="sxs-lookup"><span data-stu-id="8e7e5-113">For more information on this process, see [Azure AD Connect sync: Understand and customize synchronization](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-whatis).</span></span>

<span data-ttu-id="8e7e5-114">En plus de synchroniser d’autres données d’annuaire, pour des raisons de S/MIME, l’outil synchronisera les attributs **userCertificate** et **userSMIMECertificate** pour chaque objet utilisateur afin que les données puissent être utilisées pour signer et chiffrer les messages.</span><span class="sxs-lookup"><span data-stu-id="8e7e5-114">Along with synchronizing other directory data, for S/MIME purposes, the tool will synchronize the  **userCertificate** and **userSMIMECertificate** attributes for each user object so the data can be used to sign and encrypt messages.</span></span>

## <a name="more-information"></a><span data-ttu-id="8e7e5-115">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="8e7e5-115">More Information</span></span>

[<span data-ttu-id="8e7e5-116">S/MIME pour la signature et le chiffrement des messages</span><span class="sxs-lookup"><span data-stu-id="8e7e5-116">S/MIME for message signing and encryption</span></span>](s-mime-for-message-signing-and-encryption.md)

[<span data-ttu-id="8e7e5-117">Qu’est-ce que Azure AD Connect ?</span><span class="sxs-lookup"><span data-stu-id="8e7e5-117">What is Azure AD Connect?</span></span>](https://docs.microsoft.com/azure/active-directory/hybrid/whatis-azure-ad-connect)
