---
title: Utiliser l Microsoft OneDrive Learning opérabilité des outils de gestion
ms.author: heidip
author: MicrosoftHeidi
manager: serdars
ms.reviewer: amitman
audience: admin
ms.topic: article
ms.service: o365-administration
f1.keywords:
- CSH
ms.collection: M365-modern-desktop
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
description: Créez et classez des devoirs, créez et organisez du contenu de cours et collaborez sur des fichiers en temps réel avec la nouvelle application d’interopérabilité Microsoft OneDrive Learning Tools.
ms.openlocfilehash: 985a316bac689b9bc6c53ab65782d548fcad0db8
ms.sourcegitcommit: a4c93a4c7d7db08fe3b032b58d5c7dbbb9476e90
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2021
ms.locfileid: "53257019"
---
# <a name="integrate-microsoft-onedrive-lti-with-canvas"></a><span data-ttu-id="65617-103">Intégrer Microsoft OneDrive LTI à Canvas</span><span class="sxs-lookup"><span data-stu-id="65617-103">Integrate Microsoft OneDrive LTI with Canvas</span></span>

<span data-ttu-id="65617-104">L’intégration Microsoft OneDrive LTI à Canvas est un processus en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="65617-104">Integrating Microsoft OneDrive LTI with Canvas is a two step process.</span></span> <span data-ttu-id="65617-105">La première étape active la Microsoft OneDrive canvas, et la deuxième étape rend l’Microsoft OneDrive LTI disponible dans les cours Canvas.</span><span class="sxs-lookup"><span data-stu-id="65617-105">The first step enables Microsoft OneDrive in Canvas, and the second step makes the Microsoft OneDrive LTI available within Canvas courses.</span></span>

## <a name="recommended-browser-settings"></a><span data-ttu-id="65617-106">Paramètres de navigateur recommandés</span><span class="sxs-lookup"><span data-stu-id="65617-106">Recommended browser settings</span></span>

- <span data-ttu-id="65617-107">Les cookies doivent être activés pour Microsoft OneDrive.</span><span class="sxs-lookup"><span data-stu-id="65617-107">Cookies should be enabled for Microsoft OneDrive.</span></span>
- <span data-ttu-id="65617-108">Les fenêtres pop-up ne doivent pas être bloquées Microsoft OneDrive.</span><span class="sxs-lookup"><span data-stu-id="65617-108">Popups should not be blocked for Microsoft OneDrive.</span></span>

> [!NOTE]
> - <span data-ttu-id="65617-109">Les cookies ne sont pas activés par défaut dans le navigateur Chrome en modecognito et doivent être activés.</span><span class="sxs-lookup"><span data-stu-id="65617-109">Cookies are not enabled by default in the Chrome browser incognito mode, and will need to be enabled.</span></span>
> - <span data-ttu-id="65617-110">Microsoft OneDrive LTI fonctionne en mode privé dans Microsoft Edge navigateur.</span><span class="sxs-lookup"><span data-stu-id="65617-110">Microsoft OneDrive LTI works in the private mode in Microsoft Edge browser.</span></span> <span data-ttu-id="65617-111">Assurez-vous que vous n’avez pas bloqué les cookies (qui sont activés par défaut).</span><span class="sxs-lookup"><span data-stu-id="65617-111">Ensure that you have not blocked cookies (which are enabled by default).</span></span>

## <a name="enable-microsoft-onedrive-lti-in-canvas"></a><span data-ttu-id="65617-112">Activer Microsoft OneDrive LTI dans Canvas</span><span class="sxs-lookup"><span data-stu-id="65617-112">Enable Microsoft OneDrive LTI in Canvas</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65617-113">La personne qui effectue cette intégration doit être administrateur de Canvas et administrateur du client Microsoft 365 client.</span><span class="sxs-lookup"><span data-stu-id="65617-113">The person who performs this integration should be an administrator of Canvas and an administrator of the Microsoft 365 tenant.</span></span>

