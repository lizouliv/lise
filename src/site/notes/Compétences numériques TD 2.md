---
{"dg-publish":true,"permalink":"/competences-numeriques-td-2/","ctime":"2026-11-14T12:11:12.586+01:00","mtime":"2026-11-14T12:11:12.586+01:00","dg-note-properties":{"date created":"2026-11-14, 12 10","date modified":"2026-11-14, 12 10","sector":"[[References/AES]]","semester":"[[References/S3]]","class":"[[References/Compétences numériques]]","form":"[[References/TD]]","part":"[[References/2]]"}}
---


[[TD-TT-1.pdf|TD-TT-1.pdf]]
[[TD-TT-1-modele.pdf|TD-TT-1-modele.pdf]]

# TD 2 : Traitement de texte — Maîtrise des styles (LibreOffice Writer)
**Sujet support :** *TD Thématique Traitement de texte – Séance 01* (`TD-TT-1`) — Antoine Widlöcher, Pierre Beust, Isabelle Duchatelle.

---

## Livrables prêts à l'emploi (Dossier `Attachments/TD2 Livrables/`)
- **Document ODT mis en forme (3 pages) :** `Attachments/TD2 Livrables/TD-TT-1-realise.odt`
- **Document PDF exporté (3 pages) :** `Attachments/TD2 Livrables/TD-TT-1-realise.pdf`
- **Archive ZIP finale à déposer :** `Attachments/TD2 Livrables/TD-TT-1-rendu.zip`

---

## Résolution synthétique du TD

### Exercice 1 : Préparation de l'environnement et importation des données brutes
- **Catégorie :** Initialisation documentaire et séparation contenu / forme
- **Méthode de référence :** Importation de texte brut dans LibreOffice Writer

> [!abstract] Énoncé synthétique
> Créer un répertoire de travail dédié, récupérer les fichiers de la séance (`TD-TT-1.pdf`, `TD-TT-1-modele.pdf`, `TD-TT-1-donnees.txt`), créer un document `.odt` vierge dans LibreOffice Writer et y copier le contenu texte brut sans mise en forme préalable.

#### Résolution étape par étape
1. **Étape 1 - Identification des hypothèses :** Le fichier `TD-TT-1-donnees.txt` contient uniquement du texte brut encodé en UTF-8 (29 lignes : titre, sous-titre, résumé, titres de section et sous-section, paragraphes, citations longues et listes), dépourvu de tout formatage.
2. **Étape 2 - Déroulé de la manipulation :**
   - Créer un sous-répertoire dédié dans l'espace de travail et y placer les fichiers téléchargés.
   - Ouvrir LibreOffice Writer (`Fichier > Nouveau > Document texte`) et enregistrer immédiatement le document au format natif `.odt` (`Ctrl + S` régulier).
   - Ouvrir `TD-TT-1-donnees.txt`, tout sélectionner (`Ctrl + A`), copier (`Ctrl + C`), puis coller dans le document Writer (`Ctrl + V`, ou collage spécial texte non formaté).
3. **Étape 3 - Résultat final et vérification :** Le document contient les 29 paragraphes bruts prêts à être structurés exclusivement à l'aide des styles.

