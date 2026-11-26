---
{"dg-publish":true,"permalink":"/la-fonction-d-offre-agregee/","ctime":"2026-11-25T18:50:11.269+01:00","mtime":"2026-11-25T19:52:39.581+01:00","dg-note-properties":{"date created":"2026-11-25, 18 50","date modified":"2026-11-25, 19 52","sector":"[[References/AES]]","semester":"[[References/S3]]","class":"[[References/Micro]]","form":"[[References/CM]]","part":"[[References/4]]"}}
---


# La fonction d'offre agrégée

> [!info] Précision terminologique
> Dans les notes manuscrites, le titre apparaît sous la forme *" fonction d'offre abridged "* (par opposition à l'offre *" non-abrégée "*). Il s'agit en microéconomie de la **fonction d'offre agrégée** du marché, obtenue par [[Agrégation horizontale\|Agrégation horizontale]] à partir de la [[Fonction d'offre individuelle\|fonction d'offre individuelle]] de chaque producteur.

---

## 1. Passage de l'offre individuelle à l'offre agrégée

On considère un marché composé de deux entreprises identiques $i \in \{1, 2\}$, produisant respectivement les quantités $Q_1$ et $Q_2$. On note $Q = Q_1 + Q_2$ la quantité totale offerte sur le marché et l'on cherche la **fonction inverse d'offre agrégée** $P_o(Q_1 + Q_2)$.

### A. Étape préliminaire : la fonction d'offre individuelle
Pour chaque entreprise $i$, la quantité optimale $Q_i^{**}$ qui maximise son profit vérifie la condition du premier ordre (égalité du prix au [[Coût marginal\|Coût marginal]]) :
$$p = C_i'(Q_i^{**})$$
On en déduit la **fonction inverse d'offre individuelle** :
$$P_{oi}(Q_i) = C_i'(Q_i)$$

### B. Règle fondamentale : ne jamais additionner les fonctions inverses
> [!warning] Piège classique à éviter
> La fonction inverse d'offre agrégée **n'est pas** la somme des fonctions inverses individuelles :
> $$P_o(Q_1 + Q_2) \neq P_{o1}(Q_1) + P_{o2}(Q_2)$$
> En effet, toutes les entreprises font face au **même prix $p$** : ce sont les **quantités** offertes $Q_1$ et $Q_2$ qui s'additionnent à prix constant ([[Agrégation horizontale\|Agrégation horizontale]]), et non les prix qui s'additionnent à quantité constante.

---

## 2. Méthode générale en 2 étapes (cas de courbes linéaires)

Lorsque les courbes d'offre individuelles sont des droites passant par l'origine, la fonction inverse d'offre agrégée est une droite affine de la forme :
$$P_o(Q_1 + Q_2) = a + b(Q_1 + Q_2) \quad \text{soit } P_o(Q) = a + bQ$$

Pour déterminer les paramètres $a$ (ordonnée à l'origine) et $b$ (pente), on compare deux points particuliers :

1. **Trouver $a$ à l'origine ($Q = 0$) :**
   - Lorsque $p = 0$, chaque entreprise offre une quantité nulle ($Q_1 = 0$ et $Q_2 = 0$), donc $P_{o1}(0) = P_{o2}(0) = 0$.
   - Les deux courbes individuelles passant par l'origine $(0, 0)$, la courbe agrégée passe également par l'origine :
     $$P_o(0) = P_{o1}(0) = 0 \implies a = 0$$
   - L'expression se réduit donc à : $P_o(Q_1 + Q_2) = b(Q_1 + Q_2)$.

2. **Trouver $b$ à prix égal (comparaison entre les points $A$ et $B$) :**
   - **Point $A$ (entreprise 1 seule, sous l'hypothèse $Q_2 = 0$) :** on choisit $Q_1 = 1$ et $Q_2 = 0$ (soit $Q_1 + Q_2 = 1$). Le prix correspondant sur la courbe individuelle est $p = P_{o1}(1)$.
   - **Point $B$ (les deux entreprises produisent au même prix $p$) :** au **même prix** $p = P_{o1}(1)$, l'entreprise 2 identique offre elle aussi $Q_2 = 1$, d'où une quantité totale offerte sur le marché de $Q_1 + Q_2 = 1 + 1 = 2$.
   - En égalisant les prix aux points $A$ et $B$ :
     $$P_o(2) = P_{o1}(1) \implies 2b = P_{o1}(1) \implies b = \frac{P_{o1}(1)}{2}$$

> [!tip] Interprétation graphique
> À un même niveau de prix $p$, la quantité totale offerte sur le marché est doublée par rapport à l'offre d'une seule firme ($Q = 2$ au lieu de $Q_1 = 1$). Graphiquement, la droite d'offre agrégée $P_o(Q)$ est donc **deux fois moins pentue** (plus aplatie) que chaque droite d'offre individuelle $P_{oi}(Q_i)$.

---

## 3. Applications du cours

### Exemple 1 : $C_i(Q_i) = Q_i^2 + 1000$ ($i \in \{1, 2\}$)

> [!example] Résolution pas à pas — Exemple 1
> 1. **Offre individuelle :**
>    Pour chaque firme $i$, $p = C_i'(Q_i^{**}) = 2Q_i^{**}$, d'où la fonction inverse d'offre individuelle :
>    $$P_{oi}(Q_i) = 2Q_i$$
>    Si $p = 0$, alors $Q_1 = 0$ et $Q_2 = 0$ : les deux droites passent par l'origine.
> 2. **Calcul de $a$ :**
>    Comme $P_{o1}(0) = P_{o2}(0) = 0$, on a $P_o(0) = a = 0$, soit $P_o(Q_1 + Q_2) = b(Q_1 + Q_2)$.
> 3. **Calcul de $b$ :**
>    - Point $A$ ($Q_1 = 1, Q_2 = 0$) : $P_{o1}(1) = 2 \times 1 = 2$.
>    - Point $B$ ($Q_1 = 1, Q_2 = 1 \implies Q = 2$) : $P_o(2) = 2b$.
>    - Égalité des prix : $P_o(2) = P_{o1}(1) \implies 2b = 2 \implies b = 1$.
> 4. **Fonction inverse d'offre agrégée :**
>    $$P_o(Q) = Q \quad \text{(soit } P_o(Q_1 + Q_2) = Q_1 + Q_2\text{)}$$

*(Vérification algébrique directe : $p = 2Q_i \implies Q_i(p) = \frac{p}{2}$, d'où $Q = Q_1 + Q_2 = \frac{p}{2} + \frac{p}{2} = p \implies P_o(Q) = Q$.)*

### Exemple 2 : $C_i(Q_i) = \frac{1}{2}Q_i^2$ ($i \in \{1, 2\}$)

> [!example] Résolution pas à pas — Exemple 2
> 1. **Offre individuelle :**
>    Pour chaque firme $i$, $p = C_i'(Q_i^{**}) = \frac{1}{2} \cdot 2Q_i^{**} = Q_i^{**}$, d'où :
>    $$P_{oi}(Q_i) = Q_i$$
> 2. **Calcul de $a$ :**
>    $P_o(0) = a$ et $P_o(0) = 0$ (courbes passant par l'origine) $\implies a = 0$, d'où $P_o(Q_1 + Q_2) = b(Q_1 + Q_2)$.
> 3. **Calcul de $b$ :**
>    - Point $A$ ($Q_1 = 1$, sous l'hypothèse $Q_2 = 0$) : $P_{o1}(1) = 1$.
>    - Point $B$ ($Q_1 = 1$ et $Q_2 = 1 \implies Q_1 + Q_2 = 2$) : $P_o(1 + 1) = P_o(2) = 2b$.
>    - Égalité des prix : $2b = 1 \implies b = \frac{1}{2}$.
> 4. **Fonction inverse d'offre agrégée :**
>    $$P_o(Q) = \frac{1}{2}Q$$

*(Vérification algébrique directe : $p = Q_i \implies Q_i(p) = p$, d'où $Q = Q_1 + Q_2 = 2p \implies P_o(Q) = \frac{1}{2}Q$. Sur le repère $(Q, p)$, la courbe agrégée $P_o(Q) = \frac{1}{2}Q$ est bien deux fois plus plate que la courbe individuelle $P_{o1}(Q_1) = Q_1$.)*

---

## Liens associés
- [[Coût marginal\|Coût marginal]]
- [[Fonction d'offre individuelle\|Fonction d'offre individuelle]]
- [[Agrégation horizontale\|Agrégation horizontale]]
- [[Introduction -Microéconomie\|Introduction -Microéconomie]]
- [[Microéconomie - Plan\|Microéconomie - Plan]]
- [[Drive/Josepha/S3/microéconomie de la production/Chapitre 3 - Etude de la fonction de coût\|Chapitre 3 - Etude de la fonction de coût]]