1. <span data-ttu-id="65617-114">Connectez-vous <a href="https://onedrivelti.microsoft.com/admin" target="_blank">au Microsoft OneDrive d’inscription LTI</a></span><span class="sxs-lookup"><span data-stu-id="65617-114">Sign into the <a href="https://onedrivelti.microsoft.com/admin" target="_blank">Microsoft OneDrive LTI Registration Portal</a></span></span>
1. <span data-ttu-id="65617-115">Sélectionnez le **bouton Consentement de l’administrateur** et acceptez les autorisations.</span><span class="sxs-lookup"><span data-stu-id="65617-115">Select the **Admin Consent** button and accept the permissions.</span></span>
1. <span data-ttu-id="65617-116">Sélectionnez **le bouton Créer un client LTI.**</span><span class="sxs-lookup"><span data-stu-id="65617-116">Select the **Create new LTI Tenant** button.</span></span> <span data-ttu-id="65617-117">Dans la page Inscription LTI, sélectionnez **Canvas** dans la liste et entrez l’URL de base de votre instance de canvas.</span><span class="sxs-lookup"><span data-stu-id="65617-117">On the LTI Registration page select **Canvas** in the dropdown and enter the base URL of your Canvas instance.</span></span>

> [!NOTE]
> <span data-ttu-id="65617-118">Si votre instance de canvas est, par exemple, https://contoso.test.instructure.com ]( https://contoso.test.instructure.com) , l’URL complète doit être entrée.</span><span class="sxs-lookup"><span data-stu-id="65617-118">If your Canvas instance is, for example, https://contoso.test.instructure.com](https://contoso.test.instructure.com), then the complete URL should be entered.</span></span>

:::image type="content" source="media/OneDrive-LTI-07.png" alt-text="Page d’administration du client LTI, avec un champ de liste liste pour choisir la plateforme grand public LTI et un champ de texte d’URL.":::

4. <span data-ttu-id="65617-120">Copiez le JSON en sélectionnant le bouton **Copier** (icône à droite qui affiche deux pages l’une sur l’autre).</span><span class="sxs-lookup"><span data-stu-id="65617-120">Copy the JSON by selecting the **Copy** button (an icon on the right that shows two pages on top of one another).</span></span> <span data-ttu-id="65617-121">Cette clé sera utilisée pour générer la clé dans Canvas.</span><span class="sxs-lookup"><span data-stu-id="65617-121">This will be used to generate the key in Canvas.</span></span>

:::image type="content" source="media/OneDrive-LTI-08.png" alt-text="Image montrant le bouton copier qui copie le texte JSON affiché et le rend disponible pour la génération de touches dans Canvas.":::

5. <span data-ttu-id="65617-123">Connectez-vous à votre instance  de canvas en tant qu’administrateur et sélectionnez Clés de développeur dans le menu sur le côté gauche de la page.</span><span class="sxs-lookup"><span data-stu-id="65617-123">Sign into your Canvas instance as the administrator and select **Developer Keys** from the menu on the left side of the page.</span></span> <span data-ttu-id="65617-124">Dans la dernière page, créez une clé de développeur en choisissant **Clé LTI** dans la partie supérieure droite de la page.</span><span class="sxs-lookup"><span data-stu-id="65617-124">From the dropdown, create a developer key by choosing **LTI Key** from the dropdown on the upper right of the page.</span></span>

:::image type="content" source="media/OneDrive-LTI-14.png" alt-text="Capture d’écran montrant la barre de navigation de gauche avec les clés de développeur sélectionnées, et l’entrée de clé LTI sélectionnée dans une dropdown à droite de la page.":::

