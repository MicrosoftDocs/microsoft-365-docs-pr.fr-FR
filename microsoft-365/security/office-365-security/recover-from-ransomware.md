---
title: Récupérer après une attaque par rançongiciel
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.article: how-to
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
description: Les administrateurs Microsoft 365 peuvent apprendre à récupérer d’une attaque par ransomware.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: b834adb3d9ba5f85984e09b4bb1e4b48673c32f2
ms.sourcegitcommit: a1846b1ee2e4fa397e39c1271c997fc4cf6d5619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "50166902"
---
# <a name="recover-from-a-ransomware-attack-in-microsoft-365"></a><span data-ttu-id="68e1e-103">Récupérer d’une attaque par ransomware dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="68e1e-103">Recover from a ransomware attack in Microsoft 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="68e1e-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="68e1e-104">**Applies to**</span></span>
- [<span data-ttu-id="68e1e-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="68e1e-105">Exchange Online Protection</span></span>](https://go.microsoft.com/fwlink/?linkid=2148611)
- [<span data-ttu-id="68e1e-106">Microsoft Defender pour Office 365 plan 1 et plan 2</span><span class="sxs-lookup"><span data-stu-id="68e1e-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](https://go.microsoft.com/fwlink/?linkid=2148715)
- [<span data-ttu-id="68e1e-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="68e1e-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="68e1e-108">Même si vous prenez toutes les précautions nécessaires pour protéger votre organisation, vous pouvez toujours être la victime d’une attaque par [ransomware.](https://docs.microsoft.com/windows/security/threat-protection/intelligence/ransomware-malware)</span><span class="sxs-lookup"><span data-stu-id="68e1e-108">Even if you take every precaution to protect your organization, you can still fall victim to a [ransomware](https://docs.microsoft.com/windows/security/threat-protection/intelligence/ransomware-malware) attack.</span></span> <span data-ttu-id="68e1e-109">Les ransomware sont une grande entreprise et les attaques sont très sophistiquées.</span><span class="sxs-lookup"><span data-stu-id="68e1e-109">Ransomware is big business, and the attacks are very sophisticated.</span></span>

<span data-ttu-id="68e1e-110">Les étapes de cet article vous offrent la meilleure opportunité de récupérer des données et d’arrêter la propagation interne de l’infection.</span><span class="sxs-lookup"><span data-stu-id="68e1e-110">The steps in this article will give you the best chance to recover data and stop the internal spread of infection.</span></span> <span data-ttu-id="68e1e-111">Avant de commencer, prenez en compte les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="68e1e-111">Before you get started, consider the following items:</span></span>

- <span data-ttu-id="68e1e-112">Il n’existe aucune garantie que le paiement de la rançon retourne l’accès à vos fichiers.</span><span class="sxs-lookup"><span data-stu-id="68e1e-112">There's no guarantee that paying the ransom will return access to your files.</span></span> <span data-ttu-id="68e1e-113">En fait, le paiement de la rançon peut faire de vous une cible pour d’autres ransomware.</span><span class="sxs-lookup"><span data-stu-id="68e1e-113">In fact, paying the ransom can make you a target for more ransomware.</span></span>

  <span data-ttu-id="68e1e-114">Si vous avez déjà payé, mais que vous avez récupéré sans utiliser la solution de l’attaquant, contactez votre banque pour voir si elle peut bloquer la transaction.</span><span class="sxs-lookup"><span data-stu-id="68e1e-114">If you already paid, but you recovered without using the attacker's solution, contact your bank to see if they can block the transaction.</span></span>

  <span data-ttu-id="68e1e-115">Nous vous recommandons également de signaler l’attaque par ransomware aux forces de l’ordre, aux sites web de signalement des fraudes et à Microsoft, comme décrit plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="68e1e-115">We also recommend that you report the ransomware attack to law enforcement, scam reporting websites, and Microsoft as described later in this article.</span></span>

- <span data-ttu-id="68e1e-116">Il est important que vous répondiez rapidement à l’attaque et à ses conséquences.</span><span class="sxs-lookup"><span data-stu-id="68e1e-116">It's important for you respond quickly to the attack and its consequences.</span></span> <span data-ttu-id="68e1e-117">Plus vous patientez longtemps, moins il est probable que vous récupériez les données affectées.</span><span class="sxs-lookup"><span data-stu-id="68e1e-117">The longer you wait, the less likely it is that you can recover the affected data.</span></span>

## <a name="step-1-verify-your-backups"></a><span data-ttu-id="68e1e-118">Étape 1 : Vérifier vos sauvegardes</span><span class="sxs-lookup"><span data-stu-id="68e1e-118">Step 1: Verify your backups</span></span>

<span data-ttu-id="68e1e-119">Si vous avez des sauvegardes hors connexion,  vous pouvez probablement restaurer les données chiffrées après avoir supprimé la charge utile du ransomware (programme malveillant) de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="68e1e-119">If you have offline backups, you can probably restore the encrypted data **after** you've removed the ransomware payload (malware) from your environment.</span></span>

<span data-ttu-id="68e1e-120">Si vous n’avez pas de sauvegardes ou si vos sauvegardes ont également été affectées par le ransomware, vous pouvez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="68e1e-120">If you don't have backups, or if your backups were also affected by the ransomware, you can skip this step.</span></span>

## <a name="step-2-disable-exchange-activesync-and-onedrive-sync"></a><span data-ttu-id="68e1e-121">Étape 2 : Désactiver la synchronisation Exchange ActiveSync et OneDrive</span><span class="sxs-lookup"><span data-stu-id="68e1e-121">Step 2: Disable Exchange ActiveSync and OneDrive sync</span></span>

<span data-ttu-id="68e1e-122">Le point clé ici est d’arrêter la propagation du chiffrement des données par le ransomware.</span><span class="sxs-lookup"><span data-stu-id="68e1e-122">The key point here is to stop the spread of data encryption by the ransomware.</span></span>

<span data-ttu-id="68e1e-123">Si vous pensez que le courrier électronique est une cible du chiffrement de ransomware, désactivez temporairement l’accès des utilisateurs aux boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="68e1e-123">If you suspect email as a target of the ransomware encryption, temporarily disable user access to mailboxes.</span></span> <span data-ttu-id="68e1e-124">Exchange ActiveSync synchronise les données entre les appareils et les boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="68e1e-124">Exchange ActiveSync synchronizes data between devices and Exchange Online mailboxes.</span></span>

<span data-ttu-id="68e1e-125">Pour désactiver la Exchange ActiveSync d’une boîte aux lettres, consultez la Exchange ActiveSync pour les [utilisateurs dans Exchange Online.](https://support.microsoft.com/help/2795303)</span><span class="sxs-lookup"><span data-stu-id="68e1e-125">To disable Exchange ActiveSync for a mailbox, see [How to disable Exchange ActiveSync for users in Exchange Online](https://support.microsoft.com/help/2795303).</span></span>

<span data-ttu-id="68e1e-126">Pour désactiver d’autres types d’accès à une boîte aux lettres, voir :</span><span class="sxs-lookup"><span data-stu-id="68e1e-126">To disable other types of access to a mailbox, see:</span></span>

- <span data-ttu-id="68e1e-127">[Activez ou désactivez MAPI pour une boîte aux lettres.](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-user-mailboxes/enable-or-disable-mapi)</span><span class="sxs-lookup"><span data-stu-id="68e1e-127">[Enable or disable MAPI for a mailbox](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-user-mailboxes/enable-or-disable-mapi).</span></span>

- [<span data-ttu-id="68e1e-128">Activer ou désactiver l’accès POP3 ou IMAP4 pour un utilisateur</span><span class="sxs-lookup"><span data-stu-id="68e1e-128">Enable or Disable POP3 or IMAP4 access for a user</span></span>](https://docs.microsoft.com/Exchange/clients-and-mobile-in-exchange-online/pop3-and-imap4/enable-or-disable-pop3-or-imap4-access)

<span data-ttu-id="68e1e-129">L’interruption de la synchronisation OneDrive permet de protéger vos données cloud contre la mise à jour par des appareils potentiellement infectés.</span><span class="sxs-lookup"><span data-stu-id="68e1e-129">Pausing OneDrive sync will help protect your cloud data from being updated by potentially infected devices.</span></span> <span data-ttu-id="68e1e-130">Pour plus d’informations, [voir Comment suspendre et reprendre la synchronisation dans OneDrive](https://support.microsoft.com/office/2152bfa4-a2a5-4d3a-ace8-92912fb4421e).</span><span class="sxs-lookup"><span data-stu-id="68e1e-130">For more information, see [How to Pause and Resume sync in OneDrive](https://support.microsoft.com/office/2152bfa4-a2a5-4d3a-ace8-92912fb4421e).</span></span>

## <a name="step-3-remove-the-malware-from-the-affected-devices"></a><span data-ttu-id="68e1e-131">Étape 3 : Supprimer les programmes malveillants des appareils concernés</span><span class="sxs-lookup"><span data-stu-id="68e1e-131">Step 3: Remove the malware from the affected devices</span></span>

<span data-ttu-id="68e1e-132">Exécutez une analyse antivirus complète et actuelle sur tous les ordinateurs et appareils suspectés de détecter et de supprimer la charge utile associée au ransomware.</span><span class="sxs-lookup"><span data-stu-id="68e1e-132">Run a full, current antivirus scan on all suspected computers and devices to detect and remove the payload that's associated with the ransomware.</span></span>

<span data-ttu-id="68e1e-133">N’oubliez pas d’analyser les appareils qui synchronisent des données ou les cibles des lecteurs réseau mappés.</span><span class="sxs-lookup"><span data-stu-id="68e1e-133">Don't forget to scan devices that are synchronizing data, or the targets of mapped network drives.</span></span>

<span data-ttu-id="68e1e-134">Vous pouvez utiliser [Windows Defender](https://www.microsoft.com/windows/comprehensive-security) ou (pour les clients [plus anciens) Microsoft Security Essentials](https://www.microsoft.com/download/details.aspx?id=5201).</span><span class="sxs-lookup"><span data-stu-id="68e1e-134">You can use [Windows Defender](https://www.microsoft.com/windows/comprehensive-security) or (for older clients) [Microsoft Security Essentials](https://www.microsoft.com/download/details.aspx?id=5201).</span></span>

<span data-ttu-id="68e1e-135">Une alternative qui vous aidera également à supprimer des ransomware ou des programmes malveillants est l’outil de suppression de logiciels malveillants [(MSRT).](https://www.microsoft.com/download/details.aspx?id=9905)</span><span class="sxs-lookup"><span data-stu-id="68e1e-135">An alternative that will also help you remove ransomware or malware is the [Malicious Software Removal Tool (MSRT)](https://www.microsoft.com/download/details.aspx?id=9905).</span></span>

<span data-ttu-id="68e1e-136">Si ces options ne fonctionnent pas, vous pouvez essayer Windows Defender [hors](https://support.microsoft.com/help/17466) connexion ou résoudre les problèmes liés à la détection et à la suppression [de programmes malveillants.](https://support.microsoft.com/help/4466982)</span><span class="sxs-lookup"><span data-stu-id="68e1e-136">If these options don't work, you can try [Windows Defender Offline](https://support.microsoft.com/help/17466) or [Troubleshoot problems with detecting and removing malware](https://support.microsoft.com/help/4466982).</span></span>

## <a name="step-4-recover-files-on-a-cleaned-computer-or-device"></a><span data-ttu-id="68e1e-137">Étape 4 : Récupérer des fichiers sur un ordinateur ou un appareil nettoyé</span><span class="sxs-lookup"><span data-stu-id="68e1e-137">Step 4: Recover files on a cleaned computer or device</span></span>

<span data-ttu-id="68e1e-138">Une fois que vous avez terminé l’étape précédente pour supprimer la charge utile du ransomware de [](https://support.microsoft.com/help/17128) votre environnement (ce qui empêchera le ransomware de chiffrer ou de supprimer vos fichiers), vous pouvez utiliser l’historique des fichiers dans Windows 10 et Windows 8.1 ou la Protection système dans Windows 7 pour tenter de récupérer vos fichiers et dossiers locaux.</span><span class="sxs-lookup"><span data-stu-id="68e1e-138">After you've completed the previous step to remove the ransomware payload from your environment (which will prevent the ransomware from encrypting or removing your files), you can use [File History](https://support.microsoft.com/help/17128) in Windows 10 and Windows 8.1 or System Protection in Windows 7 to attempt to recover your local files and folders.</span></span>

<span data-ttu-id="68e1e-139">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="68e1e-139">**Notes**:</span></span>

- <span data-ttu-id="68e1e-140">Certains ransomware chiffrent ou suppriment également les versions de sauvegarde, vous ne pouvez donc pas utiliser l’historique des fichiers ou la Protection système pour restaurer des fichiers.</span><span class="sxs-lookup"><span data-stu-id="68e1e-140">Some ransomware will also encrypt or delete the backup versions, so you can't use File History or System Protection to restore files.</span></span> <span data-ttu-id="68e1e-141">Si cela se produit, vous devez utiliser des sauvegardes sur des lecteurs externes ou des appareils qui n’ont pas été affectés par le ransomware ou OneDrive, comme décrit dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="68e1e-141">If that happens, you need use backups on external drives or devices that were not affected by the ransomware or OneDrive as described in the next section.</span></span>

- <span data-ttu-id="68e1e-142">Si un dossier est synchronisé avec OneDrive et que vous n’utilisez pas la dernière version de Windows, l’utilisation de l’historique des fichiers peut être limitée.</span><span class="sxs-lookup"><span data-stu-id="68e1e-142">If a folder is synchronized to OneDrive and you aren't using the latest version of Windows, there might be some limitations using File History.</span></span>

## <a name="step-5-recover-your-files-in-your-onedrive-for-business"></a><span data-ttu-id="68e1e-143">Étape 5 : Récupérer vos fichiers dans votre OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="68e1e-143">Step 5: Recover your files in your OneDrive for Business</span></span>

<span data-ttu-id="68e1e-144">La restauration de fichiers dans OneDrive Entreprise vous permet de restaurer l’intégralité de votre OneDrive à un point antérieur dans le temps au cours des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="68e1e-144">Files Restore in OneDrive for Business allows you to restore your entire OneDrive to a previous point in time within the last 30 days.</span></span> <span data-ttu-id="68e1e-145">Pour plus d’informations, [voir Restaurer votre OneDrive.](https://support.microsoft.com/office/fa231298-759d-41cf-bcd0-25ac53eb8a15)</span><span class="sxs-lookup"><span data-stu-id="68e1e-145">For more information, see [Restore your OneDrive](https://support.microsoft.com/office/fa231298-759d-41cf-bcd0-25ac53eb8a15).</span></span>

## <a name="step-6-recover-deleted-email"></a><span data-ttu-id="68e1e-146">Étape 6 : Récupérer les messages supprimés</span><span class="sxs-lookup"><span data-stu-id="68e1e-146">Step 6: Recover deleted email</span></span>

<span data-ttu-id="68e1e-147">Dans les rares cas où le ransomware a supprimé tous vos messages électroniques, vous pouvez probablement récupérer les éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="68e1e-147">In the rare case that the ransomware deleted all your email, you can probably recover the deleted items.</span></span> <span data-ttu-id="68e1e-148">Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="68e1e-148">For more information, see:</span></span>

- [<span data-ttu-id="68e1e-149">Récupérer des messages supprimés dans la boîte aux lettres d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="68e1e-149">Recover deleted messages in a user's mailbox</span></span>](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-user-mailboxes/recover-deleted-messages)

- [<span data-ttu-id="68e1e-150">Récupérer des éléments supprimés dans Outlook pour Windows</span><span class="sxs-lookup"><span data-stu-id="68e1e-150">Recover deleted items in Outlook for Windows</span></span>](https://support.microsoft.com/office/49e81f3c-c8f4-4426-a0b9-c0fd751d48ce)

## <a name="step-7-re-enable-exchange-activesync-and-onedrive-sync"></a><span data-ttu-id="68e1e-151">Étape 7 : Ré-activer la synchronisation Exchange ActiveSync et OneDrive</span><span class="sxs-lookup"><span data-stu-id="68e1e-151">Step 7: Re-enable Exchange ActiveSync and OneDrive sync</span></span>

<span data-ttu-id="68e1e-152">Après avoir nettoyé vos ordinateurs et appareils et récupéré vos données, vous pouvez réactiver la synchronisation Exchange ActiveSync et OneDrive que vous avez précédemment désactivée à [l’étape 2.](#step-2-disable-exchange-activesync-and-onedrive-sync)</span><span class="sxs-lookup"><span data-stu-id="68e1e-152">After you've cleaned your computers and devices and recovered your data, you can re-enable Exchange ActiveSync and OneDrive sync that you previously disabled in [Step 2](#step-2-disable-exchange-activesync-and-onedrive-sync).</span></span>

## <a name="step-8-optional-block-onedrive-sync-for-specific-file-extensions"></a><span data-ttu-id="68e1e-153">Étape 8 (facultative) : bloquer la synchronisation OneDrive pour des extensions de fichier spécifiques</span><span class="sxs-lookup"><span data-stu-id="68e1e-153">Step 8 (Optional): Block OneDrive sync for specific file extensions</span></span>

<span data-ttu-id="68e1e-154">Une fois que vous avez récupéré, vous pouvez empêcher les clients OneDrive Entreprise de synchroniser les types de fichiers affectés par ce ransomware.</span><span class="sxs-lookup"><span data-stu-id="68e1e-154">After you've recovered, you can prevent OneDrive for Business clients from synchronizing the file types that were affected by this ransomware.</span></span> <span data-ttu-id="68e1e-155">Pour plus d’informations, [voir Set-SPOTenantSyncClientRestriction](https://docs.microsoft.com/powershell/module/sharepoint-online/set-spotenantsyncclientrestriction)</span><span class="sxs-lookup"><span data-stu-id="68e1e-155">For more information, see [Set-SPOTenantSyncClientRestriction](https://docs.microsoft.com/powershell/module/sharepoint-online/set-spotenantsyncclientrestriction)</span></span>

## <a name="report-the-attack"></a><span data-ttu-id="68e1e-156">Signaler l’attaque</span><span class="sxs-lookup"><span data-stu-id="68e1e-156">Report the attack</span></span>

### <a name="contact-law-enforcement"></a><span data-ttu-id="68e1e-157">Contacter l’application de la loi</span><span class="sxs-lookup"><span data-stu-id="68e1e-157">Contact law enforcement</span></span>

<span data-ttu-id="68e1e-158">Vous devez contacter vos autorités judiciaires locales ou fédérales.</span><span class="sxs-lookup"><span data-stu-id="68e1e-158">You should contact your local or federal law enforcement agencies.</span></span> <span data-ttu-id="68e1e-159">Par exemple, si vous êtes aux États-Unis, vous pouvez contacter le [bureau local DE LASV](https://www.fbi.gov/contact-us/field), [IC3](http://www.ic3.gov/complaint/default.aspx) ou [le service secret](http://www.secretservice.gov/).</span><span class="sxs-lookup"><span data-stu-id="68e1e-159">For example, if you are in the United States you can contact the [FBI local field office](https://www.fbi.gov/contact-us/field), [IC3](http://www.ic3.gov/complaint/default.aspx) or [Secret Service](http://www.secretservice.gov/).</span></span>

### <a name="submit-a-report-to-your-countrys-scam-reporting-website"></a><span data-ttu-id="68e1e-160">Envoyer un rapport sur le site web de signalement des fraudes de votre pays</span><span class="sxs-lookup"><span data-stu-id="68e1e-160">Submit a report to your country's scam reporting website</span></span>

<span data-ttu-id="68e1e-161">Les sites web de signalement des fraudes fournissent des informations sur la prévention et la prévention des fraudes.</span><span class="sxs-lookup"><span data-stu-id="68e1e-161">Scam reporting websites provide information about how to prevent and avoid scams.</span></span> <span data-ttu-id="68e1e-162">Ils fournissent également des mécanismes permettant de signaler si vous avez été victime d’une fraude.</span><span class="sxs-lookup"><span data-stu-id="68e1e-162">They also provide mechanisms to report if you were victim of scam.</span></span>

- <span data-ttu-id="68e1e-163">Australie : [SCAMwatch](http://www.scamwatch.gov.au/)</span><span class="sxs-lookup"><span data-stu-id="68e1e-163">Australia: [SCAMwatch](http://www.scamwatch.gov.au/)</span></span>

- <span data-ttu-id="68e1e-164">Canada : [Centre anti-fraude canadien](http://www.antifraudcentre-centreantifraude.ca/)</span><span class="sxs-lookup"><span data-stu-id="68e1e-164">Canada: [Canadian Anti-Fraud Centre](http://www.antifraudcentre-centreantifraude.ca/)</span></span>

- <span data-ttu-id="68e1e-165">France : [Agence nationale de la sécurité des systèmes d’information](http://www.ssi.gouv.fr/)</span><span class="sxs-lookup"><span data-stu-id="68e1e-165">France: [Agence nationale de la sécurité des systèmes d'information](http://www.ssi.gouv.fr/)</span></span>

- <span data-ttu-id="68e1e-166">Allemagne : [ContrôleAmt für Sicherheit in der Informationstechnik](https://www.bsi.bund.de/DE/Home/home_node.html)</span><span class="sxs-lookup"><span data-stu-id="68e1e-166">Germany: [Bundesamt für Sicherheit in der Informationstechnik](https://www.bsi.bund.de/DE/Home/home_node.html)</span></span>

- <span data-ttu-id="68e1e-167">Irlande : [An Síochána](http://www.garda.ie/)</span><span class="sxs-lookup"><span data-stu-id="68e1e-167">Ireland: [An Garda Síochána](http://www.garda.ie/)</span></span>

- <span data-ttu-id="68e1e-168">Nouvelle-Zélande : [fraudes de consommateur](http://www.consumeraffairs.govt.nz/scams)</span><span class="sxs-lookup"><span data-stu-id="68e1e-168">New Zealand: [Consumer Affairs Scams](http://www.consumeraffairs.govt.nz/scams)</span></span>

- <span data-ttu-id="68e1e-169">Royaume-Uni : fraude [d’action](http://www.actionfraud.police.uk/)</span><span class="sxs-lookup"><span data-stu-id="68e1e-169">United Kingdom: [Action Fraud](http://www.actionfraud.police.uk/)</span></span>

- <span data-ttu-id="68e1e-170">États-Unis : [Sur Guard Online](http://www.onguardonline.gov/)</span><span class="sxs-lookup"><span data-stu-id="68e1e-170">United States: [On Guard Online](http://www.onguardonline.gov/)</span></span>

<span data-ttu-id="68e1e-171">Si votre pays n’est pas répertorié, demandez à vos autorités judiciaires locales ou fédérales.</span><span class="sxs-lookup"><span data-stu-id="68e1e-171">If your country isn't listed, ask your local or federal law enforcement agencies.</span></span>

### <a name="submit-email-messages-to-microsoft"></a><span data-ttu-id="68e1e-172">Envoyer des messages électroniques à Microsoft</span><span class="sxs-lookup"><span data-stu-id="68e1e-172">Submit email messages to Microsoft</span></span>

<span data-ttu-id="68e1e-173">Vous pouvez signaler des messages de hameçonnage qui contiennent un ransomware à l’aide de l’une des différentes méthodes.</span><span class="sxs-lookup"><span data-stu-id="68e1e-173">You can report phishing messages that contain ransomware by using one of several methods.</span></span> <span data-ttu-id="68e1e-174">Pour plus d’informations, voir [Signaler des messages et des fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="68e1e-174">For more information, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="68e1e-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68e1e-175">See also</span></span>

- [<span data-ttu-id="68e1e-176">Ransomware</span><span class="sxs-lookup"><span data-stu-id="68e1e-176">Ransomware</span></span>](https://docs.microsoft.com/windows/security/threat-protection/intelligence/ransomware-malware)

- [<span data-ttu-id="68e1e-177">Réponse ransomware : payer ou ne pas payer ?</span><span class="sxs-lookup"><span data-stu-id="68e1e-177">Ransomware response—to pay or not to pay?</span></span>](https://www.microsoft.com/security/blog/2019/12/16/ransomware-response-to-pay-or-not-to-pay/)

- [<span data-ttu-id="68e1e-178">NorskQue répond aux attaques par ransomware avec transparence</span><span class="sxs-lookup"><span data-stu-id="68e1e-178">Norsk Hydro responds to ransomware attack with transparency</span></span>](https://www.microsoft.com/security/blog/2019/12/17/norsk-hydro-ransomware-attack-transparency/)

- [<span data-ttu-id="68e1e-179">Détection de ransomware et récupération de vos fichiers dans OneDrive</span><span class="sxs-lookup"><span data-stu-id="68e1e-179">Ransomware detection and recovering your files in OneDrive</span></span>](https://support.microsoft.com/office/0d90ec50-6bfd-40f4-acc7-b8c12c73637f)

- [<span data-ttu-id="68e1e-180">Rapport Microsoft Security Intelligence</span><span class="sxs-lookup"><span data-stu-id="68e1e-180">Microsoft Security Intelligence Report</span></span>](https://www.microsoft.com/securityinsights/)

- [<span data-ttu-id="68e1e-181">Activer ou désactiver des macros dans les fichiers Office</span><span class="sxs-lookup"><span data-stu-id="68e1e-181">Enable or disable macros in Office files</span></span>](https://support.microsoft.com/office/12b036fd-d140-4e74-b45e-16fed1a7e5c6)

- [<span data-ttu-id="68e1e-182">Paramètres recommandés pour EOP et Microsoft Defender pour la sécurité Office 365</span><span class="sxs-lookup"><span data-stu-id="68e1e-182">Recommended settings for EOP and Microsoft Defender for Office 365 security</span></span>](recommended-settings-for-eop-and-office365-atp.md)

- [<span data-ttu-id="68e1e-183">Une mise à niveau fiable : la sécurité de nouvelle génération sur Windows 10 prouve sa résilience contre les attaques de ransomware en 2017</span><span class="sxs-lookup"><span data-stu-id="68e1e-183">A worthy upgrade: Next-gen security on Windows 10 proves resilient against ransomware outbreaks in 2017</span></span>](https://www.microsoft.com/security/blog/2018/01/10/a-worthy-upgrade-next-gen-security-on-windows-10-proves-resilient-against-ransomware-outbreaks-in-2017/)

- [<span data-ttu-id="68e1e-184">No mas, Samas: What’s in this ransomware’s modus operandi?</span><span class="sxs-lookup"><span data-stu-id="68e1e-184">No mas, Samas: What's in this ransomware's modus operandi?</span></span>](https://www.microsoft.com/security/blog/2016/03/17/no-mas-samas-whats-in-this-ransomwares-modus-operandi/)

- [<span data-ttu-id="68e1e-185">Programmes malveillants verrouillés, afin de les éviter</span><span class="sxs-lookup"><span data-stu-id="68e1e-185">Locky malware, lucky to avoid it</span></span>](https://www.microsoft.com/security/blog/2016/02/24/locky-malware-lucky-to-avoid-it/)

- [<span data-ttu-id="68e1e-186">MSRT juillet 2016 : ransomware Cerber</span><span class="sxs-lookup"><span data-stu-id="68e1e-186">MSRT July 2016: Cerber ransomware</span></span>](https://www.microsoft.com/security/blog/2016/07/12/msrt-july-2016-cerber-ransomware/)

- [<span data-ttu-id="68e1e-187">Les trois têtes du ransomware Cerber de type Cerber</span><span class="sxs-lookup"><span data-stu-id="68e1e-187">The three heads of the Cerberus-like Cerber ransomware</span></span>](https://www.microsoft.com/security/blog/2016/03/09/the-three-heads-of-the-cerberus-like-cerber-ransomware/)

- [<span data-ttu-id="68e1e-188">Ransomware troldesh influencé par (le) code Da Postal</span><span class="sxs-lookup"><span data-stu-id="68e1e-188">Troldesh ransomware influenced by (the) Da Vinci code</span></span>](https://www.microsoft.com/security/blog/2016/07/13/troldesh-ransomware-influenced-by-the-da-vinci-code/)
