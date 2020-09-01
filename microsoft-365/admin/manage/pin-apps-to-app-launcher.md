---
title: Épingler des applications au lanceur d’applications de vos utilisateurs
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.collection:
- Adm_O365
- M365-subscription-management
ms.service: o365-administration
localization_priority: Normal
description: En tant qu’administrateur général, vous pouvez épingler jusqu’à trois applications au lanceur d’applications de vos utilisateurs.
ms.openlocfilehash: d9b95a20f332a9b1f2f6b0ebba28a70c58677b58
ms.sourcegitcommit: 87449335d9a1124ee82fa2e95e4745155a95a62f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2020
ms.locfileid: "47310874"
---
# <a name="pin-apps-to-your-users-app-launcher"></a><span data-ttu-id="9a898-103">Épingler des applications au lanceur d’applications de vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="9a898-103">Pin apps to your users' app launcher</span></span>

<span data-ttu-id="9a898-104">Vous pouvez utiliser des contrôles dans le portail Azure Active Directory pour épingler jusqu’à trois applications à Office.com et le lanceur d’applications pour tous les utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9a898-104">You can use controls in the Azure Active Directory portal to pin up to three apps to Office.com and the app launcher for all the users in your organization.</span></span> <span data-ttu-id="9a898-105">Vous pouvez également organiser des groupes d’applications.</span><span class="sxs-lookup"><span data-stu-id="9a898-105">You can also organize groups of applications.</span></span> <span data-ttu-id="9a898-106">Toute application que vous ajoutez peut être désépinglée ultérieurement par l’utilisateur à tout moment.</span><span class="sxs-lookup"><span data-stu-id="9a898-106">Any app you add can later be unpinned by the user at any time.</span></span> <span data-ttu-id="9a898-107">Pour épingler une application pour vos utilisateurs, vous devez être un administrateur d’application Cloud ou un administrateur d’application dans Azure Active Directory, ou un administrateur global dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="9a898-107">To pin an app for your users, you must be a Cloud application administrator, or Application administrator in Azure Active Directory, or a Global administrator in Office 365.</span></span> <span data-ttu-id="9a898-108">Pour plus d’informations sur les rôles d’administrateur, consultez la rubrique [rôles d’administrateur dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles) et [rôles d’administrateur dans Microsoft 365](../add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="9a898-108">For more information about admin roles, see [admin roles in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles) and [admin roles in Microsoft 365](../add-users/about-admin-roles.md).</span></span> 

