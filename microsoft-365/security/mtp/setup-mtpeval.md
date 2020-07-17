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
ms.openlocfilehash: 6cba773d0c4bea259db151d5a8f1d8e03954a045
ms.sourcegitcommit: f80c6c52e5b08290f74baec1d64c4070046c32e4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2020
ms.locfileid: "44717294"
---
# <a name="set-up-your-microsoft-threat-protection-trial-lab-environment"></a><span data-ttu-id="9c3e4-104">Configurer votre environnement de laboratoire d’évaluation de la protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="9c3e4-104">Set up your Microsoft Threat Protection trial lab environment</span></span> 

<span data-ttu-id="9c3e4-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9c3e4-105">**Applies to:**</span></span>
- <span data-ttu-id="9c3e4-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="9c3e4-106">Microsoft Threat Protection</span></span> 


<span data-ttu-id="9c3e4-107">La création d’un environnement de laboratoire de test Microsoft Threat Protection et son déploiement est un processus en trois phases :</span><span class="sxs-lookup"><span data-stu-id="9c3e4-107">Creating a Microsoft Threat Protection trial lab environment and deploying it is a three-phase process:</span></span>

<br>
<table border="0" width="100%" align="center">
  <tr style="text-align:center;">
    <td align="center" style="width:25%; border:0;" >
      <a href= "https://docs.microsoft.com/microsoft-365/security/mtp/prepare-mtpeval?view=o365-worldwide"> 
        <img src="../../media/prepare.png" alt="Prepare your Microsoft Threat Protection trial lab environment" title="Préparer votre atelier d’évaluation de la protection contre les menaces Microsoft" />
      <br/><span data-ttu-id="9c3e4-109">Phase 1 : préparer</a></span><span class="sxs-lookup"><span data-stu-id="9c3e4-109">Phase 1: Prepare </a></span></span><br>
    </td>
     <td align="center"bgcolor="#d5f5e3">
      <a href="https://docs.microsoft.com/microsoft-365/security/mtp/setup-mtpeval?view=o365-worldwide">
        <img src="../../media/setup.png" alt="Set up your Microsoft Threat Protection trial lab environment" title="Configurer votre atelier d’évaluation de la protection contre les menaces Microsoft" />
      <br/><span data-ttu-id="9c3e4-111">Phase 2 : configuration</a></span><span class="sxs-lookup"><span data-stu-id="9c3e4-111">Phase 2: Setup </a></span></span><br>
    </td>
    <td align="center">
      <a href="https://docs.microsoft.com/microsoft-365/security/mtp/config-mtpeval?view=o365-worldwide">
        <img src="../../media/config-onboard.png" alt="
Configure each Microsoft Threat Protection pillar for your Microsoft Threat Protection trial lab environment and onboard your endpoints" title="
Configurez chaque pilier de protection contre les menaces Microsoft pour votre environnement de laboratoire d’évaluation de la protection contre les menaces Microsoft et embarquez vos points de terminaison." />
      <br/><span data-ttu-id="9c3e4-113">Phase 3 : configurer & Onboard</a></span><span class="sxs-lookup"><span data-stu-id="9c3e4-113">Phase 3: Configure & Onboard </a></span></span><br>
</td>


  </tr>
</table>

<span data-ttu-id="9c3e4-114">Vous êtes actuellement dans la phase de configuration.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-114">You are currently in the set up phase.</span></span> <span data-ttu-id="9c3e4-115">Suivez les étapes initiales pour accéder au centre de sécurité Microsoft 365, puis configurez votre environnement de laboratoire d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-115">Take the initial steps to access Microsoft 365 Security Center then setup your trial lab environment.</span></span>

<span data-ttu-id="9c3e4-116">Inscrivez-vous à un abonnement Office 365 ou Azure Active Directory pour générer un client *. onmicrosoft.com* que vous pouvez utiliser pour vous inscrire à votre licence Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-116">Sign up for an Office 365 or Azure Active Directory subscription to generate a *.onmicrosoft.com* tenant that you can use to sign up for your Microsoft 365 E5 license.</span></span> 

