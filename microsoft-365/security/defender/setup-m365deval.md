---
title: Configurer votre laboratoire d'essai ou votre environnement pilote Microsoft 365 Defender
description: Accéder au Centre de sécurité Microsoft 365, puis configurer votre environnement de laboratoire d'essai Microsoft 365 Defender
keywords: Configuration de la version d'évaluation de Microsoft 365 Defender, programme d'installation pilote de Microsoft 365 Defender, essayez Microsoft 365 Defender, programme d'installation du laboratoire d'évaluation Microsoft 365 Defender
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dolmont
author: DulceMontemayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365solution-scenario
- m365solution-evalutatemtp
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: ae81f6be0a83d5d0141f0f0c8c89f8f2207cc56c
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51935424"
---
# <a name="set-up-your-microsoft-365-defender-trial-lab-environment"></a><span data-ttu-id="2158a-104">Configurer votre environnement de laboratoire d'essai Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="2158a-104">Set up your Microsoft 365 Defender trial lab environment</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="2158a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="2158a-105">**Applies to:**</span></span>
- <span data-ttu-id="2158a-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="2158a-106">Microsoft 365 Defender</span></span> 


<span data-ttu-id="2158a-107">La création d'un laboratoire d'évaluation ou d'un environnement pilote Microsoft 365 Defender et son déploiement sont un processus en trois phases :</span><span class="sxs-lookup"><span data-stu-id="2158a-107">Creating a Microsoft 365 Defender trial lab or pilot environment and deploying it is a three-phase process:</span></span>

|<span data-ttu-id="2158a-108">[![Phase 1 : préparation](../../media/phase-diagrams/prepare.png)](prepare-m365d-eval.md)</span><span class="sxs-lookup"><span data-stu-id="2158a-108">[![Phase 1: Prepare](../../media/phase-diagrams/prepare.png)](prepare-m365d-eval.md)</span></span><br/>[<span data-ttu-id="2158a-109">Phase 1 : préparation</span><span class="sxs-lookup"><span data-stu-id="2158a-109">Phase 1: Prepare</span></span>](prepare-m365d-eval.md) |![Phase 2 : configuration](../../media/phase-diagrams/setup.png)<br/><span data-ttu-id="2158a-111">Phase 2 : configuration</span><span class="sxs-lookup"><span data-stu-id="2158a-111">Phase 2: Set up</span></span> |<span data-ttu-id="2158a-112">[![Phase 3 : intégration](../../media/phase-diagrams/onboard.png)](config-m365d-eval.md)</span><span class="sxs-lookup"><span data-stu-id="2158a-112">[![Phase 3: Onboard](../../media/phase-diagrams/onboard.png)](config-m365d-eval.md)</span></span><br/>[<span data-ttu-id="2158a-113">Phase 3 : intégration</span><span class="sxs-lookup"><span data-stu-id="2158a-113">Phase 3: Onboard</span></span>](config-m365d-eval.md) | <span data-ttu-id="2158a-114">[![Retour au pilote](../../media/phase-diagrams/backtopilot.png)](m365d-pilot.md)</span><span class="sxs-lookup"><span data-stu-id="2158a-114">[![Back to pilot](../../media/phase-diagrams/backtopilot.png)](m365d-pilot.md)</span></span><br/>[<span data-ttu-id="2158a-115">Retour au manuel pilote</span><span class="sxs-lookup"><span data-stu-id="2158a-115">Back to pilot playbook</span></span>](m365d-pilot.md) |
|--|--|--|--|
||<span data-ttu-id="2158a-116">*Vous êtes là !*</span><span class="sxs-lookup"><span data-stu-id="2158a-116">*You are here!*</span></span>  | | |


<span data-ttu-id="2158a-117">Vous êtes actuellement en phase de mise en place.</span><span class="sxs-lookup"><span data-stu-id="2158a-117">You're currently in the set up phase.</span></span> <span data-ttu-id="2158a-118">Prenez les étapes initiales pour accéder au Centre de sécurité Microsoft 365, puis configurer votre laboratoire d'évaluation ou votre environnement pilote.</span><span class="sxs-lookup"><span data-stu-id="2158a-118">Take the initial steps to access Microsoft 365 Security Center then set up your trial lab or pilot environment.</span></span>

