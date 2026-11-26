---
{"dg-publish":true,"permalink":"/script-ti-83-fiscalite-des-entreprises/","ctime":"2026-11-18T19:53:16.973+01:00","mtime":"2026-11-18T19:53:16.973+01:00","dg-note-properties":{"date created":"2026-11-18, 19 54","date modified":"2026-11-18, 19 54","sector":"[[References/AES]]","semester":"[[References/S3]]","class":"[[References/Fiscal]]","form":"[[References/TD]]","part":null}}
---


# Script TI-83 Premium CE (sans Python) : `FISCA.8xp`

Programme TI-Basic tout-en-un (`19 083 octets`, compatible **TI-83 Premium CE** en français sans module Python) couvrant l'ensemble des calculs et points de vigilance des séances 1 à 5 de TD ([[Drive/Josepha/S3/fiscalité des entreprises/TD/TD1 - l_impôt sur le revenu\|TD1 - l_impôt sur le revenu]], [[Drive/Josepha/S3/fiscalité des entreprises/TD/TD2 - l_imposition de l_entreprise individuelle\|TD2 - l_imposition de l_entreprise individuelle]], [[TD Séance 3 - Fiscalité des entreprises\|TD Séance 3 - Fiscalité des entreprises]], [[TD Séance 4 - L'impôt sur les sociétés\|TD Séance 4 - L'impôt sur les sociétés]], [[TD Séance 5 - La taxe sur la valeur ajoutée\|TD Séance 5 - La taxe sur la valeur ajoutée]]) ainsi que les exercices types de contrôle continu et de partiel.

> [!tip] Fichiers prêts à l'emploi
> - **Fichier binaire prêt à transférer :** [[FISCA.8xp\|FISCA.8xp]] *(dans `Attachments/FISCA TI-83/FISCA.8xp`)*
> - **Code source TI-Basic lisible :** [[FISCA_source_TI_Basic.txt\|FISCA_source_TI_Basic.txt]] *(dans `Attachments/FISCA TI-83/FISCA_source_TI_Basic.txt`)*

---

## 1. Installation sur la TI-83 Premium CE

