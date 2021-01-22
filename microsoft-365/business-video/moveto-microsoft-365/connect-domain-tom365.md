---
title: Connecter votre domaine à Microsoft 365
f1.keywords:
- NOCSH
ms.author: twerner
author: twernermsft
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
ms.custom:
- AdminSurgePortfolio
- adminvideo
- okr_smb
monikerRange: o365-worldwide
search.appverid:
- BCS160
- MET150
- MOE150
description: Découvrez comment connecter votre domaine à Microsoft 365.
ms.openlocfilehash: 1bec66a43026321ddf1979c73902a533bee3a07b
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49925109"
---
# <a name="connect-your-domain-to-microsoft-365-for-business"></a><span data-ttu-id="dd037-103">Connecter votre domaine à Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="dd037-103">Connect your domain to Microsoft 365 for business</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4LFpy?autoplay=false]

<span data-ttu-id="dd037-104">Une fois que vous avez installé Microsoft 365 et déplacé vos données de courrier à partir de Google Workspace, vous pouvez connecter votre domaine à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="dd037-104">Once you’ve set up Microsoft 365 and moved your email data from Google Workspace, you can connect your domain to Microsoft 365.</span></span> 

<span data-ttu-id="dd037-105">Vous devez d’abord supprimer les enregistrements DNS existants de Google, puis nous pouvons ajouter de nouveaux enregistrements DNS à partir de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="dd037-105">First you will need to delete existing DNS records from Google, then we can add new DNS records from Microsoft 365.</span></span>

## <a name="try-it"></a><span data-ttu-id="dd037-106">Essayez !</span><span class="sxs-lookup"><span data-stu-id="dd037-106">Try it!</span></span>

1. <span data-ttu-id="dd037-107">Connectez-vous à votre console d’administration Google Workspace [sur admin.google.com](https://admin.google.com).</span><span class="sxs-lookup"><span data-stu-id="dd037-107">Sign into your Google Workspace admin console at [admin.google.com](https://admin.google.com).</span></span>
1. <span data-ttu-id="dd037-108">Select **Domains**, **Manage domains**, **View details**, **Manage domain**, then **DNS** in the left nav.</span><span class="sxs-lookup"><span data-stu-id="dd037-108">Select **Domains**, **Manage domains**, **View details**, **Manage domain**, then **DNS** in the left nav.</span></span>
1. <span data-ttu-id="dd037-109">Faites défiler vers le bas **jusqu’aux enregistrements** synthétiques, **ouvrez Google Workspace,** **sélectionnez Supprimer,** puis **Supprimez à** nouveau.</span><span class="sxs-lookup"><span data-stu-id="dd037-109">Scroll down to **Synthetic records**, open **Google Workspace**, select **Delete**, then **Delete** again.</span></span>
1. <span data-ttu-id="dd037-110">Faites défiler vers le bas **jusqu’aux** enregistrements de ressources personnalisés et supprimez tous les enregistrements DNS existants qui apparaissent, y compris ceux que vous avez peut-être créés précédemment pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="dd037-110">Scroll down to **Custom resource records** and delete any existing DNS records that appear, including any you may have created previously for Microsoft 365.</span></span>
1. <span data-ttu-id="dd037-111">Go to the [Microsoft 365 admin center](https://admin.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="dd037-111">Go to the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>
1. <span data-ttu-id="dd037-112">In the left nav, choose, **Show all**, **Settings**, **Domains**.</span><span class="sxs-lookup"><span data-stu-id="dd037-112">In the left nav, choose, **Show all**, **Settings**, **Domains**.</span></span>
1. <span data-ttu-id="dd037-113">Choisissez ensuite votre domaine par défaut.</span><span class="sxs-lookup"><span data-stu-id="dd037-113">Then choose your default domain.</span></span>
1. <span data-ttu-id="dd037-114">Sélectionnez **Continuer le programme** d’installation, puis, pour connecter votre domaine, choisissez **Continuer.**</span><span class="sxs-lookup"><span data-stu-id="dd037-114">Select **Continue setup**, then, to connect your domain, choose  **Continue**.</span></span>
1. <span data-ttu-id="dd037-115">Faites défiler vers le bas pour afficher les enregistrements DNS qui doivent être copiés dans Google.</span><span class="sxs-lookup"><span data-stu-id="dd037-115">Scroll down to view the DNS records that need to be copied to Google.</span></span>
1. <span data-ttu-id="dd037-116">Ouvrez **MX Records** et sous **Points vers l’adresse ou la valeur,** copiez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="dd037-116">Open **MX Records**, and under **Points to address or value**, copy the record.</span></span>
1. <span data-ttu-id="dd037-117">Revenir à Google et, dans la section **Enregistrements de** ressource personnalisés, ouvrez ladown du type d’enregistrement et sélectionnez **MX**.</span><span class="sxs-lookup"><span data-stu-id="dd037-117">Return to Google, and in the **Custom resource records** section, open the record type dropdown and select **MX**.</span></span>
1. <span data-ttu-id="dd037-118">Dans le **champ** Données, collez l’enregistrement que vous avez copié.</span><span class="sxs-lookup"><span data-stu-id="dd037-118">In the **Data** field, paste the record you copied.</span></span>
1. <span data-ttu-id="dd037-119">Puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="dd037-119">Then select **Add**.</span></span>
1. <span data-ttu-id="dd037-120">Répétez le processus pour les enregistrements CNAME et TXT et ajoutez les valeurs dans la page de gestion DNS Google.</span><span class="sxs-lookup"><span data-stu-id="dd037-120">Repeat the process for CNAME and TXT records and add the values in the Google DNS management page.</span></span>
1. <span data-ttu-id="dd037-121">Revenir au Centre d’administration Microsoft 365 et sélectionnez **Continuer.**</span><span class="sxs-lookup"><span data-stu-id="dd037-121">Return to the Microsoft 365 Admin center and select **Continue**.</span></span>

    <span data-ttu-id="dd037-122">La configuration de votre domaine est terminée.</span><span class="sxs-lookup"><span data-stu-id="dd037-122">Your domain setup is complete.</span></span>