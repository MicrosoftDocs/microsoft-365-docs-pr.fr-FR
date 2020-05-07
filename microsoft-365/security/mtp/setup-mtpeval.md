---
title: Configurer votre environnement de laboratoire d’évaluation de la protection contre les menaces Microsoft
description: Accédez au centre de sécurité Microsoft 365, puis configurez votre environnement de laboratoire d’évaluation de la protection contre les menaces Microsoft.
keywords: Programme d’installation de la protection contre les menaces Microsoft, essayez le programme d’évaluation de Microsoft Threat Protection.
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
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: 50557b0824999f0220af4d12b906b0274db4471e
ms.sourcegitcommit: 5476c2578400894640ae74bfe8e93c3319f685bd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2020
ms.locfileid: "44049614"
---
# <a name="set-up-your-microsoft-threat-protection-trial-lab-environment"></a><span data-ttu-id="9aeef-104">Configurer votre environnement de laboratoire d’évaluation de la protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="9aeef-104">Set up your Microsoft Threat Protection trial lab environment</span></span> 

<span data-ttu-id="9aeef-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9aeef-105">**Applies to:**</span></span>
- <span data-ttu-id="9aeef-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="9aeef-106">Microsoft Threat Protection</span></span> 


<span data-ttu-id="9aeef-107">La création d’un environnement de laboratoire de test Microsoft Threat Protection et son déploiement est un processus en trois phases :</span><span class="sxs-lookup"><span data-stu-id="9aeef-107">Creating a Microsoft Threat Protection trial lab environment and deploying it is a three-phase process:</span></span>

<br>
<table border="0" width="100%" align="center">
  <tr style="text-align:center;">
    <td align="center" style="width:25%; border:0;" >
      <a href= "https://docs.microsoft.com/microsoft-365/security/mtp/prepare-mtpeval?view=o365-worldwide"> 
        <img src="../../media/prepare.png" alt="Prepare your Microsoft Threat Protection trial lab environment" title="Préparer votre atelier d’évaluation de la protection contre les menaces Microsoft" />
      <br/><span data-ttu-id="9aeef-109">Phase 1 : préparer</a></span><span class="sxs-lookup"><span data-stu-id="9aeef-109">Phase 1: Prepare </a></span></span><br>
    </td>
     <td align="center"bgcolor="#d5f5e3">
      <a href="https://docs.microsoft.com/microsoft-365/security/mtp/setup-mtpeval?view=o365-worldwide">
        <img src="../../media/setup.png" alt="Set up your Microsoft Threat Protection trial lab environment" title="Configurer votre atelier d’évaluation de la protection contre les menaces Microsoft" />
      <br/><span data-ttu-id="9aeef-111">Phase 2 : configuration</a></span><span class="sxs-lookup"><span data-stu-id="9aeef-111">Phase 2: Setup </a></span></span><br>
    </td>
    <td align="center">
      <a href="https://docs.microsoft.com/microsoft-365/security/mtp/config-mtpeval?view=o365-worldwide">
        <img src="../../media/config-onboard.png" alt="
Configure each Microsoft Threat Protection pillar for your Microsoft Threat Protection trial lab environment and onboard your endpoints" title="
Configurez chaque pilier de protection contre les menaces Microsoft pour votre environnement de laboratoire d’évaluation de la protection contre les menaces Microsoft et embarquez vos points de terminaison." />
      <br/><span data-ttu-id="9aeef-113">Phase 3 : configurer & Onboard</a></span><span class="sxs-lookup"><span data-stu-id="9aeef-113">Phase 3: Configure & Onboard </a></span></span><br>
</td>


  </tr>
</table>

<span data-ttu-id="9aeef-114">Vous êtes actuellement dans la phase de configuration.</span><span class="sxs-lookup"><span data-stu-id="9aeef-114">You are currently in the set up phase.</span></span> <span data-ttu-id="9aeef-115">Suivez les étapes initiales pour accéder au centre de sécurité Microsoft 365, puis configurez votre environnement de laboratoire d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="9aeef-115">Take the initial steps to access Microsoft 365 Security Center then setup your trial lab environment.</span></span>

