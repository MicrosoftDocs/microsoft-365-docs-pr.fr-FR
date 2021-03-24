---
title: Planification d’une mise à jour de Microsoft Defender pour Endpoint (Linux)
description: Découvrez comment planifier une mise à jour de Microsoft Defender pour Endpoint (Linux) pour mieux protéger les ressources de votre organisation.
keywords: microsoft, defender, atp, linux, analyses, antivirus, microsoft defender pour point de terminaison (linux)
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
ms.openlocfilehash: b4c2e4d80628dab40de9e99abb27237176b9f171
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51062465"
---
# <a name="schedule-an-update-of-the-microsoft-defender-for-endpoint-linux"></a><span data-ttu-id="53400-104">Planifier une mise à jour de Microsoft Defender pour endpoint (Linux)</span><span class="sxs-lookup"><span data-stu-id="53400-104">Schedule an update of the Microsoft Defender for Endpoint (Linux)</span></span>

<span data-ttu-id="53400-105">Pour exécuter une mise à jour sur Microsoft Defender pour endpoint pour Linux, voir Déployer les mises à jour de [Microsoft Defender pour Endpoint pour Linux.](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/linux-updates)</span><span class="sxs-lookup"><span data-stu-id="53400-105">To run an update on Microsoft Defender for Endpoint for Linux, see [Deploy updates for Microsoft Defender for Endpoint for Linux](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/linux-updates).</span></span>

<span data-ttu-id="53400-106">Linux (et Unix) ont un outil appelé **crontab** (semblable au Programmeur des tâches) pour pouvoir exécuter des tâches programmées.</span><span class="sxs-lookup"><span data-stu-id="53400-106">Linux (and Unix) have a tool called **crontab** (similar to Task Scheduler) to be able to run scheduled tasks.</span></span>

## <a name="pre-requisite"></a><span data-ttu-id="53400-107">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="53400-107">Pre-requisite</span></span>

> [!NOTE]
> <span data-ttu-id="53400-108">Pour obtenir la liste de tous les fuseaux horaires, exécutez la commande suivante : `timedatectl list-timezones`</span><span class="sxs-lookup"><span data-stu-id="53400-108">To get a list of all the time zones, run the following command: `timedatectl list-timezones`</span></span><br>
> <span data-ttu-id="53400-109">Exemples pour les fuseaux horaires :</span><span class="sxs-lookup"><span data-stu-id="53400-109">Examples for timezones:</span></span> <br>
> - `America/Los_Angeles`
> - `America/New_York`
> - `America/Chicago`
> - `America/Denver`

## <a name="to-set-the-cron-job"></a><span data-ttu-id="53400-110">Pour définir le travail Cron</span><span class="sxs-lookup"><span data-stu-id="53400-110">To set the Cron job</span></span>
<span data-ttu-id="53400-111">Utilisez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="53400-111">Use the following commands:</span></span>

<span data-ttu-id="53400-112">**Pour sauvegarder les entrées de crontab**</span><span class="sxs-lookup"><span data-stu-id="53400-112">**To backup crontab entries**</span></span>

`sudo crontab -l > /var/tmp/cron_backup_201118.dat`

> [!NOTE]
> <span data-ttu-id="53400-113">Where 201118 == YYMMDD</span><span class="sxs-lookup"><span data-stu-id="53400-113">Where 201118 == YYMMDD</span></span>

> [!TIP]
> <span data-ttu-id="53400-114">Faites-le avant de modifier ou de supprimer.</span><span class="sxs-lookup"><span data-stu-id="53400-114">Do this before you edit or remove.</span></span> <br>

<span data-ttu-id="53400-115">Pour modifier le crontab et ajouter un nouveau travail en tant qu’utilisateur racine :</span><span class="sxs-lookup"><span data-stu-id="53400-115">To edit the crontab, and add a new job as a root user:</span></span> <br>
`sudo crontab -e`

> [!NOTE]
> <span data-ttu-id="53400-116">L’éditeur par défaut est VIM.</span><span class="sxs-lookup"><span data-stu-id="53400-116">The default editor is VIM.</span></span>