<span data-ttu-id="2158a-119">Inscrivez-vous à un abonnement Office 365 ou Azure Active Directory pour générer un client *.onmicrosoft.com* que vous pouvez utiliser pour vous inscrire à votre licence Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="2158a-119">Sign up for an Office 365 or Azure Active Directory subscription to generate a *.onmicrosoft.com* tenant that you can use to sign up for your Microsoft 365 E5 license.</span></span> 

>[!NOTE]
><span data-ttu-id="2158a-120">Si vous avez déjà un abonnement Office 365 ou Azure Active Directory, vous pouvez ignorer les étapes de création de la version d'essai ou du client pilote Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="2158a-120">If you already have an existing Office 365 or Azure Active Directory subscription, you can skip the Office 365 E5 trial or pilot tenant creation steps.</span></span>

<span data-ttu-id="2158a-121">Dans cette phase, vous serez guidé vers :</span><span class="sxs-lookup"><span data-stu-id="2158a-121">In this phase, you'll be guided to:</span></span>
- <span data-ttu-id="2158a-122">Créer un client d'essai Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="2158a-122">Create an Office 365 E5 trial tenant</span></span>
- <span data-ttu-id="2158a-123">Activer l'abonnement d'essai Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2158a-123">Enable Microsoft 365 trial subscription</span></span>


## <a name="create-an-office-365-e5-trial-tenant"></a><span data-ttu-id="2158a-124">Créer un client d'essai Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="2158a-124">Create an Office 365 E5 trial tenant</span></span>
>[!NOTE]
><span data-ttu-id="2158a-125">Si vous avez déjà un abonnement Office 365 ou Azure Active Directory, vous pouvez ignorer les étapes de création du client d'essai Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="2158a-125">If you already have an existing Office 365 or Azure Active Directory subscription, you can skip the Office 365 E5 trial tenant creation steps.</span></span>

