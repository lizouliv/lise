---
{"dg-publish":true,"permalink":"/agent/skills/transcript/skill/","ctime":"2026-11-08T19:42:46.000+01:00","mtime":"2026-11-25T18:53:03.624+01:00","dg-note-properties":{"date created":"2026-11-07, 22 50","date modified":"2026-11-25, 18 53","sector":null,"semester":null,"class":null,"form":null,"part":null,"name":"transcript","description":"Détecte et lit directement les fichiers de transcription brute (.txt, .md, images) dans le dossier Transcripts/ pour les transformer en fiches de cours structurées au format Obsidian, crée ou complète les fiches d'articles, d'arrêts et de notions citées (via Légifrance), vérifie l'intégrité de tous les wikilinks, puis supprime les fichiers sources traités du dossier Transcripts/."}}
---


# Skill : Synthèse de transcription en cours Obsidian

Ce skill permet de localiser automatiquement des fichiers de transcription brute (texte ou photos de cours) dans le dossier `Transcripts/` (ou `transcripts/`), d'analyser leur contenu, de les transformer en fiches de cours académiques dans le coffre Obsidian, de créer ou compléter les fiches de références associées (articles, arrêts, notions clés), puis de nettoyer les fichiers traités dans `Transcripts/`.

---

## 1. Localisation et sélection automatique des fichiers sources

1. **Dossier source dédié (`Transcripts/`)** :
   - Toutes les transcriptions brutes déposées sous forme de fichiers texte (`.txt`, `.md`, `.vtt`, `.srt`, etc.) ou d'images/photos de notes (`.jpg`, `.png`, etc.) sont stockées dans le dossier `Transcripts/` à la racine du coffre.
   - L'agent doit **toujours inspecter directement** le dossier `Transcripts/` (insensible à la casse) dès que l'utilisateur demande de traiter une transcription.

2. **Résolution du fichier cible** :
   - **Fichier ou matière spécifié(e)** : Si l'utilisateur mentionne un nom de fichier, une matière ou un mot-clé (ex: *"résume la transcription de droit pénal"*, *"traite le fichier seance3.txt"*), l'agent parcourt `Transcripts/` pour trouver le fichier correspondant (par son nom ou en vérifiant les premières lignes) et le charge directement sans exiger de chemin absolu.
   - **Fichier non spécifié** :
     - S'il n'y a qu'un seul fichier dans `Transcripts/`, le charger et le traiter directement.
     - S'il y a plusieurs fichiers, lister les fichiers présents dans `Transcripts/` et traiter ceux qui correspondent à la séance (ou le plus récent / demander confirmation si plusieurs séances distinctes coexistent).
   - **Dossier vide ou fichier introuvable** : Informer l'utilisateur que le dossier `Transcripts/` ne contient pas le fichier attendu et l'inviter à y déposer sa transcription.

3. **Destination des notes et suppression après traitement** : La note de cours générée sera enregistrée à la racine du coffre (avec les autres cours AES existants), **jamais** dans `Transcripts/` ni dans `Drive/`. Une fois les notes créées/mises à jour et tous les wikilinks vérifiés sans erreur, l'agent **supprime les fichiers sources qui ont été traités** dans `Transcripts/` (sans toucher aux éventuels autres fichiers non traités).

---

## 2. Déduction des métadonnées et analyse du contexte

1. **Identification des métadonnées du cours** :
   - À partir du titre du fichier source ou du contenu de la transcription, déterminer :
     - `sector` : `"[[AES]]"` (réservé exclusivement à `[[AES]]` ; `[[Josepha]]` ne concerne en aucun cas les transcriptions et est réservé au dossier `Drive/`).
     - `semester` : semestre correspondant (ex: `"[[S3]]"`, `"[[S2]]"`).
     - `class` : matière en wikilink vers sa fiche dans `References/` (ex: `"[[Pénal]]"`, `"[[Administratif]]"`, `"[[Compta]]"`, `"[[Travail]]"`, `"[[Fiscal]]"`, `"[[GRH]]"`, `"[[Micro]]"`, `"[[CCPE]]"`, `"[[Anglais]]"`).
     - `form` : `"[[CM]]"` pour un cours magistral ou `"[[TD]]"` pour des travaux dirigés.
     - `part` : numéro ou intitulé de la partie/séance en wikilink (ex: `"[[1]]"`, `"[[2]]"`, etc.).
