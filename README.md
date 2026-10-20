# Field Scan - Surveillance et Diagnostic Automatisé de Bananeraies

**Field Scan** est un projet d'IA autonome visant à surveiller la santé et la croissance d'une plantation industrielle de bananiers à l'aide de l'imagerie satellite (Copernicus Sentinel-2) et de la vision par ordinateur (classification des maladies foliaires).

---

##  Objectifs du Projet
1. **Suivi Temporel & Stress Hydrique** : Analyse des variations de NDVI/NDMI entre la saison sèche et la saison des pluies (Sentinel-2, EPSG:32717).
2. **Comptage des Plants** : Détection et estimation du nombre de pieds de bananiers par parcelle.
3. **Diagnostic des Maladies** : Classification fine des pathologies foliaires (*Black Sigatoka*, *Cordana*, *Pestalotiopsis*, *Fusarium*) à partir de photos de terrain.

---

##  Structure du Dépôt

```text
Field-scan/
├── data_card.md          # Fiche de traçabilité des données et licences
├── requirements.txt      # Liste des dépendances Python
├── README.md             # Présentation et guide du projet
├── semaine_1_decouverte.ipynb  # Notebook d'exploration initial (Semaine 1)
└── src/                  # Modules Python (à venir)
