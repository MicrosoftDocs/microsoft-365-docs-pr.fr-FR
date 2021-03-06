---
title: Ce qu’incluent les modèles de stratégie DLP
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 6/29/2018
audience: Admin
ms.topic: reference
f1_keywords:
- ms.o365.cc.DLPNewPolicyFromTemplate
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.custom:
- seo-marvel-apr2020
recommendations: false
description: Découvrez ce que les modèles de stratégie de protection contre la perte de données (DLP) dans le Centre de sécurité & conformité Office 365 inclut.
ms.openlocfilehash: afcc641e6e868c1988f6b30a286c082e960d056c
ms.sourcegitcommit: 1206319a5d3fed8d52a2581b8beafc34ab064b1c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2021
ms.locfileid: "52086695"
---
# <a name="what-the-dlp-policy-templates-include"></a>Ce qu’incluent les modèles de stratégie DLP

La protection contre la perte de données (DLP) dans le Centre de conformité de sécurité inclut des modèles de stratégie prêts à l’emploi qui respectent les exigences de conformité courantes, telles que l’aide à la protection des informations sensibles soumises à la loi &amp; AMÉRICAINE HIPAA (Health Insurance Act), la loi AMÉRICAINE Gramm-Leach-Bliley Act (GLBA) ou le Patriot Act des États-Unis. Cette rubrique répertorie tous les modèles de stratégie, les types d’informations sensibles qu’ils recherchent et les conditions et actions par défaut. Elle ne comprend pas tous les détails de configuration de chaque modèle de stratégie, mais présente suffisamment d’informations pour vous aider à déterminer quel modèle est le meilleur point de départ pour votre cas. N’oubliez pas que vous pouvez personnaliser ces modèles de stratégie pour répondre à vos besoins spécifiques.
  