<span data-ttu-id="53400-117">Vous pouvez voir :</span><span class="sxs-lookup"><span data-stu-id="53400-117">You might see:</span></span>

<span data-ttu-id="53400-118">0\*\*\*\*/etc/opt/microsoft/mdatp/logrorate.sh</span><span class="sxs-lookup"><span data-stu-id="53400-118">0\*\*\*\*/etc/opt/microsoft/mdatp/logrorate.sh</span></span>

<span data-ttu-id="53400-119">And</span><span class="sxs-lookup"><span data-stu-id="53400-119">And</span></span>

<span data-ttu-id="53400-120">02\*\*sat /bin/mdatp scan quick>~/mdatp_cron_job.log</span><span class="sxs-lookup"><span data-stu-id="53400-120">02\*\*sat /bin/mdatp scan quick>~/mdatp_cron_job.log</span></span>

<span data-ttu-id="53400-121">Voir [Analyses de planification avec Microsoft Defender for Endpoint (Linux)](linux-schedule-scan-atp.md)</span><span class="sxs-lookup"><span data-stu-id="53400-121">See [Schedule scans with Microsoft Defender for Endpoint (Linux)](linux-schedule-scan-atp.md)</span></span>

<span data-ttu-id="53400-122">Appuyez sur « Insérer »</span><span class="sxs-lookup"><span data-stu-id="53400-122">Press “Insert”</span></span>

<span data-ttu-id="53400-123">Ajoutez les entrées suivantes :</span><span class="sxs-lookup"><span data-stu-id="53400-123">Add the following entries:</span></span>

<span data-ttu-id="53400-124">CRON_TZ=Amérique/Los_Angeles</span><span class="sxs-lookup"><span data-stu-id="53400-124">CRON_TZ=America/Los_Angeles</span></span>

> #<a name="rhel-and-variants-centos-and-oracle-linux"></a><span data-ttu-id="53400-125">! RHEL et variantes (CentOS et Oracle Linux)</span><span class="sxs-lookup"><span data-stu-id="53400-125">!RHEL and variants (CentOS and Oracle Linux)</span></span>

`06**sun[$(date +\%d) -le 15] sudo yum update mdatp>>~/mdatp_cron_job.log`

> #<a name="sles-and-variants"></a><span data-ttu-id="53400-126">! SLES et variantes</span><span class="sxs-lookup"><span data-stu-id="53400-126">!SLES and variants</span></span>

`06**sun[$(date +\%d) -le 15] sudo zypper update mdatp>>~/mdatp_cron_job.log`

> #<a name="ubuntu-and-debian-systems"></a><span data-ttu-id="53400-127">! Systèmes Ubuntu et Debian</span><span class="sxs-lookup"><span data-stu-id="53400-127">!Ubuntu and Debian systems</span></span>

`06**sun [$(date +\%d) -le 15] sudo apt-get install --only-upgrade mdatp>>~/mdatp_cron_job.log`

> [!NOTE]
> <span data-ttu-id="53400-128">Dans les exemples ci-dessus, nous la fixons à 00 minutes, 6 heures (heure au format 24 heures), n’importe quel jour du mois, n’importe quel mois, le dimanche. [$(date + d) -le 15] == Ne s’exécute pas, sauf s’il est égal ou inférieur au \% 15e jour (3e semaine).</span><span class="sxs-lookup"><span data-stu-id="53400-128">In the examples above, we are setting it to 00 minutes, 6 a.m.(hour in 24 hour format), any day of the month, any month, on Sundays.[$(date +\%d) -le 15] == Won’t run unless it’s equal or less than the 15th day (3rd week).</span></span> <span data-ttu-id="53400-129">Cela signifie qu’il s’exécutera tous les 3e dimanche (7) du mois à 6 h 00.</span><span class="sxs-lookup"><span data-stu-id="53400-129">Meaning it will run every 3rd Sundays(7) of the month at 6:00 a.m.</span></span> <span data-ttu-id="53400-130">Pacifique (UTC -8).</span><span class="sxs-lookup"><span data-stu-id="53400-130">Pacific (UTC -8).</span></span>

