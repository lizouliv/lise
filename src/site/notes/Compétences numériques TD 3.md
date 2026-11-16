---
{"dg-publish":true,"permalink":"/competences-numeriques-td-3/","ctime":"2026-11-14T12:11:13.876+01:00","mtime":"2026-11-14T12:11:13.876+01:00","dg-note-properties":{"date created":"2026-11-14, 12 10","date modified":"2026-11-14, 12 10","sector":"[[References/AES]]","semester":"[[References/S3]]","class":"[[References/Compétences numériques]]","form":"[[References/TD]]","part":"[[References/3]]"}}
---


[[TD-TT-3.pdf|TD-TT-3.pdf]]
[[TD-TT-3-modele.pdf|TD-TT-3-modele.pdf]]

# TD 3 : Traitement de texte — Images, diagrammes, légendes, renvois et table des illustrations
**Sujet support :** *TD Thématique Traitement de texte – Séance 03* (`TD-TT-3`) — Antoine Widlöcher, Pierre Beust, Isabelle Duchatelle.

---

## Livrables prêts à l'emploi (Dossier `Attachments/TD3 Livrables/`)
- **Document ODT mis en forme (2 pages) :** `Attachments/TD3 Livrables/TD-TT-3-realise.odt`
- **Document PDF exporté (2 pages) :** `Attachments/TD3 Livrables/TD-TT-3-realise.pdf`
- **Archive ZIP finale à déposer :** `Attachments/TD3 Livrables/TD-TT-3-rendu.zip`

---

## Résolution synthétique du TD

### Exercice 1 : Insertion d'images, modes d'ancrage, adaptation du texte et redimensionnement
- **Catégorie :** Intégration graphique, ancrage et habillage dans LibreOffice Writer
- **Méthode de référence :** Gestion de l'ancrage et de l'adaptation au texte des objets flottants

> [!abstract] Énoncé synthétique
> Éditer `TD-TT-3-donnees.odt` pour y insérer le logo d'exposition (`TD-TT-3-logo.png`) ancré à la page avec un dégagement inférieur de $2\text{ cm}$, puis insérer la première œuvre (`TD-TT-3-oeuvre1.png`) ancrée au premier paragraphe avec alignement, habillage et redimensionnement homothétique.

#### Résolution étape par étape
1. **Étape 1 - Identification des hypothèses :** Le document `TD-TT-3-donnees.odt` dispose de marges de $3\text{ cm}$ haut/bas et $4\text{ cm}$ gauche/droite (soit une largeur utile de $13\text{ cm}$), de titres en *Titre 1*, de trois paragraphes en *Corps de texte* et de marqueurs `XXXXX` à remplacer ultérieurement par des renvois.
2. **Étape 2 - Déroulé de la manipulation et réponses aux questions :**
   - **Logo (`TD-TT-3-logo.png`, Q1–Q6) :**
     - Insérer l'image via `Insertion > Image...`.
     - Clic droit > `Ancrage > À la page` : le logo est lié géométriquement à la page 1 et ne se déplace pas avec le texte.
     - Clic droit > `Adapter > Aucune adaptation` (*Pas d'adaptation*) : le texte est repoussé entièrement au-dessous de l'image plutôt que de l'entourer.
     - Utiliser `Alt + Flèches directionnelles` (après avoir sélectionné l'image) pour effectuer des déplacements fins au pixel/millimètre près.
     - Clic droit > `Propriétés...` (ou `Image...`) > onglet `Adapter` : fixer l'espacement *Bas* à `2 cm` pour que le premier titre ne débute qu'à $2\text{ cm}$ sous le logo.
   - **Première œuvre (`TD-TT-3-oeuvre1.png`, Q7–Q14) :**
     - Placer le curseur à l'intérieur du premier paragraphe de corps de texte, puis insérer `TD-TT-3-oeuvre1.png`.
     - Clic droit > `Ancrage > Au paragraphe` : l'image reste solidaire de ce paragraphe si du texte est ajouté ou supprimé au-dessus.
     - Dans `Propriétés > Type` : aligner horizontalement à *Droite* par rapport à la *Zone de texte du paragraphe*, verticalement en *Haut* de la *Zone de texte du paragraphe*.
     - Dans `Propriétés > Adapter` : choisir *Parallèle* (ou *Avant* / *Renvoi à gauche*) et définir un espacement horizontal (ex. `0,4 cm` à gauche) pour que le texte ne colle pas à l'image.
     - **Redimensionnement sans déformation (Q11) :** Maintenir la touche `Maj` (`Shift`) enfoncée tout en tirant une **poignée d'angle** de l'image, ou bien cocher l'option **« Conserver le ratio »** dans `Propriétés > Type` avant de modifier la largeur ou la hauteur.
3. **Étape 3 - Résultat final et vérification :** Le logo domine la page 1 avec $2\text{ cm}$ de respiration, et la première œuvre est habillée proprement sur la droite du premier paragraphe sans aucune déformation.

> [!check]- Remarques méthodologiques et pièges à éviter
> - Ne jamais tirer les poignées latérales ou verticales d'une image sans verrouiller le ratio, au risque d'écraser le visuel.
> - Distinguer l'ancrage *À la page* (réservé aux éléments fixes de couverture ou d'en-tête graphique comme le logo) de l'ancrage *Au paragraphe* (indispensable pour les figures qui doivent suivre le texte qu'elles illustrent).