> [!check]- Remarques méthodologiques et pièges à éviter
> - Ne jamais appliquer de mise en forme directe (gras, taille, alignement via la barre d'outils) avant d'avoir posé l'architecture logique par les styles.
> - Sauvegarder dès l'ouverture sous le format natif `.odt` pour conserver l'intégralité des styles hiérarchiques et paramètres de page de Writer.

---

### Exercice 2 : Application des styles prédéfinis et insertion de la table des matières
- **Catégorie :** Structuration logique par styles natifs (paragraphes, caractères, listes, page)
- **Méthode de référence :** Application des styles prédéfinis et génération d'index

> [!abstract] Énoncé synthétique
> Appliquer les styles de paragraphes prédéfinis selon la stratégie du continuum (*Corps de texte*, *Titre principal*, *Sous-titre*, *Titre 1*, *Titre 2*, *Citation*), appliquer les styles de caractères (*Citation*, *Accentuation forte*) et de listes (*Puce 1*, *Numérotation 1*) avec insertion des espaces insécables requis, appliquer le style de page *Première page*, puis insérer une table des matières après le résumé.

#### Résolution étape par étape
1. **Étape 1 - Identification des hypothèses :** L'application de styles prédéfinis attribue un rôle sémantique à chaque bloc avant toute personnalisation visuelle. Le volet latéral *Styles* s'ouvre avec `F11`.
2. **Étape 2 - Déroulé de la manipulation :**
   - **Stratégie du continuum (paragraphes) :** Sélectionner tout le document (`Ctrl + A`) et appliquer le style de paragraphe *Corps de texte* (*Text body*), qui est le style majoritaire. Marquer ensuite les ruptures : *Titre principal* sur la ligne 1, *Sous-titre* sur la ligne 2, *Titre 1* sur « Un titre de section » et « Un autre titre de section », *Titre 2* sur « Un titre de sous-section » et « Un autre titre de sous-section », et *Citation* sur les deux paragraphes commençant par « Une citation porteuse... ».
   - **Styles de caractères :** À la fin du premier paragraphe de corps de texte, encadrer `ce contenu est quelconque, mais réaliste` de guillemets français `« ... »` avec espaces insécables (`Ctrl + Maj + Espace`), puis appliquer le style de caractères *Citation*. Sélectionner la première occurrence du mot `réaliste` dans ce même paragraphe et lui appliquer le style de caractères *Accentuation forte*.
   - **Styles de listes et typographie française :** Appliquer le style de liste *Puce 1* aux 4 items de la liste non numérotée et *Numérotation 1* aux 4 items de la liste numérotée. En typographie française, insérer une espace insécable (`Ctrl + Maj + Espace`) avant les ponctuations doubles (`:` et `;`) qui en sont dépourvues, notamment en fin d'items (`...non numérotée ;`, `...numérotée ;`) et autour des guillemets `« ... »`, afin d'éviter qu'un signe de ponctuation ne soit renvoyé seul en début de ligne.
   - **Style de page et table des matières :** Placer le curseur sur la première page et double-cliquer sur le style de page *Première page*. Placer ensuite le curseur après le texte du résumé, puis ouvrir `Insertion > Table des matières et index > Table des matières, index ou bibliographie...` et valider pour générer la table des matières basée sur les styles *Titre 1* et *Titre 2*.
3. **Étape 3 - Résultat final et vérification :** Le document possède une structure hiérarchique complète, une table des matières dynamique et une première page distincte, sans aucun formatage direct.

> [!check]- Remarques méthodologiques et pièges à éviter
> - Dans LibreOffice Writer, le style de paragraphe *Citation* (*Quotations*) et le style de caractères *Citation* (*Quotation*) portent le même nom français mais se trouvent dans deux onglets distincts du panneau `F11` (onglet Paragraphes vs onglet Caractères).
> - Les espaces insécables s'affichent avec un fond grisé lorsque les marques de formatage (`Ctrl + F10`) sont activées, ce qui facilite la vérification.

---

### Exercice 3 : Modification des styles prédéfinis et mécanisme d'héritage
- **Catégorie :** Personnalisation de styles hiérarchiques et règles typographiques
- **Méthode de référence :** Héritage et cascade des styles dans LibreOffice Writer

> [!abstract] Énoncé synthétique
> Filtrer les *Styles appliqués*, modifier le style parent des titres pour basculer vers une police à empattements, configurer l'aspect des titres, du corps de texte, des citations longues, de la table des matières, des styles de caractères et des listes, et répondre aux questions théoriques sur l'héritage, la continuité des bordures et les coupures de mots.

#### Résolution étape par étape
1. **Étape 1 - Identification des hypothèses :** Les styles de paragraphes forment une arborescence d'héritage : toute propriété non surchargée dans un style enfant est héritée de son style parent. En bas du panneau `F11`, sélectionner le filtre **Styles appliqués**.
2. **Étape 2 - Déroulé de la manipulation et réponses aux questions :**
   - **Hiérarchie des titres (Q2–Q4) :** Pour appliquer une police à empattements (ex. *Times New Roman* ou *Liberation Serif*) à l'ensemble des titres en une seule opération, il faut modifier le style parent **`Titre`** (*Heading*). En effet, *Titre principal*, *Sous-titre*, *Titre 1*, *Titre 2* et même **`Titre de table des matières`** (*Contents Heading*) héritent tous directement ou indirectement du style *Titre* : c'est la raison pour laquelle le titre « Table des matières » bascule automatiquement vers la police à empattements dès que *Titre* est modifié.
   - **Titre principal et Sous-titre (Q5–Q8) :**
     - Modifier *Titre principal* : taille `20 pt`, gras, aligné à droite, espacement en dessous `0,4 cm`, bordure à droite espacée de `0,5 cm` du texte.
     - Modifier *Sous-titre* : aligné à droite, bordure à droite espacée de `0,5 cm` du texte.
     - **Continuité du trait de bordure (Q8) :** Dans l'onglet *Bordures* des deux styles, cocher **« Fusionner avec le style de paragraphe suivant »** (`style:join-border="true"`) tout en conservant exactement le même style/épaisseur/couleur de trait, le même retrait droit (`0 cm`) et le même espacement au texte (`0,5 cm`). L'espacement vertical de `0,4 cm` doit être porté par le retrait/espacement interne (padding bas) ou les marges fusionnées afin qu'aucune coupure blanche n'interrompe la ligne verticale.
   - **Titres de section et sous-section (Q9–Q10) :** Modifier *Titre 1* (espacement au-dessus `0,8 cm`) et *Titre 2* (retrait avant le texte / à gauche `0,5 cm`, style de police *Normal* / sans italique).
   - **Corps de texte et coupures de mots françaises (Q11–Q12) :** Modifier *Corps de texte* : alignement *Justifié*, taille `10 pt`, retrait de première ligne `0,5 cm`, coupure automatique des mots activée (onglet *Enchaînements*), traitement des lignes veuves et orphelines fixé à `2` lignes. Les coupures de mots respectent automatiquement la typographie française parce que le dictionnaire de césure utilisé est déterminé par la propriété **Langue** (*Français (France)*) définie dans l'onglet *Police* du style parent.
   - **Citations longues et Table des matières (Q13–Q14) :** Modifier *Citation* (*Quotations*) : `10 pt`, italique, retrait gauche porté à `2 cm`, justifié, césure automatique et veuves/orphelines à `2` lignes. Modifier les styles *Table des matières niveau 1* et *Table des matières niveau 2* pour fixer leur taille à `8 pt`.
   - **Styles de caractères et de listes :** Consulter *Citation* (italique) sans le modifier ; modifier *Accentuation forte* pour passer de *Gras* à *Italique*. Modifier *Puce 1* : onglet *Position* (`Aligné à : 0,5 cm`, `Numérotation suivie par : Espace`, `Retrait à : 0,9 cm`) et onglet *Personnaliser* (choisir un tiret demi-cadratin `–` dans la police du corps de texte, bloc *Ponctuation générale*). Modifier *Numérotation 1* avec les mêmes retraits (`0,5 cm` / `0,9 cm`, suivi d'un espace) et le format de numérotation alphabétique minuscule avec parenthèse (`a)`, `b)`, `c)`...).
3. **Étape 3 - Résultat final et vérification :** L'ensemble de la hiérarchie typographique, des césures françaises et des listes reproduit fidèlement la mise en page du modèle.

> [!check]- Remarques méthodologiques et pièges à éviter
> - Si une propriété (par exemple la police sur *Sous-titre*) a été modifiée manuellement sur un enfant, l'héritage depuis *Titre* est rompu pour cet attribut ; il faut alors cliquer sur le bouton *Standard* dans l'onglet concerné du style enfant pour restaurer l'héritage.
> - Pour des listes à puces propres, utiliser `Position` (`Aligné à` / `Retrait à` / `Suivi par Espace`) plutôt que des tabulations par défaut qui créent un décalage excessif.

---

### Exercice 4 : Styles de pages, enchaînements cycliques, marges et en-têtes/pieds de page
- **Catégorie :** Mise en page avancée et pagination recto-verso
- **Méthode de référence :** Enchaînement de styles de pages et tabulations d'en-tête/pied de page

> [!abstract] Énoncé synthétique
> Paramétrer les pieds de page, enchaîner les styles *Première page*, *Page gauche* et *Page droite*, uniformiser les marges ($3\text{ cm}$ haut/bas, $4\text{ cm}$ gauche/droite), corriger la tabulation du pied de page à $6{,}5\text{ cm}$, fixer la taille des en-têtes/pieds de page à $9\text{ pt}$, insérer le rappel de section en en-tête de *Page droite* et ajouter les filets de bordure.

#### Résolution étape par étape
1. **Étape 1 - Identification des hypothèses :** En format A4 ($21\text{ cm} \times 29{,}7\text{ cm}$), des marges gauche et droite de $4\text{ cm}$ réduisent la largeur utile de la zone de texte de $17\text{ cm}$ (marges par défaut de $2\text{ cm}$) à :
   $$21 - 2 \times 4 = 13\text{ cm}$$
   Le milieu exact de la ligne vaut donc $\frac{13}{2} = 6{,}5\text{ cm}$ et le bord droit se situe à $13\text{ cm}$.
2. **Étape 2 - Déroulé de la manipulation et réponses aux questions :**
   - **Pied de page de Première page (Q1–Q3) :** Activer le pied de page dans le style *Première page*. Au centre (après une tabulation), insérer les champs `Numéro de page` / `Nombre de pages` ; à droite (après une seconde tabulation), insérer le champ `Date` au format long (`1 janvier 2000`, donnant ici `14 novembre 2026`).
   - **Enchaînement des styles de pages (Q4–Q6) :**
     - En réglant le *Style de suite* de *Première page* sur *Page gauche* (Q4), la page 2 adopte automatiquement *Page gauche* (le pied de page disparaît provisoirement car *Page gauche* n'en a pas encore).
     - En ajoutant des pages à la fin du document (Q5), la page 3 repasse au *Style par défaut* car *Page gauche* a par défaut *Style par défaut* comme style de suite.
     - En réglant le *Style de suite* de *Page gauche* sur *Page droite* (Q6), la page 3 prend *Page droite*, mais il faut **également régler le *Style de suite* de *Page droite* sur *Page gauche*** afin de boucler l'alternance cyclique gauche/droite sur toutes les pages ultérieures.
   - **Marges et décalage du numéro de page (Q7–Q12) :**
     - Définir les marges à `3 cm` (haut/bas) et `4 cm` (gauche/droite) sur *Première page*, *Page gauche* et *Page droite*.
     - **Observation (Q8) :** Le numéro de page de la page 1 apparaît décalé vers la droite. En effet, les tabulations du style de paragraphe *Pied de page* étaient calibrées sur l'ancienne largeur utile ($17\text{ cm}$ : centre à $8{,}5\text{ cm}$, droite à $17\text{ cm}$). Avec des marges de $4\text{ cm}$, $8{,}5\text{ cm} > 6{,}5\text{ cm}$ et $17\text{ cm}$ dépasse la marge droite, repoussant la date à la ligne suivante ou hors zone.
     - **Correction (Q9–Q12) :** Modifier le style de paragraphe *Pied de page* : placer le taquet de tabulation centré à `6,5 cm` et le taquet droit à `13 cm`, puis fixer la taille de police à `9 pt`. Lorsqu'on active ensuite le pied de page sur *Page gauche* et *Page droite* en y insérant la pagination après une tabulation, le numéro se centre immédiatement à `6,5 cm` sans aucun réglage supplémentaire car les trois styles de page partagent le même style de paragraphe *Pied de page*.
   - **En-tête de Page droite et bordures (Q13–Q15) :** Activer l'en-tête uniquement sur *Page droite*, saisir deux tabulations pour aligner à droite, puis insérer `Insertion > Champ > Autres champs > Document > Chapitre` (Format : *Nom du chapitre*, Niveau : `1`). Modifier le style de paragraphe *En-tête* à `9 pt` (taquets à `6,5 cm` et `13 cm`), ajouter une bordure inférieure sur *En-tête* et une bordure supérieure sur *Pied de page*.
3. **Étape 3 - Résultat final et vérification :** Le document comporte exactement 3 pages : la page 1 (`1/3`, date à droite), la page 2 (`2/3`, sans en-tête) et la page 3 (`3/3`, avec le rappel `Un autre titre de section` en en-tête).

> [!check]- Remarques méthodologiques et pièges à éviter
> - Ne pas confondre le *style de page* (qui gère les marges, l'orientation et l'activation/contenu des en-têtes et pieds de page) avec les *styles de paragraphe* `En-tête` et `Pied de page` (qui gèrent la police, les tabulations et les bordures du texte qu'ils contiennent).
> - Toujours vérifier le sens des deux flèches de suite : `Page gauche` $\leftrightarrow$ `Page droite`.

---

### Exercice 5 : Création de styles personnalisés de paragraphes et de caractères
- **Catégorie :** Extension de la feuille de styles et recherche ciblée
- **Méthode de référence :** Création de styles personnalisés par héritage et lettrines

> [!abstract] Énoncé synthétique
> Créer quatre styles de paragraphes personnalisés (*Corps de texte - Premier bloc*, *Citation à retenir*, *Titre du résumé*, *Résumé*) et un style de caractères (*Nom propre de personne*), puis appliquer ce dernier à toutes les occurrences de « Platon » via l'outil de recherche.

#### Résolution étape par étape
1. **Étape 1 - Identification des hypothèses :** Chaque style personnalisé doit s'inscrire dans la chaîne d'héritage existante afin de bénéficier automatiquement des polices, langues et règles de césure du document.
2. **Étape 2 - Déroulé de la manipulation :**
   - **`Corps de texte - Premier bloc` :** Créer à partir de *Corps de texte* (`F11` > Clic droit > *Nouveau*), définir *Corps de texte* comme *Style de suite*, supprimer le retrait de première ligne (`0 cm`) et activer une **Lettrine** (onglet *Lettrines* : 1 caractère sur 2 lignes). Mettre à jour le *Style de suite* de *Titre 1* et *Titre 2* vers `Corps de texte - Premier bloc`, puis appliquer ce style au premier paragraphe de chaque section et sous-section.
   - **`Citation à retenir` :** Créer à partir de *Citation* (*Quotations*), ajouter une bordure à droite espacée de `0,5 cm` du texte, et **diminuer le retrait droit de `0,5 cm`** (de `2 cm` à `1,5 cm`) afin que la bordure soit décalée vers l'extérieur tout en maintenant l'alignement droit du texte au niveau des citations ordinaires. L'appliquer à la seconde citation longue.
   - **`Titre du résumé` et `Résumé` :**
     - *Titre du résumé* : centré, `10 pt` gras, espacement au-dessus `1 cm`, retraits gauche et droite `2 cm`, bordure supérieure espacée de `0,4 cm`.
     - *Résumé* : héritier de `Corps de texte - Premier bloc` (ce qui lui confère la lettrine `V`), `8 pt` italique, espacement en dessous `1 cm`, retraits gauche et droite `2 cm`, bordure inférieure espacée de `0,4 cm`.
     - **Coupures de mots dans le résumé (Q9) :** Vérifier dans l'onglet *Enchaînements* du style `Résumé` que l'option *Coupure des mots : Automatiquement* est cochée (elle est héritée de *Corps de texte* via `Corps de texte - Premier bloc`, mais indispensable sur un bloc étroit de `8 pt`).
   - **`Nom propre de personne` (style de caractères) :** Créer un style de caractères avec *Effets de caractères > Casse : Petites majuscules*. Ouvrir *Rechercher et remplacer* (`Ctrl + H`), saisir `Platon`, cliquer sur **Tout rechercher** pour sélectionner simultanément les 4 occurrences dans le document, puis double-cliquer sur `Nom propre de personne` dans le panneau `F11`.
3. **Étape 3 - Résultat final et vérification :** Les lettrines, l'encadré horizontal du résumé, le filet vertical de la citation importante et les petites majuscules sur `Platon` correspondent exactement au modèle.

> [!check]- Remarques méthodologiques et pièges à éviter
> - Dans un style hérité comme `Résumé`, toute propriété laissée inchangée reste liée au parent ; si les coupures ne s'appliquent pas, vérifier que le style parent ou la langue (`Français`) n'a pas été surchargé.
> - Le bouton *Tout rechercher* de `Ctrl + H` est la méthode la plus rapide et la plus fiable pour appliquer un style de caractères en une seule passe sans oubli.

---

### Exercice 6 : Discussion méthodologique, nommage des styles et archivage ZIP
- **Catégorie :** Ingénierie documentaire, bonnes pratiques de nommage et export
- **Méthode de référence :** Conception sémantique d'une feuille de styles et export PDF/ZIP

> [!abstract] Énoncé synthétique
> Répondre aux trois questions méthodologiques de la section *Discussion* (nommage logique vs visuel, abstraction des styles prédéfinis, convention de nommage), puis exporter le document en PDF et produire l'archive ZIP de rendu.

#### Résolution étape par étape
1. **Étape 1 - Identification des hypothèses :** La séparation entre le fond (rôle sémantique) et la forme (rendu typographique) constitue le principe directeur de la rédaction structurée.
2. **Étape 2 - Déroulé des réponses argumentées et export :**
   - **Q1 — Nommage logique vs propriétés visuelles :** Non, les noms de styles ne doivent **pas** décrire leur mise en forme visuelle. Nommer un style *Corps de texte avec lettrine* pose un problème de maintenance : si l'auteur décide ultérieurement de remplacer la lettrine par un fond coloré ou un gras initial pour distinguer le début des sections, le nom du style devient contradictoire avec son apparence. Le nom logique **`Corps de texte - Premier bloc`** décrit le *rôle structurel* du paragraphe (ouvrir une section) et reste juste quelle que soit son évolution graphique.
   - **Q2 — S'abstraire totalement des styles prédéfinis et intérêt :** Pour s'affranchir des styles prédéfinis, il faut créer ses propres styles personnalisés (en les faisant éventuellement hériter directement de *Style par défaut* ou d'un style racine personnalisé) pour l'ensemble des composants du document, et reconfigurer les outils automatiques (notamment `Outils > Numérotation des chapitres` et les options de la Table des matières) pour qu'ils pointent vers ces styles personnalisés plutôt que vers *Titre 1*, *Titre 2*, etc. **Intérêts :** maîtrise totale de l'arborescence d'héritage sans effets de bord cachés d'une version à l'autre du logiciel, indépendance vis-à-vis de la langue d'interface (noms unifiés français/anglais), et portabilité exacte d'un modèle éditorial d'entreprise.
   - **Q3 — Convention de nommage pour repérer les styles personnalisés :** Utiliser un **préfixe commun court** (par exemple `Perso_` ou `Doc_` ou `00_`, comme `Perso_TitreResume`, `Perso_CitationRetenir`). Comme les listes de styles de LibreOffice sont triées par ordre alphabétique, tous les styles personnalisés se retrouvent instantanément regroupés en un seul bloc contigu, tout en restant visibles dans l'affichage *Styles appliqués* ou *Styles personnalisés*.
   - **Export PDF et archivage :** Exporter au format PDF via `Fichier > Exporter au format PDF...` (`TD-TT-1-realise.pdf`), puis regrouper `TD-TT-1-realise.odt` et `TD-TT-1-realise.pdf` dans l'archive `TD-TT-1-rendu.zip`.
3. **Étape 3 - Résultat final et vérification :** Les livrables `TD-TT-1-realise.odt`, `TD-TT-1-realise.pdf` (3 pages conformes au modèle) et `TD-TT-1-rendu.zip` sont validés dans `Attachments/TD2 Livrables/`.

> [!check]- Remarques méthodologiques et pièges à éviter
> - Bien vérifier avant l'export PDF que la table des matières a été mise à jour (`Clic droit > Mettre à jour l'index`) afin que tous les numéros de page soient exacts.

---

## Méthodes et fiches mobilisées
- Importation de texte brut dans LibreOffice Writer : Exercice 1
- Application des styles prédéfinis et génération d'index : Exercice 2
- Héritage et cascade des styles dans LibreOffice Writer : Exercice 3
- Enchaînement de styles de pages et tabulations d'en-tête/pied de page : Exercice 4
- Création de styles personnalisés par héritage et lettrines : Exercice 5
- Conception sémantique d'une feuille de styles et export PDF/ZIP : Exercice 6