<span data-ttu-id="53400-131">Appuyez sur « Échap »</span><span class="sxs-lookup"><span data-stu-id="53400-131">Press “Esc”</span></span>

<span data-ttu-id="53400-132">Tapez « :wq » avec les guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="53400-132">Type “:wq” w/o the double quotes.</span></span>

> [!NOTE]
> <span data-ttu-id="53400-133">w == write, q == quit</span><span class="sxs-lookup"><span data-stu-id="53400-133">w == write, q == quit</span></span>

<span data-ttu-id="53400-134">Pour afficher vos travaux cron, tapez `sudo crontab -l`</span><span class="sxs-lookup"><span data-stu-id="53400-134">To view your cron jobs, type `sudo crontab -l`</span></span>

:::image type="content" source="images/update-MDE-linux-4634577.jpg" alt-text="mettre à jour MDE linux":::

<span data-ttu-id="53400-136">Pour inspecter les séries de travail de recherche : `sudo grep mdatp /var/log/cron`</span><span class="sxs-lookup"><span data-stu-id="53400-136">To inspect cron job runs: `sudo grep mdatp /var/log/cron`</span></span>

<span data-ttu-id="53400-137">Pour inspecter le fichier mdatp_cron_job.log `sudo nano mdatp_cron_job.log`</span><span class="sxs-lookup"><span data-stu-id="53400-137">To inspect the mdatp_cron_job.log `sudo nano mdatp_cron_job.log`</span></span>

## <a name="for-those-who-use-ansible-chef-or-puppet"></a><span data-ttu-id="53400-138">Pour les personnes qui utilisent Ansible, Chef ou Autres</span><span class="sxs-lookup"><span data-stu-id="53400-138">For those who use Ansible, Chef, or Puppet</span></span>

<span data-ttu-id="53400-139">Utilisez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="53400-139">Use the following commands:</span></span>
### <a name="to-set-cron-jobs-in-ansible"></a><span data-ttu-id="53400-140">Pour définir des travaux de cron dans Ansible</span><span class="sxs-lookup"><span data-stu-id="53400-140">To set cron jobs in Ansible</span></span>

`cron – Manage cron.d and crontab entries`

