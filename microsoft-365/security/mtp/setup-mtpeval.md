---
title: Configuration de votre laboratoire d’évaluation Microsoft 365 Defender ou de votre environnement pilote
description: Accédez au centre de sécurité Microsoft 365, puis configurez votre environnement de laboratoire de test Microsoft 365 Defender.
keywords: Programme d’installation de la protection contre les menaces Microsoft, programme d’installation pilote de Microsoft Threat Protection, essayez Microsoft Threat Protection, programme d’évaluation de la protection contre les menaces Microsoft
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: w10
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dolmont
author: DulceMontemayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365solution-scenario
- m365solution-evalutatemtp
ms.topic: article
ms.openlocfilehash: 503b7a6a6b3ad6394293e9f70dbdd336f6bee9dd
ms.sourcegitcommit: ce46d1bd67091d4ed0e2b776dfed55e2d88cdbf4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49131308"
---
# <a name="set-up-your-microsoft-365-defender-trial-lab-environment"></a><span data-ttu-id="937b2-104">Configuration de votre environnement de laboratoire de test Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="937b2-104">Set up your Microsoft 365 Defender trial lab environment</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="937b2-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="937b2-105">**Applies to:**</span></span>
- <span data-ttu-id="937b2-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="937b2-106">Microsoft 365 Defender</span></span> 


<span data-ttu-id="937b2-107">La création d’un laboratoire de test Microsoft 365 Defender ou d’un environnement pilote et son déploiement est un processus en trois phases :</span><span class="sxs-lookup"><span data-stu-id="937b2-107">Creating a Microsoft 365 Defender trial lab or pilot environment and deploying it is a three-phase process:</span></span>

|<span data-ttu-id="937b2-108">[![Phase 1 : préparer](../../media/phase-diagrams/prepare.png)](prepare-mtpeval.md)</span><span class="sxs-lookup"><span data-stu-id="937b2-108">[![Phase 1: Prepare](../../media/phase-diagrams/prepare.png)](prepare-mtpeval.md)</span></span><br/>[<span data-ttu-id="937b2-109">Phase 1 : préparer</span><span class="sxs-lookup"><span data-stu-id="937b2-109">Phase 1: Prepare</span></span>](prepare-mtpeval.md) |![Phase 2 : configurer](../../media/phase-diagrams/setup.png)<br/><span data-ttu-id="937b2-111">Phase 2 : configurer</span><span class="sxs-lookup"><span data-stu-id="937b2-111">Phase 2: Set up</span></span> |<span data-ttu-id="937b2-112">[![Phase 3 : intégration](../../media/phase-diagrams/onboard.png)](config-mtpeval.md)</span><span class="sxs-lookup"><span data-stu-id="937b2-112">[![Phase 3: Onboard](../../media/phase-diagrams/onboard.png)](config-mtpeval.md)</span></span><br/>[<span data-ttu-id="937b2-113">Phase 3 : intégration</span><span class="sxs-lookup"><span data-stu-id="937b2-113">Phase 3: Onboard</span></span>](config-mtpeval.md) | <span data-ttu-id="937b2-114">[![Retour au pilote](../../media/phase-diagrams/backtopilot.png)](mtp-pilot.md)</span><span class="sxs-lookup"><span data-stu-id="937b2-114">[![Back to pilot](../../media/phase-diagrams/backtopilot.png)](mtp-pilot.md)</span></span><br/>[<span data-ttu-id="937b2-115">Retour au manuel pilote</span><span class="sxs-lookup"><span data-stu-id="937b2-115">Back to pilot playbook</span></span>](mtp-pilot.md) |
|--|--|--|--|
||<span data-ttu-id="937b2-116">*Vous êtes là !*</span><span class="sxs-lookup"><span data-stu-id="937b2-116">*You are here!*</span></span>  | | |


<span data-ttu-id="937b2-117">Vous êtes actuellement dans la phase de configuration.</span><span class="sxs-lookup"><span data-stu-id="937b2-117">You're currently in the set up phase.</span></span> <span data-ttu-id="937b2-118">Suivez les étapes initiales pour accéder au centre de sécurité Microsoft 365, puis configurez votre laboratoire d’évaluation ou votre environnement pilote.</span><span class="sxs-lookup"><span data-stu-id="937b2-118">Take the initial steps to access Microsoft 365 Security Center then set up your trial lab or pilot environment.</span></span>

