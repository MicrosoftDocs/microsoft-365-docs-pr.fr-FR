---
title: Gérer les règles de suppression de microsoft Defender pour les points de terminaison
description: Vous devrez peut-être empêcher l'apparition d'alertes dans le portail à l'aide de règles de suppression. Découvrez comment gérer vos règles de suppression dans Microsoft Defender pour point de terminaison.
keywords: gérer la suppression, les règles, le nom de la règle, l'étendue, l'action, les alertes, activer, désactiver
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: f1549512a02fe3af71d32c6b33c69cc705de99a8
ms.sourcegitcommit: 22505ce322f68a2d0ce70d71caf3b0a657fa838a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2021
ms.locfileid: "51862126"
---
# <a name="manage-suppression-rules"></a><span data-ttu-id="fca35-105">Gérer des règles de suppression</span><span class="sxs-lookup"><span data-stu-id="fca35-105">Manage suppression rules</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="fca35-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="fca35-106">**Applies to:**</span></span>
- [<span data-ttu-id="fca35-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="fca35-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="fca35-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="fca35-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="fca35-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="fca35-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="fca35-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="fca35-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)


<span data-ttu-id="fca35-111">Dans certains scénarios, vous devrez peut-être supprimer l'apparition d'alertes dans le portail.</span><span class="sxs-lookup"><span data-stu-id="fca35-111">There might be scenarios where you need to suppress alerts from appearing in the portal.</span></span> <span data-ttu-id="fca35-112">Vous pouvez créer des règles de suppression pour des alertes spécifiques qui sont connues comme étant anodins, telles que des outils ou des processus connus dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="fca35-112">You can create suppression rules for specific alerts that are known to be innocuous such as known tools or processes in your organization.</span></span> <span data-ttu-id="fca35-113">Pour plus d'informations sur la suppression des alertes, voir [Supprimer des alertes.](manage-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="fca35-113">For more information on how to suppress alerts, see [Suppress alerts](manage-alerts.md).</span></span>

<span data-ttu-id="fca35-114">Vous pouvez afficher la liste de toutes les règles de suppression et les gérer au même endroit.</span><span class="sxs-lookup"><span data-stu-id="fca35-114">You can view a list of all the suppression rules and manage them in one place.</span></span> <span data-ttu-id="fca35-115">Vous pouvez également activer ou désactiver une règle de suppression d'alerte.</span><span class="sxs-lookup"><span data-stu-id="fca35-115">You can also turn an alert suppression rule on or off.</span></span>


1. <span data-ttu-id="fca35-116">Dans le volet de navigation, sélectionnez **Suppression de l'alerte**  >  **paramètres.**</span><span class="sxs-lookup"><span data-stu-id="fca35-116">In the navigation pane, select **Settings** > **Alert suppression**.</span></span> <span data-ttu-id="fca35-117">La liste des règles de suppression créées par les utilisateurs de votre organisation s'affiche.</span><span class="sxs-lookup"><span data-stu-id="fca35-117">The list of suppression rules that users in your organization have created is displayed.</span></span>

2. <span data-ttu-id="fca35-118">Sélectionnez une règle en cliquant sur la case à cocher en regard du nom de la règle.</span><span class="sxs-lookup"><span data-stu-id="fca35-118">Select a rule by clicking on the check-box beside the rule name.</span></span>

3. <span data-ttu-id="fca35-119">Cliquez **sur Activer,** **Modifier la règle** ou Supprimer une **règle.**</span><span class="sxs-lookup"><span data-stu-id="fca35-119">Click **Turn rule on**, **Edit rule**, or  **Delete rule**.</span></span> <span data-ttu-id="fca35-120">Lorsque vous modifiez une règle, vous pouvez choisir de publier des alertes qu'elle a déjà supprimées, que ces alertes correspondent ou non aux nouveaux critères.</span><span class="sxs-lookup"><span data-stu-id="fca35-120">When making changes to a rule, you can choose to release alerts that it has already suppressed, regardless whether or not these alerts match the new criteria.</span></span> 


## <a name="view-details-of-a-suppression-rule"></a><span data-ttu-id="fca35-121">Afficher les détails d'une règle de suppression</span><span class="sxs-lookup"><span data-stu-id="fca35-121">View details of a suppression rule</span></span>

1. <span data-ttu-id="fca35-122">Dans le volet de navigation, sélectionnez **Suppression de l'alerte**  >  **paramètres.**</span><span class="sxs-lookup"><span data-stu-id="fca35-122">In the navigation pane, select **Settings** > **Alert suppression**.</span></span> <span data-ttu-id="fca35-123">La liste des règles de suppression créées par les utilisateurs de votre organisation s'affiche.</span><span class="sxs-lookup"><span data-stu-id="fca35-123">The list of suppression rules that users in your organization have created is displayed.</span></span>

2. <span data-ttu-id="fca35-124">Cliquez sur un nom de règle.</span><span class="sxs-lookup"><span data-stu-id="fca35-124">Click on a rule name.</span></span> <span data-ttu-id="fca35-125">Les détails de la règle s’affichent.</span><span class="sxs-lookup"><span data-stu-id="fca35-125">Details of the rule is displayed.</span></span> <span data-ttu-id="fca35-126">Vous verrez les détails de la règle tels que l’état, l’étendue, l’action, le nombre d’alertes correspondantes, créés par et la date de création de la règle.</span><span class="sxs-lookup"><span data-stu-id="fca35-126">You'll see the rule details such as  status, scope, action, number of matching alerts, created by, and date when the rule was created.</span></span> <span data-ttu-id="fca35-127">Vous pouvez également afficher les alertes associées et les conditions de règle.</span><span class="sxs-lookup"><span data-stu-id="fca35-127">You can also view associated alerts and the rule conditions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fca35-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fca35-128">Related topics</span></span>

- [<span data-ttu-id="fca35-129">Gérer des alertes</span><span class="sxs-lookup"><span data-stu-id="fca35-129">Manage alerts</span></span>](manage-alerts.md)
