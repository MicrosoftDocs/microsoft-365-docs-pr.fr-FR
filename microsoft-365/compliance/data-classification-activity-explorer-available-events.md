---
title: Actions d'étiquetage signalées dans l'Explorateur d'activités
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
- m365solution-mip
- m365initiative-compliance
search.appverid:
- MOE150
- MET150
description: liste des activités d’étiquetage disponibles dans l’Explorateur d’activités.
ms.openlocfilehash: d4f6884ad39b16aeb0345f0c976d6ad87f03c05a
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52532253"
---
# <a name="labeling-activities-that-are-available-in-activity-explorer"></a>Activités d’étiquetage disponibles dans l’Explorateur d’activités

## <a name="sensitivity-label-applied"></a>Étiquette de niveau de sensibilité appliquée

Cet événement est généré chaque fois qu’un document non étiqueté est étiqueté ou qu’un message électronique est envoyé avec une étiquette de sensibilité. 

- Elle est capturée au moment de l’Office applications natives et web. 
- Elle est capturée au moment de l’occurrence dans les modules complémentaires Azure Information Protection. 
- Les actions de mise à niveau et de rétrogradation des étiquettes peuvent également être surveillées via le champ et le filtre du type d’événement *Label.*   


|Source  |Signalé dans l’Explorateur d’activités | Remarque  |
|---------|---------|---------|
| Word, Excel, PowerPoint|oui |
|Outlook| oui |à partir de Win 32 |
|SharePoint en ligne, OneDrive|oui | |
|Exchange        |oui         | |
|Client unifié Azure Information Protection (AIP) et scanneur unifié AIP |oui |l’action nouvelle *étiquette* AIP est mappée sur l’étiquette *appliquée dans* l’Explorateur d’activités   |
|Microsoft information protection (MIP) SDK         |oui|l’action nouvelle *étiquette* AIP est mappée sur l’étiquette *appliquée dans* l’Explorateur d’activités|
|Rights Management Service (RMS)         |non applicable         | |
|Power BI bureau et web        | non| accessibles dans les journaux Microsoft 365 audit         |
|Microsoft Cloud App Security (MCAS)         |non|         |

## <a name="sensitivity-label-changed"></a>Étiquette de sensibilité modifiée

Cet événement est généré chaque fois qu’une étiquette de niveau de sensibilité est mise à jour sur le document ou l’e-mail.

- Pour les sources du client unifié AIP, de l’analyseur unifié et du SDK MIP, l’étiquette de mise à niveau *AIP* et l’action de *rétrogradation* des étiquettes sont mises en relation avec l’étiquette de l’explorateur *d’activités modifiée.*

- Elle est capturée au moment de l’Office applications natives et web. 
- Elle est capturée au moment de l’occurrence dans les application de scanneurs et les add-ins client unifiés Azure Information Protection
- Les actions de mise à niveau et de rétrogradation des étiquettes peuvent également être surveillées via le champ et le filtre du type d’événement *Label.* Le *texte de justification* est également capturé à l’exception de SharePoint Online et OneDrive.
- L’étiquetage de la sensibilité effectué dans Office applications natives sur Outlook collecte la dernière action générée avant les actions d’envoi d’e-mail/d’enregistrer des fichiers. Par exemple, si l’utilisateur modifie plusieurs fois l’étiquette d’un e-mail avant de l’envoyer, la dernière étiquette trouvée dans l’e-mail lors de son envoi est capturée dans le journal d’audit, puis signalée dans l’Explorateur d’activités. 


|Source  |Signalé dans l’Explorateur d’activités|Remarque  |
|---------|---------|---------| 
|Word, Excel, PowerPoint         |oui         |
|Outlook         |oui         |Win 32|
|SharePoint En ligne, OneDrive         |oui         |
|Exchange         |oui         |
|Client unifié AIP         |oui         |
|Scanneur unifié AIP         |oui         |
|MIP SDK         |oui         |
|Service RMS         |non applicable         |
|Power BI bureau et Web         |non         |accessibles dans les journaux Microsoft 365 audit |
|MCAS     |non         |         |

## <a name="sensitivity-label-removed"></a>Étiquette de sensibilité supprimée

Cet événement est généré chaque fois qu’une étiquette de niveau de sensibilité est supprimée d’un fichier ou d’un document.

- Cet événement est capturé au moment de l’Office applications natives et web.
- Elle est capturée au moment de l’occurrence dans les modules complémentaires Azure Information Protection. 
- L’étiquetage de la sensibilité, avec Office d’étiquette MIP native, sur Outlook collecte le dernier événement d’étiquetage généré avant les actions d’envoi d’e-mail/d’enregistrer un fichier.