<span data-ttu-id="937b2-119">Inscrivez-vous à un abonnement Office 365 ou Azure Active Directory pour générer un client *. onmicrosoft.com* que vous pouvez utiliser pour vous inscrire à votre licence Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="937b2-119">Sign up for an Office 365 or Azure Active Directory subscription to generate a *.onmicrosoft.com* tenant that you can use to sign up for your Microsoft 365 E5 license.</span></span> 

>[!NOTE]
><span data-ttu-id="937b2-120">Si vous disposez déjà d’un abonnement Office 365 ou Azure Active Directory existant, vous pouvez ignorer les étapes de création d’une version d’évaluation d’Office 365 E5 ou de client pilote.</span><span class="sxs-lookup"><span data-stu-id="937b2-120">If you already have an existing Office 365 or Azure Active Directory subscription, you can skip the Office 365 E5 trial or pilot tenant creation steps.</span></span>

<span data-ttu-id="937b2-121">Dans cette phase, vous serez guidé pour :</span><span class="sxs-lookup"><span data-stu-id="937b2-121">In this phase, you'll be guided to:</span></span>
- <span data-ttu-id="937b2-122">Créer un client d’évaluation Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="937b2-122">Create an Office 365 E5 trial tenant</span></span>
- <span data-ttu-id="937b2-123">Activer l’abonnement à la version d’évaluation de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="937b2-123">Enable Microsoft 365 trial subscription</span></span>


## <a name="create-an-office-365-e5-trial-tenant"></a><span data-ttu-id="937b2-124">Créer un client d’évaluation Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="937b2-124">Create an Office 365 E5 trial tenant</span></span>
>[!NOTE]
><span data-ttu-id="937b2-125">Si vous disposez déjà d’un abonnement Office 365 ou Azure Active Directory existant, vous pouvez ignorer les étapes de création d’un client d’évaluation d’Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="937b2-125">If you already have an existing Office 365 or Azure Active Directory subscription, you can skip the Office 365 E5 trial tenant creation steps.</span></span>

