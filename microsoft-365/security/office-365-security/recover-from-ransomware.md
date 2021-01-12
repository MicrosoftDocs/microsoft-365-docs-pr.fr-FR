---
title: Récupérer après une attaque par rançongiciel
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.article: how-to
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
description: Les administrateurs Microsoft 365 peuvent apprendre à récupérer d’une attaque par ransomware.
ms.openlocfilehash: 753171578dc7b76aefadf4b8587e84320d98b912
ms.sourcegitcommit: 9833f95ab6ab95aea20d68a277246dca2223f93d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/11/2021
ms.locfileid: "49794447"
---
# <a name="recover-from-a-ransomware-attack-in-microsoft-365"></a><span data-ttu-id="2891b-103">Récupérer d’une attaque par ransomware dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2891b-103">Recover from a ransomware attack in Microsoft 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="2891b-104">Même si vous prenez toutes les précautions nécessaires pour protéger votre organisation, vous pouvez toujours être la victime d’une attaque par [ransomware.](https://docs.microsoft.com/windows/security/threat-protection/intelligence/ransomware-malware)</span><span class="sxs-lookup"><span data-stu-id="2891b-104">Even if you take every precaution to protect your organization, you can still fall victim to a [ransomware](https://docs.microsoft.com/windows/security/threat-protection/intelligence/ransomware-malware) attack.</span></span> <span data-ttu-id="2891b-105">Les ransomware sont une grande entreprise et les attaques sont très sophistiquées.</span><span class="sxs-lookup"><span data-stu-id="2891b-105">Ransomware is big business, and the attacks are very sophisticated.</span></span>

<span data-ttu-id="2891b-106">Les étapes de cet article vous offrent la meilleure opportunité de récupérer des données et d’arrêter la propagation interne de l’infection.</span><span class="sxs-lookup"><span data-stu-id="2891b-106">The steps in this article will give you the best chance to recover data and stop the internal spread of infection.</span></span> <span data-ttu-id="2891b-107">Avant de commencer, prenez en compte les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="2891b-107">Before you get started, consider the following items:</span></span>

- <span data-ttu-id="2891b-108">Il n’existe aucune garantie que le paiement de la rançon retourne l’accès à vos fichiers.</span><span class="sxs-lookup"><span data-stu-id="2891b-108">There's no guarantee that paying the ransom will return access to your files.</span></span> <span data-ttu-id="2891b-109">En fait, le paiement de la rançon peut faire de vous une cible pour d’autres ransomware.</span><span class="sxs-lookup"><span data-stu-id="2891b-109">In fact, paying the ransom can make you a target for more ransomware.</span></span>

  <span data-ttu-id="2891b-110">Si vous avez déjà payé, mais que vous avez récupéré sans utiliser la solution de l’attaquant, contactez votre banque pour voir si elle peut bloquer la transaction.</span><span class="sxs-lookup"><span data-stu-id="2891b-110">If you already paid, but you recovered without using the attacker's solution, contact your bank to see if they can block the transaction.</span></span>

  <span data-ttu-id="2891b-111">Nous vous recommandons également de signaler l’attaque par ransomware aux forces de l’ordre, aux sites web de signalement des fraudes et à Microsoft, comme décrit plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="2891b-111">We also recommend that you report the ransomware attack to law enforcement, scam reporting websites, and Microsoft as described later in this article.</span></span>

- <span data-ttu-id="2891b-112">Il est important que vous répondiez rapidement à l’attaque et à ses conséquences.</span><span class="sxs-lookup"><span data-stu-id="2891b-112">It's important for you respond quickly to the attack and its consequences.</span></span> <span data-ttu-id="2891b-113">Plus vous patientez longtemps, moins il est probable que vous récupériez les données affectées.</span><span class="sxs-lookup"><span data-stu-id="2891b-113">The longer you wait, the less likely it is that you can recover the affected data.</span></span>

## <a name="step-1-verify-your-backups"></a><span data-ttu-id="2891b-114">Étape 1 : Vérifier vos sauvegardes</span><span class="sxs-lookup"><span data-stu-id="2891b-114">Step 1: Verify your backups</span></span>