## <a name="australia-financial-data"></a>Données financières en Australie

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Données financières pour l’Australie : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Code SWIFT — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de dossier fiscal australien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire australien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Données financières pour l’Australie : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Code SWIFT — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de dossier fiscal australien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire australien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="australia-health-records-act-hrip-act"></a>Australia Health Records Act (HRIP Act)

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Loi HRIP australienne : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de dossier fiscal australien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de dossier médical australien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Loi HRIP australienne : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de dossier fiscal australien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de dossier médical australien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="australia-personally-identifiable-information-pii-data"></a>Australia Personally Identifiable Information (PII) Data

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|PII pour l’Australie : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de dossier fiscal australien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de permis de conduire australien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|PII pour l’Australie : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de dossier fiscal australien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de permis de conduire australien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="australia-privacy-act"></a>Australia Privacy Act

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Protection des données pour l’Australie : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de permis de conduire australien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de passeport australien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Protection des données pour l’Australie : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de permis de conduire australien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de passeport australien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="canada-financial-data"></a>Données financières au Canada

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Données financières pour le Canada : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire canadien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Données financières pour le Canada : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="canada-health-information-act-hia"></a>Canada Health Information Act (HIA)

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Loi HIA canadienne : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de passeport canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de service de santé canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Loi HIA canadienne : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de passeport canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de service de santé canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="canada-personal-health-act-phipa---ontario"></a>Canada Personal Health Act (PHIPA) - Ontario

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Loi LPRPS canadienne : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de passeport canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de service de santé canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Loi LPRPS canadienne : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de passeport canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de service de santé canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="canada-personal-health-information-act-phia---manitoba"></a>Canada Personal Health Information Act (PHIA) - Manitoba

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Loi LRMP canadienne : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de service de santé canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Loi LRMP canadienne : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de service de santé canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="canada-personal-information-protection-act-pipa"></a>Canada Personal Information Protection Act (PIPA)

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Loi PIPA canadienne : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de passeport canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de service de santé canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Loi PIPA canadienne : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de passeport canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de service de santé canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="canada-personal-information-protection-act-pipeda"></a>Canada Personal Information Protection and Electronic Documents Act (PIPEDA)

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Loi LPRPDE canadienne : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de permis de conduire canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de passeport canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de service de santé canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Loi LPRPDE canadienne : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de permis de conduire canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de passeport canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de service de santé canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="canada-personally-identifiable-information-pii-data"></a>Canada Personally Identifiable Information (PII) Data

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|PII pour le Canada : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de permis de conduire canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de passeport canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de service de santé canadien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|PII pour le Canada : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de permis de conduire canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de passeport canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale du Canada — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de service de santé canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro d’identification médical personnel (PHIN) canadien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="france-data-protection-act"></a>Loi informatique et liberté en France

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Loi sur la protection des données pour la France : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Carte nationale d’identité (CNI) française — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale (INSEE) français — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Loi sur la protection des données pour la France : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Carte nationale d’identité (CNI) française — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale (INSEE) français — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="france-financial-data"></a>Données financières en France

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Données financières pour la France : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de carte de crédit de l’U.E. — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Données financières pour la France : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de carte de crédit de l’U.E. — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="france-personally-identifiable-information-pii-data"></a>France Personally Identifiable Information (PII) Data

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|PII pour la France : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de sécurité sociale (INSEE) français — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de permis de conduire français — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de passeport français — Nombre minimal 1, nombre maximal 9  <br/>  Carte nationale d’identité (CNI) française — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|PII pour la France : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de sécurité sociale (INSEE) français — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de permis de conduire français — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de passeport français — Nombre minimal 10, nombre maximal « tout »  <br/>  Carte nationale d’identité (CNI) française — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="general-data-protection-regulation-gdpr"></a>Règlement général sur la protection des données (RGPD)

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Contenu sensible de l’UE à faible volume trouvé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit de l’U.E. — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de permis de conduire de l’UE — Nombre minimum 1, nombre maximum 9  <br/>  Numéro d’identification national de l’UE — Nombre minimum 1, nombre maximum 9  <br/>  Numéro de passeport de l’UE — Nombre minimum 1, nombre maximum 9  <br/>  Numéro de sécurité sociale de l’UE (SSN) ou ID équivalent — Nombre minimum 1, nombre maximum 9  <br/>  Numéro d’identification fiscale de l’UE —Nombre minimum 1, nombre max 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer des rapports d’incident à l’administrateur  <br/> |
|Volume élevé de contenu sensible de l’UE trouvé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit de l’U.E. — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de permis de conduire de l’UE — Nombre minimum 1, nombre maximum 9  <br/>  Numéro d’identification national de l’UE — Nombre minimum 1, nombre maximum 9  <br/>  Numéro de passeport de l’UE — Nombre minimum 1, nombre maximum 9  <br/>  Numéro de sécurité sociale de l’UE (SSN) ou ID équivalent — Nombre minimum 1, nombre maximum 9  <br/>  Numéro d’identification fiscale de l’UE —Nombre minimum 1, nombre max 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Restreindre l’accès au contenu pour utilisateurs externe  <br/>  Informer les utilisateurs à l’aide de courriers électroniques et de conseils de stratégie  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer des rapports d’incident à l’administrateur  <br/> |
   