<span data-ttu-id="9aeef-116">Inscrivez-vous à un abonnement Office 365 ou Azure Active Directory pour générer un client *. onmicrosoft.com* que vous pouvez utiliser pour vous inscrire à votre licence Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="9aeef-116">Sign up for an Office 365 or Azure Active Directory subscription to generate a *.onmicrosoft.com* tenant that you can use to sign up for your Microsoft 365 E5 license.</span></span> 

>[!NOTE]
><span data-ttu-id="9aeef-117">Si vous disposez déjà d’un abonnement Office 365 ou Azure Active Directory existant, vous pouvez ignorer les étapes de création d’un client d’évaluation d’Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="9aeef-117">If you already have an existing Office 365 or Azure Active Directory subscription, you can skip the Office 365 E5 trial tenant creation steps.</span></span>

<span data-ttu-id="9aeef-118">Dans cette phase, vous serez guidé pour :</span><span class="sxs-lookup"><span data-stu-id="9aeef-118">In this phase, you'll be guided to:</span></span>
- <span data-ttu-id="9aeef-119">Créer un client d’évaluation Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="9aeef-119">Create an Office 365 E5 trial tenant</span></span>
- <span data-ttu-id="9aeef-120">Activer l’abonnement à la version d’évaluation de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9aeef-120">Enable Microsoft 365 trial subscription</span></span>


## <a name="create-an-office-365-e5-trial-tenant"></a><span data-ttu-id="9aeef-121">Créer un client d’évaluation Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="9aeef-121">Create an Office 365 E5 trial tenant</span></span>
>[!NOTE]
><span data-ttu-id="9aeef-122">Si vous disposez déjà d’un abonnement Office 365 ou Azure Active Directory existant, vous pouvez ignorer les étapes de création d’un client d’évaluation d’Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="9aeef-122">If you already have an existing Office 365 or Azure Active Directory subscription, you can skip the Office 365 E5 trial tenant creation steps.</span></span>

