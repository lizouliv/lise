---
{"dg-publish":true,"permalink":"/script-ti-83-comptabilite-generale/","ctime":"2026-11-23T18:19:16.548+01:00","mtime":"2026-11-25T00:38:43.006+01:00","dg-note-properties":{"date created":"2026-11-23, 18 19","date modified":"2026-11-24, 21 08","sector":"[[References/AES]]","semester":"[[References/S3]]","class":"[[References/Compta]]","form":"[[References/TD]]","part":null}}
---


# Script TI-83 Premium CE (sans Python) : `COMPTA.8xp`

Programme TI-Basic tout-en-un (`26 227 octets`, compatible **TI-83 Premium CE** en français sans module Python) conçu pour le contrôle continu et le partiel de Comptabilité générale ([[cc compta\|cc compta]], [[Comptabilité financière\|Comptabilité financière]], [[Compta - Séance TD 2\|Compta - Séance TD 2]], [[Compta - Séance TD 3\|Compta - Séance TD 3]]).

> [!note] Périmètre CC (séances 1 à 4, sans TVA) vs Partiel
> Pour un sujet **sans TVA** (jusqu'à la séance 4 : écritures au journal, Bilan, Compte de résultat simplifié), saisis simplement **`0`** lorsque `TAUX TVA %(0=SANS)?` est demandé : le programme masque automatiquement les lignes de TVA et n'affiche que les écritures hors TVA. Les modules TVA (`445x`, CA3) et acomptes restent prêts pour les séances suivantes.

Il couvre les trois piliers de l'épreuve — **(1) Écritures au journal**, **(2) Bilan**, **(3) Compte de résultat simplifié** — ainsi que le passage bidirectionnel **Écritures $\leftrightarrow$ Tableaux** pour refaire les exercices de TD.

> [!tip] Fichiers prêts à l'emploi
> - **Fichier binaire prêt à transférer :** [[COMPTA.8xp\|COMPTA.8xp]] *(dans `Attachments/COMPTA TI-83/COMPTA.8xp`)*
> - **Code source TI-Basic lisible :** [[COMPTA_source_TI_Basic.txt\|COMPTA_source_TI_Basic.txt]] *(dans `Attachments/COMPTA TI-83/COMPTA_source_TI_Basic.txt`)*

---

## 1. Installation sur la TI-83 Premium CE

1. Installer et ouvrir **TI Connect CE** sur PC, puis brancher la calculatrice en USB.
2. Aller dans l'onglet **Explorateur de calculatrice** (icône de dossiers à gauche).
3. Glisser-déposer directement le fichier `Attachments/COMPTA TI-83/COMPTA.8xp` dans la fenêtre de **TI Connect CE** (destination : **RAM**, pour pouvoir l'exécuter).
4. Sur la calculatrice : appuyer sur `prgm`, sélectionner **`COMPTA`** puis `entrer` deux fois.

> [!note] Affichage en français, listes personnalisées et touche signe moins
> - Le fichier `.8xp` contient les jetons binaires natifs TI : sur une calculatrice réglée en français, les instructions s'affichent automatiquement en français (`EffÉcr`, `Si`, `Alors`, `Menu(`, `arrondi(`, `partEnt(`, etc.).
> - Lors de la saisie d'un **résultat déficitaire ou d'une variation négative** (ex. `-13000`), toujours utiliser la touche **`(-)`** en bas du clavier (et non la touche de soustraction `−`).
> - Pour le moteur **Écritures $\rightarrow$ Tableaux**, toujours démarrer un nouvel exercice par **`1:NOUVEL EXO (RAZ)`** afin d'initialiser les listes dédiées (`∟CPT`, `∟DEB`, `∟CRD`, `∟BIL`, `∟RES`).

---

## 2. Contenu détaillé du menu principal (`COMPTA`)

### 1 : Écritures au journal (`Lbl 10` à `16`)
- **1 : Sens D/C & Classement (`Lbl 11`) :** Saisir n'importe quel n° de compte PCG (`1` à `5` chiffres) et son sens d'évolution (`+` ou `-`). Gère automatiquement toutes les exceptions (`609`/`619`/`629`, `709`, `4091`/`4097`, `4191`/`4197`, `28`/`29`/`39`/`49`/`59`, `129`, `425`, `486`/`487`, `4456`/`4457`/`4458`, `519`) et indique **`PASSER AU DEBIT`** ou **`PASSER AU CREDIT`** ainsi que sa destination au **Bilan** ou au **Compte de résultat**.
- **2 : Écriture Achat / Vente (`Lbl 12`) :** Calcule et affiche les lignes exactes (`Débit` / `Crédit` et numéros de comptes) pour biens, prestations de services (`4458` si à crédit) et immobilisations (`21xx` incluant port/mise en service, `44562`, `404`, ou véhicule de tourisme TTC en `2182` sans TVA déductible), avec remise, port et escompte au comptant (`665`/`765`).
- **3 : Écriture Acompte & Solde (`Lbl 13`) :** Versement/réception d'acompte (`4091`/`4191` + régularisation TVA `4458`) et facture finale nette d'acompte.
- **4 : Écriture d'Avoir (`Lbl 14`) :** Avoirs sur RRR hors facture de doit (`609`/`709`), retours (`607`/`707`) et escomptes de règlement (`765`/`665`) à partir d'une base HT ou TTC (`4097`/`4197`).
- **5 : Emprunt / Salaires / Crédit-Bail (`Lbl 15`) :** Souscription (`164`, frais `627`), échéance (`164` + `661` / `512`), écritures complètes du bulletin de paie (`641`, `421`, `43x`, `645`, `425`) et redevance de crédit-bail (`612`).
- **6 : Vérif Équilibre Écriture (`Lbl 16`) :** Additionne à la volée les débits et crédits d'une écriture complexe et vérifie $\sum \text{Débit} = \sum \text{Crédit}$.

### 2 : Bilan simplifié (`Lbl 20` à `23`)
- **1 : Construire / Calculer Bilan (`Lbl 21`) :** Saisie structurée de l'**Actif immobilisé** (`20`, `21`, `26/27`), de l'**Actif circulant** (`3`, `4`, `50`, `512D/53`) et du **Passif** (`101`, `106`, `15`, `164`, `401/404`, autres dettes/découvert). Permet au choix de :
  - **trouver le Capital manquant** ($\text{Total Actif} - \text{Dettes} - \text{Réserves}$),
  - **trouver le Résultat par le Bilan** (double détermination),
  - **vérifier l'équilibre $\text{Actif} = \text{Passif}$**.
- **2 : Ouverture & Capital manquant (`Lbl 22`) :** Outil rapide pour les bilans de création d'entreprise.
- **3 : Mémo Structure Bilan (`Lbl 23`) :** Rappel de l'ordre de liquidité croissante (Actif) et d'exigibilité croissante (Passif) avec les principaux comptes.

### 3 : Compte de résultat simplifié (`Lbl 30` à `34`)
- **1 : Établir Compte de résultat simplifié (`Lbl 31`) :** Calcule les produits et charges par nature (Exploitation `I`/`II`, Financier `V`/`VI`, Exceptionnel `VII`/`VIII`, IS/Participation `IX+X`), avec calcul optionnel de la variation des stocks ($\text{SI} - \text{SF}$), et affiche les **4 résultats intermédiaires** (`1. Résultat d'exploitation`, `2. Résultat financier`, `3. Résultat courant avant impôts`, `4. Résultat exceptionnel`), `Total Produits`, `Total Charges` et **`Résultat Net` (Bénéfice ou Perte)**.
- **2 : Variation des stocks SI / SF (`Lbl 32`) :** Distinction $\text{SI} - \text{SF}$ en charge (`603x`) vs $\text{SF} - \text{SI}$ en produit (`713`), coût d'achat des marchandises vendues et écritures d'inventaire.
- **3 : VA & Soldes de gestion (`Lbl 33`) :** Consommation intermédiaire (`60 + 61 + 62`), Valeur Ajoutée (`CA - CI`), EBE (`VA - 63 - 64`) et taux de VA.
- **4 : Mémo Compte de résultat (`Lbl 34`) :** Rappel synthétique des classes 6 et 7 et pièges classiques.

### 4 : Partir des écritures $\rightarrow$ Tableaux (`Lbl 40` à `46`)
- **1 : Nouvel Exo (RAZ) (`Lbl 41`) & 2 : Ajouter Écriture (`Lbl 42`) :** Mini-moteur de journal complet : chaque écriture est contrôlée ($\text{Débit} = \text{Crédit}$) et agrégée automatiquement par numéro de compte dans les listes `∟CPT`, `∟DEB`, `∟CRD`.
- **3 : Ajouter Solde Direct (`Lbl 43`) :** Permet de saisir directement les soldes d'une Balance existante.
- **4 : Voir Balance & Grand Livre (`Lbl 44`) :** Trie automatiquement tous les comptes dans l'ordre du PCG (`101`, `164`, `2183`, `401`, `512`, `53`, `604`, `706`...), affiche mouvements et soldes compte par compte, puis vérifie les **3 égalités fondamentales de la Balance**.
- **5 : Générer CR & Bilan (`Lbl 45`) :** Ventile automatiquement chaque compte soldé dans le **Compte de résultat simplifié** et le **Bilan** (y compris `28/29/39/49` en déduction d'actif, `609`/`709` inversés, `409`/`419`, `512` créditeur basculé en découvert au Passif) et valide la **double détermination du résultat**.
- **6 : Impact d'une écriture sur les tableaux (`Lbl 46`) :** Saisir un compte débité, un compte crédité et un montant pour visualiser l'effet exact sur l'Actif, le Passif, les Charges, les Produits et le Résultat.

### 5 : Partir des tableaux $\rightarrow$ Écritures (`Lbl 50` à `54`)
- **1 : Bilan départ $\rightarrow$ Ouverture (`Lbl 51`) :** Génère l'écriture d'ouverture au journal (`01/01`) depuis une saisie manuelle ou directement depuis le Bilan en mémoire (`∟BIL`), avec calcul automatique du capital si absent.
- **2 : Variations Bilan N-1 / N $\rightarrow$ Écritures (`Lbl 52`) :** Reconstitue les écritures et flux entre deux bilans comparatifs (acquisitions/cessions d'immos, dotation aux amortissements `681`/`28`, annulation `SI` / constatation `SF`, encaissements clients, règlements fournisseurs, emprunts et trésorerie nette).
- **3 : CR $\rightarrow$ Clôture & Affectation (`Lbl 53`) :** Génère l'écriture de solde des comptes de gestion (`120` bénéfice ou `129` perte) depuis une saisie ou la mémoire (`∟RES`), puis l'écriture d'affectation du résultat (`1061`, `1068`, `457`, `110`).
- **4 : Impact tableaux $\rightarrow$ Écriture (`Lbl 54`) :** Vérifie la cohérence $(\Delta\text{Actif} + \Delta\text{Charges}) = (\Delta\text{Passif} + \Delta\text{Produits})$ et indique les masses à passer au Débit et au Crédit.

### 6 : Calculs & Mémos PCG (`Lbl 60` à `74`)
- **1 : Facture de Doit & `Net -> Brut` (`Lbl 61`) :** Saisie directe ou multi-lignes (`Qté × PU`), cascade Remise 1, Remise 2, Escompte, Port, TVA, Acompte $\rightarrow$ Net à payer, plus mode inverse **`Net -> Brut`** (retrouver le prix brut avant remises successives).
- **2 : Conversion `HT <-> TTC` (`Lbl 62`)** à taux libre (`20 %`, `10 %`, `5,5 %`, `2,1 %`).
- **3 : Déclaration de TVA / CA3 (`Lbl 63`) :** Depuis les bases HT ou les soldes des comptes `445x`, calcule la **TVA à décaisser (`44551`)** ou le **crédit à reporter (`44567`)** et affiche l'écriture de liquidation.
- **4 : Tableau d'emprunt — 3 modes (`Lbl 64`) :** Annuités constantes, amortissement constant ou *in fine*, échéance par échéance (`Cap début`, `Intérêts 661`, `Amortissement 164`, `Annuité 512`, `Cap fin` à `0` et cumul d'intérêts).
- **5 : Mémos & Plan de comptes (`Lbl 70` à `74`) :** Quatre fiches synthétiques adaptées à l'écran `26 × 10` :
  - **1 : Comptes de Bilan (Classes 1 à 5)**
  - **2 : Comptes de Gestion (Classes 6 et 7)**
  - **3 : Les 8 Principes comptables du PCG**
  - **4 : Règles de TVA & Pièges d'examen**

---

## 3. Rappel sur l'usage en examen
- Certains sujets de partiel et de contrôle continu mentionnent `Documents autorisés : plan comptable non annoté et calculatrice non programmée`. Vérifier systématiquement les consignes de l'épreuve le jour J et utiliser `COMPTA` pour refaire les exercices de TD, vérifier l'équilibre des journaux/balances et contrôler ses tableaux de synthèse.
