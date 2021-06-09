---
title: Planifier des analyses avec Microsoft Defender pour Endpoint (Linux)
description: Découvrez comment planifier un temps d’analyse automatique pour Microsoft Defender pour Endpoint (Linux) afin de mieux protéger les ressources de votre organisation.
keywords: microsoft, defender, Microsoft Defender pour le point de terminaison, linux, analyses, antivirus, microsoft defender pour point de terminaison (linux)
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 5a4beaefb2fcc12d46cf61c22644217dce1807a6
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52845365"
---
# <a name="schedule-scans-with-microsoft-defender-for-endpoint-linux"></a><span data-ttu-id="22531-104">Planifier des analyses avec Microsoft Defender pour Endpoint (Linux)</span><span class="sxs-lookup"><span data-stu-id="22531-104">Schedule scans with Microsoft Defender for Endpoint (Linux)</span></span>

<span data-ttu-id="22531-105">Pour exécuter une analyse pour Linux, voir [Commandes pris en charge.](/microsoft-365/security/defender-endpoint/linux-resources#supported-commands)</span><span class="sxs-lookup"><span data-stu-id="22531-105">To run a scan for Linux, see [Supported Commands](/microsoft-365/security/defender-endpoint/linux-resources#supported-commands).</span></span>

<span data-ttu-id="22531-106">Linux (et Unix) ont un outil appelé **crontab** (semblable au Programmeur des tâches) pour pouvoir exécuter des tâches programmées.</span><span class="sxs-lookup"><span data-stu-id="22531-106">Linux (and Unix) have a tool called **crontab** (similar to Task Scheduler) to be able to run scheduled tasks.</span></span>

## <a name="pre-requisite"></a><span data-ttu-id="22531-107">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="22531-107">Pre-requisite</span></span>

> [!NOTE]
> <span data-ttu-id="22531-108">Pour obtenir la liste de tous les fuseaux horaires, exécutez la commande suivante : `timedatectl list-timezones`</span><span class="sxs-lookup"><span data-stu-id="22531-108">To get a list of all the time zones, run the following command: `timedatectl list-timezones`</span></span><br>
> <span data-ttu-id="22531-109">Exemples pour les fuseaux horaires :</span><span class="sxs-lookup"><span data-stu-id="22531-109">Examples for timezones:</span></span>
> - `America/Los_Angeles`
> - `America/New_York`
> - `America/Chicago`
> - `America/Denver`

## <a name="to-set-the-cron-job"></a><span data-ttu-id="22531-110">Pour définir le travail Cron</span><span class="sxs-lookup"><span data-stu-id="22531-110">To set the Cron job</span></span>
<span data-ttu-id="22531-111">Utilisez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="22531-111">Use the following commands:</span></span>

<span data-ttu-id="22531-112">**Pour sauvegarder les entrées de crontab**</span><span class="sxs-lookup"><span data-stu-id="22531-112">**To backup crontab entries**</span></span>

`sudo crontab -l > /var/tmp/cron_backup_200919.dat`

> [!NOTE]
> <span data-ttu-id="22531-113">Where 200919 == YRMMDD</span><span class="sxs-lookup"><span data-stu-id="22531-113">Where 200919 == YRMMDD</span></span>

> [!TIP]
> <span data-ttu-id="22531-114">Faites-le avant de modifier ou de supprimer.</span><span class="sxs-lookup"><span data-stu-id="22531-114">Do this before you edit or remove.</span></span> <br>

<span data-ttu-id="22531-115">Pour modifier le crontab et ajouter un nouveau travail en tant qu’utilisateur racine :</span><span class="sxs-lookup"><span data-stu-id="22531-115">To edit the crontab, and add a new job as a root user:</span></span> <br>
`sudo crontab -e`

> [!NOTE]
> <span data-ttu-id="22531-116">L’éditeur par défaut est VIM.</span><span class="sxs-lookup"><span data-stu-id="22531-116">The default editor is VIM.</span></span>

<span data-ttu-id="22531-117">Vous pouvez voir :</span><span class="sxs-lookup"><span data-stu-id="22531-117">You might see:</span></span>

<span data-ttu-id="22531-118">0 \* \* \* \* /etc/opt/microsoft/mdatp/logrorate.sh</span><span class="sxs-lookup"><span data-stu-id="22531-118">0 \* \* \* \* /etc/opt/microsoft/mdatp/logrorate.sh</span></span>

<span data-ttu-id="22531-119">Appuyez sur « Insérer »</span><span class="sxs-lookup"><span data-stu-id="22531-119">Press “Insert”</span></span>

<span data-ttu-id="22531-120">Ajoutez les entrées suivantes :</span><span class="sxs-lookup"><span data-stu-id="22531-120">Add the following entries:</span></span>

<span data-ttu-id="22531-121">CRON_TZ=Amérique/Los_Angeles</span><span class="sxs-lookup"><span data-stu-id="22531-121">CRON_TZ=America/Los_Angeles</span></span>

<span data-ttu-id="22531-122">0 2 \* \* sat /bin/mdatp scan quick > ~/mdatp_cron_job.log</span><span class="sxs-lookup"><span data-stu-id="22531-122">0 2 \* \* sat /bin/mdatp scan quick > ~/mdatp_cron_job.log</span></span>

> [!NOTE]
><span data-ttu-id="22531-123">Dans cet exemple, nous l’avons définie sur 00 minutes, 2 heures du matin.</span><span class="sxs-lookup"><span data-stu-id="22531-123">In this example, we have  set it to 00 minutes, 2 a.m.</span></span> <span data-ttu-id="22531-124">(heure au format 24 heures), tous les jours du mois, tous les mois, le samedi.</span><span class="sxs-lookup"><span data-stu-id="22531-124">(hour in 24 hour format), any day of the month, any month, on Saturdays.</span></span> <span data-ttu-id="22531-125">Cela signifie qu’il sera exécuté le samedi à 2 h 00.</span><span class="sxs-lookup"><span data-stu-id="22531-125">Meaning it will run Saturdays at 2:00 a.m.</span></span> <span data-ttu-id="22531-126">Pacifique (UTC –8).</span><span class="sxs-lookup"><span data-stu-id="22531-126">Pacific (UTC –8).</span></span>

<span data-ttu-id="22531-127">Appuyez sur « Échap »</span><span class="sxs-lookup"><span data-stu-id="22531-127">Press “Esc”</span></span>

<span data-ttu-id="22531-128">Tapez « :wq » sans guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="22531-128">Type “:wq” without the double quotes.</span></span>

> [!NOTE]
> <span data-ttu-id="22531-129">w == write, q == quit</span><span class="sxs-lookup"><span data-stu-id="22531-129">w == write, q == quit</span></span>

<span data-ttu-id="22531-130">Pour afficher vos travaux cron, tapez `sudo crontab -l`</span><span class="sxs-lookup"><span data-stu-id="22531-130">To view your cron jobs, type `sudo crontab -l`</span></span>

:::image type="content" source="/microsoft-365/security/defender-endpoint/images/linux-mdatp-1" alt-text="linux mdatp":::

<span data-ttu-id="22531-132">**Pour inspecter les séries de travail de cron**</span><span class="sxs-lookup"><span data-stu-id="22531-132">**To inspect cron job runs**</span></span>

`sudo grep mdatp /var/log/cron`

<span data-ttu-id="22531-133">**Pour inspecter le fichier mdatp_cron_job.log**</span><span class="sxs-lookup"><span data-stu-id="22531-133">**To inspect the mdatp_cron_job.log**</span></span>

`sudo nano mdatp_cron_job.log`

## <a name="for-those-who-use-ansible-chef-or-puppet"></a><span data-ttu-id="22531-134">Pour les personnes qui utilisent Ansible, Chef ou Autres</span><span class="sxs-lookup"><span data-stu-id="22531-134">For those who use Ansible, Chef, or Puppet</span></span>

<span data-ttu-id="22531-135">Utilisez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="22531-135">Use the following commands:</span></span>
### <a name="to-set-cron-jobs-in-ansible"></a><span data-ttu-id="22531-136">Pour définir des travaux de cron dans Ansible</span><span class="sxs-lookup"><span data-stu-id="22531-136">To set cron jobs in Ansible</span></span>

`cron – Manage cron.d and crontab entries`

<span data-ttu-id="22531-137">Pour plus d’informations, voir [https://docs.ansible.com/ansible/latest/modules/cron_module.html](https://docs.ansible.com/ansible/latest/modules/cron_module.html).</span><span class="sxs-lookup"><span data-stu-id="22531-137">See [https://docs.ansible.com/ansible/latest/modules/cron_module.html](https://docs.ansible.com/ansible/latest/modules/cron_module.html) for more information.</span></span>

### <a name="to-set-crontabs-in-chef"></a><span data-ttu-id="22531-138">Pour définir des crontabs dans chef</span><span class="sxs-lookup"><span data-stu-id="22531-138">To set crontabs in Chef</span></span>
`cron resource`

<span data-ttu-id="22531-139">Pour plus d’informations, voir [https://docs.chef.io/resources/cron/](https://docs.chef.io/resources/cron/).</span><span class="sxs-lookup"><span data-stu-id="22531-139">See [https://docs.chef.io/resources/cron/](https://docs.chef.io/resources/cron/) for more information.</span></span>

### <a name="to-set-cron-jobs-in-puppet"></a><span data-ttu-id="22531-140">Pour définir des travaux de cron dans l’ombre</span><span class="sxs-lookup"><span data-stu-id="22531-140">To set cron jobs in Puppet</span></span>
<span data-ttu-id="22531-141">Type de ressource : cron</span><span class="sxs-lookup"><span data-stu-id="22531-141">Resource Type: cron</span></span>

<span data-ttu-id="22531-142">Pour plus d’informations, voir [https://puppet.com/docs/puppet/5.5/types/cron.html](https://puppet.com/docs/puppet/5.5/types/cron.html).</span><span class="sxs-lookup"><span data-stu-id="22531-142">See [https://puppet.com/docs/puppet/5.5/types/cron.html](https://puppet.com/docs/puppet/5.5/types/cron.html) for more information.</span></span>

<span data-ttu-id="22531-143">Automatisation avec l’annexe : tâches Cron et tâches programmées</span><span class="sxs-lookup"><span data-stu-id="22531-143">Automating with Puppet: Cron jobs and scheduled tasks</span></span>

<span data-ttu-id="22531-144">Pour plus d’informations, voir [https://puppet.com/blog/automating-puppet-cron-jobs-and-scheduled-tasks/](https://puppet.com/blog/automating-puppet-cron-jobs-and-scheduled-tasks/).</span><span class="sxs-lookup"><span data-stu-id="22531-144">See [https://puppet.com/blog/automating-puppet-cron-jobs-and-scheduled-tasks/](https://puppet.com/blog/automating-puppet-cron-jobs-and-scheduled-tasks/) for more information.</span></span>

## <a name="additional-information"></a><span data-ttu-id="22531-145">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="22531-145">Additional information</span></span>

<span data-ttu-id="22531-146">**Pour obtenir de l’aide sur crontab**</span><span class="sxs-lookup"><span data-stu-id="22531-146">**To get help with crontab**</span></span>

`man crontab`

<span data-ttu-id="22531-147">**Pour obtenir la liste du fichier crontab de l’utilisateur actuel**</span><span class="sxs-lookup"><span data-stu-id="22531-147">**To get a list of crontab file of the current user**</span></span>

`crontab -l`

<span data-ttu-id="22531-148">**Pour obtenir la liste du fichier crontab d’un autre utilisateur**</span><span class="sxs-lookup"><span data-stu-id="22531-148">**To get a list of crontab file of another user**</span></span>

`crontab -u username -l`

<span data-ttu-id="22531-149">**Pour sauvegarder les entrées de crontab**</span><span class="sxs-lookup"><span data-stu-id="22531-149">**To backup crontab entries**</span></span>

`crontab -l > /var/tmp/cron_backup.dat`

> [!TIP]
> <span data-ttu-id="22531-150">Faites-le avant de modifier ou de supprimer.</span><span class="sxs-lookup"><span data-stu-id="22531-150">Do this before you edit or remove.</span></span> <br>

<span data-ttu-id="22531-151">**Pour restaurer des entrées de crontab**</span><span class="sxs-lookup"><span data-stu-id="22531-151">**To restore crontab entries**</span></span>

`crontab /var/tmp/cron_backup.dat`

<span data-ttu-id="22531-152">**Pour modifier le crontab et ajouter un nouveau travail en tant qu’utilisateur racine**</span><span class="sxs-lookup"><span data-stu-id="22531-152">**To edit the crontab and add a new job as a root user**</span></span>

`sudo crontab -e`

<span data-ttu-id="22531-153">**Pour modifier le crontab et ajouter un nouveau travail**</span><span class="sxs-lookup"><span data-stu-id="22531-153">**To edit the crontab and add a new job**</span></span>

`crontab -e`

<span data-ttu-id="22531-154">**Pour modifier les entrées de crontab d’autres utilisateurs**</span><span class="sxs-lookup"><span data-stu-id="22531-154">**To edit other user’s crontab entries**</span></span>

`crontab -u username -e`

<span data-ttu-id="22531-155">**Pour supprimer toutes les entrées crontab**</span><span class="sxs-lookup"><span data-stu-id="22531-155">**To remove all crontab entries**</span></span>

`crontab -r`

<span data-ttu-id="22531-156">**Pour supprimer les entrées de crontab d’autres utilisateurs**</span><span class="sxs-lookup"><span data-stu-id="22531-156">**To remove other user’s crontab entries**</span></span>

`crontab -u username -r`

<span data-ttu-id="22531-157">**Explication**</span><span class="sxs-lookup"><span data-stu-id="22531-157">**Explanation**</span></span>

<span data-ttu-id="22531-158">+—————- minute (valeurs : 0 – 59) (caractères spéciaux : , – \* /)</span><span class="sxs-lookup"><span data-stu-id="22531-158">+—————- minute (values: 0 – 59) (special characters: , – \* /)</span></span>  <br>
<span data-ttu-id="22531-159">| +————- heure (valeurs : 0 – 23) (caractères spéciaux : , – \* /)</span><span class="sxs-lookup"><span data-stu-id="22531-159">| +————- hour (values: 0 – 23) (special characters: , – \* /)</span></span> <br>
<span data-ttu-id="22531-160">| | +———- jour du mois (valeurs : 1 – 31) (caractères spéciaux : , – \* / L W C)</span><span class="sxs-lookup"><span data-stu-id="22531-160">| | +———- day of month (values: 1 – 31) (special characters: , – \* / L W C)</span></span>  <br>
<span data-ttu-id="22531-161">| | | +——- mois (valeurs : 1 – 12) (caractères spéciaux : ,- \* / )</span><span class="sxs-lookup"><span data-stu-id="22531-161">| | | +——- month (values: 1 – 12) (special characters: ,- \* / )</span></span>  <br>
<span data-ttu-id="22531-162">| | | | +— jour de la semaine (valeurs : 0 – 6) (Sunday=0 ou 7) (caractères spéciaux : , – \* / L W C)</span><span class="sxs-lookup"><span data-stu-id="22531-162">| | | | +—- day of week (values: 0 – 6) (Sunday=0 or 7) (special characters: , – \* / L W C)</span></span> <br>
<span data-ttu-id="22531-163">| | | | | commande \*\*\*\*\*\* à exécuter</span><span class="sxs-lookup"><span data-stu-id="22531-163">| | | | |\*\*\*\*\*command to be executed</span></span>