>[!NOTE]
><span data-ttu-id="9c3e4-117">Si vous disposez déjà d’un abonnement Office 365 ou Azure Active Directory existant, vous pouvez ignorer les étapes de création d’un client d’évaluation d’Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-117">If you already have an existing Office 365 or Azure Active Directory subscription, you can skip the Office 365 E5 trial tenant creation steps.</span></span>

<span data-ttu-id="9c3e4-118">Dans cette phase, vous serez guidé pour :</span><span class="sxs-lookup"><span data-stu-id="9c3e4-118">In this phase, you'll be guided to:</span></span>
- <span data-ttu-id="9c3e4-119">Créer un client d’évaluation Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="9c3e4-119">Create an Office 365 E5 trial tenant</span></span>
- <span data-ttu-id="9c3e4-120">Activer l’abonnement à la version d’évaluation de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9c3e4-120">Enable Microsoft 365 trial subscription</span></span>


## <a name="create-an-office-365-e5-trial-tenant"></a><span data-ttu-id="9c3e4-121">Créer un client d’évaluation Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="9c3e4-121">Create an Office 365 E5 trial tenant</span></span>
>[!NOTE]
><span data-ttu-id="9c3e4-122">Si vous disposez déjà d’un abonnement Office 365 ou Azure Active Directory existant, vous pouvez ignorer les étapes de création d’un client d’évaluation d’Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-122">If you already have an existing Office 365 or Azure Active Directory subscription, you can skip the Office 365 E5 trial tenant creation steps.</span></span>

