---
{"dg-publish":true,"permalink":"/entrainement-compta-ecritures-bilan-et-compte-de-resultat/","ctime":"2026-11-23T18:22:23.427+01:00","mtime":"2026-11-25T16:11:16.733+01:00","dg-note-properties":{"date created":"2026-11-23, 18 22","date modified":"2026-11-25, 16 11","sector":"[[References/AES]]","semester":"[[References/S3]]","class":"[[References/Compta]]","form":"[[References/TD]]","part":null}}
---


# Entraînement Compta — Écritures au journal, Bilan & Compte de résultat simplifié *(Séances 1 à 4)*

> [!abstract] Objectif de la fiche (préparation CC — Séances 1 à 4)
> Conformément aux consignes du CC ([[cc compta\|cc compta]]) et aux 4 premières séances de TD ([[Comptabilité financière\|Comptabilité financière]], [[Compta - Séance TD 2\|Compta - Séance TD 2]], [Séance 2 - TD Compta Générale Exercices.pdf](/img/user/S%C3%A9ance%202%20-%20TD%20Compta%20G%C3%A9n%C3%A9rale%20Exercices.pdf)) :
> - **Périmètre exact :** Opérations courantes, ouverture, immobilisations, emprunts, stocks, amortissements, Balance, Bilan et Compte de résultat simplifié.
> - **Les 3 piliers évalués :** **(1) Écritures au journal**, **(2) Bilan**, **(3) Compte de résultat simplifié**.
> - **Les deux sens demandés :**
>   - **Sens 1 :** *Partir des écritures au journal pour créer les tableaux* (Balance $\rightarrow$ Compte de résultat simplifié $\rightarrow$ Bilan + double détermination du résultat).
>   - **Sens 2 :** *Partir des tableaux (Bilan / Compte de résultat) pour créer ou reconstituer les écritures* (ouverture, variations $N-1 / N$, variation des stocks, dotations, clôture `120`/`129`, affectation du résultat).

---

## Mémo express : les 4 ponts entre Journal et Tableaux

1. **Journal $\rightarrow$ Compte de résultat simplifié (Classes `6` et `7`) :**
   - Comptes **`6`** (`60` à `69`) $\rightarrow$ **Charges** : `60` Achats & variation de stocks (`603`), `61/62` Services extérieurs, `63` Impôts & taxes, `64` Personnel, `65` Autres charges, `66` Charges financières (`661` intérêts), `67` Charges exceptionnelles (`671` amendes), `68` Dotations aux amortissements.
   - Comptes **`7`** (`70` à `79`) $\rightarrow$ **Produits** : `70` Ventes (`701`, `706`, `707`), `71` Production stockée, `74/75` Subventions / autres produits, `76` Produits financiers, `77` Produits exceptionnels.
   - **Variation des stocks de marchandises / MP (`603`) :** $\Delta S = \text{SI} - \text{SF}$ *(en charge ; négative si $\text{SF} > \text{SI}$, positive si $\text{SI} > \text{SF}$)*.
   - **Règle d'or :** *Les immobilisations (`2x`), emprunts (`164`), créances (`411`), dettes (`401`/`404`) et mouvements banque/caisse (`512`/`53`) ne vont **jamais** au Compte de résultat !*
2. **Journal $\rightarrow$ Bilan (Classes `1` à `5`) :**
   - **Actif :** Immos (`20` à `27`, diminuées des amortissements `28`), Stocks (`31`/`37`), Créances (`411`), Disponibilités (`512` débiteur, `53` Caisse).
   - **Passif :** Capitaux propres (`101` Capital, `106` Réserves, `+120` bénéfice ou `−129` perte), Dettes (`164` Emprunts, `401` Fournisseurs d'exploitation, `404` Fournisseurs d'immos, et **`512` créditeur / découvert bancaire** sans jamais compenser avec la Caisse ou un autre compte bancaire positif).
3. **Double détermination du résultat :**
   $$\text{Résultat (Compte de résultat)} = \text{Produits} - \text{Charges} = \text{Total Actif} - (\text{Passif hors Résultat})$$
4. **Tableaux $\rightarrow$ Écritures (formules clés de reconstitution) :**
   - **Ouverture (`01/01`) :** Débiter tous les comptes d'Actif / Créditer Capital + Dettes (et $\text{Capital manquant} = \text{Total Actif} - \text{Dettes}$).
   - **Encaissements clients :** $\text{Créances}_{N-1} + \text{Ventes} - \text{Créances}_N$.
   - **Paiements fournisseurs :** $\text{Fournisseurs}_{N-1} + \text{Achats} - \text{Fournisseurs}_N$.
   - **Clôture des comptes de gestion :** Débiter `7xx` (`Total Produits`) / Créditer `6xx` (`Total Charges`) + Créditer `120` (si bénéfice) ou Débiter `129` (si perte).

---

# PARTIE I — Reprise & adaptation des exercices de TD *(Séances 1 à 4)*

> [!tip] Conseil méthode
> Fais chaque exercice sur papier dans les conditions de l'examen (plan comptable non annoté et calculatrice simple), puis déplie le corrigé pour vérifier tes écritures, tes soldes et la double détermination du résultat.

---

## Exercice 1 (TD 1 — Ex 3.2) : Société *Passe et Repasse* *(Tableaux $\rightarrow$ Écritures $\rightarrow$ Tableaux)*

**Thèmes :** Écriture d'ouverture depuis un bilan de départ, enregistrement d'opérations courantes, emprunt (capital + intérêts), puis Compte de résultat simplifié et Bilan de clôture.

### Énoncé (repris du TD)
La société **Passe et Repasse**, spécialisée dans le nettoyage, le repassage et la livraison de linge, est créée le **1er octobre N**. Son bilan de départ se présente ainsi :

| ACTIF | Exercice N | PASSIF | Exercice N |
| :--- | :---: | :--- | :---: |
| **Immobilisations corporelles** | | **Capitaux propres** | |
| Matériel et outillage (`2154`) | 40 000 | Capital (`101`) | 100 000 |
| Matériel de transport (`2182`) | 70 000 | | |
| *Total de l'actif immobilisé* | *110 000* | *Total des capitaux propres* | *100 000* |
| **Actif circulant** | | **Dettes** | |
| Disponibilités — Banques (`512`) | 10 000 | Emprunt (`164`) | 20 000 |
| *Total de l'actif circulant* | *10 000* | *Total des dettes* | *20 000* |
| **TOTAL GÉNÉRAL DE L'ACTIF** | **120 000** | **TOTAL GÉNÉRAL DU PASSIF** | **120 000** |