---

### Exercice 2 : Insertion et habillage d'un diagramme issu de LibreOffice Calc
- **Catégorie :** Objets OLE incorporés et intégration tableur-traitement de texte
- **Méthode de référence :** Importation de diagrammes OLE depuis LibreOffice Calc

> [!abstract] Énoncé synthétique
> Récupérer par copier-coller le diagramme statistique présent dans `TD-TT-3-productions.ods` pour l'insérer dans la section « Productions de l'auteur », puis paramétrer son ancrage, son alignement et l'adaptation du texte.

#### Résolution étape par étape
1. **Étape 1 - Identification des hypothèses :** Le classeur `TD-TT-3-productions.ods` contient un diagramme en barres groupées (« Toiles », « Sculptures », « Films » de `2000` à `2010`) embarqué comme objet ODF (`Object 1`).
2. **Étape 2 - Déroulé de la manipulation :**
   - Ouvrir `TD-TT-3-productions.ods` dans LibreOffice Calc, cliquer une fois sur le diagramme pour le sélectionner et copier (`Ctrl + C`).
   - Dans Writer, placer le curseur sous le titre « Productions de l'auteur » (avant le paragraphe de texte) et coller (`Ctrl + V`). L'objet devient un diagramme autonome doté de sa propre table de données interne (`local-table`).
   - Clic droit > `Ancrage > Au paragraphe`.
   - Alignement horizontal : *Centré* par rapport à la zone de texte ; redimensionner proportionnellement (`Maj + glisser`, ex. largeur $12{,}5\text{ cm}$) pour tenir dans la largeur utile de $13\text{ cm}$.
   - Adaptation du texte : *Aucune adaptation* (renvoi au-dessus/au-dessous), afin que le texte explicatif se place sous le diagramme.
3. **Étape 3 - Résultat final et vérification :** Le diagramme apparaît net, centré sous son titre de section en page 2, sans chevaucher les marges.