<span data-ttu-id="2891b-115">Si vous avez des sauvegardes hors connexion,  vous pouvez probablement restaurer les données chiffrées après avoir supprimé la charge utile de ransomware (programmes malveillants) de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="2891b-115">If you have offline backups, you can probably restore the encrypted data **after** you've removed the ransomware payload (malware) from your environment.</span></span>

<span data-ttu-id="2891b-116">Si vous n’avez pas de sauvegardes ou si vos sauvegardes ont également été affectées par le ransomware, vous pouvez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="2891b-116">If you don't have backups, or if your backups were also affected by the ransomware, you can skip this step.</span></span>

## <a name="step-2-disable-exchange-activesync-and-onedrive-sync"></a><span data-ttu-id="2891b-117">Étape 2 : Désactiver la synchronisation Exchange ActiveSync et OneDrive</span><span class="sxs-lookup"><span data-stu-id="2891b-117">Step 2: Disable Exchange ActiveSync and OneDrive sync</span></span>

<span data-ttu-id="2891b-118">Le point clé ici est d’arrêter la propagation du chiffrement des données par le ransomware.</span><span class="sxs-lookup"><span data-stu-id="2891b-118">The key point here is to stop the spread of data encryption by the ransomware.</span></span>

<span data-ttu-id="2891b-119">Si vous pensez que le courrier électronique est une cible du chiffrement de ransomware, désactivez temporairement l’accès des utilisateurs aux boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="2891b-119">If you suspect email as a target of the ransomware encryption, temporarily disable user access to mailboxes.</span></span> <span data-ttu-id="2891b-120">Exchange ActiveSync synchronise les données entre les appareils et les boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="2891b-120">Exchange ActiveSync synchronizes data between devices and Exchange Online mailboxes.</span></span>