1. <span data-ttu-id="9aeef-123">Accédez au [portail produit Office 365 E5](https://www.microsoft.com/microsoft-365/business/office-365-enterprise-e5-business-software?activetab=pivot%3aoverviewtab) et sélectionnez **version d’évaluation gratuite**.</span><span class="sxs-lookup"><span data-stu-id="9aeef-123">Go to the [Office 365 E5 product portal](https://www.microsoft.com/microsoft-365/business/office-365-enterprise-e5-business-software?activetab=pivot%3aoverviewtab) and select **Free trial**.</span></span>
<span data-ttu-id="9aeef-124">![Image of_page](../../media/mtp-eval-9.png)</span><span class="sxs-lookup"><span data-stu-id="9aeef-124">![Image of_page](../../media/mtp-eval-9.png)</span></span> <br>
  
2. <span data-ttu-id="9aeef-125">Terminez l’enregistrement de la version d’évaluation en saisissant votre adresse de courrier (personnel ou d’entreprise).</span><span class="sxs-lookup"><span data-stu-id="9aeef-125">Complete the trial registration by entering your email address (personal or corporate).</span></span> <span data-ttu-id="9aeef-126">Cliquez sur **configurer le compte**.</span><span class="sxs-lookup"><span data-stu-id="9aeef-126">Click **Set up account**.</span></span>
<span data-ttu-id="9aeef-127">![Image of_page](../../media/mtp-eval-10.png)</span><span class="sxs-lookup"><span data-stu-id="9aeef-127">![Image of_page](../../media/mtp-eval-10.png)</span></span> <br> 

3. <span data-ttu-id="9aeef-128">Indiquez votre prénom, nom, numéro de téléphone professionnel, nom de la société, taille de la société et pays ou région.</span><span class="sxs-lookup"><span data-stu-id="9aeef-128">Fill in your first name, last name, business phone number, company name, company size and country or region.</span></span>  
<br>![Image of_page](../../media/mtp-eval-11.png) <br>
>[!NOTE]
><span data-ttu-id="9aeef-130">Le pays ou la région que vous définissez ici détermine la région de centre de données que votre Office 365 sera hébergée.</span><span class="sxs-lookup"><span data-stu-id="9aeef-130">The country or region you set here determines the data center region your Office 365 will be hosted.</span></span>
  
4. <span data-ttu-id="9aeef-131">Choisissez vos préférences de vérification : par le biais d’un message texte ou d’un appel.</span><span class="sxs-lookup"><span data-stu-id="9aeef-131">Choose your verification preference: through a text message or call.</span></span> <span data-ttu-id="9aeef-132">Cliquez sur **Envoyer un code de vérification**.</span><span class="sxs-lookup"><span data-stu-id="9aeef-132">Click **Send Verification Code**.</span></span> 
<span data-ttu-id="9aeef-133">![Image of_page](../../media/mtp-eval-12.png)</span><span class="sxs-lookup"><span data-stu-id="9aeef-133">![Image of_page](../../media/mtp-eval-12.png)</span></span> <br>

5. <span data-ttu-id="9aeef-134">Définissez le nom de domaine personnalisé pour votre client, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="9aeef-134">Set the custom domain name for your tenant, then click **Next**.</span></span>
<br><span data-ttu-id="9aeef-135">![Image of_page](../../media/mtp-eval-13.png)</span><span class="sxs-lookup"><span data-stu-id="9aeef-135">![Image of_page](../../media/mtp-eval-13.png)</span></span> <br>
 
6. <span data-ttu-id="9aeef-136">Configurez la première identité qui sera un administrateur général pour le client.</span><span class="sxs-lookup"><span data-stu-id="9aeef-136">Set up the first identity which will be a Global Administrator for the tenant.</span></span> <span data-ttu-id="9aeef-137">Indiquez le **nom** et le **mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="9aeef-137">Fill in **Name** and **Password**.</span></span> <span data-ttu-id="9aeef-138">Cliquez sur **Inscription**.</span><span class="sxs-lookup"><span data-stu-id="9aeef-138">Click **Sign up**.</span></span>
<span data-ttu-id="9aeef-139">![Image of_page](../../media/mtp-eval-14.png)</span><span class="sxs-lookup"><span data-stu-id="9aeef-139">![Image of_page](../../media/mtp-eval-14.png)</span></span> <br>
<span data-ttu-id="9aeef-140">c</span><span class="sxs-lookup"><span data-stu-id="9aeef-140">c</span></span>
7. <span data-ttu-id="9aeef-141">Cliquez sur **accéder au programme d’installation** pour terminer la mise en service du client version d’évaluation d’Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="9aeef-141">Click **Go to Setup** to complete the Office 365 E5 trial tenant provisioning.</span></span>
<br><span data-ttu-id="9aeef-142">![Image of_page](../../media/mtp-eval-15.png)</span><span class="sxs-lookup"><span data-stu-id="9aeef-142">![Image of_page](../../media/mtp-eval-15.png)</span></span> <br>

8. <span data-ttu-id="9aeef-143">Connectez votre domaine d’entreprise au client Office 365.</span><span class="sxs-lookup"><span data-stu-id="9aeef-143">Connect your corporate domain to the Office 365 tenant.</span></span> <span data-ttu-id="9aeef-144">Module Choisissez **connecter un domaine que vous possédez déjà** et tapez votre nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="9aeef-144">[Optional] Choose **Connect a domain you already own** and type in your domain name.</span></span> <span data-ttu-id="9aeef-145">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="9aeef-145">Click **Next**.</span></span>
<br><span data-ttu-id="9aeef-146">![Image of_page](../../media/mtp-eval-16.png)</span><span class="sxs-lookup"><span data-stu-id="9aeef-146">![Image of_page](../../media/mtp-eval-16.png)</span></span> <br>
 
9. <span data-ttu-id="9aeef-147">Vous devrez ajouter un enregistrement TXT ou MX pour valider la propriété de domaine.</span><span class="sxs-lookup"><span data-stu-id="9aeef-147">You will need to add a TXT or MX record to validate the domain ownership.</span></span> <span data-ttu-id="9aeef-148">Une fois que vous avez ajouté l’enregistrement TXT ou MX à votre domaine, sélectionnez **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="9aeef-148">Once you’ve added the TXT or MX record to your domain, select **Verify**.</span></span>
<br><span data-ttu-id="9aeef-149">![Image of_page](../../media/mtp-eval-17.png)</span><span class="sxs-lookup"><span data-stu-id="9aeef-149">![Image of_page](../../media/mtp-eval-17.png)</span></span> <br>
 
10. <span data-ttu-id="9aeef-150">Module Créez des comptes d’utilisateur supplémentaires pour votre client.</span><span class="sxs-lookup"><span data-stu-id="9aeef-150">[Optional] Create more user accounts for your tenant.</span></span> <span data-ttu-id="9aeef-151">Vous pouvez ignorer cette étape en cliquant sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="9aeef-151">You can skip this step by clicking **Next**.</span></span>
<span data-ttu-id="9aeef-152">![Image of_page](../../media/mtp-eval-18.png)</span><span class="sxs-lookup"><span data-stu-id="9aeef-152">![Image of_page](../../media/mtp-eval-18.png)</span></span> <br>
 
11. <span data-ttu-id="9aeef-153">Module Téléchargez les applications Office.</span><span class="sxs-lookup"><span data-stu-id="9aeef-153">[Optional] Download Office apps.</span></span> <span data-ttu-id="9aeef-154">Cliquez sur **suivant** pour ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="9aeef-154">Click **Next** to skip this step.</span></span> 
<br><span data-ttu-id="9aeef-155">![Image of_page](../../media/mtp-eval-19.png)</span><span class="sxs-lookup"><span data-stu-id="9aeef-155">![Image of_page](../../media/mtp-eval-19.png)</span></span> <br>

12. <span data-ttu-id="9aeef-156">Module Migrez les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="9aeef-156">[Optional] Migrate email messages.</span></span> <span data-ttu-id="9aeef-157">Encore une fois, vous pouvez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="9aeef-157">Again, you can skip this step.</span></span>
<br><span data-ttu-id="9aeef-158">![Image of_page](../../media/mtp-eval-20.png)</span><span class="sxs-lookup"><span data-stu-id="9aeef-158">![Image of_page](../../media/mtp-eval-20.png)</span></span> <br>
 
13. <span data-ttu-id="9aeef-159">Sélectionnez services en ligne.</span><span class="sxs-lookup"><span data-stu-id="9aeef-159">Choose online services.</span></span> <span data-ttu-id="9aeef-160">Sélectionnez **Exchange** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="9aeef-160">Select **Exchange** and click **Next**.</span></span> 
<br><span data-ttu-id="9aeef-161">![Image of_page](../../media/mtp-eval-21.png)</span><span class="sxs-lookup"><span data-stu-id="9aeef-161">![Image of_page](../../media/mtp-eval-21.png)</span></span> <br>

14. <span data-ttu-id="9aeef-162">Ajoutez des enregistrements MX, CNAMe et TXT à votre domaine.</span><span class="sxs-lookup"><span data-stu-id="9aeef-162">Add MX, CNAME and TXT records to your domain.</span></span> <span data-ttu-id="9aeef-163">Lorsque vous avez terminé, sélectionnez **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="9aeef-163">When completed, select **Verify**.</span></span>
<br><span data-ttu-id="9aeef-164">![Image of_page](../../media/mtp-eval-22.png)</span><span class="sxs-lookup"><span data-stu-id="9aeef-164">![Image of_page](../../media/mtp-eval-22.png)</span></span> <br>
 
15. <span data-ttu-id="9aeef-165">Félicitations, vous avez terminé la mise en service de votre client Office 365.</span><span class="sxs-lookup"><span data-stu-id="9aeef-165">Congratulations, you have completed the provisioning of your Office 365 tenant.</span></span>
<br><span data-ttu-id="9aeef-166">![Image of_page](../../media/mtp-eval-23.png)</span><span class="sxs-lookup"><span data-stu-id="9aeef-166">![Image of_page](../../media/mtp-eval-23.png)</span></span> <br>

## <a name="enable-microsoft-365-trial-subscription"></a><span data-ttu-id="9aeef-167">Activer l’abonnement à la version d’évaluation de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9aeef-167">Enable Microsoft 365 trial subscription</span></span>

>[!NOTE]
><span data-ttu-id="9aeef-168">L’inscription à une version d’évaluation vous donne 25 licences utilisateur à utiliser pour un mois.</span><span class="sxs-lookup"><span data-stu-id="9aeef-168">Signing up for a trial gives you 25 user licenses to use for a month.</span></span> <span data-ttu-id="9aeef-169">Pour plus d’informations, voir [essayer ou acheter un abonnement M365](https://docs.microsoft.com/microsoft-365/commerce/try-or-buy-microsoft-365?view=o365-worldwide#try-or-buy-a-microsoft-365-subscription-1) .</span><span class="sxs-lookup"><span data-stu-id="9aeef-169">See [Try or Buy an M365 subscription](https://docs.microsoft.com/microsoft-365/commerce/try-or-buy-microsoft-365?view=o365-worldwide#try-or-buy-a-microsoft-365-subscription-1) for details.</span></span>

1. <span data-ttu-id="9aeef-170">Dans le [Centre d’administration Microsoft 365](https://admin.microsoft.com/), cliquez sur **facturation** , puis accédez à **acheter des services**.</span><span class="sxs-lookup"><span data-stu-id="9aeef-170">From [Microsoft 365 Admin Center](https://admin.microsoft.com/), click **Billing** and then navigate to **Purchase services**.</span></span>

2. <span data-ttu-id="9aeef-171">Sélectionnez **Microsoft 365 E5** , puis cliquez sur **Démarrer la version d’évaluation gratuite**.</span><span class="sxs-lookup"><span data-stu-id="9aeef-171">Select **Microsoft 365 E5** and click **Start free trial**.</span></span> 
<span data-ttu-id="9aeef-172">![Image of_page](../../media/mtp-eval-24.png)</span><span class="sxs-lookup"><span data-stu-id="9aeef-172">![Image of_page](../../media/mtp-eval-24.png)</span></span> <br>

3. <span data-ttu-id="9aeef-173">Choisissez vos préférences de vérification : par le biais d’un message texte ou d’un appel.</span><span class="sxs-lookup"><span data-stu-id="9aeef-173">Choose your verification preference: through a text message or call.</span></span> <span data-ttu-id="9aeef-174">Une fois que vous avez décidé, entrez le numéro de téléphone, sélectionnez **me texte** ou **appelez-moi** en fonction de votre sélection.</span><span class="sxs-lookup"><span data-stu-id="9aeef-174">Once you have decided, enter the phone number, select **Text me** or **Call me** depending on your selection.</span></span>
<span data-ttu-id="9aeef-175">![Image of_page](../../media/mtp-eval-25.png)</span><span class="sxs-lookup"><span data-stu-id="9aeef-175">![Image of_page](../../media/mtp-eval-25.png)</span></span> <br>
 
4. <span data-ttu-id="9aeef-176">Entrez le code de vérification, puis cliquez sur **Démarrer votre version d’évaluation gratuite**.</span><span class="sxs-lookup"><span data-stu-id="9aeef-176">Enter the verification code and click **Start your free trial**.</span></span> 
<br><span data-ttu-id="9aeef-177">![Image of_page](../../media/mtp-eval-26.png)</span><span class="sxs-lookup"><span data-stu-id="9aeef-177">![Image of_page](../../media/mtp-eval-26.png)</span></span> <br>

5. <span data-ttu-id="9aeef-178">Cliquez sur **essayer maintenant** pour confirmer votre version d’évaluation de Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="9aeef-178">Click **Try now** to confirm your Microsoft 365 E5 trial.</span></span>
<br><span data-ttu-id="9aeef-179">![Image of_page](../../media/mtp-eval-27.png)</span><span class="sxs-lookup"><span data-stu-id="9aeef-179">![Image of_page](../../media/mtp-eval-27.png)</span></span> <br>
 
6. <span data-ttu-id="9aeef-180"> > Accédez au **Centre** > **Users**d’administration Microsoft 365 utilisateurs**actifs**.</span><span class="sxs-lookup"><span data-stu-id="9aeef-180">Go to the **Microsoft 365 Admin Center** > **Users** > **Active users**.</span></span> <span data-ttu-id="9aeef-181">Sélectionnez votre compte d’utilisateur, sélectionnez **gérer les licences de produits**, puis échangez la licence d’Office 365 E5 à **Microsoft 365 E5**.</span><span class="sxs-lookup"><span data-stu-id="9aeef-181">Select your user account, select **Manage product licenses**, then swap the license from Office 365 E5 to **Microsoft 365 E5**.</span></span> <span data-ttu-id="9aeef-182">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="9aeef-182">Click **Save**.</span></span>
<span data-ttu-id="9aeef-183">![Image of_page](../../media/mtp-eval-28.png)</span><span class="sxs-lookup"><span data-stu-id="9aeef-183">![Image of_page](../../media/mtp-eval-28.png)</span></span> <br>
 
7. <span data-ttu-id="9aeef-184">Sélectionnez à nouveau le compte d’administrateur général, puis cliquez sur **gérer le nom d’utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="9aeef-184">Select the global administrator account again then click **Manage username**.</span></span>
<br><span data-ttu-id="9aeef-185">![Image of_page](../../media/mtp-eval-29.png)</span><span class="sxs-lookup"><span data-stu-id="9aeef-185">![Image of_page](../../media/mtp-eval-29.png)</span></span> <br>

8. <span data-ttu-id="9aeef-186">Module Modifiez le domaine de *onmicrosoft.com* à votre propre domaine, en fonction de ce que vous avez choisi lors des étapes précédentes.</span><span class="sxs-lookup"><span data-stu-id="9aeef-186">[Optional] Change the domain from *onmicrosoft.com* to your own domain—depending on what you chose on the previous steps.</span></span> <span data-ttu-id="9aeef-187">Cliquez sur **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="9aeef-187">Click **Save changes**.</span></span>
<br><span data-ttu-id="9aeef-188">![Image of_page](../../media/mtp-eval-30.png)</span><span class="sxs-lookup"><span data-stu-id="9aeef-188">![Image of_page](../../media/mtp-eval-30.png)</span></span> <br>



## <a name="next-step"></a><span data-ttu-id="9aeef-189">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="9aeef-189">Next step</span></span>
<span data-ttu-id="9aeef-190">||| | :-------| :-----| config-Onboard. png)</span><span class="sxs-lookup"><span data-stu-id="9aeef-190">||| |:-------|:-----|config-onboard.png)</span></span> <br><span data-ttu-id="9aeef-191">[Phase 3 : configurer & Onboard](config-mtpeval.md) | Configurez chaque pilier de protection contre les menaces Microsoft pour votre environnement de laboratoire de test Microsoft Threat Protection et intégrez vos points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="9aeef-191">[Phase 3: Configure & Onboard](config-mtpeval.md) | Configure each Microsoft Threat Protection pillar for your Microsoft Threat Protection trial lab environment and onboard your endpoints.</span></span>