**Opérations du premier trimestre (octobre à décembre N) :**
- **A –** Ventes de prestations de services (un tiers au comptant par chèque et le reste à crédit) : **120 000 €**
- **B –** Réception de la facture EDF : **3 480 €**
- **C –** Achats de produits d'entretien (non stockés) à crédit : **5 170 €**
- **D –** Paiement par chèque d'une insertion publicitaire : **1 900 €**
- **E –** Réparations et entretien des véhicules de livraison payés par chèque bancaire : **4 640 €**
- **F –** Prélèvement bancaire relatif à l'échéance de l'emprunt (dont **1 200 €** d'intérêts) : **3 600 €**
- **G –** Réception de chèques bancaires de la part de clients : **2 800 €**
- **H –** Retrait d'espèces à la banque pour alimenter la caisse : **1 500 €**
- **I –** Paiement de factures par chèques bancaires aux fournisseurs : **3 660 €**
- **J –** Paiement par virement bancaire d'une assurance multirisques : **4 500 €**
- **K –** Règlement par virements bancaires des salaires : **12 850 €**

### Travail à faire
1. À partir du Bilan de départ, passer l'écriture d'ouverture au Journal au `01/10/N`.
2. Enregistrer au Journal les opérations **A** à **K**.
3. Établir le **Compte de résultat simplifié** et le **Bilan au 31 décembre N** en vérifiant la double détermination du résultat.

> [!success]- Corrigé complet — Exercice 1 (*Société Passe et Repasse*)
> ### 1 & 2. Livre-Journal
>
> | Date / Op. | N° Compte | Intitulé des comptes | Débit (€) | Crédit (€) |
> | :---: | :---: | :--- | :---: | :---: |
> | **01/10** | `2154`<br>`2182`<br>`512`<br>`101`<br>`164` | Matériel et outillage<br>Matériel de transport<br>Banques<br>$\quad$Capital<br>$\quad$Emprunts auprès des étb. de crédit<br>*(Reprise du bilan d'ouverture au 01/10/N)* | 40 000<br>70 000<br>10 000 | <br><br><br>100 000<br>20 000 |
> | **A** | `512`<br>`411`<br>`706` | Banques ($\frac{1}{3} \times 120\,000$)<br>Clients ($\frac{2}{3} \times 120\,000$)<br>$\quad$Prestations de services | 40 000<br>80 000 | <br><br>120 000 |
> | **B** | `6061`<br>`401` | Fournitures non stockables (eau, énergie)<br>$\quad$Fournisseurs | 3 480 | <br>3 480 |
> | **C** | `6063`<br>`401` | Fournitures d'entretien et petit équipement<br>$\quad$Fournisseurs | 5 170 | <br>5 170 |
> | **D** | `623`<br>`512` | Publicité, publications, relations publiques<br>$\quad$Banques | 1 900 | <br>1 900 |
> | **E** | `615`<br>`512` | Entretien et réparations<br>$\quad$Banques | 4 640 | <br>4 640 |
> | **F** | `164`<br>`661`<br>`512` | Emprunts ($3\,600 - 1\,200$)<br>Charges d'intérêts<br>$\quad$Banques | 2 400<br>1 200 | <br><br>3 600 |
> | **G** | `512`<br>`411` | Banques<br>$\quad$Clients | 2 800 | <br>2 800 |
> | **H** | `53`<br>`512` | Caisse<br>$\quad$Banques | 1 500 | <br>1 500 |
> | **I** | `401`<br>`512` | Fournisseurs<br>$\quad$Banques | 3 660 | <br>3 660 |
> | **J** | `616`<br>`512` | Primes d'assurances<br>$\quad$Banques | 4 500 | <br>4 500 |
> | **K** | `641`<br>`512` | Rémunérations du personnel<br>$\quad$Banques | 12 850 | <br>12 850 |
> | **TOTAUX** | | **TOTAL DU LIVRE-JOURNAL** | **284 100** | **284 100** |
>
> **Soldes clés des comptes de tiers et trésorerie :**
> - `512 Banques` : $52\,800 - 32\,650 = \mathbf{20\,150\ \text{€}}$ (`SD`) ; `53 Caisse` : $\mathbf{1\,500\ \text{€}}$ (`SD`) $\Rightarrow$ Disponibilités = $\mathbf{21\,650\ \text{€}}$
> - `411 Clients` : $80\,000 - 2\,800 = \mathbf{77\,200\ \text{€}}$ (`SD`)
> - `401 Fournisseurs` : $(3\,480 + 5\,170) - 3\,660 = \mathbf{4\,990\ \text{€}}$ (`SC`)
> - `164 Emprunts` : $20\,000 - 2\,400 = \mathbf{17\,600\ \text{€}}$ (`SC`)
> - *(Balance : Total Mouvements $D = C = \mathbf{284\,100\ \text{€}}$ ; Total Soldes $D = C = \mathbf{242\,590\ \text{€}}$.)*
>
> ### 3. Compte de résultat simplifié au 31/12/N
>
> | Compte de résultat simplifié | Exercice N (€) |
> | :--- | :---: |
> | **Produits d'exploitation** — Prestations de services (`706`) | 120 000 |
> | **Total des produits d'exploitation (I)** | **120 000** |
> | **Charges d'exploitation** | |
> | Achats non stockés (`6061` + `6063` : $3\,480 + 5\,170$) | 8 650 |
> | Autres charges externes (`615` + `616` + `623` : $4\,640 + 4\,500 + 1\,900$) | 11 040 |
> | Rémunérations du personnel (`641`) | 12 850 |
> | **Total des charges d'exploitation (II)** | **32 540** |
> | **1. RÉSULTAT D'EXPLOITATION (I − II)** | **87 460** |
> | **Produits financiers (V)** | 0 |
> | **Charges financières (VI)** — Intérêts de l'emprunt (`661`) | 1 200 |
> | **2. RÉSULTAT FINANCIER (V − VI)** | **−1 200** |
> | **3. RÉSULTAT COURANT AVANT IMPÔTS (I − II + V − VI)** | **86 260** |
> | **Produits exceptionnels (VII)** / **Charges exceptionnelles (VIII)** | 0 / 0 |
> | **Total des produits (I + V + VII)** | **120 000** |
> | **Total des charges (II + VI + VIII)** | **33 740** |
> | **BÉNÉFICE NET DE L'EXERCICE** | **+86 260** |
>
> ### 4. Bilan au 31/12/N
>
> | ACTIF | Exercice N (€) | PASSIF | Exercice N (€) |
> | :--- | :---: | :--- | :---: |
> | **Actif immobilisé (corporel)** | | **Capitaux propres** | |
> | Matériel et outillage (`2154`) | 40 000 | Capital (`101`) | 100 000 |
> | Matériel de transport (`2182`) | 70 000 | **Résultat de l'exercice (Bénéfice)** (`120`) | **86 260** |
> | *Total de l'actif immobilisé* | *110 000* | *Total des capitaux propres* | *186 260* |
> | **Actif circulant** | | **Dettes** | |
> | Créances clients (`411`) | 77 200 | Emprunts (`164`) | 17 600 |
> | Disponibilités (`512` + `53` : $20\,150 + 1\,500$) | 21 650 | Dettes fournisseurs (`401`) | 4 990 |
> | *Total de l'actif circulant* | *98 850* | *Total des dettes* | *22 590* |
> | **TOTAL GÉNÉRAL DE L'ACTIF** | **208 850** | **TOTAL GÉNÉRAL DU PASSIF** | **208 850** |

---

## Exercice 2 (TD 1 — Ex 1.1 & 2.1 adaptés) : *M. Alméda* & *Société Pégase* *(Tableaux $\rightarrow$ Écritures)*

**Thèmes :** Retrouver le capital manquant et générer l'écriture d'ouverture (*M. Alméda*) ; établir le Compte de résultat simplifié avec variation des stocks $\text{SI} - \text{SF}$ et passer les écritures d'inventaire + clôture (*Société Pégase*).

### Énoncé (repris du TD)
**Partie A — Bilan de départ de M. Alméda (01/10/N) :**
M. Alméda crée une entreprise de vente de jouets en bois. Il emprunte **50 000 €** auprès de sa banque et acquiert un local (**95 000 €**), des rayonnages (**11 250 €**), du mobilier de bureau (**1 625 €**), du matériel de bureau et informatique (**12 000 €**), et un stock initial de jouets (**38 000 €**). Il dépose **16 200 €** sur le compte bancaire et **925 €** en caisse.
1. Déterminer le montant du capital social et présenter le Bilan simplifié de départ au `01/10/N`.
2. En déduire l'écriture de création au Journal.

**Partie B — Compte de résultat simplifié de la société Pégase (31/12/N) :**
Sur l'exercice N, la société Pégase (articles de sellerie) relève :
- Achats de marchandises : **430 000 €** ; Fournitures de bureau non stockées : **3 400 €** ; Chiffre d'affaires (ventes de marchandises) : **786 000 €**
- Eau, gaz, électricité : **18 600 €** ; Télécommunications : **22 600 €** ; Taxe d'apprentissage : **13 200 €**
- Salaires bruts : **32 000 €** ; Cotisations patronales : **15 800 €**
- Revenus de placements financiers : **5 730 €** ; Intérêts d'emprunt : **6 915 €**
- Dotations aux amortissements des immobilisations : **14 000 €**
- Stock initial de marchandises (`01/01/N`) : **85 000 €** ; Stock final de marchandises (`31/12/N`) : **98 000 €**.
1. Calculer la variation des stocks et présenter le **Compte de résultat simplifié** complet (`1. Résultat d'exploitation`, `2. Résultat financier`, `3. Résultat courant`, `Total Produits`, `Total Charges`, `Bénéfice/Perte`).
2. À partir de ce tableau, passer au Journal au `31/12/N` : les écritures d'inventaire de variation des stocks (`6037` / `37`), de dotation aux amortissements (`681` / `281`), puis l'écriture de clôture constatant le résultat (`120` ou `129`).

> [!success]- Corrigé complet — Exercice 2 (*Alméda* & *Pégase*)
> ### Partie A — M. Alméda
> 1. **Capital & Bilan d'ouverture :**
>    - Actif immobilisé : $95\,000 + 11\,250 + 1\,625 + 12\,000 = \mathbf{119\,875\ \text{€}}$
>    - Actif circulant : $38\,000 + 16\,200 + 925 = \mathbf{55\,125\ \text{€}}$
>    - **Total Actif** $= \mathbf{175\,000\ \text{€}}$ $\Rightarrow$ $\text{Capital} = 175\,000 - 50\,000 = \mathbf{125\,000\ \text{€}}$.
> 2. **Écriture d'ouverture au Journal (`01/10/N`) :**
>    - **Débit :** `213` Constructions (`95 000`), `2181` Agencements (`11 250`), `2183` Matériel bureau/info (`12 000`), `2184` Mobilier (`1 625`), `37` Stocks (`38 000`), `512` Banques (`16 200`), `53` Caisse (`925`) = **`175 000 €`**
>    - **Crédit :** `101` Capital (`125 000`), `164` Emprunts (`50 000`) = **`175 000 €`**.
>
> ### Partie B — Société Pégase
> 1. **Variation des stocks (`6037`) :** $\Delta S = \text{SI} - \text{SF} = 85\,000 - 98\,000 = \mathbf{-13\,000\ \text{€}}$ *(stockage $\Rightarrow$ vient en diminution des charges)*.
>
> | Compte de résultat simplifié | Exercice N (€) |
> | :--- | :---: |
> | **Produits d'exploitation** — Ventes de marchandises (`707`) | 786 000 |
> | **Total des produits d'exploitation (I)** | **786 000** |
> | **Charges d'exploitation** | |
> | Achats de marchandises (`607`) | 430 000 |
> | Variation des stocks de marchandises (`6037`) | −13 000 |
> | Achats non stockés (`606` : fournitures $3\,400$ + eau/gaz/élec $18\,600$) | 22 000 |
> | Autres charges externes — télécoms (`626`) | 22 600 |
> | Impôts et taxes — taxe d'apprentissage (`63`) | 13 200 |
> | Charges de personnel (`641` + `645` : $32\,000 + 15\,800$) | 47 800 |
> | Dotations aux amortissements (`681`) | 14 000 |
> | **Total des charges d'exploitation (II)** | **536 600** |
> | **1. RÉSULTAT D'EXPLOITATION (I − II)** | **249 400** |
> | **Produits financiers (V)** — Revenus de placements (`76`) | 5 730 |
> | **Charges financières (VI)** — Intérêts d'emprunt (`661`) | 6 915 |
> | **2. RÉSULTAT FINANCIER (V − VI)** | **−1 185** |
> | **3. RÉSULTAT COURANT AVANT IMPÔTS (I − II + V − VI)** | **248 215** |
> | **Total des produits (I + V)** | **791 730** |
> | **Total des charges (II + VI)** | **543 515** |
> | **BÉNÉFICE NET** | **+248 215** |
>
> 2. **Écritures d'inventaire & clôture (`31/12/N`) :**
>    - **D `6037` (`85 000`) / C `37` (`85 000`)** *(annulation SI)* ; **D `37` (`98 000`) / C `6037` (`98 000`)** *(constatation SF)*.
>    - **D `681` (`14 000`) / C `281` (`14 000`)** *(dotation amortissements)*.
>    - **Clôture :** **D `707` (`786 000`), D `76` (`5 730`), D `6037` (`13 000`) / C `607` (`430 000`), C `606..681` (`119 600`), C `661` (`6 915`), C `120` (`248 215`)**.

---

## Exercice 3 (TD 1 *Premiers enregistrements* — Ex 2) : *Entreprise Fernand* *(Écritures $\rightarrow$ Tableaux)*

**Thèmes :** Opérations de création et d'exploitation courante $\rightarrow$ Journal complet $\rightarrow$ Compte de résultat simplifié et Bilan de clôture *(résultat déficitaire `129`)*.

### Énoncé (repris du TD)
L'entreprise **Fernand** réalise les opérations suivantes :
1. Apport de **25 000 €** à la Banque de Dépôt du Centre par le propriétaire, M. Fernand.
2. Apports par M. Fernand d'un véhicule commercial de **12 500 €** et de matériel informatique pour **5 500 €**.
3. Achat à crédit au fournisseur MATBURO de meubles pour équiper les bureaux de la direction : **4 580 €**.
4. Paiement du loyer des locaux commerciaux à l'agence immobilière du Centre : **2 200 €** *(par banque)*.
5. Achat au fournisseur Dupont de marchandises *(à crédit)* pour **8 750 €**.
6. Retrait d'espèces sur le compte en banque pour alimenter la caisse : **1 300 €**.
7. Vente de marchandises au client Trouvé pour **5 670 €** ; paiement à 30 jours fin de mois.
8. Vente de marchandises à la cliente Pierrette pour **345 €** ; paiement en espèces.
9. Paiement par chèque bancaire du fournisseur MATBURO.
10. Paiement du client Trouvé par chèque.
11. Règlement par banque de la moitié de la dette au fournisseur Dupont.

### Travail à faire
1. Enregistrer les opérations **1** à **11** au Journal.
2. Dresser le **Compte de résultat simplifié** et le **Bilan de clôture**.

> [!success]- Corrigé complet — Exercice 3 (*Entreprise Fernand*)
> ### 1. Livre-Journal
>
> | Op. | N° Compte | Intitulé des comptes | Débit (€) | Crédit (€) |
> | :---: | :---: | :--- | :---: | :---: |
> | **1** | `512` / `101` | Banques / Capital | 25 000 | 25 000 |
> | **2** | `2182`, `2183` / `101` | Matériel de transport (12 500), Mat. info (5 500) / Capital | 18 000 | 18 000 |
> | **3** | `2184` / `404` | Mobilier / **Fournisseurs d'immobilisations** | 4 580 | 4 580 |
> | **4** | `613` / `512` | Locations / Banques | 2 200 | 2 200 |
> | **5** | `607` / `401` | Achats de marchandises / Fournisseurs | 8 750 | 8 750 |
> | **6** | `53` / `512` | Caisse / Banques | 1 300 | 1 300 |
> | **7** | `411` / `707` | Clients / Ventes de marchandises | 5 670 | 5 670 |
> | **8** | `53` / `707` | Caisse / Ventes de marchandises | 345 | 345 |
> | **9** | `404` / `512` | Fournisseurs d'immobilisations / Banques | 4 580 | 4 580 |
> | **10** | `512` / `411` | Banques / Clients | 5 670 | 5 670 |
> | **11** | `401` / `512` | Fournisseurs ($\frac{8\,750}{2}$) / Banques | 4 375 | 4 375 |
> | **TOT.** | | **TOTAL JOURNAL (= MOUVEMENTS BALANCE)** | **80 470** | **80 470** |
>
> *(Total Soldes Balance $D = C = \mathbf{53\,390\ \text{€}}$ — `512` SD `18 215`, `53` SD `1 645`, `401` SC `4 375`, `404` et `411` soldés.)*
>
> ### 2. Compte de résultat simplifié & Bilan
> - **Compte de résultat simplifié :** Produits `707` = `6 015 €` | Charges (`607` `8 750` + `613` `2 200`) = `10 950 €` $\Rightarrow$ **Perte nette (`129`) = `−4 935 €`**.
>
> | ACTIF | Montant (€) | PASSIF | Montant (€) |
> | :--- | :---: | :--- | :---: |
> | **Actif immobilisé** | | **Capitaux propres** | |
> | Matériel de transport (`2182`) | 12 500 | Capital (`101`) | 43 000 |
> | Matériel info (`2183`) + Mobilier (`2184`) | 10 080 | **Résultat de l'exercice (Perte `129`)** | **−4 935** |
> | *Total Actif immobilisé* | *22 580* | *Total Capitaux propres* | *38 065* |
> | **Actif circulant** | | **Dettes** | |
> | Disponibilités (`512`: $18\,215$ + `53`: $1\,645$) | 19 860 | Dettes fournisseurs (`401`) | 4 375 |
> | **TOTAL ACTIF** | **42 440** | **TOTAL PASSIF** | **42 440** |

---

## Exercice 4 (TD 1 *Premiers enregistrements* — Ex 1) : *Entreprise Véron* *(Écritures $\rightarrow$ Tableaux)*

**Thèmes :** Enregistrement au Journal (dont une immobilisation payée **moitié comptant / moitié à crédit**), Balance, Compte de résultat simplifié et Bilan.

### Énoncé (repris du TD)
L'entreprise **Véron** réalise les opérations suivantes au cours du mois d'octobre :
1. Emprunt de **110 000 €** à la Banque de Dépôt du Centre.
2. Achat de marchandises pour **3 500 €** payées par chèque au fournisseur Pierre.
3. Ventes de marchandises au client Paul ; paiement au comptant par chèque bancaire de **4 500 €**.
4. Achat de marchandises pour **15 000 €** au fournisseur Éric. Paiement à 30 jours fin de mois.
5. Virement de la banque pour alimenter la caisse en espèces pour **600 €**.
6. Ventes de marchandises à la cliente Nathalie pour **16 750 €**. Paiement à 30 jours fin de mois.
7. Remboursement partiel de l'emprunt pour **2 500 €** *(capital uniquement)* par prélèvement automatique sur le compte bancaire.
8. Achat d'une photocopieuse valant **6 500 €** au fournisseur Lemoulec ; paiement **moitié à crédit, moitié au comptant** par chèque bancaire.
9. Fin du mois : règlement par chèque bancaire du fournisseur Éric.
10. Encaissement du chèque de la cliente Nathalie.

### Travail à faire
1. Enregistrer les opérations **1** à **10** au Journal.
2. Établir la **Balance** (vérification des égalités), le **Compte de résultat simplifié** et le **Bilan de fin d'octobre**.

> [!success]- Corrigé complet — Exercice 4 (*Entreprise Véron*)
> ### 1. Livre-Journal
>
> | Op. | N° Compte | Intitulé des comptes | Débit (€) | Crédit (€) |
> | :---: | :---: | :--- | :---: | :---: |
> | **1** | `512` / `164` | Banques / Emprunts | 110 000 | 110 000 |
> | **2** | `607` / `512` | Achats de marchandises / Banques | 3 500 | 3 500 |
> | **3** | `512` / `707` | Banques / Ventes de marchandises | 4 500 | 4 500 |
> | **4** | `607` / `401` | Achats de marchandises / Fournisseurs | 15 000 | 15 000 |
> | **5** | `53` / `512` | Caisse / Banques | 600 | 600 |
> | **6** | `411` / `707` | Clients / Ventes de marchandises | 16 750 | 16 750 |
> | **7** | `164` / `512` | Emprunts / Banques | 2 500 | 2 500 |
> | **8** | `2183`<br>`404`<br>`512` | Matériel de bureau et informatique<br>$\quad$**Fournisseurs d'immobilisations** ($\frac{6\,500}{2}$)<br>$\quad$Banques ($\frac{6\,500}{2}$) | 6 500 | <br>3 250<br>3 250 |
> | **9** | `401` / `512` | Fournisseurs / Banques | 15 000 | 15 000 |
> | **10** | `512` / `411` | Banques / Clients | 16 750 | 16 750 |
> | **TOT.** | | **TOTAL JOURNAL (= MOUVEMENTS BALANCE)** | **191 100** | **191 100** |
>
> *(Total Soldes Balance $D = C = \mathbf{132\,000\ \text{€}}$ — `512` SD `106 400`, `53` SD `600`, `164` SC `107 500`, `404` SC `3 250`, `401` et `411` soldés.)*
>
> ### 2. Compte de résultat simplifié & Bilan
> - **Compte de résultat simplifié :** Produits `707` ($4\,500 + 16\,750 = \mathbf{21\,250\ \text{€}}$) − Charges `607` ($3\,500 + 15\,000 = \mathbf{18\,500\ \text{€}}$) = **Bénéfice Net (`120`) = `+2 750 €`**.
>
> | ACTIF | Montant (€) | PASSIF | Montant (€) |
> | :--- | :---: | :--- | :---: |
> | **Actif immobilisé** | | **Capitaux propres** | |
> | Matériel de bureau et info (`2183`) | 6 500 | Capital (`101`) | 0 |
> | | | **Résultat de l'exercice (`120`)** | **2 750** |
> | *Total Actif immobilisé* | *6 500* | *Total Capitaux propres* | *2 750* |
> | **Actif circulant** | | **Dettes** | |
> | Disponibilités (`512`: $106\,400$ + `53`: $600$) | 107 000 | Emprunts (`164`) | 107 500 |
> | | | Dettes sur immobilisations (`404`) | 3 250 |
> | **TOTAL ACTIF** | **113 500** | **TOTAL PASSIF** | **113 500** |

---

## Exercice 5 (TD 2 — Ex 4.1 inversé) : *Entreprise Guliver* à rebours *(Tableaux $\rightarrow$ Écritures)*

**Thèmes :** Reprise de [[Compta - Séance TD 2\|Compta - Séance TD 2]] en sens inverse — reconstituer des écritures uniquement à partir du Bilan initial, du Bilan final et du Compte de résultat simplifié.

### Énoncé
On dispose des trois tableaux de synthèse de l'agence **Guliver** :
- **Bilan au 01/01/N (création) :** Matériel bureau `2183` : $4\,000\text{ €}$, Mobilier `2184` : $6\,200\text{ €}$, Banques `512` : $4\,300\text{ €}$, Caisse `53` : $500\text{ €}$ | Capital `101` : $10\,000\text{ €}$, Emprunt `164` : $5\,000\text{ €}$.
- **Bilan au 31/01/N :** Matériel bureau `2183` : $7\,000\text{ €}$, Mobilier `2184` : $6\,200\text{ €}$, Créances clients `411` : $27\,000\text{ €}$, Disponibilités (`512` + `53`) : $9\,790\text{ €}$ | Capital `101` : $10\,000\text{ €}$, Résultat `120` : $17\,990\text{ €}$, Emprunts `164` : $5\,000\text{ €}$, Dettes fournisseurs `401` : $14\,000\text{ €}$, Dettes sur immos `404` : $3\,000\text{ €}$.
- **Compte de résultat de janvier N :** Prestations de services `706` : $44\,300\text{ €}$ | Achats de prestations `604` : $20\,000\text{ €}$, Autres charges externes : $2\,510\text{ €}$, Salaires `641` : $3\,800\text{ €}$ $\rightarrow$ Bénéfice = $17\,990\text{ €}$.

### Travail à faire
En comparant les deux Bilans et le Compte de résultat *(sans regarder le journal d'origine)* :
1. Passer l'écriture d'ouverture au `01/01/N`.
2. Reconstituer en écritures synthétiques : (a) l'acquisition d'immobilisation, (b) les ventes et encaissements clients, (c) les achats de prestations et règlements fournisseurs, (d) les charges externes et salaires payés. Vérifier que la trésorerie finale obtenue égale bien **$9\,790\ \text{€}$**.
3. Passer l'écriture de clôture soldant les charges et produits au `31/01/N`.

> [!success]- Corrigé complet — Exercice 5 (*Guliver inversé*)
> 1. **Ouverture (`01/01/N`) :** Débit `2183` ($4\,000$), `2184` ($6\,200$), `512` ($4\,300$), `53` ($500$) / Crédit `101` ($10\,000$), `164` ($5\,000$) — Total $15\,000\ \text{€}$.
> 2. **Reconstitution par variation des postes :**
>    - **(a) Acquisition d'immo :** $\Delta 2183 = 7\,000 - 4\,000 = +3\,000$ et $\Delta 404 = +3\,000$ $\Rightarrow$ **D `2183` : $3\,000$ / C `404` : $3\,000$**.
>    - **(b) Ventes & Encaissements clients :**
>      - Ventes totales : `44 300 €` (`C 706`).
>      - $\text{Encaissements reçus} = \text{Clients}_{01/01} + \text{Ventes} - \text{Clients}_{31/01} = 0 + 44\,300 - 27\,000 = \mathbf{17\,300\ \text{€}}$.
>      - Écriture synthétique : **D `512` ($17\,300$), D `411` ($27\,000$) / C `706` ($44\,300$)**.
>    - **(c) Achats & Règlements fournisseurs :**
>      - Achats : `20 000 €` (`D 604`).
>      - $\text{Paiements fournisseurs} = \text{Fourn}_{01/01} + \text{Achats} - \text{Fourn}_{31/01} = 0 + 20\,000 - 14\,000 = \mathbf{6\,000\ \text{€}}$.
>      - Écritures synthétiques : **D `604` ($20\,000$) / C `401` ($20\,000$)** puis **D `401` ($6\,000$) / C `512` ($6\,000$)**.
>    - **(d) Charges payées au comptant :** **D `606/613/623` ($2\,510$), D `641` ($3\,800$) / C `512/53` ($6\,310$)**.
>    - **Contrôle de la trésorerie finale :** $(4\,300 + 500) + 17\,300 - 6\,000 - 2\,510 - 3\,800 = \mathbf{9\,790\ \text{€}}$ *(exact !)*.
> 3. **Clôture (`31/01/N`) :** **D `706` ($44\,300$) / C `604` ($20\,000$), C `606/613/623` ($2\,510$), C `641` ($3\,800$), C `120` ($17\,990$)**.

---

# PARTIE II — Nouveaux exercices inédits *(basés sur les TD & la consigne)*

---

## Exercice 6 (Inédit — *Écritures $\rightarrow$ Tableaux*) : *Librairie L'Encre Normande*

**Thèmes :** Remise sur facture de doit, immo à crédit (`404`), stock initial / stock final ($\text{SI} > \text{SF}$), emprunt (`164` + `661`), amortissement (`681`/`2818`), **résultat déficitaire (`129`)** et **découvert bancaire (`512` créditeur au Passif, règle de non-compensation)**.

### Énoncé
Au **1er janvier N**, le bilan d'ouverture de la librairie **L'Encre Normande** comporte :
- Mobilier (`2184`) : **8 000 €** | Stock de marchandises (`37`) : **12 000 €** | Banques (`512`) : **3 000 €** | Caisse (`53`) : **1 000 €**
- Capital (`101`) : **14 000 €** | Emprunt (`164`) : **10 000 €**.

**Opérations de janvier N :**
- **05/01 :** Achat à crédit de livres (marchandises) : montant brut **18 000 €**, remise habituelle de **10 %**.
- **10/01 :** Acquisition à crédit d'un ordinateur de caisse : **2 400 €**.
- **14/01 :** Ventes de livres au comptant : **14 500 €** par virements bancaires et **1 500 €** en espèces.
- **18/01 :** Paiement par virement bancaire du loyer (**2 200 €**) et de la prime d'assurance (**900 €**).
- **22/01 :** Vente à crédit de manuels à un lycée : **9 500 €**.
- **25/01 :** Règlement partiel de fournisseurs de marchandises par virement : **14 000 €**.
- **28/01 :** Paiement des salaires par virement bancaire : **4 800 €**.
- **30/01 :** Prélèvement de l'échéance mensuelle d'emprunt : **2 500 €** *(dont **400 €** d'intérêts)*.
- **31/01 (Inventaire) :** Le stock final de marchandises est évalué à **9 500 €** et la dotation aux amortissements du matériel & mobilier s'élève à **1 100 €**.

### Travail à faire
1. Comptabiliser l'écriture d'ouverture, toutes les opérations de janvier N et les écritures d'inventaire au `31/01`.
2. Établir le **Compte de résultat simplifié** de janvier N.
3. Dresser le **Bilan au 31/01/N** *(attention particulière au solde de `512` Banques, aux amortissements `2818` et au résultat !)*.

> [!success]- Corrigé complet — Exercice 6 (*L'Encre Normande*)
> ### 1. Livre-Journal
>
> | Date | N° Compte | Intitulé des comptes | Débit (€) | Crédit (€) |
> | :---: | :---: | :--- | :---: | :---: |
> | **01/01** | `2184`<br>`37`<br>`512`<br>`53`<br>`101`<br>`164` | Mobilier<br>Stocks de marchandises<br>Banques<br>Caisse<br>$\quad$Capital<br>$\quad$Emprunts | 8 000<br>12 000<br>3 000<br>1 000 | <br><br><br><br>14 000<br>10 000 |
> | **05/01** | `607` / `401` | Achats de marchandises ($18\,000 \times 0{,}90$) / Fournisseurs | 16 200 | 16 200 |
> | **10/01** | `2183` / `404` | Matériel informatique / Fournisseurs d'immobilisations | 2 400 | 2 400 |
> | **14/01** | `512`, `53` / `707` | Banques (14 500), Caisse (1 500) / Ventes de marchandises | 16 000 | 16 000 |
> | **18/01** | `613`, `616` / `512` | Locations (2 200), Assurances (900) / Banques | 3 100 | 3 100 |
> | **22/01** | `411` / `707` | Clients / Ventes de marchandises | 9 500 | 9 500 |
> | **25/01** | `401` / `512` | Fournisseurs / Banques | 14 000 | 14 000 |
> | **28/01** | `641` / `512` | Rémunérations du personnel / Banques | 4 800 | 4 800 |
> | **30/01** | `164`, `661` / `512` | Emprunts (2 100), Charges d'intérêts (400) / Banques | 2 500 | 2 500 |
> | **31/01** | `6037` / `37` | Variation des stocks *(annulation SI)* / Stocks | 12 000 | 12 000 |
> | **31/01** | `37` / `6037` | Stocks *(constatation SF)* / Variation des stocks | 9 500 | 9 500 |
> | **31/01** | `681` / `2818` | Dotations aux amortissements / Amortissements | 1 100 | 1 100 |
> | **TOTAUX** | | **TOTAL JOURNAL (= MOUVEMENTS BALANCE)** | **115 100** | **115 100** |
>
> **Piège clé sur la trésorerie (`512` vs `53`) :**
> - `512 Banques` : Débit $17\,500$ − Crédit $24\,400$ = **Solde créditeur de `6 900 €`** (*découvert bancaire*!).
> - `53 Caisse` : **Solde débiteur de `2 500 €`**.
> - **Non-compensation :** La Caisse (`2 500 €`) reste à l'**Actif** et le découvert (`6 900 €`) va au **Passif (Dettes)** ! *(Total Soldes Balance $D = C = \mathbf{60\,000\ \text{€}}$.)*
>
> ### 2. Compte de résultat simplifié au 31/01/N
>
> | Compte de résultat simplifié | Exercice N (€) |
> | :--- | :---: |
> | **Produits d'exploitation** — Ventes de marchandises (`707`) | 25 500 |
> | **Total des produits d'exploitation (I)** | **25 500** |
> | **Charges d'exploitation** | |
> | Achats de marchandises (`607`) | 16 200 |
> | Variation des stocks (`6037` : $\text{SI } 12\,000 - \text{SF } 9\,500$) | +2 500 |
> | Autres charges externes (`613` + `616` : $2\,200 + 900$) | 3 100 |
> | Rémunérations du personnel (`641`) | 4 800 |
> | Dotations aux amortissements (`681`) | 1 100 |
> | **Total des charges d'exploitation (II)** | **27 700** |
> | **1. RÉSULTAT D'EXPLOITATION (I − II)** | **−2 200** |
> | **Charges financières (VI)** — Intérêts (`661`) | 400 |
> | **2. RÉSULTAT FINANCIER (V − VI)** | **−400** |
> | **3. RÉSULTAT COURANT AVANT IMPÔTS** | **−2 600** |
> | **Total des produits (I)** | **25 500** |
> | **Total des charges (II + VI)** | **28 100** |
> | **PERTE NETTE DE L'EXERCICE (`129`)** | **−2 600** |
>
> ### 3. Bilan au 31/01/N
>
> | ACTIF | Montant (€) | PASSIF | Montant (€) |
> | :--- | :---: | :--- | :---: |
> | **Actif immobilisé** | | **Capitaux propres** | |
> | Mobilier & mat. info. brut (`2184` + `2183`) : $10\,400$ | | Capital (`101`) | 14 000 |
> | *− Amortissements (`2818`)* : *−1 100* $\rightarrow$ **Net** | **9 300** | **Résultat de l'exercice (Perte `129`)** | **−2 600** |
> | *Total Actif immobilisé* | *9 300* | *Total Capitaux propres* | *11 400* |
> | **Actif circulant** | | **Dettes** | |
> | Stocks de marchandises (`37`) | 9 500 | Emprunts (`164`) | 7 900 |
> | Créances clients (`411`) | 9 500 | Dettes fournisseurs (`401`: $2\,200$) + immo (`404`: $2\,400$) | 4 600 |
> | Disponibilités — Caisse (`53` uniquement) | 2 500 | **Découvert bancaire (`512` créditeur)** | **6 900** |
> | *Total Actif circulant* | *21 500* | *Total Dettes* | *19 400* |
> | **TOTAL GÉNÉRAL DE L'ACTIF** | **30 800** | **TOTAL GÉNÉRAL DU PASSIF** | **30 800** |

---

## Exercice 7 (Inédit — *Écritures $\rightarrow$ Tableaux*, Synthèse CC) : *Atelier Bois & Design*

**Thèmes :** Sujet complet de niveau CC couvrant les **3 blocs** du Compte de résultat simplifié (Exploitation, Financier, Exceptionnel), une immo financée moitié comptant/moitié à crédit, une remise sur facture, du stockage ($\text{SF} > \text{SI}$), des amortissements (`681`/`2815`) et le Bilan complet.

### Énoncé
La menuiserie **Atelier Bois & Design** est créée le **01/12/N** avec les éléments initiaux suivants :
- Matériel industriel (`2154`) : **18 000 €** | Stock de matières premières (`31`) : **6 000 €** | Banques (`512`) : **26 000 €**
- Capital (`101`) : **40 000 €** | Emprunt bancaire (`164`) : **10 000 €**.

**Opérations de décembre N :**
- **03/12 :** Acquisition d'une scie numérique pour un prix brut de **8 000 €** avec une remise de **5 %** ; règlement **moitié par virement bancaire et moitié à crédit** (`60 jours`).
- **05/12 :** Achat à crédit de matières premières (bois) : montant brut **14 000 €**, remise de **10 %**.
- **08/12 :** Ventes de meubles fabriqués, encaissées au comptant par virement : **15 400 €**.
- **12/12 :** Paiement par virement bancaire du loyer de l'atelier (**2 100 €**) et de l'assurance multirisques (**650 €**).
- **15/12 :** Retrait d'espèces à la banque pour alimenter la caisse : **800 €**.
- **17/12 :** Achat de fournitures de bureau non stockées, payé en espèces : **250 €**.
- **20/12 :** Vente à crédit de meubles à un hôtel : **19 200 €**.
- **23/12 :** Paiement partiel de fournisseurs de matières premières par virement : **8 000 €**.
- **26/12 :** Réception d'un chèque d'un client en règlement partiel : **11 000 €**.
- **28/12 :** Paiement des salaires par virement bancaire : **5 900 €**.
- **29/12 :** Prélèvement bancaire de l'échéance d'emprunt : **2 300 €** *(dont **300 €** d'intérêts)*.
- **30/12 :** Encaissement d'intérêts de placement bancaire : **350 €** ; et paiement en espèces d'une amende routière : **150 €**.
- **31/12 (Inventaire) :** Le stock final de matières premières est évalué à **8 500 €**, et la dotation aux amortissements du matériel industriel s'élève à **2 200 €**.

### Travail à faire
1. Enregistrer l'ouverture, toutes les opérations de décembre et les écritures d'inventaire au **Journal**.
2. Établir le **Compte de résultat simplifié** complet (Exploitation, Financier, Exceptionnel).
3. Établir le **Bilan au 31/12/N** et vérifier la double détermination du résultat.

> [!success]- Corrigé complet — Exercice 7 (*Atelier Bois & Design*)
> ### 1. Livre-Journal
>
> | Date | N° Compte | Intitulé des comptes | Débit (€) | Crédit (€) |
> | :---: | :---: | :--- | :---: | :---: |
> | **01/12** | `2154`, `31`, `512` / `101`, `164` | Mat. indus (18 000), Stock MP (6 000), Banques (26 000) / Capital (40 000), Emprunt (10 000) | 50 000 | 50 000 |
> | **03/12** | `2154`<br>`512`<br>`404` | Matériel industriel ($8\,000 \times 0{,}95$)<br>$\quad$Banques ($\frac{7\,600}{2}$)<br>$\quad$Fournisseurs d'immobilisations ($\frac{7\,600}{2}$) | 7 600 | <br>3 800<br>3 800 |
> | **05/12** | `601` / `401` | Achats de matières premières ($14\,000 \times 0{,}90$) / Fournisseurs | 12 600 | 12 600 |
> | **08/12** | `512` / `701` | Banques / Ventes de produits finis | 15 400 | 15 400 |
> | **12/12** | `613`, `616` / `512` | Locations (2 100), Assurances (650) / Banques | 2 750 | 2 750 |
> | **15/12** | `53` / `512` | Caisse / Banques | 800 | 800 |
> | **17/12** | `6064` / `53` | Fournitures administratives / Caisse | 250 | 250 |
> | **20/12** | `411` / `701` | Clients / Ventes de produits finis | 19 200 | 19 200 |
> | **23/12** | `401` / `512` | Fournisseurs / Banques | 8 000 | 8 000 |
> | **26/12** | `512` / `411` | Banques / Clients | 11 000 | 11 000 |
> | **28/12** | `641` / `512` | Rémunérations du personnel / Banques | 5 900 | 5 900 |
> | **29/12** | `164`, `661` / `512` | Emprunts (2 000), Charges d'intérêts (300) / Banques | 2 300 | 2 300 |
> | **30/12** | `512` / `76` | Banques / Produits financiers | 350 | 350 |
> | **30/12** | `671` / `53` | Charges exceptionnelles (amende) / Caisse | 150 | 150 |
> | **31/12** | `6031` / `31` | Variation des stocks MP *(annulation SI)* / Stocks MP | 6 000 | 6 000 |
> | **31/12** | `31` / `6031` | Stocks MP *(constatation SF)* / Variation des stocks MP | 8 500 | 8 500 |
> | **31/12** | `681` / `2815` | Dotations aux amortissements / Amortissements mat. indus | 2 200 | 2 200 |
> | **TOTAUX** | | **TOTAL JOURNAL (= MOUVEMENTS BALANCE)** | **153 000** | **153 000** |
>
> *(Total Soldes Balance $D = C = \mathbf{96\,050\ \text{€}}$ — `512` SD `29 200`, `53` SD `400`, `411` SD `8 200`, `401` SC `4 600`, `404` SC `3 800`, `164` SC `8 000`, `2154` SD `25 600`, `2815` SC `2 200`, `31` SD `8 500`.)*
>
> ### 2. Compte de résultat simplifié au 31/12/N
>
> | Compte de résultat simplifié | Exercice N (€) |
> | :--- | :---: |
> | **Produits d'exploitation** — Ventes de produits finis (`701`) | 34 600 |
> | **Total des produits d'exploitation (I)** | **34 600** |
> | **Charges d'exploitation** | |
> | Achats de matières premières (`601`) | 12 600 |
> | Variation des stocks MP (`6031` : $\text{SI } 6\,000 - \text{SF } 8\,500$) | −2 500 |
> | Autres achats & charges externes (`6064` + `613` + `616` : $250 + 2\,100 + 650$) | 3 000 |
> | Rémunérations du personnel (`641`) | 5 900 |
> | Dotations aux amortissements (`681`) | 2 200 |
> | **Total des charges d'exploitation (II)** | **21 200** |
> | **1. RÉSULTAT D'EXPLOITATION (I − II)** | **13 400** |
> | **Produits financiers (V)** — Intérêts de placement (`76`) | 350 |
> | **Charges financières (VI)** — Intérêts d'emprunt (`661`) | 300 |
> | **2. RÉSULTAT FINANCIER (V − VI)** | **+50** |
> | **3. RÉSULTAT COURANT AVANT IMPÔTS (I − II + V − VI)** | **13 450** |
> | **Produits exceptionnels (VII)** | 0 |
> | **Charges exceptionnelles (VIII)** — Amende (`671`) | 150 |
> | **4. RÉSULTAT EXCEPTIONNEL (VII − VIII)** | **−150** |
> | **Total des produits (I + V + VII)** | **34 950** |
> | **Total des charges (II + VI + VIII)** | **21 650** |
> | **BÉNÉFICE NET DE L'EXERCICE (`120`)** | **+13 300** |
>
> ### 3. Bilan au 31/12/N
>
> | ACTIF | Montant (€) | PASSIF | Montant (€) |
> | :--- | :---: | :--- | :---: |
> | **Actif immobilisé** | | **Capitaux propres** | |
> | Matériel industriel brut (`2154`) : $25\,600$ | | Capital (`101`) | 40 000 |
> | *− Amortissements (`2815`)* : *−2 200* $\rightarrow$ **Net** | **23 400** | **Résultat de l'exercice (`120`)** | **13 300** |
> | *Total Actif immobilisé* | *23 400* | *Total Capitaux propres* | *53 300* |
> | **Actif circulant** | | **Dettes** | |
> | Stocks de matières premières (`31`) | 8 500 | Emprunts (`164`) | 8 000 |
> | Créances clients (`411`) | 8 200 | Dettes fournisseurs (`401`) | 4 600 |
> | Disponibilités (`512`: $29\,200$ + `53`: $400$) | 29 600 | Dettes sur immobilisations (`404`) | 3 800 |
> | *Total Actif circulant* | *46 300* | *Total Dettes* | *16 400* |
> | **TOTAL GÉNÉRAL DE L'ACTIF** | **69 700** | **TOTAL GÉNÉRAL DU PASSIF** | **69 700** |

---

## Exercice 8 (Inédit — *Tableaux $\rightarrow$ Écritures complet*) : *SARL Café des Docks*

**Thèmes :** Partir du **Bilan $N-1$**, du **Bilan $N$** et du **Compte de résultat simplifié $N$** pour reconstituer toutes les écritures au Journal (réouverture, affectation du résultat $N-1$, acquisition d'immo, dotations, variation de stocks, flux clients/fournisseurs/emprunt, clôture).

### Énoncé
Vous disposez des états de synthèse de la **SARL Café des Docks** *(aucune cession d'immobilisation durant N)* :

#### 1. Bilans comparatifs au 31/12/N-1 et au 31/12/N
| ACTIF (€) | N-1 | N | PASSIF (€) | N-1 | N |
| :--- | :---: | :---: | :--- | :---: | :---: |
| Matériel industriel brut (`2154`) | 30 000 | 42 000 | Capital social (`101`) | 25 000 | 30 000 |
| *− Amortissements cumulés (`2815`)* | *(−6 000)* | *(−11 000)* | Réserves (`106`) | 3 000 | 5 000 |
| **Matériel industriel Net** | **24 000** | **31 000** | Résultat de l'exercice (`120`) | 4 000 | 11 500 |
| Stocks de marchandises (`37`) | 8 000 | 10 500 | **Total Capitaux propres** | **32 000** | **46 500** |
| Créances clients (`411`) | 11 000 | 14 000 | Emprunts (`164`) | 12 000 | 9 000 |
| Banques (`512`) | 7 000 | 9 000 | Dettes fournisseurs (`401`) | 6 000 | 9 000 |
| **TOTAL ACTIF** | **50 000** | **64 500** | **TOTAL PASSIF** | **50 000** | **64 500** |

#### 2. Compte de résultat simplifié de l'exercice N
| Compte de résultat simplifié N | Montant (€) |
| :--- | :---: |
| Ventes de marchandises (`707`) | **85 000** |
| **Total Produits d'exploitation (I)** | **85 000** |
| Achats de marchandises (`607`) | 48 000 |
| Variation des stocks (`6037`) | −2 500 |
| Autres charges externes (`61/62`) | 9 000 |
| Charges de personnel (`64`) | 13 500 |
| Dotations aux amortissements (`681`) | 5 000 |
| **Total Charges d'exploitation (II)** | **73 000** |
| **1. RÉSULTAT D'EXPLOITATION (I − II)** | **12 000** |
| Charges financières — Intérêts (`661`) | 500 |
| **2. RÉSULTAT FINANCIER** | **−500** |
| **BÉNÉFICE NET (I − II − VI)** | **+11 500** |

**Renseignement complémentaire :** L'assemblée générale a affecté le résultat $N-1$ ($4\,000\ \text{€}$) ainsi : `5 %` en réserve légale (`1061`), `1 800 €` en autres réserves (`1068`), et le solde versé en dividendes par virement bancaire. L'augmentation de capital de $N$ a été réalisée par apport en numéraire versé en banque.

### Travail à faire
1. Passer l'écriture de réouverture au `01/01/N` d'après le Bilan $N-1$.
2. Passer l'écriture d'affectation du résultat $N-1$ et son versement en dividendes.
3. À partir des variations entre les deux Bilans et du Compte de résultat $N$, reconstituer et enregistrer :
   - l'acquisition de matériel industriel (payée au comptant par banque) ;
   - l'augmentation de capital ;
   - les écritures d'inventaire (annulation `SI`, constatation `SF`, dotation aux amortissements) ;
   - les flux d'encaissements clients, de paiements fournisseurs, de charges payées et de remboursement d'emprunt ;
   - vérifier que le solde final reconstitué de la banque égale bien **`9 000 €`**.
4. Passer l'écriture de clôture soldant les comptes de gestion de l'exercice $N$.

> [!success]- Corrigé complet — Exercice 8 (*SARL Café des Docks*)
> ### 1. Réouverture (`01/01/N`)
> - **Débit :** `2154` (`30 000`), `37` (`8 000`), `411` (`11 000`), `512` (`7 000`) = `56 000`
> - **Crédit :** `2815` (`6 000`), `101` (`25 000`), `106` (`3 000`), `120` (`4 000`), `164` (`12 000`), `401` (`6 000`) = `56 000`.
>
> ### 2. Affectation du résultat N-1 (`4 000 €`)
> - Réserve légale (`5 % × 4 000`) = `200 €` ; Autres réserves = `1 800 €` ; Dividendes = `4 000 − 200 − 1 800 = 2 000 €`.
> - **Écriture d'affectation :** **D `120` (`4 000`) / C `1061` (`200`), C `1068` (`1 800`), C `457` (`2 000`)**, puis paiement : **D `457` (`2 000`) / C `512` (`2 000`)**.
>
> ### 3. Reconstitution des opérations & flux de l'exercice N
> - **Acquisition matériel (`Δ 2154` brut = `42 000 − 30 000 = +12 000`) :** **D `2154` (`12 000`) / C `512` (`12 000`)**.
> - **Augmentation capital (`Δ 101` = `30 000 − 25 000 = +5 000`) :** **D `512` (`5 000`) / C `101` (`5 000`)**.
> - **Écritures d'inventaire (`31/12/N`) :**
>   - Annulation `SI` : **D `6037` (`8 000`) / C `37` (`8 000`)**
>   - Constatation `SF` : **D `37` (`10 500`) / C `6037` (`10 500`)** $\rightarrow$ solde `6037` créditeur = `−2 500 €` en charge !
>   - Dotation amortissements (`Δ 2815` = `11 000 − 6 000 = 5 000`) : **D `681` (`5 000`) / C `2815` (`5 000`)**.
> - **Ventes & Encaissements clients :**
>   - Ventes (`707`) : **D `411` (`85 000`) / C `707` (`85 000`)**
>   - Encaissements = $11\,000 + 85\,000 - 14\,000 = \mathbf{82\,000\ \text{€}}$ $\Rightarrow$ **D `512` (`82 000`) / C `411` (`82 000`)**.
> - **Achats & Paiements fournisseurs :**
>   - Achats (`607`) : **D `607` (`48 000`) / C `401` (`48 000`)**
>   - Paiements = $6\,000 + 48\,000 - 9\,000 = \mathbf{45\,000\ \text{€}}$ $\Rightarrow$ **D `401` (`45 000`) / C `512` (`45 000`)**.
> - **Autres charges payées :** **D `61/62` (`9 000`), D `64` (`13 500`) / C `512` (`22 500`)**.
> - **Échéance d'emprunt (`Δ 164` = `12 000 − 9 000 = −3 000` + `661` = `500`) :** **D `164` (`3 000`), D `661` (`500`) / C `512` (`3 500`)**.
> - **Contrôle de la trésorerie finale (`512`) :**
>   $$7\,000 + 82\,000 + 5\,000 - 2\,000 - 12\,000 - 45\,000 - 22\,500 - 3\,500 = \mathbf{9\,000\ \text{€}}\quad (\text{exactement le Bilan N !})$$
>
> ### 4. Clôture des comptes de gestion (`31/12/N`)
> - **D `707` (`85 000`), D `6037` (`2 500`) / C `607` (`48 000`), C `61/62` (`9 000`), C `64` (`13 500`), C `681` (`5 000`), C `661` (`500`), C `120` (`11 500`)** *(Total `87 500 = 87 500`)*.

---

## Exercice 9 (Inédit — Flash `Tableaux <-> Écritures` : 8 cas pratiques)

**Objectif :** Réflexe immédiat sur le lien entre écritures au journal, Bilan et Compte de résultat simplifié.

### Partie A — Partir de l'impact dans les Tableaux $\rightarrow$ Retrouver l'écriture au Journal
1. **Cas 1 :** À l'Actif, `Matériel informatique` augmente de `+3 000 €` ; au Passif, `Dettes sur immobilisations` augmente de `+3 000 €` ; le Compte de résultat est inchangé.
2. **Cas 2 :** Au Compte de résultat, `Charges d'intérêts` augmente de `+350 €` ; au Bilan, `Emprunts` diminue de `−1 200 €` et `Banques` diminue de `−1 550 €`.
3. **Cas 3 :** À l'Actif, `Stocks de marchandises` augmente de `+2 000 €` ; au Compte de résultat, la ligne `Variation des stocks` en Charges est de `−2 000 €` (le bénéfice augmente de `+2 000 €`).
4. **Cas 4 :** À l'Actif, `Banques` diminue de `−1 800 €` et `Caisse` augmente de `+1 800 €` ; le total Actif, le Passif et le Compte de résultat restent inchangés.

### Partie B — Partir de l'écriture au Journal $\rightarrow$ Donner l'impact exact sur le Bilan et le CR
5. **Cas 5 :** **D `681` (`1 500 €`) / C `2818` (`1 500 €`)**
6. **Cas 6 :** **D `401` (`6 000 €`) / C `512` (`6 000 €`)**
7. **Cas 7 :** **D `512` (`12 000 €`) / C `164` (`12 000 €`)**
8. **Cas 8 :** **D `486` Charges constatées d'avance (`500 €`) / C `616` Primes d'assurances (`500 €`)**

> [!success]- Corrigé complet — Exercice 9 (8 cas flash)
> ### Partie A — Tableaux $\rightarrow$ Écritures
> 1. **Cas 1 :** Acquisition d'immobilisation à crédit $\Rightarrow$ **D `2183` (`3 000`) / C `404` (`3 000`)**.
> 2. **Cas 2 :** Paiement d'une échéance d'emprunt $\Rightarrow$ **D `164` (`1 200`), D `661` (`350`) / C `512` (`1 550`)**.
> 3. **Cas 3 :** Hausse du stock final ($\text{SF} > \text{SI}$ de `2 000 €`) $\Rightarrow$ **D `37` (`2 000`) / C `6037` (`2 000`)**.
> 4. **Cas 4 :** Retrait d'espèces à la banque pour alimenter la caisse $\Rightarrow$ **D `53` (`1 800`) / C `512` (`1 800`)**.
>
> ### Partie B — Écritures $\rightarrow$ Tableaux
> 5. **Cas 5 (`D 681 / C 2818 : 1 500`) :** CR : **Charges `+1 500 €`** (Résultat `−1 500 €`) | Bilan : **Actif immobilisé net `−1 500 €`**, Capitaux propres (via Résultat) **`−1 500 €`**.
> 6. **Cas 6 (`D 401 / C 512 : 6 000`) :** CR : **aucun impact (`0 €`)** | Bilan : **Actif (Disponibilités) `−6 000 €`**, **Passif (Dettes fournisseurs) `−6 000 €`**.
> 7. **Cas 7 (`D 512 / C 164 : 12 000`) :** CR : **aucun impact (`0 €`)** | Bilan : **Actif (Disponibilités) `+12 000 €`**, **Passif (Emprunts) `+12 000 €`**.
> 8. **Cas 8 (`D 486 / C 616 : 500`) :** CR : **Charges `−500 €`** (Résultat **`+500 €`**) | Bilan : **Actif circulant (CCA `486`) `+500 €`**, Passif Capitaux propres (Résultat) **`+500 €`**.
