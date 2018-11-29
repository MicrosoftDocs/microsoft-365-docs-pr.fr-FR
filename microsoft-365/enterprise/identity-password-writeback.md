---
title: 'Étape 9 : simplifier les mises à jour des mots de passe'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 03/01/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom: ''
description: Comprendre et configurer l’écriture différée de mot de passe pour les environnements hybrides.
ms.openlocfilehash: 55da101ca729de804ae76dafbe35a46969af9d8d
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867021"
---
# <a name="step-9-simplify-password-updates"></a><span data-ttu-id="37336-103">Étape 9 : simplifier les mises à jour des mots de passe</span><span class="sxs-lookup"><span data-stu-id="37336-103">Step 9: Simplify password updates</span></span>

<span data-ttu-id="37336-104">*Cette étape est facultative pour les environnements hybrides et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="37336-104">*This step is optional for hybrid environments and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon-small.png)

<span data-ttu-id="37336-p101">À cette étape, vous allez autoriser les utilisateurs à réinitialiser leur mot de passe via Azure Active Directory (AD). Ils seront ensuite copiés sur votre instance Windows Server Active Directory (AD) locale. Ce processus est appelé écriture différée de mot de passe. Avec l’écriture différée de mot de passe, les utilisateurs n’ont pas besoin de mettre à jour leur mot de passe localement via Windows Server AD où les comptes d’utilisateurs et leurs attributs sont stockés. Cette étape est utile aux utilisateurs itinérants ou distants qui ne disposent pas d’une connexion d’accès à distance au réseau local.</span><span class="sxs-lookup"><span data-stu-id="37336-p101">In this step, you'll allow users to reset their passwords through Azure Active Directory (AD), which is then replicated to your local Windows Server Active Directory (AD). This process is known as password writeback. With password writeback, users don’t need to update their passwords through the on-premises Windows Server AD where user accounts and their attributes are stored. This is valuable to roaming or remote users who do not have a remote access connection to the on-premises network.</span></span>

<span data-ttu-id="37336-109">L’écriture différée de mot de passe est requise pour exploiter entièrement les fonctionnalités de la protection des identités, comme obliger les utilisateurs à modifier leur mot de passe en local lorsqu’un risque élevé de compromission de compte a été détecté.</span><span class="sxs-lookup"><span data-stu-id="37336-109">Password writeback is required to fully utilize Identity Protection feature capabilities, such as requiring users to change their on-premises passwords when there has been a high risk of account compromise detected.</span></span>

<span data-ttu-id="37336-110">Pour obtenir plus d’informations et les instructions de configuration, consultez l’article [Azure AD SSPR avec l’écriture différée de mot de passe](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-writeback).</span><span class="sxs-lookup"><span data-stu-id="37336-110">For additional information and configuration instructions, see [Azure AD SSPR with password writeback](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-writeback).</span></span>

>[!Note]
><span data-ttu-id="37336-p102">Procédez à la mise à niveau vers la dernière version d’Azure AD Connect pour vous assurer la meilleure expérience possible et les nouvelles fonctionnalités dès leur diffusion. Pour obtenir plus d’informations, consultez l’article [Installation personnalisée d’Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-get-started-custom).</span><span class="sxs-lookup"><span data-stu-id="37336-p102">Upgrade to the latest version of Azure AD Connect to ensure the best possible experience and new features as they are released. For more information, see [Custom installation of Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-get-started-custom).</span></span>
>

<span data-ttu-id="37336-113">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-pw-writeback) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="37336-113">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-pw-writeback) for this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="37336-114">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="37336-114">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step10.png)| [<span data-ttu-id="37336-115">Simplifier la connexion de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="37336-115">Simplify user sign-in</span></span>](identity-single-sign-on.md) |