2. **Cohérence du plan et style** :
   - Parcourir les notes déjà existantes de la matière dans le coffre pour aligner la hiérarchie des titres (`#`, `##`, `###`) et la nomenclature des chapitres.

---

## 3. Format du Frontmatter YAML obligatoire (Fiche de cours)

Chaque note de cours générée doit débuter par le bloc exact suivant :

```yaml
---
date created: "YYYY-MM-DD, HH mm"
date modified: "YYYY-MM-DD, HH mm"
sector: "[[AES]]"
semester: "[[S3]]"
class: "[[Matière]]"
form: "[[CM]]"
part: "[[1]]"
dg-publish: true
---
```

---

## 4. Nettoyage et structuration académique du contenu

1. **Suppression des scories orales** :
   - Éliminer les hésitations, tics de langage (*"euh"*, *"du coup"*, *"vous voyez"*), répétitions, digressions et apartés organisationnels de l'enseignant.
   - Reformuler dans un style universitaire rigoureux, clair, fluide et synthétique.
2. **Mise en page Obsidian** :
   - Structuration claire en sections (`##`) et sous-sections (`###`).
   - Mise en valeur des définitions, arrêts ou principes juridiques/économiques avec des callouts Obsidian (`> [!abstract]`, `> [!info]`, `> [!quote]`, `> [!tip]`, `> [!warning]`).
   - Formules en LaTeX `$formule$` pour les mathématiques, microéconomie ou comptabilité.
   - Listes à puces serrées (séparées par `\n` simple).
3. **Conclusion de la note** :
   - Ajouter systématiquement en fin de note une section `## Liens associés` listant les fiches du coffre mentionnées dans le corps du texte.

---

## 5. Création, mise à jour et vérification des notes liées (Articles, Arrêts & Notions)

Lors du traitement d'une transcription, l'agent doit identifier tous les **articles de droit**, **arrêts de jurisprudence** et **notions clés** cités en cours afin de créer ou enrichir leurs fiches dédiées et de les lier dans le cours.

### A. Nomenclature et Frontmatter des fiches liées
Respecter scrupuleusement les formats canoniques définis dans le skill `legifrance` (fichiers placés à la racine du coffre) :
- **Articles (`form: "[[Code]]"`)** : `Art. [L./R./D.] [Numéro] [Abréviation]` *(ex. `Art. 121-3 C. pén.`, `Art. L. 1245-1 C. trav.`, `Art. 1137 C. civ.`, `Art. 55 Const.`, `Art. 8 Conv. EDH`, `Art. 8 DDHC 1789`)*.
- **Arrêts (`form: "[[Arret]]"`)** : `[Juridiction abrégée], [date complète]` *(ex. `Cass. soc., 10 juillet 2002`, `Crim., 18 juin 1993, Sang contaminé`)* ou `Arrêt [Nom], [Juridiction], [date]` ou `Arrêt [Nom du grand arrêt]` / `CE, [date]` / `Décision [Nom ou Date]`.
- **Notions clés (`form: "[[Notion]]"`)** : Intitulé canonique court et précis *(ex. `Animus Necandi`, `Dol éventuel`, `CDI`, `Marginalisme`)*.

Chaque fiche d'article, d'arrêt ou de notion créée ou modifiée doit obligatoirement débuter par ce frontmatter YAML standardisé (et voir ses propriétés vérifiées et `date modified` actualisée en cas de modification) :

