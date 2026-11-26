---
{"dg-publish":true,"permalink":"/entrainement-fiscalite-bic-is-ir/","ctime":"2026-11-20T02:16:27.581+01:00","mtime":"2026-11-20T13:37:43.086+01:00","dg-note-properties":{"date created":"2026-11-20, 2 16","date modified":"2026-11-20, 13 37","sector":"[[References/AES]]","semester":"[[References/S3]]","class":"[[References/Fiscal]]","form":"[[References/TD]]","part":null}}
---


# Entraînement Fiscalité — BIC, IS, IR

> [!info] Suivi de l'épreuve blanche *(sans TVA — / 20 points)*
> - **Exercice 1 — BIC (8 pts) :** Terminé et corrigé *(note initiale : $2{,}75/8$, puis calcul final validé à $141\,150\text{ €}$ + $25\,000\text{ €}$ de PVLT)*.
> - **Exercice 2 — IS (7 pts) :** **À faire ci-dessous** *(pense à écrire " fini " quand tu envoies ta réponse)*.
> - **Exercice 3 — IR (5 pts) :** À venir juste après la correction de l'Exercice 2.

---

## 1. Les 4 réflexes clés débloqués en BIC (et utiles pour l'IS)

1. **" Déductible $\neq$ `−` " (`R.A.F. = 0 €`) :**
   - Quand une charge est déjà comptabilisée et qu'elle est **déductible**, le comptable l'a déjà soustraite $\rightarrow$ **`0 €` (R.A.F.)**, ne jamais la retrancher une 2e fois !
   - On ne **réintègre (`+`)** que les charges non déductibles (ou un produit imposable oublié en compta).
   - On ne **déduit (`−`)** que les produits déjà comptabilisés mais exonérés / rattachés à une autre année / taxés à part (ou une charge déductible oubliée).
2. **Formule du résultat fiscal :**
   $$\text{Résultat fiscal} = \text{Bénéfice comptable} + \text{Réintégrations} - \text{Déductions}$$
3. **Prorata temporis :**
   - Dès qu'un bien est acquis ou mis en service en cours d'année, découper l'annuité ($\frac{\text{jours}}{360}$ en linéaire, mois complets de 30 jours).
