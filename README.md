<div align="center">

# Réponse à incident cyber — AtlasGrid

### Étude de cas de gestion de crise : enquêter, décider, restaurer

**Exercice KASBAH · Scénario fictif MIRAGE · Dossier de réponse à incident**

[Commencer la lecture](#-commencer-ici) · [Voir la chronologie](dossier_incident/chronologie/MEMOIRE_INCIDENT_MIRAGE.md) · [Consulter les livrables](livrables_jury/README.md)

</div>

> [!IMPORTANT]
> **Dossier pédagogique fictif.** AtlasGrid, MIRAGE, SIROCCO et les événements décrits sont imaginaires. Ce dépôt présente une démarche de gestion de crise cyber : qualification des signaux, investigation, décision, continuité d'activité et reprise contrôlée.

---

## Qu'est-ce que ce projet ?

Ce dépôt est la restitution d'un **jeu sérieux de simulation de crise cyber**, nommé **KASBAH**. Vous incarnez une cellule de crise d'AtlasGrid confrontée au rançongiciel fictif **MIRAGE**. Au fil de messages, de journaux techniques et de décisions à prendre, l'objectif n'est pas seulement de « trouver le coupable » : il faut apprendre à **raisonner avec des éléments incomplets**, protéger l'entreprise et justifier chaque choix.

Le challenge consiste à :

- distinguer une **preuve** d'une **fausse piste** ou d'un simple **bruit** ;
- reconstituer une chronologie défendable, pièce par pièce ;
- arbitrer sous pression : isolement, communication, notification, sauvegardes, rançon et reprise ;
- produire des livrables compréhensibles par une direction, un client, un assureur ou un jury.

> **Ce que démontre ce dépôt :** une méthode de réponse à incident qui associe analyse technique, continuité d'activité, communication de crise et gouvernance.

## Les trois actes du jeu

| Acte | Ce qui se joue | Ce que la cellule doit accomplir | Accès direct |
| --- | --- | --- | --- |
| **I · Signaux faibles** | Alertes isolées, courriel suspect, plaintes d'utilisateurs : rien n'est encore certain. | Cartographier les actifs, qualifier les premiers signaux et séparer le fait du bruit. | [Explorer l'acte I](dossier_incident/chronologie/GALERIE_CAPTURES.md#1-acte-i--signaux-faibles-et-premières-qualifications) |
| **II · L'ultimatum** | Les serveurs sont chiffrés, une rançon est demandée et la pression monte. | Mesurer l'impact, établir la chaîne technique et décider sans céder aux rumeurs ni à la précipitation. | [Explorer l'acte II](dossier_incident/chronologie/GALERIE_CAPTURES.md#2-acte-ii--ransomware-propagation-et-reconstitution-technique) |
| **III · Reconstruire** | L'incident est contenu ; il faut remettre l'activité sur pied et rendre des comptes. | Choisir une sauvegarde saine, restaurer par priorités, rouvrir progressivement et préparer le plan 30/60/90 jours. | [Explorer l'acte III](dossier_incident/chronologie/GALERIE_CAPTURES.md#5-acte-iii--reconstruction-et-reprise) |

## Résumé du scénario

Un compte prestataire partagé, `svc_oasisnet`, est utilisé de nuit en dehors de son profil habituel. Une règle réseau temporaire est créée, puis des données sont transférées vers une destination externe. Les sauvegardes en ligne sont ensuite dégradées avant que le poste FIN-112 ne serve de point de départ au chiffrement MIRAGE. La cellule isole l'environnement, rejette la rançon, choisit une copie air-gap à Settat et rétablit d'abord le cœur ERP avant de rouvrir les services clients par paliers.

La [mémoire de crise](dossier_incident/chronologie/MEMOIRE_INCIDENT_MIRAGE.md) raconte ce déroulé dans son intégralité, avec les faits confirmés et les limites à ne pas dépasser.

## Navigation rapide

| Pour… | Ouvrir… |
| --- | --- |
| Découvrir le scénario sans jargon | [Mémoire de crise](dossier_incident/chronologie/MEMOIRE_INCIDENT_MIRAGE.md) |
| Suivre les événements dans l'ordre | [Chronologie complète](dossier_incident/chronologie/FICHE_CHRONOLOGIE_COMPLETE.md) |
| Examiner chaque capture et qualification | [Galerie des captures](dossier_incident/chronologie/GALERIE_CAPTURES.md) |
| Comprendre ce qui a été retenu ou écarté | [Preuves, fausses pistes et bruits](dossier_incident/triage/) |
| Lire les arbitrages de la cellule | [Registre des décisions](dossier_incident/decisions/) |
| Présenter le travail à un jury ou une direction | [Livrables PDF](livrables_jury/README.md) |

## L'incident en bref

| Ce qui s'est passé | Ce que la cellule a fait |
| --- | --- |
| Le rançongiciel **MIRAGE** a chiffré 23 des 40 serveurs d'AtlasGrid, dont l'ERP, la paie, la facturation et les partages de fichiers. | La cellule a isolé le périmètre, préservé les traces et recherché la cause sans confondre les faits avec les rumeurs. |
| Un compte prestataire utilisé hors de son profil habituel, une sortie réseau anormale et des sauvegardes en ligne dégradées ont formé la chaîne d'incident. | Elle a refusé de payer, choisi la copie déconnectée de Settat et rétabli l'ERP avant les autres services. |
| Des alertes concurrentes ont compliqué l'analyse. | Chaque élément a été classé comme **preuve**, **fausse piste** ou **bruit**, avec une justification vérifiable. |

<div align="center">

**Résultat : 12 décisions majeures tracées · reprise encadrée par paliers · dossier conçu pour être auditable**

</div>

## Commencer ici

Ce dépôt se lit comme un dossier d'incident, pas comme une documentation technique. Choisissez votre point d'entrée :

<table>
  <tr>
    <td width="33%" valign="top">
      <h3>1. Découvrir</h3>
      <p>Pour comprendre l'histoire sans jargon.</p>
      <a href="dossier_incident/chronologie/MEMOIRE_INCIDENT_MIRAGE.md"><strong>Lire le récit de l'incident</strong></a>
    </td>
    <td width="33%" valign="top">
      <h3>2. Vérifier</h3>
      <p>Pour suivre les faits et leurs sources.</p>
      <a href="dossier_incident/chronologie/FICHE_CHRONOLOGIE_COMPLETE.md"><strong>Ouvrir la chronologie sourcée</strong></a>
    </td>
    <td width="33%" valign="top">
      <h3>3. Restituer</h3>
      <p>Pour préparer un jury ou une direction.</p>
      <a href="livrables_jury/README.md"><strong>Accéder aux livrables PDF</strong></a>
    </td>
  </tr>
</table>

Pour un premier passage complet, le [guide du jury](GUIDE_DU_JURY.md) donne le vocabulaire, le parcours recommandé et les attentes de lecture.

## La chaîne d'incident établie

Cette vue présente la chaîne sous la forme d'un **parcours de preuves** : chaque étape indique le fait retenu, son effet et les pièces qui le soutiennent. Elle se lit de haut en bas.

| Étape | Acte | Fait retenu | Effet sur l'incident | Pièces associées |
| --- | --- | --- | --- | --- |
| Point à confirmer | I | Le rapport OasisNet décrit une compromission possible de sa console d'infogérance à J-42. | Cette information éclaire l'origine possible du compte partagé, sans établir tout le périmètre côté prestataire. | [A-08](dossier_incident/preuves/36_A08_rapport_preliminaire_OasisNet.md) |
| 1. Accès anormal | I | `svc_oasisnet` ouvre des sessions VPN nocturnes, sans MFA et hors de son profil habituel. | Le compte prestataire devient le point d'accès anormal central de l'enquête. | [A-02](dossier_incident/preuves/04_A02_VPN_svc_oasisnet_anormal.md) · [A-10](dossier_incident/preuves/13_A10_SIEM_acces_svc_oasisnet.md) |
| 2. Préparation de la sortie | II | Une règle `OUT-TEMP-443` est créée sur FIN-112, sans journalisation. | Une communication sortante non contrôlée devient possible. | [A-09](dossier_incident/preuves/10_A09_regle_firewall_C2.md) |
| 3. Transferts sortants | II | FIN-112 puis FILER-RBT transfèrent 117,8 Go sur dix nuits vers la même destination externe. | L'exfiltration est objectivée ; le volume et le contenu exact restent distincts. | [A-03](dossier_incident/preuves/14_A03_proxy_exfiltration_117_8Go.md) |
| 4. Sabotage de la reprise | II | La rétention est modifiée et les sauvegardes en ligne récentes deviennent inutilisables. | Les options de restauration rapide sont dégradées avant le chiffrement. | [A-05](dossier_incident/preuves/08_A05_sauvegardes_modifiees_indisponibles.md) |
| 5. Chiffrement MIRAGE | II | `svhost32.exe` s'exécute sur FIN-112 ; Defender est neutralisé, les fichiers sont chiffrés et les mécanismes de récupération supprimés. | FIN-112 est établi comme patient zéro et le rançongiciel se propage. | [A-01](dossier_incident/preuves/02_A01_EDR_FIN-112_MIRAGE.md) · [A-12](dossier_incident/preuves/15_A12_chronologie_EDR_FIN-112.md) |
| 6. Impact constaté | II | L'inventaire recense 23 serveurs chiffrés sur 40. | ERP, paie, facturation et partages de fichiers deviennent prioritaires. | [A-13](dossier_incident/preuves/12_A13_inventaire_serveurs_impact.md) |
| 7. Reprise sûre | III | Les points en ligne récents sont suspects ou infectés ; la copie air-gap de Settat est isolée. | La cellule refuse de payer et restaure l'ERP, puis les services clients, par paliers contrôlés. | [A-30](dossier_incident/preuves/35_A30_integrite_sauvegardes_en_ligne.md) · [Décisions de reprise](dossier_incident/decisions/) |

La chaîne principale est donc : **accès anormal via `svc_oasisnet`, préparation d'une sortie, transferts sortants, sabotage des sauvegardes, chiffrement depuis FIN-112, puis restauration hors ligne**.

Le phishing A-11 est réel mais son lien causal avec MIRAGE n'est pas démontré. De même, le volume établi est de **117,8 Go** ; les 300 Go revendiqués par SIROCCO ne sont pas confirmés. La [chronologie consolidée](dossier_incident/chronologie/FICHE_CHRONOLOGIE_COMPLETE.md) précise ces limites et relie chaque maillon à sa source.

## Ce que le dossier établit

| Sujet | Constat étayé | À retenir |
| --- | --- | --- |
| **Accès initial** | `svc_oasisnet` est utilisé de nuit, hors de son fonctionnement attendu. | Une compromission liée au prestataire est plausible ; l'étendue exacte reste à confirmer. |
| **Exfiltration** | Le proxy confirme **117,8 Go** de transferts sortants. | La revendication de 300 Go de SIROCCO n'est pas démontrée. |
| **Impact** | L'inventaire SCCM constate 23 serveurs chiffrés. | Les activités ERP, paie, facturation et fichiers sont touchées. |
| **Sauvegardes** | Les points en ligne récents sont suspects ou infectés. | La copie air-gap de Settat est la base de restauration sûre. |
| **Reprise** | L'ERP est restauré avant la paie et la facturation. | Les services clients sont rouverts progressivement, avec contrôles à chaque palier. |

## Du signal à la décision

| Catégorie | Rôle dans l'enquête | Accès direct |
| --- | --- | --- |
| **Preuves** | Éléments qui établissent un fait de la chaîne d'incident. | [Consulter les 15 preuves](dossier_incident/preuves/) |
| **Fausses pistes** | Hypothèses investiguées puis réfutées, pour rendre le raisonnement transparent. | [Voir les pistes écartées](dossier_incident/triage/fausses_pistes/) |
| **Bruits** | Signaux réels, mais sans lien démontré avec MIRAGE. | [Voir les bruits qualifiés](dossier_incident/triage/bruits/) |
| **Décisions** | Arbitrages de la cellule, leur justification et leur conséquence. | [Lire les 12 décisions](dossier_incident/decisions/) |

> Une conclusion sans source n'est pas une preuve. Chaque fiche indique ce que le document permet d'affirmer — et ce qu'il ne permet pas d'affirmer.

## Retrouver rapidement l'information

| Vous voulez… | Consultez… |
| --- | --- |
| Comprendre le scénario et le périmètre | [Dossier incident](dossier_incident/README.md) |
| Suivre l'ordre des événements | [Chronologie](dossier_incident/chronologie/) |
| Examiner les éléments techniques | [Preuves et captures](dossier_incident/preuves/) |
| Comprendre les choix de crise | [Décisions de la cellule](dossier_incident/decisions/) |
| Identifier les actifs et dépendances | [Cartographie](dossier_incident/cartographie/) |
| Explorer les travaux par métier | [Pôles de la cellule](dossier_incident/poles/) |
| Télécharger les documents prêts à présenter | [Livrables jury](livrables_jury/) |

## Décisions de reprise retenues

| Décision | Pourquoi | Résultat recherché |
| --- | --- | --- |
| **Ne pas payer** | Un paiement ne garantit ni le déchiffrement, ni l'effacement des données exfiltrées. | Conserver une reprise indépendante et défendable. |
| **Restaurer depuis Settat** | Les sauvegardes en ligne récentes contiennent des indicateurs MIRAGE. | Éviter de réintroduire le rançongiciel. |
| **Prioriser l'ERP** | La paie et la facturation dépendent de ce socle commun. | Débloquer plusieurs services par une restauration cohérente. |
| **Rouvrir par paliers** | Chaque service doit être vérifié avant extension. | Reprendre sans transformer la restauration en nouvel incident. |

Les choix, leurs effets et leurs références sont détaillés dans le [registre des décisions](dossier_incident/decisions/README.md).

---

<div align="center">

<sub>Conçu dans le cadre de l'exercice KASBAH organisé par EMSI et CyberSup · AtlasGrid est un cas fictif à vocation pédagogique.</sub>

</div>