```yaml
---
date created: "YYYY-MM-DD, HH mm"
date modified: "YYYY-MM-DD, HH mm"
sector: "[[AES]]"
semester: "[[S3]]"
class: "[[Matière]]"
form: "[[Code]]" # ou "[[Arret]]" ou "[[Notion]]"
part:
dg-publish: true
---
```

### B. Création ou complétion des notes
- **Si la fiche n'existe pas dans le coffre** : Créer le fichier `.md` correspondant au cours de la même action et le renseigner.
- **Si la fiche existe déjà** (notamment si elle est vide ou partielle) : La modifier pour la compléter ou l'actualiser avec les apports du cours (et mettre à jour `date modified`).

### C. Accès autorisé et strictement limité à Légifrance (`https://www.legifrance.gouv.fr/` / API PISTE)
- **Autorisation exclusive** : **Uniquement pour mener à bien cette étape** de création et de complétion des notes d'articles, d'arrêts ou de textes juridiques cités dans les transcriptions, l'agent interroge Légifrance en priorité via le serveur MCP `legifrance` (`legifrance_get_article`, `legifrance_search`, `legifrance_consult`) ou le client CLI du skill `legifrance` (ou, en secours, via recherche web ciblée sur le domaine `legifrance.gouv.fr`).
- **Usage** :
  - Pour les **articles (`[[Code]]`)** : Rechercher et extraire le texte officiel en vigueur via l'API Légifrance / `legifrance.gouv.fr` pour renseigner exactement la note.
  - Pour les **arrêts (`[[Arret]]`)** : Vérifier les références exactes (date, juridiction, numéro, attendu ou considérant de principe) via l'API Légifrance / `legifrance.gouv.fr`.

### D. Style de rédaction des fiches liées : aller droit à l'essentiel
- **Articles (`form: "[[Code]]"`)** : Reproduire le texte officiel de l'article sous le titre `# Art. ...`.
- **Arrêts (`form: "[[Arret]]"`)** : **Aller à l'essentiel sans être verbeux ni répétitif** :
  - Contexte/faits résumés en 1 à 2 phrases maximum (uniquement si nécessaire).
  - Principe juridique dégagé (attendu/considérant clé et portée en cours) formulé de manière directe, synthétique et percutante.
- **Notions clés (`form: "[[Notion]]"`)** : **Aller à l'essentiel sans digression ni répétition** :
  - Définition claire, directe et synthétique (quelques lignes ou puces résumant la définition et les conditions/effets essentiels).

### E. Vérification systématique des Wikilinks
- Insérer les wikilinks (`[[Nom exact de la note]]` ou `[[Nom exact de la note|Texte fluide]]`) dans la fiche de cours et dans la section `## Liens associés`.
- **Contrôle final obligatoire** : Vérifier systématiquement que chaque wikilink inséré correspond **exactement** au nom d'un fichier `.md` réellement présent sur le disque (casse, accents, abréviations et ponctuation inclus) afin de garantir que tous les liens fonctionnent et qu'il n'existe aucune page fantôme.

---

## 6. Emplacement, nettoyage et confirmation

1. **Enregistrement de la fiche de cours finale** :
   - Enregistrer la note de cours produite directement à la racine du coffre (au même niveau que les autres cours magistraux AES existants, ex. `1 - Introduction droit admin.md`), **jamais** dans `Transcripts/` ni dans `Drive/`.
2. **Suppression des fichiers sources traités** :
   - Uniquement après avoir enregistré la fiche de cours et les fiches liées et vérifié l'intégrité de tous les wikilinks, supprimer de `Transcripts/` les fichiers sources qui viennent d'être traités (ne jamais supprimer des fichiers non traités).
3. **Compte-rendu à l'utilisateur** :
   - Préciser le ou les fichiers sources détectés, traités puis supprimés dans `Transcripts/`.
   - Confirmer le chemin de la nouvelle fiche de cours créée.
   - Lister les fiches d'articles, d'arrêts et de notions créées ou mises à jour ainsi que la confirmation de la vérification des liens.