6. <span data-ttu-id="65617-126">Dans la page Configurer,  dans la zone de texte Méthode, sélectionnez Coller **JSON** comme méthode et collez le texte JSON que vous avez copié à l’étape 5 dans le champ de texte qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="65617-126">On the Configure page, in the **Method** dropdown, select **Paste JSON** as the method and paste the JSON text you copied in Step 5 in the text field that appears.</span></span>
7. <span data-ttu-id="65617-127">Enregistrez la clé et elle devient disponible dans Canvas dans un **état Off.**</span><span class="sxs-lookup"><span data-stu-id="65617-127">Save the key, and it becomes available in Canvas in an **Off** state.</span></span> <span data-ttu-id="65617-128">Activer la clé **et** copier la clé donnée dans la colonne **Détails** à utiliser à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="65617-128">Turn the key **On** and copy the key given in the **Details** column to be used in the next step.</span></span>

:::image type="content" source="media/OneDrive-LTI-19.png" alt-text="Page Canvas avec la touche définie dans un état « off ». Elle doit être allumée et la clé doit être copiée à partir de la colonne de détails de cette page.":::

8. <span data-ttu-id="65617-130">Revenir au portail Microsoft OneDrive inscription LTI et collez la clé dans le champ **ID client** canvas.</span><span class="sxs-lookup"><span data-stu-id="65617-130">Return to the Microsoft OneDrive LTI Registration portal and paste the key in the **Canvas Client ID** field.</span></span> <span data-ttu-id="65617-131">Sélectionnez **Suivant** lorsque vous êtes prêt.</span><span class="sxs-lookup"><span data-stu-id="65617-131">Select **Next** when you're ready.</span></span>

:::image type="content" source="media/OneDrive-LTI-20.png" alt-text="Page d’inscription du client LTI, qui affiche le texte JSON et la zone de texte dans laquelle la clé doit être copiée.":::

9. <span data-ttu-id="65617-133">Examinez et enregistrez vos modifications.</span><span class="sxs-lookup"><span data-stu-id="65617-133">Review and save your changes.</span></span> <span data-ttu-id="65617-134">Un message s’affiche lors de l’inscription réussie.</span><span class="sxs-lookup"><span data-stu-id="65617-134">A message will be displayed on successful registration.</span></span>
10. <span data-ttu-id="65617-135">Vous pouvez également examiner vos détails d’inscription en sélectionnant le bouton Afficher les locataires **LTI** sur la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="65617-135">Your registration details can also be reviewed by selecting the **View LTI Tenants** button on the home page.</span></span>

## <a name="enable-microsoft-onedrive-lti-in-canvas-courses"></a><span data-ttu-id="65617-136">Activer Microsoft OneDrive LTI dans les cours de canevas</span><span class="sxs-lookup"><span data-stu-id="65617-136">Enable Microsoft OneDrive LTI in Canvas Courses</span></span>

<span data-ttu-id="65617-137">Un administrateur canvas peut activer Microsoft OneDrive LTI pour tous les cours.</span><span class="sxs-lookup"><span data-stu-id="65617-137">A Canvas administrator can enable Microsoft OneDrive LTI for all courses.</span></span> <span data-ttu-id="65617-138">Si Microsoft OneDrive LTI est nécessaire dans un cours spécifique (et pas dans tous les cours), l’enseignant du cours doit suivre les mêmes étapes dans les paramètres du cours.</span><span class="sxs-lookup"><span data-stu-id="65617-138">If Microsoft OneDrive LTI is needed in a specific course (and not all courses), the course educator needs to follow the same steps within the course settings.</span></span>