<span data-ttu-id="53400-141">Pour plus d’informations, voir [https://docs.ansible.com/ansible/latest/modules/cron_module.html](https://docs.ansible.com/ansible/latest/modules/cron_module.html).</span><span class="sxs-lookup"><span data-stu-id="53400-141">See [https://docs.ansible.com/ansible/latest/modules/cron_module.html](https://docs.ansible.com/ansible/latest/modules/cron_module.html) for more information.</span></span>

### <a name="to-set-crontabs-in-chef"></a><span data-ttu-id="53400-142">Pour définir des crontabs dans chef</span><span class="sxs-lookup"><span data-stu-id="53400-142">To set crontabs in Chef</span></span>
`cron resource`

<span data-ttu-id="53400-143">Pour plus d’informations, voir [https://docs.chef.io/resources/cron/](https://docs.chef.io/resources/cron/).</span><span class="sxs-lookup"><span data-stu-id="53400-143">See [https://docs.chef.io/resources/cron/](https://docs.chef.io/resources/cron/) for more information.</span></span>

### <a name="to-set-cron-jobs-in-puppet"></a><span data-ttu-id="53400-144">Pour définir des travaux de cron dans l’ombre</span><span class="sxs-lookup"><span data-stu-id="53400-144">To set cron jobs in Puppet</span></span>
<span data-ttu-id="53400-145">Type de ressource : cron</span><span class="sxs-lookup"><span data-stu-id="53400-145">Resource Type: cron</span></span>

<span data-ttu-id="53400-146">Pour plus d’informations, voir [https://puppet.com/docs/puppet/5.5/types/cron.html](https://puppet.com/docs/puppet/5.5/types/cron.html).</span><span class="sxs-lookup"><span data-stu-id="53400-146">See [https://puppet.com/docs/puppet/5.5/types/cron.html](https://puppet.com/docs/puppet/5.5/types/cron.html) for more information.</span></span>

<span data-ttu-id="53400-147">Automatisation avec l’annexe : tâches Cron et tâches programmées</span><span class="sxs-lookup"><span data-stu-id="53400-147">Automating with Puppet: Cron jobs and scheduled tasks</span></span>

<span data-ttu-id="53400-148">Pour plus d’informations, voir [https://puppet.com/blog/automating-puppet-cron-jobs-and-scheduled-tasks/](https://puppet.com/blog/automating-puppet-cron-jobs-and-scheduled-tasks/).</span><span class="sxs-lookup"><span data-stu-id="53400-148">See [https://puppet.com/blog/automating-puppet-cron-jobs-and-scheduled-tasks/](https://puppet.com/blog/automating-puppet-cron-jobs-and-scheduled-tasks/) for more information.</span></span>

## <a name="additional-information"></a><span data-ttu-id="53400-149">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="53400-149">Additional information</span></span>

<span data-ttu-id="53400-150">**Pour obtenir de l’aide sur crontab**</span><span class="sxs-lookup"><span data-stu-id="53400-150">**To get help with crontab**</span></span>

`man crontab`

<span data-ttu-id="53400-151">**Pour obtenir la liste du fichier crontab de l’utilisateur actuel**</span><span class="sxs-lookup"><span data-stu-id="53400-151">**To get a list of crontab file of the current user**</span></span>

`crontab -l`

<span data-ttu-id="53400-152">**Pour obtenir la liste du fichier crontab d’un autre utilisateur**</span><span class="sxs-lookup"><span data-stu-id="53400-152">**To get a list of crontab file of another user**</span></span>

`crontab -u username -l`

<span data-ttu-id="53400-153">**Pour sauvegarder les entrées de crontab**</span><span class="sxs-lookup"><span data-stu-id="53400-153">**To backup crontab entries**</span></span>

`crontab -l > /var/tmp/cron_backup.dat`

> [!TIP]
> <span data-ttu-id="53400-154">Faites-le avant de modifier ou de supprimer.</span><span class="sxs-lookup"><span data-stu-id="53400-154">Do this before you edit or remove.</span></span> <br>

<span data-ttu-id="53400-155">**Pour restaurer des entrées crontab**</span><span class="sxs-lookup"><span data-stu-id="53400-155">**To restore crontab entries**</span></span>

`crontab /var/tmp/cron_backup.dat`

<span data-ttu-id="53400-156">**Pour modifier le crontab et ajouter un nouveau travail en tant qu’utilisateur racine**</span><span class="sxs-lookup"><span data-stu-id="53400-156">**To edit the crontab and add a new job as a root user**</span></span>

`sudo crontab -e`

<span data-ttu-id="53400-157">**Pour modifier le crontab et ajouter un nouveau travail**</span><span class="sxs-lookup"><span data-stu-id="53400-157">**To edit the crontab and add a new job**</span></span>

`crontab -e`

<span data-ttu-id="53400-158">**Pour modifier les entrées de crontab d’autres utilisateurs**</span><span class="sxs-lookup"><span data-stu-id="53400-158">**To edit other user’s crontab entries**</span></span>

`crontab -u username -e`

<span data-ttu-id="53400-159">**Pour supprimer toutes les entrées crontab**</span><span class="sxs-lookup"><span data-stu-id="53400-159">**To remove all crontab entries**</span></span>

`crontab -r`

<span data-ttu-id="53400-160">**Pour supprimer les entrées de crontab d’autres utilisateurs**</span><span class="sxs-lookup"><span data-stu-id="53400-160">**To remove other user’s crontab entries**</span></span>

`crontab -u username -r`

<span data-ttu-id="53400-161">**Explication**</span><span class="sxs-lookup"><span data-stu-id="53400-161">**Explanation**</span></span>

<pre>
+—————- minute (values: 0 – 59) (special characters: , – * /)  <br>
| +————- hour (values: 0 – 23) (special characters: , – * /) <br>
| | +———- day of month (values: 1 – 31) (special characters: , – * / L W C)  <br>
| | | +——- month (values: 1 – 12) (special characters: ,- * / )  <br>
| | | | +—- day of week (values: 0 – 6) (Sunday=0 or 7) (special characters: , – * / L W C) <br>
| | | | |*****command to be executed
</pre>

