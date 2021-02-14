---
title: Microsoft Teams
description: Installation de Teams sur les appareils et mise à jour par la suite
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation, applications, applications métier, applications métier
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
# <a name="microsoft-teams"></a><span data-ttu-id="11c28-104">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="11c28-104">Microsoft Teams</span></span>

<span data-ttu-id="11c28-105">[Teams](https://www.microsoft.com/microsoft-365/microsoft-teams/group-chat-software) est une application [de](https://support.microsoft.com/office/microsoft-teams-basics-6d5f52e6-5306-4096-ac24-c3082b79eaf0) messagerie pour votre organisation qui fournit également un espace de travail pour la collaboration et la communication en temps réel, les réunions et le partage de fichiers et d’applications.</span><span class="sxs-lookup"><span data-stu-id="11c28-105">[Teams](https://www.microsoft.com/microsoft-365/microsoft-teams/group-chat-software) is a [messaging app](https://support.microsoft.com/office/microsoft-teams-basics-6d5f52e6-5306-4096-ac24-c3082b79eaf0) for your organization that also provides a workspace for real-time collaboration and communication, meetings, and file and app sharing.</span></span>

## <a name="initial-deployment"></a><span data-ttu-id="11c28-106">Déploiement initial</span><span class="sxs-lookup"><span data-stu-id="11c28-106">Initial deployment</span></span>

<span data-ttu-id="11c28-107">La plupart des fournisseurs de matériel n’incluent pas encore Teams dans le cadre de leurs images. Ainsi, Bureau géré Microsoft déploie Teams sur vos appareils à l’aide de Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="11c28-107">Most hardware vendors don't yet include Teams as a part of their images, so Microsoft Managed Desktop deploys Teams to your devices by using Microsoft Intune.</span></span> <span data-ttu-id="11c28-108">Sur tous les appareils gérés, le [package .msi Teams](https://docs.microsoft.com/MicrosoftTeams/msi-deployment#how-the-microsoft-teams-msi-package-works) est installé, ce qui garantit que Microsoft Teams est prêt à être utilisé par tous les utilisateurs qui se connectent à un appareil.</span><span class="sxs-lookup"><span data-stu-id="11c28-108">All managed devices have the [Teams .msi package](https://docs.microsoft.com/MicrosoftTeams/msi-deployment#how-the-microsoft-teams-msi-package-works) installed, ensuring that all users who sign in to a device have Microsoft Teams ready to use.</span></span> <span data-ttu-id="11c28-109">Lorsque le package a terminé l’installation pour la première fois, Teams démarre automatiquement et ajoute un raccourci au Bureau.</span><span class="sxs-lookup"><span data-stu-id="11c28-109">When the package first finishes installing, Teams automatically starts and adds a shortcut to the desktop.</span></span>

### <a name="microsoft-intune-changes"></a><span data-ttu-id="11c28-110">Modifications apportées à Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="11c28-110">Microsoft Intune changes</span></span>

<span data-ttu-id="11c28-111">Bureau géré Microsoft ajoute deux applications à votre organisation Azure AD pour Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="11c28-111">Microsoft Managed Desktop adds two applications to your Azure AD organization for Microsoft Teams.</span></span> <span data-ttu-id="11c28-112">Ils sont déployés sur des clients 64 bits ou 32 bits selon les besoins de l’appareil :</span><span class="sxs-lookup"><span data-stu-id="11c28-112">They are deployed to either 64-bit or 32-bit clients as appropriate for the device:</span></span>  

- <span data-ttu-id="11c28-113">Espace de travail moderne – Programme d’installation à l’échelle de l’ordinateur Teams x64</span><span class="sxs-lookup"><span data-stu-id="11c28-113">Modern Workplace – Teams Machine Wide Installer x64</span></span>  
- <span data-ttu-id="11c28-114">Espace de travail moderne – Programme d’installation à l’échelle de l’ordinateur Teams x32</span><span class="sxs-lookup"><span data-stu-id="11c28-114">Modern Workplace – Teams Machine Wide Installer x32</span></span>

## <a name="updates"></a><span data-ttu-id="11c28-115">Mises à jour</span><span class="sxs-lookup"><span data-stu-id="11c28-115">Updates</span></span>

<span data-ttu-id="11c28-116">Teams suit un chemin de mise à jour distinct de Microsoft 365 Apps for enterprise et le client de bureau se met à jour automatiquement.</span><span class="sxs-lookup"><span data-stu-id="11c28-116">Teams follows a separate update path from Microsoft 365 Apps for enterprise and the desktop client updates itself automatically.</span></span> <span data-ttu-id="11c28-117">Teams recherche les mises à jour toutes les heures, les télécharge, puis attend que l’ordinateur soit inactif avant d’installer silencieusement la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="11c28-117">Teams checks for updates every few hours, downloads them, and then waits for the computer to be idle before silently installing the update.</span></span>  

<span data-ttu-id="11c28-118">Le groupe de produits Teams n’autorise pas les administrateurs à contrôler les mises à jour, donc Bureau géré Microsoft utilise le canal de mise à jour [automatique standard.](https://docs.microsoft.com/microsoftteams/teams-client-update#can-admins-deploy-updates-instead-of-teams-auto-updating)</span><span class="sxs-lookup"><span data-stu-id="11c28-118">The Teams product group doesn't allow admins to control updates, so Microsoft Managed Desktop uses the [standard automatic update channel](https://docs.microsoft.com/microsoftteams/teams-client-update#can-admins-deploy-updates-instead-of-teams-auto-updating).</span></span>

### <a name="manually-updating-teams"></a><span data-ttu-id="11c28-119">Mise à jour manuelle de Teams</span><span class="sxs-lookup"><span data-stu-id="11c28-119">Manually updating Teams</span></span>

<span data-ttu-id="11c28-120">Les utilisateurs individuels peuvent également télécharger les mises à jour en sélectionnant Vérifier les mises à jour dans le menu déroulant Profil en   haut à droite de \*\*\*\*   l’application.</span><span class="sxs-lookup"><span data-stu-id="11c28-120">Individual users can also download updates by selecting **Check for updates** on the **Profile** drop-down menu at the top right of the app.</span></span> <span data-ttu-id="11c28-121">Si une mise à jour est disponible, elle est téléchargée et installée en mode silencieux lorsque l’ordinateur est inactif.</span><span class="sxs-lookup"><span data-stu-id="11c28-121">If an update is available, it will be downloaded and silently installed when the computer is idle.</span></span>

## <a name="delivery-optimization-of-updates"></a><span data-ttu-id="11c28-122">Optimisation de la distribution des mises à jour</span><span class="sxs-lookup"><span data-stu-id="11c28-122">Delivery optimization of updates</span></span>

<span data-ttu-id="11c28-123">L’optimisation de la distribution pour les mises à jour Teams est désactivée par défaut et ne nécessite aucune action de la part des administrateurs ou des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="11c28-123">Delivery optimization for Teams updates is turned on by default and requires no action from admins or users.</span></span> 