|Source  |Signalé dans l’Explorateur d’activités | Remarque  |
|---------|---------|---------| 
|Word, Excel, PowerPoint         |oui         |
|Outlook         |oui         |Win 32|
|SharePoint En ligne, OneDrive         |oui         |
|Exchange         |oui         |
|Client unifié AIP         |oui         |L’action supprimer *l’étiquette* AIP est mappée sur *l’action* supprimée d’étiquette dans l’Explorateur d’activités|
|Scanneur unifié AIP         |oui         |L’action supprimer *l’étiquette* AIP est mappée sur *l’action* supprimée d’étiquette dans l’Explorateur d’activités |
|MIP SDK         |oui         |L’action supprimer *l’étiquette* AIP est mappée sur *l’action* supprimée d’étiquette dans l’Explorateur d’activités |
|Service RMS         |non applicable         |
|Power BI bureau et Web         |non         |accessibles dans les journaux Microsoft 365 audit |
|MCAS     |non         |         |
 

## <a name="sensitivity-label-file-read"></a>Fichier d’étiquette de niveau de sensibilité lu

Cet événement est généré chaque fois qu’un document protégé ou étiqueté de sensibilité est ouvert.

|Source  |Signalé dans l’Explorateur d’activités | Remarque  |
|---------|---------|---------| 
|Word, Excel, PowerPoint         |oui         |
|Outlook         |non         |
|SharePoint En ligne, OneDrive         |non         |
|Exchange         |non         |
|Client unifié AIP         |oui         |l’action *d’accès* AIP est mappée à l’action *de lecture de* fichier dans l’Explorateur d’activités|
|Scanneur unifié AIP         |oui         |l’action *d’accès* AIP est mappée à l’action *de lecture de* fichier dans l’Explorateur d’activités|
|MIP SDK         |oui         |l’action *d’accès* AIP est mappée à l’action *de lecture de* fichier dans l’Explorateur d’activités|
|Service RMS         |oui         |*l’action d’accès* est mappée à l’action *de lecture de* fichier dans l’Explorateur d’activités |
|Power BI bureau et Web         |non         |accessible dans les journaux Microsoft 365 audit |
|MCAS     |non         |         |


## <a name="files-discovered"></a>Fichiers découverts

Cet événement est généré chaque fois que des fichiers sont détectés lorsque le scanneur AIP est utilisé pour analyser des données sensibles à différents emplacements et trouve des fichiers.

|Source  |Signalé dans l’Explorateur d’activités | Remarque  |
|---------|---------|---------| 
|Word, Excel, PowerPoint         |non applicable         |
|Outlook         |non applicable         |
|SharePoint En ligne, OneDrive         |non applicable         |
|Exchange         |non applicable         |
|Client unifié AIP         |non applicable       |
|Scanneur unifié AIP         |oui         |l’action de *découverte* AIP est mappée sur les *fichiers détectés* dans l’Explorateur d’activités|
|MIP SDK         |oui         |L’action de *découverte* AIP est mappée sur l’action *de fichier découverte* dans l’Explorateur d’activités|
|Service RMS         |non applicable         |
|Power BI bureau et Web         |non applicable         |
|MCAS     |non applicable         |         |


## <a name="sensitivity-label-file-renamed"></a>Fichier d’étiquette de sensibilité renommé

Cet événement est généré chaque fois qu’un document avec une étiquette de sensibilité est renommé. 

|Source  | Signalé dans l’Explorateur d’activités | Remarque  |
|---------|---------|---------| 
|Word, Excel, PowerPoint         |oui         |
|Outlook         |non applicable         |
|SharePoint En ligne, OneDrive         |non        |
|Exchange         |non applicable         |
|Client unifié AIP         |non         |
|Scanneur unifié AIP         |non         |
|MIP SDK         |non         |
|Service RMS         |non      |
|Power BI bureau et Web         |non         |
|MCAS     |non         |         |


## <a name="file-removed"></a>Fichier supprimé

Cet événement est généré chaque fois que le scanneur AIP détecte qu’un fichier précédemment analysé a été supprimé.

|Source  |Signalé dans l’Explorateur d’activités | Remarque  |
|---------|---------|---------| 
|Word, Excel, PowerPoint         |non applicable         |
|Outlook         |non applicable         |
|SharePoint En ligne, OneDrive         |non applicable           |
|Exchange         |non applicable         |
|Client unifié AIP         |non applicable            |
|Scanneur unifié AIP         |oui         |
|MIP SDK         |non applicable            |
|Service RMS         |non applicable         |
|Power BI bureau et Web         |non applicable  |
|MCAS     |non applicable        |         |

### <a name="protection-applied"></a>Protection appliquée

Cet événement est généré la première fois que la protection est ajoutée manuellement à un élément qui n’a pas d’étiquette.

