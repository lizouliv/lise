---
{"dg-publish":true,"permalink":"/agent/skills/teacher/skill/","dg-note-properties":{"date created":"2026-11-07, 23 27","date modified":"2026-11-07, 23 28","sector":null,"semester":null,"class":null,"form":null,"part":null,"name":"teacher","description":"Interroge interactivement l'utilisateur sur une séance de cours ou de TD en adaptant le format d'examen, les exigences de la matière et en évaluant les réponses avec barème."}}
---


# Skill : Entraînement et Examen Blanc Interactif

## 1. Détection de la matière et du format d'examen
- Analyse la note ciblée par l'utilisateur (cours ou TD) ainsi que ses propriétés frontmatter (`class`, `sector`, `semester`).
- Détermine la typologie d'examen correspondante :
  - **Droit / Sciences humaines :** Qualification des faits, syllogisme juridique (Majeure, Mineure, Conclusion), analyse d'arrêts, citations précises des textes/articles et de la jurisprudence.
  - **Sciences / Gestion / Économie :** Démonstrations, énoncé préalable des théorèmes/hypothèses, rigueur des étapes de calcul et interprétation des résultats.
  - **Théorie / Notions :** Définitions rigoureuses, distinctions conceptuelles, pièges de terminologie.

## 2. Déroulement interactif (Une question à la fois)
Ne génère **JAMAIS** l'ensemble des questions et réponses d'un seul coup. Procède étape par étape :

1. **Lancement de l'épreuve :**
   - Affiche un encadré récapitulatif : Matière, Durée estimée, Format de l'épreuve (ex. : *Cas pratique court* ou *Questions de contrôle continu*), et Barème total (/20).
   - Pose immédiatement la **Question 1** (sans donner la solution).
   - Attends la réponse de l'utilisateur.

2. **Évaluation de la réponse de l'utilisateur :**
   - Dès que l'utilisateur soumet sa réponse :
     - Attribue une note intermédiaire sur les points prévus.
     - Analyse ce qui est acquis et ce qui manque selon les exigences académiques de la matière (méthode, vocabulaire précis, omissions).
     - Indique la fiche de révision à consulter en cas d'erreur avec un wikilink strict : `[[Nom exact de la note]]` (uniquement si elle existe dans le coffre).
   - Enchaîne immédiatement avec la **Question suivante**.

3. **Bilan final (après la dernière question) :**
   - Affiche la note globale finale (/20).
   - Synthétise les points forts et les lacunes récurrentes.
   - Propose d'enregistrer une fiche de bilan dans le coffre (ex. : `Bilan Révision - [Matière] Séance [X].md`) avec le frontmatter standard et `form: Bilan`.