1. <span data-ttu-id="9c3e4-123">Accédez au [portail produit Office 365 E5](https://www.microsoft.com/microsoft-365/business/office-365-enterprise-e5-business-software?activetab=pivot%3aoverviewtab) et sélectionnez **version d’évaluation gratuite**.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-123">Go to the [Office 365 E5 product portal](https://www.microsoft.com/microsoft-365/business/office-365-enterprise-e5-business-software?activetab=pivot%3aoverviewtab) and select **Free trial**.</span></span>
<span data-ttu-id="9c3e4-124">![Image of_Office 365 E5 page d’évaluation gratuite](../../media/mtp-eval-9.png)</span><span class="sxs-lookup"><span data-stu-id="9c3e4-124">![Image of_Office 365 E5 free trial page](../../media/mtp-eval-9.png)</span></span> <br>
  
2. <span data-ttu-id="9c3e4-125">Terminez l’enregistrement de la version d’évaluation en saisissant votre adresse de courrier (personnel ou d’entreprise).</span><span class="sxs-lookup"><span data-stu-id="9c3e4-125">Complete the trial registration by entering your email address (personal or corporate).</span></span> <span data-ttu-id="9c3e4-126">Cliquez sur **configurer le compte**.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-126">Click **Set up account**.</span></span>
<span data-ttu-id="9c3e4-127">![Image of_Office 365 E5 page de configuration de l’enregistrement de la version d’évaluation](../../media/mtp-eval-10.png)</span><span class="sxs-lookup"><span data-stu-id="9c3e4-127">![Image of_Office 365 E5 trial registration setup page](../../media/mtp-eval-10.png)</span></span> <br> 

3. <span data-ttu-id="9c3e4-128">Indiquez votre prénom, nom, numéro de téléphone professionnel, nom de la société, taille de la société et pays ou région.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-128">Fill in your first name, last name, business phone number, company name, company size and country or region.</span></span>  
<br>![Image of_Office 365 E5 page de configuration de l’enregistrement de la version d’évaluation demandant des informations sur le nom, le téléphone et la société](../../media/mtp-eval-11.png) <br>
>[!NOTE]
><span data-ttu-id="9c3e4-130">Le pays ou la région que vous définissez ici détermine la région de centre de données que votre Office 365 sera hébergée.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-130">The country or region you set here determines the data center region your Office 365 will be hosted.</span></span>
  
4. <span data-ttu-id="9c3e4-131">Choisissez vos préférences de vérification : par le biais d’un message texte ou d’un appel.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-131">Choose your verification preference: through a text message or call.</span></span> <span data-ttu-id="9c3e4-132">Cliquez sur **Envoyer un code de vérification**.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-132">Click **Send Verification Code**.</span></span> 
<span data-ttu-id="9c3e4-133">![Image of_Office 365 E5 page de configuration de l’enregistrement de la version d’évaluation demandant une préférence de vérification](../../media/mtp-eval-12.png)</span><span class="sxs-lookup"><span data-stu-id="9c3e4-133">![Image of_Office 365 E5 trial registration setup page asking for verification preference](../../media/mtp-eval-12.png)</span></span> <br>

5. <span data-ttu-id="9c3e4-134">Définissez le nom de domaine personnalisé pour votre client, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-134">Set the custom domain name for your tenant, then click **Next**.</span></span>
<br><span data-ttu-id="9c3e4-135">![Image of_Office 365 E5 page de configuration de l’enregistrement d’évaluation où vous pouvez configurer votre nom de domaine personnalisé](../../media/mtp-eval-13.png)</span><span class="sxs-lookup"><span data-stu-id="9c3e4-135">![Image of_Office 365 E5 trial registration setup page where you can set up your custom domain name](../../media/mtp-eval-13.png)</span></span> <br>
 
6. <span data-ttu-id="9c3e4-136">Configurez la première identité qui sera un administrateur général pour le client.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-136">Set up the first identity which will be a Global Administrator for the tenant.</span></span> <span data-ttu-id="9c3e4-137">Indiquez le **nom** et le **mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-137">Fill in **Name** and **Password**.</span></span> <span data-ttu-id="9c3e4-138">Cliquez sur **Inscription**.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-138">Click **Sign up**.</span></span>
<span data-ttu-id="9c3e4-139">![Image of_Office 365 E5 page de configuration de l’enregistrement d’évaluation où vous pouvez définir l’identité de votre entreprise](../../media/mtp-eval-14.png)</span><span class="sxs-lookup"><span data-stu-id="9c3e4-139">![Image of_Office 365 E5 trial registration setup page where you can set your business identity](../../media/mtp-eval-14.png)</span></span> <br>

7. <span data-ttu-id="9c3e4-140">Cliquez sur **accéder au programme d’installation** pour terminer la mise en service du client version d’évaluation d’Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-140">Click **Go to Setup** to complete the Office 365 E5 trial tenant provisioning.</span></span>
<br><span data-ttu-id="9c3e4-141">![Image de la page de configuration de l’inscription à la version d’évaluation d’Office 365 E5 invitant à cliquer sur le bouton Go Setup](../../media/mtp-eval-15.png)</span><span class="sxs-lookup"><span data-stu-id="9c3e4-141">![Image of Office 365 E5 trial registration setup page prompting to click Go Setup button](../../media/mtp-eval-15.png)</span></span> <br>

8. <span data-ttu-id="9c3e4-142">Connectez votre domaine d’entreprise au client Office 365.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-142">Connect your corporate domain to the Office 365 tenant.</span></span> <span data-ttu-id="9c3e4-143">Module Choisissez **connecter un domaine que vous possédez déjà** et tapez votre nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-143">[Optional] Choose **Connect a domain you already own** and type in your domain name.</span></span> <span data-ttu-id="9c3e4-144">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-144">Click **Next**.</span></span>
<br><span data-ttu-id="9c3e4-145">![Image of_Office 365 E5 page de configuration où vous devez personnaliser votre connexion et votre courrier électronique](../../media/mtp-eval-16.png)</span><span class="sxs-lookup"><span data-stu-id="9c3e4-145">![Image of_Office 365 E5 Setup page where you should personalize your sign-in and email](../../media/mtp-eval-16.png)</span></span> <br>
 
9. <span data-ttu-id="9c3e4-146">Vous devrez ajouter un enregistrement TXT ou MX pour valider la propriété de domaine.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-146">You will need to add a TXT or MX record to validate the domain ownership.</span></span> <span data-ttu-id="9c3e4-147">Une fois que vous avez ajouté l’enregistrement TXT ou MX à votre domaine, sélectionnez **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-147">Once you’ve added the TXT or MX record to your domain, select **Verify**.</span></span>
<br><span data-ttu-id="9c3e4-148">![Image of_Office 365 E5 page de configuration où vous devez ajouter un fichier TXT de l’enregistrement MX pour vérifier votre domaine](../../media/mtp-eval-17.png)</span><span class="sxs-lookup"><span data-stu-id="9c3e4-148">![Image of_Office 365 E5 setup page where you should add a TXT of MX record to verify your domain](../../media/mtp-eval-17.png)</span></span> <br>
 
10. <span data-ttu-id="9c3e4-149">Module Créez des comptes d’utilisateur supplémentaires pour votre client.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-149">[Optional] Create more user accounts for your tenant.</span></span> <span data-ttu-id="9c3e4-150">Vous pouvez ignorer cette étape en cliquant sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-150">You can skip this step by clicking **Next**.</span></span>
<span data-ttu-id="9c3e4-151">![Image of_Office 365 E5 page de configuration où vous pouvez ajouter d’autres utilisateurs](../../media/mtp-eval-18.png)</span><span class="sxs-lookup"><span data-stu-id="9c3e4-151">![Image of_Office 365 E5 setup page where you can add more users](../../media/mtp-eval-18.png)</span></span> <br>
 
11. <span data-ttu-id="9c3e4-152">Module Téléchargez les applications Office.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-152">[Optional] Download Office apps.</span></span> <span data-ttu-id="9c3e4-153">Cliquez sur **suivant** pour ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-153">Click **Next** to skip this step.</span></span> 
<br><span data-ttu-id="9c3e4-154">![Image of_Office 365 E5 page où vous pouvez installer vos applications Office](../../media/mtp-eval-19.png)</span><span class="sxs-lookup"><span data-stu-id="9c3e4-154">![Image of_Office 365 E5 page where you can install your Office apps](../../media/mtp-eval-19.png)</span></span> <br>

12. <span data-ttu-id="9c3e4-155">Module Migrez les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-155">[Optional] Migrate email messages.</span></span> <span data-ttu-id="9c3e4-156">Encore une fois, vous pouvez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-156">Again, you can skip this step.</span></span>
<br><span data-ttu-id="9c3e4-157">![Image of_Office 365 E5 où vous pouvez choisir de migrer les messages électroniques ou non](../../media/mtp-eval-20.png)</span><span class="sxs-lookup"><span data-stu-id="9c3e4-157">![Image of_Office 365 E5 where you can set whether to migrate email messages or not](../../media/mtp-eval-20.png)</span></span> <br>
 
13. <span data-ttu-id="9c3e4-158">Sélectionnez services en ligne.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-158">Choose online services.</span></span> <span data-ttu-id="9c3e4-159">Sélectionnez **Exchange** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-159">Select **Exchange** and click **Next**.</span></span> 
<br><span data-ttu-id="9c3e4-160">![Image of_Office 365 E5 où vous pouvez choisir vos services en ligne](../../media/mtp-eval-21.png)</span><span class="sxs-lookup"><span data-stu-id="9c3e4-160">![Image of_Office 365 E5 where you can choose your online services](../../media/mtp-eval-21.png)</span></span> <br>

14. <span data-ttu-id="9c3e4-161">Ajoutez des enregistrements MX, CNAMe et TXT à votre domaine.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-161">Add MX, CNAME and TXT records to your domain.</span></span> <span data-ttu-id="9c3e4-162">Lorsque vous avez terminé, sélectionnez **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-162">When completed, select **Verify**.</span></span>
<br><span data-ttu-id="9c3e4-163">![Image of_Office 365 E5 ici, vous pouvez ajouter vos enregistrements DNS](../../media/mtp-eval-22.png)</span><span class="sxs-lookup"><span data-stu-id="9c3e4-163">![Image of_Office 365 E5 here you can add your DNS records](../../media/mtp-eval-22.png)</span></span> <br>
 
15. <span data-ttu-id="9c3e4-164">Félicitations, vous avez terminé la mise en service de votre client Office 365.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-164">Congratulations, you have completed the provisioning of your Office 365 tenant.</span></span>
<br><span data-ttu-id="9c3e4-165">![Image of_Office 365 E5 page de confirmation de l’exécution du programme d’installation](../../media/mtp-eval-23.png)</span><span class="sxs-lookup"><span data-stu-id="9c3e4-165">![Image of_Office 365 E5 setup completion confirmation page](../../media/mtp-eval-23.png)</span></span> <br>

## <a name="enable-microsoft-365-trial-subscription"></a><span data-ttu-id="9c3e4-166">Activer l’abonnement à la version d’évaluation de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9c3e4-166">Enable Microsoft 365 trial subscription</span></span>

>[!NOTE]
><span data-ttu-id="9c3e4-167">L’inscription à une version d’évaluation vous donne 25 licences utilisateur à utiliser pour un mois.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-167">Signing up for a trial gives you 25 user licenses to use for a month.</span></span> <span data-ttu-id="9c3e4-168">Pour plus d’informations, voir [essayer ou acheter un abonnement M365](https://docs.microsoft.com/microsoft-365/commerce/try-or-buy-microsoft-365?view=o365-worldwide#try-or-buy-a-microsoft-365-subscription-1) .</span><span class="sxs-lookup"><span data-stu-id="9c3e4-168">See [Try or Buy an M365 subscription](https://docs.microsoft.com/microsoft-365/commerce/try-or-buy-microsoft-365?view=o365-worldwide#try-or-buy-a-microsoft-365-subscription-1) for details.</span></span>

1. <span data-ttu-id="9c3e4-169">Dans le [Centre d’administration Microsoft 365](https://admin.microsoft.com/), cliquez sur **facturation** , puis accédez à **acheter des services**.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-169">From [Microsoft 365 Admin Center](https://admin.microsoft.com/), click **Billing** and then navigate to **Purchase services**.</span></span>

2. <span data-ttu-id="9c3e4-170">Sélectionnez **Microsoft 365 E5** , puis cliquez sur **Démarrer la version d’évaluation gratuite**.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-170">Select **Microsoft 365 E5** and click **Start free trial**.</span></span> 
<span data-ttu-id="9c3e4-171">![Image of_Microsoft 365 E5 page d’évaluation gratuite Start](../../media/mtp-eval-24.png)</span><span class="sxs-lookup"><span data-stu-id="9c3e4-171">![Image of_Microsoft 365 E5 Start free trial page](../../media/mtp-eval-24.png)</span></span> <br>

3. <span data-ttu-id="9c3e4-172">Choisissez vos préférences de vérification : par le biais d’un message texte ou d’un appel.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-172">Choose your verification preference: through a text message or call.</span></span> <span data-ttu-id="9c3e4-173">Une fois que vous avez décidé, entrez le numéro de téléphone, sélectionnez **me texte** ou **appelez-moi** en fonction de votre sélection.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-173">Once you have decided, enter the phone number, select **Text me** or **Call me** depending on your selection.</span></span>
<span data-ttu-id="9c3e4-174">![Image of_Microsoft 365 E5 page d’évaluation gratuite demande de coordonnées pour envoyer du code pour prouver que vous n’êtes pas un robot](../../media/mtp-eval-25.png)</span><span class="sxs-lookup"><span data-stu-id="9c3e4-174">![Image of_Microsoft 365 E5 Start free trial page asking for contact details to send code to prove you are not a robot](../../media/mtp-eval-25.png)</span></span> <br>
 
4. <span data-ttu-id="9c3e4-175">Entrez le code de vérification, puis cliquez sur **Démarrer votre version d’évaluation gratuite**.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-175">Enter the verification code and click **Start your free trial**.</span></span> 
<br><span data-ttu-id="9c3e4-176">![Image of_Microsoft 365 E5 page d’évaluation gratuite où vous pouvez renseigner le code de vérification le système envoyé pour prouver que vous n’êtes pas un automate](../../media/mtp-eval-26.png)</span><span class="sxs-lookup"><span data-stu-id="9c3e4-176">![Image of_Microsoft 365 E5 Start free trial page where you can fill out verification code the system sent to prove you are not a robot](../../media/mtp-eval-26.png)</span></span> <br>

5. <span data-ttu-id="9c3e4-177">Cliquez sur **essayer maintenant** pour confirmer votre version d’évaluation de Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-177">Click **Try now** to confirm your Microsoft 365 E5 trial.</span></span>
<br><span data-ttu-id="9c3e4-178">![Image of_Microsoft 365 E5 page de la version d’évaluation gratuite où vous devez pointer le bouton essayer maintenant pour démarrer](../../media/mtp-eval-27.png)</span><span class="sxs-lookup"><span data-stu-id="9c3e4-178">![Image of_Microsoft 365 E5 Start free trial page where you should clock the Try now button to start](../../media/mtp-eval-27.png)</span></span> <br>
 
6. <span data-ttu-id="9c3e4-179">Accédez au **Centre d’administration Microsoft 365**  >  **utilisateurs**  >  **actifs**.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-179">Go to the **Microsoft 365 Admin Center** > **Users** > **Active users**.</span></span> <span data-ttu-id="9c3e4-180">Sélectionnez votre compte d’utilisateur, sélectionnez **gérer les licences de produits**, puis échangez la licence d’Office 365 E5 à **Microsoft 365 E5**.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-180">Select your user account, select **Manage product licenses**, then swap the license from Office 365 E5 to **Microsoft 365 E5**.</span></span> <span data-ttu-id="9c3e4-181">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-181">Click **Save**.</span></span>
<span data-ttu-id="9c3e4-182">![Page du centre d’administration de l’image of_Microsoft 365, dans laquelle vous pouvez sélectionner Microsoft 365 E5 licence](../../media/mtp-eval-28.png)</span><span class="sxs-lookup"><span data-stu-id="9c3e4-182">![Image of_Microsoft 365 Admin Center page where you can select Microsoft 365 E5 license](../../media/mtp-eval-28.png)</span></span> <br>
 
7. <span data-ttu-id="9c3e4-183">Sélectionnez à nouveau le compte d’administrateur général, puis cliquez sur **gérer le nom d’utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-183">Select the global administrator account again then click **Manage username**.</span></span>
<br><span data-ttu-id="9c3e4-184">![Page du centre d’administration de l’image of_Microsoft 365, dans laquelle vous pouvez sélectionner un compte, puis gérer le nom d’utilisateur](../../media/mtp-eval-29.png)</span><span class="sxs-lookup"><span data-stu-id="9c3e4-184">![Image of_Microsoft 365 Admin Center page where you can select Account and then Manage username](../../media/mtp-eval-29.png)</span></span> <br>

8. <span data-ttu-id="9c3e4-185">Module Modifiez le domaine de *onmicrosoft.com* à votre propre domaine, en fonction de ce que vous avez choisi lors des étapes précédentes.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-185">[Optional] Change the domain from *onmicrosoft.com* to your own domain—depending on what you chose on the previous steps.</span></span> <span data-ttu-id="9c3e4-186">Cliquez sur **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-186">Click **Save changes**.</span></span>
<br><span data-ttu-id="9c3e4-187">![Page du centre d’administration de l’image of_Microsoft 365, dans laquelle vous pouvez modifier votre préférence de domaine](../../media/mtp-eval-30.png)</span><span class="sxs-lookup"><span data-stu-id="9c3e4-187">![Image of_Microsoft 365 Admin Center page where you can change your domain preference](../../media/mtp-eval-30.png)</span></span> <br>



## <a name="next-step"></a><span data-ttu-id="9c3e4-188">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="9c3e4-188">Next step</span></span>
|||
|:-------|:-----|
|<span data-ttu-id="9c3e4-189">![Phase 3 : configurer & Onboard](../../media/config-onboard.png)</span><span class="sxs-lookup"><span data-stu-id="9c3e4-189">![Phase 3: Configure & Onboard](../../media/config-onboard.png)</span></span> <br>[<span data-ttu-id="9c3e4-190">Phase 3 : configurer & Onboard</span><span class="sxs-lookup"><span data-stu-id="9c3e4-190">Phase 3: Configure & Onboard</span></span>](config-mtpeval.md) | <span data-ttu-id="9c3e4-191">Configurez chaque pilier de protection contre les menaces Microsoft pour votre laboratoire d’évaluation de la protection contre les menaces Microsoft et embarquez vos points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-191">Configure each Microsoft Threat Protection pillar for your Microsoft Threat Protection evaluation lab and onboard your endpoints.</span></span>
