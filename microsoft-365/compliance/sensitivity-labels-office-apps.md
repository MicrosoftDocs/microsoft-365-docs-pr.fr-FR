---
title: Fonctionnement des étiquettes de confidentialité dans les applications Office
ms.author: greglin
author: greg-lindsay
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Avec les étiquettes de sensibilité, vous pouvez classer et protéger le contenu sensible, tout en vous assurant que la productivité et la possibilité de collaboration des membres de votre organisation ne sont pas altérées. Vous pouvez utiliser les étiquettes de sensibilité afin d’appliquer des paramètres de protection, comme le chiffrement ou les filigranes, sur le contenu étiqueté.
ms.openlocfilehash: f702423f0b1074b5619ef1c321cc5e9f1daef1d7
ms.sourcegitcommit: 15173ab87325b7d79bab683702b35d77a355cd6b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/08/2019
ms.locfileid: "37417563"
---
# <a name="how-sensitivity-labels-work-in-office-apps"></a><span data-ttu-id="455e7-104">Fonctionnement des étiquettes de confidentialité dans les applications Office</span><span class="sxs-lookup"><span data-stu-id="455e7-104">How sensitivity labels work in Office apps</span></span>

## <a name="what-prerequisites-are-there-to-use-sensitivity-labels-in-office-applications"></a><span data-ttu-id="455e7-105">Quels sont les conditions préalables à l’utilisation des étiquettes de confidentialité dans les applications Office ?</span><span class="sxs-lookup"><span data-stu-id="455e7-105">What prerequisites are there to use sensitivity labels in Office applications?</span></span>

### <a name="common-requirements"></a><span data-ttu-id="455e7-106">Conditions courantes</span><span class="sxs-lookup"><span data-stu-id="455e7-106">Common requirements</span></span> 

