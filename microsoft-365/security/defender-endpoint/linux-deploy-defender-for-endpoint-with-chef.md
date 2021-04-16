---
title: Comment déployer Defender pour endpoint sur Linux avec Chef
description: Découvrez comment déployer Defender pour Endpoint sur Linux avec Chef
keywords: microsoft, defender, atp, linux, analyses, antivirus, microsoft defender pour point de terminaison (linux)
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: v-lsaldanha
author: lovina-saldanha
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 362222e4737b1a8dd6b8a0a284bf3bfb1903c288
ms.sourcegitcommit: 22505ce322f68a2d0ce70d71caf3b0a657fa838a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2021
ms.locfileid: "51861445"
---
# <a name="deploy-defender-for-endpoint-on-linux-with-chef"></a><span data-ttu-id="f3b22-104">Déployer Defender pour endpoint sur Linux avec Chef</span><span class="sxs-lookup"><span data-stu-id="f3b22-104">Deploy Defender for Endpoint on Linux with Chef</span></span>

<span data-ttu-id="f3b22-105">Avant de commencer :</span><span class="sxs-lookup"><span data-stu-id="f3b22-105">Before you begin:</span></span>

- <span data-ttu-id="f3b22-106">Installez unzip s'il n'est pas déjà installé.</span><span class="sxs-lookup"><span data-stu-id="f3b22-106">Install unzip if it’s not already installed.</span></span> <span data-ttu-id="f3b22-107">Les composants Chef sont déjà installés et un référentiel Chef existe (le chef génère un référentiel ) pour stocker le guide de référence qui sera utilisé pour déployer defender pour point de terminaison sur les serveurs Linux gérés par <reponame> Chef.</span><span class="sxs-lookup"><span data-stu-id="f3b22-107">The Chef components are already installed and a Chef repository exists (chef generate repo <reponame>) to store the cookbook that will be used to deploy to Defender for Endpoint on Chef managed Linux servers.</span></span>

<span data-ttu-id="f3b22-108">Vous pouvez créer un nouveau classeur dans votre référentiel existant en exécutant la commande suivante à partir du dossier des classeurs qui se trouve dans votre référentiel de chef :</span><span class="sxs-lookup"><span data-stu-id="f3b22-108">You can create a new cookbook in your existing repository by running the following command from inside the cookbooks folder that is in your chef repository:</span></span></br>
`chef generate cookbook mdatp`

<span data-ttu-id="f3b22-109">Cette commande crée une structure de dossiers pour le nouveau classeur appelé mdatp.</span><span class="sxs-lookup"><span data-stu-id="f3b22-109">This command will create a new folder structure for the new cookbook called mdatp.</span></span>  <span data-ttu-id="f3b22-110">Vous pouvez également utiliser un livre de recettes existant si vous en avez déjà un que vous souhaitez utiliser pour ajouter le déploiement MDE.</span><span class="sxs-lookup"><span data-stu-id="f3b22-110">You can also use an existing cookbook if you already have one you’d like to use to add the MDE deployment into.</span></span>
<span data-ttu-id="f3b22-111">Une fois le classeur créé, créez un dossier de fichiers à l'intérieur du dossier de classeur qui vient d'être créé :</span><span class="sxs-lookup"><span data-stu-id="f3b22-111">After the cookbook is created, create a files folder inside the cookbook folder that just got created:</span></span>

`mkdir mdatp/files`

<span data-ttu-id="f3b22-112">Transférez le fichier zip d'intégration Linux Server qui peut être téléchargé à partir du portail centre de sécurité Microsoft Defender vers ce nouveau dossier de fichiers.</span><span class="sxs-lookup"><span data-stu-id="f3b22-112">Transfer the Linux Server Onboarding zip file that can be downloaded from the Microsoft Defender Security Center portal to this new files folder.</span></span>