1. Installer et ouvrir **TI Connect CE** sur PC, puis brancher la calculatrice en USB.
2. Aller dans l'onglet **Explorateur de calculatrice** (icône de dossiers à gauche).
3. Glisser-déposer directement le fichier `Attachments/FISCA TI-83/FISCA.8xp` dans la fenêtre de **TI Connect CE** (destination : **RAM**, pour pouvoir l'exécuter).
4. Sur la calculatrice : appuyer sur `prgm`, sélectionner **`FISCA`** puis `entrer` deux fois.

> [!note] Affichage automatique en français et touche signe moins
> - Le fichier `.8xp` contient les jetons binaires natifs TI : sur une calculatrice réglée en français, les instructions s'affichent automatiquement en français (`EffÉcr`, `Si`, `Alors`, `Menu(`, `arrondi(`, `partEnt(`, etc.).
> - Lors de la saisie d'un **résultat déficitaire ou négatif** (ex. `-100000`), toujours utiliser la touche **`(-)`** en bas du clavier (et non la touche de soustraction `−`).

---

## 2. Contenu détaillé du menu principal (`FISCA`)

### 1 : Impôt sur le revenu ([[Drive/Josepha/S3/fiscalité des entreprises/TD/TD1 - l_impôt sur le revenu\|TD 1]])
- **1 : Nombre de parts & Quotient familial (`Lbl 11`) :** Statut marital/PACS, parent isolé (`+0,5` / `+0,25`), enfants à charge pleine (`+0,5` puis `+1` dès le 3e) ou en garde alternée, demi-parts supplémentaires, et calcul du QF.
- **2 : Calcul complet de l'IR au barème (`Lbl 12`) :** Barème progressif **2026 (rev. 2025)** et **2025 (rev. 2024)**, calcul automatique du **plafonnement du quotient familial** (`1 807 €` / `4 262 €` isolé en 2026 ; `1 791 €` / `4 224 €` en 2025), **décote**, **TMI** et **taux moyen**.
- **3 : Dividendes — PFU vs Barème (`Lbl 13`) :** Compare le **PFU (`31,4 %` en 2026 ou `30 %` en 2025)** à l'**option barème progressif** (abattement `40 %` + prélèvements sociaux sur le brut) selon la TMI et affiche l'économie réalisée.
- **4 : Revenus catégoriels (`Lbl 14`) :**
  - *Traitements & Salaires :* Abattement `10 %` vs frais réels (rappel exonération étudiante $\le 5\,405\text{ €}$).
  - *BNC :* Micro-BNC (`-34 %`, min `305 €`, seuil `77 700 €`) vs déclaration contrôlée.
  - *Revenus fonciers :* Micro-foncier (`-30 %`, seuil `15 000 €`) vs réel, avec ventilation automatique du **déficit foncier** (imputation sur le revenu global plafonnée à `10 700 €` hors intérêts d'emprunt ; report sur 10 ans pour le surplus et les intérêts).
- **5 : Plus-value immobilière & Surtaxe (`Lbl 15`) :** Abattements progressifs IR (`22 ans`) et prélèvements sociaux (`30 ans`), calcul de l'IR (`19 %`), des PS (`17,2 %` ou `18,6 %`) et de la **surtaxe de l'article 1609 nonies G du CGI** (au-delà de `50 000 €`, hors terrains à bâtir).

### 2 : Stocks & Plus-values professionnelles ([[Drive/Josepha/S3/fiscalité des entreprises/TD/TD2 - l_imposition de l_entreprise individuelle\|TD 2]])
- **1 : Stocks CUMP vs PEPS/FIFO (`Lbl 21`) :** Saisie de `N` lots d'achat (du plus ancien au plus récent), calcul du CUMP unitaire, de la valorisation CUMP (exacte et arrondie à 2 décimales), de la valorisation PEPS/FIFO, et identification de la méthode qui **minore le résultat fiscal**.
- **2 : Cession d'immobilisation (`Lbl 22`) :** Calcul de la **VNC**, de la plus ou moins-value et qualification automatique **Court Terme (CT) / Long Terme (LT)** (biens amortissables vs non amortissables, seuil de 2 ans).
- **3 : Cession de titres de portefeuille en FIFO (`Lbl 23`) :** Saisie de `N` lots par ancienneté, application automatique du FIFO et ventilation en CT / LT.
- **4 : Compensation PV/MV & Résultat fiscal (`Lbl 24`) :** Compensation nette CT/LT, option d'**étalement sur 3 ans** de la PVNCT (`-2/3` en N), réintégration d'un tiers antérieur, calcul de l'impôt sur PVNLT, et simulation de l'**imputation de la PVNLT sur le déficit fiscal**.

### 3 : Amortissements, Véhicules, CCA & SNC ([[TD Séance 3 - Fiscalité des entreprises\|TD 3]])
- **1 : Plan d'amortissement linéaire (`Lbl 31`) :** Prorata temporis en **jours sur 360** à partir de la date de mise en service (DMS), affichage année par année (base, taux, prorata, annuité, cumul, VNC finale à `0`).
- **2 : Plan d'amortissement dégressif (`Lbl 32`) :** Coefficient fiscal automatique (`1,25` pour 3–4 ans ; `1,75` pour 5–6 ans ; `2,25` pour $> 6$ ans), prorata en mois depuis le **1er jour du mois d'acquisition**, et **basculement automatique** au quotient linéaire (`BASC!`) dès que $\frac{100}{\text{années restantes}} \ge \text{taux dégressif}$.
- **3 : Véhicule de tourisme CO2 (`Lbl 33`) :** Plafonds WLTP de l'article 39-4 du CGI (`30 000 €` si $< 20\text{ g}$, `20 300 €` si $< 50\text{ g}$, `18 300 €` si $< 160\text{ g}$, `9 900 €` si $\ge 160\text{ g}$, ou plafond manuel), dotation comptable, dotation fiscale et **réintégration** en année 1 (proratisée) et en année pleine.
- **4 : Intérêts des comptes courants d'associés (`Lbl 34`) :** Supporte **plusieurs périodes/soldes** dans l'exercice, vérifie la libération intégrale du capital et le plafond au TMP, et calcule l'excédent à réintégrer.
- **5 : Société de personnes / SNC — Art. 8 CGI (`Lbl 35`) :** Calcule le résultat fiscal de la SNC, le bénéfice résiduel à répartir, puis le **revenu BIC imposable** et le **RCM** de chaque associé selon son pourcentage de parts et ses rémunérations/CCA propres.
- **6 : Outils Provision créance & Pas-de-porte (`Lbl 36`) :**
  - *Provision créance douteuse :* Calcule la dotation maximale justifiée nette de la provision antérieure et la réintégration/déduction.
  - *Droit d'entrée (bail commercial) :* Compare le droit d'entrée à l'économie de loyer sur la durée du bail, calcule l'étalement annuel déductible et la réintégration si comptabilisé en charge.

### 4 : Impôt sur les sociétés ([[TD Séance 4 - L'impôt sur les sociétés\|TD 4]])
- **1 : Liquidation de l'IS (`Lbl 41`) :** Taux réduit PME **`15 %`** ($\le 42\,500\text{ €}$), taux normal **`25 %`**, taux réduit brevets Nexus **`10 %`**, **CSB `3,3 %`** (si $\text{CA} \ge 7{,}63\text{ M€}$ et $\text{IS brut} > 763\,000\text{ €}$), **réduction mécénat** (`60 %` / `40 %`, plafond $\max(20\,000\text{ €} ; 0{,}5\% \text{ CA})$ avec réintégration auto du don si non déjà faite) et crédits d'impôt.
- **2 : Acomptes trimestriels d'IS & Solde (`Lbl 42`) :** Calcul des 4 échéances (`15/03`, `15/06`, `15/09`, `15/12`) avec arrondi légal de l'art. 1668 du CGI (`0,50 €` arrondi à `1 €`), **régularisation automatique au 2e acompte du 15 juin**, et solde de liquidation du `15/05`.
- **3 : Outils IS (`Lbl 43`) :** Régime mère-fille (QPFC `5 %` ou `1 %`), cession de titres de participation $\ge 2\text{ ans}$ (QPFC `12 %`), et plafond des **jetons de présence** (`5 % × moyenne 5/10 meilleurs salaires × nb administrateurs`).
- **4 : Déficits à l'IS (`Lbl 44`) :** Plafond du report en avant (`1 M€ + 50 %` au-delà) et créance de **carry-back** (`25 %` dans la limite de `1 M€` et du bénéfice imposé N-1).

### 5 : Taxe sur la valeur ajoutée ([[TD Séance 5 - La taxe sur la valeur ajoutée\|TD 5]])
- **1 : Conversion rapide `HT <-> TTC` (`Lbl 51`)** à taux libre (`20 %`, `10 %`, `5,5 %`, `2,1 %`).
- **2 : Assistant liquidation CA3 (`Lbl 52`) :** Saisie du crédit de TVA antérieur, boucle multi-opérations (`Collectée`, `Déductible` avec coefficient, `Autoliquidation` import/AIC) avec affichage du solde intermédiaire en temps réel et calcul final de la **TVA nette à payer** ou du **crédit à reporter**.
- **3 : Coefficient de déduction — Art. 206 ann. II CGI (`Lbl 53`) :** Calcul optionnel du prorata de taxation et **arrondi officiel par excès au centième** sur chaque coefficient intermédiaire et sur le produit final.
- **4 : Régularisations sur immobilisations — Art. 207 ann. II CGI (`Lbl 54`) :**
  - *Régularisation annuelle :* Vérifie le seuil de variation $> 0{,}10$ et calcule le complément ou le reversement (`/5` meuble ou `/20` immeuble).
  - *Régularisation globale (cession) :* Calcule les années restantes et le reversement (cession exonérée) ou le complément de déduction (cession taxée).

### 6 : Mémos & Pièges d'examen (`Lbl 60` à `64`)
Quatre fiches synthétiques consultables directement sur l'écran `26 × 10` de la calculatrice :
- **1 : IR / Micro / PFU**
- **2 : Amortissements / Plafonds CO2 / CCA**
- **3 : IS / PME / CSB / Titres de participation**
- **4 : TVA — Règles d'exigibilité, territorialité & pièges classiques**

---

## 3. Rappel sur l'usage en examen
- Certains sujets de partiel (ex. session décembre 2025) mentionnent `Documents autorisés : calculette non programmable`, tandis que certains contrôles continus mentionnent `calculette`. Vérifier systématiquement les consignes de l'épreuve le jour J et utiliser `FISCA` pour préparer les séances de TD, vérifier ses tableaux d'amortissement et s'entraîner sur les annales.
