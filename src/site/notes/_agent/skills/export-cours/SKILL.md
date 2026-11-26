---
{"dg-publish":true,"permalink":"/agent/skills/export-cours/skill/","dg-note-properties":{"date created":"2026-11-08, 16 04","date modified":"2026-11-08, 19 45","sector":null,"semester":null,"class":null,"form":null,"part":null,"name":"drive-docx","description":"Exporte et convertit les cours partagés au format Word (.docx) dans Drive (cours de Josepha) en notes Markdown enrichies et standardisées dans Drive/Josepha avec frontmatter YAML conforme, extraction d'images et tableaux."}}
---


# Skill : Exportation et conversion de cours en notes Obsidian

Ce skill guide l'extraction, la conversion et la standardisation des documents de cours partagés sous format Word `.docx` (cours de Josepha dans `Drive/`) en notes Markdown natives, enrichies et classées dans `Drive/Josepha/...`.

---

## 1. Consignes fondamentales et sécurité du coffre

1. **Répertoire protégé `.obsidian/`** :
   - Il est strictement interdit de modifier, renommer, créer ou supprimer des fichiers ou des dossiers situés dans `.obsidian/`.
2. **Syntaxe des liens internes (Wikilinks)** :
   - Utilise exclusivement la syntaxe wikilink Obsidian : `[[Nom de la note]]` ou `[[Nom de la note|Texte d'ancrage]]`.
   - N'utilise **JAMAIS** la syntaxe markdown `[texte](chemin/note.md)` pour lier des notes entre elles.
3. **Interdiction absolue des pages fantômes** :
   - Ne crée jamais de lien vers une note qui n'existe pas encore dans le coffre, à moins de créer la note correspondante au cours de la même action.
   - Vérifie systématiquement les fichiers existants (notamment dans `References/`) avant d'insérer un wikilink. Si une notion n'a pas de fiche dédiée, laisse le texte en clair sans crochets.

---

## 2. Standardisation du Frontmatter YAML

Chaque note exportée ou modifiée doit obligatoirement débuter par ce bloc YAML exact :

```yaml
---
date created: "YYYY-MM-DD, HH mm"
date modified: "YYYY-MM-DD, HH mm"
sector: "[[Josepha]]"
semester: "[[S3]]"
class: "[[Compta]]"
form: "[[CM]]"
part: "[[1]]"
dg-publish: true
---
```

### Règles d'attribution des propriétés 
- **`date created` et `date modified`** : Format `"YYYY-MM-DD, HH mm"` (ex: `"2026-11-08, 16 05"`).
- **`sector`** : Par défaut `"[[Josepha]]"` pour les cours et documents issus de cette source (ou `"[[AES]]"` / secteur spécifié).
- **`semester`** : Wikilink vers le semestre correspondant, ex: `"[[S3]]"`, `"[[S2]]"`.
- **`class`** : Wikilink vers la matière correspondante dans `References/` :
  - Droit administratif $\rightarrow$ `"[[Administratif]]"`
  - Droit du travail $\rightarrow$ `"[[Travail]]"`
  - Droit pénal général $\rightarrow$ `"[[Pénal]]"`
  - Fiscalité des entreprises $\rightarrow$ `"[[Fiscal]]"`
  - Comptabilité générale $\rightarrow$ `"[[Compta]]"`
  - Gestion des ressources humaines $\rightarrow$ `"[[GRH]]"`
  - Microéconomie de la production $\rightarrow$ `"[[Micro]]"`
  - Continuité et controverses de la pensée économique $\rightarrow$ `"[[CCPE]]"`
  - Anglais $\rightarrow$ `"[[Anglais]]"`
- **`form`** : Wikilink vers le type d'enseignement :
  - Cours magistraux $\rightarrow$ `"[[CM]]"`
  - Travaux dirigés, fiches d'exercices, cas pratiques $\rightarrow$ `"[[TD]]"`
- **`part`** : Wikilink vers le numéro de partie ou séance s'il est identifiable, ex: `"[[1]]"`, `"[[2]]"`, `"[[3]]"`, `"[[0]]"` pour les introductions, ou laisser vide `""` si non applicable.
- **`dg-publish`** : Toujours `true`.