<span data-ttu-id="f3b22-113">Sur la station de travail Chef, accédez au dossier mdatp/recipes.</span><span class="sxs-lookup"><span data-stu-id="f3b22-113">On the Chef Workstation, navigate to the mdatp/recipes folder.</span></span> <span data-ttu-id="f3b22-114">Ce dossier est créé lors de la création du classeur.</span><span class="sxs-lookup"><span data-stu-id="f3b22-114">This folder is created when the cookbook was generated.</span></span> <span data-ttu-id="f3b22-115">Utilisez votre éditeur de texte préféré (comme vi ou nano) pour ajouter les instructions suivantes à la fin du fichier default.rb :</span><span class="sxs-lookup"><span data-stu-id="f3b22-115">Use your preferred text editor (like vi or nano) to add the following instructions to the end of the default.rb file:</span></span>
-   <span data-ttu-id="f3b22-116">include_recipe '::onboard_mdatp'</span><span class="sxs-lookup"><span data-stu-id="f3b22-116">include_recipe '::onboard_mdatp'</span></span>
- <span data-ttu-id="f3b22-117">include_recipe '::install_mdatp'</span><span class="sxs-lookup"><span data-stu-id="f3b22-117">include_recipe '::install_mdatp'</span></span>

<span data-ttu-id="f3b22-118">Enregistrez et fermez ensuite le fichier default.rb.</span><span class="sxs-lookup"><span data-stu-id="f3b22-118">Then save and close the default.rb file.</span></span>
<span data-ttu-id="f3b22-119">Créez ensuite un fichier de recette nommé install_mdatp.rb dans le dossier recettes et ajoutez ce texte au fichier :</span><span class="sxs-lookup"><span data-stu-id="f3b22-119">Next create a new recipe file named install_mdatp.rb in the recipes folder and add this text to the file:</span></span>

```powershell

#Add Microsoft Defender   
Repo  
case node['platform_family']
when 'debian'
 apt_repository 'MDAPRepo' do
   arch               'amd64'
   cache_rebuild      true
   cookbook           false
   deb_src            false
   key                'BC528686B50D79E339D3721CEB3E94ADBE1229CF'
   keyserver          "keyserver.ubuntu.com"
   distribution       'focal'
   repo_name          'microsoft-prod'
   components         ['main']
   trusted            true
   uri                "https://packages.microsoft.com/ubuntu/20.04/prod"
 end
 apt_package "mdatp"
when 'rhel'
 yum_repository 'microsoft-prod' do
   baseurl            "https://packages.microsoft.com/rhel/7/prod/"
   description        "Microsoft Defender for Endpoint"
   enabled            true
   gpgcheck           true
   gpgkey             "https://packages.microsoft.com/keys/microsoft.asc"
 end
 if node['platform_version'] <= 8 then
    yum_package "mdatp"
 else
    dnf_package "mdatp"
 end
end
```

<span data-ttu-id="f3b22-120">Vous devez modifier le numéro de version, la distribution et le nom du repo pour qu'il corresponde à la version que vous déployez et au canal que vous souhaitez déployer.</span><span class="sxs-lookup"><span data-stu-id="f3b22-120">You’ll need to modify the version number, distribution, and repo name to match the version you’re deploying to and the channel you’d like to deploy.</span></span>
<span data-ttu-id="f3b22-121">Ensuite, vous devez créer un onboard_mdatp.rb dans le dossier mdatp/recipies.</span><span class="sxs-lookup"><span data-stu-id="f3b22-121">Next you should create an onboard_mdatp.rb file in the mdatp/recipies folder.</span></span>  <span data-ttu-id="f3b22-122">Ajoutez le texte suivant à ce fichier :</span><span class="sxs-lookup"><span data-stu-id="f3b22-122">Add the following text to that file:</span></span>

```powershell

#Create MDATP Directory
mdatp = "/etc/opt/microsoft/mdatp"
zip_path = "/path/to/chef-repo/cookbooks/mdatp/files/WindowsDefenderATPOnboardingPackage.zip"

directory "#{mdatp}" do
  owner 'root'
  group 'root'
  mode 0755
  recursive true
end

#Extract WindowsDefenderATPOnbaordingPackage.zip into /etc/opt/microsoft/mdatp

bash 'Extract Onbaording Json MDATP' do
  code <<-EOS
  unzip #{zip_path} -d #{mdatp}
  EOS
  not_if { ::File.exist?('/etc/opt/microsoft/mdatp/mdatp_onboard.json') }
end
```

