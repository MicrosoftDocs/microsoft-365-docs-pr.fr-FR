---
title: Microsoft Teams
description: Comment teams est-il installé sur les appareils et mis à jour par la suite ?
keywords: Microsoft Managed Desktop, Microsoft 365, service, documentation, applications, applications métiers, applications métier
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.author: jaimeo
manager: laurawi
ms.topic: article
audience: ITPro
ms.openlocfilehash: ea2ef7637a8d360e3b598aec4852425d977ae4ec
ms.sourcegitcommit: dffb9b72acd2e0bd286ff7e79c251e7ec6e8ecae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2020
ms.locfileid: "47950917"
---
# <a name="microsoft-teams"></a><span data-ttu-id="7b4a0-104">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7b4a0-104">Microsoft Teams</span></span>

<span data-ttu-id="7b4a0-105">[Teams](https://www.microsoft.com/microsoft-365/microsoft-teams/group-chat-software) est une [application de messagerie](https://support.microsoft.com/office/microsoft-teams-basics-6d5f52e6-5306-4096-ac24-c3082b79eaf0) pour votre organisation qui fournit également un espace de travail pour la collaboration et la communication en temps réel, les réunions et le partage de fichiers et d’applications.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-105">[Teams](https://www.microsoft.com/microsoft-365/microsoft-teams/group-chat-software) is a [messaging app](https://support.microsoft.com/office/microsoft-teams-basics-6d5f52e6-5306-4096-ac24-c3082b79eaf0) for your organization that also provides a workspace for real-time collaboration and communication, meetings, and file and app sharing.</span></span>

## <a name="initial-deployment"></a><span data-ttu-id="7b4a0-106">Déploiement initial</span><span class="sxs-lookup"><span data-stu-id="7b4a0-106">Initial deployment</span></span>

<span data-ttu-id="7b4a0-107">La plupart des fournisseurs de matériel n’incluent pas encore teams dans leurs images, de sorte que Microsoft Managed Desktop déploie teams sur vos appareils à l’aide de Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-107">Most hardware vendors don't yet include Teams as a part of their images, so Microsoft Managed Desktop deploys Teams to your devices by using Microsoft Intune.</span></span> <span data-ttu-id="7b4a0-108">Le [package Teams. msi](https://docs.microsoft.com/MicrosoftTeams/msi-deployment#how-the-microsoft-teams-msi-package-works) est installé sur tous les appareils gérés afin de s’assurer que Microsoft teams est prêt à utiliser tous les utilisateurs qui se connectent à un appareil.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-108">All managed devices have the [Teams .msi package](https://docs.microsoft.com/MicrosoftTeams/msi-deployment#how-the-microsoft-teams-msi-package-works) installed, ensuring that all users who sign in to a device have Microsoft Teams ready to use.</span></span> <span data-ttu-id="7b4a0-109">Une fois l’installation du package terminée, teams démarre automatiquement et ajoute un raccourci vers le bureau.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-109">When the package first finishes installing, Teams automatically starts and adds a shortcut to the desktop.</span></span>

### <a name="microsoft-intune-changes"></a><span data-ttu-id="7b4a0-110">Modifications apportées à Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="7b4a0-110">Microsoft Intune changes</span></span>

<span data-ttu-id="7b4a0-111">Microsoft Managed Desktop ajoute deux applications à votre organisation Azure AD pour Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-111">Microsoft Managed Desktop adds two applications to your Azure AD organization for Microsoft Teams.</span></span> <span data-ttu-id="7b4a0-112">Elles sont déployées sur les clients 64 bits ou 32 bits en fonction du périphérique :</span><span class="sxs-lookup"><span data-stu-id="7b4a0-112">They are deployed to either 64-bit or 32-bit clients as appropriate for the device:</span></span>  

- <span data-ttu-id="7b4a0-113">Espace de travail moderne – programme d’installation x64 à l’échelle de l’ordinateur teams</span><span class="sxs-lookup"><span data-stu-id="7b4a0-113">Modern Workplace – Teams Machine Wide Installer x64</span></span>  
- <span data-ttu-id="7b4a0-114">Espace de travail moderne – programme d’installation de l’ordinateur teams x32</span><span class="sxs-lookup"><span data-stu-id="7b4a0-114">Modern Workplace – Teams Machine Wide Installer x32</span></span>

## <a name="updates"></a><span data-ttu-id="7b4a0-115">Mises à jour</span><span class="sxs-lookup"><span data-stu-id="7b4a0-115">Updates</span></span>

<span data-ttu-id="7b4a0-116">Teams suit un chemin de mise à jour distinct de Microsoft 365 Apps for Enterprise et le client de bureau lui-même est automatiquement mis à jour.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-116">Teams follows a separate update path from Microsoft 365 Apps for enterprise and the desktop client updates itself automatically.</span></span> <span data-ttu-id="7b4a0-117">Teams vérifie les mises à jour toutes les quelques heures, les télécharge, puis attend que l’ordinateur soit inactif avant d’installer la mise à jour en silence.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-117">Teams checks for updates every few hours, downloads them, and then waits for the computer to be idle before silently installing the update.</span></span>  

<span data-ttu-id="7b4a0-118">Le groupe de produits Teams ne permet pas aux administrateurs de contrôler les mises à jour, de sorte que Microsoft Managed Desktop utilise le [canal de mise à jour automatique standard](https://docs.microsoft.com/microsoftteams/teams-client-update#can-admins-deploy-updates-instead-of-teams-auto-updating).</span><span class="sxs-lookup"><span data-stu-id="7b4a0-118">The Teams product group doesn't allow admins to control updates, so Microsoft Managed Desktop uses the [standard automatic update channel](https://docs.microsoft.com/microsoftteams/teams-client-update#can-admins-deploy-updates-instead-of-teams-auto-updating).</span></span>

### <a name="manually-updating-teams"></a><span data-ttu-id="7b4a0-119">Mise à jour manuelle de teams</span><span class="sxs-lookup"><span data-stu-id="7b4a0-119">Manually updating Teams</span></span>

<span data-ttu-id="7b4a0-120">Les utilisateurs individuels peuvent également télécharger des mises à jour en sélectionnant **vérifier les mises à jour**   dans le **Profile**   menu déroulant Profil dans le coin supérieur droit de l’application.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-120">Individual users can also download updates by selecting **Check for updates** on the **Profile** drop-down menu at the top right of the app.</span></span> <span data-ttu-id="7b4a0-121">Si une mise à jour est disponible, elle est téléchargée et installée silencieusement lorsque l’ordinateur est inactif.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-121">If an update is available, it will be downloaded and silently installed when the computer is idle.</span></span>

## <a name="delivery-optimization-of-updates"></a><span data-ttu-id="7b4a0-122">Optimisation de la distribution des mises à jour</span><span class="sxs-lookup"><span data-stu-id="7b4a0-122">Delivery optimization of updates</span></span>

<span data-ttu-id="7b4a0-123">L’optimisation de la remise des mises à jour de teams est activée par défaut et ne nécessite aucune action de la part des administrateurs ou des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-123">Delivery optimization for Teams updates is turned on by default and requires no action from admins or users.</span></span> 