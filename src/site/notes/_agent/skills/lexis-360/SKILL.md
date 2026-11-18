---
{"dg-publish":true,"permalink":"/agent/skills/lexis-360/skill/","ctime":"2026-11-18T17:24:42.826+01:00","mtime":"2026-11-18T18:54:31.361+01:00","dg-note-properties":{"date created":"2026-11-18, 17 25","date modified":"2026-11-18, 18 55","sector":null,"semester":null,"class":null,"form":null,"part":null,"name":"lexis-360","description":"Audite les cours de droit du coffre Obsidian pour dresser la liste priorisée des fiches Lexis 360 Intelligence (Fiches pédagogiques, Fiches pratiques, Synthèses JurisClasseur) manquantes à télécharger manuellement, exploite les renvois internes des PDF locaux et intègre les nouveaux PDF téléchargés dans le coffre."}}
---


# Skill : Audit et intégration des fiches Lexis 360 Intelligence

Ce skill systématise la démarche d'audit des cours de droit dans le coffre Obsidian afin d'identifier **exactement** quels documents **Lexis 360 Intelligence** manquent pour les cours et TD, d'exploiter les renvois cachés dans les PDF déjà téléchargés, puis d'intégrer proprement les nouveaux PDF dans le coffre.

---

## 1. Cadre d'usage, sécurité et faisabilité

1. **Aucun scraping ni collecte d'identifiants :**
   - Ne jamais demander d'identifiants ou mots de passe universitaires (ENT / Lexis 360 Intelligence) et ne jamais tenter de scraper, contourner l'authentification ou franchir des protections anti-bot.
   - Le portail `dev.lexisnexis.com` concerne des API d'entreprise B2B (principalement anglophones : Metabase News, Lex Machina, State Net) et ne fournit pas d'accès API étudiant aux *Fiches pédagogiques* ni au *JurisClasseur* français. Le téléchargement des PDF reste manuel depuis l'ENT sur **Lexis 360 Intelligence**.
2. **Intégrité du coffre (`AGENTS.md`) :**
   - Respecter strictement l'interdiction de modifier ou consulter `.obsidian/`.
   - Utiliser exclusivement des wikilinks Obsidian (`[[Note]]`, `![[Document.pdf]]`), jamais de liens Markdown `[texte](chemin.md)` ni de pages fantômes.

---

## 2. Mode 1 — Audit des fiches Lexis 360 manquantes à télécharger

Suivre strictement ces 5 étapes dans l'ordre :

### Étape 1 : Inventaire automatisé du coffre
Exécuter le script autonome d'inventaire (bibliothèque standard Python uniquement) depuis la racine du coffre :

```bash
/Library/Frameworks/Python.framework/Versions/3.14/bin/python3 -s "_agent/skills/lexis-360/scripts/inventory_lexis.py" --semester S3
```

