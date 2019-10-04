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
ms.openlocfilehash: 1de7eadfcf95a54917c1d5e2cc0d42cc1ad486a5
ms.sourcegitcommit: c7f7ff463141f7d7f0970b64e5a04341db7e4fa8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2019
ms.locfileid: "37378649"
---
# <a name="how-sensitivity-labels-work-in-office-apps"></a><span data-ttu-id="b9edd-104">Fonctionnement des étiquettes de confidentialité dans les applications Office</span><span class="sxs-lookup"><span data-stu-id="b9edd-104">How sensitivity labels work in Office apps</span></span>

## <a name="what-prerequisites-are-there-to-use-sensitivity-labels-in-office-applications"></a><span data-ttu-id="b9edd-105">Quels sont les conditions préalables à l’utilisation des étiquettes de confidentialité dans les applications Office ?</span><span class="sxs-lookup"><span data-stu-id="b9edd-105">What prerequisites are there to use sensitivity labels in Office applications?</span></span>

### <a name="common-requirements"></a><span data-ttu-id="b9edd-106">Conditions courantes</span><span class="sxs-lookup"><span data-stu-id="b9edd-106">Common requirements</span></span> 

- <span data-ttu-id="b9edd-107">Les étiquettes de confidentialité unifiée doivent être [configurées et publiées dans le Centre de sécurité et conformité](https://aka.ms/managemip)</span><span class="sxs-lookup"><span data-stu-id="b9edd-107">Unified sensitivity labels must be [configured and published in the Security and Compliance Center](https://aka.ms/managemip)</span></span>
- <span data-ttu-id="b9edd-108">Les utilisateurs doivent être connectés à Office à l’aide de leur compte professionnel.</span><span class="sxs-lookup"><span data-stu-id="b9edd-108">Users must be signed in to Office with their work account.</span></span>
- <span data-ttu-id="b9edd-109">Les utilisateurs doivent disposer d’une licence Office 365 E3 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="b9edd-109">Users must have an Office 365 E3 or above license assigned.</span></span>

### <a name="additional-requirements-for-office-for-windows"></a><span data-ttu-id="b9edd-110">Conditions requises supplémentaires pour Office pour Windows</span><span class="sxs-lookup"><span data-stu-id="b9edd-110">Additional requirements for Office for Windows</span></span> 

- <span data-ttu-id="b9edd-111">Le client Azure Information Protection ne doit pas être exécuté dans Office.</span><span class="sxs-lookup"><span data-stu-id="b9edd-111">The Azure Information Protection client must not be running in Office.</span></span> <span data-ttu-id="b9edd-112">Voir aussi : [Les étiquettes de confidentialité peuvent-elles fonctionner avec le client Azure Information Protection dans Office pour Windows ?](#can-sensitivity-labels-run-alongside-the-azure-information-protection-client-in-office-for-windows).</span><span class="sxs-lookup"><span data-stu-id="b9edd-112">See also: [Can sensitivity labels run alongside the Azure Information Protection client in Office for Windows?](#can-sensitivity-labels-run-alongside-the-azure-information-protection-client-in-office-for-windows).</span></span>

### <a name="additional-requirements-for-outlook-on-all-platforms"></a><span data-ttu-id="b9edd-113">Conditions requises supplémentaires pour Outlook sur toutes les plateformes</span><span class="sxs-lookup"><span data-stu-id="b9edd-113">Additional requirements for Outlook on all platforms</span></span> 

- <span data-ttu-id="b9edd-114">Dans la configuration d’étiquette, si vous activez le marquage de contenu, vous devez utiliser Exchange Online pour que ce marquage de contenu soit insérée en transit.</span><span class="sxs-lookup"><span data-stu-id="b9edd-114">In your label configuration, if you turn on content marking, you must be using Exchange Online for that content marking to be inserted in transit.</span></span>

## <a name="what-sensitivity-label-capabilities-are-supported-in-office-today"></a><span data-ttu-id="b9edd-115">Quelles fonctionnalités d’étiquette de confidentialité sont prises en charge dans Office actuellement ?</span><span class="sxs-lookup"><span data-stu-id="b9edd-115">What sensitivity label capabilities are supported in Office today?</span></span> 

<table border="1" cellspacing="0" cellpadding="0">
<th><span data-ttu-id="b9edd-116"><font size="-1">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="b9edd-116"><font size="-1"></span></span><th><span data-ttu-id="b9edd-117"><font size="-1">Windows</span><span class="sxs-lookup"><span data-stu-id="b9edd-117"><font size="-1"></span></span><th><span data-ttu-id="b9edd-118"><font size="-1">Mac<th colspan="2"><font size="-1">iOS<th colspan="2"><font size="-1">Android<th colspan="2"><font size="-1">Web</span><span class="sxs-lookup"><span data-stu-id="b9edd-118"><font size="-1">Mac<th colspan="2"><font size="-1">iOS<th colspan="2"><font size="-1">Android<th colspan="2"><font size="-1">Web</span></span></tr>
<tr><td>

<td><span data-ttu-id="b9edd-119"><font size="-1"> Word</span><span class="sxs-lookup"><span data-stu-id="b9edd-119"><font size="-1">Word</span></span><br>
<span data-ttu-id="b9edd-120">Excel</span><span class="sxs-lookup"><span data-stu-id="b9edd-120">Excel</span></span><br>
<span data-ttu-id="b9edd-121">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="b9edd-121">PowerPoint</span></span><br>
<span data-ttu-id="b9edd-122">Outlook</span><span class="sxs-lookup"><span data-stu-id="b9edd-122">Outlook</span></span>


<td><span data-ttu-id="b9edd-123"><font size="-1"> Word</span><span class="sxs-lookup"><span data-stu-id="b9edd-123"><font size="-1">Word</span></span><br>
<span data-ttu-id="b9edd-124">Excel</span><span class="sxs-lookup"><span data-stu-id="b9edd-124">Excel</span></span><br>
<span data-ttu-id="b9edd-125">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="b9edd-125">PowerPoint</span></span><br>
<span data-ttu-id="b9edd-126">Outlook</span><span class="sxs-lookup"><span data-stu-id="b9edd-126">Outlook</span></span>

<td><span data-ttu-id="b9edd-127"><font size="-1"> Word</span><span class="sxs-lookup"><span data-stu-id="b9edd-127"><font size="-1">Word</span></span><br>
<span data-ttu-id="b9edd-128">Excel</span><span class="sxs-lookup"><span data-stu-id="b9edd-128">Excel</span></span><br>
<span data-ttu-id="b9edd-129">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="b9edd-129">PowerPoint</span></span>
<td><span data-ttu-id="b9edd-130"><font size="-1">Outlook</span><span class="sxs-lookup"><span data-stu-id="b9edd-130"><font size="-1">Outlook</span></span>

<td><span data-ttu-id="b9edd-131"><font size="-1"> Word</span><span class="sxs-lookup"><span data-stu-id="b9edd-131"><font size="-1">Word</span></span><br>
<span data-ttu-id="b9edd-132">Excel</span><span class="sxs-lookup"><span data-stu-id="b9edd-132">Excel</span></span><br>
<span data-ttu-id="b9edd-133">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="b9edd-133">PowerPoint</span></span>
<td><span data-ttu-id="b9edd-134"><font size="-1">Outlook</span><span class="sxs-lookup"><span data-stu-id="b9edd-134"><font size="-1">Outlook</span></span>

<td><span data-ttu-id="b9edd-135"><font size="-1"> Word</span><span class="sxs-lookup"><span data-stu-id="b9edd-135"><font size="-1">Word</span></span><br>
<span data-ttu-id="b9edd-136">Excel</span><span class="sxs-lookup"><span data-stu-id="b9edd-136">Excel</span></span><br>
<span data-ttu-id="b9edd-137">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="b9edd-137">PowerPoint</span></span>
<td><span data-ttu-id="b9edd-138"><font size="-1"> Outlook </b>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-138">Outlook</span></span></tr>

<tr>
<td><span data-ttu-id="b9edd-139"><font size="-1">Appliquer, modifier ou supprimer manuellement une étiquette</span><span class="sxs-lookup"><span data-stu-id="b9edd-139"><font size="-1">Manually apply, change, or remove label</span></span><td><span data-ttu-id="b9edd-140"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-140">Yes</span></span><br><span data-ttu-id="b9edd-141"><font size="-1">1910+</font>

</span><span class="sxs-lookup"><span data-stu-id="b9edd-141"><font size="-1">1910+</font>

</span></span><td><span data-ttu-id="b9edd-142"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-142">Yes</span></span><br><span data-ttu-id="b9edd-143"><font size="-1">16.21.0+</font>

</span><span class="sxs-lookup"><span data-stu-id="b9edd-143"><font size="-1">16.21.0+</font>

</span></span><td><span data-ttu-id="b9edd-144"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-144">Yes</span></span><br><span data-ttu-id="b9edd-145"><font size="-1">2.21+</font>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-145"><font size="-1">2.21+</font>
</span></span><td><span data-ttu-id="b9edd-146"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-146"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="b9edd-147"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-147">Yes</span></span><br><span data-ttu-id="b9edd-148"><font size="-1">16.0.11231+</font>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-148"><font size="-1">16.0.11231+</font>
</span></span><td><span data-ttu-id="b9edd-149"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-149"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="b9edd-150"><font size="-1">Bientôt disponible<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b9edd-150"><font size="-1">Coming soon<sup>3</sup></span></span><td><span data-ttu-id="b9edd-151"><font size="-1">Bientôt disponible<sup>3</sup>

</span><span class="sxs-lookup"><span data-stu-id="b9edd-151"><font size="-1">Coming soon<sup>3</sup>

</span></span><tr>
<td><span data-ttu-id="b9edd-152"><font size="-1"><a href="https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels#what-label-policies-can-do">Appliquer une étiquette par défaut</a>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-152"><font size="-1"><a href="https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels#what-label-policies-can-do">Apply a default label</a>
</span></span><td><span data-ttu-id="b9edd-153"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-153">Yes</span></span><br><span data-ttu-id="b9edd-154"><font size="-1">1910+</font>

</span><span class="sxs-lookup"><span data-stu-id="b9edd-154"><font size="-1">1910+</font>

</span></span><td><span data-ttu-id="b9edd-155"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-155">Yes</span></span><br><span data-ttu-id="b9edd-156"><font size="-1">16.21.0+</font>

</span><span class="sxs-lookup"><span data-stu-id="b9edd-156"><font size="-1">16.21.0+</font>

</span></span><td><span data-ttu-id="b9edd-157"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-157">Yes</span></span><br><span data-ttu-id="b9edd-158"><font size="-1">2.21+</font>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-158"><font size="-1">2.21+</font>
</span></span><td><span data-ttu-id="b9edd-159"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-159"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="b9edd-160"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-160">Yes</span></span><br><span data-ttu-id="b9edd-161"><font size="-1">16.0.11231+</font>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-161"><font size="-1">16.0.11231+</font>
</span></span><td><span data-ttu-id="b9edd-162"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-162"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="b9edd-163"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-163"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="b9edd-164"><font size="-1">Bientôt disponible<sup>3</sup>

</span><span class="sxs-lookup"><span data-stu-id="b9edd-164"><font size="-1">Coming soon<sup>3</sup>

</span></span><tr><td><span data-ttu-id="b9edd-165"><font size="-1"><a href="https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels#what-label-policies-can-do">Demander une justification pour changer une étiquette</a><sup>1</sup>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-165"><font size="-1"><a href="https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels#what-label-policies-can-do">Require a justification for changing a label</a><sup>1</sup>
</span></span><td><span data-ttu-id="b9edd-166"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-166">Yes</span></span><br><span data-ttu-id="b9edd-167"><font size="-1">1910+</font>

</span><span class="sxs-lookup"><span data-stu-id="b9edd-167"><font size="-1">1910+</font>

</span></span><td><span data-ttu-id="b9edd-168"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-168">Yes</span></span><br><span data-ttu-id="b9edd-169"><font size="-1">16.21.0+</font>

</span><span class="sxs-lookup"><span data-stu-id="b9edd-169"><font size="-1">16.21.0+</font>

</span></span><td><span data-ttu-id="b9edd-170"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-170">Yes</span></span><br><span data-ttu-id="b9edd-171"><font size="-1">2.21+</font>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-171"><font size="-1">2.21+</font>
</span></span><td><span data-ttu-id="b9edd-172"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-172"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="b9edd-173"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-173">Yes</span></span><br><span data-ttu-id="b9edd-174"><font size="-1">16.0.11231+</font>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-174"><font size="-1">16.0.11231+</font>
</span></span><td><span data-ttu-id="b9edd-175"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-175"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="b9edd-176"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-176"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="b9edd-177"><font size="-1">Bientôt disponible<sup>3</sup>

</span><span class="sxs-lookup"><span data-stu-id="b9edd-177"><font size="-1">Coming soon<sup>3</sup>

</span></span><tr><td><span data-ttu-id="b9edd-178"><font size="-1"><a href="https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels#what-label-policies-can-do">Fournir un lien d’aide vers une page d’aide personnalisée</a>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-178"><font size="-1"><a href="https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels#what-label-policies-can-do">Provide help link to a custom help page</a>
</span></span><td><span data-ttu-id="b9edd-179"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-179">Yes</span></span><br><span data-ttu-id="b9edd-180"><font size="-1">1910+</font>

</span><span class="sxs-lookup"><span data-stu-id="b9edd-180"><font size="-1">1910+</font>

</span></span><td><span data-ttu-id="b9edd-181"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-181">Yes</span></span><br><span data-ttu-id="b9edd-182"><font size="-1">16.21.0+</font>

</span><span class="sxs-lookup"><span data-stu-id="b9edd-182"><font size="-1">16.21.0+</font>

</span></span><td><span data-ttu-id="b9edd-183"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-183">Yes</span></span><br><span data-ttu-id="b9edd-184"><font size="-1">2.21+</font>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-184"><font size="-1">2.21+</font>
</span></span><td><span data-ttu-id="b9edd-185"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-185"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="b9edd-186"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-186">Yes</span></span><br><span data-ttu-id="b9edd-187"><font size="-1">16.0.11231+</font>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-187"><font size="-1">16.0.11231+</font>
</span></span><td><span data-ttu-id="b9edd-188"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-188"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="b9edd-189"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-189"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="b9edd-190"><font size="-1">Bientôt disponible<sup>3</sup>

</span><span class="sxs-lookup"><span data-stu-id="b9edd-190"><font size="-1">Coming soon<sup>3</sup>

</span></span><tr><td><span data-ttu-id="b9edd-191"><font size="-1"><a href="https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels#what-sensitivity-labels-can-do">Marquer le contenu</a>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-191"><font size="-1"><a href="https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels#what-sensitivity-labels-can-do">Mark the content</a>
</span></span><td><span data-ttu-id="b9edd-192"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-192">Yes</span></span><br><span data-ttu-id="b9edd-193"><font size="-1">1910+</font>

</span><span class="sxs-lookup"><span data-stu-id="b9edd-193"><font size="-1">1910+</font>

</span></span><td><span data-ttu-id="b9edd-194"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-194">Yes</span></span><br><span data-ttu-id="b9edd-195"><font size="-1">16.21.0+</font>

</span><span class="sxs-lookup"><span data-stu-id="b9edd-195"><font size="-1">16.21.0+</font>

</span></span><td><span data-ttu-id="b9edd-196"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-196">Yes</span></span><br><span data-ttu-id="b9edd-197"><font size="-1">2.21+</font>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-197"><font size="-1">2.21+</font>
</span></span><td><span data-ttu-id="b9edd-198"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-198"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="b9edd-199"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-199">Yes</span></span><br><span data-ttu-id="b9edd-200"><font size="-1">16.0.11231+</font
</span><span class="sxs-lookup"><span data-stu-id="b9edd-200"><font size="-1">16.0.11231+</font
</span></span>><td><span data-ttu-id="b9edd-201"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-201"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="b9edd-202"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-202"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="b9edd-203"><font size="-1">Bientôt disponible<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b9edd-203"><font size="-1">Coming soon<sup>3</sup></span></span>

<tr><td><span data-ttu-id="b9edd-204"><font size="-1">Attribuer des autorisations prédéfinies</span><span class="sxs-lookup"><span data-stu-id="b9edd-204"><font size="-1">Assign pre-defined permissions</span></span>
<td><span data-ttu-id="b9edd-205"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-205">Yes</span></span><br><span data-ttu-id="b9edd-206"><font size="-1">1910+</font>

</span><span class="sxs-lookup"><span data-stu-id="b9edd-206"><font size="-1">1910+</font>

</span></span><td><span data-ttu-id="b9edd-207"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-207">Yes</span></span><br><span data-ttu-id="b9edd-208"><font size="-1">16.21.0+</font>

</span><span class="sxs-lookup"><span data-stu-id="b9edd-208"><font size="-1">16.21.0+</font>

</span></span><td><span data-ttu-id="b9edd-209"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-209">Yes</span></span><br><span data-ttu-id="b9edd-210"><font size="-1">2.21+</font>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-210"><font size="-1">2.21+</font>
</span></span><td><span data-ttu-id="b9edd-211"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-211"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="b9edd-212"><font size="-1"><b>Oui</b></span><span class="sxs-lookup"><span data-stu-id="b9edd-212">Yes</span></span><br><span data-ttu-id="b9edd-213"><font size="-1">16.0.11231+</font>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-213"><font size="-1">16.0.11231+</font>
</span></span><td><span data-ttu-id="b9edd-214"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-214"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="b9edd-215"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-215"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="b9edd-216"><font size="-1">Bientôt disponible<sup>3</sup>

</span><span class="sxs-lookup"><span data-stu-id="b9edd-216"><font size="-1">Coming soon<sup>3</sup>

</span></span><tr><td><span data-ttu-id="b9edd-217"><font size="-1"><a href="https://docs.microsoft.com/microsoft-365/compliance/encryption-sensitivity-labels#let-users-assign-permissions">Permettre aux utilisateurs d’attribuer des autorisations</a>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-217">Let users assign permissions</span></span><td><span data-ttu-id="b9edd-218"><font size="-1"><b>Oui</b><sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="b9edd-218"><font size="-1"><b>Yes</b><sup>2</sup></span></span><br><span data-ttu-id="b9edd-219"><font size="-1">1910+</font>

</span><span class="sxs-lookup"><span data-stu-id="b9edd-219"><font size="-1">1910+</font>

</span></span><td><span data-ttu-id="b9edd-220"><font size="-1"><b>Oui</b><sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="b9edd-220"><font size="-1"><b>Yes</b><sup>2</sup></span></span><br><span data-ttu-id="b9edd-221"><font size="-1">16.21.0+</font></span><span class="sxs-lookup"><span data-stu-id="b9edd-221"><font size="-1">16.21.0+</font></span></span>

<td><span data-ttu-id="b9edd-222"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-222"><font size="-1">TBD</span></span>
<td><span data-ttu-id="b9edd-223"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-223"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="b9edd-224"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-224"><font size="-1">TBD</span></span><td
><span data-ttu-id="b9edd-225"><font size="-1">Bientôt disponible<sup>3</sup>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-225"><font size="-1">Coming soon<sup>3</sup>
</span></span><td><span data-ttu-id="b9edd-226"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-226"><font size="-1">TBD</span></span>
<td><span data-ttu-id="b9edd-227"><font size="-1">Bientôt disponible<sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="b9edd-227"><font size="-1">Coming soon<sup>3</sup></span></span>

<tr><td><span data-ttu-id="b9edd-228"><font size="-1">Envoyer les données d’<a href="https://docs.microsoft.com/microsoft-365/compliance/label-analytics">analyse des étiquettes</a> pour les administrateurs</span><span class="sxs-lookup"><span data-stu-id="b9edd-228"><font size="-1">Send <a href="https://docs.microsoft.com/microsoft-365/compliance/label-analytics">label analytics</a> data for administrators</span></span>
<td><span data-ttu-id="b9edd-229"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-229"><font size="-1">TBD</span></span>

<td><span data-ttu-id="b9edd-230"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-230"><font size="-1">TBD</span></span>

<td><span data-ttu-id="b9edd-231"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-231"><font size="-1">TBD</span></span>
<td><span data-ttu-id="b9edd-232"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-232"><font size="-1">TBD</span></span>
<td><span data-ttu-id="b9edd-233"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-233"><font size="-1">TBD</span></span>
<td><span data-ttu-id="b9edd-234"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-234"><font size="-1">TBD</span></span>
<td><span data-ttu-id="b9edd-235"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-235"><font size="-1">TBD</span></span>
<td><span data-ttu-id="b9edd-236"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-236"><font size="-1">TBD</span></span>

<tr><td><span data-ttu-id="b9edd-237"><font size="-1">Demander aux utilisateurs d'appliquer une étiquette à leurs e-mails et documents</span><span class="sxs-lookup"><span data-stu-id="b9edd-237"><font size="-1">Require users to apply a label to their email and documents</span></span>
<td><span data-ttu-id="b9edd-238"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-238"><font size="-1">TBD</span></span>

<td><span data-ttu-id="b9edd-239"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-239"><font size="-1">TBD</span></span>

<td><span data-ttu-id="b9edd-240"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-240"><font size="-1">TBD</span></span>
<td><span data-ttu-id="b9edd-241"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-241"><font size="-1">TBD</span></span>
<td><span data-ttu-id="b9edd-242"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-242"><font size="-1">TBD</span></span>
<td><span data-ttu-id="b9edd-243"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-243"><font size="-1">TBD</span></span>
<td><span data-ttu-id="b9edd-244"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-244"><font size="-1">TBD</span></span>
<td><span data-ttu-id="b9edd-245"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-245"><font size="-1">TBD</span></span>

<tr><td><span data-ttu-id="b9edd-246"><font size="-1"><a href="https://docs.microsoft.com/microsoft-365/compliance/apply-sensitivity-label-automatically">Appliquer automatiquement une étiquette de confidentialité au contenu</a>
</span><span class="sxs-lookup"><span data-stu-id="b9edd-246">Apply a sensitivity label to content automatically</span></span><td><span data-ttu-id="b9edd-247"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-247"><font size="-1">TBD</span></span>

<td><span data-ttu-id="b9edd-248"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-248"><font size="-1">TBD</span></span>

<td><span data-ttu-id="b9edd-249"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-249"><font size="-1">TBD</span></span>
<td><span data-ttu-id="b9edd-250"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-250"><font size="-1">TBD</span></span>
<td><span data-ttu-id="b9edd-251"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-251"><font size="-1">TBD</span></span>
<td><span data-ttu-id="b9edd-252"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-252"><font size="-1">TBD</span></span>
<td><span data-ttu-id="b9edd-253"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-253"><font size="-1">TBD</span></span>
<td><span data-ttu-id="b9edd-254"><font size="-1">À DÉFINIR</span><span class="sxs-lookup"><span data-stu-id="b9edd-254"><font size="-1">TBD</span></span>
</table>

<br><span data-ttu-id="b9edd-255"><sup>1</sup>Si elles sont configurées, les utilisateurs sont invités à justifier les rétrogradations d’étiquettes.</span><span class="sxs-lookup"><span data-stu-id="b9edd-255"><sup>1</sup>If configured, users are prompted to justify label downgrades.</span></span> <span data-ttu-id="b9edd-256">Toutefois, les données de justification ne sont pas encore disponibles pour les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="b9edd-256">However, the justification data is not made available for administrators yet.</span></span> <span data-ttu-id="b9edd-257">Elles seront disponibles lorsque la fonctionnalité « envoyer les données d’analyse des étiquettes pour les administrateurs » est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b9edd-257">It will become available when the “send label analytics data for administrators” capability is supported.</span></span>
<br><span data-ttu-id="b9edd-258"><sup>2</sup>Permettre aux utilisateurs d'attribuer des autorisations n'est actuellement disponible que dans Outlook pour Windows et Mac.</span><span class="sxs-lookup"><span data-stu-id="b9edd-258"><sup>2</sup>Let users assign permissions is currently only available in Outlook for Windows and Mac.</span></span> <span data-ttu-id="b9edd-259">La disponibilité pour Word, Excel et PowerPoint est à définir.</span><span class="sxs-lookup"><span data-stu-id="b9edd-259">Availability for Word, Excel, and PowerPoint is TBD.</span></span>
<br><span data-ttu-id="b9edd-260"><sup>3</sup>Prévu pour le quatrième trimestre de l'année civile 2019.</span><span class="sxs-lookup"><span data-stu-id="b9edd-260"><sup>3</sup>Expected Q4 of calendar year 2019.</span></span>

## <a name="when-do-content-marks-or-encryption-get-applied-after-content-is-given-a-sensitivity-label"></a><span data-ttu-id="b9edd-261">Quand les marques de contenu ou le chiffrement sont-ils appliqués une fois qu’une étiquette de confidentialité est attribuée au contenu ?</span><span class="sxs-lookup"><span data-stu-id="b9edd-261">When do content marks or encryption get applied after content is given a sensitivity label?</span></span>

| <span data-ttu-id="b9edd-262">Application</span><span class="sxs-lookup"><span data-stu-id="b9edd-262">Application</span></span> | <span data-ttu-id="b9edd-263">Marquage du contenu</span><span class="sxs-lookup"><span data-stu-id="b9edd-263">Content marking</span></span> | <span data-ttu-id="b9edd-264">Chiffrement</span><span class="sxs-lookup"><span data-stu-id="b9edd-264">Encryption</span></span>
| --- | --- | --- |
| <span data-ttu-id="b9edd-265">Word, Excel, PowerPoint sur toutes les plateformes</span><span class="sxs-lookup"><span data-stu-id="b9edd-265">Word, Excel, PowerPoint on all platforms</span></span> | <span data-ttu-id="b9edd-266">Immédiatement</span><span class="sxs-lookup"><span data-stu-id="b9edd-266">Immediately</span></span> | <span data-ttu-id="b9edd-267">Immédiatement</span><span class="sxs-lookup"><span data-stu-id="b9edd-267">Immediately</span></span> |
| <span data-ttu-id="b9edd-268">Outlook pour PC et Mac</span><span class="sxs-lookup"><span data-stu-id="b9edd-268">Outlook for PC and Mac</span></span> | <span data-ttu-id="b9edd-269">Une fois l’e-mail envoyé par Exchange Online</span><span class="sxs-lookup"><span data-stu-id="b9edd-269">After the email is sent by Exchange Online</span></span> | <span data-ttu-id="b9edd-270">Immédiatement</span><span class="sxs-lookup"><span data-stu-id="b9edd-270">Immediately</span></span> |
| <span data-ttu-id="b9edd-271">Word, Excel, PowerPoint sur toutes les plateformes</span><span class="sxs-lookup"><span data-stu-id="b9edd-271">Word, Excel, PowerPoint on all platforms</span></span> | <span data-ttu-id="b9edd-272">Une fois l’e-mail envoyé par Exchange Online</span><span class="sxs-lookup"><span data-stu-id="b9edd-272">After the email is sent by Exchange Online</span></span> | <span data-ttu-id="b9edd-273">Une fois l’e-mail envoyé par Exchange Online</span><span class="sxs-lookup"><span data-stu-id="b9edd-273">After the email is sent by Exchange Online</span></span> |

## <a name="can-sensitivity-labels-run-alongside-the-azure-information-protection-client-in-office-for-windows"></a><span data-ttu-id="b9edd-274">Les étiquettes de confidentialité peuvent-elles fonctionner avec le client Azure Information Protection dans Office pour Windows ?</span><span class="sxs-lookup"><span data-stu-id="b9edd-274">Can sensitivity labels run alongside the Azure Information Protection client in Office for Windows?</span></span>

<span data-ttu-id="b9edd-275">Non.</span><span class="sxs-lookup"><span data-stu-id="b9edd-275">No.</span></span> <span data-ttu-id="b9edd-276">Les étiquettes de confidentialité sont désactivées si le client Azure Information Protection est chargé dans Office pour Windows.</span><span class="sxs-lookup"><span data-stu-id="b9edd-276">Sensitivity labels are turned off if the Azure Information Protection client is loaded in Office for Windows.</span></span>

<span data-ttu-id="b9edd-277">Si le client Azure Information Protection est installé sur votre ordinateur, mais que vous préférez utiliser des étiquettes de confidentialité, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="b9edd-277">If you have the Azure Information Protection client installed, but you want to use sensitivity labels instead, you can:</span></span>

1. <span data-ttu-id="b9edd-278">Configurer le paramètre de stratégie de groupe  **Utiliser la fonctionnalité Confidentialité d’Office pour appliquer et afficher les étiquettes de confidentialité**, accessible sous **Configuration utilisateur/Modèles d’administration/Microsoft Office 2016/Paramètres de sécurité**.</span><span class="sxs-lookup"><span data-stu-id="b9edd-278">Configure the **Use the Sensitivity feature in Office to apply and view sensitivity labels** Group Policy setting, which can be found under **User Configuration/Administrative Templates/Microsoft Office 2016/Security Settings**.</span></span>

  ><span data-ttu-id="b9edd-279">Remarque : ce paramètre peut être déployé via les mécanismes de déploiement de stratégie de groupe traditionnels ou par le [service de stratégie Cloud Office](https://docs.microsoft.com/DeployOffice/overview-office-cloud-policy-service).</span><span class="sxs-lookup"><span data-stu-id="b9edd-279">Note: this setting can be deployed via traditional group policy deployment mechanisms, or by the [Office cloud policy service](https://docs.microsoft.com/DeployOffice/overview-office-cloud-policy-service).</span></span> 
 
  <span data-ttu-id="b9edd-280">Vous pouvez également désinstaller ou  [désactiver](https://support.office.com/article/view-manage-and-install-add-ins-in-office-programs-16278816-1948-4028-91e5-76dca5380f8d) le client Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="b9edd-280">Alternatively, you can uninstall or [disable](https://support.office.com/article/view-manage-and-install-add-ins-in-office-programs-16278816-1948-4028-91e5-76dca5380f8d) the Azure Information Protection client.</span></span> 

2. <span data-ttu-id="b9edd-281">Redémarrez toutes les applications Office.</span><span class="sxs-lookup"><span data-stu-id="b9edd-281">Restart all Office applications.</span></span>

## <a name="will-sensitivity-labels-be-supported-in-non-subscription-versions-of-office-like-office-2016-or-office-2019"></a><span data-ttu-id="b9edd-282">Les étiquettes de confidentialité seront-elles prises en charge dans les versions sans abonnement d'Office comme Office 2016 ou Office 2019 ?</span><span class="sxs-lookup"><span data-stu-id="b9edd-282">Will sensitivity labels be supported in non-subscription versions of Office like Office 2016 or Office 2019?</span></span>

<span data-ttu-id="b9edd-283">Non.</span><span class="sxs-lookup"><span data-stu-id="b9edd-283">No.</span></span> <span data-ttu-id="b9edd-284">Les étiquettes de confidentialité ne sont prises en charge que dans l’abonnement Office 365 et ne seront pas prises en charge dans les versions sans abonnement.</span><span class="sxs-lookup"><span data-stu-id="b9edd-284">Sensitivity labels will only be supported in the Office 365 subscription and will not be supported in any non-subscription version.</span></span> <span data-ttu-id="b9edd-285">Toutefois, le client de l’étiquetage unifié Azure Information Protection peut être utilisé dans les versions sans abonnement d’Office.</span><span class="sxs-lookup"><span data-stu-id="b9edd-285">However, the Azure Information Protection unified labeling client may be used in non-subscription versions of Office.</span></span> 

## <a name="i-previously-deployed-protection-templates-before-setting-up-sensitivity-labels-where-did-they-go"></a><span data-ttu-id="b9edd-286">J’ai précédemment déployé les modèles de protection avant de configurer les étiquettes de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="b9edd-286">I previously deployed protection templates before setting up sensitivity labels.</span></span> <span data-ttu-id="b9edd-287">Où sont-ils passés ?</span><span class="sxs-lookup"><span data-stu-id="b9edd-287">Where did they go?</span></span>

<span data-ttu-id="b9edd-288">Les [modèles de protection](https://docs.microsoft.com/azure/information-protection/configure-policy-templates) définis par l’administrateur sont masqués dans l’expérience utilisateur Office lorsque les étiquettes de confidentialité sont activées, car elles sont redondantes avec les étiquettes de confidentialité pour lesquelles le chiffrement est activé.</span><span class="sxs-lookup"><span data-stu-id="b9edd-288">Administrator-defined [protection templates](https://docs.microsoft.com/azure/information-protection/configure-policy-templates) are hidden from the Office user experience when sensitivity labels are enabled because they are redundant with sensitivity labels that have encryption enabled.</span></span> 

## <a name="can-a-file-or-email-have-more-than-one-classification"></a><span data-ttu-id="b9edd-289">Un fichier ou un e-mail peut-il avoir plusieurs classifications ?</span><span class="sxs-lookup"><span data-stu-id="b9edd-289">Can a file or email have more than one classification?</span></span>

<span data-ttu-id="b9edd-290">Les utilisateurs ne peuvent sélectionner qu’une seule étiquette à la fois pour chaque document ou e-mail, ce qui se traduit souvent par une seule classification.</span><span class="sxs-lookup"><span data-stu-id="b9edd-290">Users can select just one label at a time for each document or email, which often results in just one classification.</span></span> <span data-ttu-id="b9edd-291">Toutefois, si les utilisateurs sélectionnent une sous-étiquette, cela a pour effet d’appliquer deux étiquettes en même temps : une étiquette primaire et une étiquette secondaire.</span><span class="sxs-lookup"><span data-stu-id="b9edd-291">However, if users select a sublabel, this actually applies two labels at the same time; a primary label and a secondary label.</span></span> <span data-ttu-id="b9edd-292">L’utilisation de sous-étiquettes permet à un fichier d’avoir deux classifications indiquant une relation parent/enfant pour un niveau de contrôle supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="b9edd-292">By using sublabels, a file can have two classifications that denote a parent/child relationship for an additional level of control.</span></span> 

<span data-ttu-id="b9edd-293">Par exemple, l’étiquette  **Confidentiel**  pourrait contenir des sous-étiquettes telles que  **Légal** et **Finance**.</span><span class="sxs-lookup"><span data-stu-id="b9edd-293">For example, the label **Confidential** might contain sublabels such as **Legal** and **Finance**.</span></span> <span data-ttu-id="b9edd-294">Vous pouvez appliquer différentes marquages visuels de classification et différents modèles de gestion des droits à ces sous-étiquettes.</span><span class="sxs-lookup"><span data-stu-id="b9edd-294">You can apply different classification visual markings and different Rights Management templates to these sublabels.</span></span> <span data-ttu-id="b9edd-295">Un utilisateur ne peut pas sélectionner l’étiquette **Confidentiel** , mais une seule de ses sous-étiquettes, par exemple  **Légal**.</span><span class="sxs-lookup"><span data-stu-id="b9edd-295">A user cannot select the **Confidential** label by itself; only one of its sublabels, such as **Legal**.</span></span> <span data-ttu-id="b9edd-296">Par conséquent, l’étiquette qu’ils voient s’afficher est **Confidentiel** / **Légal**.</span><span class="sxs-lookup"><span data-stu-id="b9edd-296">As a result, the label that they see set is **Confidential** / **Legal**.</span></span> <span data-ttu-id="b9edd-297">Les métadonnées associées à ce fichier incluent une propriété de texte personnalisée pour **Confidentiel**, une propriété de texte personnalisée pour **Légal** et une autre qui contient les deux valeurs (**Confidentiel Légal**).</span><span class="sxs-lookup"><span data-stu-id="b9edd-297">The metadata for that file includes one custom text property for **Confidential**, one custom text property for **Legal**, and another that contains both values (**Confidential Legal**).</span></span> 

<span data-ttu-id="b9edd-298">Lorsque vous utilisez des sous-étiquettes, ne configurez pas les marquages visuels, la protection et les conditions sur l’étiquette primaire.</span><span class="sxs-lookup"><span data-stu-id="b9edd-298">When you use sublabels, don't configure visual markings, protection, and conditions at the primary label.</span></span> <span data-ttu-id="b9edd-299">Lorsque vous utilisez des sous-niveaux, configurez ces paramètres sur la sous-étiquette uniquement.</span><span class="sxs-lookup"><span data-stu-id="b9edd-299">When you use sublevels, configure these setting on the sublabel only.</span></span> <span data-ttu-id="b9edd-300">Si vous configurez ces paramètres sur l’étiquette primaire et sur sa sous-étiquette, les paramètres de la sous-étiquette sont prioritaires.</span><span class="sxs-lookup"><span data-stu-id="b9edd-300">If you configure these settings on the primary label and its sublabel, the settings at the sublabel take precedence.</span></span>

## <a name="when-an-email-is-labeled-do-any-attachments-automatically-get-the-same-labeling"></a><span data-ttu-id="b9edd-301">Lorsqu’un message électronique est étiqueté, les pièces jointes reçoivent-elles automatiquement la même étiquette ?</span><span class="sxs-lookup"><span data-stu-id="b9edd-301">When an email is labeled, do any attachments automatically get the same labeling?</span></span>

<span data-ttu-id="b9edd-302">Non.</span><span class="sxs-lookup"><span data-stu-id="b9edd-302">No.</span></span> <span data-ttu-id="b9edd-303">Lorsque vous étiquetez un message électronique comportant des pièces jointes, celles-ci n’héritent pas de la même étiquette.</span><span class="sxs-lookup"><span data-stu-id="b9edd-303">When you label an email message that has attachments, those attachments do not inherit the same label.</span></span> <span data-ttu-id="b9edd-304">Les pièces jointes restent sans étiquette ou ne conservent qu’une étiquette appliquée séparément.</span><span class="sxs-lookup"><span data-stu-id="b9edd-304">The attachments remain either without a label or retain a separately applied label.</span></span> <span data-ttu-id="b9edd-305">Toutefois, si l’étiquette de l’e-mail applique la protection, cette protection est appliquée aux pièces jointes Office.</span><span class="sxs-lookup"><span data-stu-id="b9edd-305">However, if the label for the email applies protection, that protection is applied to Office attachments.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9edd-306">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="b9edd-306">Additional resources</span></span>

[<span data-ttu-id="b9edd-307">Forum aux questions sur la classification et l’étiquetage dans Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="b9edd-307">Frequently asked questions about classification and labeling in Azure Information Protection</span></span>](https://docs.microsoft.com/azure/information-protection/faqs-infoprotect)<br>
[<span data-ttu-id="b9edd-308">Appliquer des étiquettes de niveau de confidentialité à vos documents et vos e-mails dans Office</span><span class="sxs-lookup"><span data-stu-id="b9edd-308">Apply sensitivity labels to your documents and email within Office</span></span>](https://support.office.com/article/apply-sensitivity-labels-to-your-documents-and-email-within-office-2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9)