|Source  |Signalé dans l’Explorateur d’activités | Remarque  |
|---------|---------|---------| 
|Word, Excel, PowerPoint         |non         |
|Outlook         |non         |
|SharePoint En ligne, OneDrive         |non applicable           |
|Exchange         |non       |
|Client unifié AIP         |oui            |
|Scanneur unifié AIP         |non applicable         |
|MIP SDK         |oui            |
|Service RMS         |non applicable         |
|Power BI bureau et Web         |non applicable            |
|MCAS     |non applicable        |         |

## <a name="protection-changed"></a>Protection modifiée

Cet événement est généré chaque fois que la protection sur un document non marqué est modifiée manuellement.

|Source  |Signalé dans l’Explorateur d’activités |
|---------|---------| 
|Word, Excel, PowerPoint         |non         |
|Outlook         |non         |
|SharePoint En ligne, OneDrive         |non applicable           |
|Exchange         |non       |
|Client unifié AIP         |oui            |
|Scanneur unifié AIP         |non applicable         |
|MIP SDK         |oui            |
|Service RMS         |non applicable         |
|Power BI bureau et Web         |non applicable            |
|MCAS     |non applicable        |

## <a name="protection-removed"></a>Protection supprimée

Cet événement est généré chaque fois que la protection sur un document non marqué est modifiée manuellement.

|Source  |Signalé dans l’Explorateur d’activités |
|---------|---------| 
|Word, Excel, PowerPoint         |non         |
|Outlook         |non         |
|SharePoint En ligne, OneDrive         |non applicable           |
|Exchange         |non       |
|Client unifié AIP         |oui            |
|Scanneur unifié AIP         |non applicable         |
|MIP SDK         |oui            |
|Service RMS         |non applicable         |
|Power BI bureau et Web         |non applicable            |
|MCAS     |non applicable        |

## <a name="dlp-policy-matched"></a>Stratégie DLP en correspondance

Cet événement est généré chaque fois qu’une stratégie DLP est en correspondance sur un document ou un e-mail.

|Source  |Signalé dans l’Explorateur d’activités |
|---------|---------| 
|Exchange         |oui       |
|SharePoint Online|oui          |
|OneDrive |oui|
|Teams |oui   |
|Appareils Windows 10         |oui |
|MAC         |non     |
|local         |non|
|MCAS     |non        | 

Les événements pour Windows 10 périphériques de terminaison (DLP de point de terminaison) sont les :

- fichier supprimé
- fichier créé
- Fichier copié dans le Presse-papiers
- fichier modifié
- lecture de fichier
- fichier imprimé
- fichier renommé
- fichier copié sur le partage réseau
- fichier accessible par une application non autorisé


## <a name="retention-label-applied"></a>Étiquette de rétention appliquée 

Cet événement est généré chaque fois qu’un document non étiqueté est étiqueté ou qu’un message électronique est envoyé avec une étiquette de rétention.

- Elle est capturée au moment de l’enregistrer pour un document et au moment de l’envoi d’un e-mail.

|Source  |Signalé dans l’Explorateur d’activités |
|---------|---------| 
|Exchange         |non       |
|SharePoint Online|oui          |
|OneDrive |oui|

## <a name="retention-label-changed"></a>Étiquette de rétention modifiée

Cet événement est généré chaque fois qu’une étiquette est mise à jour sur un document ou un e-mail.

- Elle est capturée au moment de l’enregistrer pour un document et au moment de l’envoi d’un e-mail.

|Source  |Signalé dans l’Explorateur d’activités |
|---------|---------| 
|Exchange         |non       |
|SharePoint Online|oui          |
|OneDrive |oui|
 
## <a name="retention-label-removed"></a>Étiquette de rétention supprimée

Cet événement est généré chaque fois qu’une étiquette est supprimée d’un fichier ou d’un document.

- Elle est capturée au moment de l’enregistrer pour un document et au moment de l’envoi d’un e-mail.

|Source  |Signalé dans l’Explorateur d’activités |
|---------|---------| 
|Exchange         |non       |
|SharePoint Online|oui          |
|OneDrive |oui|


## <a name="known-issues"></a>Problèmes connus
  
- Lorsque l’info-conseil d’outil d’étiquette recommandée est affichée à un utilisateur final, elle n’est pas capturée. Toutefois, si l’utilisateur choisit d’appliquer l’étiquette recommandée, l’étiquette s’affiche sous le champ Comment *appliquer* comme *recommandé*  

- Le texte de justification n’est actuellement pas disponible lors de la rétrogradation des étiquettes de niveau de sensibilité à partir de SharePoint et OneDrive.  

- Les types d’informations sensibles ne sont actuellement pas disponibles pour les activités d’élisage automatique à partir de Word, Excel, PowerPoint et Outlook, ainsi que de SharePoint Online et OneDrive.