---

## 3. Directives de conversion Markdown et mise en page

### A. Hiérarchie des titres et structure
- Convertir les titres selon la structure logique du document plutôt qu'un texte plat :
  - Titre de la partie / Document principal $\rightarrow$ `# Titre`
  - Chapitres / Grands titres $\rightarrow$ `## Chapitre X - …`
  - Sections / Titres intermédiaires $\rightarrow$ `### Section X - …` ou `### I - …`
  - Paragraphes / Sous-sections $\rightarrow$ `#### §1 - …` ou `#### A - …`
  - Points de vigilance ou exercices $\rightarrow$ `#### Exercice X` ou `##### …`

### B. Extraction et intégration des images (médias)
1. Tout document contenant des éléments visuels (`word/media/imageX.png`, schémas, graphiques, écritures comptables sous forme d'image) doit voir ses images extraites dans `Attachments/`.
2. Nommer les images extraites de façon claire et sans risque de collision :
   - Format : `s3_<matière>_<chapitre_slug>_img<Num:02d>.<ext>`
3. Insérer les images dans le corps de texte ou les cellules de tableaux à l'aide de la syntaxe native Obsidian :
   ```markdown
   ![[s3_compta_chapitre_1_-_introduction_à_la_img01.png]]
   ```

### C. Tableaux
- Convertir systématiquement les tableaux Word en tableaux GitHub Flavored Markdown :
  ```markdown
  | Colonne 1 | Colonne 2 | Colonne 3 |
  | --- | --- | --- |
  | Donnée 1 | Donnée 2 | Donnée 3 |
  ```
- Remplacer les retours à la ligne internes aux cellules par des balises `<br>`.
- Échapper les barres verticales contenues dans le texte (`\|`).
- Si une cellule contient une image, insérer `![[s3_compta_chapitre_1_-_introduction_à_la_img01.png]]` directement dans la cellule.

### D. Listes et typographie
- **Listes serrées** : Les éléments de liste consécutifs doivent être séparés par un simple saut de ligne `\n` pour un rendu compact dans Obsidian.
- **Nettoyage des astérisques** :
  - Les espaces doivent toujours être placés **à l'extérieur** des marqueurs de style (`**texte** `, jamais `** texte **`).
  - S'assurer qu'aucun astérisque orphelin n'apparaît en début de ligne (`- **Texte**` et non `- *Texte**`).
- **Formules et mathématiques** :
  - Conserver les indices `~x~` ou `_x` et exposants `^x^`.
  - Employer le format LaTeX `$formule$` ou des symboles Unicode lisibles (`√`, `Δ`, `α`, `β`, `π`) pour les équations économiques et comptables.

---

## 4. Procédure étape par étape lors d'une demande d'export

1. **Cartographie des sources** : Identifier les fichiers sources (`.docx`, images, `.pdf`) dans `Attachments/<semestre>/<matière>/...` ou `Drive/Lise/<semestre>/<matière>/...` (ou dans le sous-dossier spécifié).
2. **Identification des métadonnées** : Déduire la matière (`class`), le semestre (`semester`), le type (`form`) et la partie (`part`).
3. **Extraction & Conversion** :
   - Parcourir les paragraphes et tableaux dans l'ordre du document.
   - Extraire chaque image vers `Attachments/`.
   - Convertir les blocs en Markdown propre et lisible.
4. **Génération du fichier `.md`** :
   - Placer impérativement le fichier dans l'arborescence de destination sous `Drive/<sector>/<semester>/<matière>/...` (ex: `Drive/Josepha/S3/<matière>/…`), et **JAMAIS** directement à la racine du coffre (ne jamais créer de dossier racine `S3/`).
   - Insérer en tête le frontmatter YAML normalisé.
5. **Vérification finale** :
   - Vérifier l'absence totale de liens fantômes (`phantom links`).
   - Vérifier la présence effective de toutes les images référencées dans `Attachments/`.
   - Confirmer la bonne conformité YAML.