<span data-ttu-id="f3b22-123">Veillez à mettre à jour le nom du chemin d'accès à l'emplacement du fichier d'intégration.</span><span class="sxs-lookup"><span data-stu-id="f3b22-123">Make sure to update the path name to the location of the onboarding file.</span></span>
<span data-ttu-id="f3b22-124">Pour tester son déploiement sur la station de travail Chef, exécutez simplement ``sudo chef-client -z -o mdatp`` .</span><span class="sxs-lookup"><span data-stu-id="f3b22-124">To test deploy it on the Chef workstation, just run ``sudo chef-client -z -o mdatp``.</span></span>
<span data-ttu-id="f3b22-125">Après votre déploiement, vous devez envisager de créer et de déployer un fichier de configuration sur les serveurs en fonction des préférences définies pour Microsoft Defender ATP pour Linux - Sécurité  [Windows | Microsoft Docs](/windows/security/threat-protection/microsoft-defender-atp/linux-preferences).</span><span class="sxs-lookup"><span data-stu-id="f3b22-125">After your deployment you should consider creating and deploying a configuration file to the servers based on  [Set preferences for Microsoft Defender ATP for Linux - Windows security | Microsoft Docs](/windows/security/threat-protection/microsoft-defender-atp/linux-preferences).</span></span>  
<span data-ttu-id="f3b22-126">Une fois que vous avez créé et testé votre fichier de configuration, vous pouvez le placer dans le dossier de guide/mdatp/fichiers où vous avez également placé le package d'intégration.</span><span class="sxs-lookup"><span data-stu-id="f3b22-126">After you've created and tested your configuration file, you can place it into the cookbook/mdatp/files folder where you also placed the onboarding package.</span></span>  <span data-ttu-id="f3b22-127">Vous pouvez ensuite créer un fichier settings_mdatp.rb dans le dossier mdatp/recipies et ajouter ce texte :</span><span class="sxs-lookup"><span data-stu-id="f3b22-127">Then you can create a settings_mdatp.rb file in the mdatp/recipies folder and add this text:</span></span>

```powershell
#Copy the configuration file
cookbook_file '/etc/opt/microsoft/mdatp/managed/mdatp_managed.json' do
  source 'mdatp_managed.json'
  owner 'root'
  group 'root'
  mode '0755'
  action :create
end
```

<span data-ttu-id="f3b22-128">Pour inclure cette étape dans la recette, ajoutez simplement include_recipe « :: settings_mdatp » à votre fichier default.rb dans le dossier de la recette.</span><span class="sxs-lookup"><span data-stu-id="f3b22-128">To include this step as part of the recipe just add include_recipe ':: settings_mdatp' to your default.rb file within the recipe folder.</span></span>
<span data-ttu-id="f3b22-129">Vous pouvez également utiliser crontab pour planifier des mises à jour automatiques Planifier une mise à jour de [Microsoft Defender pour Endpoint (Linux).](linux-update-MDE-Linux.md)</span><span class="sxs-lookup"><span data-stu-id="f3b22-129">You can also use crontab to schedule automatic updates [Schedule an update of the Microsoft Defender for Endpoint (Linux)](linux-update-MDE-Linux.md).</span></span>

<span data-ttu-id="f3b22-130">Désinstallez le manuel MDATP :</span><span class="sxs-lookup"><span data-stu-id="f3b22-130">Uninstall MDATP cookbook:</span></span>

```powershell
#Uninstall the Defender package
case node['platform_family']
when 'debian'
 apt_package "mdatp" do
   action :remove
 end
when 'rhel'
 if node['platform_version'] <= 8 
then
    yum_package "mdatp" do
      action :remove
    end
 else
    dnf_package "mdatp" do
      action :remove
    end
 end
end
```