## <a name="germany-financial-data"></a>Données financières en Allemagne

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Données financières pour l’Allemagne : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de carte de crédit de l’U.E. — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Données financières pour l’Allemagne : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de carte de crédit de l’U.E. — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="germany-personally-identifiable-information-pii-data"></a>Germany Personally Identifiable Information (PII) Data

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|PII pour l’Allemagne : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de permis de conduire allemand — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de passeport allemand — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|PII pour l’Allemagne : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de permis de conduire allemand — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de passeport allemand — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="israel-financial-data"></a>Données financières en Israël

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Données financières pour Israël : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de compte bancaire israélien — Nombre minimal 1, nombre maximal 9  <br/>  Code SWIFT — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Données financières pour Israël : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de compte bancaire israélien — Nombre minimal 10, nombre maximal « tout »  <br/>  Code SWIFT — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="israel-personally-identifiable-information-pii-data"></a>Israel Personally Identifiable Information (PII) Data

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|PII pour Israël : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  ID national israélien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|PII pour Israël : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  ID national israélien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="israel-protection-of-privacy"></a>Israel Protection of Privacy

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Protection des données pour Israël : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  ID national israélien — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire israélien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Protection des données pour Israël : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  ID national israélien — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire israélien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="japan-financial-data"></a>Données financières au Japon

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Données financières pour le Japon : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de compte bancaire japonais — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Données financières pour le Japon : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de compte bancaire japonais — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="japan-personally-identifiable-information-pii-data"></a>Japan Personally Identifiable Information (PII) Data

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|PII pour le Japon : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’enregistrement de résident japonais — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale japonaise (SIN) — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|PII pour le Japon : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’enregistrement de résident japonais — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale japonaise (SIN) — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="japan-protection-of-personal-information"></a>Japan Protection of Personal Information

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Loi PPI pour le Japon : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’enregistrement de résident japonais — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale japonaise (SIN) — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Loi PPI pour le Japon : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’enregistrement de résident japonais — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale japonaise (SIN) — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="pci-data-security-standard-pci-dss"></a>PCI Data Security Standard (PCI DSS)

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Norme PCI DSS : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Norme PCI DSS : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="saudi-arabia---anti-cyber-crime-law"></a>Saudi Arabia - Anti-Cyber Crime Law

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|ACC pour l’Arabie Saoudite : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Code SWIFT — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire international (IBAN) — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|ACC pour l’Arabie Saoudite : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Code SWIFT — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire international (IBAN) — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="saudi-arabia-financial-data"></a>Données financières en Arabie Saoudite

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Données financières pour l’Arabie Saoudite : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Code SWIFT — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire international (IBAN) — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Données financières pour l’Arabie Saoudite : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Code SWIFT — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire international (IBAN) — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="saudi-arabia-personally-identifiable-information-pii-data"></a>Saudi Arabia Personally Identifiable Information (PII) Data

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|PII pour l’Arabie Saoudite : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  ID national saoudien — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|PII pour l’Arabie Saoudite : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  ID national saoudien — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="uk-access-to-medical-reports-act"></a>U.K. Access to Medical Reports Act

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Loi AMRA pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro du service de santé national (NHS) du Royaume-Uni — Nombre minimal 1, nombre maximal 9  <br/>  Numéro d’assurance national (NINO) du Royaume-Uni — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Loi AMRA pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro du service de santé national (NHS) du Royaume-Uni — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro d’assurance national (NINO) du Royaume-Uni — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="uk-data-protection-act"></a>U.K. Data Protection Act

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|DPA pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’assurance national (NINO) du Royaume-Uni — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de passeport des États-Unis/du Royaume-Uni — Nombre minimal 1, nombre maximal 9  <br/>  Code SWIFT — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|DPA pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’assurance national (NINO) du Royaume-Uni — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de passeport des États-Unis/du Royaume-Uni — Nombre minimal 10, nombre maximal « tout »  <br/>  Code SWIFT — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="uk-financial-data"></a>Données financières R.U.

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Données financières pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de carte de crédit de l’U.E. — Nombre minimal 1, nombre maximal 9  <br/>  Code SWIFT — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Données financières pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de carte de crédit de l’U.E. — Nombre minimal 10, nombre maximal « tout »  <br/>  Code SWIFT — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="uk-personal-information-online-code-of-practice-piocp"></a>U.K. Personal Information Online Code of Practice (PIOCP)

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|PIOCP pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’assurance national (NINO) du Royaume-Uni — Nombre minimal 1, nombre maximal 9  <br/>  Numéro du service de santé national (NHS) du Royaume-Uni — Nombre minimal 1, nombre maximal 9  <br/>  Code SWIFT — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|PIOCP pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’assurance national (NINO) du Royaume-Uni — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro du service de santé national (NHS) du Royaume-Uni — Nombre minimal 10, nombre maximal « tout »  <br/>  Code SWIFT — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="uk-personally-identifiable-information-pii-data"></a>U.K. Personally Identifiable Information (PII) Data

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|PII pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’assurance national (NINO) du Royaume-Uni — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de passeport des États-Unis/du Royaume-Uni — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|PII pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’assurance national (NINO) du Royaume-Uni — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de passeport des États-Unis/du Royaume-Uni — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="uk-privacy-and-electronic-communications-regulations"></a>U.K. Privacy and Electronic Communications Regulations

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|PECR pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Code SWIFT — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|PECR pour le Royaume-Uni : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Code SWIFT — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="us-federal-trade-commission-ftc-consumer-rules"></a>U.S. Federal Trade Commission (FTC) Consumer Rules

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Règles de protection des consommateurs du FTC pour les États-Unis : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Numéro d’acheminement ABA — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Règles de protection des consommateurs du FTC pour les États-Unis : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro d’acheminement ABA — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="us-financial-data"></a>Données financières US

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Données financières pour les États-Unis : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Numéro d’acheminement ABA — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Données financières pour les États-Unis : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro d’acheminement ABA — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="us-gramm-leach-bliley-act-glba"></a>U.S. Gramm-Leach-Bliley Act (GLBA)

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Loi GLBA américaine : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Numéro d’identification du contribuable individuel (ITIN) des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale (N° S.S.) des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Loi GLBA américaine : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro d’identification du contribuable individuel (ITIN) des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale (N° S.S.) des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="us-health-insurance-act-hipaa"></a>U.S. Health Insurance Act (HIPAA)

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Le contenu correspond à la loi AMÉRICAINE HIPAA  <br/> | Contient l’une des informations sensibles suivantes :  <br/>  Numéro de sécurité sociale (SSN) des États-Unis — Nombre minimum 1, nombre maximum « tout »  <br/>  Numéro de la Drug Enforcement Agency (DEA) — Nombre minimum 1, nombre max « tout »  <br/> **ET** <br/>  Le contenu contient l’un des termes ci-après :  <br/>  Classification internationale des maladie (ICD-9-CM) — Nombre minimum 1, nombre maximum « tout »  <br/>  Classification internationale des maladie (ICD-10-CM) — Nombre minimum 1, nombre maximum « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
   
