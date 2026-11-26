---
{"dg-publish":true,"permalink":"/agent/skills/td/skill/","dg-note-properties":{"date created":"2026-11-07, 23 10","date modified":"2026-11-16, 15 42","sector":null,"semester":null,"class":null,"form":null,"part":null,"name":"td","description":"Analyse un sujet de TD, découpe la séance et résout les exercices selon la mise en page épurée et structurée d'Exos TD 5 (parties, énoncé synthétique, question de droit, résolution fluide en 3 étapes, callout pièges)."}}
---


# Skill : Résolution de séance de Travaux Dirigés (TD)

Ce skill formalise la structure épurée et directe issue du modèle **Exos TD 5** pour résoudre, synthétiser et réviser les séances de Travaux Dirigés sans lourdeur superflue.

---

## 1. En-tête YAML obligatoire

Chaque note de TD débute par le frontmatter standard du coffre avec wikilinks :

```yaml
---
date created: "YYYY-MM-DD, HH mm"
date modified: "YYYY-MM-DD, HH mm"
sector: "[[AES]]"
semester: "[[S3]]"
class: "[[Travail]]" # ou "[[Responsabilité civile]]", "[[Fiscalité]]", etc.
form: "[[TD]]"
part: "[[5]]" # Numéro de la séance
dg-publish: true
---
```

---

## 2. Structure globale de la note

```markdown
# TD [Numéro] : [Intitulé complet du TD]

![[NomDuFichierSujet.pdf]]

---

# Partie I : [Titre de la première partie, ex. Analyse d'arrêts]

[Exercices de la Partie I...]

---

# Partie II : [Titre de la seconde partie, ex. Cas pratiques]

[Exercices de la Partie II...]
```

*(Si le TD ne comporte pas de découpage en plusieurs sous-ensembles, les exercices se succèdent directement sous le titre principal).*

---

## 3. Canevas simplifié de chaque exercice

Pour chaque exercice, adopte le canevas épuré suivant (sans métadonnées superflues ni redondances) :

```markdown
### Exercice [Numéro] : [Intitulé court / Nom de l'arrêt / Thème de l'exercice]
- **Catégorie :** [Analyse d'arrêt / Cas pratique / Calcul...] – [Thématique précise et concepts clés]

> [!abstract] Énoncé synthétique
> [Faits résumés ou mise en situation concise]
> 
> **Question de droit posée :** [Question de droit précise] (ou **Problématique posée :**)

#### Résolution
1. **Étape 1 - Identification des hypothèses :**
   - Visas des textes applicables : liens canoniques vers les articles (`[[Art. ...]]`) ou définitions préalables.
2. **Étape 2 - Déroulé de l'argumentation :**
   - Attendu de principe ou règle de droit (citation en bloc `> ` si arrêt) :
     > " Règle ou attendu de principe "
   - Application concrète et articulée aux faits de l'espèce (Majeure $\rightarrow$ Mineure).
3. **Étape 3 - Résultat final et vérification :**
   - Décision finale (cassation/rejet, validation ou solution du cas pratique) et portée pratique directe.

> [!check]- Remarques méthodologiques et pièges à éviter
> - **[Piège fréquent ou confusion à proscrire] :** Explication synthétique.
> - **[Point d'attention examen] :** Conseil pratique de rédaction.

---
```

---

## 4. Règles de rédaction et allègements clés

1. **Pas de ligne « Méthode de référence » :** La catégorie en tête d'exercice suffit amplement. Inutile d'ajouter une ligne artificielle de lien vers une méthode générale.
2. **Intitulé direct `#### Résolution` :** Privilégier `#### Résolution` plutôt que la formule lourde `#### Résolution étape par étape`.
3. **Pas de bloc final récapitulatif lourd :** Ne pas ajouter de section `## Méthodes et fiches mobilisées` en queue de note. Tous les wikilinks (`[[Art. ...]]`, `[[Cass. ...]]`, `[[Notion]]`) sont intégrés directement et organiquement dans les étapes de résolution (visas, attendus, motifs).
4. **Callout repliable pour les pièges :** Toujours utiliser la syntaxe repliable `> [!check]- Remarques méthodologiques et pièges à éviter` pour garder la fiche aérée en lecture rapide.
5. **Séparateur horizontal :** Insérer systématiquement `---` entre deux exercices.