<span data-ttu-id="2891b-121">Pour désactiver la Exchange ActiveSync d’une boîte aux lettres, consultez la Exchange ActiveSync pour les [utilisateurs dans Exchange Online.](https://support.microsoft.com/help/2795303)</span><span class="sxs-lookup"><span data-stu-id="2891b-121">To disable Exchange ActiveSync for a mailbox, see [How to disable Exchange ActiveSync for users in Exchange Online](https://support.microsoft.com/help/2795303).</span></span>

<span data-ttu-id="2891b-122">Pour désactiver d’autres types d’accès à une boîte aux lettres, voir :</span><span class="sxs-lookup"><span data-stu-id="2891b-122">To disable other types of access to a mailbox, see:</span></span>

- <span data-ttu-id="2891b-123">[Activez ou désactivez MAPI pour une boîte aux lettres.](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-user-mailboxes/enable-or-disable-mapi)</span><span class="sxs-lookup"><span data-stu-id="2891b-123">[Enable or disable MAPI for a mailbox](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-user-mailboxes/enable-or-disable-mapi).</span></span>

- [<span data-ttu-id="2891b-124">Activer ou désactiver l’accès POP3 ou IMAP4 pour un utilisateur</span><span class="sxs-lookup"><span data-stu-id="2891b-124">Enable or Disable POP3 or IMAP4 access for a user</span></span>](https://docs.microsoft.com/Exchange/clients-and-mobile-in-exchange-online/pop3-and-imap4/enable-or-disable-pop3-or-imap4-access)

<span data-ttu-id="2891b-125">L’interruption de la synchronisation OneDrive permet de protéger vos données cloud contre la mise à jour par des appareils potentiellement infectés.</span><span class="sxs-lookup"><span data-stu-id="2891b-125">Pausing OneDrive sync will help protect your cloud data from being updated by potentially infected devices.</span></span> <span data-ttu-id="2891b-126">Pour plus d’informations, [voir Comment suspendre et reprendre la synchronisation dans OneDrive](https://support.microsoft.com/office/2152bfa4-a2a5-4d3a-ace8-92912fb4421e).</span><span class="sxs-lookup"><span data-stu-id="2891b-126">For more information, see [How to Pause and Resume sync in OneDrive](https://support.microsoft.com/office/2152bfa4-a2a5-4d3a-ace8-92912fb4421e).</span></span>

## <a name="step-3-remove-the-malware-from-the-affected-devices"></a><span data-ttu-id="2891b-127">Étape 3 : Supprimer les programmes malveillants des appareils concernés</span><span class="sxs-lookup"><span data-stu-id="2891b-127">Step 3: Remove the malware from the affected devices</span></span>

<span data-ttu-id="2891b-128">Exécutez une analyse antivirus complète et actuelle sur tous les ordinateurs et appareils suspectés de détecter et de supprimer la charge utile associée au ransomware.</span><span class="sxs-lookup"><span data-stu-id="2891b-128">Run a full, current antivirus scan on all suspected computers and devices to detect and remove the payload that's associated with the ransomware.</span></span>

<span data-ttu-id="2891b-129">N’oubliez pas d’analyser les appareils qui synchronisent des données ou les cibles des lecteurs réseau mappés.</span><span class="sxs-lookup"><span data-stu-id="2891b-129">Don't forget to scan devices that are synchronizing data, or the targets of mapped network drives.</span></span>

<span data-ttu-id="2891b-130">Vous pouvez utiliser [Windows Defender](https://www.microsoft.com/windows/comprehensive-security) ou (pour les clients [plus anciens) Microsoft Security Essentials](https://www.microsoft.com/download/details.aspx?id=5201).</span><span class="sxs-lookup"><span data-stu-id="2891b-130">You can use [Windows Defender](https://www.microsoft.com/windows/comprehensive-security) or (for older clients) [Microsoft Security Essentials](https://www.microsoft.com/download/details.aspx?id=5201).</span></span>

<span data-ttu-id="2891b-131">Une alternative qui vous aidera également à supprimer des ransomware ou des programmes malveillants est l’outil de suppression de logiciels malveillants [(MSRT).](https://www.microsoft.com/download/details.aspx?id=9905)</span><span class="sxs-lookup"><span data-stu-id="2891b-131">An alternative that will also help you remove ransomware or malware is the [Malicious Software Removal Tool (MSRT)](https://www.microsoft.com/download/details.aspx?id=9905).</span></span>

<span data-ttu-id="2891b-132">Si ces options ne fonctionnent pas, vous pouvez essayer Windows Defender [hors](https://support.microsoft.com/help/17466) connexion ou résoudre les problèmes liés à la détection et à la suppression [de programmes malveillants.](https://support.microsoft.com/help/4466982)</span><span class="sxs-lookup"><span data-stu-id="2891b-132">If these options don't work, you can try [Windows Defender Offline](https://support.microsoft.com/help/17466) or [Troubleshoot problems with detecting and removing malware](https://support.microsoft.com/help/4466982).</span></span>

## <a name="step-4-recover-files-on-a-cleaned-computer-or-device"></a><span data-ttu-id="2891b-133">Étape 4 : Récupérer des fichiers sur un ordinateur ou un appareil nettoyé</span><span class="sxs-lookup"><span data-stu-id="2891b-133">Step 4: Recover files on a cleaned computer or device</span></span>

<span data-ttu-id="2891b-134">Une fois que vous avez terminé l’étape précédente pour supprimer la charge utile de ransomware de [](https://support.microsoft.com/help/17128) votre environnement (ce qui empêchera le ransomware de chiffrer ou de supprimer vos fichiers), vous pouvez utiliser l’historique des fichiers dans Windows 10 et Windows 8.1 ou la Protection système dans Windows 7 pour tenter de récupérer vos fichiers et dossiers locaux.</span><span class="sxs-lookup"><span data-stu-id="2891b-134">After you've completed the previous step to remove the ransomware payload from your environment (which will prevent the ransomware from encrypting or removing your files), you can use [File History](https://support.microsoft.com/help/17128) in Windows 10 and Windows 8.1 or System Protection in Windows 7 to attempt to recover your local files and folders.</span></span>

<span data-ttu-id="2891b-135">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="2891b-135">**Notes**:</span></span>

- <span data-ttu-id="2891b-136">Certains ransomware chiffrent ou suppriment également les versions de sauvegarde, vous ne pouvez donc pas utiliser l’historique des fichiers ou la Protection système pour restaurer des fichiers.</span><span class="sxs-lookup"><span data-stu-id="2891b-136">Some ransomware will also encrypt or delete the backup versions, so you can't use File History or System Protection to restore files.</span></span> <span data-ttu-id="2891b-137">Si cela se produit, vous devez utiliser des sauvegardes sur des lecteurs externes ou des appareils qui n’ont pas été affectés par le ransomware ou OneDrive, comme décrit dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="2891b-137">If that happens, you need use backups on external drives or devices that were not affected by the ransomware or OneDrive as described in the next section.</span></span>

- <span data-ttu-id="2891b-138">Si un dossier est synchronisé avec OneDrive et que vous n’utilisez pas la dernière version de Windows, l’utilisation de l’historique des fichiers peut être limitée.</span><span class="sxs-lookup"><span data-stu-id="2891b-138">If a folder is synchronized to OneDrive and you aren't using the latest version of Windows, there might be some limitations using File History.</span></span>

## <a name="step-5-recover-your-files-in-your-onedrive-for-business"></a><span data-ttu-id="2891b-139">Étape 5 : Récupérer vos fichiers dans votre OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="2891b-139">Step 5: Recover your files in your OneDrive for Business</span></span>

<span data-ttu-id="2891b-140">La restauration de fichiers dans OneDrive Entreprise vous permet de restaurer l’intégralité de votre OneDrive à un point antérieur dans le temps au cours des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="2891b-140">Files Restore in OneDrive for Business allows you to restore your entire OneDrive to a previous point in time within the last 30 days.</span></span> <span data-ttu-id="2891b-141">Pour plus d’informations, [voir Restaurer votre OneDrive.](https://support.microsoft.com/office/fa231298-759d-41cf-bcd0-25ac53eb8a15)</span><span class="sxs-lookup"><span data-stu-id="2891b-141">For more information, see [Restore your OneDrive](https://support.microsoft.com/office/fa231298-759d-41cf-bcd0-25ac53eb8a15).</span></span>

## <a name="step-6-recover-deleted-email"></a><span data-ttu-id="2891b-142">Étape 6 : Récupérer les messages supprimés</span><span class="sxs-lookup"><span data-stu-id="2891b-142">Step 6: Recover deleted email</span></span>

<span data-ttu-id="2891b-143">Dans les rares cas où le ransomware a supprimé tous vos messages électroniques, vous pouvez probablement récupérer les éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="2891b-143">In the rare case that the ransomware deleted all your email, you can probably recover the deleted items.</span></span> <span data-ttu-id="2891b-144">Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="2891b-144">For more information, see:</span></span>

- [<span data-ttu-id="2891b-145">Récupérer des messages supprimés dans la boîte aux lettres d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="2891b-145">Recover deleted messages in a user's mailbox</span></span>](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-user-mailboxes/recover-deleted-messages)

- [<span data-ttu-id="2891b-146">Récupérer des éléments supprimés dans Outlook pour Windows</span><span class="sxs-lookup"><span data-stu-id="2891b-146">Recover deleted items in Outlook for Windows</span></span>](https://support.microsoft.com/office/49e81f3c-c8f4-4426-a0b9-c0fd751d48ce)

## <a name="step-7-re-enable-exchange-activesync-and-onedrive-sync"></a><span data-ttu-id="2891b-147">Étape 7 : Ré-activer la synchronisation Exchange ActiveSync et OneDrive</span><span class="sxs-lookup"><span data-stu-id="2891b-147">Step 7: Re-enable Exchange ActiveSync and OneDrive sync</span></span>

<span data-ttu-id="2891b-148">Après avoir nettoyé vos ordinateurs et appareils et récupéré vos données, vous pouvez réactiver la synchronisation Exchange ActiveSync et OneDrive que vous avez précédemment désactivée à [l’étape 2.](#step-2-disable-exchange-activesync-and-onedrive-sync)</span><span class="sxs-lookup"><span data-stu-id="2891b-148">After you've cleaned your computers and devices and recovered your data, you can re-enable Exchange ActiveSync and OneDrive sync that you previously disabled in [Step 2](#step-2-disable-exchange-activesync-and-onedrive-sync).</span></span>

## <a name="step-8-optional-block-onedrive-sync-for-specific-file-extensions"></a><span data-ttu-id="2891b-149">Étape 8 (facultative) : bloquer la synchronisation OneDrive pour des extensions de fichier spécifiques</span><span class="sxs-lookup"><span data-stu-id="2891b-149">Step 8 (Optional): Block OneDrive sync for specific file extensions</span></span>

<span data-ttu-id="2891b-150">Une fois que vous avez récupéré, vous pouvez empêcher les clients OneDrive Entreprise de synchroniser les types de fichiers affectés par ce ransomware.</span><span class="sxs-lookup"><span data-stu-id="2891b-150">After you've recovered, you can prevent OneDrive for Business clients from synchronizing the file types that were affected by this ransomware.</span></span> <span data-ttu-id="2891b-151">Pour plus d’informations, [voir Set-SPOTenantSyncClientRestriction](https://docs.microsoft.com/powershell/module/sharepoint-online/set-spotenantsyncclientrestriction)</span><span class="sxs-lookup"><span data-stu-id="2891b-151">For more information, see [Set-SPOTenantSyncClientRestriction](https://docs.microsoft.com/powershell/module/sharepoint-online/set-spotenantsyncclientrestriction)</span></span>

## <a name="report-the-attack"></a><span data-ttu-id="2891b-152">Signaler l’attaque</span><span class="sxs-lookup"><span data-stu-id="2891b-152">Report the attack</span></span>

### <a name="contact-law-enforcement"></a><span data-ttu-id="2891b-153">Contacter l’application de la loi</span><span class="sxs-lookup"><span data-stu-id="2891b-153">Contact law enforcement</span></span>

<span data-ttu-id="2891b-154">Vous devez contacter vos autorités judiciaires locales ou fédérales.</span><span class="sxs-lookup"><span data-stu-id="2891b-154">You should contact your local or federal law enforcement agencies.</span></span> <span data-ttu-id="2891b-155">Par exemple, si vous êtes aux États-Unis, vous pouvez contacter le [bureau local DE LASV](https://www.fbi.gov/contact-us/field), [IC3](http://www.ic3.gov/complaint/default.aspx) ou [le service secret](http://www.secretservice.gov/).</span><span class="sxs-lookup"><span data-stu-id="2891b-155">For example, if you are in the United States you can contact the [FBI local field office](https://www.fbi.gov/contact-us/field), [IC3](http://www.ic3.gov/complaint/default.aspx) or [Secret Service](http://www.secretservice.gov/).</span></span>

### <a name="submit-a-report-to-your-countrys-scam-reporting-website"></a><span data-ttu-id="2891b-156">Envoyer un rapport sur le site web de signalement des fraudes de votre pays</span><span class="sxs-lookup"><span data-stu-id="2891b-156">Submit a report to your country's scam reporting website</span></span>

<span data-ttu-id="2891b-157">Les sites web de signalement des fraudes fournissent des informations sur la prévention et la prévention des fraudes.</span><span class="sxs-lookup"><span data-stu-id="2891b-157">Scam reporting websites provide information about how to prevent and avoid scams.</span></span> <span data-ttu-id="2891b-158">Ils fournissent également des mécanismes permettant de signaler si vous avez été victime d’une fraude.</span><span class="sxs-lookup"><span data-stu-id="2891b-158">They also provide mechanisms to report if you were victim of scam.</span></span>

- <span data-ttu-id="2891b-159">Australie : [SCAMwatch](http://www.scamwatch.gov.au/)</span><span class="sxs-lookup"><span data-stu-id="2891b-159">Australia: [SCAMwatch](http://www.scamwatch.gov.au/)</span></span>

- <span data-ttu-id="2891b-160">Canada : [Centre anti-fraude canadien](http://www.antifraudcentre-centreantifraude.ca/)</span><span class="sxs-lookup"><span data-stu-id="2891b-160">Canada: [Canadian Anti-Fraud Centre](http://www.antifraudcentre-centreantifraude.ca/)</span></span>

- <span data-ttu-id="2891b-161">France : [Agence nationale de la sécurité des systèmes d’information](http://www.ssi.gouv.fr/)</span><span class="sxs-lookup"><span data-stu-id="2891b-161">France: [Agence nationale de la sécurité des systèmes d'information](http://www.ssi.gouv.fr/)</span></span>

- <span data-ttu-id="2891b-162">Allemagne : [ContrôleAmt für Sicherheit in der Informationstechnik](https://www.bsi.bund.de/DE/Home/home_node.html)</span><span class="sxs-lookup"><span data-stu-id="2891b-162">Germany: [Bundesamt für Sicherheit in der Informationstechnik](https://www.bsi.bund.de/DE/Home/home_node.html)</span></span>

- <span data-ttu-id="2891b-163">Irlande : [An Síochána](http://www.garda.ie/)</span><span class="sxs-lookup"><span data-stu-id="2891b-163">Ireland: [An Garda Síochána](http://www.garda.ie/)</span></span>

- <span data-ttu-id="2891b-164">Nouvelle-Zélande : [fraudes de consommateur](http://www.consumeraffairs.govt.nz/scams)</span><span class="sxs-lookup"><span data-stu-id="2891b-164">New Zealand: [Consumer Affairs Scams](http://www.consumeraffairs.govt.nz/scams)</span></span>

- <span data-ttu-id="2891b-165">Royaume-Uni : fraude [d’action](http://www.actionfraud.police.uk/)</span><span class="sxs-lookup"><span data-stu-id="2891b-165">United Kingdom: [Action Fraud](http://www.actionfraud.police.uk/)</span></span>

- <span data-ttu-id="2891b-166">États-Unis : [Sur Guard Online](http://www.onguardonline.gov/)</span><span class="sxs-lookup"><span data-stu-id="2891b-166">United States: [On Guard Online](http://www.onguardonline.gov/)</span></span>

<span data-ttu-id="2891b-167">Si votre pays n’est pas répertorié, demandez à vos autorités judiciaires locales ou fédérales.</span><span class="sxs-lookup"><span data-stu-id="2891b-167">If your country isn't listed, ask your local or federal law enforcement agencies.</span></span>

### <a name="submit-email-messages-to-microsoft"></a><span data-ttu-id="2891b-168">Envoyer des messages électroniques à Microsoft</span><span class="sxs-lookup"><span data-stu-id="2891b-168">Submit email messages to Microsoft</span></span>

<span data-ttu-id="2891b-169">Vous pouvez signaler des messages de hameçonnage qui contiennent un ransomware à l’aide de l’une des différentes méthodes.</span><span class="sxs-lookup"><span data-stu-id="2891b-169">You can report phishing messages that contain ransomware by using one of several methods.</span></span> <span data-ttu-id="2891b-170">Pour plus d’informations, voir [Signaler des messages et des fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="2891b-170">For more information, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2891b-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2891b-171">See also</span></span>

- [<span data-ttu-id="2891b-172">Ransomware</span><span class="sxs-lookup"><span data-stu-id="2891b-172">Ransomware</span></span>](https://docs.microsoft.com/windows/security/threat-protection/intelligence/ransomware-malware)

- [<span data-ttu-id="2891b-173">Réponse ransomware : payer ou ne pas payer ?</span><span class="sxs-lookup"><span data-stu-id="2891b-173">Ransomware response—to pay or not to pay?</span></span>](https://www.microsoft.com/security/blog/2019/12/16/ransomware-response-to-pay-or-not-to-pay/)

- [<span data-ttu-id="2891b-174">NorskQue répond aux attaques par ransomware avec transparence</span><span class="sxs-lookup"><span data-stu-id="2891b-174">Norsk Hydro responds to ransomware attack with transparency</span></span>](https://www.microsoft.com/security/blog/2019/12/17/norsk-hydro-ransomware-attack-transparency/)

- [<span data-ttu-id="2891b-175">Détection de ransomware et récupération de vos fichiers dans OneDrive</span><span class="sxs-lookup"><span data-stu-id="2891b-175">Ransomware detection and recovering your files in OneDrive</span></span>](https://support.microsoft.com/office/0d90ec50-6bfd-40f4-acc7-b8c12c73637f)

- [<span data-ttu-id="2891b-176">Rapport Microsoft Security Intelligence</span><span class="sxs-lookup"><span data-stu-id="2891b-176">Microsoft Security Intelligence Report</span></span>](https://www.microsoft.com/securityinsights/)

- [<span data-ttu-id="2891b-177">Activer ou désactiver des macros dans les fichiers Office</span><span class="sxs-lookup"><span data-stu-id="2891b-177">Enable or disable macros in Office files</span></span>](https://support.microsoft.com/office/12b036fd-d140-4e74-b45e-16fed1a7e5c6)

- [<span data-ttu-id="2891b-178">Paramètres recommandés pour la sécurité d’EOP et de Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="2891b-178">Recommended settings for EOP and Microsoft Defender for Office 365 security</span></span>](recommended-settings-for-eop-and-office365-atp.md)

- [<span data-ttu-id="2891b-179">Une mise à niveau fiable : la sécurité de nouvelle génération sur Windows 10 prouve une résilience contre les attaques de ransomware en 2017</span><span class="sxs-lookup"><span data-stu-id="2891b-179">A worthy upgrade: Next-gen security on Windows 10 proves resilient against ransomware outbreaks in 2017</span></span>](https://www.microsoft.com/security/blog/2018/01/10/a-worthy-upgrade-next-gen-security-on-windows-10-proves-resilient-against-ransomware-outbreaks-in-2017/)

- [<span data-ttu-id="2891b-180">No mas, Samas: What’s in this ransomware’s modus operandi?</span><span class="sxs-lookup"><span data-stu-id="2891b-180">No mas, Samas: What's in this ransomware's modus operandi?</span></span>](https://www.microsoft.com/security/blog/2016/03/17/no-mas-samas-whats-in-this-ransomwares-modus-operandi/)

- [<span data-ttu-id="2891b-181">Programmes malveillants verrouillés, afin de les éviter</span><span class="sxs-lookup"><span data-stu-id="2891b-181">Locky malware, lucky to avoid it</span></span>](https://www.microsoft.com/security/blog/2016/02/24/locky-malware-lucky-to-avoid-it/)

- [<span data-ttu-id="2891b-182">MSRT juillet 2016 : ransomware Cerber</span><span class="sxs-lookup"><span data-stu-id="2891b-182">MSRT July 2016: Cerber ransomware</span></span>](https://www.microsoft.com/security/blog/2016/07/12/msrt-july-2016-cerber-ransomware/)

- [<span data-ttu-id="2891b-183">Les trois têtes du ransomware Cerber de type Cerber</span><span class="sxs-lookup"><span data-stu-id="2891b-183">The three heads of the Cerberus-like Cerber ransomware</span></span>](https://www.microsoft.com/security/blog/2016/03/09/the-three-heads-of-the-cerberus-like-cerber-ransomware/)

- [<span data-ttu-id="2891b-184">Ransomware troldesh influencé par (le) code Da Postal</span><span class="sxs-lookup"><span data-stu-id="2891b-184">Troldesh ransomware influenced by (the) Da Vinci code</span></span>](https://www.microsoft.com/security/blog/2016/07/13/troldesh-ransomware-influenced-by-the-da-vinci-code/)