- <span data-ttu-id="455e7-107">Les étiquettes de confidentialité unifiée doivent être [configurées et publiées dans le Centre de sécurité et conformité](https://aka.ms/managemip)</span><span class="sxs-lookup"><span data-stu-id="455e7-107">Unified sensitivity labels must be [configured and published in the Security and Compliance Center](https://aka.ms/managemip)</span></span>
- <span data-ttu-id="455e7-108">Les utilisateurs doivent être connectés à Office à l’aide de leur compte professionnel.</span><span class="sxs-lookup"><span data-stu-id="455e7-108">Users must be signed in to Office with their work account.</span></span>
- <span data-ttu-id="455e7-109">Les utilisateurs doivent disposer d’une licence Office 365 E3 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="455e7-109">Users must have an Office 365 E3 or above license assigned.</span></span>

### <a name="additional-requirements-for-office-for-windows"></a><span data-ttu-id="455e7-110">Conditions requises supplémentaires pour Office pour Windows</span><span class="sxs-lookup"><span data-stu-id="455e7-110">Additional requirements for Office for Windows</span></span> 

- <span data-ttu-id="455e7-111">Le client Azure Information Protection ne doit pas être exécuté dans Office.</span><span class="sxs-lookup"><span data-stu-id="455e7-111">The Azure Information Protection client must not be running in Office.</span></span> <span data-ttu-id="455e7-112">Voir aussi : [Les étiquettes de confidentialité peuvent-elles fonctionner avec le client Azure Information Protection dans Office pour Windows ?](#can-sensitivity-labels-run-alongside-the-azure-information-protection-client-in-office-for-windows).</span><span class="sxs-lookup"><span data-stu-id="455e7-112">See also: [Can sensitivity labels run alongside the Azure Information Protection client in Office for Windows?](#can-sensitivity-labels-run-alongside-the-azure-information-protection-client-in-office-for-windows).</span></span>

### <a name="additional-requirements-for-outlook-on-all-platforms"></a><span data-ttu-id="455e7-113">Conditions requises supplémentaires pour Outlook sur toutes les plateformes</span><span class="sxs-lookup"><span data-stu-id="455e7-113">Additional requirements for Outlook on all platforms</span></span> 

- <span data-ttu-id="455e7-114">Dans la configuration d’étiquette, si vous activez le marquage de contenu, vous devez utiliser Exchange Online pour que ce marquage de contenu soit insérée en transit.</span><span class="sxs-lookup"><span data-stu-id="455e7-114">In your label configuration, if you turn on content marking, you must be using Exchange Online for that content marking to be inserted in transit.</span></span>

## <a name="what-sensitivity-label-capabilities-are-supported-in-office-today"></a><span data-ttu-id="455e7-115">Quelles fonctionnalités d’étiquette de confidentialité sont prises en charge dans Office actuellement ?</span><span class="sxs-lookup"><span data-stu-id="455e7-115">What sensitivity label capabilities are supported in Office today?</span></span> 

<table border="1" cellspacing="0" cellpadding="0">
<th><span data-ttu-id="455e7-116"><font size="-1">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="455e7-116"><font size="-1">Capability</span></span><th><span data-ttu-id="455e7-117"><font size="-1">Windows</span><span class="sxs-lookup"><span data-stu-id="455e7-117"><font size="-1">Windows</span></span><th><span data-ttu-id="455e7-118"><font size="-1">Mac<th colspan="2"><font size="-1">iOS<th colspan="2"><font size="-1">Android<th colspan="2"><font size="-1">Web</span><span class="sxs-lookup"><span data-stu-id="455e7-118"><font size="-1">Mac<th colspan="2"><font size="-1">iOS<th colspan="2"><font size="-1">Android<th colspan="2"><font size="-1">Web</span></span></tr>
<tr><td>

<td><span data-ttu-id="455e7-119"><font size="-1"> Word</span><span class="sxs-lookup"><span data-stu-id="455e7-119"><font size="-1"> Word</span></span><br>
<span data-ttu-id="455e7-120">Excel</span><span class="sxs-lookup"><span data-stu-id="455e7-120">Excel</span></span><br>
<span data-ttu-id="455e7-121">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="455e7-121">PowerPoint</span></span><br>
<span data-ttu-id="455e7-122">Outlook</span><span class="sxs-lookup"><span data-stu-id="455e7-122">Outlook</span></span>


<td><span data-ttu-id="455e7-123"><font size="-1"> Word</span><span class="sxs-lookup"><span data-stu-id="455e7-123"><font size="-1"> Word</span></span><br>
<span data-ttu-id="455e7-124">Excel</span><span class="sxs-lookup"><span data-stu-id="455e7-124">Excel</span></span><br>
<span data-ttu-id="455e7-125">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="455e7-125">PowerPoint</span></span><br>
<span data-ttu-id="455e7-126">Outlook</span><span class="sxs-lookup"><span data-stu-id="455e7-126">Outlook</span></span>

<td><span data-ttu-id="455e7-127"><font size="-1"> Word</span><span class="sxs-lookup"><span data-stu-id="455e7-127"><font size="-1"> Word</span></span><br>
<span data-ttu-id="455e7-128">Excel</span><span class="sxs-lookup"><span data-stu-id="455e7-128">Excel</span></span><br>
<span data-ttu-id="455e7-129">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="455e7-129">PowerPoint</span></span>
<td><span data-ttu-id="455e7-130"><font size="-1">Outlook</span><span class="sxs-lookup"><span data-stu-id="455e7-130"><font size="-1"> Outlook</span></span>

<td><span data-ttu-id="455e7-131"><font size="-1"> Word</span><span class="sxs-lookup"><span data-stu-id="455e7-131"><font size="-1"> Word</span></span><br>
<span data-ttu-id="455e7-132">Excel</span><span class="sxs-lookup"><span data-stu-id="455e7-132">Excel</span></span><br>
<span data-ttu-id="455e7-133">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="455e7-133">PowerPoint</span></span>
<td><span data-ttu-id="455e7-134"><font size="-1">Outlook</span><span class="sxs-lookup"><span data-stu-id="455e7-134"><font size="-1"> Outlook</span></span>

<td><span data-ttu-id="455e7-135"><font size="-1"> Word</span><span class="sxs-lookup"><span data-stu-id="455e7-135"><font size="-1"> Word</span></span><br>
<span data-ttu-id="455e7-136">Excel</span><span class="sxs-lookup"><span data-stu-id="455e7-136">Excel</span></span><br>
<span data-ttu-id="455e7-137">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="455e7-137">PowerPoint</span></span>
<td><span data-ttu-id="455e7-138"><font size="-1"> Outlook </b>
</span><span class="sxs-lookup"><span data-stu-id="455e7-138"><font size="-1"> Outlook </b>
</span></span></tr>

<tr>
<td><span data-ttu-id="455e7-139"><font size="-1">Appliquer, modifier ou supprimer manuellement une étiquette</span><span class="sxs-lookup"><span data-stu-id="455e7-139"><font size="-1">Manually apply, change, or remove label</span></span><td><span data-ttu-id="455e7-140"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-140"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-141"><font size="-1">1910+</font>

</span><span class="sxs-lookup"><span data-stu-id="455e7-141"><font size="-1">1910+</font>

</span></span><td><span data-ttu-id="455e7-142"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-142"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-143"><font size="-1">16.21.0+</font>

</span><span class="sxs-lookup"><span data-stu-id="455e7-143"><font size="-1">16.21.0+</font>

</span></span><td><span data-ttu-id="455e7-144"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-144"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-145"><font size="-1">2.21+</font>
</span><span class="sxs-lookup"><span data-stu-id="455e7-145"><font size="-1">2.21+</font>
</span></span><td><span data-ttu-id="455e7-146"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="455e7-146"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="455e7-147"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-147"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-148"><font size="-1">16.0.11231+</font>
</span><span class="sxs-lookup"><span data-stu-id="455e7-148"><font size="-1">16.0.11231+</font>
</span></span><td><span data-ttu-id="455e7-149"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="455e7-149"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="455e7-150"><font size="-1">Bientôt disponible<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="455e7-150"><font size="-1">Coming soon<sup>3</sup></span></span><td><span data-ttu-id="455e7-151"><font size="-1">Bientôt disponible<sup>3</sup>

</span><span class="sxs-lookup"><span data-stu-id="455e7-151"><font size="-1">Coming soon<sup>3</sup>

</span></span><tr>
<td><span data-ttu-id="455e7-152"><font size="-1"><a href="https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels#what-label-policies-can-do">Appliquer une étiquette par défaut</a>
</span><span class="sxs-lookup"><span data-stu-id="455e7-152"><font size="-1"><a href="https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels#what-label-policies-can-do">Apply a default label</a>
</span></span><td><span data-ttu-id="455e7-153"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-153"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-154"><font size="-1">1910+</font>

</span><span class="sxs-lookup"><span data-stu-id="455e7-154"><font size="-1">1910+</font>

</span></span><td><span data-ttu-id="455e7-155"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-155"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-156"><font size="-1">16.21.0+</font>

</span><span class="sxs-lookup"><span data-stu-id="455e7-156"><font size="-1">16.21.0+</font>

</span></span><td><span data-ttu-id="455e7-157"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-157"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-158"><font size="-1">2.21+</font>
</span><span class="sxs-lookup"><span data-stu-id="455e7-158"><font size="-1">2.21+</font>
</span></span><td><span data-ttu-id="455e7-159"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="455e7-159"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="455e7-160"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-160"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-161"><font size="-1">16.0.11231+</font>
</span><span class="sxs-lookup"><span data-stu-id="455e7-161"><font size="-1">16.0.11231+</font>
</span></span><td><span data-ttu-id="455e7-162"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="455e7-162"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="455e7-163"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="455e7-163"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="455e7-164"><font size="-1">Bientôt disponible<sup>3</sup>

</span><span class="sxs-lookup"><span data-stu-id="455e7-164"><font size="-1">Coming soon<sup>3</sup>

</span></span><tr><td><span data-ttu-id="455e7-165"><font size="-1"><a href="https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels#what-label-policies-can-do">Demander une justification pour changer une étiquette</a><sup>1</sup>
</span><span class="sxs-lookup"><span data-stu-id="455e7-165"><font size="-1"><a href="https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels#what-label-policies-can-do">Require a justification for changing a label</a><sup>1</sup>
</span></span><td><span data-ttu-id="455e7-166"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-166"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-167"><font size="-1">1910+</font>

</span><span class="sxs-lookup"><span data-stu-id="455e7-167"><font size="-1">1910+</font>

</span></span><td><span data-ttu-id="455e7-168"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-168"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-169"><font size="-1">16.21.0+</font>

</span><span class="sxs-lookup"><span data-stu-id="455e7-169"><font size="-1">16.21.0+</font>

</span></span><td><span data-ttu-id="455e7-170"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-170"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-171"><font size="-1">2.21+</font>
</span><span class="sxs-lookup"><span data-stu-id="455e7-171"><font size="-1">2.21+</font>
</span></span><td><span data-ttu-id="455e7-172"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="455e7-172"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="455e7-173"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-173"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-174"><font size="-1">16.0.11231+</font>
</span><span class="sxs-lookup"><span data-stu-id="455e7-174"><font size="-1">16.0.11231+</font>
</span></span><td><span data-ttu-id="455e7-175"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="455e7-175"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="455e7-176"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="455e7-176"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="455e7-177"><font size="-1">Bientôt disponible<sup>3</sup>

</span><span class="sxs-lookup"><span data-stu-id="455e7-177"><font size="-1">Coming soon<sup>3</sup>

</span></span><tr><td><span data-ttu-id="455e7-178"><font size="-1"><a href="https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels#what-label-policies-can-do">Fournir un lien d’aide vers une page d’aide personnalisée</a>
</span><span class="sxs-lookup"><span data-stu-id="455e7-178"><font size="-1"><a href="https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels#what-label-policies-can-do">Provide help link to a custom help page</a>
</span></span><td><span data-ttu-id="455e7-179"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-179"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-180"><font size="-1">1910+</font>

</span><span class="sxs-lookup"><span data-stu-id="455e7-180"><font size="-1">1910+</font>

</span></span><td><span data-ttu-id="455e7-181"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-181"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-182"><font size="-1">16.21.0+</font>

</span><span class="sxs-lookup"><span data-stu-id="455e7-182"><font size="-1">16.21.0+</font>

</span></span><td><span data-ttu-id="455e7-183"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-183"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-184"><font size="-1">2.21+</font>
</span><span class="sxs-lookup"><span data-stu-id="455e7-184"><font size="-1">2.21+</font>
</span></span><td><span data-ttu-id="455e7-185"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="455e7-185"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="455e7-186"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-186"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-187"><font size="-1">16.0.11231+</font>
</span><span class="sxs-lookup"><span data-stu-id="455e7-187"><font size="-1">16.0.11231+</font>
</span></span><td><span data-ttu-id="455e7-188"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="455e7-188"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="455e7-189"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="455e7-189"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="455e7-190"><font size="-1">Bientôt disponible<sup>3</sup>

</span><span class="sxs-lookup"><span data-stu-id="455e7-190"><font size="-1">Coming soon<sup>3</sup>

</span></span><tr><td><span data-ttu-id="455e7-191"><font size="-1"><a href="https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels#what-sensitivity-labels-can-do">Marquer le contenu</a>
</span><span class="sxs-lookup"><span data-stu-id="455e7-191"><font size="-1"><a href="https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels#what-sensitivity-labels-can-do">Mark the content</a>
</span></span><td><span data-ttu-id="455e7-192"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-192"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-193"><font size="-1">1910+</font>

</span><span class="sxs-lookup"><span data-stu-id="455e7-193"><font size="-1">1910+</font>

</span></span><td><span data-ttu-id="455e7-194"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-194"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-195"><font size="-1">16.21.0+</font>

</span><span class="sxs-lookup"><span data-stu-id="455e7-195"><font size="-1">16.21.0+</font>

</span></span><td><span data-ttu-id="455e7-196"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-196"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-197"><font size="-1">2.21+</font>
</span><span class="sxs-lookup"><span data-stu-id="455e7-197"><font size="-1">2.21+</font>
</span></span><td><span data-ttu-id="455e7-198"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="455e7-198"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="455e7-199"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-199"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-200"><font size="-1">16.0.11231+</font
</span><span class="sxs-lookup"><span data-stu-id="455e7-200"><font size="-1">16.0.11231+</font
</span></span>><td><span data-ttu-id="455e7-201"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="455e7-201"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="455e7-202"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="455e7-202"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="455e7-203"><font size="-1">Bientôt disponible<sup>3</sup>

</span><span class="sxs-lookup"><span data-stu-id="455e7-203"><font size="-1">Coming soon<sup>3</sup>

</span></span><tr><td><span data-ttu-id="455e7-204"><font size="-1">
  <a href="https://docs.microsoft.com/en-us/microsoft-365/compliance/encryption-sensitivity-labels#assign-permissions-now">Attribuer des autorisations prédéfinies</a>
</span><span class="sxs-lookup"><span data-stu-id="455e7-204"><font size="-1">Assign pre-defined permissions</span></span><td><span data-ttu-id="455e7-205"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-205"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-206"><font size="-1">1910+</font>

</span><span class="sxs-lookup"><span data-stu-id="455e7-206"><font size="-1">1910+</font>

</span></span><td><span data-ttu-id="455e7-207"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-207"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-208"><font size="-1">16.21.0+</font>

</span><span class="sxs-lookup"><span data-stu-id="455e7-208"><font size="-1">16.21.0+</font>

</span></span><td><span data-ttu-id="455e7-209"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-209"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-210"><font size="-1">2.21+</font>
</span><span class="sxs-lookup"><span data-stu-id="455e7-210"><font size="-1">2.21+</font>
</span></span><td><span data-ttu-id="455e7-211"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="455e7-211"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="455e7-212"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="455e7-212"><font size="-1"><b>Yes</b></span></span><br><span data-ttu-id="455e7-213"><font size="-1">16.0.11231+</font>
</span><span class="sxs-lookup"><span data-stu-id="455e7-213"><font size="-1">16.0.11231+</font>
</span></span><td><span data-ttu-id="455e7-214"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="455e7-214"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="455e7-215"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="455e7-215"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="455e7-216"><font size="-1">Bientôt disponible<sup>3</sup>

</span><span class="sxs-lookup"><span data-stu-id="455e7-216"><font size="-1">Coming soon<sup>3</sup>

</span></span><tr><td><span data-ttu-id="455e7-217"><font size="-1"><a href="https://docs.microsoft.com/microsoft-365/compliance/encryption-sensitivity-labels#let-users-assign-permissions">Permettre aux utilisateurs d’attribuer des autorisations</a>
</span><span class="sxs-lookup"><span data-stu-id="455e7-217"><font size="-1"><a href="https://docs.microsoft.com/microsoft-365/compliance/encryption-sensitivity-labels#let-users-assign-permissions">Let users assign permissions</a>
</span></span><td><span data-ttu-id="455e7-218"><font size="-1"><b>Oui</b><sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="455e7-218"><font size="-1"><b>Yes</b><sup>2</sup></span></span><br><span data-ttu-id="455e7-219"><font size="-1">1910+</font>

</span><span class="sxs-lookup"><span data-stu-id="455e7-219"><font size="-1">1910+</font>

</span></span><td><span data-ttu-id="455e7-220"><font size="-1"><b>Oui</b><sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="455e7-220"><font size="-1"><b>Yes</b><sup>2</sup></span></span><br><span data-ttu-id="455e7-221"><font size="-1">16.21.0+</font></span><span class="sxs-lookup"><span data-stu-id="455e7-221"><font size="-1">16.21.0+</font></span></span>

<td><span data-ttu-id="455e7-222"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-222"><font size="-1">TBD</span></span>
<td><span data-ttu-id="455e7-223"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="455e7-223"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="455e7-224"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-224"><font size="-1">TBD</span></span><td
><span data-ttu-id="455e7-225"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="455e7-225"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="455e7-226"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-226"><font size="-1">TBD</span></span>
<td><span data-ttu-id="455e7-227"><font size="-1">Bientôt disponible<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="455e7-227"><font size="-1">Coming soon<sup>3</sup></span></span>

<tr><td><span data-ttu-id="455e7-228"><font size="-1">Envoyer les données d’<a href="https://docs.microsoft.com/microsoft-365/compliance/label-analytics">analyse des étiquettes</a> pour les administrateurs</span><span class="sxs-lookup"><span data-stu-id="455e7-228"><font size="-1">Send <a href="https://docs.microsoft.com/microsoft-365/compliance/label-analytics">label analytics</a> data for administrators</span></span>
<td><span data-ttu-id="455e7-229"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-229"><font size="-1">TBD</span></span>

<td><span data-ttu-id="455e7-230"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-230"><font size="-1">TBD</span></span>

<td><span data-ttu-id="455e7-231"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-231"><font size="-1">TBD</span></span>
<td><span data-ttu-id="455e7-232"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-232"><font size="-1">TBD</span></span>
<td><span data-ttu-id="455e7-233"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-233"><font size="-1">TBD</span></span>
<td><span data-ttu-id="455e7-234"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-234"><font size="-1">TBD</span></span>
<td><span data-ttu-id="455e7-235"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-235"><font size="-1">TBD</span></span>
<td><span data-ttu-id="455e7-236"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-236"><font size="-1">TBD</span></span>

<tr><td><span data-ttu-id="455e7-237"><font size="-1">
  <a href="https://docs.microsoft.com/en-us/microsoft-365/compliance/sensitivity-labels#what-label-policies-can-do">Demander aux utilisateurs d'appliquer une étiquette à leurs e-mails et documents</a>
</span><span class="sxs-lookup"><span data-stu-id="455e7-237"><font size="-1">Require users to apply a label to their email and documents</span></span><td><span data-ttu-id="455e7-238"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-238"><font size="-1">TBD</span></span>

<td><span data-ttu-id="455e7-239"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-239"><font size="-1">TBD</span></span>

<td><span data-ttu-id="455e7-240"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-240"><font size="-1">TBD</span></span>
<td><span data-ttu-id="455e7-241"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-241"><font size="-1">TBD</span></span>
<td><span data-ttu-id="455e7-242"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-242"><font size="-1">TBD</span></span>
<td><span data-ttu-id="455e7-243"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-243"><font size="-1">TBD</span></span>
<td><span data-ttu-id="455e7-244"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-244"><font size="-1">TBD</span></span>
<td><span data-ttu-id="455e7-245"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-245"><font size="-1">TBD</span></span>

<tr><td><span data-ttu-id="455e7-246"><font size="-1"><a href="https://docs.microsoft.com/microsoft-365/compliance/apply-sensitivity-label-automatically">Appliquer automatiquement une étiquette de confidentialité au contenu</a>
</span><span class="sxs-lookup"><span data-stu-id="455e7-246"><font size="-1"><a href="https://docs.microsoft.com/microsoft-365/compliance/apply-sensitivity-label-automatically">Apply a sensitivity label to content automatically</a>
</span></span><td><span data-ttu-id="455e7-247"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-247"><font size="-1">TBD</span></span>

<td><span data-ttu-id="455e7-248"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-248"><font size="-1">TBD</span></span>

<td><span data-ttu-id="455e7-249"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-249"><font size="-1">TBD</span></span>
<td><span data-ttu-id="455e7-250"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-250"><font size="-1">TBD</span></span>
<td><span data-ttu-id="455e7-251"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-251"><font size="-1">TBD</span></span>
<td><span data-ttu-id="455e7-252"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-252"><font size="-1">TBD</span></span>
<td><span data-ttu-id="455e7-253"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-253"><font size="-1">TBD</span></span>
<td><span data-ttu-id="455e7-254"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="455e7-254"><font size="-1">TBD</span></span>
</table>

<br><span data-ttu-id="455e7-255"><sup>1</sup>Si elles sont configurées, les utilisateurs sont invités à justifier les rétrogradations d’étiquettes.</span><span class="sxs-lookup"><span data-stu-id="455e7-255"><sup>1</sup>If configured, users are prompted to justify label downgrades.</span></span> <span data-ttu-id="455e7-256">Toutefois, les données de justification ne sont pas encore disponibles pour les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="455e7-256">However, the justification data is not made available for administrators yet.</span></span> <span data-ttu-id="455e7-257">Elles seront disponibles lorsque la fonctionnalité « envoyer les données d’analyse des étiquettes pour les administrateurs » est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="455e7-257">It will become available when the “send label analytics data for administrators” capability is supported.</span></span>
<br><span data-ttu-id="455e7-258"><sup>2</sup>Permettre aux utilisateurs d'attribuer des autorisations n'est actuellement disponible que dans Outlook pour Windows et Mac.</span><span class="sxs-lookup"><span data-stu-id="455e7-258"><sup>2</sup>Let users assign permissions is currently only available in Outlook for Windows and Mac.</span></span> <span data-ttu-id="455e7-259">La disponibilité pour Word, Excel et PowerPoint est à définir.</span><span class="sxs-lookup"><span data-stu-id="455e7-259">Availability for Word, Excel, and PowerPoint is TBD.</span></span>
<br><span data-ttu-id="455e7-260"><sup>3</sup>Prévu pour le quatrième trimestre de l'année civile 2019.</span><span class="sxs-lookup"><span data-stu-id="455e7-260"><sup>3</sup>Expected Q4 of calendar year 2019.</span></span>

## <a name="when-do-content-marks-or-encryption-get-applied-after-content-is-given-a-sensitivity-label"></a><span data-ttu-id="455e7-261">Quand les marques de contenu ou le chiffrement sont-ils appliqués une fois qu’une étiquette de confidentialité est attribuée au contenu ?</span><span class="sxs-lookup"><span data-stu-id="455e7-261">When do content marks or encryption get applied after content is given a sensitivity label?</span></span>

| <span data-ttu-id="455e7-262">Application</span><span class="sxs-lookup"><span data-stu-id="455e7-262">Application</span></span> | <span data-ttu-id="455e7-263">Marquage du contenu</span><span class="sxs-lookup"><span data-stu-id="455e7-263">Content marking</span></span> | <span data-ttu-id="455e7-264">Chiffrement</span><span class="sxs-lookup"><span data-stu-id="455e7-264">Encryption</span></span>
| --- | --- | --- |
| <span data-ttu-id="455e7-265">Word, Excel, PowerPoint sur toutes les plateformes</span><span class="sxs-lookup"><span data-stu-id="455e7-265">Word, Excel, PowerPoint on all platforms</span></span> | <span data-ttu-id="455e7-266">Immédiatement</span><span class="sxs-lookup"><span data-stu-id="455e7-266">Immediately</span></span> | <span data-ttu-id="455e7-267">Immédiatement</span><span class="sxs-lookup"><span data-stu-id="455e7-267">Immediately</span></span> |
| <span data-ttu-id="455e7-268">Outlook pour PC et Mac</span><span class="sxs-lookup"><span data-stu-id="455e7-268">Outlook for PC and Mac</span></span> | <span data-ttu-id="455e7-269">Une fois l’e-mail envoyé par Exchange Online</span><span class="sxs-lookup"><span data-stu-id="455e7-269">After the email is sent by Exchange Online</span></span> | <span data-ttu-id="455e7-270">Immédiatement</span><span class="sxs-lookup"><span data-stu-id="455e7-270">Immediately</span></span> |
| <span data-ttu-id="455e7-271">Outlook sur le web, iOS et Android</span><span class="sxs-lookup"><span data-stu-id="455e7-271">Outlook on the web, iOS, and Android</span></span> | <span data-ttu-id="455e7-272">Une fois l’e-mail envoyé par Exchange Online</span><span class="sxs-lookup"><span data-stu-id="455e7-272">After the email is sent by Exchange Online</span></span> | <span data-ttu-id="455e7-273">Une fois l’e-mail envoyé par Exchange Online</span><span class="sxs-lookup"><span data-stu-id="455e7-273">After the email is sent by Exchange Online</span></span> |

## <a name="can-sensitivity-labels-run-alongside-the-azure-information-protection-client-in-office-for-windows"></a><span data-ttu-id="455e7-274">Les étiquettes de confidentialité peuvent-elles fonctionner avec le client Azure Information Protection dans Office pour Windows ?</span><span class="sxs-lookup"><span data-stu-id="455e7-274">Can sensitivity labels run alongside the Azure Information Protection client in Office for Windows?</span></span>

<span data-ttu-id="455e7-275">Non.</span><span class="sxs-lookup"><span data-stu-id="455e7-275">No.</span></span> <span data-ttu-id="455e7-276">Les étiquettes de confidentialité sont désactivées si le client Azure Information Protection est chargé dans Office pour Windows.</span><span class="sxs-lookup"><span data-stu-id="455e7-276">Sensitivity labels are turned off if the Azure Information Protection client is loaded in Office for Windows.</span></span>

<span data-ttu-id="455e7-277">Si le client Azure Information Protection est installé sur votre ordinateur, mais que vous préférez utiliser des étiquettes de confidentialité, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="455e7-277">If you have the Azure Information Protection client installed, but you want to use sensitivity labels instead, you can:</span></span>

1. <span data-ttu-id="455e7-278">Configurer le paramètre de stratégie de groupe  **Utiliser la fonctionnalité Confidentialité d’Office pour appliquer et afficher les étiquettes de confidentialité**, accessible sous **Configuration utilisateur/Modèles d’administration/Microsoft Office 2016/Paramètres de sécurité**.</span><span class="sxs-lookup"><span data-stu-id="455e7-278">Configure the **Use the Sensitivity feature in Office to apply and view sensitivity labels** Group Policy setting, which can be found under **User Configuration/Administrative Templates/Microsoft Office 2016/Security Settings**.</span></span>

  ><span data-ttu-id="455e7-279">Remarque : ce paramètre peut être déployé via les mécanismes de déploiement de stratégie de groupe traditionnels ou par le [service de stratégie Cloud Office](https://docs.microsoft.com/DeployOffice/overview-office-cloud-policy-service).</span><span class="sxs-lookup"><span data-stu-id="455e7-279">Note: this setting can be deployed via traditional group policy deployment mechanisms, or by the [Office cloud policy service](https://docs.microsoft.com/DeployOffice/overview-office-cloud-policy-service).</span></span> 
 
  <span data-ttu-id="455e7-280">Vous pouvez également désinstaller ou  [désactiver](https://support.office.com/article/view-manage-and-install-add-ins-in-office-programs-16278816-1948-4028-91e5-76dca5380f8d) le client Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="455e7-280">Alternatively, you can uninstall or [disable](https://support.office.com/article/view-manage-and-install-add-ins-in-office-programs-16278816-1948-4028-91e5-76dca5380f8d) the Azure Information Protection client.</span></span> 

2. <span data-ttu-id="455e7-281">Redémarrez toutes les applications Office.</span><span class="sxs-lookup"><span data-stu-id="455e7-281">Restart all Office applications.</span></span>

## <a name="will-sensitivity-labels-be-supported-in-non-subscription-versions-of-office-like-office-2016-or-office-2019"></a><span data-ttu-id="455e7-282">Les étiquettes de confidentialité seront-elles prises en charge dans les versions sans abonnement d'Office comme Office 2016 ou Office 2019 ?</span><span class="sxs-lookup"><span data-stu-id="455e7-282">Will sensitivity labels be supported in non-subscription versions of Office like Office 2016 or Office 2019?</span></span>

<span data-ttu-id="455e7-283">Non.</span><span class="sxs-lookup"><span data-stu-id="455e7-283">No.</span></span> <span data-ttu-id="455e7-284">Les étiquettes de confidentialité ne sont prises en charge que dans l’abonnement Office 365 et ne seront pas prises en charge dans les versions sans abonnement.</span><span class="sxs-lookup"><span data-stu-id="455e7-284">Sensitivity labels will only be supported in the Office 365 subscription and will not be supported in any non-subscription version.</span></span> <span data-ttu-id="455e7-285">Toutefois, le client de l’étiquetage unifié Azure Information Protection peut être utilisé dans les versions sans abonnement d’Office.</span><span class="sxs-lookup"><span data-stu-id="455e7-285">However, the Azure Information Protection unified labeling client may be used in non-subscription versions of Office.</span></span> 

## <a name="i-previously-deployed-protection-templates-before-setting-up-sensitivity-labels-where-did-they-go"></a><span data-ttu-id="455e7-286">J’ai précédemment déployé les modèles de protection avant de configurer les étiquettes de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="455e7-286">I previously deployed protection templates before setting up sensitivity labels.</span></span> <span data-ttu-id="455e7-287">Où sont-ils passés ?</span><span class="sxs-lookup"><span data-stu-id="455e7-287">Where did they go?</span></span>

<span data-ttu-id="455e7-288">Les [modèles de protection](https://docs.microsoft.com/azure/information-protection/configure-policy-templates) définis par l’administrateur sont masqués dans l’expérience utilisateur Office lorsque les étiquettes de confidentialité sont activées, car elles sont redondantes avec les étiquettes de confidentialité pour lesquelles le chiffrement est activé.</span><span class="sxs-lookup"><span data-stu-id="455e7-288">Administrator-defined [protection templates](https://docs.microsoft.com/azure/information-protection/configure-policy-templates) are hidden from the Office user experience when sensitivity labels are enabled because they are redundant with sensitivity labels that have encryption enabled.</span></span> 

## <a name="can-a-file-or-email-have-more-than-one-classification"></a><span data-ttu-id="455e7-289">Un fichier ou un e-mail peut-il avoir plusieurs classifications ?</span><span class="sxs-lookup"><span data-stu-id="455e7-289">Can a file or email have more than one classification?</span></span>

<span data-ttu-id="455e7-290">Non.</span><span class="sxs-lookup"><span data-stu-id="455e7-290">No.</span></span> <span data-ttu-id="455e7-291">Les utilisateurs ne peuvent sélectionner qu’une étiquette à la fois pour chaque document ou e-mail.</span><span class="sxs-lookup"><span data-stu-id="455e7-291">Users can select just one label at a time for each document or email, which often results in just one classification.</span></span>

## <a name="when-an-email-is-labeled-do-any-attachments-automatically-get-the-same-labeling"></a><span data-ttu-id="455e7-292">Lorsqu’un message électronique est étiqueté, les pièces jointes reçoivent-elles automatiquement la même étiquette ?</span><span class="sxs-lookup"><span data-stu-id="455e7-292">When an email is labeled, do any attachments automatically get the same labeling?</span></span>

<span data-ttu-id="455e7-293">Non.</span><span class="sxs-lookup"><span data-stu-id="455e7-293">No.</span></span> <span data-ttu-id="455e7-294">Lorsque vous étiquetez un message électronique comportant des pièces jointes, celles-ci n’héritent pas de la même étiquette.</span><span class="sxs-lookup"><span data-stu-id="455e7-294">When you label an email message that has attachments, those attachments do not inherit the same label.</span></span> <span data-ttu-id="455e7-295">Les pièces jointes restent sans étiquette ou ne conservent qu’une étiquette appliquée séparément.</span><span class="sxs-lookup"><span data-stu-id="455e7-295">The attachments remain either without a label or retain a separately applied label.</span></span> <span data-ttu-id="455e7-296">Toutefois, si l’étiquette de l’e-mail applique la protection, cette protection est appliquée aux pièces jointes Office.</span><span class="sxs-lookup"><span data-stu-id="455e7-296">However, if the label for the email applies protection, that protection is applied to Office attachments.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="455e7-297">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="455e7-297">Additional resources</span></span>

[<span data-ttu-id="455e7-298">Forum aux questions sur la classification et l’étiquetage dans Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="455e7-298">Frequently asked questions about classification and labeling in Azure Information Protection</span></span>](https://docs.microsoft.com/azure/information-protection/faqs-infoprotect)<br>
[<span data-ttu-id="455e7-299">Appliquer des étiquettes de niveau de confidentialité à vos documents et vos e-mails dans Office</span><span class="sxs-lookup"><span data-stu-id="455e7-299">Apply sensitivity labels to your documents and email within Office</span></span>](https://support.office.com/article/apply-sensitivity-labels-to-your-documents-and-email-within-office-2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9)