> [!check]- Remarques méthodologiques et pièges à éviter
> - Préférer le collage natif Calc $\rightarrow$ Writer (qui préserve l'objet vectoriel modifiable et l'échelle nette à l'impression) à une simple capture d'écran matricielle.

---

### Exercice 3 : Création des légendes, analyse des champs de séquence et styles de cadre
- **Catégorie :** Légendage structuré, champs dynamiques et automatisation
- **Méthode de référence :** Légendes, champs de séquence et styles de cadre dans LibreOffice Writer

> [!abstract] Énoncé synthétique
> Ajouter la légende `"fond vert"` (catégorie `Figure`) à la première œuvre, analyser la structure créée (cadre et champ de séquence via *Noms de champ*), personnaliser les styles *Légende*/*Figure* et *Cadre*, configurer les légendes automatiques, insérer la seconde œuvre (`TD-TT-3-oeuvre2.png`) et légender manuellement le diagramme.

#### Résolution étape par étape
1. **Étape 1 - Identification des hypothèses :** L'ajout d'une légende modifie la structure interne de l'objet dans l'arbre XML du document ODT en encapsulant l'image dans un conteneur parent.
2. **Étape 2 - Déroulé de la manipulation et réponses aux questions :**
   - **Légende de la 1re œuvre (Q1–Q4) :** Clic droit sur l'image de l'Œuvre 1 > `Insérer une légende...`. Saisir `"fond vert"` (ou `Fond vert` selon le libellé choisi), sélectionner la catégorie **`Figure`** (à créer ou choisir dans la liste déroulante) et valider.
   - **Éléments ajoutés au document (Q5) :** LibreOffice Writer ajoute automatiquement deux éléments :
     1. Un **cadre** (*Frame*) englobant qui devient le nouvel élément positionné/ancré dans le paragraphe (l'image elle-même passe en ancrage *Comme caractère* à l'intérieur du cadre).
     2. Un paragraphe de **légende** placé sous l'image à l'intérieur de ce cadre, contenant le préfixe `Figure`, un champ numérique et le texte descriptif.
   - **Observation avec `Affichage > Noms de champ` (`Ctrl + F9`, Q6–Q7) :** À la place du chiffre `1`, Writer affiche l'expression du champ de séquence **`Séquence Figure = Figure+1`**. On en déduit que la numérotation des figures n'est pas écrite en dur : c'est un compteur automatique recalculé dynamiquement dès qu'une figure est ajoutée, déplacée ou supprimée dans le document. Désactiver ensuite `Noms de champ`.
   - **Repositionnement et styles (Q8–Q12) :**
     - Pour déplacer l'ensemble image + légende, il faut cliquer sur le **bord du cadre englobant** et non sur l'image interne (sinon seule l'image bouge à l'intérieur du cadre).
     - Le style de paragraphe utilisé par la légende est **`Figure`** (héritier de **`Légende`** / *Caption*). Modifier ce style : alignement *Centré*, taille réduite à `10 pt`, italique.
     - Modifier le style de cadre **`Cadre`** (`F11` > onglet *Styles de cadre*) : onglet *Bordures* $\rightarrow$ supprimer la bordure ; onglet *Adapter* $\rightarrow$ définir un espacement avec le texte (ex. `0,35 cm` à gauche et à droite). Appliquer ce style au cadre de la 1re œuvre (attention : la bordure éventuelle de l'image ou du cadre disparaît et l'habillage devient homogène).
   - **Légendes automatiques et figures suivantes (Q13–Q16) :**
     - **Intérêt des légendes automatiques (Q13) :** Paramétrées via `Outils > Options > LibreOffice Writer > Légende automatique`, elles évitent les oublis, garantissent l'uniformité de catégorie (`Figure`), de style de paragraphe et de style de cadre sur tout le document, et font gagner un temps considérable sur les documents longs.
     - Activer *Image LibreOffice Writer* avec catégorie `Figure`, style de caractère/paragraphe et style de cadre adaptés (Q14).
     - Insérer la seconde œuvre `TD-TT-3-oeuvre2.png` dans le deuxième paragraphe (Q15) : la légende `Figure 2: "fond rose"` est créée automatiquement ; positionner le cadre à gauche avec adaptation parallèle à droite.
     - Ajouter manuellement la légende du diagramme déjà inséré (`Clic droit > Insérer une légende...`, catégorie `Figure`, texte `Productions de l'auteur ces dernières années`) pour obtenir `Figure 3: Productions de l'auteur ces dernières années` (Q16).
3. **Étape 3 - Résultat final et vérification :** Les trois figures sont numérotées séquentiellement (`Figure 1`, `Figure 2`, `Figure 3`), encapsulées dans des cadres sans bordure et légendées en `10 pt` italique centré.

> [!check]- Remarques méthodologiques et pièges à éviter
> - Lorsque l'on ajoute une légende après avoir déjà aligné une image, il est courant que Writer réinitialise l'alignement sur le nouveau cadre englobant : il faut alors régler l'alignement et l'adaptation **sur le cadre**, pas sur l'image qu'il contient.
> - Les légendes automatiques ne s'appliquent qu'aux éléments insérés *après* leur activation (d'où la nécessité de légender manuellement le diagramme inséré à l'exercice 2).

---

### Exercice 4 : Insertion de renvois automatiques (références croisées)
- **Catégorie :** Référencement dynamique intra-documentaire
- **Méthode de référence :** Insertion de renvois vers des champs de séquence

> [!abstract] Énoncé synthétique
> Remplacer les deux séquences `XXXXX` dans les titres des deux premières sections par des renvois automatiques pointant vers les légendes des œuvres correspondantes, au format « Figure X ».

#### Résolution étape par étape
1. **Étape 1 - Identification des hypothèses :** Chaque légende contient un compteur de séquence nommé `Figure` (`Figure 1`, `Figure 2`, `Figure 3`) reconnu comme cible de renvoi par Writer.
2. **Étape 2 - Déroulé de la manipulation :**
   - Dans le titre `Commentaire de l’œuvre « Fond vert » (voir XXXXX)`, sélectionner et supprimer `XXXXX`.
   - Ouvrir `Insertion > Renvoi...` (`Ctrl + F2`, onglet *Renvois*).
   - Dans la colonne *Type*, sélectionner **`Figure`**.
   - Dans la colonne *Sélection*, choisir la cible `Figure 1: "fond vert"`.
   - Dans la liste *Insérer une référence à*, choisir **`Catégorie et numéro`** (afin d'obtenir uniquement `Figure 1` sans le texte complet de la légende) puis cliquer sur *Insérer*.
   - Répéter l'opération sur le deuxième titre pour insérer la référence `Catégorie et numéro` vers la seconde figure (`Figure 2`).
3. **Étape 3 - Résultat final et vérification :** Les deux titres affichent dynamiquement `Commentaire de l’œuvre « Fond vert » (voir Figure 1)` et `Commentaire de l’œuvre « Fond rose » (voir Figure 2)`. Si l'ordre des figures venait à être inversé, ces renvois se mettraient à jour automatiquement (ou via `Outils > Actualiser > Tout actualiser` / `F9`).

> [!check]- Remarques méthodologiques et pièges à éviter
> - Ne jamais taper « Figure 1 » à la main dans le texte : seul un champ de renvoi garantit la cohérence en cas de réorganisation du document.
> - Bien choisir *Catégorie et numéro* (et non *Texte de référence* qui inclurait `"fond vert"`, ni *Numéro uniquement* qui omettrait le mot `Figure`).

---

### Exercice 5 : Génération et mise à jour de la table des illustrations
- **Catégorie :** Indexation automatique des figures
- **Méthode de référence :** Génération et actualisation d'un Index des illustrations

> [!abstract] Énoncé synthétique
> Insérer en fin de document un *Index des illustrations* listant toutes les légendes de catégorie `Figure` avec leur *Texte de référence*, puis vérifier son fonctionnement dynamique en modifiant une légende et en mettant l'index à jour.

#### Résolution étape par étape
1. **Étape 1 - Identification des hypothèses :** Une table des illustrations peut être filtrée par *catégorie de légende* (`Figure`) ou par *noms d'objets*. Ici, toutes nos figures utilisent la séquence `Figure`.
2. **Étape 2 - Déroulé de la manipulation :**
   - Placer le curseur en fin de document (page 2, sous le dernier paragraphe ; retirer ou remplacer le titre d'attente `Comment contacter l'auteur` selon le modèle).
   - Ouvrir `Insertion > Table des matières et index > Table des matières, index ou bibliographie...`.
   - Dans l'onglet *Type* : sélectionner **`Index des illustrations`** et saisir le titre `Index des figures`.
   - Dans la zone *Créer à partir de* : cocher *Légendes*, choisir la catégorie **`Figure`**, et dans la liste *Afficher*, sélectionner **`Texte de référence`** (ce qui inclut la catégorie, le numéro de figure et le texte de la légende). Valider par *OK*.
   - **Test de mise à jour (Q6–Q7) :** Modifier le libellé d'une légende dans le corps du document (par exemple passer de `Fond vert` à `"fond vert"`), puis effectuer un **clic droit sur la table des illustrations > Mettre à jour l'index**. La ligne correspondante est immédiatement actualisée avec le nouveau texte et le numéro de page vérifié.
3. **Étape 3 - Résultat final et vérification :** La page 2 se termine par l'index aligné par points de suite :
   - `Figure 1: "fond vert" ............................................................. 1`
   - `Figure 2: "fond rose" ............................................................. 1`
   - `Figure 3: Productions de l'auteur ces dernières années .......................... 2`

> [!check]- Remarques méthodologiques et pièges à éviter
> - Contrairement aux renvois qui suivent souvent la renumérotation, un index (table des matières ou table des illustrations) n'est pas recalculé à chaque frappe pour des raisons de performance : il faut **toujours** penser à lancer `Mettre à jour l'index` avant l'export final.

---

### Exercice 6 : Export PDF et archivage ZIP
- **Catégorie :** Production des livrables finaux
- **Méthode de référence :** Export PDF natif et archivage ZIP

> [!abstract] Énoncé synthétique
> Produire la version PDF du document finalisé puis créer une archive ZIP contenant le fichier `.odt` et le fichier `.pdf` pour dépôt.

#### Résolution étape par étape
1. **Étape 1 - Identification des hypothèses :** Le document doit comporter deux pages conformes au modèle (`TD-TT-3-modele.pdf`), avec toutes les tables et champs à jour.
2. **Étape 2 - Déroulé de la manipulation :**
   - Lancer `Outils > Actualiser > Tout actualiser` (`F9`), puis sauvegarder le document `.odt` (`TD-TT-3-realise.odt`).
   - Exporter au format PDF via `Fichier > Exporter au format PDF...` pour générer `TD-TT-3-realise.pdf` (2 pages).
   - Compresser `TD-TT-3-realise.odt` et `TD-TT-3-realise.pdf` ensemble dans une archive `TD-TT-3-rendu.zip`.
3. **Étape 3 - Résultat final et vérification :** Les livrables `TD-TT-3-realise.odt`, `TD-TT-3-realise.pdf` (2 pages fidèles au modèle) et `TD-TT-3-rendu.zip` sont enregistrés et vérifiés dans `Attachments/TD3 Livrables/`.

> [!check]- Remarques méthodologiques et pièges à éviter
> - Toujours contrôler visuellement le PDF généré page par page pour s'assurer qu'aucune figure n'a déclenché un saut de page involontaire ni débordé des marges, et que le diagramme embarqué affiche bien l'ensemble des séries et années.

---

## Méthodes et fiches mobilisées
- Gestion de l'ancrage et de l'adaptation au texte des objets flottants : Exercice 1
- Importation de diagrammes OLE depuis LibreOffice Calc : Exercice 2
- Légendes, champs de séquence et styles de cadre dans LibreOffice Writer : Exercice 3
- Insertion de renvois vers des champs de séquence : Exercice 4
- Génération et actualisation d'un Index des illustrations : Exercice 5
- Export PDF natif et archivage ZIP : Exercice 6