<span data-ttu-id="9a898-109">Pour plus d’informations sur le lanceur d’applications et Office.com, consultez l’article relatif [au lanceur d’applications](https://support.microsoft.com/office/79f12104-6fed-442f-96a0-eb089a3f476a) et [aux mises à jour vers Office.com et à l’article du blog du lanceur d’applications Office 365](https://techcommunity.microsoft.com/t5/office-365-blog/updates-to-office-com-and-the-office-365-app-launcher/ba-p/1150503) .</span><span class="sxs-lookup"><span data-stu-id="9a898-109">For more information about the app launcher and Office.com, see [meet the app launcher](https://support.microsoft.com/office/79f12104-6fed-442f-96a0-eb089a3f476a) and [updates to office.com and the-Office 365 app launcher](https://techcommunity.microsoft.com/t5/office-365-blog/updates-to-office-com-and-the-office-365-app-launcher/ba-p/1150503) blog article.</span></span>

## <a name="use-the-azure-active-directory-portal-to-pin-apps"></a><span data-ttu-id="9a898-110">Utiliser le portail Azure Active Directory pour épingler des applications</span><span class="sxs-lookup"><span data-stu-id="9a898-110">Use the Azure Active Directory portal to pin apps</span></span>

1. <span data-ttu-id="9a898-111">Accédez au centre d’administration Microsoft 365 à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a> .</span><span class="sxs-lookup"><span data-stu-id="9a898-111">Go to the Microsoft 365 admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>.</span></span>
2. <span data-ttu-id="9a898-112">Dans le volet de navigation de gauche, choisissez **Afficher tout**, puis sous **centres d’administration**, sélectionnez **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="9a898-112">In the left nav, choose **Show all**, and under **Admin centers**, choose **Azure Active Directory**.</span></span>
3. <span data-ttu-id="9a898-113">Dans **Azure Active Directory**, choisissez **Enterprise applications**  >  **paramètres utilisateur**des applications d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="9a898-113">In **Azure Active Directory**, choose **Enterprise applications** > **User settings**.</span></span>
4. <span data-ttu-id="9a898-114">Dans la section **paramètres Office 365** , sélectionnez **Ajouter une application**.</span><span class="sxs-lookup"><span data-stu-id="9a898-114">In the **Office 365 Settings** section, choose **Add application**.</span></span>
5. <span data-ttu-id="9a898-115">Choisissez les applications que vous souhaitez épingler au lanceur d’applications des utilisateurs, puis choisissez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="9a898-115">Choose the applications you want to pin to the users' app launcher, and then choose **Add**.</span></span>

:::image type="content" source="../../media/add-apps.png" alt-text="Paramètres Microsoft 365 pour épingler des applications.":::

### <a name="pin-a-custom-app"></a><span data-ttu-id="9a898-117">Épingler une application personnalisée</span><span class="sxs-lookup"><span data-stu-id="9a898-117">Pin a custom app</span></span>

> [!NOTE]
> <span data-ttu-id="9a898-118">L’interface utilisateur indiquera si vous avez besoin d’acheter des licences Azure AD supplémentaires pour utiliser cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="9a898-118">The user interface will indicate if you need need to purchase additional Azure AD licenses to use this feature.</span></span> <span data-ttu-id="9a898-119">Pour plus d’informations, consultez la rubrique [tarification Azure Active Directory](https://azure.microsoft.com/pricing/details/active-directory/).</span><span class="sxs-lookup"><span data-stu-id="9a898-119">For more information see [Azure Active Directory pricing](https://azure.microsoft.com/pricing/details/active-directory/).</span></span>

1. <span data-ttu-id="9a898-120">Dans **Azure Active Directory**, sélectionnez **applications d’entreprise**  >  **nouvelle application** en haut de la page **toutes les applications** .</span><span class="sxs-lookup"><span data-stu-id="9a898-120">In **Azure Active Directory**, choose **Enterprise applications** > **New application** on the top of the **All applications** page.</span></span>
2. <span data-ttu-id="9a898-121">Sur la page **Ajouter une application** , choisissez **application non-Galerie** ou **créer votre propre application** si vous êtes dans la version préliminaire d’Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9a898-121">On the **Add an application** page, choose **Non-gallery application** or **Create your own application** if you are in the preview version of Azure Active Directory.</span></span> 
3. <span data-ttu-id="9a898-122">Tapez un nom pour l’application, puis attribuez un utilisateur sous l’onglet **utilisateurs et groupes** .</span><span class="sxs-lookup"><span data-stu-id="9a898-122">Type a name for the application and then assign user in the **Users and groups** tab.</span></span>
4. <span data-ttu-id="9a898-123">Utilisez l’onglet **Propriétés** pour charger une icône pour l’application.</span><span class="sxs-lookup"><span data-stu-id="9a898-123">Use the **Properties** tab to upload an icon for the app.</span></span>
5. <span data-ttu-id="9a898-124">Pour affecter une URL à l’application, dans l’onglet **authentification unique** , choisissez **lié** , puis entrez une URL.</span><span class="sxs-lookup"><span data-stu-id="9a898-124">To assign a URL to the app, in the **Single sign-on** tab, choose **Linked** and then enter a URL.</span></span>
6. <span data-ttu-id="9a898-125">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="9a898-125">Choose **Save**.</span></span>

## <a name="create-application-collections"></a><span data-ttu-id="9a898-126">Créer des collections d’applications</span><span class="sxs-lookup"><span data-stu-id="9a898-126">Create application collections</span></span>

<span data-ttu-id="9a898-127">Vous pouvez également créer des collections d’applications pour les utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9a898-127">You can also create application collections for the users in your organization.</span></span> <span data-ttu-id="9a898-128">Pour obtenir des instructions, consultez la rubrique [créer des collections dans le portail mes applications dans le portail Azure](https://docs.microsoft.com/azure/active-directory/manage-apps/access-panel-collections).</span><span class="sxs-lookup"><span data-stu-id="9a898-128">For instructions, see [create collections on the My Apps portal in the Azure portal](https://docs.microsoft.com/azure/active-directory/manage-apps/access-panel-collections).</span></span>