4. **Cessions et [[Plus-value\|plus-values]] :**
   - $\text{VNC} = \text{Prix d'achat} - \text{Amortissements}$
   - $\text{PV (ou MV) totale} = \text{Prix de vente} - \text{VNC}$
   - En BIC ($\ge 2\text{ ans}$, bien amortissable) : $\text{PVCT} = \min(\text{PV} ; \text{Amortissements})$ et $\text{PVLT} = \text{PV totale} - \text{PVCT}$ (sortie du résultat BIC par `− PVLT` pour être taxée à part à taux réduit).
   - **Piège voiture :** pour calculer la $\text{VNC}$ lors d'une cession, on ignore totalement le plafond $\text{CO}_2$ (on retient les vrais amortissements comptables).
   - **Basculer vers l'IS :** à l'IS, la distinction CT/LT **disparaît** pour les locaux/terrains/machines ordinaires, **sauf** pour les **titres de participation** détenus $\ge 2\text{ ans}$.

> [!success]- Corrigé complet de l'Exercice 1 — BIC (*L'Atelier Normand*, 2025)
> **Bénéfice comptable initial :** $120\,000\text{ €}$
>
> | Op. | Détail | Réintégrations (`+`) | Déductions (`−`) | Règle & Justification |
> | :---: | :--- | :---: | :---: | :--- |
> | **A** | Rémunération exploitant ($24\,000$) / épouse ($18\,000$) | **$+ 24\,000\text{ €}$** | — | Patron non déductible en EI ; conjoint salarié à temps plein déductible (**Art. 154 CGI** $\rightarrow 0\text{ €}$) |
> | **B** | Imprimante ($420$) + Ordi ($1\,200$, 1er oct., 3 ans) | **$+ 1\,200\text{ €}$** | **$- 100\text{ €}$** | Imprimante $\le 500\text{ € HT}$ ($0\text{ €}$) ; ordi $> 500\text{ € HT}$ immobilisé, amort. 3 mois : $1\,200 \times \frac{1}{3} \times \frac{90}{360} = 100\text{ €}$ |
> | **C** | Véhicule tourisme $35\text{ g}$ ($32\,300\text{ € TTC}$, 1er juill., 5 ans) | **$+ 1\,200\text{ €}$** | — | Plafond $20\,300\text{ €}$ (**[[Art. 39 CGI\|Art. 39-4 CGI]]**), $6\text{ mois}$ : $(32\,300 - 20\,300) \times 20\% \times \frac{180}{360} = 1\,200\text{ €}$ |
> | **D** | Partie de chasse ($6\,000$) / 50 coffrets ($1\,500$) | **$+ 6\,000\text{ €}$** | — | Chasse somptuaire interdite (**[[Art. 39 CGI\|Art. 39-4 CGI]]**) ; coffrets à $30\text{ € TTC}$ déductibles ($0\text{ €}$) |
> | **E** | CET ($2\,800$) / IR ($4\,500$) / Amende ($350$) | **$+ 4\,850\text{ €}$** | — | CET pro déductible ($0\text{ €}$) ; IR perso non déductible ; amende exclue (**[[Art. 39 CGI\|Art. 39-2 CGI]]**) |
> | **F** | Prov. licenciement éco ($10\,000$) / client ($4\,000$) | **$+ 10\,000\text{ €}$** | — | Licenciement éco exclu (**[[Art. 39 CGI\|Art. 39-1 5° CGI]]**) ; client en liquidation probable ($0\text{ €}$) |
> | **G** | Abandon de créance à un ami ($5\,000$) | **$+ 5\,000\text{ €}$** | — | Acte anormal de gestion (étranger à l'exploitation) |
> | **H** | Acompte encaissé en déc. 2025 (livraison févr. 2026) | — | **$- 6\,000\text{ €}$** | Produit rattaché à la livraison en 2026 (**[[Art. 38 CGI\|Art. 38-2 bis CGI]]**) |
> | **I** | Cession local acquis 2018 à $65\,000$, amorti $20\,000$, vendu $90\,000$ | — | **$- 25\,000\text{ €}$** | $\text{VNC} = 45\,000$, $\text{PV} = 45\,000$. $\text{PVCT} = 20\,000$ (reste dans BIC) ; $\text{PVLT} = 25\,000$ (taxée à part) |
> | **Total** | **Totaux extra-comptables** | **$+ 52\,250\text{ €}$** | **$- 31\,100\text{ €}$** | **Net : $+ 21\,150\text{ €}$** |
>
> - **Résultat fiscal BIC (barème IR) :** $120\,000 + 52\,250 - 31\,100 = \mathbf{141\,150\text{ €}}$
> - **Sort de la PVLT ($25\,000\text{ €}$) :** Imposée séparément au taux réduit ($12{,}8\%$ + prélèvements sociaux, soit $30\% = 7\,500\text{ €}$, ou $19\%$ selon l'ancien taux du cours).

---

## 2. Exercice 2 / 3 — IS : Du BIC vers l'IS et liquidation *(7 points)*

**Énoncé :**
La **SA " NORMA TECH "** (soumise à l'[[Lexis 360/Fiscal/Lexis - L'impôt sur les sociétés\|IS]], exercice = année civile **2025**) réalise un **chiffre d'affaires HT de $12\,000\,000\text{ €}$**. Son capital de $500\,000\text{ €}$ est **entièrement libéré** et détenu à **$80\%$** par des personnes physiques.

Le **bénéfice comptable avant IS** de l'exercice 2025 s'élève à **$300\,000\text{ €}$**. Toutes les opérations ci-dessous ont été comptabilisées *(sauf mention contraire)* :

- **A —** La SA a versé et comptabilisé en charges **$60\,000\text{ €}$** de rémunération au PDG (travail effectif, montant non excessif) et **$25\,000\text{ €}$** d'acompte d'**impôt sur les sociétés (IS)** enregistré en charges d'impôts.
- **B —** Le **1er avril 2025**, la SA a acquis et mis en service un véhicule de tourisme émettant **$180\text{ g}$ de $\text{CO}_2/\text{km}$** pour **$29\,900\text{ € TTC}$**, amorti en linéaire sur **5 ans** (dotation comptable 2025 enregistrée). Elle a également comptabilisé **$1\,200\text{ €}$** d'amende URSSAF pour retard de déclaration.
- **C —** La SA a perçu et enregistré en produits financiers :
  - **$100\,000\text{ €}$** de dividendes de sa filiale française SAS BETA, détenue à **$15\%$** en pleine propriété depuis **4 ans** *(régime mère-fille)* ;
  - **$20\,000\text{ €}$** de dividendes d'une société cotée dans laquelle elle détient **$1\%$** du capital *(titres de placement)*.