1. <span data-ttu-id="937b2-126">Accédez au [portail produit Office 365 E5](https://www.microsoft.com/microsoft-365/business/office-365-enterprise-e5-business-software?activetab=pivot%3aoverviewtab) et sélectionnez **version d’évaluation gratuite**.</span><span class="sxs-lookup"><span data-stu-id="937b2-126">Go to the [Office 365 E5 product portal](https://www.microsoft.com/microsoft-365/business/office-365-enterprise-e5-business-software?activetab=pivot%3aoverviewtab) and select **Free trial**.</span></span>

   ![Image of_Office 365 E5 page d’évaluation gratuite](../../media/mtp-eval-9.png)
  
2. <span data-ttu-id="937b2-128">Terminez l’enregistrement de la version d’évaluation en saisissant votre adresse de courrier (personnel ou d’entreprise).</span><span class="sxs-lookup"><span data-stu-id="937b2-128">Complete the trial registration by entering your email address (personal or corporate).</span></span> <span data-ttu-id="937b2-129">Cliquez sur **configurer le compte**.</span><span class="sxs-lookup"><span data-stu-id="937b2-129">Click **Set up account**.</span></span>

   ![Image of_Office 365 E5 page de configuration de l’enregistrement de la version d’évaluation](../../media/mtp-eval-10.png)

3. <span data-ttu-id="937b2-131">Renseignez votre prénom, nom, numéro de téléphone professionnel, nom de la société, taille de la société et pays ou région.</span><span class="sxs-lookup"><span data-stu-id="937b2-131">Fill in your first name, last name, business phone number, company name, company size, and country or region.</span></span>  

   ![Image of_Office 365 E5 page de configuration de l’enregistrement de la version d’évaluation demandant des informations sur le nom, le téléphone et la société](../../media/mtp-eval-11.png)
   
   > [!NOTE]
   > <span data-ttu-id="937b2-133">Le pays ou la région que vous définissez ici détermine la région de centre de données que votre Office 365 sera hébergée.</span><span class="sxs-lookup"><span data-stu-id="937b2-133">The country or region you set here determines the data center region your Office 365 will be hosted.</span></span>
  
4. <span data-ttu-id="937b2-134">Choisissez vos préférences de vérification : par le biais d’un message texte ou d’un appel.</span><span class="sxs-lookup"><span data-stu-id="937b2-134">Choose your verification preference: through a text message or call.</span></span> <span data-ttu-id="937b2-135">Cliquez sur **Envoyer un code de vérification**.</span><span class="sxs-lookup"><span data-stu-id="937b2-135">Click **Send Verification Code**.</span></span> 

   ![Image of_Office 365 E5 page de configuration de l’enregistrement de la version d’évaluation demandant une préférence de vérification](../../media/mtp-eval-12.png)

5. <span data-ttu-id="937b2-137">Définissez le nom de domaine personnalisé pour votre client, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="937b2-137">Set the custom domain name for your tenant, then click **Next**.</span></span>

   ![Image of_Office 365 E5 page de configuration de l’enregistrement d’évaluation où vous pouvez configurer votre nom de domaine personnalisé](../../media/mtp-eval-13.png)
 
6. <span data-ttu-id="937b2-139">Configurez la première identité, qui sera un administrateur général pour le client.</span><span class="sxs-lookup"><span data-stu-id="937b2-139">Set up the first identity, which will be a Global Administrator for the tenant.</span></span> <span data-ttu-id="937b2-140">Indiquez le **nom** et le **mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="937b2-140">Fill in **Name** and **Password**.</span></span> <span data-ttu-id="937b2-141">Cliquez sur **Inscription**.</span><span class="sxs-lookup"><span data-stu-id="937b2-141">Click **Sign up**.</span></span>

   ![Image of_Office 365 E5 page de configuration de l’enregistrement d’évaluation où vous pouvez définir l’identité de votre entreprise](../../media/mtp-eval-14.png)

7. <span data-ttu-id="937b2-143">Cliquez sur **accéder au programme d’installation** pour terminer la mise en service du client version d’évaluation d’Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="937b2-143">Click **Go to Setup** to complete the Office 365 E5 trial tenant provisioning.</span></span>

   ![Image de la page de configuration de l’inscription à la version d’évaluation d’Office 365 E5 invitant à cliquer sur le bouton Go Setup](../../media/mtp-eval-15.png)

8. <span data-ttu-id="937b2-145">Connectez votre domaine d’entreprise au client Office 365.</span><span class="sxs-lookup"><span data-stu-id="937b2-145">Connect your corporate domain to the Office 365 tenant.</span></span> <span data-ttu-id="937b2-146">Module Choisissez **connecter un domaine que vous possédez déjà** et tapez votre nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="937b2-146">[Optional] Choose **Connect a domain you already own** and type in your domain name.</span></span> <span data-ttu-id="937b2-147">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="937b2-147">Click **Next**.</span></span>

   ![Image of_Office 365 E5 page de configuration où vous devez personnaliser votre connexion et votre courrier électronique](../../media/mtp-eval-16.png)
 
9. <span data-ttu-id="937b2-149">Ajoutez un enregistrement TXT ou MX pour valider la propriété de domaine.</span><span class="sxs-lookup"><span data-stu-id="937b2-149">Add a TXT or MX record to validate the domain ownership.</span></span> <span data-ttu-id="937b2-150">Une fois que vous avez ajouté l’enregistrement TXT ou MX à votre domaine, sélectionnez **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="937b2-150">Once you’ve added the TXT or MX record to your domain, select **Verify**.</span></span>

   ![Image of_Office 365 E5 page de configuration où vous devez ajouter un fichier TXT de l’enregistrement MX pour vérifier votre domaine](../../media/mtp-eval-17.png)
 
10. <span data-ttu-id="937b2-152">Module Créez des comptes d’utilisateur supplémentaires pour votre client.</span><span class="sxs-lookup"><span data-stu-id="937b2-152">[Optional] Create more user accounts for your tenant.</span></span> <span data-ttu-id="937b2-153">Vous pouvez ignorer cette étape en cliquant sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="937b2-153">You can skip this step by clicking **Next**.</span></span>

    ![Image of_Office 365 E5 page de configuration où vous pouvez ajouter d’autres utilisateurs](../../media/mtp-eval-18.png)
 
11. <span data-ttu-id="937b2-155">Module Téléchargez les applications Office.</span><span class="sxs-lookup"><span data-stu-id="937b2-155">[Optional] Download Office apps.</span></span> <span data-ttu-id="937b2-156">Cliquez sur **suivant** pour ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="937b2-156">Click **Next** to skip this step.</span></span> 

    ![Image of_Office 365 E5 page où vous pouvez installer vos applications Office](../../media/mtp-eval-19.png)

12. <span data-ttu-id="937b2-158">Module Migrez les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="937b2-158">[Optional] Migrate email messages.</span></span> <span data-ttu-id="937b2-159">Encore une fois, vous pouvez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="937b2-159">Again, you can skip this step.</span></span>

    ![Image of_Office 365 E5 où vous pouvez choisir de migrer les messages électroniques ou non](../../media/mtp-eval-20.png)
 
13. <span data-ttu-id="937b2-161">Sélectionnez services en ligne.</span><span class="sxs-lookup"><span data-stu-id="937b2-161">Choose online services.</span></span> <span data-ttu-id="937b2-162">Sélectionnez **Exchange** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="937b2-162">Select **Exchange** and click **Next**.</span></span> 

    ![Image of_Office 365 E5 où vous pouvez choisir vos services en ligne](../../media/mtp-eval-21.png)

14. <span data-ttu-id="937b2-164">Ajoutez des enregistrements MX, CNAMe et TXT à votre domaine.</span><span class="sxs-lookup"><span data-stu-id="937b2-164">Add MX, CNAME, and TXT records to your domain.</span></span> <span data-ttu-id="937b2-165">Lorsque vous avez terminé, sélectionnez **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="937b2-165">When completed, select **Verify**.</span></span>

    ![Image of_Office 365 E5 ici, vous pouvez ajouter vos enregistrements DNS](../../media/mtp-eval-22.png)
 
15. <span data-ttu-id="937b2-167">Félicitations, vous avez terminé la mise en service de votre client Office 365.</span><span class="sxs-lookup"><span data-stu-id="937b2-167">Congratulations, you have completed the provisioning of your Office 365 tenant.</span></span>

    ![Image of_Office 365 E5 page de confirmation de l’exécution du programme d’installation](../../media/mtp-eval-23.png)

## <a name="enable-microsoft-365-trial-subscription"></a><span data-ttu-id="937b2-169">Activer l’abonnement à la version d’évaluation de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="937b2-169">Enable Microsoft 365 trial subscription</span></span>

>[!NOTE]
><span data-ttu-id="937b2-170">L’inscription à une version d’évaluation vous donne 25 licences utilisateur à utiliser pour un mois.</span><span class="sxs-lookup"><span data-stu-id="937b2-170">Signing up for a trial gives you 25 user licenses to use for a month.</span></span> <span data-ttu-id="937b2-171">Pour plus d’informations, voir [essayer ou acheter un abonnement M365](https://docs.microsoft.com/microsoft-365/commerce/try-or-buy-microsoft-365#try-or-buy-a-microsoft-365-subscription-1) .</span><span class="sxs-lookup"><span data-stu-id="937b2-171">See [Try or Buy an M365 subscription](https://docs.microsoft.com/microsoft-365/commerce/try-or-buy-microsoft-365#try-or-buy-a-microsoft-365-subscription-1) for details.</span></span>

1. <span data-ttu-id="937b2-172">Dans le [Centre d’administration Microsoft 365](https://admin.microsoft.com/), cliquez sur **facturation** , puis accédez à **acheter des services**.</span><span class="sxs-lookup"><span data-stu-id="937b2-172">From [Microsoft 365 Admin Center](https://admin.microsoft.com/), click **Billing** and then navigate to **Purchase services**.</span></span>

2. <span data-ttu-id="937b2-173">Sélectionnez **Microsoft 365 E5** , puis cliquez sur **Démarrer la version d’évaluation gratuite**.</span><span class="sxs-lookup"><span data-stu-id="937b2-173">Select **Microsoft 365 E5** and click **Start free trial**.</span></span> 

   ![Image of_Microsoft 365 E5 page d’évaluation gratuite Start](../../media/mtp-eval-24.png)

3. <span data-ttu-id="937b2-175">Choisissez vos préférences de vérification : par le biais d’un message texte ou d’un appel.</span><span class="sxs-lookup"><span data-stu-id="937b2-175">Choose your verification preference: through a text message or call.</span></span> <span data-ttu-id="937b2-176">Une fois que vous avez décidé, entrez le numéro de téléphone, sélectionnez **me texte** ou **appelez-moi** en fonction de votre sélection.</span><span class="sxs-lookup"><span data-stu-id="937b2-176">Once you have decided, enter the phone number, select **Text me** or **Call me** depending on your selection.</span></span>

   ![Image of_Microsoft 365 E5 page d’évaluation gratuite demande de coordonnées pour envoyer du code pour prouver que vous n’êtes pas un robot](../../media/mtp-eval-25.png)
 
4. <span data-ttu-id="937b2-178">Entrez le code de vérification, puis cliquez sur **Démarrer votre version d’évaluation gratuite**.</span><span class="sxs-lookup"><span data-stu-id="937b2-178">Enter the verification code and click **Start your free trial**.</span></span>

   ![Image of_Microsoft 365 E5 page d’évaluation gratuite où vous pouvez renseigner le code de vérification le système envoyé pour prouver que vous n’êtes pas un automate](../../media/mtp-eval-26.png)

5. <span data-ttu-id="937b2-180">Cliquez sur **essayer maintenant** pour confirmer votre version d’évaluation de Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="937b2-180">Click **Try now** to confirm your Microsoft 365 E5 trial.</span></span>

   ![Image of_Microsoft 365 E5 page de la version d’évaluation gratuite où vous devez pointer le bouton essayer maintenant pour démarrer](../../media/mtp-eval-27.png)
 
6. <span data-ttu-id="937b2-182">Accédez au **Centre d’administration Microsoft 365**  >  **utilisateurs**  >  **actifs**.</span><span class="sxs-lookup"><span data-stu-id="937b2-182">Go to the **Microsoft 365 Admin Center** > **Users** > **Active users**.</span></span> <span data-ttu-id="937b2-183">Sélectionnez votre compte d’utilisateur, sélectionnez **gérer les licences de produits**, puis échangez la licence d’Office 365 E5 à **Microsoft 365 E5**.</span><span class="sxs-lookup"><span data-stu-id="937b2-183">Select your user account, select **Manage product licenses**, then swap the license from Office 365 E5 to **Microsoft 365 E5**.</span></span> <span data-ttu-id="937b2-184">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="937b2-184">Click **Save**.</span></span>

   ![Page du centre d’administration de l’image of_Microsoft 365, dans laquelle vous pouvez sélectionner Microsoft 365 E5 licence](../../media/mtp-eval-28.png)
 
7. <span data-ttu-id="937b2-186">Sélectionnez à nouveau le compte d’administrateur général, puis cliquez sur **gérer le nom d’utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="937b2-186">Select the global administrator account again then click **Manage username**.</span></span>

   ![Page du centre d’administration de l’image of_Microsoft 365, dans laquelle vous pouvez sélectionner un compte, puis gérer le nom d’utilisateur](../../media/mtp-eval-29.png)

8. <span data-ttu-id="937b2-188">Module Modifiez le domaine de *onmicrosoft.com* à votre propre domaine, en fonction de ce que vous avez choisi lors des étapes précédentes.</span><span class="sxs-lookup"><span data-stu-id="937b2-188">[Optional] Change the domain from *onmicrosoft.com* to your own domain—depending on what you chose on the previous steps.</span></span> <span data-ttu-id="937b2-189">Cliquez sur **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="937b2-189">Click **Save changes**.</span></span>

   ![Page du centre d’administration de l’image of_Microsoft 365, dans laquelle vous pouvez modifier votre préférence de domaine](../../media/mtp-eval-30.png)



## <a name="next-step"></a><span data-ttu-id="937b2-191">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="937b2-191">Next step</span></span>
|[<span data-ttu-id="937b2-192">Phase 3 : configurer & Onboard</span><span class="sxs-lookup"><span data-stu-id="937b2-192">Phase 3: Configure & Onboard</span></span>](config-mtpeval.md) | <span data-ttu-id="937b2-193">Configurez chaque pilier de Microsoft 365 Defender pour votre laboratoire de test Microsoft 365 Defender ou votre environnement pilote et embarquez vos points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="937b2-193">Configure each Microsoft 365 Defender pillar for your Microsoft 365 Defender trial lab or pilot environment and onboard your endpoints.</span></span>
|:-------|:-----|