1. <span data-ttu-id="2158a-126">Go to the [Office 365 E5 product portal](https://www.microsoft.com/microsoft-365/business/office-365-enterprise-e5-business-software?activetab=pivot%3aoverviewtab) and select Free **trial**.</span><span class="sxs-lookup"><span data-stu-id="2158a-126">Go to the [Office 365 E5 product portal](https://www.microsoft.com/microsoft-365/business/office-365-enterprise-e5-business-software?activetab=pivot%3aoverviewtab) and select **Free trial**.</span></span>

   ![Image of_Office page d'essai gratuit 365 E5](../../media/mtp-eval-9.png)
  
2. <span data-ttu-id="2158a-128">Terminez l'inscription de la version d'essai en entrant votre adresse de messagerie (personnelle ou d'entreprise).</span><span class="sxs-lookup"><span data-stu-id="2158a-128">Complete the trial registration by entering your email address (personal or corporate).</span></span> <span data-ttu-id="2158a-129">Cliquez **sur Configurer le compte.**</span><span class="sxs-lookup"><span data-stu-id="2158a-129">Click **Set up account**.</span></span>

   ![Image of_Office page de configuration de l'enregistrement de la version d'essai 365 E5](../../media/mtp-eval-10.png)

3. <span data-ttu-id="2158a-131">Remplissez votre prénom, nom, numéro de téléphone d'entreprise, nom de société, taille de la société et pays ou région.</span><span class="sxs-lookup"><span data-stu-id="2158a-131">Fill in your first name, last name, business phone number, company name, company size, and country or region.</span></span>  

   ![Image of_Office page de configuration de l'enregistrement de la version d'essai 365 E5 demandant le nom, le téléphone et les détails de la société](../../media/mtp-eval-11.png)
   
   > [!NOTE]
   > <span data-ttu-id="2158a-133">Le pays ou la région que vous définissez ici détermine la région de centre de données où votre Office 365 sera hébergé.</span><span class="sxs-lookup"><span data-stu-id="2158a-133">The country or region you set here determines the data center region your Office 365 will be hosted.</span></span>
  
4. <span data-ttu-id="2158a-134">Choisissez votre préférence de vérification : via un SMS ou un appel.</span><span class="sxs-lookup"><span data-stu-id="2158a-134">Choose your verification preference: through a text message or call.</span></span> <span data-ttu-id="2158a-135">Cliquez **sur Envoyer le code de vérification.**</span><span class="sxs-lookup"><span data-stu-id="2158a-135">Click **Send Verification Code**.</span></span> 

   ![Image of_Office page de configuration de l'inscription de la version d'essai 365 E5 demandant les préférences de vérification](../../media/mtp-eval-12.png)

5. <span data-ttu-id="2158a-137">Définissez le nom de domaine personnalisé de votre client, puis cliquez sur **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="2158a-137">Set the custom domain name for your tenant, then click **Next**.</span></span>

   ![Image of_Office page de configuration de l'inscription de la version d'essai 365 E5 dans laquelle vous pouvez configurer votre nom de domaine personnalisé](../../media/mtp-eval-13.png)
 
6. <span data-ttu-id="2158a-139">Configurer la première identité, qui sera un administrateur général pour le client.</span><span class="sxs-lookup"><span data-stu-id="2158a-139">Set up the first identity, which will be a Global Administrator for the tenant.</span></span> <span data-ttu-id="2158a-140">Remplissez le **nom et le** mot de **passe.**</span><span class="sxs-lookup"><span data-stu-id="2158a-140">Fill in **Name** and **Password**.</span></span> <span data-ttu-id="2158a-141">Cliquez sur **Inscription**.</span><span class="sxs-lookup"><span data-stu-id="2158a-141">Click **Sign up**.</span></span>

   ![Image of_Office page de configuration de l'inscription de la version d'essai 365 E5 dans laquelle vous pouvez définir votre identité professionnelle](../../media/mtp-eval-14.png)

7. <span data-ttu-id="2158a-143">Cliquez **sur Aller au programme d'installation** pour terminer la mise en service du client d'essai Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="2158a-143">Click **Go to Setup** to complete the Office 365 E5 trial tenant provisioning.</span></span>

   ![Image de la page de configuration de l'inscription d'essai Office 365 E5 vous invite à cliquer sur le bouton Aller au programme d'installation](../../media/mtp-eval-15.png)

8. <span data-ttu-id="2158a-145">Connectez votre domaine d'entreprise au client Office 365.</span><span class="sxs-lookup"><span data-stu-id="2158a-145">Connect your corporate domain to the Office 365 tenant.</span></span> <span data-ttu-id="2158a-146">[Facultatif] Choisissez **Connecter un domaine que vous possédez déjà** et tapez votre nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="2158a-146">[Optional] Choose **Connect a domain you already own** and type in your domain name.</span></span> <span data-ttu-id="2158a-147">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="2158a-147">Click **Next**.</span></span>

   ![Image of_Office page d'installation 365 E5 dans laquelle vous devez personnaliser votre connectez-vous et votre courrier électronique](../../media/mtp-eval-16.png)
 
9. <span data-ttu-id="2158a-149">Ajoutez un enregistrement TXT ou MX pour valider la propriété du domaine.</span><span class="sxs-lookup"><span data-stu-id="2158a-149">Add a TXT or MX record to validate the domain ownership.</span></span> <span data-ttu-id="2158a-150">Une fois que vous avez ajouté l'enregistrement TXT ou MX à votre domaine, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="2158a-150">Once you’ve added the TXT or MX record to your domain, select **Verify**.</span></span>

   ![Image of_Office page d'installation 365 E5 dans laquelle vous devez ajouter un TXT d'enregistrement MX pour vérifier votre domaine](../../media/mtp-eval-17.png)
 
10. <span data-ttu-id="2158a-152">[Facultatif] Créez d'autres comptes d'utilisateur pour votre client.</span><span class="sxs-lookup"><span data-stu-id="2158a-152">[Optional] Create more user accounts for your tenant.</span></span> <span data-ttu-id="2158a-153">Vous pouvez ignorer cette étape en cliquant sur **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="2158a-153">You can skip this step by clicking **Next**.</span></span>

    ![Image of_Office page d'installation 365 E5 dans laquelle vous pouvez ajouter d'autres utilisateurs](../../media/mtp-eval-18.png)
 
11. <span data-ttu-id="2158a-155">[Facultatif] Téléchargez les applications Office.</span><span class="sxs-lookup"><span data-stu-id="2158a-155">[Optional] Download Office apps.</span></span> <span data-ttu-id="2158a-156">Cliquez **sur Suivant** pour ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="2158a-156">Click **Next** to skip this step.</span></span> 

    ![Image of_Office page 365 E5 où vous pouvez installer vos applications Office](../../media/mtp-eval-19.png)

12. <span data-ttu-id="2158a-158">[Facultatif] Migrer les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="2158a-158">[Optional] Migrate email messages.</span></span> <span data-ttu-id="2158a-159">Là encore, vous pouvez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="2158a-159">Again, you can skip this step.</span></span>

    ![Image of_Office 365 E5 dans laquelle vous pouvez définir s'il faut migrer ou non des messages électroniques](../../media/mtp-eval-20.png)
 
13. <span data-ttu-id="2158a-161">Choisissez des services en ligne.</span><span class="sxs-lookup"><span data-stu-id="2158a-161">Choose online services.</span></span> <span data-ttu-id="2158a-162">Sélectionnez **Exchange,** puis cliquez sur **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="2158a-162">Select **Exchange** and click **Next**.</span></span> 

    ![Image of_Office 365 E5 dans laquelle vous pouvez choisir vos services en ligne](../../media/mtp-eval-21.png)

14. <span data-ttu-id="2158a-164">Ajoutez des enregistrements MX, CNAME et TXT à votre domaine.</span><span class="sxs-lookup"><span data-stu-id="2158a-164">Add MX, CNAME, and TXT records to your domain.</span></span> <span data-ttu-id="2158a-165">Lorsque vous avez terminé, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="2158a-165">When completed, select **Verify**.</span></span>

    ![Image of_Office 365 E5 ici, vous pouvez ajouter vos enregistrements DNS](../../media/mtp-eval-22.png)
 
15. <span data-ttu-id="2158a-167">Félicitations, vous avez terminé la mise en service de votre client Office 365.</span><span class="sxs-lookup"><span data-stu-id="2158a-167">Congratulations, you have completed the provisioning of your Office 365 tenant.</span></span>

    ![Image of_Office page de confirmation de l'achèvement de l'installation 365 E5](../../media/mtp-eval-23.png)

## <a name="enable-microsoft-365-trial-subscription"></a><span data-ttu-id="2158a-169">Activer l'abonnement d'essai Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2158a-169">Enable Microsoft 365 trial subscription</span></span>

>[!NOTE]
><span data-ttu-id="2158a-170">L'inscription à une version d'essai vous donne 25 licences utilisateur à utiliser pendant un mois.</span><span class="sxs-lookup"><span data-stu-id="2158a-170">Signing up for a trial gives you 25 user licenses to use for a month.</span></span> <span data-ttu-id="2158a-171">Pour plus d'informations, voir Essayer ou acheter un abonnement [M365.](../../commerce/try-or-buy-microsoft-365.md)</span><span class="sxs-lookup"><span data-stu-id="2158a-171">See [Try or Buy an M365 subscription](../../commerce/try-or-buy-microsoft-365.md) for details.</span></span>

1. <span data-ttu-id="2158a-172">À [partir du Centre d'administration Microsoft 365,](https://admin.microsoft.com/)cliquez sur **Facturation,** puis accédez à **Acheter des services.**</span><span class="sxs-lookup"><span data-stu-id="2158a-172">From [Microsoft 365 Admin Center](https://admin.microsoft.com/), click **Billing** and then navigate to **Purchase services**.</span></span>

2. <span data-ttu-id="2158a-173">Sélectionnez **Microsoft 365 E5** et cliquez sur **Démarrer la version d'essai gratuite.**</span><span class="sxs-lookup"><span data-stu-id="2158a-173">Select **Microsoft 365 E5** and click **Start free trial**.</span></span> 

   ![Image of_Microsoft page d'essai gratuit de démarrage 365 E5](../../media/mtp-eval-24.png)

3. <span data-ttu-id="2158a-175">Choisissez votre préférence de vérification : via un SMS ou un appel.</span><span class="sxs-lookup"><span data-stu-id="2158a-175">Choose your verification preference: through a text message or call.</span></span> <span data-ttu-id="2158a-176">Une fois que vous avez décidé, entrez le numéro de téléphone, sélectionnez **M'envoyer** un sms ou **m'appeler** en fonction de votre sélection.</span><span class="sxs-lookup"><span data-stu-id="2158a-176">Once you have decided, enter the phone number, select **Text me** or **Call me** depending on your selection.</span></span>

   ![Image of_Microsoft 365 E5 : page d'essai gratuit de démarrage demandant des coordonnées pour envoyer du code pour prouver que vous n'êtes pas un robot](../../media/mtp-eval-25.png)
 
4. <span data-ttu-id="2158a-178">Entrez le code de vérification, puis cliquez **sur Démarrer votre version d'essai gratuite.**</span><span class="sxs-lookup"><span data-stu-id="2158a-178">Enter the verification code and click **Start your free trial**.</span></span>

   ![Image of_Microsoft 365 E5 Page d'essai gratuit de démarrage dans laquelle vous pouvez remplir le code de vérification envoyé par le système pour prouver que vous n'êtes pas un robot](../../media/mtp-eval-26.png)

5. <span data-ttu-id="2158a-180">Cliquez **sur Essayer maintenant** pour confirmer votre version d'essai de Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="2158a-180">Click **Try now** to confirm your Microsoft 365 E5 trial.</span></span>

   ![Image of_Microsoft 365 E5 Démarrage de la page d'essai gratuit où vous devez horloger le bouton Essayer maintenant pour démarrer](../../media/mtp-eval-27.png)
 
6. <span data-ttu-id="2158a-182">Go to the **Microsoft 365 Admin Center**  >  **Users**  >  **Active users**.</span><span class="sxs-lookup"><span data-stu-id="2158a-182">Go to the **Microsoft 365 Admin Center** > **Users** > **Active users**.</span></span> <span data-ttu-id="2158a-183">Sélectionnez votre compte d'utilisateur, sélectionnez Gérer les **licences** de produits, puis remplacez la licence d'Office 365 E5 par **Microsoft 365 E5.**</span><span class="sxs-lookup"><span data-stu-id="2158a-183">Select your user account, select **Manage product licenses**, then swap the license from Office 365 E5 to **Microsoft 365 E5**.</span></span> <span data-ttu-id="2158a-184">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2158a-184">Click **Save**.</span></span>

   ![Image of_Microsoft page du Centre d'administration 365 dans laquelle vous pouvez sélectionner une licence Microsoft 365 E5](../../media/mtp-eval-28.png)
 
7. <span data-ttu-id="2158a-186">Sélectionnez de nouveau le compte d'administrateur général, puis cliquez **sur Gérer le nom d'utilisateur.**</span><span class="sxs-lookup"><span data-stu-id="2158a-186">Select the global administrator account again then click **Manage username**.</span></span>

   ![Image of_Microsoft page du Centre d'administration 365 dans laquelle vous pouvez sélectionner Compte, puis Gérer le nom d'utilisateur](../../media/mtp-eval-29.png)

8. <span data-ttu-id="2158a-188">[Facultatif] Modifiez le domaine de *onmicrosoft.com* à votre propre domaine, en fonction de ce que vous avez choisi lors des étapes précédentes.</span><span class="sxs-lookup"><span data-stu-id="2158a-188">[Optional] Change the domain from *onmicrosoft.com* to your own domain—depending on what you chose on the previous steps.</span></span> <span data-ttu-id="2158a-189">Cliquez sur **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="2158a-189">Click **Save changes**.</span></span>

   ![Image of_Microsoft page du Centre d'administration 365 dans laquelle vous pouvez modifier vos préférences de domaine](../../media/mtp-eval-30.png)



## <a name="next-step"></a><span data-ttu-id="2158a-191">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="2158a-191">Next step</span></span>
|[<span data-ttu-id="2158a-192">Phase 3 : Configurer & intégré</span><span class="sxs-lookup"><span data-stu-id="2158a-192">Phase 3: Configure & Onboard</span></span>](config-m365d-eval.md) | <span data-ttu-id="2158a-193">Configurez chaque pilier Microsoft 365 Defender pour votre laboratoire d'évaluation ou votre environnement pilote Microsoft 365 Defender et intégrer vos points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="2158a-193">Configure each Microsoft 365 Defender pillar for your Microsoft 365 Defender trial lab or pilot environment and onboard your endpoints.</span></span>
|:-------|:-----|
