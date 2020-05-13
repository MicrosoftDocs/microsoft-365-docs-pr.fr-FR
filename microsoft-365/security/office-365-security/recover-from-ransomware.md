---
title: Récupérer des attaques par ransomware
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Les administrateurs de Microsoft 365 peuvent découvrir comment effectuer une récupération suite à une attaque par ransomware.
ms.openlocfilehash: 51f5bb365fe707615444c1399479171aa72755e1
ms.sourcegitcommit: 93c0088d272cd45f1632a1dcaf04159f234abccd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2020
ms.locfileid: "44208257"
---
# <a name="recover-from-a-ransomware-attack-in-microsoft-365"></a><span data-ttu-id="f38f5-103">Récupération d’une attaque par ransomware dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f38f5-103">Recover from a ransomware attack in Microsoft 365</span></span>

<span data-ttu-id="f38f5-104">Même si vous avez toutes les précautions à prendre pour protéger votre organisation, vous pouvez toujours devenir victime d’une attaque par [ransomware](https://docs.microsoft.com/windows/security/threat-protection/intelligence/ransomware-malware) .</span><span class="sxs-lookup"><span data-stu-id="f38f5-104">Even if you take every precaution to protect your organization, you can still fall victim to a [ransomware](https://docs.microsoft.com/windows/security/threat-protection/intelligence/ransomware-malware) attack.</span></span> <span data-ttu-id="f38f5-105">Les ransomware sont de grandes entreprises et les attaques sont vérifiées de façon sophistiquée.</span><span class="sxs-lookup"><span data-stu-id="f38f5-105">Ransomware is big business, and the attacks are verify sophisticated.</span></span>

<span data-ttu-id="f38f5-106">Les étapes de cette rubrique vous permettront de récupérer les données qui ont été chiffrées par le ransomware, et vous aideront à arrêter la propagation de l’infection dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f38f5-106">The steps in this topic will give you the best chance to recover data that was encrypted by the ransomware, and will help stop the spread of the infection in your organization.</span></span> <span data-ttu-id="f38f5-107">Avant de commencer, prenez en compte les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="f38f5-107">Before you get started, consider the following items:</span></span>

- <span data-ttu-id="f38f5-108">Il n’existe aucune garantie que le fait de payer le ransomware renverra l’accès à vos fichiers.</span><span class="sxs-lookup"><span data-stu-id="f38f5-108">There's no guarantee that paying the ransom will return access to your files.</span></span> <span data-ttu-id="f38f5-109">En fait, le paiement du ransomware peut vous faire une cible pour plus de ransomware.</span><span class="sxs-lookup"><span data-stu-id="f38f5-109">In fact, paying the ransom can make you a target for more ransomware.</span></span> <span data-ttu-id="f38f5-110">Si vous avez déjà payé, mais que vous avez réussi à récupérer vos fichiers sans avoir à utiliser la résolution de l’agresseur, vous devez appeler votre banque pour savoir si elle peut bloquer la transaction.</span><span class="sxs-lookup"><span data-stu-id="f38f5-110">If you've already paid, but you were able to successfully recover your files without having to use the attacker's resolution, you should call your bank to see if they can block the transaction.</span></span> <span data-ttu-id="f38f5-111">Nous vous recommandons également de signaler les attaques par ransomware à l’application de la Loi, les sites Web de signalement de fraude et Microsoft, comme décrit plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="f38f5-111">We also recommend that you report the ransomware attack to law enforcement, scam reporting websites and Microsoft as described later in this topic.</span></span>

- <span data-ttu-id="f38f5-112">Il est très important de répondre rapidement à l’attaque et ses conséquences.</span><span class="sxs-lookup"><span data-stu-id="f38f5-112">It's very important that you respond quickly to the attack and its consequences.</span></span> <span data-ttu-id="f38f5-113">Plus vous patientez, moins vous pouvez récupérer les données affectées.</span><span class="sxs-lookup"><span data-stu-id="f38f5-113">The longer you wait, the less likely it is that you can recover the affected data.</span></span>

## <a name="step-1-verify-your-backups"></a><span data-ttu-id="f38f5-114">Étape 1 : vérifier vos sauvegardes</span><span class="sxs-lookup"><span data-stu-id="f38f5-114">Step 1: Verify your backups</span></span>

<span data-ttu-id="f38f5-115">Si vous avez des sauvegardes hors connexion, vous pouvez probablement restaurer les données chiffrées **après avoir** supprimé la charge du ransomware (programme malveillant) de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="f38f5-115">If you have offline backups, you can probably restore the encrypted data **after** you've removed the ransomware payload (malware) from your environment.</span></span>

<span data-ttu-id="f38f5-116">Si vous n’avez pas de sauvegardes, ou si vos sauvegardes ont également été affectées par le ransomware, vous pouvez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="f38f5-116">If you don't have backups, or if your backups were also affected by the ransomware, you can skip this step.</span></span>

## <a name="step-2-disable-activesync-and-onedrive-sync"></a><span data-ttu-id="f38f5-117">Étape 2 : désactivation d’ActiveSync et de la synchronisation OneDrive</span><span class="sxs-lookup"><span data-stu-id="f38f5-117">Step 2: Disable ActiveSync and OneDrive sync</span></span>

<span data-ttu-id="f38f5-118">Le point important ici est d’arrêter la propagation du chiffrement des données par les ransomware.</span><span class="sxs-lookup"><span data-stu-id="f38f5-118">The key point here is to stop the spread of data encryption by the ransomware.</span></span>

<span data-ttu-id="f38f5-119">Si vous pensez que le courrier électronique est une cible, vous devez temporairement désactiver l’accès des utilisateurs aux boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="f38f5-119">If you suspect that email is a target, you should temporarily disable user access to mailboxes.</span></span> <span data-ttu-id="f38f5-120">Exchange ActiveSync est utilisé par les appareils mobiles pour synchroniser les données entre l’appareil et la boîte aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="f38f5-120">Exchange ActiveSync is used by mobile devices to synchronize data between the device and the Exchange Online mailbox.</span></span>

<span data-ttu-id="f38f5-121">Pour désactiver ActiveSync pour une boîte aux lettres, consultez [la rubrique How to Disable Exchange ActiveSync for users in Exchange Online](https://support.microsoft.com/help/2795303/how-to-disable-exchange-activesync-for-users-in-office-365).</span><span class="sxs-lookup"><span data-stu-id="f38f5-121">To disable ActiveSync for a mailbox, see [How to disable Exchange ActiveSync for users in Exchange Online](https://support.microsoft.com/help/2795303/how-to-disable-exchange-activesync-for-users-in-office-365).</span></span>

<span data-ttu-id="f38f5-122">Pour désactiver d’autres types d’accès à une boîte aux lettres, voir :</span><span class="sxs-lookup"><span data-stu-id="f38f5-122">To disable other types of access to a mailbox, see:</span></span>

- <span data-ttu-id="f38f5-123">[Activer ou désactiver MAPI pour une boîte aux lettres](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-user-mailboxes/enable-or-disable-mapi).</span><span class="sxs-lookup"><span data-stu-id="f38f5-123">[Enable or disable MAPI for a mailbox](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-user-mailboxes/enable-or-disable-mapi).</span></span>

- [<span data-ttu-id="f38f5-124">Activer ou désactiver l’accès POP3 ou IMAP4 pour un utilisateur</span><span class="sxs-lookup"><span data-stu-id="f38f5-124">Enable or Disable POP3 or IMAP4 access for a user</span></span>](https://docs.microsoft.com/Exchange/clients-and-mobile-in-exchange-online/pop3-and-imap4/enable-or-disable-pop3-or-imap4-access)

<span data-ttu-id="f38f5-125">La suspension de la synchronisation de OneDrive permettra de protéger vos données de Cloud contre la mise à jour des appareils potentiellement infectés.</span><span class="sxs-lookup"><span data-stu-id="f38f5-125">Pausing OneDrive sync will help protect your cloud data from being updated by potentially infected devices.</span></span> <span data-ttu-id="f38f5-126">Pour plus d’informations, consultez [la rubrique How to pause and Resume Sync in OneDrive](https://support.office.com/article/2152bfa4-a2a5-4d3a-ace8-92912fb4421e).</span><span class="sxs-lookup"><span data-stu-id="f38f5-126">For more information, see [How to Pause and Resume sync in OneDrive](https://support.office.com/article/2152bfa4-a2a5-4d3a-ace8-92912fb4421e).</span></span>

## <a name="step-3-remove-the-malware-from-the-affected-devices"></a><span data-ttu-id="f38f5-127">Étape 3 : supprimer le programme malveillant des appareils affectés</span><span class="sxs-lookup"><span data-stu-id="f38f5-127">Step 3: Remove the malware from the affected devices</span></span>

<span data-ttu-id="f38f5-128">Exécutez une analyse antivirus complète avec les mises à jour les plus récentes sur tous les ordinateurs et appareils suspects pour détecter et supprimer la charge utile associée aux ransomware.</span><span class="sxs-lookup"><span data-stu-id="f38f5-128">Run a full antivirus scan with the latest updates on all suspected computers and devices to detect and remove the payload that's associated with the ransomware.</span></span> <span data-ttu-id="f38f5-129">N’oubliez pas les appareils qui synchronisent des données ou la cible des lecteurs réseau mappés (ces ordinateurs et périphériques doivent également être analysés).</span><span class="sxs-lookup"><span data-stu-id="f38f5-129">Don't forget devices that are synchronizing data, or the target of mapped network drives (those computers and devices need to be scanned, too).</span></span>

<span data-ttu-id="f38f5-130">Vous pouvez utiliser [Windows Defender](https://www.microsoft.com/windows/comprehensive-security) ou (pour les clients plus anciens) [Microsoft Security Essentials](https://www.microsoft.com/download/details.aspx?id=5201).</span><span class="sxs-lookup"><span data-stu-id="f38f5-130">You can use [Windows Defender](https://www.microsoft.com/windows/comprehensive-security) or (for older clients) [Microsoft Security Essentials](https://www.microsoft.com/download/details.aspx?id=5201).</span></span>

<span data-ttu-id="f38f5-131">L' [outil de suppression des logiciels malveillants (MSRT)](https://www.microsoft.com/download/details.aspx?id=9905)peut également être utilisé pour supprimer des ransomware ou des programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="f38f5-131">An alternative that will also help you remove ransomware or malware is the [Malicious Software Removal Tool (MSRT)](https://www.microsoft.com/download/details.aspx?id=9905).</span></span>

<span data-ttu-id="f38f5-132">Si ces options ne fonctionnent pas, vous pouvez essayer [Windows Defender Offline](https://support.microsoft.com/help/17466/windows-defender-offline-help-protect-my-pc) ou [résoudre les problèmes liés à la détection et à la suppression de programmes malveillants](https://support.microsoft.com/help/4466982/windows-10-troubleshoot-problems-with-detecting-and-removing-malware).</span><span class="sxs-lookup"><span data-stu-id="f38f5-132">If these options don't work, you can try [Windows Defender Offline](https://support.microsoft.com/help/17466/windows-defender-offline-help-protect-my-pc) or [Troubleshoot problems with detecting and removing malware](https://support.microsoft.com/help/4466982/windows-10-troubleshoot-problems-with-detecting-and-removing-malware).</span></span>

## <a name="step-4-recover-files-on-a-cleaned-computer-or-device"></a><span data-ttu-id="f38f5-133">Étape 4 : récupérer des fichiers sur un ordinateur ou un périphérique nettoyé</span><span class="sxs-lookup"><span data-stu-id="f38f5-133">Step 4: Recover files on a cleaned computer or device</span></span>

<span data-ttu-id="f38f5-134">Une fois que vous avez terminé l’étape précédente pour supprimer la charge du ransomware de votre environnement (ce qui empêchera les ransomware de chiffrer ou supprimer vos fichiers), vous pouvez utiliser [l’historique des fichiers](https://support.microsoft.com/help/17128/windows-8-file-history) dans Windows 10 et Windows 8,1 ou la protection du système dans Windows 7 pour tenter de récupérer vos fichiers et dossiers locaux.</span><span class="sxs-lookup"><span data-stu-id="f38f5-134">After you've completed the previous step to remove the ransomware payload from your environment (which will prevent the ransomware from encrypting or removing your files), you can use [File History](https://support.microsoft.com/help/17128/windows-8-file-history) in Windows 10 and Windows 8.1 or System Protection in Windows 7 to attempt to recover your local files and folders.</span></span>

<span data-ttu-id="f38f5-135">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="f38f5-135">**Notes**:</span></span>

- <span data-ttu-id="f38f5-136">Certains ransomware seront également en mesure de chiffrer ou de supprimer les versions de sauvegarde, de sorte que vous ne pouvez pas utiliser l’historique des fichiers ou la protection du système pour restaurer des fichiers.</span><span class="sxs-lookup"><span data-stu-id="f38f5-136">Some ransomware will also encrypt or delete the backup versions, so you can't use File History or System Protection to restore files.</span></span> <span data-ttu-id="f38f5-137">Dans ce cas, vous devez utiliser des sauvegardes sur des lecteurs externes ou des périphériques qui n’ont pas été affectés par le ransomware ou le OneDrive, comme décrit dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="f38f5-137">If that happens, you need use backups on external drives or devices that were not affected by the ransomware or OneDrive as described in the next section.</span></span>

- <span data-ttu-id="f38f5-138">Si un dossier est synchronisé avec OneDrive et que vous n’utilisez pas la dernière version de Windows, certaines limites peuvent se présenter à l’aide de l’historique des fichiers.</span><span class="sxs-lookup"><span data-stu-id="f38f5-138">If a folder is synchronized to OneDrive and you aren't using the latest version of Windows, there might be some limitations using File History.</span></span>

## <a name="step-5-recover-your-files-in-your-onedrive-for-business"></a><span data-ttu-id="f38f5-139">Étape 5 : récupération de vos fichiers dans OneDrive entreprise</span><span class="sxs-lookup"><span data-stu-id="f38f5-139">Step 5: Recover your files in your OneDrive for Business</span></span>

<span data-ttu-id="f38f5-140">La restauration des fichiers dans OneDrive entreprise vous permet de restaurer l’intégralité de votre OneDrive à un point antérieur dans le temps au cours des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="f38f5-140">Files Restore in OneDrive for Business allows you to restore your entire OneDrive to a previous point in time within the last 30 days.</span></span> <span data-ttu-id="f38f5-141">Pour plus d’informations, consultez [la rubrique restaurer votre espace OneDrive](https://support.office.com/article/fa231298-759d-41cf-bcd0-25ac53eb8a15).</span><span class="sxs-lookup"><span data-stu-id="f38f5-141">For more information, see [Restore your OneDrive](https://support.office.com/article/fa231298-759d-41cf-bcd0-25ac53eb8a15).</span></span>

## <a name="step-6-recover-deleted-email"></a><span data-ttu-id="f38f5-142">Étape 6 : récupérer les messages électroniques supprimés</span><span class="sxs-lookup"><span data-stu-id="f38f5-142">Step 6: Recover deleted email</span></span>

<span data-ttu-id="f38f5-143">Dans le cas rare où le ransomware a supprimé tous vos courriers électroniques, vous pouvez probablement récupérer les éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="f38f5-143">In the rare case that the ransomware deleted all your email, you can probably recover the deleted items.</span></span> <span data-ttu-id="f38f5-144">Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="f38f5-144">For more information, see:</span></span>

- [<span data-ttu-id="f38f5-145">Récupérer des messages supprimés dans la boîte aux lettres d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="f38f5-145">Recover deleted messages in a user's mailbox</span></span>](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-user-mailboxes/recover-deleted-messages)

- [<span data-ttu-id="f38f5-146">Récupérer des éléments supprimés dans Outlook pour Windows</span><span class="sxs-lookup"><span data-stu-id="f38f5-146">Recover deleted items in Outlook for Windows</span></span>](https://support.office.com/article/49e81f3c-c8f4-4426-a0b9-c0fd751d48ce)

## <a name="step-7-re-enable-exchange-activesync-and-onedrive-sync"></a><span data-ttu-id="f38f5-147">Étape 7 : réactivation de la synchronisation Exchange ActiveSync et OneDrive</span><span class="sxs-lookup"><span data-stu-id="f38f5-147">Step 7: Re-enable Exchange ActiveSync and OneDrive sync</span></span>

<span data-ttu-id="f38f5-148">Une fois que vous avez nettoyé vos ordinateurs et vos appareils et récupéré vos données, vous pouvez réactiver la synchronisation ActiveSync et OneDrive que vous avez précédemment désactivée à l' [étape 2](#step-2-disable-activesync-and-onedrive-sync).</span><span class="sxs-lookup"><span data-stu-id="f38f5-148">After you've cleaned your computers and devices and recovered your data, you can re-enable ActiveSync and OneDrive sync that you previously disabled in [Step 2](#step-2-disable-activesync-and-onedrive-sync).</span></span>

## <a name="step-8-optional-block-onedrive-sync-for-specific-file-extensions"></a><span data-ttu-id="f38f5-149">Étape 8 (facultatif) : bloquer la synchronisation de OneDrive pour des extensions de fichier spécifiques</span><span class="sxs-lookup"><span data-stu-id="f38f5-149">Step 8 (Optional): Block OneDrive sync for specific file extensions</span></span>

<span data-ttu-id="f38f5-150">Une fois que vous avez effectué la récupération, vous pouvez empêcher les clients OneDrive entreprise de synchroniser les types de fichiers qui ont été affectés par ces ransomware.</span><span class="sxs-lookup"><span data-stu-id="f38f5-150">After you've recovered, you can prevent OneDrive for Business clients from synchronizing the file types that were affected by this ransomware.</span></span> <span data-ttu-id="f38f5-151">Pour plus d’informations, consultez la rubrique [Set-SPOTenantSyncClientRestriction](https://docs.microsoft.com/powershell/module/sharepoint-online/set-spotenantsyncclientrestriction)</span><span class="sxs-lookup"><span data-stu-id="f38f5-151">For more information, see [Set-SPOTenantSyncClientRestriction](https://docs.microsoft.com/powershell/module/sharepoint-online/set-spotenantsyncclientrestriction)</span></span>

## <a name="report-the-attack"></a><span data-ttu-id="f38f5-152">Signaler l’attaque</span><span class="sxs-lookup"><span data-stu-id="f38f5-152">Report the attack</span></span>

### <a name="contact-law-enforcement"></a><span data-ttu-id="f38f5-153">Application de la Loi sur les contacts</span><span class="sxs-lookup"><span data-stu-id="f38f5-153">Contact law enforcement</span></span>

<span data-ttu-id="f38f5-154">Vous devez contacter vos organismes d’application de la loi fédérale ou locale.</span><span class="sxs-lookup"><span data-stu-id="f38f5-154">You should contact your local or federal law enforcement agencies.</span></span> <span data-ttu-id="f38f5-155">Par exemple, si vous êtes aux États-Unis, vous pouvez contacter le service de [terrain local FBI](https://www.fbi.gov/contact-us/field), le [IC3](http://www.ic3.gov/complaint/default.aspx) ou le [service secret](http://www.secretservice.gov/).</span><span class="sxs-lookup"><span data-stu-id="f38f5-155">For example, if you are in the United States you can contact the [FBI local field office](https://www.fbi.gov/contact-us/field), [IC3](http://www.ic3.gov/complaint/default.aspx) or [Secret Service](http://www.secretservice.gov/).</span></span>

### <a name="submit-a-report-to-your-countrys-scam-reporting-website"></a><span data-ttu-id="f38f5-156">Envoyer un rapport sur le site Web de notification d’escroquerie de votre pays</span><span class="sxs-lookup"><span data-stu-id="f38f5-156">Submit a report to your country's scam reporting website</span></span>

<span data-ttu-id="f38f5-157">Les sites Web de signalement de fraude fournissent des informations sur la façon d’empêcher et d’éviter les arnaques.</span><span class="sxs-lookup"><span data-stu-id="f38f5-157">Scam reporting websites provide information about how to prevent and avoid scams.</span></span> <span data-ttu-id="f38f5-158">Ils fournissent également des mécanismes de signalement si vous avez été victime d’une escroquerie.</span><span class="sxs-lookup"><span data-stu-id="f38f5-158">They also provide mechanisms to report if you were victim of scam.</span></span>

- <span data-ttu-id="f38f5-159">Australie : [SCAMwatch](http://www.scamwatch.gov.au/)</span><span class="sxs-lookup"><span data-stu-id="f38f5-159">Australia: [SCAMwatch](http://www.scamwatch.gov.au/)</span></span>

- <span data-ttu-id="f38f5-160">Canada : [Centre anti-fraude canadien](http://www.antifraudcentre-centreantifraude.ca/)</span><span class="sxs-lookup"><span data-stu-id="f38f5-160">Canada: [Canadian Anti-Fraud Centre](http://www.antifraudcentre-centreantifraude.ca/)</span></span>

- <span data-ttu-id="f38f5-161">France : [Agence nationale de la sécurité des systèmes d’information](http://www.ssi.gouv.fr/)</span><span class="sxs-lookup"><span data-stu-id="f38f5-161">France: [Agence nationale de la sécurité des systèmes d'information](http://www.ssi.gouv.fr/)</span></span>

- <span data-ttu-id="f38f5-162">Allemagne : [Bundesamt für Sicherheit dans der Informationstechnik](https://www.bsi.bund.de/DE/Home/home_node.html)</span><span class="sxs-lookup"><span data-stu-id="f38f5-162">Germany: [Bundesamt für Sicherheit in der Informationstechnik](https://www.bsi.bund.de/DE/Home/home_node.html)</span></span>

- <span data-ttu-id="f38f5-163">Irlande : [un Garda Síochána](http://www.garda.ie/)</span><span class="sxs-lookup"><span data-stu-id="f38f5-163">Ireland: [An Garda Síochána](http://www.garda.ie/)</span></span>

- <span data-ttu-id="f38f5-164">Nouvelle-Zélande : [arnaques](http://www.consumeraffairs.govt.nz/scams) pour les consommateurs</span><span class="sxs-lookup"><span data-stu-id="f38f5-164">New Zealand: [Consumer Affairs Scams](http://www.consumeraffairs.govt.nz/scams)</span></span>

- <span data-ttu-id="f38f5-165">Royaume-Uni : [fraude d’action](http://www.actionfraud.police.uk/)</span><span class="sxs-lookup"><span data-stu-id="f38f5-165">United Kingdom: [Action Fraud](http://www.actionfraud.police.uk/)</span></span>

- <span data-ttu-id="f38f5-166">États-Unis : [on Guard Online](http://www.onguardonline.gov/)</span><span class="sxs-lookup"><span data-stu-id="f38f5-166">United States: [On Guard Online](http://www.onguardonline.gov/)</span></span>

<span data-ttu-id="f38f5-167">Si votre pays n’est pas indiqué, demandez à vos organismes d’application de la loi locale ou fédérale.</span><span class="sxs-lookup"><span data-stu-id="f38f5-167">If your country isn't listed, ask your local or federal law enforcement agencies.</span></span>

### <a name="submit-email-messages-to-microsoft"></a><span data-ttu-id="f38f5-168">Envoyer des messages électroniques à Microsoft</span><span class="sxs-lookup"><span data-stu-id="f38f5-168">Submit email messages to Microsoft</span></span>

<span data-ttu-id="f38f5-169">Vous pouvez signaler un message de hameçonnage contenant des ransomware à l’aide de l’une des méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="f38f5-169">You can report phishing message that contain ransomware by using one of several methods.</span></span> <span data-ttu-id="f38f5-170">Pour plus d’informations, voir [Signaler des messages et des fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="f38f5-170">For more information, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f38f5-171">Articles associés</span><span class="sxs-lookup"><span data-stu-id="f38f5-171">See also</span></span>

- [<span data-ttu-id="f38f5-172">Rançongiciels</span><span class="sxs-lookup"><span data-stu-id="f38f5-172">Ransomware</span></span>](https://docs.microsoft.com/windows/security/threat-protection/intelligence/ransomware-malware)

- [<span data-ttu-id="f38f5-173">Réponse contre les ransomware : souhaitez-vous payer ou ne pas payer ?</span><span class="sxs-lookup"><span data-stu-id="f38f5-173">Ransomware response—to pay or not to pay?</span></span>](https://www.microsoft.com/security/blog/2019/12/16/ransomware-response-to-pay-or-not-to-pay/)

- [<span data-ttu-id="f38f5-174">Norsk Hydro répond aux attaques par ransomware avec transparence</span><span class="sxs-lookup"><span data-stu-id="f38f5-174">Norsk Hydro responds to ransomware attack with transparency</span></span>](https://www.microsoft.com/security/blog/2019/12/17/norsk-hydro-ransomware-attack-transparency/)

- [<span data-ttu-id="f38f5-175">Détection de ransomware et RECUPERATION de vos fichiers dans OneDrive</span><span class="sxs-lookup"><span data-stu-id="f38f5-175">Ransomware detection and recovering your files in OneDrive</span></span>](https://support.office.com/article/0d90ec50-6bfd-40f4-acc7-b8c12c73637f)

- [<span data-ttu-id="f38f5-176">Rapport sur les renseignements de sécurité Microsoft</span><span class="sxs-lookup"><span data-stu-id="f38f5-176">Microsoft Security Intelligence Report</span></span>](https://www.microsoft.com/securityinsights/)

- [<span data-ttu-id="f38f5-177">Activer ou désactiver les macros dans les fichiers Office</span><span class="sxs-lookup"><span data-stu-id="f38f5-177">Enable or disable macros in Office files</span></span>](https://support.office.com/article/12b036fd-d140-4e74-b45e-16fed1a7e5c6)

- [<span data-ttu-id="f38f5-178">Paramètres recommandés pour la sécurité ATP d’Office 365</span><span class="sxs-lookup"><span data-stu-id="f38f5-178">Recommended settings for EOP and Office 365 ATP security</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/recommended-settings-for-eop-and-office365-atp)

- [<span data-ttu-id="f38f5-179">Une mise à niveau fiable : la sécurité de la génération suivante sur Windows 10 s’avère résiliente contre les foyers de ransomware dans 2017</span><span class="sxs-lookup"><span data-stu-id="f38f5-179">A worthy upgrade: Next-gen security on Windows 10 proves resilient against ransomware outbreaks in 2017</span></span>](https://www.microsoft.com/security/blog/2018/01/10/a-worthy-upgrade-next-gen-security-on-windows-10-proves-resilient-against-ransomware-outbreaks-in-2017/)

- [<span data-ttu-id="f38f5-180">Aucune Mas, Samas : qu’est-ce que le modus operandi de ce ransomware ?</span><span class="sxs-lookup"><span data-stu-id="f38f5-180">No mas, Samas: What's in this ransomware's modus operandi?</span></span>](https://www.microsoft.com/security/blog/2016/03/17/no-mas-samas-whats-in-this-ransomwares-modus-operandi/)

- [<span data-ttu-id="f38f5-181">Protection contre les programmes malveillants, la chance de l’éviter</span><span class="sxs-lookup"><span data-stu-id="f38f5-181">Locky malware, lucky to avoid it</span></span>](https://www.microsoft.com/security/blog/2016/02/24/locky-malware-lucky-to-avoid-it/)

- [<span data-ttu-id="f38f5-182">MSRT juillet 2016 : cerber ransomware</span><span class="sxs-lookup"><span data-stu-id="f38f5-182">MSRT July 2016: Cerber ransomware</span></span>](https://www.microsoft.com/security/blog/2016/07/12/msrt-july-2016-cerber-ransomware/)

- [<span data-ttu-id="f38f5-183">Les trois têtes du Cerberus cerber ransomware</span><span class="sxs-lookup"><span data-stu-id="f38f5-183">The three heads of the Cerberus-like Cerber ransomware</span></span>](https://www.microsoft.com/security/blog/2016/03/09/the-three-heads-of-the-cerberus-like-cerber-ransomware/)

- [<span data-ttu-id="f38f5-184">Troldesh ransomware influencé par (le) Code da Vinci</span><span class="sxs-lookup"><span data-stu-id="f38f5-184">Troldesh ransomware influenced by (the) Da Vinci code</span></span>](https://www.microsoft.com/security/blog/2016/07/13/troldesh-ransomware-influenced-by-the-da-vinci-code/)