- **D —** En septembre 2025, la SA a cédé deux immobilisations acquises en **2019** *(plus-values déjà incluses dans les $300\,000\text{ €}$)* :
  - Un **terrain nu** acheté $80\,000\text{ €}$ et revendu $110\,000\text{ €}$ ;
  - Des **titres de participation** ($20\%$ d'une filiale) achetés $50\,000\text{ €}$ et revendus $100\,000\text{ €}$.
- **E —** Le PDG a laissé **$100\,000\text{ €}$** en compte courant d'associé du **1er janvier au 30 juin 2025** ($6\text{ mois}$), rémunérés au taux de **$6{,}55\%$** *(taux plafond fiscal TMP de l'exercice : **$4{,}55\%$**)*.
- **F —** La SA détient **$40\%$** de la **SNC DELTA** (société de personnes soumise à l'IR). En 2025, la SNC DELTA a réalisé un bénéfice fiscal de **$50\,000\text{ €}$**, mais n'a distribué aucun dividende : **aucune écriture** n'a été passée dans la comptabilité de la SA.
- **G —** La SA a versé et comptabilisé **$28\,000\text{ €}$** de jetons de présence (rémunération des administrateurs). La société compte **8 administrateurs** et la rémunération moyenne annuelle des **5 personnes les mieux rémunérées** est de **$60\,000\text{ €}$**.
- **H —** La SA a comptabilisé en charges un don de **$10\,000\text{ €}$** aux *Restaurants du Cœur* (mécénat d'entreprise éligible à l'Art. 238 bis CGI).

> [!note]- Rappel des plafonds CO2 ([[Art. 39 CGI\|Art. 39-4 CGI]])
> - $< 20\text{ g/km}$ : **$30\,000\text{ €}$**
> - $\ge 20\text{ g}$ et $< 50\text{ g/km}$ : **$20\,300\text{ €}$**
> - $\ge 50\text{ g}$ et $< 160\text{ g/km}$ : **$18\,300\text{ €}$**
> - $\ge 160\text{ g/km}$ : **$9\,900\text{ €}$**

### Travail demandé *(à remplir demain)*
1. Pour chaque opération (**A** à **H**), indique le **traitement fiscal** (règle + `+ réintégration`, `- déduction` ou `0 € / R.A.F.`). *(5 pts)*
2. Calcule le **résultat fiscal IS** de 2025, puis **liquide l'IS dû** *(taux normal / taux réduit PME ?, CSB de $3{,}3\%$ ?, réduction mécénat ?)*. *(2 pts)*

| Op. | Traitement juridique & justification | Réintégration (`+`) | Déduction (`−`) | R.A.F. (`0 €`) |
| :---: | :--- | :---: | :---: | :---: |
| **A** | | | | |
| **B** | | | | |
| **C** | | | | |
| **D** | | | | |
| **E** | | | | |
| **F** | | | | |
| **G** | | | | |
| **H** | | | | |
| **Total** | | | | |

- **Résultat fiscal IS 2025 :** `…`
- **Taux applicables & CSB :** `…`
- **IS net dû (après mécénat) :** `…`

---

## 3. Fiches du coffre utiles pour réviser
- **BIC :** [[Drive/Josepha/S3/fiscalité des entreprises/CM/Partie 2 - L_imposition des entreprises individuelles et des sociétés/Chapitre 1 - L_imposition des entreprises individuelles\|Chapitre 1 - L_imposition des entreprises individuelles]] · [[Drive/Josepha/S3/fiscalité des entreprises/TD/TD2 - l_imposition de l_entreprise individuelle\|TD2 - l_imposition de l_entreprise individuelle]] · [[TD Séance 3 - Fiscalité des entreprises\|TD Séance 3 - Fiscalité des entreprises]]
- **IS :** [[Drive/Josepha/S3/fiscalité des entreprises/CM/Partie 3 - L_impôt sur les sociétés/Chapitre 2 - L_assiette de l’IS\|Chapitre 2 - L_assiette de l’IS]] · [[Drive/Josepha/S3/fiscalité des entreprises/CM/Partie 3 - L_impôt sur les sociétés/Chapitre 3 - Le calcul de l_IS\|Chapitre 3 - Le calcul de l_IS]] · [[TD Séance 4 - L'impôt sur les sociétés\|TD Séance 4 - L'impôt sur les sociétés]] · [[Lexis 360/Fiscal/Lexis - L'impôt sur les sociétés\|Lexis - L'impôt sur les sociétés]]
- **IR (pour l'Exercice 3) :** [[Partie I - l'impot sur le revenu (IR)\|Partie I - l'impot sur le revenu (IR)]]