## <a name="us-patriot-act"></a>U.S. Patriot Act

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Loi USA Patriot Act américaine : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Numéro d’identification du contribuable individuel (ITIN) des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale (N° S.S.) des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Loi USA Patriot Act américaine : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro d’identification du contribuable individuel (ITIN) des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale (N° S.S.) des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="us-personally-identifiable-information-pii-data"></a>U.S. Personally Identifiable Information (PII) Data

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|PII pour les États-Unis : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’identification du contribuable individuel (ITIN) des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale (N° S.S.) des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de passeport des États-Unis/du Royaume-Uni — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|PII pour les États-Unis : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro d’identification du contribuable individuel (ITIN) des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale (N° S.S.) des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de passeport des États-Unis/du Royaume-Uni — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="us-state-breach-notification-laws"></a>U.S. State Breach Notification Laws

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Lois américaines sur les violations de la sécurité : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de compte bancaire des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de permis de conduire des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Numéro de sécurité sociale (N° S.S.) des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Lois américaines sur les violations de la sécurité : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de carte de crédit — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de compte bancaire des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de permis de conduire des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Numéro de sécurité sociale (N° S.S.) des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   
## <a name="us-state-social-security-number-confidentiality-laws"></a>U.S. State Social Security Number Confidentiality Laws

|**Nom de la règle**|**Conditions  <br/> (y compris les types d’informations sensibles)**|**Actions**|
|:-----|:-----|:-----|
|Lois SSN américaines : analyser le contenu partagé hors de l’organisation - faible nombre  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de sécurité sociale (N° S.S.) des États-Unis — Nombre minimal 1, nombre maximal 9  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> |Envoyer une notification  <br/> |
|Lois SSN américaines : analyser le contenu partagé hors de l’organisation - nombre élevé  <br/> | Le contenu contient des informations sensibles :  <br/>  Numéro de sécurité sociale (N° S.S.) des États-Unis — Nombre minimal 10, nombre maximal « tout »  <br/>  Le contenu est partagé avec :  <br/>  Des personnes extérieures à mon organisation  <br/> | Bloquer l’accès au contenu  <br/>  Envoyer une notification  <br/>  Autoriser le remplacement  <br/>  Exiger une justification professionnelle  <br/>  Envoyer un rapport d’incident  <br/> |
   