1. <span data-ttu-id="65617-139">Connectez-vous en tant qu’administrateur et Paramètres **section.**</span><span class="sxs-lookup"><span data-stu-id="65617-139">Sign in as an administrator and go to the **Settings** section.</span></span>
2. <span data-ttu-id="65617-140">Go to the **Apps** section and select the **View App Configurations** button.</span><span class="sxs-lookup"><span data-stu-id="65617-140">Go to the **Apps** section and select the **View App Configurations** button.</span></span>
3. <span data-ttu-id="65617-141">Sélectionnez le **bouton Ajouter une** application.</span><span class="sxs-lookup"><span data-stu-id="65617-141">Select the **Add App** button.</span></span>
4. <span data-ttu-id="65617-142">Dans la **liste finale Type de configuration,** choisissez l’option Par **ID** client.</span><span class="sxs-lookup"><span data-stu-id="65617-142">In the **Configuration Type** dropdown, choose the **By Client ID** option.</span></span>
5. <span data-ttu-id="65617-143">Collez la valeur de la clé de développeur générée précédemment dans le champ **ID client,** puis sélectionnez **le bouton** Envoyer.</span><span class="sxs-lookup"><span data-stu-id="65617-143">Paste the value of the developer key generated previously in the **Client ID** field, and select the **Submit** button.</span></span>

:::image type="content" source="media/OneDrive-LTI-31.png" alt-text="Page Ajouter une application, affichant l’option Par ID client sous le menu déroulant Type de configuration.":::

## <a name="collaboration-settings-for-microsoft-onedrive-lti-in-canvas-courses"></a><span data-ttu-id="65617-145">Collaboration Paramètres for Microsoft OneDrive LTI in Canvas Courses</span><span class="sxs-lookup"><span data-stu-id="65617-145">Collaboration Settings for Microsoft OneDrive LTI in Canvas Courses</span></span>

> [!NOTE]
> <span data-ttu-id="65617-146">Pour que la collaboration fonctionne pour les enseignants et les étudiants, vous ne devez pas activer le paramètre de collaboration.</span><span class="sxs-lookup"><span data-stu-id="65617-146">For collaboration to work for educators and students, you shouldn't enable the collaboration setting.</span></span> <span data-ttu-id="65617-147">Pour vous assurer que le paramètre n’est pas activé, suivez les étapes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="65617-147">To make sure the setting isn't enabled, follow the steps below.</span></span>

1. <span data-ttu-id="65617-148">Connectez-vous en tant qu’administrateur et Paramètres **section.**</span><span class="sxs-lookup"><span data-stu-id="65617-148">Sign in as an admin and go to the **Settings** section.</span></span>
1. <span data-ttu-id="65617-149">Go to **Feature Options** section, and then go to the **Course** section.</span><span class="sxs-lookup"><span data-stu-id="65617-149">Go to **Feature Options** section, and then go to the **Course** section.</span></span>
1. <span data-ttu-id="65617-150">Définissez **la fonctionnalité outil collaborations externes** comme non activée.</span><span class="sxs-lookup"><span data-stu-id="65617-150">Set the **External Collaborations Tool** feature to be not enabled.</span></span>

> [!NOTE]
> <span data-ttu-id="65617-151">La collaboration peut être affectée à des étudiants individuels et à des groupes d’étudiants.</span><span class="sxs-lookup"><span data-stu-id="65617-151">Collaboration can be assigned to individual students and to groups of students.</span></span> <span data-ttu-id="65617-152">L’affectation à des étudiants individuels fonctionne par défaut.</span><span class="sxs-lookup"><span data-stu-id="65617-152">Assigning to individual students works by default.</span></span> <span data-ttu-id="65617-153">Pour être en mesure d’affecter la collaboration à un groupe d’étudiants, suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="65617-153">To be able to assign collaboration to group of students, follow these steps:</span></span>

1. <span data-ttu-id="65617-154">Connectez-vous en tant qu’administrateur et allez à la section **Clés de** développeur.</span><span class="sxs-lookup"><span data-stu-id="65617-154">Login as admin and go to the **Developer Keys** section.</span></span>
1. <span data-ttu-id="65617-155">Recherchez la clé avec la valeur 170000000000710 et définissez-la sur **On**.</span><span class="sxs-lookup"><span data-stu-id="65617-155">Find the key with value 170000000000710 and set it to **On**.</span></span>