*(Adapter `--semester`, ajouter `--class <Matière>` pour cibler une seule matière, ou `--include-shared` si besoin d'inspecter le détail de `Drive/Josepha`).*

Ce script résout automatiquement les pièges du coffre :
- Normalise l'Unicode macOS (NFD $\rightarrow$ NFC) et les apostrophes pour éviter de rater des fichiers accentués.
- Sépare les cours personnels (`sector: "[[AES]]"`, racine et `Drive/Lise/`) des cours partagés (`sector: "[[Josepha]]"`, `Drive/Josepha/`).
- Détecte **tous** les PDF Lexis 360 Intelligence (y compris sans `"Lexis"` dans leur nom de fichier) via leurs métadonnées et liens internes.
- Repère les PDF Lexis **orphelins** (présents sur disque mais non liés dans une note Obsidian) et les liens `.pdf]]` cassés.
- Extrait les identifiants techniques de renvois (`FP_FP-...`, `EF_SY-...`, `EF_FA-...`) cités à l'intérieur des PDF locaux et déjà dédupliqués contre les fichiers présents.

### Étape 2 : Cartographie des plans, CM et TD par matière
Pour chaque matière juridique du périmètre :
1. Lire les notes de structure identifiées à l'étape 1 : `References/<Matière>.md`, plans de cours (`PLAN DE COURS - ...`, `*- Plan.md`, plans PDF dans `Drive/Lise/`), et index existants (`Lexis - <Matière>.md`).
2. Parcourir les intitulés, chapitres et sommaires des notes `[[CM]]` et `[[TD]]` personnelles pour dresser la liste réelle des thèmes du cours.
3. Distinguer l'avancement réel : chapitres effectivement rédigés ou vus en TD vs marqueurs `(à venir)` / notes ébauches.
4. N'utiliser `Drive/Josepha/` qu'en référence secondaire si une matière n'a pas encore de plan ou de CM personnel complet (en le mentionnant explicitement).

### Étape 3 : Extraction des renvois exacts depuis les PDF Lexis locaux
La section 4 du rapport de [inventory_lexis.py](./scripts/inventory_lexis.py) liste les PDF locaux contenant des renvois vers des fiches/synthèses absentes du coffre.
- Ouvrir ces PDF **directement avec `read_file`** (les flux internes des PDF Lexis encodent le texte en glyphes CID ; `read_file` est le moyen fiable d'en extraire le texte).
- Lire en priorité les **pages 1 à 3** de chaque *Fiche pédagogique* :
  - Section **`3.1. Synthèses JurisClasseur`** et **`3.2. Fascicules JurisClasseur`** $\rightarrow$ titres exacts des synthèses et fascicules associés.
  - En-tête et corps / encadrés `Connaissances` $\rightarrow$ renvois inline `V. Fiche pédagogique n° XXXX : Titre` et `V. Fiche pratique n° XXXX : Titre`.
- Recouper chaque titre/numéro trouvé avec la liste locale de l'étape 1 (attention aux fiches de méthodologie déjà présentes sous un nom personnalisé, ex. `Maîtriser le commentaire d'arrêt.pdf` ou `Résoudre un cas pratique - Lexis 360 Intelligence.pdf`).

### Étape 4 : Analyse des écarts (Gap Analysis) et priorisation
Croiser les chapitres/TD (étape 2) avec les PDF déjà présents et les renvois extraits (étape 3), puis classer les documents manquants selon deux niveaux :
- **Priorité 1 (Immédiat) :** thèmes déjà vus en CM ou travaillés en TD, fiches sœurs directement appelées par les fiches du cours, ou matières juridiques quasiment dépourvues de PDF Lexis.
- **Priorité 2 (À venir / Approfondissement) :** chapitres marqués `(à venir)` dans le syllabus, compléments de méthodologie manquants (ex. dissertation/cas pratique/note de synthèse si absents) et *Synthèses JurisClasseur* de consolidation.

> [!IMPORTANT]
> **Règle stricte anti-hallucination :** Ne jamais inventer un numéro `n° XXXX` de Fiche pédagogique/pratique ni une référence *JurisClasseur*. N'afficher un numéro exact que s'il a été lu directement dans un PDF du coffre via `read_file` à l'étape 3 ; dans tous les autres cas, formuler une suggestion par thème exact du cours accompagnée des mots-clés de recherche.

### Étape 5 : Restitution actionnable à l'utilisateur
Présenter un compte-rendu clair et directement utilisable :
1. **État des lieux rapide** par matière (nombre de PDF déjà présents + rappel des PDF déjà téléchargés mais **orphelins** à lier).
2. **Checklist de téléchargement par matière** (classée par **Priorité 1** puis **Priorité 2**), précisant pour chaque document :
   - Intitulé et référence exacte (si lue à l'étape 3) ;
   - Lien direct avec le cours / TD / fiche qui y renvoie ;
   - **Requête recommandée** dans la barre de recherche **Lexis 360 Intelligence** et filtre conseillé (*Fiches pédagogiques*, *Synthèses JurisClasseur*, *Fiches pratiques*).
3. **Prochaine étape :** inviter l'utilisateur à déposer les nouveaux PDF dans le coffre puis à demander l'intégration (**Mode 2**).

---

## 3. Mode 2 — Intégration Obsidian après téléchargement (séparée des cours)

Déclenché lorsque l'utilisateur indique avoir téléchargé les PDF manquants dans le coffre :
1. **Détecter les nouveaux fichiers :** relancer `inventory_lexis.py` pour identifier tous les PDF Lexis orphelins (`ORPHELIN (non lié)`).
2. **Séparation stricte Cours vs Documentation Lexis :**
   - **Ne jamais modifier ni enrichir une note de cours** (`CM`, `TD` ou `Notion` personnelle à la racine) avec des extraits ou PDF Lexis.
   - **Centraliser les PDF sources** dans `Attachments/Lexis 360/` (jamais à la racine du coffre).
   - **Créer ou compléter les fiches Lexis exclusivement dans `Lexis 360/<Matière>/Lexis - <Titre>.md`** (ou index `Lexis 360/<Matière>/Lexis - <Matière>.md`), précédées d'un bandeau `> [!info] Documentation externe — Lexis 360 Intelligence` et du frontmatter YAML dédié (`[[Lexis]]` dans `References/Lexis.md`) :

```yaml
---
date created: "YYYY-MM-DD, HH mm"
date modified: "YYYY-MM-DD, HH mm"
sector: "[[Lexis]]"
semester: "[[S3]]"
class: "[[Matière]]"
form: "[[Lexis]]"
part:
dg-publish: true
---

# Lexis - Titre de la fiche

> [!info] Documentation externe — Lexis 360 Intelligence
> Fiche documentaire externe, distincte de tes notes de cours.

![[Nom exact du fichier - Lexis 360 Intelligence.pdf]]
```

   *(Avant d'écrire tout wikilink dans le frontmatter ou le corps, vérifier que les cibles `[[Lexis]]`, `[[S3]]`, `[[Matière]]` existent bien dans `References/` et que toutes les cibles `[[...]]` existent dans le coffre).*
3. **Contrôle final :** relancer `inventory_lexis.py` et vérifier qu'il ne reste ni PDF Lexis orphelin, ni lien `.pdf]]` cassé, ni mélange dans les cours (`sector == AES`).
